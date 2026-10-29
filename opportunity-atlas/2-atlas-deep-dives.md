# Atlas Deep Dives

**Prototype the STR noise and occupancy puck first.** Deeper research lowered four of the five scores from the 2026-10-28 screen and left only the clamp-on CNC monitor at 20/25. The CNC monitor now has the best on-paper score and the most open space: no cheap, local-first, one-time clamp-on product was found, and the only one-time incumbent (Vorne XL) costs $4,490-4,990. But its buyer evidence is the thinnest of the five. It has no independent shop-owner voice, no proof that small shops spend money, and no published accuracy for detecting run/idle/off from current draw. The STR puck scores 19/25. It has the best mix of dated, first-person pain from 2026 (subscription anger, billing errors, lock-in), proven host spending ($60-180 per home per year to Minut), a B2C one-time price that matches the founder's model, a design object that guests will see, and a launch test (paid deposits from the YouTube audience) that one person can run in 90 days. Its biggest risk is open space: Layla already advertises one-time sensors at $149-299, though an affiliate review says a paid plan is needed after 12 months. Settle that first by buying a Layla and a Minut in week one. Crew Beacon Tag (16) and Unit Door Sentinel (17) fell furthest, because free phone photos and entrenched bundled alarm vendors weaken willingness to pay. The school aerosol sensor (18) has real money and loud complaints, but Triton ULTRA already sells local-only with no required subscription, and district procurement is slow. Run the CNC monitor second, on the same ESP32-plus-local-hub firmware.

Score key used throughout: **P** = pain, **W** = willingness to pay, **O** = open space, **B** = buildable solo, **F** = founder fit, each 1-5. "(vendor)" marks a figure from a company selling in the category; "(estimate)" marks the researchers' own unsourced reasoning; "not found" means the research looked and came up empty.

## Crew Beacon Tag

Flat-fee NFC/BLE proof-of-visit tag that lawn, cleaning and guard crews tap at each client site to produce a signed, non-clonable visit record.

### Buyers

Segment counts conflict by 2x or more depending on definition. The realistic addressable base is employer firms with recurring routes.

