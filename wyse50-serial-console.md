# Giving a Wyse 50 terminal a login session from a Mac

A complete, from-scratch explanation. No prior knowledge of serial ports,
terminals, or macOS internals assumed.

This document replaces an earlier, terser version of itself — everything from
that draft is here, with the background filled in.

---

## Part 1 — What we were actually trying to do

### What a "dumb terminal" is

A Wyse 50 (early 1980s) looks like a computer but isn't one. It has no CPU
running your programs, no operating system, no disk, no network. It does exactly
two things:

1. When you press a key, it sends one or more bytes out a cable.
2. When bytes arrive on that cable, it paints them on the screen.

That's the whole device. It's a keyboard and a screen on the end of a wire.

So "give the Wyse a terminal session" cannot mean installing anything on the
Wyse. It means: **something running on the Mac has to sit at the other end of
that wire, read the bytes the Wyse sends, run a shell, and send the output
back.** The Wyse is a window into a program running on the Mac.

### What "a login session" needs

When you open Terminal.app on your Mac, a lot is quietly arranged for you:

- A **shell** (`zsh`) runs your commands.
- A **terminal device** connects the shell to your screen and keyboard, and
  handles line editing (backspace, `Ctrl-C`, etc.).
- A **login** step establishes who you are, sets up your environment, and
  records the session.

For the Wyse we have to build all three of those explicitly, because nothing
does it for us.

---

## Part 2 — Background you need

### Serial ports and RS-232

The cable between the Wyse and the Mac is **RS-232 serial**. "Serial" means the
bits go one after another down a single wire, rather than side by side. The
essential wires:

| Wire | Purpose |
|---|---|
| **TxD** | Transmit data — this end talks |
| **RxD** | Receive data — this end listens |
| **GND** | Ground, the shared voltage reference |

