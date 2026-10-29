# Hybrid Deep Dives

Prototype Pet Heat Watch first, with the Water family (Sump Puck) as runner-up. Three ideas tie at 19/25 (Pet Heat Watch, Water family, Shop Air Node), so the choice rests on tie-breakers rather than score. Pet Heat Watch has the only confirmed legal driver on the business side (Pennsylvania requires hourly stored temperature records in dog kennels), documented consumer anger at pay-forever plans (Waggle about $199-299 a year all-in), real animal deaths on both sides, the lowest node BOM of the three (about $17.50 at 1,000 units against $27-40 for the sump puck and $60-75 for Shop Air Node), and a node-plus-hub platform that the Water family reuses almost unchanged. Its flaws are a life-safety liability and a pay-once promise that breaks for RV owners who need cellular. Score moves: Pet Heat Watch 20 to 19 (buildability down: LTE-M fallback and battery shipping add work); Water family 20 to 19 (BOM headroom thin, no landlord voices found, YoLink courting the same landlords); Machine Pulse 20 to 18 (B2C cut from 3 to 2, no new buyer proof); Shop Air Node 21 to 19 (B2B cut from 3 to 2 because no OSHA monitoring mandate exists, buildability cut from 5 to 4 because a good dust sensor roughly doubles the BOM); Shore-Power Watch 17 to 15 (buildability cut from 3 to 2: precision residual-current sensing, mains-adjacent safety and liability). Every demand score remains a hypothesis: no direct buyer quotes could be retrieved for any idea on either side.

Score key: B2B demand / B2C demand / Shared hardware / Buildable solo / Founder fit, each 1-5, total out of 25. Shared hardware 5 means one device serves both buyers; Buildable solo 2 means certification or safety liability is likely. (vendor) marks a figure from a vendor, retailer or affiliate page; (estimate) marks my reasoning or an unverified figure. All BOMs, buyer counts for the proposed products and proposed prices are (estimate). "Old" scores come from the earlier hybrid screen; "New" scores come from these deep dives.

## Pet Heat Watch

*A camera-free temperature and power-loss node with a local siren and a free BLE, Wi-Fi or LoRa path, for pet owners (homes, RVs, cars) and for kennels, rescues and boarding operators.*

### Buyers