| Segment | Count (source, year) | Who decides / how they buy |
|---|---|---|
| Landscaping, NAICS 561730 | **117,969 employer establishments, 802,899 employees** (Census CBP 2023 via aggregator, [Vanta Insights](https://vantainsights.com/industry/561730-landscaping-services)); 516,572 nonemployer operators (Census Nonemployer 2023, secondary, [Startbusinessbystate](https://startbusinessbystate.com/landscaping-industry-statistics/)); total-business counts conflict: 556,238 (2026, [IBISWorld](https://www.ibisworld.com/united-states/number-of-businesses/landscaping-services/1497/)) to 726,565 (2025, [Aspire](https://www.youraspire.com/blog/landscaping-industry-statistics)) | Owner or ops manager; trade shows, software resellers (screen). Budget: not found |
| Janitorial, NAICS 56172 (561720 not published separately) | **67,799 establishments, 1,088,193 employees** (CBP 2023, [Vanta Insights](https://vantainsights.com/industry/561720-janitorial-services)); 61% of establishments under 5 employees (2023, low confidence, [Mewayz](https://data.mewayz.com/industry/janitorial-services/)); 1,227,883 incl. nonemployers (2025, [IBISWorld](https://img3.ibisworld.com/united-states/number-of-businesses/janitorial-services/1496)) | Owner; titles beyond owner not found |
| Security guards, NAICS 561612 | **11,104 establishments, 799,400 employees** (CBP 2023, [Vanta Insights](https://vantainsights.com/industry/561612-security-guards-and-patrol-services)); about 9,500 (year not stated, [First Research](https://www.firstresearch.com/Industry-Research/Security-Guard-Services.html)); 7,707 firms / 10,659 establishments (year not stated, [Mewayz](https://data.mewayz.com/industry/561612)) | Owner or ops; large contracts formal. Risk pool PRISM resells discounted Guard1 to members ([PRISM](https://www.prismrisk.gov/services/risk-control/partner-programs/checkpoint-system/guard-1/)) |

NALP's 2025 benchmark puts finding qualified employees as the top concern (55%) and direct labor as the largest cost ([NALP](https://blog.landscapeprofessionals.org/gain-competitive-insights-with-the-2025-financial-benchmark-report/)). The realistic early buyer is the owner of a 5-50 person lawn or cleaning company with 20-200 recurring sites (estimate). Guard firms already own a tour system, so the tag is a replacement sale there, not a new one.

### Competitors

The category is crowded and mostly phone-first. Cheap flat-fee tag-and-app combos already exist.

| Product | Hardware price | Subscription price | Strengths | Top complaints |
|---|---|---|---|---|
| PatrolTech | Not found | Free for 5 checkpoints; Pro $29/mo for 10 + $2 each extra; Business $79/mo for 40 ([Slashdot](https://slashdot.org/software/p/PatrolTech/)); Capterra shows "from $3, usage-based" (conflict, [Capterra](https://www.capterra.ie/software/1071796/PatrolTech)) | Cheapest flat fee; sets the ceiling | Not found |
| Silvertrac | Not found | $249/mo flat, up to 10 devices, no trial (2026, [Capterra](https://capterra.com/p/135436/Silvertrac-Software/pricing/)) | 4.7/5 from 279 reviews | Data-entry heavy at start; too pricey to bundle into a standard service ([Capterra](https://capterra.com/p/135436/Silvertrac-Software/reviews/)) |
| Guard1 | No list price; Real Time Base System $4,995, Android licence $395 ([Capterra IE](https://www.capterra.ie/software/109708/guard1)); packages about $995-5,995 ([SoftwareFinder](https://softwarefinder.com/facility-management-software/guard1)); "from $99 per user, one-time" ([GetApp](https://www.getapp.com/all-software/a/guard1/)). Sources conflict | Not found | Legacy incumbent; risk-pool channel | Not found |
| QR-Patrol | n/a | About EUR 2.20 / 4.40 / 8.29 per guard per month (aggregator, [Capterra](https://www.capterra.com/p/144995/QR-Patrol/pricing/)) | Cheap per guard | Not found |
| Miratag | Not found | Not found | Proximity NFC against copied codes (vendor, [Miratag](https://miratag.com/en/blog/nfc-guard-tour-system-patrol-verification)) | Not found |
| Scan4Clean / Janitorial Manager | Quote only | Quote only | QR + NFC built for cleaning (vendor, [Janitorial Manager](https://www.janitorialmanager.com/work-management-system/scan4clean/)) | Not found |
| Linxup vehicle GPS | $69 tracker month-to-month, free on 3-yr contract (vendor) | $25/vehicle/mo (vendor, [Linxup](https://www.linxup.com/pricing)) | Proves vehicle presence | Hard-to-cancel contract, billing disputes ([BBB](https://www.bbb.org/us/mo/chesterfield/profile/fleet-services/linxup-0734-310605225)); Capterra 3.9 (88 reviews) |
| LMN / Aspire / Jobber suites | Not found | Not found | Owners already pay for them; Jobber 4.6/5 from 1,420 reviews ([Software Advice](https://www.softwareadvice.com.au/compare/3660/142804/jobber-lawncare/vs/lmn)) | LMN time tracking "never worked" ([Software Advice](https://www.softwareadvice.com/landscaping/lmn-profile/reviews)); Aspire "price is high" ([Capterra](https://www.capterra.com/p/161544/Aspire/reviews/?page=6)) |
| Free: timestamped photos, door tags | $0 | $0 | Already habit ([RazorSync](https://www.razorsync.com/resources/can-you-prove-the-service-was-provided/), [Clip](https://clip.com/but-you-werent-here-how-to-prove-you-did-your-job/)) | Contestable |

CleanScan, SimplePatrol, Teambridge (geofenced proof of service), Trackforce and Therms also exist; their prices were not found. GPS logs alone are contestable: a BC tribunal weighed a lawn company's GPS record of a roughly 6-minute visit against the lawn's size ([CRT](https://decisions.civilresolutionbc.ca/crt/crtd/en/485143/1/document.do)). No product was found that sells a flat-fee, non-clonable, local-first site tag aimed at lawn and cleaning crews. That gap is a positioning gap, not an empty category.

### Pain in buyers' words

| Paraphrase | Source | Date |
|---|---|---|
| Customer disputed a mow using a photo taken two days later; owner says mower lines are visible; $45 job unpaid | [LawnSite 503826](https://www.lawnsite.com/threads/customer-claims-i-didnt-cut-his-grass-and-will-not-pay.503826/) (search snippet) | Not shown |
| Commenters: put a front-lawn photo on the invoice; show GPS and camera footage; get a text admitting payment | Same thread | Not shown |
| Send an attorney letter by certified mail, then small claims, or drop the customer | [LawnSite 457540](https://www.lawnsite.com/threads/empty-threat-customer-wont-pay.457540/) | Not shown |
| Clients ask guard firms "can you prove someone was here"; guards photograph and share codes to fake patrols (vendor) | [Miratag](https://miratag.com/en/blog/guard-tour-system-patrol-verification-guide) | Not shown |
| NYCHA guards missed shifts and falsified handwritten timesheets | [NYC DOI](https://nyc.gov/assets/doi/reports/pdf/2025/14NYCHASecurityFireReleaseRpt03.26.2025.pdf) | 2025 |
| Florida appeal turned on guard-tour records showing two check-ins in two hours | [FindLaw](https://caselaw.findlaw.com/fl-district-court-of-appeal/1651188.html) | Not shown |

Lawn disputes are frequent but small ($45 in the one cited case). Guard and janitorial disputes carry contract-loss and liability stakes, which is where willingness to pay is likelier (estimate). Dispute frequency and dollar cost per dispute: not found. LawnSite threads 459192, 512717 and 487646 were titles only.

### v1 product sketch

Two architectures (estimate). **Option A** is a passive, sealed NTAG 424 DNA tag in a designed housing. NTAG 424 DNA signs each read with AES-128 CMAC, so a copied code fails (vendor claim, [WakDev](https://www.wakdev.com/en/knowledge-base/nfc-chips/nxp-ntag424-dna.html)). The phone taps it, verifies locally and keeps the signed log on-device or in the owner's own storage. No battery, almost no firmware. **Option B** adds a BLE beacon (nRF52 + secure element + coin cell) for hands-free logging.

| Part | Price (source, year) |
|---|---|
| Raytac MDBT42Q (nRF52832) | $4.95 qty 1 (Digi-Key via [Flux](https://www.flux.ai/jecstronic/mdbt42q-512kv2.md), date unclear); $9.93 ([Farnell](https://il.farnell.com/seeed-studio/317030213/bluetooth-module-ble-4-2-2msps/dp/3932109)) |
| Raytac MDBT50Q-1MV2 (nRF52840) | $9.45 qty 1 ([TME](https://www.tme.com/us/en-us/details/mdbt50q-1mv2/iot-wifi-bluetooth-modules/raytac/), 2026-10-29) |
| ATECC608B secure element | $1.36 qty 1, $1.28 at 100+ ([LCSC](https://www.lcsc.com/product-image/C1020341.html)) |
| NTAG 424 DNA finished tag | EUR 0.20-0.23 at MOQ 5,000 (Alibaba, unverified, [Alibaba](https://spanish.alibaba.com/f/nxp_67.html)); chip-only: not found |
| CR2032 | $0.0365 (no-name, [LCSC](https://www.lcsc.com/product-image/C70373.html)) to $0.2510 (Panasonic, Mouser via search) at 100 pcs |
| PCB, enclosure, assembly | Not found |

Sourced Option B parts total about $6-7 before PCB, enclosure and assembly (estimate). Full BOM at 100 and 1,000 units: not found. Option A's unit cost is dominated by the housing, likely well under $5 at 1,000 (estimate). Pre-certified Raytac modules keep the FCC path to modular approval plus Part 15B; grant IDs were not verified.

**B2B:** $12-20 per tag one-time, local verification app free; optional $29/mo for 25 sites only if a hosted log is wanted (screen hypothesis, unvalidated). PatrolTech's $29/mo for 10 checkpoints is the ceiling.

**B2C:** $25 tag for homeowners to log cleaner or lawn visits (screen hypothesis, unvalidated).

### Go-to-market

The main shows have already happened this year. Equip Exposition ran Oct 20-23, 2026 in Louisville, with attendance reported at 29,535 or 50,000 (conflict). It rotates to Orlando in 2029 ([Total Landscape Care](https://www.totallandscapecare.com/home/article/15827757/equip-exposition-dials-up-fun-with-three-nights-of-epic-entertainment), [Construction Business Owner](https://www.constructionbusinessowner.com/equip-exposition-announces-2-city-rotation-starting-2029/)). GSX ran Sept 14-16, 2026 in Atlanta (about 15,000 expected, 500+ exhibitors), and GSX 2027 is in Orlando ([SecuritySales](https://www.securitysales.com/news/gsx-2026-builds-on-previous-successes-adds-new-elements/620460/), [GSX](https://www.gsx.org/faqs/)). ISSA Show 2026 dates: not found. Associations are NALP, ISSA and ASIS. Insurers and risk pools such as PRISM are an untested channel. For the first 10 customers (estimate): find lawn and cleaning owners who post dispute threads, plus 2-3 small guard firms unhappy with Silvertrac's price, and give them free tags for a 60-day pilot in exchange for their dispute logs.

### Kill criteria

| # | Test | Stop if |
|---|---|---|
| 1 | Interview 20 owners with 20+ recurring sites | Fewer than 5 lost money to a "didn't do it" dispute in the last 12 months |
| 2 | 60-day free pilot with 10 users | Fewer than 3 will pay $12+ per tag (or $29/mo) instead of using free photos |
| 3 | Unit cost and field reliability | Cost at 1,000 units above about 1/4 of retail, or over 5% failed taps in rain or dirt |

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| P | 4 | 4 | Disputes documented in forums, tribunals and vendor material, but each is small ($45) and Reddit was unreachable |
| W | 3 | 2 | Free photos and GPS in suites owners already pay for; PatrolTech's $29/mo sets a low floor; no unmet paid demand found |
| O | 3 | 2 | PatrolTech, QR-Patrol, Miratag, Scan4Clean, CleanScan and Guard1 exist; only the anti-clone, flat-fee, local-first angle is open |
| B | 5 | 5 | Pre-certified modules; the passive NTAG option needs almost no firmware |
| F | 4 | 3 | Design and privacy fit, but lawn, janitorial and guard owners are far from a maker YouTube audience (estimate) |
| **Total** | **19** | **16** | |

## Unit Door Sentinel

Battery LoRa sensor on each self-storage unit door (reed switch plus accelerometer) that reports opens and prying to a site hub. No camera.

### Buyers

| Segment | Count (source, year) | Who decides / how they buy |
|---|---|---|
| All US self-storage facilities | **57,981 facilities, 2.65B rentable sq ft** (Radius+ in Self-Storage Almanac 2025, [MSM](https://digital.modernstoragemedia.com/almanac/self-storage-almanac-2025ok/section-1-industry-data)) | n/a |
| NAICS 531130 establishments | **18,564 establishments, 48,382 employees** (CBP 2023 via aggregator, [Vanta Insights](https://vantainsights.com/industry/531130-lessors-of-miniwarehouses-and-self-storage-units)). Counts companies' establishments, not facilities, so it is far below the 57,981 figure | n/a |
| Independents and small operators (target) | ~43,939 properties = **65.7% of facilities, 46.2% of sq ft** (TractIQ via [CRE Daily](https://www.credaily.com/?p=222836), ~2025, snippet); ~65% of facilities, ~40% of sq ft ([Neighbor](https://www.neighbor.com/storage-blog/self-storage-industry-statistics/), 2024) | Owner or manager, but purchase usually flows through the security or software vendor; sensors are pre-set by unit number and install in under 5 min per door ([ISS](https://www.insideselfstorage.com/suppliers-products/converting-to-a-wireless-door-alarm-system-in-self-storage-benefits-pitfalls-and-other-considerations), 2010) |
| REITs | 16.3% of properties, 29.4% of sq ft (TractIQ via CRE Daily); four REITs + U-Haul hold 35.5% of inventory ([RentCafe](https://www.rentcafe.com/blog/self-storage/the-100-largest-self-storage-companies-in-the-u-s/), 2025) | National contracts; long sales |

Per-door budget anchors are weak. The best current one is SpiderDoor's S55A motion alarm at **$140 + $2/month** (vendor, 2026, [SpiderDoor](https://contact.spiderdoor.com/self-storage-alarms)). StorageCafe says operators "usually charge between $150 and $250 per month" as a tenant alarm premium (2025, [StorageCafe](https://www.storagecafe.com/blog/wp-json/wp/v2/posts/743)). That is implausibly high for a door alarm and likely mislabeled, so treat it as unverified. Pre-2002 figures ($40-100 per door) are too old to use. A generic non-storage benchmark is $70/sensor + $250/hub + at least $100/mo (vendor, [AwareBuildings](https://www.awarebuildings.com/door-activity)). Storable (SiteLink/storEDGE) runs an API partner process, and current integration fees were not confirmed ([Storable](https://storable.com/products/software-integrations)). Third-party manager counts and the SSA fact sheet: not found.

### Competitors

| Product | Hardware price | Subscription price | Strengths | Top complaints |
|---|---|---|---|---|
| PTI Security | Not found | Not found | 40+ years, 40,000 installations (vendor, [ISS 2022](https://www.insideselfstorage.com/security/wireless-door-alarms-fortifying-your-self-storage-facility-and-improving-operational-prudence)); wired + wireless, cloud CORE platform | Battery life, frequency: not found |
| SpiderDoor | S55A motion $140; S33C door alarm "contact for pricing" (vendor) | $2/mo (S55A) | Mesh, 3-5 yr battery, 20-30 ft range; 6,800+ facilities (vendor, [SpiderDoor](https://contact.spiderdoor.com/self-storage-alarms)) | Needs powered internet gateway |
| OpenTech INSOMNIAC | One-time "low cost" fee, amount not found | None | Connects existing wired alarms, 96 channels ([OpenTech](https://opentechalliance.com/solutions/insomniac-unit-alarms/)) | Wired retrofit only |
| Janus Nokē | Quote only | Quote only | Locks + sensors + portal; 500K+ devices (vendor, [Janus](https://www.janusintl.com/news-media/blog/noke-surpasses-500k-devices-installed-and-earns-5th-innovation-award)) | Not found |
| Sentinel Systems | Not found | Not found | Hard-wired at construction | Says its wireless experiment failed on reliability ([ISS 2017](https://www.insideselfstorage.com/security/straight-talk-about-individual-door-alarms-self-storage-facilities)) |
| Quikstor, DaVinci Lock | Not found | Not found | Bundled with management software | DaVinci has 398 Trustpilot reviews, unread |
| YoLink (consumer LoRa) | Starter kit $35.70-49.99; outdoor contact $24.99 (retail, 2024-26, [Slickdeals](https://slickdeals.net/f/17636304-amazon-com-yolink-lora-smart-door-sensor-starter-kit-1-4-mile-open-air-range-door-left-open-reminders-5-years-battery-life-sms-text-email-app-alerts-alexa-49-99)) | None | 5-yr battery (vendor), ~1/4 mile, hub handles 300+ devices | Consumer cloud app, no storage-software integration |

The trade-press complaints are dated. Wireless batteries get changed "once a year or so," with cold weather the main concern, and false alarms depend on installation ([MSM 2018](https://www.modernstoragemedia.com/blog-post/sound-alarmor-not-individual-door-alarms-add-value-storage-facilities); ISS 2010). Sagging roll-up door rubber causes misalignment and false alarms ([ISS 2019](https://www.insideselfstorage.com/security/a-preventive-maintenance-plan-for-your-self-storage-security-system)). No competitor shows accelerometer pry analytics, but SpiderDoor advertises a "tamper-proof design." The differentiation would be false-alarm filtering and 5+ year battery life, not LoRa itself.

**Premise correction:** the screen's Janus figure (~1,100 units for ~$310K) was not reproduced this round. The screen's claim that operators "complain about batteries and false alarms" rests on Self-Storage Talk snippets that could not be opened (403), plus trade articles from 2010-2019.

### Pain in buyers' words

| Paraphrase | Source | Date |
|---|---|---|
| 85% of owners/operators are concerned about theft; 57% had repeated break-ins (survey) | [MSM](https://digital.modernstoragemedia.com/messenger/july-2025/the-rising-tide-of-self-storage-crime/) | Jul 2025 |
| Survey of 100+ operators headlined "fewer incidents, more security" | [MSM](https://www.modernstoragemedia.com/msm-exclusives/crime-crackdown-msm-survey-reveals-fewer-incidents-more-security) | Sept 2025 |
| SST members are discussing unit-alarm revenue, retrofit challenges, liability (no quotes) | [ISS](https://www.insideselfstorage.com/security/the-bonus-benefits-of-tighter-security-self-storage-operators-discuss-the-revenue-potential-for-individual-unit-alarms) | 2026-02-25 |
| Tenant lost $22,000 of belongings; some policies exclude losses without signs of forced entry | [WWBT](https://www.12onyourside.com/2026/05/27/henrico-woman-says-22000-belongings-stolen-storage-unit/), [Yahoo](https://www.yahoo.com/news/articles/sheriff-office-warns-rise-storage-140732431.html) | 2026-05-27 |
| Main wireless worry is frequent battery replacement, especially in cold weather | [ISS](https://www.insideselfstorage.com/suppliers-products/converting-to-a-wireless-door-alarm-system-in-self-storage-benefits-pitfalls-and-other-considerations) | 2010 |

The forced-entry insurance exclusion is the most interesting new angle: a pry log could become evidence for the tenant's claim (estimate). Verbatim operator complaints with dates and cost per incident: not found.

### v1 product sketch

| Part | Price (source, year) |
|---|---|
| Seeed Wio-SX1262 LoRa module | ~$3.89-4.29 ([Pakronics](https://www.pakronics.com.au/products/wio-sx1262-wireless-module-bulk-sx1262-embedded-supports-lora-lorawan-on-eu868-us915-ss114993390), [ThinkRobotics](https://thinkrobotics.com/products/wio-sx1262-wireless-module-sx1262-embedded)) |
| ST LIS2DH12 accelerometer | $0.22 at 1,000+ ([LCSC](https://datasheet.lcsc.com/lcsc/STMicroelectronics-LIS2DH12TR_C110926.pdf), unauthorized, verify); $0.55 ([HQOnline](https://www.hqonline.com/product-detail/gyroscopes-st-lis2dh12tr-2500237367)); $0.91 on an 8,000 reel ([DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/LIS2DH12TR/4899838)) |
| EVE ER14505 Li-SOCl2 cell | EUR 3.50 / 3.00 / 2.75 at 1 / 10 / 25 pcs ([Ormix](https://ormix.lv/en/catalog/GG0111?page=5)) |
| Reed switch, PCB, enclosure | Not found |
| Hub option: RAK7268C US915 LTE gateway | $234, excluding shipping and 25% import tariffs ([Rokland](https://store.rokland.com/collections/rakwireless-products/products/rak-wireless-wisgate-edge-lite-2-indoor-gateway-for-lorawan-rak7268c-us915)) |
| Hub option: Raspberry Pi Zero 2 W | About $15 ([Magazin Mehatronika](https://magazinmehatronika.com/en/the-2026-raspberry-pi-pricing-and-buying-guide/), 2026); LoRa concentrator HAT price not found |

Sourced node parts come to about $7-8 before the reed switch, MCU, PCB and housing (estimate). Do not publish a 100/1,000-unit BOM until PCBWay and LCSC quotes are in. Battery sizing has real anchors. Semtech's worked door-sensor example needs **1,091 mAh for 5 years** at 5 µA sleep ([Semtech](https://lora-developers.semtech.com/library/tech-papers-and-guides/the-book/example-select-a-battery)). Netvox R311A claims 5 years at 20 triggers a day on two CR2450 cells (vendor, [LoRa Alliance](https://lora-alliance.org/wp-content/uploads/2019/09/R311A_DataSheet.pdf)). Dragino LDS01 on a CR2032 targets about 1 year ([Helium](https://docs.helium.com/network-iot/devices/ready-to-use/dragino/lds01)). A CR2032 design would recreate the incumbents' battery complaint. Certification caveat: a module's modular grant is tied to its listed antenna ([Switch Science](https://www.switch-science.com/collections/all/products/9669)). The heavy work is software: supporting 200+ nodes, OTA updates and the Storable integration.

**B2B:** $15-25 per door one-time + $1/door/mo, or per-door one-time plus a per-site hub fee (screen hypothesis, unvalidated). SpiderDoor's $140 + $2/mo motion alarm is the ceiling, which leaves room to price up.

**B2C:** $39-59 stand-alone tenant alarm (screen, unsourced). Weak, because tenants cannot fit sensors to facility-owned doors without the owner's consent.

### Go-to-market

The SSA Fall Conference ran Sept 8-11, 2026 at Aria, Las Vegas. 2027 is reported for Sept 7-10, less reliably ([StoragePUG](https://www.storagepug.com/events/ssa-2026-fall-conference), [SSA](https://www.selfstorage.org/Events-Education/Events)). ISS World Expo was listed for April 8-9, 2026 (one aggregator, unconfirmed, [Neventum](https://www.neventum.com/tradeshows/iss-inside-self-storage-world-expo)). State conferences exist (NYSSA, TNSSA, AZSA, WSSA, [StoragePUG](https://www.storagepug.com/events/nyssa-2026-conference)). The channels are management-software vendors and gate/security installers. For the first 10 customers (estimate): 3-5 independents whose wired alarms have failed, each offered a free 20-door pilot; 3-5 from state-association outreach; and 1-2 through a small gate installer paid a margin. Distributor margins: not found.

### Kill criteria

| # | Test | Stop if |
|---|---|---|
| 1 | Interview 20 independents (50-500 units) | Fewer than 5 confirm battery/false-alarm pain and will pay $25/door + $1/mo |
| 2 | Pilot 100+ doors at 2 sites for 12 months | More than 2% false alarms per door per month, or any battery or radio failure |
| 3 | Integration path in 90 days | No Storable or PTI/OpenTech path, or fees push gross margin below 50% per door: shrink to a stand-alone hub dashboard or close |

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| P | 4 | 3.5 | Theft concern is high (85%/57%), but battery and false-alarm complaints come from 2010-2019 articles, and a 2025 survey reports fewer incidents |
| W | 4 | 3 | Only SpiderDoor publishes a price; OpenTech offers a $0-monthly retrofit |
| O | 3 | 3 | SpiderDoor, PTI, OpenTech, Quikstor, Sentinel and Janus bundles; the opening is filtering and battery life |
| B | 5 | 4 | Hardware is easy; 200+ nodes, OTA and integration are real software load |
| F | 4 | 3.5 | Local-first fit is real, but B2B sales through installers and trade shows is a mismatch for a solo YouTuber |
| **Total** | **20** | **17** | |

## STR noise and occupancy puck

Decibel-only noise plus occupancy sensor for short-term rentals. No audio stored, local-first alerts, one-time price.

### Buyers

| Segment | Count (source, year) | Who decides / how they buy |
|---|---|---|
| All US STR hosts | Screen's ~2.46M listings / 785K hosts (2023) is **unverified**: the cited [Airbtics](https://airbtics.com/short-term-rental-market-report-2025-the-united-states) page shows no national total, only 18.72% supply growth (2025 data, Jan 2026). AirDNA says 3.3% growth in 2025 (snippet, [Skift](https://skift.com/2025/01/30/where-to-invest-in-short-term-rentals-in-2025-airdnas-top-u-s-markets/)) | Host; Amazon, direct, PMS marketplaces (channel split not found) |
| Single- and few-listing hosts | Airbnb treats 1-20 listings as "individual" hosts ([Yahoo](https://ca.news.yahoo.com/airbnb-hosts-run-over-20-124101648.html), date unclear); 13% of hosts have two listings, 3% more than five (Anchorage letter, weak, [ADN](https://www.adn.com/opinions/letters/2025/10/21/letter-clarifying-what-the-typical-anchorage-airbnb-looks-like/), 2025) | Price-sensitive to subscriptions |
| Professional property managers | 1% of hosts, 23% of listings, 35% of revenue ([AirDNA](https://www.airdna.co/blog/vacation-rental-management-tips-top-property-managers), 2022, snippet) | Need PMS integration; Minut integrates with 30+ PMS (vendor rival claim, [Layla](https://layla.eco/blogs/minut-vs-noiseaware-vs-layla-which-noise-monitor-wins-in-2026), 2026) |
| Hosts in mandate towns | New Orleans commercial STR permits require a noise monitor (vendor summary, [Minut](https://www.minut.com/regulations/new-orleans-commercial-operators)); St. Charles MO Ordinance 22-104 (vendor summary, [Minut](https://www.minut.com/regulations/saint-charles-operators)); West Columbia SC Aug 2026 amendment, adoption unconfirmed ([PDF](https://westcolumbiasc.gov/wp-content/uploads/2026/08/Amendments-to-Rental-Housing-Ordinance.FinalRevised.pdf)); La Quinta CA pilot ([La Quinta](https://www.laquintaca.gov/residents/short-term-vacation-rentals/noise-compliance-pilot-program)); Jersey Village TX ([city](https://www.jerseyvillage.gov/347/Short-Term-Rentals)) | Tiny wedge; verify each code before claiming compliance |

Airbnb's rules require monitors to be disclosed in the listing, measure decibels only, never record or transmit audio, and stay out of bedrooms, bathrooms and sleeping areas ([Airbnb](https://news.airbnb.com/airbnb-and-minut-collaborate-on-noise-prevention-support-for-hosts/), 2022; [Hostfully](https://www.hostfully.com/blog/airbnb-noise-monitor/), 2026). A primary count of hosts by listing bucket, VRMA membership and PM hardware budgets: not found.

### Competitors

| Product | Hardware price | Subscription price | Strengths | Top complaints |
|---|---|---|---|---|
| Minut | Not published | Starter $60/yr (one property), Standard $120/home/yr, Pro $180/home/yr, Call Assist +$10/unit/mo, 1-yr minimum (per rival [Layla](https://layla.eco/blogs/minut-vs-noiseaware-vs-layla-which-noise-monitor-wins-in-2026), Oct 2026); earlier "$150 + $10/mo" ([STR Specialist](https://strspecialist.com/community/thread/noise-monitoring-airbnb-minut-vs-noiseaware-alternatives), Jan 2026) | Airbnb partner; 30+ PMS; Trustpilot 3.4/5 from 552 reviews, 68% five-star ([Trustpilot](https://www.trustpilot.com/review/minut.com?page=2)) | Price creep, billing errors, can't cancel, Wi-Fi change voids plan, useless without a plan (17% one-star) |
| NoiseAware | $199 (STR Specialist); indoor included, outdoor $99 (Layla) | $9/mo (STR Specialist); $180/property/yr for 1-9 properties, $99 fee if a monthly plan is cancelled within 4 months (Layla, rival) | Outdoor sensors, risk scoring | Outdoor false alarms from wind and dogs; outdoor unit drops offline with indoor ([BiggerPockets](https://www.biggerpockets.com/forums/530/topics/1115590-minut-vs-noiseaware), 2023) |
| Alertify | $150 | $6/mo | Noise, smoke/vape, occupancy, air quality, downloadable reports ([STR Specialist](https://strspecialist.com/community/thread/noise-monitoring-airbnb-minut-vs-noiseaware-alternatives), [Hostfully](https://www.hostfully.com/blog/airbnb-noise-monitor/)) | Not found |
| Layla | $149 / $179 / $299 one-time (vendor, [Layla](https://layla.eco/blogs/minut-vs-noiseaware-vs-layla-which-noise-monitor-wins-in-2026), Oct 2026) | "None" per vendor; **disputed**: affiliate says the $159.99 device ships with a 12-month Starter plan and needs a paid plan after ([roundup](https://www.requiemforadream.com/best-noise-monitors-for-airbnb-hosts/), Sep 2026) | dB + radar occupancy; top tier adds smoke, AQ, CO2 | Not found |
| Party Squasher, Roomonitor | Not found | Not found | Device counting with no mic; Europe-focused human escalation ([Hostfully](https://www.hostfully.com/blog/airbnb-noise-monitor/)) | Not found |

**Premise corrections.** The screen labelled Minut as owning NoiseAware (unverified). No evidence of a deal was found, and every 2026 comparison treats them as separate competitors ([Minut](https://www.minut.com/blog/minut-vs-noiseaware)). Treat the ownership claim as likely wrong. The screen also said Airbnb "subsidizes" Minut. Airbnb's 2022 announcement offered one free sensor plus 3 months of service. The current offer, per Minut's page (snippet), is once per Airbnb account, up to 10 listings, and requires a yearly Standard or Pro plan ([Minut offer](https://store.minut.com/airbnb/host-offer)). Who pays for the device is not stated. Point, Ting, consumer dB meters and smart-home hacks were not researched.

### Pain in buyers' words

| Paraphrase | Source | Date |
|---|---|---|
| Host with six properties: the monthly fee "adds up"; zero guest complaints in 18 months once told it is decibel-only | [STR Specialist](https://strspecialist.com/community/thread/noise-monitoring-airbnb-minut-vs-noiseaware-alternatives) | Jan 17, 2026 |
| Went from 4-5 neighbor complaints a year to zero in 14 months after alert escalation | Same thread | Jan 2026 |
| Minut price went from free to GBP 69 to GBP 120 to GBP 840/yr for one property (Minut cites a billing error) | [Trustpilot](https://www.trustpilot.com/review/minut.com?page=2) | Jan 8, 2026 |
| Could not reach Minut to cancel; owns two units but billed for four | Same | Apr 11 and May 27, 2026 |
| Wi-Fi change treated as a new site; subscription voided, refund refused (Minut disputes) | Same | Nov 18, 2025 |
| Wants a monitor bought outright and hates recurring fees; well-reviewed guest partied until 4 AM | [Airbnb Hosts Forum](https://airhostsforum.com/t/non-subscription-noise-monitoring-device/50629) | Nov 2021 |
| Minut only gave demos to hosts with many properties | [BiggerPockets](https://www.biggerpockets.com/forums/530/topics/1115590-minut-vs-noiseaware) | Jun 28, 2023 |

This is the only idea of the five with several dated 2026 first-person complaints aimed at the exact business model the founder would replace. The counterweight is that 68% of Minut reviewers give five stars, so the average host is satisfied. The pain sits with multi-listing hosts and people burned by billing. Reddit and Facebook host groups: not reached.

### v1 product sketch

The parts (estimate): a pre-certified ESP32-S3 module; an I2S MEMS mic with A-weighted dB computed on-chip so raw samples never leave the device; an LD2410 mmWave or a PIR for presence; optional SCD4x CO2, labelled "air quality," not "vape"; USB-C power with a small cell for an outage alert. The privacy proof is open firmware plus a hardware mic-disconnect or a published firmware audit. Ship listing-disclosure text and a placement guide that follow Airbnb's rules.

| Part | Price (source, year) |
|---|---|
| ESP32-S3-WROOM-1-N4R8 | ~$3.74 reference, tier unspecified ([LCSC](https://fat.lcsc.com/product-detail/image/ESP32-S3-WROOM-1-N4R8_C2913200.html), 2026-10-29) |
| ESP32-S3-MINI-1-N4R2 | $5.177 at 1+ ([LCSC](https://lcsc.com/product-detail/image/ESP32-S3-MINI-1-N4R2_C3013941.html)) |
| MEMS mic (ICS-43434/SPH0645), LD2410, SCD4x, enclosure, PCBA | Not found |
| Full BOM at 100 / 1,000 | Not found |

The hard product problem is alerts without a vendor cloud. Guest-facing Wi-Fi is the main failure point, as the Minut Wi-Fi complaint shows. There are three options (estimate). (a) The device pushes through a host-owned relay (ntfy, Pushover or a Telegram bot) with no vendor server. (b) The puck talks LoRa to a hub plugged into the host's own router, which removes the guest-Wi-Fi dependency and reuses the shared platform. (c) An optional paid SMS relay at cost (Twilio price not found).

**B2B:** $79-129 per unit one-time + optional ~$2/mo SMS relay for small PMs (screen hypothesis, unvalidated).

**B2C:** $99-149 one-time, no plan ever (screen hypothesis, unvalidated). Layla's $149 Standard sits at the same price.

### Go-to-market

No sourced event data was gathered (VRMA, Direct Booking Summit and SCALE dates: not found). The competition for single-listing hosts is a free device bundled with a subscription, so the pitch must be "no plan, ever." For the first 10 customers (estimate): (1) a pre-order or waitlist from the founder's YouTube audience, with the firmware repo public; (2) 3-5 small PMs (5-30 units) in ordinance towns for field trials; (3) hosts complaining about fees in STR Specialist and BiggerPockets threads; (4) Facebook host groups (not reached). Test units in the founder's own or friends' listings first. How much the host audience overlaps with the founder's YouTube audience is unverified.

### Kill criteria

| # | Test | Stop if |
|---|---|---|
| 1 | Public landing page with an honest comparison table, after ~3 videos | Fewer than 100 paid deposits at $99+ within 90 days |
| 2 | 30-day field test with 10 PMs/hosts | Fewer than 3 pay, or more than 1 false alert per unit per week |
| 3 | Competitive and technical check | Layla or Minut verifiably offers a genuinely fee-free plan for less; Airbnb/Minut extends free plans to US hosts (re-check quarterly); or alerts cannot arrive in under ~60 s without a vendor cloud |

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| P | 4 | 4 | Loud, dated 2026 billing and lock-in complaints, offset by Minut's 68% five-star share |
| W | 4 | 3 | Hosts already pay $60-180/yr or get a free device; one-time buyers exist (Layla) but volume is unknown |
| O | 2 | 2 | Layla sells one-time (disputed), Alertify at $6/mo, Airbnb's free-device offer |
| B | 5 | 5 | ESP32 + mic + radar on a pre-certified module |
| F | 5 | 5 | Electronics, YouTube story, privacy and design taste all line up |
| **Total** | **20** | **19** | |

## School aerosol sensor

"Quiet-Room": PM/VOC aerosol sensor with no microphone and no cloud, local alerts and a flat price.

### Buyers

| Segment | Count (source, year) | Who decides / how they buy |
|---|---|---|
| Public school districts | **13,303 regular districts** ([NCES CCD](https://nces.ed.gov/ccd/tables/202324_summary_2.asp), 2023-24); 13,318 districts / 91,390 public schools ([EdWeek](https://www.edweek.org/ew/issues/education-statistics/index.html), year not given) | School board vote; safety and prevention directors involved (Lancaster County SC, Minneapolis, per [The 74](https://www.the74million.org/article/vaping-is-everywhere-now-in-schools-can-bathroom-surveillance-tech-solve-the-problem-or-just-escalate-suspensions/), Nov 2025); cooperative contracts (TIPS) |
| Private schools | 30,553 schools, 5,096,365 students (2023-24, secondary, unverified, [Causo](https://hub.causo.ai/guides/private-school-lists-2026)); primary NCES 2026-015 exists ([IES](https://ies.ed.gov/nces/2026/05/characteristics-private-schools-united-states-results-2023-24-private-school-universe-survey)) | Not found |
| Colleges | 3,931 Title IV degree-granting (2020-21, [NCES](https://nces.ed.gov/programs/digest/d22/tables/dt22_105.50.asp)); 5,819 Title IV institutions (2023-24, [IES](https://ies.ed.gov/learn/press-release/total-number-higher-education-institutions-decreases-2-percent)) | Residence-hall buying data: not found |

Deal sizes are small and paid for with one-time money:

| District | Purchase | Source |
|---|---|---|
| Camas WA | 30 HALO at $859 each, $87,282 JUUL settlement money (~2023-24) | [Camas Post-Record](https://camaspostrecord.com/?p=148034) |
| Sumner County TN | 178 sensors, about $102,000 (2024) | [WSMV](https://www.wsmv.com/2024/01/25/vape-detectors-be-installed-sumner-county-schools) |
| Glynn County GA | 128 sensors with sound detection, $174,513.77 incl. licensing | [First Coast News](https://firstcoastnews.com/article/news/education/glynn-county-school-board-approves-vape-detectors-in-district-schools-brunswick-high-glynn-academy/77-c71eee93-bfe9-42d4-a6b0-28f7d8b77371) |
| Lancaster County SC | ~70 Triton sensors, over $150,000 (Nov 2025) | [The 74](https://www.the74million.org/article/vaping-is-everywhere-now-in-schools-can-bathroom-surveillance-tech-solve-the-problem-or-just-escalate-suspensions/) |
| Minneapolis | 29 HALO at ~$1,000, $100,000 pilot (2025) | Same |
| Montgomery County MD | $2M of JUUL money, HALO (Sept 2025) | [FOX 5 DC](https://www.fox5dc.com/news/high-school-vape-sensors-trigger-thousands-false-alarms-mcps-schools) |
| Osceola County FL | 19 schools, over $191,000 of opioid settlement money (Oct 8, 2026) | [MyNews13](https://mynews13.com/fl/orlando/news/2026/10/08/hundreds-of-student-vaping-cases-in-osceola-county-prompt-school-district-to-approve-vape-detectors-in-schools) |
| Lincoln NE | About $1M of JUUL money (2024) | [NPR](https://www.npr.org/2024/09/12/nx-s1-5090006/vape-detectors-schools-ecigarettes-juul) |

The screen's median of $925 per detector and $14,204 per contract across 284 districts came from a vendor analysis ([CivicIQ](https://civiciq.com/blog/school-vape-detector-contracts)), which returned 403 this round and was not re-verified. The JUUL settlement totals about $1.7B (2022, [GV Wire](https://gvwire.com/2024/09/13/fresno-schools-continue-their-efforts-to-wipe-out-vaping/)); remaining unspent balances: not found. Opioid settlement money is a new source. Federal COPS SVPP FY2026 lists vape detection as unallowable (vendor claim, [Triton](https://www.tritonsensors.com/blog/3d-sense/how-much-do-vape-detectors-cost), not verified at DOJ). TIPS contract 230305 is held by ELB US and Citon ([TIPS](https://www.tips-usa.com/assets/Vendorspdf/230305_CONTRACT_Vaping_ELB_US_Inc.pdf)). Sourcewell and BuyBoard contracts: not found. At a $400 price, a 30-180 unit district is $12k-72k, so 10 districts make a low six-figure business (estimate). The settlement window may close by 2027-28 (estimate).

### Competitors

| Product | Hardware price | Subscription price | Strengths | Top complaints |
|---|---|---|---|---|
| Motorola HALO | $859 (Camas); ~$1,000 (Minneapolis); ~$1,100 (Goshen, [Goshen News](https://www.goshennews.com/news/goshen-approves-vape-detectors/article_ed6d240a-dd0c-11ef-8dd2-1f7cf413b84e.html)) | $2,400 two-year subscription at Goshen (district level); per-unit licence not found | Market leader; IPVM finds it generally effective | Thousands of alerts a day, unnamed sensor locations, triggers from flushing and perfume ([FOX 5 DC](https://www.fox5dc.com/news/high-school-vape-sensors-trigger-thousands-false-alarms-mcps-schools), 2025); 3C mic could be turned into an audio bug ([404 Media](https://www.404media.co/it-looks-like-a-school-vape-detector-a-teen-hacker-showed-it-could-become-an-audio-bug/), Aug 8, 2025); vapor blown into a sleeve evades it, alerts can lag over 20 s (IPVM via The 74) |
| Triton ULTRA | **$1,495 MSRP incl. 10-yr warranty, support, training** (vendor, 2026, [Triton](https://www.tritonsensors.com/blog/3d-sense/how-much-do-vape-detectors-cost)) | **None required**; on-prem software included; optional cloud, price not listed | PoE daisy-chain of 5; vendor report: 8,400 events, 98.9% accuracy, 46 false positives (vendor, Sept 2026, [Triton](https://www.tritonsensors.com/vape-detection-accuracy)) | Deodorant is the largest false-positive source (20 of 46) |
| Zeptive | ~$1,100 per detector, wireless ([Yahoo/Lancaster](https://news.yahoo.com/lancaster-schools-wants-e-cigarette-220909469.html)) | Not found | Wireless | Not found |
| Verkada SV25 | ~$1,548-1,783 at resellers ([LTT Partners](https://www.lttpartners.com/products/sv25-air-quality-sensor)) | Licence $249; 5-yr $999 ([CDW](https://www.cdw.com/product/verkada-sensor-license-5-years-1-license/6250107)) | Verkada ecosystem | Has a mic; cloud-tied |
| Soter FlySense | Over $12,000 | $1,500/yr per school (WKBW via screen, not re-verified) | | Cost |
| Vape Guardian (UK) | Not found | Not found | No camera or mic; claims 95%+ fewer incidents in five weeks (vendor, [IPS News](https://ipsnews.net/business/2025/12/04/vape-guardian-solves-false-alert-crisis-in-vape-detection/), Dec 2025) | Not found |

**Premise correction:** the screen priced Triton at "$750-999 then $110-150/yr." That appears to be older Triton 3D Sense pricing; a Michigan snippet shows ~$750 plus a subscription, and Palo Alto paid $995 plus $495 software (both undated). The current ULTRA is local-only with no required licence, so "no licence" is no longer a moat. The open gap is a 3-5x cheaper, auditable, mic-free sensor with published test data. There is a removal precedent: Kyrene middle school in Arizona pulled sensors that alerted in empty bathrooms and got a full refund ([KTAR](https://ktar.com/arizona-news/chandler-middle-school-removes-ineffective-bathroom-vape-sensors), 2019).

### Pain in buyers' words

| Paraphrase | Source | Date |
|---|---|---|
| Administrators got hundreds, sometimes thousands, of alerts a day (one counted 3,500+ emails); sensors lacked location names; staff stopped checking | [FOX 5 DC](https://www.fox5dc.com/news/high-school-vape-sensors-trigger-thousands-false-alarms-mcps-schools) | Sept 17, 2025 |
| Advocate called the $2M a waste; unclear the sensors reduce vaping | Same | Sept 2025 |
| About 412 alerts per school day in Minneapolis; 81% of incidents led to suspension | [The 74](https://www.the74million.org/article/vaping-is-everywhere-now-in-schools-can-bathroom-surveillance-tech-solve-the-problem-or-just-escalate-suspensions/) | Nov 2025 |
| Mesa administrators get ~15 alerts a day, most without a catch | [KGUN 9](https://kgun9.com/news/state/mesa-public-schools-puts-vapes-detectors-in-middle-high-school-bathrooms) | Not seen |
| Student's deodorant set off a detector and she was searched | [NPR](https://www.npr.org/2024/09/12/nx-s1-5090006/vape-detectors-schools-ecigarettes-juul) | 2024 |
| A teen showed a HALO 3C could become an audio bug | [404 Media](https://www.404media.co/it-looks-like-a-school-vape-detector-a-teen-hacker-showed-it-could-become-an-audio-bug/) | Aug 8, 2025 |

The dominant pain is alert volume and ambiguity, then privacy, then cost. Evidence that sensors reduce vaping is thin. Central Unified CA found active supervision more effective (NPR snippet, 2024). Licence-renewal complaints: not found.

### v1 product sketch

Vendors fuse PM, VOC and RH/T with rate-of-change and a per-room baseline. Particle-only detectors trip on aerosol cleaners and fogged mirrors (vendor, [Rhombus](https://rhombus.com/blog/vape-detectors-for-schools/)). Aerosol sprays are the hard negatives and steam is easy (Triton, vendor). No independent accuracy study was found. The only peer-reviewed work covers instrument correction factors ([PMC10947168](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10947168/)).

| Part | Price (source, year) |
|---|---|
| Sensirion SEN66 (PM, RH/T, VOC, NOx, CO2) | $47.95-49.54 at qty 25-1, 8-17 week lead ([Future](https://futureelectronics.com/p/7192262), year not shown); $47.18 at 50, MOQ 420 (vendor, [Future](https://www.futureelectronics.com/de/c/semiconductors/analog--sensors--air-quality/products)); EUR 51.65 ([Tinytronics](https://www.tinytronics.nl/nl/sensoren/lucht/vochtigheid/sensirion-sen66-sin-t-omgevingssensor-fijnstof-luchtvochtigheid-temperatuur-co2-voc-nox)) |
| Sensirion SEN55 (no CO2) | $36.95, $33.26 at 100+ (vendor, [SparkFun](https://www.sparkfun.com/sensirion-particle-voc-humidity-and-temperature-sensor-sen55.html)) |
| SPS30 + SGP41 (split option) | $16.60 at 125 + $8.10 at 75 (vendor, Future Electronics category page, verify) |
| ESP32-S3-WROOM-1 | ~$3.74 ([LCSC](https://fat.lcsc.com/product-detail/image/ESP32-S3-WROOM-1-N4R8_C2913200.html)) |
| PoE, PCB, enclosure, tamper, misc | Not found |

BOM is about **$90-100 at 100 units and $70-80 at 1,000** (estimate, built on the SEN66 price). The design (estimate): PoE so there are no batteries to swap; tamper and cover detection; every unit named by room (the FOX 5 complaint); a report-first digest mode; local alerts via hub, SMTP, SMS gateway and webhooks; no mic, open firmware and data format. Do not market it as a life-safety device (UL 217 not researched). FCC Part 15B still applies to the finished product. A test to run: whether the PM1:PM2.5 ratio discriminates vape from spray (no published source).

**B2B:** $300-450 per sensor one-time, hub $250, optional support $30/unit/yr (estimate).

**B2C:** $80-120 for parents, apartments and hotels (estimate; demand not researched).

### Go-to-market

Public signals identify candidate first customers: Montgomery County MD (false alarms, $2M HALO), Minneapolis and Lancaster County SC (The 74), Wilson County TN (pilot in up to 3 schools, seeking grants, [WSMV](https://www.wsmv.com/2026/08/19/wilson-county-schools-pilot-vape-detection-sensors/), Aug 19, 2026), Osceola County FL (Oct 2026), and earlier buyers who may want a cheaper add-on (Goshen, Glynn, Sumner, Camas, Lincoln). The path is facilities and safety directors plus board agendas, offering a free loaner pilot in one restroom with logged data. Selling through a TIPS holder or security integrator avoids running procurement paperwork solo; the TIPS replacement RFP deadline is unknown. Conference dates (ASBO, NSBA, CoSN), state procurement thresholds and reseller margins: not found.

### Kill criteria

| # | Test | Stop if |
|---|---|---|
| 1 | Month 3 bench dataset, 1,000+ labelled events | Below 97% accuracy, or above 1% false positives on deodorant/body spray at 3 ft |
| 2 | Month 9 paid pilots | Fewer than 3 districts with 10+ units each: stop or shrink to B2C |
| 3 | Month 12 sales | Fewer than 100 units at 60%+ gross margin: close |

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| P | 4 | 4 | Verified false-alarm, privacy and cost complaints (FOX 5, The 74, 404 Media) |
| W | 4 | 3 | Districts spend $50k-200k, but from one-time settlement funds, and Triton ULTRA includes local software at $1,495 |
| O | 3 | 3 | Crowded (HALO, Zeptive, Triton, Verkada, Soter, Vape Guardian), but a sub-$500 mic-free local product is open |
| B | 4 | 4 | Off-the-shelf sensor; proving accuracy and procurement paperwork are the hard parts |
| F | 4 | 4 | Privacy and local-first match; school procurement does not suit a solo creator |
| **Total** | **19** | **18** | |

## Clamp-on CNC machine monitor

A split-core current clamp on a machine's feed that infers run/idle/off and serves a shop-local dashboard. One-time price.

### Buyers

| Segment | Count (source, year) | Who decides / how they buy |
|---|---|---|
| Machine shops, NAICS 332710 | **17,156 establishments, 223,313 employees** (CBP 2023 via aggregator, [Vanta Insights](https://vantainsights.com/industry/332710-machine-shops), unverified against Census); 20,138 "business entities," no year ([naics.com](https://www.naics.com/naics-code-description/?code=332710)); ~98.5k employees on a BLS definition (2023, [FRED](https://fred.stlouisfed.org/series/IPUEN332710W010000000)) | Owner (small) or ops/maintenance manager (mid), not verified by any source |
| All manufacturing, NAICS 31-33 | 397,330 establishments, 12,784,104 employees (2024, [BLS QCEW](https://data.bls.gov/cew/data/api/2024/a/industry/31_33.csv)); 74% of manufacturers have under 20 employees ([NAM](https://nam.org/?p=34181), year not stated) | Dealers: Scytec partnered with Absolute Machine Tools ([F&M](https://fandmmag.com/2022/02/scytec-consulting-partners-with-absolute-machine-tools), 2022) |
| Shop size | Small shop monitors ~5 machines, mid-size ~25 (vendor, [Guidewheel](https://www.guidewheel.com/blog/machine-monitoring-software-cost), Jun 2026). Size-class counts, hobby CNC and makerspace counts: not found | |

All budget norms are vendor-written: hardware $300-2,000 per machine, software $50-300 per machine per month, integration $1,000-10,000 ([JITbase](https://www.jitbase.com/blog/best-machine-monitoring-software-top-10), 2026); hardware $500-2,000 plus cloud $240-1,200 per machine per year ([Guidewheel](https://www.guidewheel.com/blog/machine-monitoring-software-cost), 2026). Small-to-mid shops run 30-60% OEE (vendor, JITbase). The Gardner Precision Machining index had one of its strongest monthly advances in 14 years at the start of 2026 ([Production Machining](https://www.productionmachining.com/articles/2026-off-to-impressive-start-for-precision-machining-index)). At ~$99 per machine, a 10-machine shop pays ~$1K, against $2.4K-12K a year in software alone at Guidewheel's own range (estimate).

### Competitors

| Product | Hardware price | Subscription price | Strengths | Top complaints |
|---|---|---|---|---|
| Guidewheel | Not found; claims retrofit sensors cost $200-2,000/asset (vendor) | **Public $15,000/yr incl. 10 machines removed mid-Sept 2026**, now "contact us" ([PricingSaaS](https://pricingsaas.com/companies/guidewheel/diffs/2026W39)); stale 2024 $59/$99 per sensor/mo ([ZoftwareHub](https://zoftwarehub.com/products/guidewheel/pricing)) | Clip-on current sensor, ~2.5 min install (vendor) | Not found |
| MachineMetrics | ~$117.50-894.50 ([Fitgap](https://us.fitgap.com/products/machinemetrics)) | Quote only ([G2](https://www.g2.com/products/machinemetrics/pricing)) | Deep controller data via MTConnect/OPC-UA | Slight real-time delay, no free trial ([Capterra](https://www.capterra.com/p/159410/MachineMetrics/)); higher per-machine cost for small sites (rival JITbase) |
| FourJaw (UK) | MachineLink GBP 200 one-time; 4G router GBP 14/mo | Standard GBP 90/mo monthly or 72 annual; Pro GBP 180 / 144 per machine; 5-machine minimum ([FourJaw](https://fourjaw.com/pricing), Oct 2026) | Self-install; up to 40% volume discount | Not found |
| Evocon | IIoT device $24/mo (1-yr) or $19 (3-yr) | $189-379 per machine/mo ([Fabrico](https://www.fabrico.io/sr/blog/evocon-pricing-guide-2026/), 2026); Capterra shows EUR 159-269 (unreconciled) | Tiered OEE | Not found |
| Vorne XL | **$4,490 / 4,690 / 4,990 one-time** ([Vorne](https://vorne.com/international/prices)) | None | Only proven one-time model; unlimited users, 3-yr warranty | Price per unit |
| JITbase | n/a | Free up to 5 machines; extras from EUR 18/mo ([JITbase](https://www.jitbase.com/plans)) | Free tier, no commitment | Not found |
| Scytec DataXchange | Activation fee | Monthly per machine; "$45/mo" unclear ([Slashdot](https://slashdot.org/software/comparison/DataXchange-vs-Macola/)) | Legacy machines via MTConnect/PLC | UI less modern (rival) |
| Haas HaasConnect | Included on Haas machines ([Haas](https://www.haascnc.com/productivity/control/haas-connect.html)) | Not stated | Free-looking bundle | Older Haas controls need serial/DPRNT or a Moxa box ([MachineMetrics](https://docs.machinemetrics.com/docs/machine-connectivity/haas-connectivity-guide)) |
| DIY: Shelly Pro 3EM | ~EUR 132.66 with 3 CTs ([Atlantek](https://shop.atlantek.net/?p=77151)); Shelly 120A CT $18.95 ([Ameridroid](https://ameridroid.com/collections/automation-devices-electrical-current-and-power-sensors)) | None | Cheap | Measures energy, not machine state or job context |

Datanomix, Amper (now inside ECI), Memex, Shoplogix, Leanworx and Mazak SmartBox prices: not found. **Premise corrections:** the screen quoted FourJaw at "GBP 36-90"; the current page shows GBP 72-180 per machine per month. The screen's Guidewheel $15K/yr figure has been removed from Guidewheel's pricing page, though its own Aug 2026 comparison still cites it ([Guidewheel](https://www.guidewheel.com/compare/vorne-xl-pricing-real-cost)). Nothing found sells a cheap, local-first, one-time clamp-on.

### Pain in buyers' words

| Paraphrase | Source | Date |
|---|---|---|
| Ops manager at a 60-machine shop expected six figures and ~3 months to implement; ownership declined | [Amper blog](https://blog.amper.xyz/how-i-went-from-evaluating-machine-monitoring-systems-to-selling-one) (vendor) | Jun 2020 |
| Leadership said it was impossible to get data out of old machines without costly integration | Same | Jun 2020 |
| Manual setup analysis arrived after "the job was over" | Same | Jun 2020 |
| Wanted to explain planned vs actual output; replies said early systems needed hardware/PLC mods | [eMastercam](https://www.emastercam.com/forums/topic/89318-anyone-using-machine-monitoring-software/) | Oct 3-5, 2016 |
| Per-machine yearly service subscription felt like more money for less service (woodworking CNC) | [WoodWeb](https://woodweb.com/cgi-bin/forums/cnc.pl?read=870991) | Not captured |
| $25K controller unlock fees; warnings against putting old machines online (snippet only) | [Practical Machinist](https://www.practicalmachinist.com/forum/threads/is-connecting-machines-to-the-network-worth-it.449903/) (screen) | Unverified |

This is the weakest voice evidence of the five: one vendor blog from 2020, a 2016 forum thread and one blocked snippet. IT/security worries, controller option fees and whether owners act on the data: not found.

### v1 product sketch

The sensing is plausible but unproven. A patent application says raw current does not reliably show whether a CNC is active and a simple threshold is insufficient ([EP4030254](https://data.epo.org/publication-server/rest/v1.2/patents/EP4030254NWA1/document.html)). Unsupervised classification from cheap non-intrusive sensors is described in [US 2022/0221514](https://patents.justia.com/patent/20220221514). NILM on production machines reached 87-88% accuracy, but for energy, not state, and VFD spindles are harder ([arXiv](https://arxiv.org/pdf/1912.01500)). No published run/idle/off accuracy was found. The design (estimate): clamp the incoming feeder, learn per-machine thresholds with hysteresis and a "teach" button (off / idle / cutting), and run an ESP32 node over Wi-Fi to a local hub serving a LAN dashboard, with an optional stack-light output. Coolant pumps share the feed current, so "spindle on" is inferred, not measured. No UL listing for v1: sell it as an accessory, and any install inside a panel needs a licensed electrician.

| Part | Price (source, year) |
|---|---|
| SCT-013-030 split-core CT | $2.60-3.20 (marketplace, low confidence, [Accio](https://www.accio.ai/find-product/coreless-current-sensor)) |
| Shelly 120A CT | $18.95 retail ([Ameridroid](https://ameridroid.com/collections/automation-devices-electrical-current-and-power-sensors), 2026) |
| ESP32-S3-WROOM-1 | ~$3.74 ([LCSC](https://fat.lcsc.com/product-detail/image/ESP32-S3-WROOM-1-N4R8_C2913200.html)) |
| Full BOM at 100 / 1,000 | Not estimated (no sourced prices) |

**B2B:** $99 per machine one-time + optional $5/mo (screen estimate, unsourced).

**B2C:** $59 for hobby CNC and laser owners (screen estimate, unsourced).

### Go-to-market

The only sourced channel evidence is the Scytec dealer partnership. Buyer norms favour trials: JITbase's free tier covers 5 machines, and a rival recommends a free 60-day pilot over a demo ([Teeptrak](https://teeptrak.com/en/?p=118472)). IMTS 2026 (Sept) has passed; FABTECH, Westec and EASTEC dates are not verified. For the first 10 shops (estimate): a YouTube build video plus 3 loaner units per shop, and local NTMA chapter or MEP referrals. Machining-creator audiences and sponsor rates: not found. The B2C hobby version is the one most likely to overlap the founder's own audience.

### Kill criteria

| # | Test | Stop if |
|---|---|---|
| 1 | 15 pilot shops with free loaner units | Fewer than 5 still running at day 60 and opening the dashboard weekly |
| 2 | Accuracy against an operator log on 10 mixed machines after one teach-in | Below 90% run/idle/off agreement, or more than 20% of machines need manual tuning |
| 3 | 100 qualified leads or video audience, 6 months | Fewer than 10 paid orders at $99-149/machine, or acquisition cost (time + free units) above 3x first-order revenue |

### Score

| Criterion | Old | New | Reason |
|---|---|---|---|
| P | 4 | 4 | Cost, complexity and old-machine fears documented, but mainly in a 2020 vendor blog; forums inaccessible |
| W | 4 | 3 | No independent evidence of small-shop spend; Guidewheel hid its price and Haas bundles monitoring |
| O | 3 | 4 | No cheap, local-first, one-time clamp-on found; Vorne is $4-5K; the rest are cloud subscriptions |
| B | 5 | 5 | ESP32 + split-core CT + local web page |
| F | 4 | 4 | Skills and local-first taste fit; no machine-shop network or B2B sales experience |
| **Total** | **20** | **20** | Confidence low-moderate: buyer counts and independent voices are missing |

## Comparison

| Idea | Old score | New score | P/W/O/B/F | Strongest evidence | Biggest risk | Rough BOM | B2B price | B2C price |
|---|---|---|---|---|---|---|---|---|
| Crew Beacon Tag | 19 | 16 | 4/2/2/5/3 | Repeated "didn't mow" disputes; NYC DOI 2025 falsified guard records | Free phone photos already settle most disputes | Option B sourced parts ~$6-7 (estimate); Option A under $5 at 1,000 (estimate) | $12-20/tag one-time; optional $29/mo for 25 sites (screen) | $25 (screen) |
| Unit Door Sentinel | 20 | 17 | 3.5/3/3/4/3.5 | 85% of operators concerned about theft (MSM 2025); SpiderDoor $140 + $2/mo price anchor | Purchases go through bundled incumbents; demand evidence is old trade press | Node sourced parts ~$7-8 (estimate); hub $15 (Pi Zero 2 W) to $234 (RAK7268C) | $15-25/door + $1/door/mo (screen) | $39-59 (screen, weak) |
| STR noise puck | 20 | 19 | 4/3/2/5/5 | Dated 2026 Trustpilot and host-forum complaints about subscriptions and billing | Layla already sells one-time at $149-299 (disputed) | Not found (ESP32-S3 ~$3.74 only) | $79-129/unit + optional ~$2/mo SMS (screen) | $99-149 one-time (screen) |
| School aerosol sensor | 19 | 18 | 4/3/3/4/4 | Thousands of false alarms a day (FOX 5 2025); HALO mic exploit (404 Media 2025); $50k-200k district deals | Triton ULTRA is already local-only at $1,495; slow procurement; one-time settlement money | ~$90-100 at 100, ~$70-80 at 1,000 (estimate) | $300-450/unit + $250 hub + optional $30/unit/yr (estimate) | $80-120 (estimate) |
| Clamp-on CNC monitor | 20 | 20 | 4/3/4/5/4 | Clear price gap: cloud subscriptions at $240-1,200/machine/yr (vendor) and Vorne at $4,490+ one-time | No independent buyer voice; current-based state detection is unproven | Not estimated (CT $2.60-18.95 + ESP32 ~$3.74 sourced) | $99/machine one-time + optional $5/mo (screen) | $59 hobby (screen) |

Every score fell or held. The deeper research mostly removed willingness-to-pay assumptions: four of the five W scores dropped by one point or more. The screen's scores rewarded buildability and fit; the deeper evidence mostly says incumbents or free workarounds already absorb the budget.

## Recommendation: what to prototype first

**Build the STR noise and occupancy puck first.** It is not the top scorer (the CNC monitor is, by one point), but it is the best bet on the four things that matter for a solo founder.

**Evidence.** The STR puck is the only idea where several real customers in 2026, with dates, complain about the exact thing the founder would remove: recurring fees, billing errors, voided plans and cancellation trouble. The CNC monitor's open space is real, but the pain evidence is a 2020 vendor blog, a 2016 forum thread and one blocked snippet. The STR evidence is about a business-model wedge. The CNC evidence is about a price gap nobody has yet confirmed buyers want filled.

**Money.** Hosts already pay $60-180 per home per year to Minut, so the spending is proven. A $99-149 one-time device beats a subscription within one to two years for the buyer. The CNC monitor has a bigger ticket per customer, but zero independent evidence of small-shop spending.

**Founder fit.** "Decibels only, raw audio never leaves the chip, no account, no plan" is a privacy story and a build video in one. The puck sits in a living room where guests see it, which is where Teenage Engineering or Nothing-style design pays off. A CT clamp lives in an electrical cabinet, and nobody buys one for its looks.

**Speed.** The STR kill test is 100 paid deposits at $99+ within 90 days of a landing page and about three videos. It runs on the founder's own audience and needs no sales calls. The CNC test needs 15 shops willing to accept loaner units, a network the founder does not have.

What would change this call: if Layla's $149 device turns out to be genuinely subscription-free and good, open space drops to near zero and the CNC monitor moves up. So do these in order:

| Week | Action |
|---|---|
| 1 | Buy one Layla and one Minut; log what works without a plan, the alert latency and the onboarding friction. This settles kill criterion 3 for about $300 |
| 1-3 | Bench prototype: ESP32-S3 + I2S mic computing dB on-chip + LD2410; alerts via ntfy/Pushover with no vendor server; measure time-to-alert on a guest-style Wi-Fi network |
| 3-6 | Enclosure on the Bambu, then a PCBWay CNC aluminium version for the hero shots; publish the firmware |
| 4-16 | Landing page with an honest comparison table (Minut, NoiseAware, Alertify, Layla), deposits at $99+, three videos; 30-day field test in own or friends' listings |

Run the CNC monitor second, as a cheap parallel bench test. It shares the ESP32 node, local hub and dashboard code. Teach-in on two or three machines (a makerspace or a friend's shop) answers its riskiest question, whether current alone separates run/idle/off at 90%+, before any market work. Park the Crew Beacon Tag and Unit Door Sentinel unless the forum reading below shows pain much stronger than the notes found. Leave the school sensor for later: it is a strong product idea, but procurement and accuracy proof make it a year-long B2B campaign, not a first test.

## Shared platform

The screen proposed one platform (a LoRa node, a local hub and an e-paper display) for many ideas. Of these five, only the Unit Door Sentinel is a pure LoRa-node product. The block that truly repeats is the **local hub with a no-cloud alert path**, which four of the five ideas need. Build that hub once and the radio choice per product becomes a detail.

| Block | Part and sourced price | Crew Tag | Door Sentinel | STR puck | School sensor | CNC monitor |
|---|---|---|---|---|---|---|
| BLE/NFC node | MDBT42Q $4.95 qty 1 (via [Flux](https://www.flux.ai/jecstronic/mdbt42q-512kv2.md)); MDBT50Q-1MV2 $9.45 ([TME](https://www.tme.com/us/en-us/details/mdbt50q-1mv2/iot-wifi-bluetooth-modules/raytac/)); ATECC608B $1.28 at 100+ ([LCSC](https://www.lcsc.com/product-image/C1020341.html)) | Yes | | | | |
| LoRa node | Wio-SX1262 ~$3.89-4.29 ([Pakronics](https://www.pakronics.com.au/products/wio-sx1262-wireless-module-bulk-sx1262-embedded-supports-lora-lorawan-on-eu868-us915-ss114993390)); Wio-E5, RAK3172, E22 prices not found | | Yes | Optional link to hub (avoids guest Wi-Fi) | Optional | |
| Wi-Fi node | ESP32-S3-WROOM-1 ~$3.74 ([LCSC](https://fat.lcsc.com/product-detail/image/ESP32-S3-WROOM-1-N4R8_C2913200.html)); S3-MINI-1 $5.177 ([LCSC](https://lcsc.com/product-detail/image/ESP32-S3-MINI-1-N4R2_C3013941.html)); C3/C6 prices not found | | | Yes | Yes | Yes |
| Local hub + alert relay | Pi Zero 2 W ~$15 ([Magazin Mehatronika](https://magazinmehatronika.com/en/the-2026-raspberry-pi-pricing-and-buying-guide/)); Pi 5 2GB $77.50 ([Phoronix](https://www.phoronix.com/news/Raspberry-Pi-5-2GB-Price-77.50), 2026-10-01); RAK7268C $234 excl. 25% tariff ([Rokland](https://store.rokland.com/collections/rakwireless-products/products/rak-wireless-wisgate-edge-lite-2-indoor-gateway-for-lorawan-rak7268c-us915)); SX1302 HAT not found | Phone acts as hub | Yes | Yes (or host-owned relay) | Yes | Yes |
| E-paper status display | Waveshare 2.13" $13.29-14.99; 2.9" $16.95-18.99; 4.2" $33.63-34.99 retail ([Waveshare](https://www.waveshare.com/product/displays/e-paper.htm?p=2)) | | Hub display | Optional dB face | Hub display | Per-machine status |
| Motion/tamper | LIS2DH12 $0.22-0.91 ([LCSC](https://datasheet.lcsc.com/lcsc/STMicroelectronics-LIS2DH12TR_C110926.pdf), [DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/LIS2DH12TR/4899838)) | | Yes (pry) | | Yes (tamper) | |
| Long-life power | ER14505 EUR 2.75-3.50 ([Ormix](https://ormix.lv/en/catalog/GG0111?page=5)); CR2032 $0.0365-0.2510 at 100 ([LCSC](https://www.lcsc.com/product-image/C70373.html)) | CR2032 (Option B) | ER14505 class | Backup cell | PoE instead | Mains |
| Idea-specific sensor | SEN66 ~$47-50; SEN55 $33.26 at 100+ ([SparkFun](https://www.sparkfun.com/sensirion-particle-voc-humidity-and-temperature-sensor-sen55.html)); SCT-013 $2.60-3.20 (low confidence); mic, LD2410, reed: not found | NTAG 424 DNA | Reed switch | Mic + mmWave | SEN66 | CT clamp |

Import surcharges matter: the 25% tariff note on RAK gateways also affects Waveshare's US landed cost. LCSC prices for the same ST part run far below Western distributors ($0.22 vs $0.55 vs $0.91), so every BOM should state its channel. The reusable software is the bigger asset: a hub that receives node events, names devices by room/door/machine, stores a local log and pushes alerts through a host-owned relay (ntfy, Pushover, SMTP, webhooks). That is the STR puck's hardest problem, and solving it there first de-risks the CNC, school and door products.

## Forums to read personally

Reddit (400 error for search), LawnSite (tollbit paywall redirect), Self-Storage Talk (403) and Practical Machinist (403) were all blocked to automated research, and no browser tools were used. Their evidence is search snippets only. The STR threads (STR Specialist, BiggerPockets, Airbnb Hosts Forum, Trustpilot) were readable and are already in this report, so the founder's reading time is worth more on the blocked forums. Ranked by how much a single read could change the plan:

| Rank | Thread | What it would test |
|---|---|---|
| 1 | Practical Machinist, ["Is connecting machines to the network worth it"](https://www.practicalmachinist.com/forum/threads/is-connecting-machines-to-the-network-worth-it.449903/); also ["Shop floor data collection"](https://www.practicalmachinist.com/forum/threads/shop-floor-data-collection.426976/) | Whether shop owners resist cloud monitoring and subscriptions, and whether they would pay for a local one. Confirms or kills the $25K unlock-fee snippet. If owners here say they want a cheap local clamp, the CNC monitor moves to first place |
| 2 | Self-Storage Talk, ["Individual Unit Alarms"](https://www.selfstoragetalk.com/forum/general-self-storage-forums/technology-software-and-security/208237-individual-unit-alarms) | Per-door prices actually paid, and whether battery and false-alarm complaints are current or 2010-era. Decides whether Door Sentinel's P and W recover |
| 3 | LawnSite, ["How do you verify that employee cut the customer's lawn?"](https://www.lawnsite.com/threads/how-do-you-verify-that-employee-cut-the-customers-lawn.512717/) | Whether owners' pain is customer disputes (photos suffice) or crew verification (a site-bound tag adds value). Only a strong crew-verification signal would revive the Crew Beacon Tag |

For each, note dates, quotes, prices paid and what tools posters already use. One afternoon covers all three.

## Method and limits

Five Sonnet researchers each took one idea, and one follow-up researcher gathered component prices and Census counts. All used web search and fetch only. No browser or computer-use tools were used. Blocked or failed: Reddit (400), LawnSite (paywall), Self-Storage Talk and Practical Machinist (403), CivicIQ (403), DigiKey/Seeed/Espressif pages (403/404), the RAK store (429) and the Census API ("Missing Key"). As a result, Census counts come from a secondary aggregator attributing CBP 2023, most component prices come from search summaries rather than distributor quote tables, and PCB, enclosure and assembly costs were not gathered for any idea. Vendor figures are labelled; "(estimate)" marks researcher reasoning; "not found" means the research looked and came up empty. The cheapest next data steps are a free Census API key for the five NAICS rows and size classes, and real PCBWay/LCSC quotes for the STR puck BOM. Research date: 2026-10-29.
