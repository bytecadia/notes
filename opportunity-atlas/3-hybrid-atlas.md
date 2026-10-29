# One small sensor, two buyers: the hybrids worth building solo

The best true hybrids are cheap, battery-powered, camera-free sensors that a household buys one of and a small business buys ten of, with the same hardware and a free local app. Five rise to the top once evidence on both sides is weighted above raw score: a pet-area temperature and power-loss monitor (pets in homes and RVs, kennels and groomers; 20/25), a workshop air and compressor node (hobby woodworkers, small shops; 21/25, the top score but with thin evidence on both sides), a sump and leak/freeze/vacancy family (homeowners, small landlords; 20 and 19), a clamp-on machine run monitor (hobby CNC and print farms, machine shops; 20), and a shore-power monitor for boats and RVs (owners, marinas and campgrounds; 17, but the strongest two-sided evidence found). The pattern across 20 ideas: the pet monitor, the water family and the shore-power unit have named products and prices on both sides, and everything else is mostly inference. Consumer prices are anchored by $20-30 commodity sensors (Govee-class), so a design-led product only wins where it does something the cheap one cannot, such as alerts that still arrive in a power or Wi-Fi outage, a local siren, or fleet logs. The playbook evidence (Minut, Sonos Pro, Shelly, Ecobee) says to ship one SKU, one price list, a free app, and a per-location paid tier for multi-site dashboards and logs. Almost all pricing here comes from vendors or resellers, and no direct customer quotes were retrievable, so treat every demand score as a hypothesis to test with the forums listed near the end.

## How to read this screen

**Method.** Five research passes (homes, shops, trades and land, mobile and community, and a playbook of companies that sell one device to both sides) used web search and page fetches only. Reddit, Trustpilot, Amazon review pages and most trade forums could not be reached, so consumer "pain in own words" is mostly missing. Where a note said "not found", this report says so. Background prices from earlier reports were used only as context.

**Score key.** Each idea is scored 1-5 on five criteria, total out of 25:
- **B2B demand**: rounded average of that side's Pain, Willingness to pay and Open space scores from the notes.
- **B2C demand**: the same for the consumer side.
- **Shared hardware**: 5 means the identical device serves both buyers; 1 means two products.
- **Buildable solo**: 5 Easy, 4 Easy-moderate, 3 Moderate, 2 Hard. Hard means certification or safety liability likely.
- **Founder fit**: fit with a design-led, privacy-first, local-first, camera-free solo engineer on pre-certified modules.

Where I merged two noted ideas or adjusted a score, the idea text says why. **(vendor)** marks a figure from a vendor or retailer page. **(estimate)** marks my reasoning or a figure the notes flag as unverified. All BOMs, buyer counts for new ideas, and prices for the proposed products are (estimate). Prices of existing products were gathered at different dates and may be stale.