Some cables also carry "modem control" wires that signal presence and readiness
rather than data — **DTR** (Data Terminal Ready), **DCD** (Data Carrier Detect),
**RTS**/**CTS** (Request/Clear To Send). They matter later.

### Line settings: what "9600 8N1" means

Both ends must agree on how to interpret the bit stream, or you get garbage.

- **9600** — baud, i.e. signal changes per second. With 8N1 framing each byte
  costs 10 bits, so 9600 baud ≈ **960 characters per second**. For scale: filling
  an 80×24 screen (1,920 characters) takes about two seconds. This is why
  full-screen redraws visibly crawl.
- **8** — eight data bits per character.
- **N** — no parity bit (no error-checking bit).
- **1** — one stop bit marking the end of each character.

Get these wrong and you don't get silence, you get **garbage** — recognizable
characters in the wrong places. That distinction is a useful diagnostic:
silence means nothing is arriving; garbage means bytes arrive misframed.

### DTE, DCE, and why you need a "null modem"

RS-232 was designed for a computer/terminal talking to a **modem**. So devices
come in two roles:

- **DTE** (Data Terminal Equipment) — computers and terminals. Transmits on TxD.
- **DCE** (Data Communication Equipment) — modems. Transmits on RxD.

A normal straight-through cable assumes you're connecting DTE to DCE, so the
wires run pin-to-pin.

Here's the catch: **the Wyse 50 is DTE, and a USB-serial adapter is also DTE.**
Connect them with a straight cable and both ends transmit on the same wire while
both listen on the other — total silence in both directions.

A **null modem** cable or adapter crosses TX and RX (and usually the handshake
pairs), making one end look like a modem to the other. You need one here. Pin
numbers differ by connector:

| Signal | DB25 (Wyse) | DB9 (USB adapter) |
|---|---|---|
| TxD | 2 | 3 |
| RxD | 3 | 2 |
| GND | 7 | 5 |

### Flow control: the concept that dominates this whole setup

The Mac can generate output far faster than the Wyse can paint it. The Wyse has
a small input buffer. When that buffer fills, the incoming bytes have nowhere to
go and are **dropped** — you see garbled, partial output.

**Flow control** is how the slow end says "stop, I'm full" and later "go ahead."
Two mechanisms:

- **Software flow control (XON/XOFF)** — the receiver sends special bytes in the
  reverse direction over the same data wires:
  - **XOFF** = `0x13` (also known as `DC3`, or `Ctrl-S`) — *stop sending*
  - **XON** = `0x11` (`DC1`, `Ctrl-Q`) — *resume*
- **Hardware flow control (RTS/CTS)** — uses dedicated wires instead of data
  bytes. More reliable, but only works if your cable actually has those wires.
  Many null modems are wired with just three (TX/RX/GND).

We use XON/XOFF, because we can't assume the cable carries RTS/CTS.

**The hazard**, which caused hours of confusion here: XON/XOFF is *stateful*. If
the terminal sends XOFF and then never sends XON — because it got powered off,
say — the Mac stays muted **forever**. The "stopped" flag lives in the Mac's
kernel, so power-cycling the terminal doesn't clear it. Everything looks healthy
and nothing appears on screen.

### Terminals aren't all the same: `TERM` and terminfo

To move the cursor or clear the screen, a program sends **escape sequences** —
byte sequences starting with `ESC` (`0x1B`) that mean commands rather than
characters. Different terminals use different sequences.

Modern terminals speak **ANSI/VT100**, e.g. `ESC[2J` clears the screen. The Wyse
50 predates that standard and uses its own: `ESC+` clears the screen, `ESC G n`
sets video attributes.

Unix solves this with **terminfo**, a database describing each terminal's
capabilities. Programs look up the right sequences instead of hardcoding them.
You select the entry with the `TERM` environment variable. macOS ships a `wy50`
entry already (`/usr/share/terminfo/77/wy50`), so we set `TERM=wy50`.

Two things break this: software that hardcodes ANSI instead of consulting
terminfo (we hit exactly that), and software emitting UTF-8, which the Wyse also
predates.

### What `getty` is, and why macOS makes this awkward

Historically, Unix ran a **getty** ("get tty") process on each terminal line. Its
job: open the line, print `login:`, and hand off to `/usr/bin/login`. When a
session ended, the system started a fresh getty, so a new prompt appeared. That
respawn behavior is exactly what we want.

On Linux you'd get this in one command, because `agetty` exists and systemd ships
a unit template for serial lines:

```
systemctl enable serial-getty@ttyUSB0.service
```

**macOS has no systemd.** Its equivalent init/service manager is **launchd**
(PID 1). And macOS has no `agetty`; while `/usr/libexec/getty` and `/etc/ttys`
still exist as historical artifacts, launchd no longer drives serial lines from
`/etc/ttys` — in practice that file only covers the console. So there is no
built-in way to do this, and the pieces get assembled by hand.

### Pseudo-terminals (ptys)

`login` and `zsh` expect a **terminal device** with line editing, job control,
and signals (`Ctrl-C`). A raw serial port isn't quite that.

A **pseudo-terminal** (pty) is a software terminal: a pair of endpoints where
whatever is written to one comes out the other. The shell attaches to one side
believing it's a normal terminal; our bridge program holds the other side and
forwards to the serial port.

### What `socat` is

`socat` ("SOcket CAT") connects two arbitrary byte streams and copies data
between them. It can open a serial port, allocate a pty, run a program attached
to it, and shuttle bytes — which is precisely the plumbing we need.

---

## Part 3 — The architecture we built

```
   ┌──────────┐
   │ Wyse 50  │  keyboard + screen, no OS
   └────┬─────┘
        │  RS-232, 9600 8N1, null modem, DB25 ↔ DB9
   ┌────▼──────────────┐
   │ FTDI USB adapter  │  driver built into macOS
   └────┬──────────────┘
        │  appears as /dev/cu.usbserial-FTEL78JL
   ┌────▼───────────────────────────────────┐
   │ socat            (root, run by launchd)│
   │  • owns the serial port                │
   │  • creates a pty                       │
   │  • copies bytes both directions        │
   └────┬───────────────────────────────────┘
        │  pty
   ┌────▼──────────────────────────┐
   │ /usr/local/sbin/wyse50-login  │  our getty-equivalent
   │  • sets tty modes + 24x80     │
   │  • sets TERM=wy50, LANG=C     │
   │  • prints a banner            │
   └────┬──────────────────────────┘
        │  exec
   ┌────▼──────────────┐
   │ /usr/bin/login -p │  authenticates you
   └────┬──────────────┘
        │
   ┌────▼─────┐
   │   zsh    │  your shell
   └──────────┘
```

launchd supervises socat. When you log out, socat exits, launchd starts a new
one, and you get a fresh `login:` — reproducing getty's respawn.

---

## Part 4 — Hardware

| Piece | Value |
|---|---|
| Adapter | FTDI FT232-class USB→RS-232. macOS has the driver built in; no kext. |
| Device node | `/dev/cu.usbserial-FTEL78JL` |
| Cable | **Null modem** — both ends are DTE |
| Jack on the Wyse | **MAIN** (not AUX/PRINTER — that's for a printer) |
| Line settings | 9600 baud, 8 data bits, no parity, 1 stop bit |
| Handshake | XON/XOFF, set on the terminal |

### Why the device name looks like that

`FTEL78JL` is the FTDI chip's own serial number, burned into the adapter. Handy —
the path is stable across reboots and USB ports for *that* adapter. But it's
hardcoded in our config, so a different adapter means a different path.

### `/dev/cu.*` versus `/dev/tty.*`

macOS exposes **two** device nodes for one serial port:

- **`/dev/tty.*`** — the "dial-in" node. Opening it **blocks** until the DCD
  (carrier) wire is asserted. Designed for waiting on an incoming call.
- **`/dev/cu.*`** — the "call-out" node. Opens immediately, ignoring DCD.

We use `cu.*` together with the `clocal=1` setting, which together mean **the Mac
never looks at the modem control wires.** That was the safe choice, since we
don't know whether your null modem carries DTR/DCD at all. It has consequences —
see Part 8.

---

## Part 5 — The files, explained line by line

### 1. `/Library/LaunchDaemons/local.wyse50-getty.plist`

A **LaunchDaemon** is a system-wide background service, run by launchd as root,
started at boot, independent of anyone being logged into the GUI. The file must
be owned by `root:wheel` with mode `644` or launchd refuses it.

```xml
<key>Label</key><string>local.wyse50-getty</string>
```
The service's unique name; how you refer to it in `launchctl` commands.

```xml
<key>ProgramArguments</key>
<array>
  <string>/opt/homebrew/bin/socat</string>
  <string>-d</string><string>-d</string>
  <string>/dev/cu.usbserial-FTEL78JL,ispeed=9600,ospeed=9600,cs8,parenb=0,cstopb=0,clocal=1,crtscts=0,ixon=1,ixoff=0,ixany=1,raw,echo=0</string>
  <string>EXEC:/usr/local/sbin/wyse50-login,pty,setsid,ctty,stderr</string>
</array>
```
The command to run, one array element per argument. Two `-d` flags raise socat's
logging verbosity. Then socat's two addresses: the serial port, and the program
to run on a pty.

```xml
<key>EnvironmentVariables</key>
<dict><key>TERM</key><string>wy50</string></dict>
```
`TERM=wy50` so programs consult the right terminfo entry. `login -p` preserves
it into your shell.

```xml
<key>KeepAlive</key><true/>
```
**The getty behavior.** Always keep this running; if it exits, start it again.
This is what makes a fresh `login:` appear after you log out, and what starts the
service at boot.

```xml
<key>ThrottleInterval</key><integer>5</integer>
```
Wait at least 5 seconds between restarts. Without this, a misconfiguration that
makes socat exit instantly would spin in a tight loop.

```xml
<key>StandardErrorPath</key><string>/var/log/wyse50-getty.log</string>
```
Where socat's diagnostics go. Essential — a background daemon has nowhere else
to complain.

#### Every serial option, and why

| Option | Meaning | Why this value |
|---|---|---|
| `ispeed=9600` `ospeed=9600` | Input/output baud | This socat build has **no `b9600` shorthand** — that form is Linux-specific. Copying a Linux example fails with `unknown option "b9600"`. |
| `cs8` | 8 data bits | The "8" in 8N1 |
| `parenb=0` | Parity disabled | The "N" |
| `cstopb=0` | One stop bit | The "1" |
| `clocal=1` | Ignore modem control wires | Don't require DCD, whose presence we can't assume |
| `crtscts=0` | Hardware flow control off | The cable may lack RTS/CTS |
| `ixon=1` | **Obey XOFF sent by the Wyse** | The overrun protection. Without it, bursts garble the screen. |
| `ixoff=0` | Don't send XON/XOFF *to* the Wyse | Nothing needs throttling that direction, and `0x11`/`0x13` are `DC1`/`DC3` to a Wyse, which may act on them |
| `ixany=1` | Any character resumes stopped output | Rescues a latched XOFF — pressing any key unsticks it |
| `raw` | No input/output processing | The pty handles line discipline; the serial side just moves bytes |
| `echo=0` | Don't echo on the serial side | Otherwise every character appears twice |

#### The pty side

```
EXEC:/usr/local/sbin/wyse50-login,pty,setsid,ctty,stderr
```

| Option | Meaning |
|---|---|
| `EXEC:` | Run this program as the other endpoint |
| `pty` | Give it a pseudo-terminal rather than a plain pipe |
| `setsid` | Make it a new session leader — required for job control |
| `ctty` | Make the pty its *controlling* terminal, so `Ctrl-C` works |
| `stderr` | Route its error output to the pty too, so you see errors |

Note what's **absent**: `rawer`. That option forces the pty into fully raw mode
with echo off, but `login` expects a normal cooked terminal. With it, you'd type
blind. We had it initially; removing it was one of the fixes.

### 2. `/usr/local/sbin/wyse50-login`

Root-owned, mode `755`. This is our getty-equivalent.

```sh
#!/bin/sh
stty sane
stty rows 24 cols 80 onlcr icrnl echo
export TERM=wy50
export LANG=C LC_ALL=C
printf '\007\r\n=== WYSE 50 LINK UP (%s) ===\r\n' "$(date '+%H:%M:%S')"
exec /usr/bin/login -p
```

- **`stty sane`** — reset the pty to conventional settings. Insurance against
  inheriting something strange.
- **`stty rows 24 cols 80`** — tell the pty the physical screen size. A Wyse 50
  is 80×24. Without this, programs think the screen is 0×0 and `vim` and `less`
  misbehave. socat can't set this itself, which is the main reason this wrapper
  script exists.
- **`onlcr`** — translate newline to carriage-return + newline on output. A bare
  newline moves the Wyse *down* but not back to column 1, so text would stair-step
  down the screen.
- **`icrnl`** — translate the carriage return the Return key sends into a newline,
  which is what Unix programs expect.
- **`echo`** — the Mac echoes your typing back. The terminal itself doesn't (it's
  in full duplex), so without this you'd type invisibly.
- **`TERM=wy50`** — select the terminfo entry.
- **`LANG=C LC_ALL=C`** — force ASCII. A Wyse 50 has no UTF-8, so multibyte
  characters from `git`, `ls`, or `vim` would render as junk.
- **The banner** — instrumentation, not decoration. It proves the whole
  socat→pty→serial path works *before* `login` can be blamed for a blank screen.
  Given how many different faults present as "nothing on screen," this is the
  single most useful line in the setup.
- **`exec /usr/bin/login -p`** — replace this script with `login`, rather than
  running it as a child. `-p` preserves the environment we set up (notably
  `TERM`). `exec` matters: it means when `login` exits, *this process* exits, so
  socat notices, so launchd respawns.

### 3. `~/.zshrc` guard

Some programs misbehave on a pre-ANSI terminal. Rather than change global config
and affect your normal terminals, this is conditional on `TERM`:

```zsh
case "$TERM" in
  wy*|wyse*|dumb|adm*|tvi*)
    unset zle_bracketed_paste
    export NO_COLOR=1
    stty oxtabs 2>/dev/null
    ;;
esac
```

- **`unset zle_bracketed_paste`** — zsh's line editor announces "bracketed paste
  mode" by sending `ESC[?2004h`. It emits this as **hardcoded ANSI**, not via
  terminfo, so it ignores that `wy50` has no such capability. The Wyse consumes
  `ESC[?` and prints the leftover `2004h` on your screen, and the stray bytes
  shove the cursor around.
- **`NO_COLOR=1`** — `git`, `rg` and friends emit ANSI color codes
  (`ESC[31m`…). The Wyse uses `ESC G n` for attributes instead, so those render
  as garbage. `NO_COLOR` is a widely honored convention for suppressing them.
- **`stty oxtabs`** — `ls` aligns its columns with TAB characters, assuming tab
  stops every 8 columns. The Wyse's stored tab stops didn't match, so columns ran
  together. `oxtabs` is a BSD/macOS output flag telling the kernel to expand each
  TAB into spaces before transmitting, so the terminal never sees a TAB at all.
  This fixes anything tab-aligned — `git status`, `df`, `mount` — not just `ls`.
  (The alternative is setting the terminal's own tab stops in its setup menu, but
  those can drift or be lost on reset.)

**Optional, not currently applied.** The Wyse's Backspace key sends `^H`
(`0x08`), while `stty sane` sets the erase character to `^?` (`DEL`, `0x7F`), so
Backspace echoes `^H` instead of erasing. Fix for one session:

```sh
stty erase '^H'
```

Add `stty erase '^H' 2>/dev/null` to the guard block to make it permanent.

### Also installed

`socat` itself, via `brew install socat` → `/opt/homebrew/bin/socat`.

---

## Part 6 — Operating it

### Normal use

Nothing to run. The daemon is always up and starts at boot.

- **Powered the Wyse on and see nothing?** Press **Return**. An empty username
  makes `login` print a new prompt. (Why this is necessary: Part 8.)
- **Log out:** type `exit` or press `Ctrl-D`. About 5 seconds later
  (`ThrottleInterval`) a beep and a fresh banner and `login:` appear.

### Commands, from the Mac

```bash
# Is it running?
launchctl print system/local.wyse50-getty | grep -E 'state|pid|last exit'

# What is socat complaining about?
tail -f /var/log/wyse50-getty.log

# Restart it — e.g. after editing the plist, or to force a fresh prompt
sudo launchctl kickstart -k system/local.wyse50-getty

# Stop it / start it
sudo launchctl bootout system/local.wyse50-getty
sudo launchctl bootstrap system /Library/LaunchDaemons/local.wyse50-getty.plist
```

Healthy is **two** processes — socat with `PPID 1` (launchd owns it), and a
`login -p` child:

```bash
pgrep -fl 'socat.*usbserial|/usr/bin/login -p'
```

> **A gotcha for scripts:** `bootout` is **asynchronous**. Running `bootstrap`
> immediately after it fails against a still-unloading service, and leaves the
> daemon simply *not loaded*. Any script doing both must poll
> `launchctl print` until the service is gone. This bit us — see Part 7.

### `sudo` in an AI coding session

Privileged commands need a password, and a password needs a terminal. Some
contexts have no TTY, so `sudo` fails with *"a terminal is required to read the
password."* Either run those commands in a real Terminal window, or use a GUI
prompt:

```bash
osascript -e 'do shell script "/path/to/script" with administrator privileges'
```

---

## Part 7 — Everything that went wrong, and why

Recorded because **almost every failure here presents identically** — a blank
screen — while having unrelated causes.

**1. `unknown option "b9600"`.** Linux examples use `b9600` for baud; this macOS
build wants `ispeed=`/`ospeed=`.

**2. Silence, while everything reported healthy.** `launchctl` said
`state = running` and a live `login -p` existed. But a supervised process that
never writes a byte is *indistinguishable* from a working one at that level of
inspection. Resolved by testing the two directions separately: writing straight
to `/dev/cu.*` proved Mac→terminal worked; reading raw from it while typing
proved terminal→Mac worked. Both fine — which located the fault past the cable.

**3. A latched XOFF — the actual cause.** With `ixon=1`, a single XOFF (`0x13`)
from the terminal stops transmission **indefinitely**. The Wyse emitted one while
powered down mid-output and never sent the matching XON, so the port stayed muted
for that whole session. Power-cycling the terminal cannot clear it, because the
flag lives in the Mac's kernel tty state. Proven by accident: running
`stty -f /dev/cu.usbserial-FTEL78JL -ixon -ixoff` flushed the queued prompt
instantly.

**4. Over-correction — the garbled screen.** Concluding "flow control is the
enemy" and setting `ixon=0,ixoff=0` cured the stall *and* removed the Wyse's only
way to say "stop, I'm full." At 9600 its buffer overruns on any burst, so a shell
painting a prompt produced garbage.

> **The key insight:** the stall and the overrun pull in **opposite directions**.
> Too much flow control and one bad XOFF mutes you forever; none at all and the
> terminal drowns. The resolution is asymmetric: `ixon=1` so the terminal can
> throttle, `ixoff=0` so the Mac doesn't inject control bytes, and `ixany=1` so
> any keypress can rescue a latched stop.

**5. `rawer` on the pty.** Raw mode with echo off, but `login` needs a cooked
terminal — you'd have typed blind. Replaced with `stty sane` in the wrapper.

**6. A silent `bootstrap` failure.** The async `bootout` problem above. The
repair script didn't check the exit code, so the daemon ended up unloaded — which
looked exactly like every other blank-screen failure. This is what the one-off
`start.sh` fixed; it isn't needed in normal operation.

**7. `2004h` printed, cursor jumping.** zsh's hardcoded-ANSI bracketed paste.

**8. `ls` columns running together.** TAB alignment against mismatched tab stops.

**9. Backspace echoing `^H`.** Erase character mismatch (`^H` vs `^?`).

**10. `sudo` unable to read a password.** No TTY in the session.

### The lesson

Nine different faults, one symptom. The only efficient way through is to make
each layer announce itself rather than inferring health from the outside — hence
the banner in the wrapper, `-d -d` logging to a file, and always testing TX and
RX as separate directions.

---

## Part 8 — Limitations and what could be better

### Powering the terminal off does not end your session

Because `clocal=1` and we use `cu.*`, the Mac never watches the carrier wire. It
has no idea the terminal was switched off. `login`/`zsh` keep running on the pty.
Turn the Wyse back on, press Return, and you're still in your old shell.

Two consequences:

1. **A power-cycle is not a way to get a fresh prompt.** The banner and `login:`
   are sent once, when the daemon starts. If the screen was dark at that moment,
   those bytes are simply gone. Press **Return** for a new prompt, or `exit` for
   a genuinely new session.
2. **Security:** the session persists unattended. Anyone can switch the terminal
   on and press Return to land in your shell.

### The upgrade: real carrier detection

To get true getty behavior — power on the terminal, get a prompt automatically —
switch to modem control: use `/dev/tty.usbserial-FTEL78JL` with `clocal=0`. Then:

- socat blocks on `open()` until the Wyse asserts DTR, i.e. until you power it on
- powering off drops carrier, socat exits, launchd respawns it, and it waits again
- and because carrier drop hangs up the line, **powering off logs you out**,
  closing the security hole

**The catch:** this needs the cable to genuinely carry DTR→DCD. A three-wire
(TX/RX/GND) null modem doesn't, and socat would block on open forever — no prompt
at all. Test first, with the Wyse powered **on**:

```bash
sudo launchctl bootout system/local.wyse50-getty
socat -u /dev/tty.usbserial-FTEL78JL,clocal=0,ispeed=9600,raw - &
sleep 2; jobs
```

Opens → DCD is present, the upgrade is safe. Hangs → three-wire cable, keep the
current setup.

### Other limitations

- **No UTF-8.** `LANG=C` is deliberate. Non-ASCII filenames appear as escapes.
- **9600 is slow.** ~960 characters/second; a full screen takes ~2s. The Wyse 50
  supports 19200 — change both `ispeed`/`ospeed`, match it in the terminal's
  setup menu, then `kickstart`. If it garbles at the higher rate, the handshake
  isn't keeping up; go back down. Alternatively 4800 is slow enough that overrun
  can't happen even if flow control fails.
- **The device path is hardcoded.** A different adapter → different path → the
  daemon respawn-loops every 5 seconds with `No such file or directory` in the log.
- **`RunAtLoad` is not set.** Not required: `KeepAlive` alone makes launchd start
  the service at load and at boot. Adding `<key>RunAtLoad</key><true/>` would be
  belt-and-braces.

---

## Part 9 — Terminal-side settings

In the Wyse's own setup menu (`Shift`+`Setup`):

- **9600 baud, 8 data bits, no parity, 1 stop bit** — must match the Mac
- **XON/XOFF handshake ON** — the Mac depends on this (`ixon=1`); without it the
  terminal has no way to prevent overrun
- **Full duplex** — the host echoes your typing. Half duplex adds local echo and
  you'd see every character twice
- **Not LOCAL mode** — that routes the keyboard to the screen and sends nothing
  down the line. It looks like a working terminal whose input is being ignored

---

## Part 10 — Troubleshooting, in order

1. **Is anything loaded?** `pgrep -fl 'socat.*usbserial'` — the failure that
   looks like all the others (Part 7, #6).
2. **What does socat say?** `tail /var/log/wyse50-getty.log`
3. **Force a fresh prompt:** `sudo launchctl kickstart -k system/local.wyse50-getty`
   with the terminal **on**. Does the banner appear?
4. **Banner but no `login:`** → the problem is `login`, not the link.
5. **No banner** → is output stalled by a latched XOFF? Press a key on the
   terminal; `ixany=1` should resume it. Inspect with
   `stty -f /dev/cu.usbserial-FTEL78JL -a`.
6. **Still nothing** → test each direction separately:
   ```bash
   # TX: does the terminal beep and show text?
   printf '\007TEST\r\n' > /dev/cu.usbserial-FTEL78JL

   # RX: type on the Wyse for 20 seconds; bytes should hexdump
   socat -u -T20 /dev/cu.usbserial-FTEL78JL,ispeed=9600,ospeed=9600,cs8,raw - | hexdump -C
   ```
7. **TX works, RX dead** → terminal in LOCAL mode, keyboard locked, or a
   one-way-wired cable.
8. **Both dead** → null modem missing, wrong jack (AUX instead of MAIN), or baud
   mismatch.
9. **Garbage rather than silence** → parity/baud mismatch, or flow control not
   working (Part 7, #3 and #4).

---

## Appendix — Glossary

| Term | Meaning |
|---|---|
| **baud** | Signal changes per second. At 8N1, 9600 baud ≈ 960 characters/sec |
| **8N1** | 8 data bits, No parity, 1 stop bit |
| **DTE / DCE** | Terminal-or-computer / modem. Determines which wire each end transmits on |
| **null modem** | Cable or adapter crossing TX and RX, needed to join two DTEs |
| **DCD** | Data Carrier Detect — wire indicating the other end is present |
| **DTR** | Data Terminal Ready — wire asserting "I am powered up and ready" |
| **RTS/CTS** | Hardware flow control wires |
| **XON / XOFF** | `0x11` / `0x13` — software flow control bytes, "resume" / "stop" |
| **flow control** | Mechanism letting a slow receiver throttle a fast sender |
| **tty** | A terminal device. Historically "teletype" |
| **pty** | Pseudo-terminal: a software terminal pair, one side for the shell |
| **getty** | Classic Unix process that opens a terminal line and prints `login:` |
| **launchd** | macOS's PID 1 — its init and service manager; the systemd analogue |
| **LaunchDaemon** | A system-wide launchd service, root-owned, started at boot |
| **`launchctl`** | The command-line tool for talking to launchd |
| **bootstrap / bootout** | launchd's load / unload operations |
| **KeepAlive** | launchd setting: restart this service whenever it exits |
| **terminfo** | Database of per-terminal escape sequences and capabilities |
| **`TERM`** | Environment variable naming which terminfo entry to use |
| **escape sequence** | Bytes beginning with `ESC` (`0x1B`) meaning a command |
| **ANSI / VT100** | The escape-sequence standard modern terminals speak; the Wyse 50 predates it |
| **bracketed paste** | Modern terminal feature; announced with `ESC[?2004h` |
| **`stty`** | Command for inspecting and setting terminal device settings |
| **`oxtabs`** | BSD `stty` flag: expand TABs to spaces on output |
| **`socat`** | Tool that connects two byte streams and copies between them |
| **FTDI** | Common maker of USB-to-serial chips; macOS has drivers built in |