**B2C:** About 94M US households own a pet (APPA 2025 report, 2024 data) and 95M in 2025 per the APPA May 2026 update ([Pet Food Industry](https://www.petfoodindustry.com/pet-food-market/market-trends-and-reports/news/15741428), [AccessNewswire](https://www.accessnewswire.com/newsroom/en/business-and-professional-services/u.s.-pet-industry-reaches-158-billion-in-2025-poised-for-continu-1165595)). The paying subset is unknown: counts of RV owners who travel with pets and of car-pet owners were not found. Decider and payer are the same person, usually a dog owner who travels or works away. (estimate) Three segments: home pets with AC (fully servable without a plan), a stationary RV at a site with a phone nearby (servable with BLE and Wi-Fi), and an RV left while the owner is away from the site (the Waggle buyer, who needs cellular).

**B2B:** IBISWorld puts US pet grooming and boarding at about 193,000-199,000 businesses for 2026, but its own pages disagree and the category lumps groomers, boarders and daycares ([IBISWorld](https://www.ibisworld.com/industry-statistics/number-of-businesses/pet-grooming-boarding-united-states/)). Narrower counts: 47,893 groomers (Poidata, listing-based), about 9,000 boarding kennels and 35,000 pet sitters in US and Canada (Dogster citing PetMD), shelters 8,502 or 14,794 depending on the IBISWorld page. Counts conflict; do not quote one total. Decider and payer is the owner-operator; most sites are small and independent. (estimate) The reachable market is independent boarding kennels, overnight daycares, shelters, rescues and transport operators, perhaps 10,000-40,000 sites with 1-3 hub sites each (no source).

### Competitors

**B2C:** Subscription cellular monitors dominate.

| Product | Hardware | Plan | Notes |
|---|---|---|---|
| Waggle | $99-159 | $25/mo (one table says $39), prepaid $119 per 6 months or $199 per year | Cellular only, US only, prepaid cannot be canceled or prorated; advertised 5-day battery, reviewer saw about 2 days |
| Necto | $130 | One year included, then $9.99/mo or $83.88/yr | Cellular, 3-day battery advertised, power-loss alert |
| MarCELL | Not captured | Subscription | Third cellular monitor |

Source for Waggle and Necto: [Everywhere With Claire, updated 5 Jun 2026](https://everywherewithclaire.com/waggle-vs-necto-pet-monitoring-systems/) (affiliate site). Wi-Fi monitors without battery backup go dark when power fails, per a forum snippet and vendor blogs (Harvest Hosts, CabinPulse (vendor)); page bodies were not read. Non-subscription BLE thermometers (Govee, SensorPush) were not researched.

**B2B:** Monnit sells kennel-marketed wireless sensors (temperature, humidity, door, water, AC current, button-press for cleaning logs), alerts by text, email or phone call, free CSV export, thresholds set in the iMonnit cloud app, and needs a Monnit gateway ([Monnit](https://monnit.com/applications/pet-animal-welfare/)). A 2016 newsletter said sensors started at $49 with free basic alerts; 2026 pricing was not found. Kestrel DROP data loggers are used for Pennsylvania dog-warden inspections ([Kestrel](https://kestrelmeters.com/blog/kestrel-drop-monitors-dog-kennels-for-pa-dog-warden)). Police K9 vehicle heat alarms (AceK9) are a separate niche.

### Pain in buyers' words

**B2C:** No verbatim quotes were obtained; this is paraphrase from search summaries of Trustpilot and a travel blog, mostly undated. One owner said a Waggle went offline about a year after purchase with no notification; one was charged twice with no active subscription; one paid for a 2-year plan in May and it stopped working in September on vacation with no support reply; one said a firmware update broke a unit ([Trustpilot](https://es.trustpilot.com/review/mywaggle.com?page=4), [RVLife](https://rvlife.com/waggle-pet-monitor-review/)). Positive reviews exist too (support called a lifesaver). A Necto reviewer said they switched over Waggle's subscription changes. Deaths: a Byron, Georgia RV dog died in August 2024 after generator failure shut off the AC ([WTSP](https://wtsp.com/article/news/local/byron-family-looking-for-answers-after-dog-dies-in-hot-rv/93-e03a1ba4-8875-484e-a7a5-1959804968a4)); PETA logged 113 companion-animal heat deaths in 2024 "that we know of" ([PETA](https://www.peta.org/features/dogs-and-other-companion-animals-suffer-heat-related-deaths/2024-incidents/)).

**B2B:** No business-owner quotes were obtained. The evidence is incident reporting: 20 dogs died in Gilbert, Arizona in 2014 after kennel AC failed ([Fox13](https://www.fox13seattle.com/news/tragic-20-dogs-die-when-air-conditioning-fails-at-kennel)); 14 died in Saskatoon in 2016, the owner was later charged and the kennel fitted sensors in seven locations ([Global News](https://globalnews.ca/news/2974529/playful-paws-adds-safeguards-after-14-dogs-die-at-the-saskatoon-kennel/)); 12 died in Columbia County, Florida after an AC breaker shut off ([First Coast News](https://firstcoastnews.com/article/news/local/12-dogs-die-after-ac-failure-columbia-county-boarding-kennel/77-acded86e-2bd8-4248-a852-26fc798c843f)); 14 died in an Indiana show truck in 2023 after a tripped breaker ([Fox6](https://fox6now.com/news/14-dogs-died-after-ac-failed-in-truck-they-were-housed-in-during-dog-show-in-indiana)). The one confirmed rule: Pennsylvania 7 Pa. Code 28a.4 requires temperature and humidity measured and recorded in each dog room, a device storing data hourly for at least 6 months, accuracy within 1 F and plus or minus 2% RH, and 4 hours to fix heat above 85 F ([Cornell LII](https://www.law.cornell.edu/regulations/pennsylvania/7-Pa-Code-SS-28a-4)). Connecticut and Minnesota set temperature standards; no other confirmed logging mandate was found.

### Price and model

**B2C:** (estimate) $49-79 once for the home, BLE or Wi-Fi unit with an honest statement that alerts reach you within range of your phone or hub. A "Cell Pack" (prepaid LTE-M credit, about $29 for 12 months) is sold separately at about $99-129 total so the base price stays pay-once. Compared with Waggle plus a plan ($250-500 over two years), this undercuts; Necto's $7-10 a month shows the market tolerates low plans. Willingness to pay is unverified. Cellular floor for a plan: Hologram's 2023 page lists $1.00 per SIM per month plus $0.10 per MB; no current 2026 price found.

**B2B:** (estimate) Kit of hub plus 4-8 nodes at $249-449 once, with an optional $9-15 per site per month for SMS and voice call-out, PDF and CSV compliance export, and multi-site view. Pennsylvania's 6-month retention can be met by local SD storage on the hub with no subscription, and Monnit's free basics mean the plan must sell convenience, not access. Accuracy documentation (and possibly NIST-traceable calibration) is a likely customer ask.

### Go-to-market

**B2C:** (estimate) YouTube build-and-test videos on the founder's channel, a free "RV dog heat" calculator page, RV forums and Facebook groups (Escapees, Good Sam, iRV2 are named venues; posting rules unverified), Amazon plus own store, and affiliate review sites that currently promote Waggle and Necto. First 10: 3-5 channel subscribers via preorder, 3 from RV-forum beta posts, 2-3 rescue or foster volunteers given a free unit for a published test log.

**B2B:** (estimate) Sell state by state starting with Pennsylvania, where records are an inspection item; cold email and call kennels from the state licensed list (availability unverified); pet-business Facebook groups; trade groups (names plausible, not verified); possibly insurers (discounts unverified). First 10: 3-4 kennels near the founder on a free 30-day pilot, 3 rescues or shelters, 2-3 Pennsylvania kennels by cold outreach, 1-2 overnight pet sitters via Rover or Wag communities.

### Kill criteria

**B2C:** (estimate) (1) Fewer than 150 preorders or deposits at $29-49 within 60 days of a landing page plus one video, or under 3% email-to-deposit. (2) Beta units show more than 2 false or missed alerts per 1,000 unit-days, or BLE and Wi-Fi alert delivery under 99% across 30 units over 60 days. (3) More than 40% of survey respondents say cellular is a requirement, which would force a recurring-cost product and contradict the pay-once thesis.

**B2B:** (estimate) (1) Of 40 Pennsylvania kennel owners contacted, fewer than 3 agree to a paid pilot at $200 or more. (2) Fewer than 30% of pilots convert to paid or to the $9-15 plan after 60 days. (3) Any customer needs a certified or NIST-traceable logger and the sensor cannot meet it within $15 more per node.

### Shared hardware and v1

Identical: PCB, temperature and humidity sensor, mains-presence input, backup battery, siren, BLE, enclosure shape. Different: B2C gets a free app (BLE or Wi-Fi push), stand, magnet, visor clip or 12V RV mount, 1-2 units. B2B adds multi-room naming, logs, export, SMS and voice escalation with acknowledgement, wall brackets with wash-down IP rating, and 4-16 nodes per site.

| Part | At 100 | At 1,000 |
|---|---|---|
| ESP32-C6 or nRF52840 module (pre-certified) | $5.00 | $3.80 |
| SHT4x temperature and humidity | $1.60 | $1.10 |
| Piezo siren 90 dB and driver | $1.50 | $1.00 |
| Power-loss sense, charger IC, 18650 or LiPo | $4.50 | $3.20 |
| LoRa module (SX1262, optional hub link) | $4.50 | $3.20 |
| PCB, assembly, passives | $4.00 | $2.20 |
| Enclosure (printed at 100; molded at 1,000, tooling extra) | $3.00 | $1.60 |
| Packaging, cable, misc | $2.00 | $1.30 |
| Node total | about $26 | about $17.50 |
| Hub (ESP32, LoRa, SD, Ethernet or Wi-Fi) | $22 | $15 |

The cell-fallback variant adds a pre-certified LTE-M module (about $10-14 at volume) and a carrier plan, and may need carrier approvals (unverified). Certification (estimate): FCC Part 15B declaration for the host with a pre-certified radio module, lab cost about $3-8k; battery packs need UN38.3 summaries for shipping (about $2-4k per pack design); no UL 217 or 268 if marketed as a pet alert, not a smoke or life-safety alarm. Alert path without a plan: local siren, BLE to a nearby phone, Wi-Fi to a free relay, LoRa to a home or kennel hub (0.5-2 km line of sight, weaker through walls); email-to-SMS is unreliable; paid options are prepaid LTE-M or SMS. Caveats: only cellular covers "owner away from the pet's location." Competitor terms of service could not be read. Design for a heartbeat (missed check-in becomes an alarm), because silent offline failure is the main complaint against Waggle. Label as supplementary, avoid "guarantee" language, publish uptime logs, carry product liability insurance (quote unverified). Business customers sign a service agreement limiting damages to fees paid.

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| B2B demand | 3 | 3 | Confirmed Pennsylvania rule and deaths, but only one confirmed state, no priced evidence, Monnit offers free basics |
| B2C demand | 3 | 3 | Clear subscription anger, but paying RV buyers need cellular and the pool is unquantified |
| Shared hardware | 5 | 5 | Same node and hub; differences are app tier, mounts and unit count |
| Buildable solo | 5 | 4 | LTE-M fallback, battery shipping and uptime reliability add work |
| Founder fit | 4 | 4 | Camera-free, local-first, design-led, channel audience; life-safety liability adds worry |
| Total | 20 | 19 | Lowered for buildability |

## Water family

*A battery-powered Sump Puck with a loud local siren and pump-current logging, plus a Leak, Freeze and Vacancy node on the same radio and hub, for homeowners and for small landlords and property managers.*

### Buyers

**B2C:** Homeowners and second-home owners. About 1 in 60 homeowners files a non-weather water claim a year, averaging about $13,954 (secondary, Triple-I via trade press, 2018-22; [Contractor Mag](https://www.contractormag.com/plumbing/article/55269168/lead-detection-devices-can-reduce-average-claim-costs-by-4k)). No federal count of US homes with a sump pump was found; the marketing claim that 60% of homes have wet basements was not traced to a primary study. The homeowner decides and pays at $30-300; insurers influence the choice.

**B2B:** About 15.5M investor-owned single-family homes, about 90% owned by owners with 1-10 properties (BatchData, Q1 2026); institutions hold 3-5% of single-family rentals (CRS, June 2026). About a third (32-37%) of short-term-rental operators use smart devices (Hostfully). The owner-landlord is both decider and payer; property managers decide for owners and usually pass the cost on (estimate). Insurers and program vendors subsidize or give away sensors. Vacancy is the highlighted risk: vendors say a leak in a vacant unit can run for days or weeks. No HOA or small-manager count was found.

### Competitors

**B2C:** The price floor is brutal.

| Product | Price | Notes |
|---|---|---|
| YoLink | 4 sensors plus hub about $40-55 on deals (Slickdeals 2025) | LoRa, hub required, no built-in sounder on base sensor, no subscription |
| Govee | $7.99 single, $35.99 gateway plus 3 sensors (deals) | 2.4 GHz only, onboarding complaints, no sourced outage complaints |
| Moen Flo | About $499 plus install (2024 roundup) | Optional $5/mo FloProtect; basic alerts need no plan |
| Moen Smart Sump Pump Monitor | $261.90 (one retailer says discontinued) | 9 V battery sounds a local alarm in an outage; closest prior art, availability unverified |
| SpotProtect SumpSpot | $215 at one reseller | Wi-Fi, 2 AA about 5 years (vendor); sources conflict on fees |
| Zoeller, Basement Watchdog, PumpSpy | About $300 | Battery-backup pumps with Wi-Fi alerts |
| Phyn, Flume | Phyn bundled via insurers at $500-899 with install | No paid plan for Phyn; Flume requires subscription if bought through insurers |

Peril Protect was reviewed at $23 a month with a $74 early cancellation fee. Sources: [Slickdeals](https://slickdeals.net/f/18431251-prime-39-99-yolink-smart-home-starter-kit-hub-4-pack-water-leak-sensor-4-at-amazon), [Moen](https://www.moen.com/products/S2000ESUSA), [Absolute Automation](https://www.absoluteautomation.com/products/spotprotect-sumpspot-wifi-sump-pump-alarm), [Phyn](https://phyn.com/pages/nationwide-california), [TechHive](https://www.techhive.com/article/579428/peril-protect-review.html).

**B2B:** Minut: sensor about $129-150 plus $10-15 a month per property; free Starter ended for new customers in 2021 and phased out from 2024; Trustpilot about 3.5/5 from about 517 reviews ([Trustpilot](https://nz.trustpilot.com/review/minut.com)). SmartRent, PointCentral, Streamlabs (Chubb), Stratis and HSB sell enterprise or property-manager platforms, mostly quote-only; Swidget sells a movable kit for vacant units; Phyn sells a property-manager dashboard. YoLink is courting landlords: a YoSmart employee posted on BiggerPockets in 2026 (no replies) asking where leaks hurt ([BiggerPockets](https://www.biggerpockets.com/forums/517/topics/1294309-water-leak-prevention-for-rental-properties)). Insurer programs: Scout Security plus bolt Prevention sells a Water and Climate Sensor Kit at $90 to eligible policyholders from August 2026, first insurer VTRO in California, claims about 40% off the water portion of premium (vendor claim; [Scout](https://www.scoutalarm.com/blogs/diy-directory/scout-launches-water-damage-prevention-program)). Chubb reportedly gives 8% for comprehensive leak detection, Nationwide up to 10%, Church Mutual a free sensor (all to verify).

### Pain in buyers' words

**B2C:** Actual buyer words: not found (Reddit, Amazon and Trustpilot were not reachable). Paraphrased themes from snippets: subscription surprise (a Hive buyer said the fee was not made clear); Wi-Fi sensors need 2.4 GHz and awkward onboarding (Govee); an editorial guide warns a monitor depending on household power and Wi-Fi may go silent in the outage it is meant to detect. A Home Assistant poster noted a Govee sensor beeps at 1.8 V total battery.

**B2B:** Landlord voices: not found. The closest proxies are Minut's Trustpilot themes (forced subscription after an earlier free tier, app, price) and the YoLink vendor post, which is not a landlord voice. Vendors and Chubb's condo guide assert that vacancy leaks go unnoticed and recommend a sensor at every fixture.

### Price and model

**B2C:** (estimate) Sump Puck $69-89 once with no plan; an optional $79 bridge for Wi-Fi and phone alerts; leak probes only as an add-on pack at $19-25 each, not the headline, because deal prices of $8-15 beat the earlier $29-39 idea. At $79 and a BOM near $40, gross margin is about 50% before fulfillment, FCC and returns; the puck only works above about $69.

**B2B:** (estimate) 4-pack of leak nodes plus a pit puck at $149-199, a free local log, and an optional $2-5 per property per month for a multi-property map, contractor sharing and PDF logs for insurers. At a $69 pack price the puck margin is thin. Insurer route: a solo founder will not land a national carrier; the realistic targets are program vendors like bolt, regional mutuals, and property-manager or HOA captive programs, which want a white-label device with a cloud API and low returns. A local-first design may clash with programs that need cloud proof of activation; plan a signed "activation receipt."

### Go-to-market

**B2C:** (estimate) YouTube teardown and outage-demo video, Amazon and own store, r/BasementFlooding-type communities, sump pump installers and plumbers as referrers (they sell $300+ battery backups), and the Home Assistant community for the open local protocol. First 10: 10 viewers or Home Assistant users with pits from a preorder list, plus 3-5 neighbors or relatives with pits for in-pit testing through a storm or thaw.

**B2B:** (estimate) First 10: 3-5 BiggerPockets or Facebook-group landlords with 5-30 doors on a 2-unit free pilot; 2-3 local property managers with vacant-turn problems; 1-2 sump or foundation contractors reselling to landlords; 1 insurance MGA or program vendor pilot once units are FCC-ready.

### Kill criteria

**B2C:** (estimate) (1) Fewer than 150 preorders or deposits at $69 within 8 weeks of a launch video. (2) Fewer than 15% of 40 interviewed pit owners say they would pay $69 or more over a $10 leak sensor after seeing the outage demo. (3) A major retailer or insurer launches an outage-proof local-siren sump sensor under $50 (watch Moen, Zoeller, Govee, Amazon Basics).

**B2B:** (estimate) (1) Fewer than 3 of 15 landlord or manager interviews say they would pay $60 or more per pit or property without a subscription. (2) No insurer, program vendor or manager agrees to a written pilot within 6 months. (3) Pilot sites see more than 5% false alarms or more than 10% hardware returns in 90 days, or any landlord prefers YoLink at less than half the cost after the demo.

### Shared hardware and v1

Identical: MCU and radio module, LoRa radio, temperature, water-contact probe, reed input, piezo siren, battery tray, enclosure family, firmware, hub and protocol. B2C differs by single-puck box, Wi-Fi and phone bridge, onboarding and no plan. B2B differs by 10 or 40-pack packaging, pre-provisioned property IDs, tamper-evident label, signed event-log export, optional Ethernet LoRa gateway and a fleet dashboard.

| Sump Puck part | Cost (estimate) |
|---|---|
| nRF52840 or ESP32-C6 pre-certified module | $4-6 |
| LoRa pre-certified module (Wio-E5 or RAK3172 class) | $6-9 |
| Ultrasonic pit-level sensor or float plus wet probe | $3-6 |
| Split-core CT clamp and ADC front end (pump current and cycles) | $4-7 |
| Piezo siren 90-100 dB and driver | $1.50-3 |
| Temperature sensor, reed input, LEDs, connectors | $2 |
| PCB, assembled | $3-6 at 100; $2-4 at 1,000 |
| Battery (4 AA lithium or 2 C) and holder | $5-8 |
| Enclosure and gaskets | $3-5 at 100; $1.50-3 at 1,000 |
| Packaging, cable, mount | $2-3 |

Sump Puck BOM: about $34-52 at 100 units and $27-40 at 1,000. Leak, Freeze and Vacancy node: about $11-16 at 100 and $8-12 at 1,000 (coin cell or 2 AAA). Hub or bridge: $18-30. Certification (estimate): pre-certified modules, then FCC Part 15 Subpart B self-declaration on the finished product (lab cost not sourced; budget low thousands); battery-only, low-voltage and no mains connection avoids UL listing for the product itself, and the CT clamps onto the pump cord. Insurers or contractors may ask for UL or ETL; whether any program does was not verified. Battery life: 3-5 years on 4 AA lithium at a 15-minute heartbeat is an estimate that needs measurement. Alert path in order: local siren on the puck's own battery; LoRa to a hub with its own backup and siren; hub pushes via Wi-Fi to phone; optional paid LTE-M bridge for second homes (off v1); missing-heartbeat alert, which Moen's design lacked. Caveat to state plainly: if the house loses power and Wi-Fi, a phone alert still needs cellular; otherwise only the pit siren and hub siren work.

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| B2B demand | 3 | 3 | Vacancy and insurer pull are real, but small landlords behave like consumers, no landlord quote, YoLink courting them |
| B2C demand | 4 | 3 | Strong claims data, but $8-15 sensors and insurer giveaways cap price; outage-proof sump niche is open but sized by unverified counts |
| Shared hardware | 5 | 5 | Same puck, probes, firmware and hub |
| Buildable solo | 4 | 4 | Pre-certified modules, no mains wiring; risks are waterproofing, pit-sensor reliability, FCC lab test, support load |
| Founder fit | 4 | 4 | Fits local-first and YouTube distribution; weaker on insurer and landlord sales |
| Total | 20 | 19 | Old score is the Sump Puck (the Leak, Freeze and Vacancy kit scored 19 at 3/3/5/4/4) |

## Machine Pulse

*A clamp-on current monitor that reports run, idle or off for machines with no network, for hobby CNC, laser, printer and woodshop owners and for small machine shops, makerspaces and print farms.*

### Buyers

**B2C:** Entry-level (under $2,500) 3D printer shipments rose 26% in full-year 2025 and Bambu Lab took the top spot with 37% share (global, not US; [Tom's Hardware](https://tomshardware.com/3d-printing/bambu-lab-overtakes-creality-as-the-worlds-top-selling-budget-3d-printer-brand)). xTool had 42.8% of laser engravers in 2024 per CIC Consulting (scope unspecified, search summary). US counts of hobby CNC and laser owners: not found. (estimate) Segments: laser and CNC hobbyists with Home Assistant or a walk-away worry, home woodshop owners wanting dust-collector and tool status, and multi-printer owners (secondary, since printers have apps). Owner is decider and payer.

**B2B:** Earlier notes counted 17,156 machine-shop establishments (Census CBP 2023 via aggregator) with 74% of manufacturers under 20 employees. NTMA claims about 1,200 member companies (older sources say 2,000). US nonprofit makerspaces number about 237 active, plus about 50 clubs and fewer than 30 commercial ([Aldrich, Aug 2024](https://howardaldrich.org/2024/08/the-evolution-of-us-makerspaces-a-decade-of-growth-and-decline/)); school shop count not found; print-farm count not found. Decider is the shop owner or operations manager (estimate, no source confirms); a roughly $99 per-machine add sits under owner sign-off without procurement (estimate).

### Competitors

**B2C:** Competition is software, not hardware: OctoEverywhere free up to 3 printers, supporter tier $2.49-3.99 a month (page inconsistent); Obico from $6.99 a month annual for new subscribers from May 2026 ([Obico guide](https://www.obico.io/blog/is-obico-free-pricing-guide/), vendor blog); SimplyPrint free for 2 printers, then $5.99-9.99 a month ([SimplyPrint](https://www.simplyprint.io/pricing)). All are camera or cloud print software; none measure the machine's electrical state. DIY is the real rival: ESPHome `ct_clamp` with an ESP32 reports RMS current to Home Assistant for $15-25 in parts, though one Home Assistant user found a 10 A clamp's readings unimpressive and the ESP32's own ADC is imprecise (an ADS1115 is recommended). Shelly 120A CT at $18.95 is the cheap packaged alternative (earlier notes).

**B2B:** Machine-monitoring vendors price $240-1,200+ per machine per year (vendor). A five-machine shop pays about $1,200-6,000 a year in software plus $2,500-10,000 in hardware and integration ([Guidewheel](https://www.guidewheel.com/blog/machine-monitoring-software-cost), vendor). JITbase is free to 5 machines. Vorne XL is $4,490-4,990 one-time and a Capterra reviewer said the data collector is not included. MachineMetrics documents a current-transducer install with a threshold for legacy machines, so the leader uses the same sensing ([MachineMetrics](https://support.machinemetrics.com/hc/en-us/articles/360041432894-How-to-Install-a-Current-Transducer)). Free paths exist for MTConnect-ready machines (AMT: under 30 minutes per machine). Guidewheel, FourJaw, Evocon, Scytec and HaasConnect are covered in earlier notes; TrackMyMachines had no pricing or complaints found.

### Pain in buyers' words

**B2C:** No first-person quotes from hobby CNC or laser owners wanting run monitoring were found. The voiced pain is Bambu Handy notification reliability (2023-2025 forum threads, search-summary paraphrase, threads not opened): alerts reportedly fire mainly for cloud-started prints and not SD, USB or on-printer starts, and some users get only finish or cancel, not error or pause ([Bambu forum](https://forum.bambulab.com/t/can-we-please-fix-the-notifications/260496)). That pain is mostly solved by software, which weakens the clamp's case.

**B2B:** No first-person shop-owner quotes with dates were found. Cost is the top objection: 41% said monitoring costs too much (vendor survey cited by FourJaw). One individual's blog argues platforms rarely pay back for a single-site shop with few machines except at one bottleneck machine (illustrative $650 a year monitoring against $6-7K a year of risk; unverified). A shop reported utilization rising from 53% to 65% or more after monitoring 10 MTConnect machines (MMS, vendor-adjacent).

### Price and model

**B2C:** (estimate) $39-59 once, local MQTT, Home Assistant and ESPHome, no cloud, no subscription, optional free phone push via a local ntfy-style relay. There is no price anchor except DIY, so it wins on "no tinkering, nice object, local-first" and loses to the Home Assistant crowd that builds it in an evening.

**B2B:** (estimate) $79-129 per node once, plus an optional $3-5 per node per month fleet tier for a hosted dashboard, email and SMS alerts and history export; the local dashboard works without it. Hardware margin at 1,000 units is roughly 60-70%. The real target is old non-networked machines (manual mills, older Haas and Fanuc, lasers, saws, compressors, welders), where current sensing is the only option.

### Go-to-market

**B2C:** (estimate) One YouTube build-and-explain video plus a preorder page; r/homeassistant, r/lasercutting, r/hobbycnc, Carbide 3D and xTool communities; a Bambu P2S angle ("what your printer app can't see": breaker trips and power loss). First 10: preorders from the founder's subscribers, 5 laser or CNC owners, 5 Home Assistant users.

**B2B:** (estimate) Not NTMA (about 1,200 members is too few and association cycles are slow). Better: Manufacturing Extension Partnership centers' advisors as free referrers, local machinist Facebook and Reddit groups, shop YouTube channels, and makerspaces as the first paid pilots. First 10: 3 makerspaces, 3 small job shops via the founder's audience, 2 print farms, 2 school shops.

### Kill criteria

**B2C:** (estimate) (1) Fewer than 150 paid preorders or deposits at $39 within 60 days of a launch video with 20k+ views. (2) Fewer than 30% of beta users still have it plugged in and alerting at day 60. (3) More than 25% of beta users need support to set thresholds, meaning the teach flow fails.

**B2B:** (estimate) (1) Of 5 pilot shops, fewer than 3 pay $79 or more per node after a 30-day free trial. (2) Shops cannot name a decision they changed from the data within 30 days. (3) Misclassification above about 10% of minutes after a one-time teach step on more than 2 of 10 machine types, with no cheap fix.

### Shared hardware and v1

Identical: PCB, firmware, CT sensing, local MQTT and HTTP, LED. B2C: retail box, 30 A or 50 A CT, Home Assistant and ESPHome integration. B2B: DIN or magnet mount, 100 A split-core CT, optional stack-light relay, multi-node hub and dashboard, SMS and email, fleet tier. A line-splitter accessory (mains contact, +$6-10) is not recommended for v1.

| Part | At 100 | At 1,000 |
|---|---|---|
| ESP32-C6 or S3 pre-certified module | $4.50 | $3.50 |
| Split-core CT 30-100 A | $5.00 | $3.00 |
| ADS1115 and burden passives | $2.50 | $1.60 |
| PCB and assembly | $4.00 | $2.20 |
| Enclosure | $4.00 | $1.80 |
| RGB LED, button, USB-C | $0.90 | $0.60 |
| 5 V wall adapter (UL-listed, third party) | $2.50 | $1.60 |
| Packaging, misc | $2.00 | $1.20 |
| Total | about $25 | about $15.50 |

A B2B relay add-on is +$3-4. Certification (estimate): pre-certified module plus FCC Part 15B declaration (about $1-3K); clamp-on with a listed 5 V adapter has no mains contact, so UL listing is not legally required, though retailers may ask for a safety report; prefer a CAT III or IV rated CT (verify on datasheet). Alert path: LED on the device, local MQTT to Home Assistant, ntfy-style push; B2B adds SMS and email through a hosted tier. Accuracy caveat: no published run/idle/off accuracy figure was found, so the claim is unproven. Expect 90% or better for off versus powered and lower, machine-dependent accuracy for idle versus cutting (estimate); current-only detection is weak for end milling and VFD spindles, and a patent text says a simple threshold is insufficient. A CT on a two-conductor cord reads about zero because currents cancel, so consumers need a splitter cord (mains contact, a safety issue) or a clamp on a single conductor inside a panel (an electrician). Test plan: log 10 machines for a week against a stack light or camera, target 90% minute-level agreement, and publish the confusion matrix.

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| B2B demand | 3 | 3 | Money per machine is proven, but no independent owner voice, JITbase free to 5 machines, small shops may not justify it |
| B2C demand | 3 | 2 | Hobby counts unknown; voiced pain is Bambu notifications; DIY competes at $15-25 |
| Shared hardware | 5 | 5 | Same board, firmware and CT |
| Buildable solo | 4 | 4 | Pre-certified module, no mains contact; accuracy tuning and splitter-cord safety are the risks |
| Founder fit | 5 | 4 | Strong electronics and audience; weaker on selling to machine shops |
| Total | 20 | 18 | B2C was over-rated; B2B has no new buyer proof |

## Shop Air Node

*A workshop environment monitor that logs dust, VOC, noise and compressor or dust-collector run time on a local dashboard, for hobby woodworkers and garage makers and for small shops, makerspaces and school shops; explicitly not an OSHA-grade or health device.*

### Buyers

**B2C:** Garage and home woodworkers, resin, laser and 3D-print hobbyists, home shop owners; the individual decides and pays. No US count of hobby woodworkers or related hobbyists was found. Spending seen in forum threads: about $40 AliExpress units, about $60 Amazon units, Dylos monitors at roughly $289-319 (undated forum post and a 2013 article) ([Sawmill Creek](https://sawmillcreek.org/threads/air-quality-monitor.300881/), [Festool Owners Group, 2025](https://festoolownersgroup.com/threads/particulate-matter-dust-sensor-options.75775)).

**B2B:** Cabinet shops: NAICS 337110 had 6,055 US establishments in 2023 (Census CBP as cited by Vanta Insights; other aggregators give 5,953 companies, not comparable). Makerspaces: 237 nonprofit, about 50 clubs, fewer than 30 commercial (Aldrich), while Nation of Makers says more than 2,000 spaces and Fab Labs including schools and libraries. School shop count: not found. Payers: owner or shop manager for small shops, with insurance or safety consultants influencing; school facilities or CTE budget (Perkins funds); a makerspace board. Mostly estimate.

### Competitors

**B2C:**

| Product | Price | Notes |
|---|---|---|
| Temtop S1, LKC1000S+ | Budget; M2000 resale $159.99-209.99 | One owner trusts S1 PM2.5; another says LKC1000S+ tracks Dyson and Trotec units but cannot verify accuracy |
| Dylos DC1100 and DC1700 | About $289-319 Pro | Two particle-count bins, fan not pump so airflow changes counts about 3x (woodgears.ca) |
| PurpleAir Touch | Not captured | Wi-Fi, PM2.5 only per the retailer listing |
| Airthings View Plus | $299 list, no subscription | Not shop-specific |
| Aranet4 Home | About $189 | CO2-focused, no particle sensor |
| iVAC dust-collector switches | $60-750 | Switches, not monitors; one complaint that a 1.5 HP collector's surge can strain the switch |

Awair availability and uHoo fees conflict across sources. Wynd: nothing found. The gap is a monitor pitched at shop dust that logs per tool and talks to the collector; none found does.

**B2B:** TSI DustTrak DRX is listed by a UK retailer at GBP 8,005-8,680 ex VAT (US price not found). Temtop PMD351 handheld is about $1,699 on eBay. Envigilance sells industrial woodworking dust monitoring (pricing not retrieved). iVAC switches as above. No complaints about industrial monitors were found.

### Pain in buyers' words

**B2C:** Paraphrases, no invented quotes. Sawmill Creek, Nov-Dec 2022: Dylos owners put on a respirator when fine counts pass about 300 or above their ambient baseline of about 500, one said no one knows exact hazard levels, a cheap-unit owner found readings of 2-3 ug/m3 implausibly low yet useful relatively, and another found four $60 units tracking two Dylos units from about 6 to 200 ug/m3. Festool Owners Group, Apr-Aug 2025: one owner found only the belt sander and occasionally the bandsaw problematic over two years; one cautioned that a consumer monitor cannot easily answer "is this air safe"; one warned of a late, over-promising Kickstarter monitor. UK Workshop, Dec 2020: a former professional tester said cheap testing has too many variables to be meaningful. Readers want trends, not absolute numbers.

**B2B:** No business-owner quotes, no insurer data and no OSHA citation specifics against small cabinet shops were found. Trade press says the absence of a combustible-dust rule does not stop OSHA citations, with housekeeping (dust layers) the cited issue ([Woodworking Network](https://www.woodworkingnetwork.com/management/absence-comdust-rule-doesnt-stop-osha-enforcement), search snippet). A Montana cabinet shop was reportedly fined about $50,000 in a wood-dust exposure death (trade press). The "OSHA requires small shops to monitor" premise is wrong: OSHA has no wood-dust-specific PEL in force (general limits 15 mg/m3 total and 5 mg/m3 respirable apply; NIOSH recommends 1 mg/m3; [Cornell LII](https://www.law.cornell.edu/cfr/text/29/1910.1000)).

### Price and model

**B2C:** (estimate) $90-130 once, no account, local dashboard and Home Assistant, sitting above the $60 Amazon unit and below Airthings $299 and Dylos. Optional $20-30 CT clamp accessory. Owners distrust absolute numbers, so lead with "trend and event logger" (per-tool events, collector correlation, dB) rather than accuracy.

**B2B:** (estimate) $150 per node plus $5 per node per month for logs and alerts (the earlier screen's figure); makerspaces and schools likely prefer a one-time purchase with a free local dashboard and an optional $5 cloud relay; schools buy under a $500 PO threshold. The credible pitch is operational (collector filter loading, run hours via CT, housekeeping alerts), not exposure measurement; compliance buyers want gravimetric or industrial instruments.

### Go-to-market

**B2C:** (estimate) Woodworking and maker YouTube builds and teardowns using the founder's own co-located test data; Sawmill Creek, Festool Owners and r/woodworking posts after calibration data exists; a Dylos-group-buy-style preorder list. First 10: 10 forum posters from those threads, as numbered units with a calibration questionnaire.

**B2B:** (estimate) Makerspaces first (public board lists, Nation of Makers network), then school CTE teachers via ACTE and technology-education communities, then cabinet shops through dust-collector installers and insurance loss-control reps. First 10: 5 makerspaces at donated or half price in exchange for logged data and a case study, 3 school shops, 2 small cabinet shops from the founder's network. Total units are small (about 6,000 cabinet shops plus a few thousand makerspaces and school shops), so sales must be low-touch.

### Kill criteria

**B2C:** (estimate) (1) Fewer than 150 email or preorder deposits at $19 refundable within 60 days of a data-backed video. (2) The founder's own co-location test shows R-squared under 0.7 against a reference on sanding and sawing dust that one correction factor cannot fix. (3) Fewer than 3 of the first 10 users still open the dashboard weekly after 60 days.

**B2B:** (estimate) (1) After 20 conversations with makerspace, school and shop owners, fewer than 3 would pay $150 or sign a PO. (2) No insurer, consultant or safety lead will accept the logs as housekeeping evidence. (3) A prospect requires OSHA-grade or ISO-calibrated data in 5 of 10 conversations.

### Shared hardware and v1

Identical: sensor head (particles, VOC, mic, temperature and humidity), MCU, enclosure design, CT clamp port, local web dashboard. B2B gets a Wi-Fi, Ethernet or PoE variant, mounting plate, fleet portal with alerts and CSV export, optional relay; B2C gets USB-C power, Home Assistant and MQTT, and retail sale. Same PCB with a firmware flag. Sound level is computed on-device and no audio is stored.

Parts (all estimates, vendor prices not retrieved): Sensirion SPS30 about $35-45 at 100 and $28-35 at 1,000, or SEN55 (with VOC and humidity) $40-55 at 100; Plantower PMS5003 or 7003 at $8-15 is cheaper but weaker per a CDC-hosted lab study; I2S MEMS mic $1-3; CT clamp $4-8 plus ADC $2; ESP32-S3 module $3-5; PCB and connectors $4-8; enclosure $3-8; power $2-3. BOM about $75-95 at 100 units and $60-75 at 1,000 (the earlier $35-45 holds only with a Plantower-class sensor and no clamp). Certification (estimate): FCC Part 15B plus pre-certified module grant, a UL-listed 5 V adapter, CT clamp only (no direct mains connection), dust-ingress testing, no health claims. Alert path: local LED and dashboard, Home Assistant, B2B email or SMS tier. Accuracy caveat: no study of Plantower or Sensirion sensors on sawdust was found. The SPS30 is precise but reads high in occupational settings and is weak on coarse particles; a cotton-dust study found Purple Air and Dylos counts uncorrelated with gravimetric samplers ([PMC9030129](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9030129/), search snippet). Ship with the statement that it estimates dust trends, is not a compliance, safety or health instrument and does not replace OSHA-method sampling. Silica detection must not be claimed. Cheapest first proof: test the SPS30 against a filter-cassette sample in the founder's own shop on sanding, table saw and planer.

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| B2B demand | 3 | 2 | Reachable buyers exist, but no OSHA monitoring mandate, compliance buyers want gravimetric gear, no business quotes |
| B2C demand | 3 | 3 | Forum evidence of repeat purchase and comparison of $40-300 monitors, but a "relative use" mindset caps price |
| Shared hardware | 5 | 5 | Same board with firmware, enclosure and accessory variants |
| Buildable solo | 5 | 4 | Needs a dust-calibration test rig and the sensor raises BOM |
| Founder fit | 5 | 5 | Electronics, maker channel, local-first, camera-free |
| Total | 21 | 19 | Down on B2B demand and buildability |

## Shore-Power Watch

*A read-only, battery-powered clamp monitor of shore-cord current and residual (leakage) current with logging, for RV and boat owners and for marinas, campgrounds, boat clubs and charter fleets.*

### Buyers

**B2C:** RV: 8.1M RV-owning US households in the 2025 Go RVing/Ipsos study versus 11.2M in 2021 (methodology changed, not comparable); median owner age 49, 30 days use a year ([RV Travel](https://www.rvtravel.com/2025-rv-demographics-1199/)). Boats: 11.8M registered and documented boats in 2024 plus about 3.6M non-registered (NMMA via Marina Dockage). Only boats at slips with AC shore power are addressable, with no count found. Owner decides and pays at retail (Camping World, Amazon, etrailer) or on forum advice.

**B2B:** No reliable marina count: a 61,000-plus aggregator figure is unverified and likely includes marine businesses, and no NMMA or Census marina count was found. RV parks and campgrounds: about 4,400 RV campgrounds (Census CBP 2016), about 4,970 for NAICS 721211 (aggregator), 15,276 for the broader IBISWorld category. Deciders: the marina owner or manager with the electrician or engineer. Scale examples: a Richmond, California marina priced power-center replacement at $1,000-1,500 per slip; a Washington city priced metering plus receptacles for 42 pedestals at $38,584 (about $919 each, my arithmetic).

### Competitors

**B2C:** RV owners already have monitors that also protect.

| Product | Price | Notes |
|---|---|---|
| Progressive Industries EMS | About $135 portable, $178 hardwired on listings; $261-349 across retailers in earlier notes | Over/under voltage and reverse polarity; a 2026 guide rates the PT30X best 30A portable |
| Hughes Power Watchdog | Not captured | Bluetooth or Wi-Fi, free app, auto shutoff, no subscription found |
| Southwire Surge Guard | $269.99-344.99 | Bluetooth; owners report pairing and Android 13 problems |
| ShockAlarm (boats) | About $129 (earlier forum figure $59-99) | Floating voltage-in-water alarm; Practical Sailor and ESDO skeptical |
| Garmin OnDeck | About $50-60 hardware | Connected or lost only; paid plan, UK listing GBP 12.99-19.99 a month |
| Maretron ACM100 | Not captured | Voltage, current, frequency, power; separate cloud subscription |

Sources: [Bound by Flame, Oct 2026](https://boundbyflame.com/best-rv-electrical-management-systems/), [Camping World](https://www.campingworld.com/power-watchdog-gen-ii-50-amp-wifi-portable-surge-protector-with-auto-shutoff-154741.html), [Freeport Marine](https://www.freeportmarine.com/products/garmin-010-13009-08-ondeck-remote-monitoring-connectivity-shore-power-sensor-hard-wired.oembed), [Practical Sailor](https://www.practical-sailor.com/subscriber-only/preventing-electric-shock-at-the-dock). A handheld leakage clamp from Fluke class competes at $150-300 (estimate). No shore-power leakage monitor was found from Fireboy-Xintex.

**B2B:** Metering vendors sell billing, not leakage: Vutility (retrofit per-slip metering, "no recurring monitoring fees" (vendor), no price), Wild Energy and EKM Metering (pages blocked; EKM says cloud data free (vendor)), HarbaPower. VoltSafe Marine (retrofit pedestal-side connector; a snippet says it includes leakage detection; 2023 beta, current status unknown) is the closest competitor ([Boating Industry, 2023](https://boatingindustry.com/top-news/2023/06/22/voltsafe-seeks-marinas-for-shore-power-pilot-program/)). Pedestal makers: Hubbell, Leviton, Dock Products; D-Marin launched its own smart pedestals. Eaton and Marina Power and Lighting pricing: not found.

### Pain in buyers' words

**B2C:** Paraphrases only; Reddit, Amazon and Hull Truth and Cruisers Forum threads were not reached. RV side: false E7, E1 and E6 codes on Power Watchdog that clear when the unit is tapped, Bluetooth dropping across the rig, an unanswered support email (Trustpilot, Hughes); a false E8 with a Victron Multiplus unless a relay is disabled (Camping World listing); a Good Sam poster said an HW50C trips at once below its 104 V threshold. Boat side: a Cape Dory owner's GFCI tripped only when a neighbor's shore power was plugged in, traced to current in the water ([Cape Dory forum](https://capedory.org/forums/viewtopic.php?p=8919)); a poster measured about 61 mA on the green conductor ([Trawler Forum](https://www.trawlerforum.com/goto/post?id=1212232)); a North Carolina poster said the marina dismissed stray current.

**B2B:** No marina-manager or campground-owner quotes were found. Vendor marketing (Vutility) says managers need to recover electricity cost and bill slips accurately. Legal pain is documented: a wrongful-death complaint over a July 10, 2025 shock at Marina Shores at Dune Harbor, Indiana alleging no warning signs ([ECM](https://ecmweb.com/safety/article/55306558/lawfirm-files-wrongful-death-and-personal-injury-complaint-following-tragic-electrical-shock-at-marina-shores)); a Lake Vermilion, Minnesota swimmer death in July 2026 (suspected shock, no suit reported); a 2011 Traverse City case (city dismissed on immunity). The strongest code hook: NEC 555.35(D) requires a leakage-current measurement device where more than three receptacles supply boats, and a pedestal with a leakage indicator and alarm can satisfy it ([ECM](https://www.ecmweb.com/national-electrical-code/code-basics/article/55335551/nec-requirements-for-marinas-and-boatyards)). Note the 100 mA feeder and 30 mA receptacle figures conflict with one search summary; verify in the code book.

### Price and model

**B2C:** (estimate) Read-only must sit well below a $135-350 EMS: about $79-129 once for RV, no plan; $99-149 for a boat leakage clamp, where the value is diagnostic ("is it my boat or the dock"). RV demand for read-only is weak because Power Watchdog gives free app monitoring plus protection; the differentiator would be history logging and no cloud. The boat leakage clamp is the real consumer gap but a niche (fresh-water cruisers, liveaboards, owners who swim).

**B2B:** (estimate) Pedestal node $150-250 plus $0-3 per pedestal per month, since competing vendors give software free and a $2-4 fee would face free alternatives. The cheapest wedge is a staff audit tool (clip-on leakage meter logging per slip plus a portable gateway) at $199-299 once with a $99 a year report export, needing no install, no AHJ and no listing.

### Go-to-market

**B2C:** (estimate) Build in public on YouTube and ship at cost to 10 forum volunteers (Trawler Forum, Cruisers Forum, iRV2) who posted about leakage or low voltage, to learn the false-alarm rate. No marine retail channel is evidenced.

**B2B:** (estimate) Small freshwater marinas and lake campgrounds near the founder, reached through state marina associations, plus boat clubs and charter fleets where one buyer owns many boats. Free pilot, charge on proof. Whether campgrounds care (their pain is pedestal quality and guest complaints) is unevidenced beyond RVer posts.

### Kill criteria

**B2C:** (estimate) (1) Fewer than 100 preorders at $99 after a YouTube video with 20k+ views. (2) Fewer than 3 of 10 field volunteers say they would pay $99 at the observed false-alarm rate. (3) A competitor adds leakage or polarity logging to a free app.

**B2B:** (estimate) (1) Fewer than 3 of 20 marina managers say they would pay $150 or more per pedestal or $200 for an audit tool. (2) An electrician or insurer says only NRTL-listed fixed devices are acceptable and the quote exceeds $30k. (3) After 5 free pilots, fewer than 2 convert to paid.

### Shared hardware and v1

Identical: MCU with BLE (nRF52840 or ESP32-C6), residual-current CT with burden and ADC front end (target about 1 mA resolution, 30 mA threshold), 1-2 load CTs, flash logging, optional SX1262 LoRa, firmware. B2C portable: USB-C or 18650 battery, split-core clamps, IP54 case, BLE to phone with auto-reconnect and a local log buffer (addresses documented pairing and dropout complaints). B2B pedestal node: pedestal-side mount, low-voltage supply, LoRa to an owned gateway (about $199) at the marina office, per-slip ID, local web dashboard, no cloud.

Variant A (clamp-only, recommended): nRF52840 $6-9; SX1262 $4-6; residual-current split-core CT plus 2 load CTs $12-25 at 100 and $8-15 at 1,000; ADC front end $3-5; battery, charger and regulator $5-8; case, gasket, PCB $8-15. BOM about $45-75 at 100 units and $30-50 at 1,000 (precision CTs are the cost driver; the earlier $25-40 was low). Variant B (plug-through with voltage and polarity, isolated meter IC, mains PSU, 30/50 A connectors) is about $90-150 at 100 and $60-100 at 1,000 and is not recommended. Certification (estimate): Path A is FCC Part 15 (about $3-8k for unintentional testing), Bluetooth SIG listing ($0-8k depending on module reuse), optional UL 61010 report, labeled "monitor only, not a protective device." Path B adds NRTL listing, $15-50k and months, which breaches the "no heavy certification" exclusion. Alert path: BLE or LoRa to a local app and gateway dashboard; a monitoring-only clamp cannot measure voltage or polarity reliably. Liability caveat: read-only does not remove liability; if an owner relies on a quiet device and a swimmer is shocked, the claim is negligence or failure-to-warn. Make no "shock detector" or swimming-safety claims, avoid in-water sensing, insure (about $1-3k a year, unsourced guess). Applicable standard for a fixed monitor is unclear (UL 61010-2-032 covers hand-held clamps). Call UL, Intertek or MET before building.

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| B2B demand | 3 | 3 | Code duty and suits are real, but metering vendors give software free and no marina quotes exist |
| B2C demand | 4 | 3 | Large owner base, but RV side is well served and weak for read-only; boat leakage gap is niche |
| Shared hardware | 4 | 4 | Same sensing core; enclosure and radio role differ |
| Buildable solo | 3 | 2 | Precision residual-current sensing and mains-adjacent safety; clamp-only variant only |
| Founder fit | 3 | 3 | Radio and design suit it; electrical-safety liability and certification conflict with exclusions; no marine channel |
| Total | 17 | 15 | Lowest of the five |

## Comparison

| Idea | Old score | New score | B2B/B2C/Shared/Build/Fit | Strongest evidence | Biggest risk | BOM at 1,000 | B2B price | B2C price |
|---|---|---|---|---|---|---|---|---|
| Pet Heat Watch | 20 | 19 | 3/3/5/4/4 | Pennsylvania 7 Pa. Code 28a.4 hourly records; Waggle plan anger; multiple kennel and RV deaths | Pay-once breaks for cellular RV buyers; a missed alert on a dead animal | About $17.50 node, $15 hub | $249-449 kit, optional $9-15/site/mo (estimate) | $49-79 once, $99-129 with cell pack (estimate) |
| Water family | 20 | 19 | 3/3/5/4/4 | Water-claim data ($13,954 average); Moen's discontinued local-alarm sump monitor leaves a gap; Scout/bolt $90 insurer kit | $8-15 competitor sensors and insurer giveaways cap price; thin margin on the puck | $27-40 sump puck, $8-12 leak node | $149-199 bundle, $69 per puck, $2-5/property/mo (estimate) | $69-89 puck, $19-25 probes (estimate) |
| Machine Pulse | 20 | 18 | 3/2/5/4/4 | Vendors charge $240-1,200+ per machine per year; MachineMetrics uses the same CT method | No buyer voice on either side; DIY at $15-25; unproven run/idle accuracy | About $15.50 | $79-129 per node, $3-5/node/mo (estimate) | $39-59 once (estimate) |
| Shop Air Node | 21 | 19 | 2/3/5/4/5 | Forum threads show owners buy and compare $40-300 monitors; honest scope documented | Optical sensors unproven on sawdust; no OSHA mandate; high BOM | $60-75 | $150 per node, $5/node/mo (estimate) | $90-130 once (estimate) |
| Shore-Power Watch | 17 | 15 | 3/3/4/2/3 | NEC 555.35(D) leakage duty; wrongful-death suits; real stray-current complaints | Liability and certification pressure; precision sensing; read-only is weak for RV buyers | $30-50 (clamp-only) | $150-250 pedestal node, or $199-299 audit tool (estimate) | $79-129 RV, $99-149 boat (estimate) |

## Recommendation: what to prototype first

Prototype Pet Heat Watch, and name the Water family (Sump Puck) as runner-up. The scores tie at 19, so the reasons are the tie-breakers. Pet Heat Watch has the only confirmed legal mandate on the business side, the clearest consumer grievance (subscription plans and Wi-Fi gadgets that die with the power), the lowest BOM at about $17.50, and a simple node-plus-hub design that the Water family reuses. Shop Air Node has the best founder fit but a high BOM, a weak B2B case and unproven sensor accuracy on sawdust. Machine Pulse is cheap but has no buyer voice on either side. Shore-Power Watch conflicts with the exclusions. The main downside to accept: a life-safety liability, which the heartbeat alert, supplementary labeling and insurance must address.

First 30 days, both sides in parallel (all estimates):

| Days | B2C track | B2B track |
|---|---|---|
| 1-5 | Landing page with a refundable $29-49 deposit and a one-question survey: is cellular a requirement? Record one build-and-explain video with a heat and power-cut demo | Write a 5-question interview script; pull the Pennsylvania licensed kennel list if available; contact 10 kennels near you and 5 rescues |
| 6-15 | Post in RV and dog-owner groups and to your subscribers; post the free "RV dog heat" calculator; track email-to-deposit rate | Run 15-20 calls or visits to kennels; ask to see their current temperature log; offer a free 30-day pilot with 2-4 nodes |
| 16-25 | Build 5-10 hand-assembled nodes (ESP32 module, SHT4x, siren, battery, power-sense); bench-test power-cut alerts and a missed-heartbeat alarm | Place pilot nodes in 3 local sites and 1-2 rescues; start hourly SD logging on a hub |
| 26-30 | Count deposits against the 150 target; read survey results | Ask each pilot site if they would pay $200 or more or $9-15 a month; count paid pilots against the 3-of-40 gate |

Check this kill criterion first: the B2C survey result that more than 40% of respondents require cellular. It needs only a landing page and about 10 days, and if it fails it breaks the pay-once promise before any hardware is built. Check second the B2B gate of fewer than 3 paid pilots from 40 Pennsylvania kennel contacts, which needs the cold-outreach count to reach 40 first, so it will resolve later than day 30. If the cellular share is high, shift the product to home and stationary-RV use only, or move to the Water family, which has no cellular dependence for its core case.

## Shared platform

These five ideas share a small set of blocks, so most of the work carries across.

| Block | Used by | Notes |
|---|---|---|
| ESP32-C6 or nRF52840 pre-certified module with BLE | All five | Core node; Wi-Fi for local network, BLE for phone |
| SX1262 LoRa module and a small hub (ESP32, LoRa, SD, Ethernet or Wi-Fi, local siren, backup battery) | Pet Heat Watch, Water family, Shore-Power Watch (B2B) | Node-to-hub link; hub logs locally and serves the dashboard |
| Piezo siren and driver, battery tray, power-loss sense | Pet Heat Watch, Water family | The outage-proof local alert is the shared differentiator |
| Missed-heartbeat watchdog | Pet Heat Watch, Water family, Shore-Power Watch | Silent offline failure is the main complaint against incumbents |
| Split-core CT with ADC front end (ADS1115 class) | Machine Pulse, Shop Air Node, Water family (pump current), Shore-Power Watch | Non-contact current sensing; a precision residual-current variant is the cost and risk driver for shore power |
| Particle, VOC and mic sensor head | Shop Air Node | Adds the most cost |
| Temperature and humidity sensor (SHT4x) | Pet Heat Watch, Water family (freeze), Shop Air Node | Cheap |
| Local firmware, MQTT and Home Assistant integration, free local dashboard | All five | One codebase; per-product thresholds and labels |
| Optional paid tier: SMS and voice call-out, PDF and CSV export, multi-site view, retention | All five on the B2B side | Simple per-site or per-node subscription; local use stays free |

One platform could serve several products with a hardware change of sensor head and enclosure only. A single "node plus hub" core would ship as Pet Heat Watch first, then as the Sump Puck (add a pit-level sensor and CT clamp), then as Machine Pulse (drop the siren and LoRa, keep the CT), with Shop Air Node as a sensor-head variant. Shore-Power Watch would use the same MCU and CT block but needs the precision residual-current front end and the liability review, so it should come last or not at all. A cheap side test worth running on the same bench: log an SPS30 against the CT clamp in your own shop, since it validates two products with one setup. Platform risk: supporting five product lines as a solo founder is a support and certification burden, so commit to one SKU family at a time.

## Forums to read personally

The research could not reach most forums, Reddit, Amazon reviews or Trustpilot; no direct buyer quotes exist for most ideas.

- **Reddit r/RVLiving, r/RVLife, Escapees, iRV2, Good Sam and Forest River forums:** how much RV owners resent Waggle and Necto fees, what they would pay once, how many need cellular, and what happens when campground power fails. iRV2 and Forest River returned 403 errors.
- **Waggle, Necto and Power Watchdog reviews on Amazon and Trustpilot:** the missing "pain in own words" for pet and RV monitoring, and dated complaints on false alerts and offline devices.
- **Kennel, groomer, boarding, shelter and rescue groups, and state kennel inspector pages:** whether temperature logging rules exist beyond Pennsylvania, how kennels log today, and what they would pay.
- **r/BasementFlooding, r/HomeImprovement, r/landlord, BiggerPockets, Airbnb Community:** whether landlords and homeowners want an outage-proof sump sensor, what they pay, whether a $10 YoLink sensor is enough, and how they react to subscriptions.
- **Sump pump installer and plumber groups, regional insurance mutuals and program vendors:** whether insurers require UL or ETL, activation proof or cloud APIs.
- **r/homeassistant, r/hobbycnc, r/lasercutting, r/3Dprinting, Bambu forum, Carbide 3D and xTool communities:** whether anyone wants run/idle monitoring from a clamp instead of building it, and for which machines.
- **Practical Machinist, r/machinists, makerspace boards and MEP advisors:** whether small shops would pay for monitoring, what decision they would change, and who in a makerspace would buy.
- **Sawmill Creek, Festool Owners Group, Lumberjocks, r/woodworking, UK Workshop:** whether a per-tool dust and noise logger beats a $60 monitor, and how owners judge accuracy and fire risk.
- **Insurance loss-control reps and cabinet-shop owners:** whether any would accept logs as housekeeping evidence.
- **Trawler Forum, Cruisers Forum, The Hull Truth, Cape Dory and Sailboat Owners forums:** boat owners' stray-current experiences and whether they would pay for a leakage clamp.
- **Marina managers, state marina associations and campground owner groups:** whether they would pay for a pedestal node or audit tool and who signs off.

## Method and limits

Five deep-dive research passes used web search and page fetches only, with the earlier hybrid screen as background. Reddit, Trustpilot, Amazon review pages and many trade forums returned errors or could not be reached, so there are no verbatim buyer quotes for any idea; pain sections are paraphrase from search snippets and mostly undated. Several pages were read only as search snippets. All BOMs, buyer pools for the new products, prices for the proposed products, battery life, certification costs and lab costs are (estimate) and need distributor quotes and a lab call. Competitor prices come from vendors, resellers, deals pages and affiliate reviewers at different dates and may be stale. Legal points (NEC Article 555, Pennsylvania 28a.4, OSHA) were read through secondary sources or snippets in some cases and are not legal advice; verify in the code or regulation text. Scores for the three tied ideas (19 each) are judgement calls, not measurements. Nothing here was tested on hardware.