**Limits.** Most B2C evidence is indirect. Several US counts (kennels, hobby CNC owners, marinas, cleaners, bars) were not found. Excluded: health and medical, pure SaaS, heavy certification. The school vape sensor was checked and rejected as a hybrid: strong B2B (about $750-$3,050 per unit (vendor)), no evidence of parent demand, crowded field ([Identisys](https://identisys.com/about-identisys/learning-center/security-blog/security-technology-blog/2024/06/19/enhance-school-safety-and-air-quality-with-halo-multi-sensor-detectors-at-new-lower-prices), [Goshen News](https://www.goshennews.com/news/goshen-approves-vape-detectors/article_ed6d240a-dd0c-11ef-8dd2-1f7cf413b84e.html)). The school-bus child-check alarm was also dropped (liability, automaker reminders erode the consumer side).

## Area-by-area screen

### Area 1: Homes and property

#### Summary
This area has the cleanest hybrid shape: a homeowner buys one or four sensors, a landlord or property manager buys dozens of the same sensor. Water damage is the anchor pain, backed by insurer discounts. The catch is price: YoLink-class sensors set a floor near $10 each (vendor), so the opening is design, local-first operation and a multi-property view rather than a new sensor. Noise monitors are a B2B product with an unproven consumer side.

#### Buyers
| Side | Who | US count | What they pay now |
|---|---|---|---|
| B2C | Homeowners with basements, sump pits, propane or oil heat | Not found for sump, propane or oil households. Insurer data: about 1 in 60 homeowners files a water claim a year, average about $13,954 (secondary source) | YoLink 4-sensor kit about $40-55 on deals, no subscription (vendor); Phyn about $699 plus install, Flo about $499 (2024 roundup); sump alarm SMS $0.99/mo (vendor); SpotProtect about $215 (vendor); Mopeka or Generac propane monitors about $161-210 (retailer) |
| B2B | Small landlords and property managers | About 15.5M investor-owned single-family homes, about 90% owned by owners with 1-10 properties (BatchData, Q1 2026) | Minut sensor about $129-150 plus $5-15/mo per home; NoiseAware about $15/mo for 1-9 properties (vendor); Phyn sells a property-manager dashboard |
| B2B | Short-term rental hosts and HOAs | About a third (32-37%) of STR operators use smart devices (Hostfully analysis); HOA count not found | Noise sensors as above; Airbnb gives discounts on Minut, Roomonitor and NoiseAware |

#### Pain points
- B2C: Water claims are common and costly (about 1 in 60 homeowners a year, about $13,954 average); insurers reward detection (Chubb 8% discount, USAA discount for 2+ detectors, both to verify). [Contractor Mag](https://www.contractormag.com/plumbing/article/55269168/lead-detection-devices-can-reduce-average-claim-costs-by-4k), [USAA](https://mobile.usaa.com/my/connected-home)
- B2B: Property managers and insurers pitch vacancy water monitoring (Minut, Stratis, Streamlabs, HSB), and Swidget sells a movable kit for vacant units. [HSB](https://www.munichre.com/hsb/en/services/applied-technology-solutions/sensor-solutions/commercial/commercial-iot-occupancies/habitational.content.html), [Swidget](https://www.swidget.com/en-ca/blogs/newsroom/leveraging-data-insights-to-improve-property-monitoring-efficiency)
- B2B: Hosts resent forced subscriptions; Minut ended free service for new customers in 2021 and phased it out from 2024. Trustpilot about 3.5/5 from about 517 reviews, with price, app and support complaints (snapshot). [Trustpilot](https://nz.trustpilot.com/review/minut.com)
- B2C: Sump alarms charge for texts and sharing; the market is fragmented and plain. [Sump Alarm listing](https://www.rcworst.com/sump-alarm-sa-120v-1l-16f-wifi-wireless-wifi-high-water-alarm-120v-16ft-float.html), [SpotProtect](https://www.absoluteautomation.com/products/spotprotect-sumpspot-wifi-sump-pump-alarm)
- B2B: Pool pros worry that homeowner sensors undercut service contracts. [Aqua Magazine](https://www.aquamagazine.com/retail/article/15123409/get-smart)
- Not found: any retrievable Reddit, BiggerPockets or Amazon review text, and any evidence of homeowner or parent demand for noise monitors.

#### Existing players
| Company | Side | Price and plan | Gap or complaint |
|---|---|---|---|
| YoLink | Both | About $10/sensor, hub, LoRa, no subscription (vendor) | Price floor; no sourced commercial terms |
| Phyn, Flo | B2C, some B2B | About $699 and $499 plus install (2024 roundup) | Expensive; plumbing install |
| Minut | B2B, some B2C | Sensor about $129-150 plus $5-15/mo/home; Enterprise at 20+ | Forced subscription backlash |
| NoiseAware | B2B | $15/mo for 1-9 properties (vendor); hardware about $199 (review) | Subscription; outdoor add-on $99 |
| SpotProtect, Sump Alarm, Moen | B2C | About $215 plus subscription for multi-user (vendor) | Ugly, SMS fees |
| Mopeka, Generac | B2C | About $161-210 cellular (retailer) | Carrier-dependent |
| Tekelek, ICON, Veeder-Root | B2B | ICON cellular about $1,780 (vendor) | Industrial price and lock-in |
| Pentair, WaterGuru | Both | WaterGuru launched a commercial division | High-end only |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score B2B/B2C/Shared/Build/Fit |
|---|---|---|---|---|---|---|
| 1 | **Sump and Crawlspace Puck**: a plain low-voltage sensor with a loud local alarm that also reports over LoRa to a hub you own. | Landlords and HOAs with sump pits in rentals and common areas: about $69 per unit plus $2/mo per unit for a multi-property map (estimate) | Basement owners in flood-prone homes: $79 once, no plan, local siren plus free app (estimate) | Easy-moderate | nRF or ESP32, float or ultrasonic probe, wall-wart or coin cell, siren, LoRa module; BOM about $18-25 (estimate) | 3/4/5/4/4 = **20** |
| 2 | **Leak, Freeze and Vacancy Kit**: one small sensor node (leak probe, temperature, door contact) sold as a 4-pack or a 40-pack. This merges the leak kit and the vacancy node from the notes, which overlap. | Small landlords and PMs on unit turns: about $24 per sensor at volume plus $1/sensor/mo or $5/property/mo (estimate) | Homeowners and second-home owners: $29-39 per sensor, 4-pack $99, no plan (estimate) | Easy-moderate | nRF or ESP32, probe, coin cell, reed switch, LoRa or Thread; BOM about $8-14 (estimate) | 3/3/5/4/4 = **19** |
| 3 | **Tank Level Puck**: external, non-contact level sensing for propane, heating oil and generator fuel with no carrier plan. | Fuel distributors (route planning) and landlords with oil heat: about $59 plus $1-2/mo, optional API (estimate) | Rural and propane households: $79 once, local gateway (estimate) | Moderate | Ultrasonic or magnetic gauge, nRF or ESP32, LoRa, battery; BOM about $20-30 (estimate) | 4/3/4/3/3 = **17** |
| 4 | **Quiet Puck**: a no-subscription noise and occupancy sensor that never records audio. | STR managers and HOAs: about $99 plus an optional $5/property/mo log tier (estimate) | Small hosts and parents: $99 once (estimate; consumer demand unevidenced) | Easy-moderate | MEMS mic (level only), ESP32, LED ring, case; BOM about $12-20 (estimate) | 3/2/4/4/4 = **17** |
| 5 | **Pool Pad Watcher**: a vendor-neutral clamp-on vibration and current node for pool pumps. | Pool service firms: about $39 per node plus $2/mo (estimate) | Pool owners: $49 once (estimate) | Moderate | Current clamp, accelerometer, nRF or ESP32; BOM about $15-20 (estimate) | 3/3/4/3/3 = **16** |

### Area 2: Shops and venues

#### Summary
Health codes, loud rooms and shared-space etiquette give businesses real reasons to buy small displays and sensors, and the same objects already sit in homes. Consumer prices are the problem: $20-30 Govee-class sensors cap what a household pays. The wedge is a display-as-object or an outage-proof alert, not a better thermometer. Two items (room loudness, status light) are cheap builds close to the founder's taste.

#### Buyers
| Side | Who | US count | What they pay now |
|---|---|---|---|
| B2B | Restaurants and foodservice | More than 1 million outlets per the National Restaurant Association; other counts range about 731,000 to 1.2M+; independents fell 2.3% in 2025 (Technomic) | Monnit ALTA sensor about $98-104 reseller; iMonnit Premiere $45/yr up to 6 sensors, $120/yr up to 25 (reseller listings, may be stale); starter-kit reseller $7.95/sensor/mo |
| B2C | Households with chest freezers, kegerators, instruments, home offices | Not found | SensorPush HT1 $54.95, no monthly fee (vendor); Govee 2-pack about $28.87 (deal); Aranet4 about $250 CAD list; Luxafor Flag 2 about $43 |
| B2B | Bars and taprooms, cafes, coworking, studios | Not found (about 10k+ taprooms is an unsourced guess) | Kegtron Pro dual tap $534.99 plus $2/tap/mo (vendor); digital menu boards about $500-$2,000+ (vendor) |

#### Pain points
- B2B: Inspectors close or fine kitchens over cold-holding above 41 F; recent cases: rice at 50 F in a Pennsylvania walk-in, a Pittsburgh Subway ordered closed, a Florida restaurant with 63 violations (statute allows fines up to $1,000 per violation per day). [MyChesCo](https://www.mychesco.com/a/news/health-medical/unsafe-rice-dirty-kitchens-chester-county-inspectors-find-trouble/), [Yahoo](https://www.yahoo.com/news/articles/subway-pittsburgh-ordered-close-over-192709034.html), [Hoodline](https://hoodline.com/2026/08/kendall-restaurant-racks-up-63-health-violations-stays-open-anyway/)
- B2C: A forum post claims a $40 temperature alarm "saved $200 of food" (title only); Wi-Fi sensors go silent in an outage; one Temp Stick unit reportedly never reconnected from a freezer. [AmazingRibs](https://pitmaster.amazingribs.com/forum/accessorize-your-pit/digital-thermometers/1645789-my-40-temp-alarm-just-saved-200-of-food), [Weather Station Experts](https://theweatherstationexperts.com/temp-stick-review/)
- B2B: Restaurants are too loud; a Detroit noodle shop installed a decibel meter to set noise by daypart (2019, no product named). Cafes measured 68.7-75.9 dB(A) in one study. [The Takeout](https://thetakeout.com/could-decibel-meter-solve-restaurant-noise-problems-1836246073), [Fresh Cup](https://freshcup.com/the-difference-between-a-buzzing-cafe-and-a-noisy-one-is-smaller-than-you-think)
- B2C: Wine and guitar owners already use roughly $20 Bluetooth sensors and say they work. [Wine Berserkers](https://www.wineberserkers.com/t/temperature-gauge-for-cellar/160493)
- B2B: Bluetooth-only busy lights fail through doors (one Luxafor user report). [Luxafor](https://luxafor.com/product-tag/busy-light/)
- Not found: consumer-side evidence for loudness meters, owner reviews for Kegtron, and any 2025-26 demand data for business CO2 displays.

#### Existing players
| Company | Side | Price and plan | Gap or complaint |
|---|---|---|---|
| Monnit/iMonnit | B2B | Sensor about $98-104 plus free Basic or $45-120/yr tiers (reseller) | Cost; walk-in probe through the seal |
| ComplianceMate | B2B | Custom pricing for 5+ sensors, annual monitoring (third-party listing) | Quote-only |
| SensorPush, Govee, Temp Stick | B2C | $29-149, no subscription (vendor and deals) | Wi-Fi dependence, freezer reliability |
| Aranet, Airthings | B2C, some B2B | Aranet4 about $250 CAD list, one 2023 sale at $149 USD | Business demand since 2021 unproven |
| Luxafor | Both | Flag 2 about $43, Cube about $63, bulk-order page | Software-tied to Teams; Bluetooth range |
| Kegtron, Plaato | Both | Kegtron Pro $535 plus $2/tap/mo; older Kegtron about $150-240 no fee; Plaato about $164 | Plaato status unconfirmed |
| SoundPrint | B2C | Phone app | Not a venue display |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score B2B/B2C/Shared/Build/Fit |
|---|---|---|---|---|---|---|
| 1 | **Room Ring**: a loudness ring that shows a target zone and stores no audio. | Cafes, restaurants, coworking, gyms: $79-129 plus optional $4/mo hourly noise report (estimate) | Home studios, apartments, kids, streamers: $49-69 once (estimate; consumer pain unproven) | Easy | MEMS mic (level only), ESP32, LED ring, case; BOM about $12-20 (estimate) | 3/2/5/5/5 = **20** |
| 2 | **Door Light**: a local-radio in-session or open sign with no app, no cloud. | Photo, music and salon rooms, coworking: $39 per light, $199 for a 6-pack (estimate) | Home offices, streamers, creators: $29-49 once (estimate) | Easy | ESP32 or nRF, LED panel, button, battery; BOM about $10 (estimate) | 2/3/5/5/4 = **19** |
| 3 | **Air Object**: a design-led CO2 display that logs locally. | Cafes, gyms, studios, salons: $99-149 plus optional $4/mo log export (estimate) | Households and home offices: $99-149 once (estimate) | Easy-moderate | NDIR CO2 module (about $15-25, estimate), ESP32, e-paper or LED display | 2/3/5/4/4 = **18** |
| 4 | **Cold Guard**: a freezer-rated probe puck that alarms locally and over LoRa when power or Wi-Fi fails; one variant for humidors, wine and instruments (merged from the humidity idea, same hardware). | Restaurants and small shops: $49-69 per sensor plus $60/yr per site for logs and PDF export (estimate) | Chest-freezer and kegerator owners: $39-59 puck plus optional $79 hub, no plan (estimate) | Easy-moderate | nRF or ESP32, NTC probe, LoRa, siren; BOM about $8-12 puck, $25-45 with gateway (estimate) | 3/2/5/4/3 = **17** |
| 5 | **Tap Counter**: a flow and keg-level monitor with pay-once pricing. | Bars and taprooms: $149-199 per tap pair plus $2/tap/mo (estimate) | Home kegerator owners: $79-99 once (estimate) | Moderate | Flow meter or load cell, ESP32; BOM about $20-35 (estimate); NSF rules for wetted parts in commercial | 3/3/4/3/3 = **16** |

### Area 3: Trades, workshops and land

#### Summary
Machines and tanks are where per-unit monitoring is already normal in business, and where hobbyists improvise their own. A clamp-on current and air-quality node can be the same box in a garage and a machine shop. The farm tank monitor has the strongest B2B pricing evidence ($600 plus a fee) and a plausible consumer gap, but outdoor LoRa coverage and freezing make it a harder build.

#### Buyers
| Side | Who | US count | What they pay now |
|---|---|---|---|
| B2B | Machine shops | About 17,100 shops (paywalled report, estimate); NAICS 3327 lists 22,081 establishments | Per-machine monthly SaaS (MachineMetrics, Datanomix, Scytec); no public USD prices; UK TrackMyMachines from GBP 45/machine/month (vendor) |
| B2C | Hobby CNC, laser and 3D-print owners; woodworkers | Not found | SimplyPrint about $4/printer/month, 2 printers free (vendor); hobby PM2.5 monitors about $60 |
| B2B and B2C | Beef operations, ranches, hobby farms | 622,162 US operations with at least one beef cow (2022 Census), 55% under 20 cows, average 47 | Behlen Country Guardian $599.99 plus required annual subscription (vendor); AguaCheck about $500 plus $20/mo (older listing) |

#### Pain points
- B2B: Hidden costs of machine monitoring: edge hardware, integrations, training. [JITbase](https://www.jitbase.com/blog/best-machine-monitoring-software-top-10)
- B2C: Hobbyists build their own current-sensor "is it cutting" monitors and Arduino email alerts; no ready product found. Counter-view: many say never leave machines unattended, and a monitor does not stop a fire. [Sawmill Creek](https://sawmillcreek.org/goto/post?id=3400210), [V1 Engineering](https://forum.v1engineering.com/t/remember-kids-dont-leave-your-machines-running-unattended/25661)
- B2B: Checking livestock water uses "a considerable proportion of time and labor costs" per UNL (paraphrase). [UNL BeefWatch](https://beef.unl.edu/beefwatch/2024/modern-water-monitoring-technology-ranch)
- B2C: Woodworkers use about $60 PM2.5 monitors to decide on a respirator and doubt accuracy; most woodworking dust is above PM2.5. [Sawmill Creek](https://sawmillcreek.org/goto/post?id=3227155), [UK Workshop](https://ukworkshop.co.uk/threads/air-quality-testing.127507/post-1423001)
- B2B: Tool tags depend on a nearby phone (Milwaukee TICK is Bluetooth-only, about 300 ft). [Airpinpoint](https://airpinpoint.com/blog/milwaukee-tool-tracker-one-key)
- Not found: owner complaints about Behlen Guardian, US fence-monitor prices, silica-monitor costs, hobbyist counts.

#### Existing players
| Company | Side | Price and plan | Gap or complaint |
|---|---|---|---|
| MachineMetrics, Datanomix, Scytec | B2B | Per-machine SaaS, no public price | Low end (clamp-on only) unserved |
| SimplyPrint, 3DPrinterOS | Both | About $4 and $9.50 per printer/month (vendor) | Little revenue per printer |
| Behlen Guardian, AguaCheck, Ranchbot | B2B | About $500-600 plus subscription | Carrier fees; Verizon-only (Behlen) |
| Gallagher i Series | B2B | Price not retrieved | Tied to its own energizers |
| Milwaukee TICK, Hilti ON!Track, Airpinpoint | B2B | TICK $29 1-pack, $99 4-pack at launch (press); Airpinpoint $11.99/device/mo | Bluetooth only, phone required |
| Mopeka, Generac, Veeder-Root | Both | $161-210 cellular (retailer) | Cellular plans $5-25/sensor/mo (vendor claim) |
| Growlink, TrolMaster, Ecowitt | Both | Hub $299-399 (retailer) | Crowded |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score B2B/B2C/Shared/Build/Fit |
|---|---|---|---|---|---|---|
| 1 | **Shop Air Node**: PM2.5/PM10, VOC, noise and compressor current in one local dashboard. | Small shops and school shops: about $150 plus $5/node/mo for logs and alerts (estimate); not OSHA-grade | Woodworkers and garage makers: $90-130 once (estimate) | Easy | PM sensor, VOC, MEMS mic, CT clamp, ESP32; BOM about $35-45 (estimate) | 3/3/5/5/5 = **21** |
| 2 | **Machine Pulse**: a clamp-on run, idle and alarm monitor for CNCs, lasers, printers and compressors. | Machine shops and print farms: about $30-60 per machine plus $4-8/machine/mo fleet tier (estimate) | Hobby CNC, laser and print owners: $35-50 once, local Home Assistant feed (estimate) | Easy-moderate | CT clamp, ESP32, RGB light; BOM about $12-18 (estimate); use a UL-listed CT | 3/3/5/4/5 = **20** |
| 3 | **Power Sentinel**: a clamp and float node for sump, well pump, compressor and freezer on/off. | Small shops, landlords, farms: about $70 plus $4/mo (estimate) | Homeowners: $50-70 once (estimate) | Easy | CT clamp, float input, ESP32 or nRF; BOM about $18 (estimate) | 3/3/5/5/4 = **20** |
| 4 | **Trough Monitor**: a solar LoRa stock-tank level and open-gate node, with fence voltage as a later add-on. | Ranches and farms: about $300-400 per node plus optional $5/mo fleet map (estimate), against the $500-600 incumbents | Small herds and hobby farms: $150-250 once, local LoRa gateway (estimate) | Moderate | Ultrasonic or pressure sensor, nRF or ESP32, LoRa, solar cell; BOM about $25-40 (estimate) | 4/3/5/3/3 = **18** |
| 5 | **Tool Tag**: mixed-brand tool tags with a local gateway and no cloud. | Contractor crews and shops: about $12/tag plus $10/mo fleet software (estimate) | Garage and van owners: $15-25 per tag (estimate; weak consumer evidence) | Moderate | nRF tag with coin cell, $40 gateway; BOM about $6/tag (estimate) | 4/2/4/3/4 = **17** |

Notes: the notes' greenhouse and soil node (3/3/2 each side, crowded), print-status puck (about $4/printer/month caps revenue) and fence-voltage monitor (US pricing unknown) were screened but not ranked into the top five. The fuel and generator tank node is folded into Area 1, Idea 3.

### Area 4: On the move and community

#### Summary
Pets, boats and RVs have the best two-sided evidence in this whole screen: documented consumer products and prices, plus a named business or rule on the other side (kennel temperature rules, marina metering, boat fleet plans). The recurring trap is cellular. Anything that must follow a moving asset needs a carrier plan or a crowdsourced network, which breaks pay-once. Stationary or gateway-based designs avoid it.

#### Buyers
| Side | Who | US count | What they pay now |
|---|---|---|---|
| B2C | Pet owners, RV owners, boaters | 94M pet households (APPA 2025), 95M in 2025 (APPA May 2026 update); about 8.1M RV-owning households (2025 Go RVing study; RVIA says about 10M); 11.8M registered boats (NMMA 2024) | Waggle device about $94-159 plus $25-39/mo or prepaid $119-199; RV surge and EMS units $261-349; ShockAlarm about $59-99; Siren 3 about $299.99 plus $125-180/yr |
| B2B | Kennels, groomers, boarding | Not found | Monnit wireless kennel sensors; Kestrel DROP used for Pennsylvania dog warden inspections |
| B2B | Marinas, campgrounds, storage yards | Not found | Marina power centers $1,000-1,500 per slip (800+ slips case); 42 pedestals priced at $38,584 (about $919 each, my arithmetic); Boat Fix fleet $139/yr per unit |

#### Pain points
- B2C: Waggle users cite cost (one reviewer computes about $298/yr), battery life, connectivity and temperature accuracy; Trustpilot shows price hike and automatic charge complaints (some reviewers may be affiliates of a competitor). [Everywhere With Claire](https://everywherewithclaire.com/waggle-rv-pet-monitor-reviews/), [Trustpilot](https://es.trustpilot.com/review/mywaggle.com?page=7)
- B2B: 14 dogs died of heat exhaustion at a Saskatoon kennel, which then added sensors in seven locations. Pennsylvania rules require temperature and humidity records per room and correction within 4 hours above an 85 F heat index. [Global News](https://globalnews.ca/news/2974529/playful-paws-adds-safeguards-after-14-dogs-die-at-the-saskatoon-kennel/), [7 Pa. Code 28a.4](https://www.law.cornell.edu/regulations/pennsylvania/7-Pa-Code-SS-28a-4)
- B2C: RV owners report low voltage, bad breakers and a microwave lost to pedestal wiring; portable $250-500 units get stolen. [JaycoOwners](https://www.jaycoowners.com/goto/post?id=5655965), [Montana owners](https://www.montanaowners.com/threads/do-i-need-a-power-surge-protector.964234/page-2)
- B2B: Marinas are replacing power centers and adding remote meters. Practical Sailor warns shock alarms can give swimmers false security. [Marina Dockage](https://www.marinadockage.com/?p=10546), [Practical Sailor](https://www.practical-sailor.com/subscriber-only/preventing-electric-shock-at-the-dock)
- B2C: Rechargeable tracker battery life and subscription creep are the recurring complaints (aggregator sources). [Logistimatics](https://logistimatics.com/blogs/guides/best-gps-tracker-for-rv)
- Not found: kennel and marina counts, Amazon or Trustpilot text for Siren and trackers, any consumer pricing or reviews for e-bike charging monitors.

#### Existing players
| Company | Side | Price and plan | Gap or complaint |
|---|---|---|---|
| Waggle | B2C | Device about $94-159 plus $25-39/mo | Subscription anger, battery, accuracy |
| Monnit | B2B | Generic wireless sensors with text, email and call alerts | Not kennel-specific |
| Progressive Industries and other RV EMS | B2C | $261-349 (retailer snapshots) | Theft of portable units; no pedestal-side data |
| ShockAlarm | B2C | About $59-99 (2020 forum) | Passive alarm, false-security warning |
| HarbaPower, VoltSafe | B2B | Pedestal metering and billing, price not public | Installer-led |
| Siren Marine | Both | Siren 3 about $299.99; $125-180/yr plans; Boat Fix fleet $139/yr | Cellular fees |
| Tracki, Spytec, Monimoto | B2C | From $9.95/mo, $24.95/mo, $179 plus $49/yr (affiliate sources) | Plans |
| Pebblebee, AirTag | Both | Airpinpoint assumes $2.99/tag/mo Pro (vendor-produced) | Platform networks are the moat |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score B2B/B2C/Shared/Build/Fit |
|---|---|---|---|---|---|---|
| 1 | **Pet Heat Watch**: a temperature and power-loss node with a local siren and a free LoRa or BLE hub. | Kennels, groomers, boarding: about $25 per node plus $10-20/mo for compliance log export (estimate), 8-16 nodes per site | Home, car and RV pet owners: $49-79 once (estimate); RV needs a phone or cell fallback | Easy | nRF or ESP32, temperature and humidity sensor, siren, LoRa or BLE; BOM about $12-20 (estimate) | 3/3/5/5/4 = **20** |
| 2 | **Dock Sentinel**: a boat, trailer and stored-RV sentinel on LoRa and BLE that reports to a gateway the marina or yard owns. | Marinas and storage yards: gateway $199-299 plus $1-2/unit/mo (estimate) | Owners: $79-129 once, no plan (estimate); no moving-theft recovery | Easy-moderate | nRF, LoRa, bilge and voltage and temperature inputs, primary cell; BOM about $18-30 (estimate) | 3/3/4/4/5 = **19** |
| 3 | **Shore-Power Watch**: a read-only non-contact monitor of voltage, frequency, current and leakage with logging. | Marinas and campgrounds: pedestal node $150-250 plus $2-4/pedestal/mo (estimate) | RV and boat owners: $99-149 once (estimate) | Moderate | Clamp CT, isolated voltage sense, LoRa or BLE; BOM about $25-40 (estimate) | 3/4/4/3/3 = **17** |
| 4 | **Rental Tag**: a tag plus dashboard for rental bikes, trailers and equipment. | Small rental operators: about $29 per tag plus $3-12/tag/mo, matching Airpinpoint-class plans (estimate) | Bike and trailer owners: $15-25 once (estimate); AirTag is the incumbent | Easy-moderate | nRF tag, battery; Find My compatibility needs Apple and Google programs (unresearched) | 3/2/5/4/3 = **17** |
| 5 | **E-Bike Charge Watch**: a plug-load and temperature monitor for charging spots (a monitor only, not a life-safety alarm). | Shops, delivery fleets, landlords: about $60 plus $5/mo (estimate) | Garage and apartment riders: $40 once (estimate; consumer evidence not found) | Moderate | Plug-load sensor, temperature probe, ESP32; fire-code detection (UL) would be heavy certification | 3/2/3/3/2 = **13** |

## Hybrid ranking: shop air and pet heat lead, but only three ideas have evidence on both sides

| Rank | Idea (area) | Score | Evidence on both sides? | Biggest risk |
|---|---|---|---|---|
| 1 | Shop Air Node (3) | 21 | Both (thin, forum snippets and school shop reading) | Dust sensors are inaccurate on coarse sawdust; business buyers may want compliance-grade |
| 2 | Pet Heat Watch (4) | 20 | Both | RV use needs cellular; life-safety liability if an alert fails |
| 3 | Sump and Crawlspace Puck (1) | 20 | B2C only | Business side is inferred; mains-adjacent wiring |
| 4 | Room Ring (2) | 20 | B2B only | Consumer pain unproven; a mic invites privacy worries |
| 5 | Machine Pulse (3) | 20 | Both | Hobbyists treat it as fire safety, inviting liability; OEMs absorbing features (Bambu flame detection) |
| 6 | Power Sentinel (3) | 20 | Neither | Commodity leak sensors; weak differentiation alone |
| 7 | Leak, Freeze and Vacancy Kit (1) | 19 | Both | YoLink price floor near $10 per sensor |
| 8 | Door Light (2) | 19 | Both | Low pain on both sides; Luxafor already spans both |
| 9 | Dock Sentinel (4) | 19 | Both | LoRa cannot recover a moving stolen asset; gateway chicken-and-egg |
| 10 | Air Object (2) | 18 | B2C only | Business pain is soft; NDIR module cost |
| 11 | Trough Monitor (3) | 18 | Both | Outdoor build, LoRa coverage, carrier cost if cellular |
| 12 | Shore-Power Watch (4) | 17 | Both | Electrical-safety certification and liability |
| 13 | Cold Guard (2) | 17 | Both | Govee price floor; incumbents bundled on the business side |
| 14 | Tank Level Puck (1) | 17 | Both | Distributors want their own telemetry; fuel hazard near gas |
| 15 | Quiet Puck (1) | 17 | B2B only | Consumer side is really small hosts; no-subscription hurts B2B recurring revenue |
| 16 | Tool Tag (3) | 17 | B2B only | Tracking without a network is weak; AirTag exists |
| 17 | Rental Tag (4) | 17 | Both | Find My coverage cannot be matched by an independent tag |
| 18 | Pool Pad Watcher (1) | 16 | Both | Pool techs fear disintermediation |
| 19 | Tap Counter (2) | 16 | Both | Small market; NSF rules for commercial |
| 20 | E-Bike Charge Watch (4) | 13 | B2B only | Missed fire is the worst liability; likely heavy certification |

**Top 5 to deep-dive, preferring two-sided evidence over raw score:**
1. **Pet Heat Watch.** Named products and prices on both sides (Waggle plans and complaints, Monnit kennel sensors), a real disaster, a state rule that requires temperature records, the cheapest build, and 94M pet households.
2. **Water family (Sump Puck plus Leak, Freeze and Vacancy Kit).** Strongest buyer counts and insurer pull; deep-dive whether to ship one SKU. The business half (landlords) needs direct testing.
3. **Machine Pulse (with Shop Air Node as a second sensor head).** Per-machine SaaS is normal for business and hobbyists build their own versions; the same clamp board drives both.
4. **Shop Air Node.** Top score and top founder fit, but both sides rest on forum snippets, so validate demand before building.
5. **Shore-Power Watch.** Best two-sided pricing evidence (RV EMS at $261-349, marina metering at about $919 per pedestal) and a LoRa gateway shared with Dock Sentinel, but only worth it as a read-only, non-contact design that stays clear of heavy certification.

## How hybrids work

Companies that sell one device to both sides split it by software tier, channel and licensing, not by hardware. No source gave a consumer-versus-business revenue split for any of them.

| Company | One device, two markets | Pricing and plans | Channel |
|---|---|---|---|
| Minut | Same sensor for a single host and a 20+ unit manager | Sensor is a one-time cost; Starter $5/mo (single property), Standard $10, Pro $15 per home; Enterprise custom at 20+ units; Call Assist add-on $10/mo ([Minut pricing](https://www.minut.com/pricing), [Minut support](https://support.minut.com/en/articles/14686401-how-to-choose-a-minut-plan)) | Self-serve below 20 units, sales above |
| Sonos Pro | Existing speakers used in shops | $35/month per location with multi-location dashboard and commercially licensed music; launched April 2023 after organic business adoption ([CE Pro](https://www.cepro.com/audio-video/sonos-pro-marks-companys-entry-into-commercial/)) | Partner music services |
| Shelly | Plus (consumer) and Pro (DIN-rail) lines | Wholesale pricing for verified installers ([CE Pro](https://www.cepro.com/news/shelly-dealer-program-details-and-how-to-register/621760)) | Installer portal plus existing distributors, no field sales team |
| Ecobee | Same thermostat | Bulk quotes for multifamily; Pro PIN identifies contractor installs; a Pro-exclusive Lite model ([Ecobee](https://www.ecobee.com/contractors)) | Email and PIN, no registration gate |
| Ring | Home doorbells at commercial properties | Requires Ring Protect; commercial monitoring excludes smoke and CO; permit and false-alarm fees apply ([Ring support](https://support.ring.com/hc/en-us/articles/360029632152)) | Consumer retail |
| Tile | Tracker | Enterprise routed through a partner (Band24) rather than in-house ([Life360](https://www.life360.com/business)) | Partner-run |
| Emporia | Vue 3 three-phase for light-commercial | $209.99 listing, no subscription (vendor) ([SmartHomeCompared](https://smarthomecompared.com/energy-monitors/emporia-vue-3-3-phase)) | Electrician install advised |
| Luxafor | Busy light | Flag 2 about $43 up to meeting-room models, bulk-order page ([Luxafor](https://luxafor.com/bulk-orders/)) | Retail plus bulk page |

**Patterns found:** (1) one SKU with tiered per-unit software (Minut); (2) consumer hardware plus a commercial software license (Sonos Pro); (3) consumer brand plus installer channel (Shelly, Ecobee, Aqara); (4) enterprise handed to a partner (Tile). A fifth pattern, the "prosumer": a small business buying like a consumer, is the pattern a solo founder can serve (estimate; evidence is indirect).

**Pricing rules:** Per-unit recurring is accepted when tied to a business activity (Minut, Sonos Pro) and rejected when it is a price hike on something bundled: Ring Protect Basic rose 25% from $39.99 to $49.99 a year in March 2024 with no new features, and customers complained ([Subscription Insider](https://www.subscriptioninsider.com/article-type/news/amazons-ring-increases-ring-protect-pricing-by-25-for-basic-plan)). Emporia and YoLink market the absence of a subscription (vendor). A location fee such as Sonos at $35 is about 3-7 times the per-unit consumer plans seen in Ring at $5-10 (my comparison).

**Failure modes:** The one concrete dropped-side case found is Phlock, a smart-lock startup that moved from homeowners to B2B, won pilots, then ran out of cash waiting on 9-12 month enterprise cycles (secondary blog, founder account) ([The Linux Code](https://thelinuxcode.com/what-i-learned-from-phlock-my-hardware-startup-that-disappeared/)). Smart-home shutdowns (Brilliant 2024, Otto, Revolv, Quirky) were general hardware failures, not B2B/B2C-specific. Life-safety and mains functions turn "business" into a legal burden (Ring restricts smoke/CO; Emporia warns about panel voltage). No sourced case of UL or insurance forcing a company out of a side was found. Channel conflict is a risk where dealers exist (Aqara requires resellers to hold MSRP).

**What this means for the design:**
- One SKU, one price list, no separate B2B hardware.
- A free app and local operation; paid tier only for multi-site dashboard, staff alerts, audit logs, API and support.
- Self-serve annual plans (Stripe) up to about 20 units, then wholesale via a distributor or Shopify B2B; refuse custom contracts below that (estimate, borrowed from Minut's threshold).
- Sense, log and notify only. No switching, no smoke/CO claims, no mains-voltage in v1.
- Pre-certified radio modules; FCC modular approval cost, UL requirements, insurance and Shopify B2B or Amazon Business details were not researched.

## Forums the founder should read personally

- **r/HomeImprovement, r/landlord, BiggerPockets, Airbnb Community (hosts):** reveals whether landlords want a sump or leak sensor at all and what they pay; the notes could not reach any of these.
- **r/restaurateur, r/KitchenConfidential:** how kitchens handle cold logs and whether anyone would pay for a loudness or CO2 display; not reached.
- **r/Homebrewing, r/guitars, r/cigars:** consumer demand for kegerator, humidity and temperature sensors; not reached.
- **Sawmill Creek, Lumberjocks, r/woodworking, r/hobbycnc, r/3Dprinting, r/lasercutting:** whether hobbyists want run monitoring and dust readings, and how they view fire liability; only snippets were seen. Pro Tool Reviews returned an error.
- **r/farming, r/CattleRanchers, Homesteading forums:** Behlen Guardian owner complaints (frozen tanks, accuracy), real willingness to pay; none found.
- **Trawler Forum, Cruisers Forum, iRV2, Jayco and Forest River owner forums:** shore-power failures, pedestal quality and what owners do about it; only snippets were read.
- **r/RVLiving, Waggle Trustpilot and Amazon reviews:** how much owners really resent the monthly fee and what they would pay once.
- **Amazon and Trustpilot reviews for Govee, SensorPush, Temp Stick, YoLink, Siren, Kegtron:** the missing "pain in own words" for most ideas.
- **Kennel and groomer groups, state kennel inspector pages:** whether the temperature log rule is common beyond Pennsylvania.
- **Marina manager and campground owner groups:** whether they would host a gateway or buy a pedestal node.

## Conclusion

The hybrid thesis holds in pockets: pets, water, shop machines and shore power. The corridor is narrow because consumer prices are pinned to $20-30 and the business half pays only for logs, alerts across locations and compliance. The safest build is one small sensor family on shared hardware (temperature, power-loss, current clamp, air) with a free local app and a simple per-location plan, then letting the first 50 buyers on each side show which side pulls. Before spending on tooling, the evidence gaps above need closing: the top five rest mostly on vendor pricing and inference, so a week of reading the listed forums and talking to five kennel owners, five landlords and five shop owners is worth more than another desk pass.
