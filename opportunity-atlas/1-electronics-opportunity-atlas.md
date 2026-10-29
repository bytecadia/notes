# Twenty sectors, five sensor bets worth testing

The best openings for a solo, privacy-first hardware founder are not in any one sector. They are in a single repeated pattern: **a cheap, battery-powered radio sensor (ESP32/Nordic plus LoRa or BLE) that reports to a local hub, sold for a one-time price into a category where incumbents charge per device per month.** That pattern scores 19-21 out of 25 in at least eight sectors. It covers stock-tank levels, self-storage unit doors, short-term-rental noise, walk-in coolers, leak/freeze pucks, machine run-time clamps, proof-of-visit tags and school aerosol sensors. Of the roughly 100 ideas screened, only five have real-user evidence behind them. In order of evidence strength they are **proof-of-visit tags for lawn and cleaning crews** (LawnSite operators repeatedly fight "you didn't mow" non-payment), **school vape/aerosol sensors** (news reports of false-alarm floods, with a median **$925 per detector** in district contracts), **self-storage door sensors** (operators already buy unit alarms but complain about batteries and false alarms), **no-subscription STR noise monitors** (Trustpilot and host-forum complaints about Minut billing) and **clamp-on CNC monitors** (incumbents charge **$240-$1,200 per machine per year**, vendor figures). The top-scoring idea on paper, a **solar LoRa stock-tank monitor (21/25)**, rests only on a price gap: rivals charge $400-$550 plus $99-$420 a year, but no rancher voice was found. A pass through the forums listed at the end is the cheapest next step. Automated research could not open Reddit, Airbnb Community, Practical Machinist, Self-Storage Talk or LawnSite, so most demand claims remain untested.

## How to read this screen

Each sector section follows the same layout: Summary, Key facts, Buyers, Pain points, Existing players, Ideas. **Establishments, employment and value added come from one source for every sector**: BLS QCEW 2024 annual averages (all ownerships summed) and BEA 2025 value added via the DBnomics mirror ([QCEW open data](https://www.bls.gov/cew/additional-resources/open-data/); [BEA via DBnomics](https://db.nomics.world/BEA/GDPbyIndustry-1)). QCEW excludes the self-employed and most farm operators, so sectors 11 and 92 are undercounted. BEA's real-estate value added includes imputed rent on owner-occupied housing, and its "Government" line covers all government, not just NAICS 92. Figures from these two sources supersede any sector size in the other notes.

Scores are the researchers' judgments on five 1-5 criteria: **P**ain, **W**illingness to pay, **O**pen space, **B**uildable solo, founder **F**it. In several sectors the researchers' stated totals did not equal the sum of their component scores (sectors 11, 21, 22, 48-49 and 56). This report uses the sum of the components and shows the stated total in brackets. Scores were changed only where the validation notes gave evidence, marked **[adj]** and explained. Labels used throughout: **(vendor)** means the figure comes from a company selling in the category; **(unverified)** means a secondary or snippet-level source the researchers could not confirm; **not found** means the research looked and came up empty. Reddit and most trade forums were not accessible to any researcher, so every "pain" row rests on trade press, surveys, vendor material or local news unless stated otherwise.

## Sector-by-sector screen

### NAICS 11: Agriculture, Forestry, Fishing and Hunting

#### Summary
About 1.88 million mostly small farms buy inputs through dealers, co-ops and online stores. Margins are volatile, so tools that pay back within two years sell. Remote monitoring of water, fences and grain where there is no coverage is the clearest electronics gap. Incumbents such as Gallagher are expensive or charge subscriptions.

#### Key facts
**114,570 establishments, 1,259,402 employees, $255.9B value added (2025)** ([QCEW 11](https://data.bls.gov/cew/data/api/2024/a/industry/11.csv)). QCEW misses most farm operators. NASS counts **1.88M farms in 2024**, averaging 466 acres ([NASS](https://esmis.nal.usda.gov/sites/default/release-files/5712m6524/z316rz25j/db78w849h/fnlo0225.pdf)). Net farm income was forecast at $140B for 2024 ([DTN](https://www.dtnpf.com/agriculture/web/ag/crops/article/2024/09/05/usda-moderates-forecast-losses-2024)). Key rules: FCC Part 15 for unlicensed radios, which pre-certified modules cover, and fence-energizer standards (both from the researchers' reading; no source retrieved).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Small/hobby and mid-size livestock and crop farms | Most of 1.88M farms; split by size not found | Online and farm stores; owner decides; price-sensitive |
| Commercial ranches and large grain operations | Not found | Ag dealers, co-ops, extension-recommended brands; accept subscriptions if payback is clear |
| Ag service channel (irrigation dealers, electric co-ops) | Not found | Resell and install |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Checking remote stock tanks | Trips about **$1,560/yr**; monitor $1,800 + $100 install + $3-10/mo, ~2-yr payback if trips halve ([USU Extension](https://extension.usu.edu/rangelands/research/remote-sensing-stock-tanks.php)) | Drive out; cameras; cellular or satellite monitors (~$30/mo satellite, [UNL](https://beef.unl.edu/beefwatch/2024/modern-water-monitoring-technology-ranch)) |
| Stored-grain spoilage | Loss per bin not found; cables ~5 cents/bushel ([The Farmer](https://editions.mydigitalpublication.com/article/Bin+sensors+provide+peace+of+mind/5012528/849774/article.html)) | Bin cables; some vendors charge for remote access |
| Electric-fence faults let stock out | Cost of escapes not found | Gallagher monitors ($277.99-$349.99) |
| Pump motors damaged by single-phasing | Not found | Non-connected phase-monitor relays ([UC ANR](https://ucanr.edu/sites/uccemodoc/files/124624.docx)) |
| Income volatility caps spending | Context only | Delay purchases |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Gallagher | Fence monitor; tank monitor (cellular/satellite) | Fence monitor $349.99, fault finder $277.99 ([Gallagher](https://store.am.gallagher.com/am/us/en_US/animal-management/electric-fencing/power/c/remotes-and-fence-testers)); tank monitor $399.99 + $99/yr (unverified) | Costly; ecosystem lock-in |
| Ranchbot | Trough Direct (satellite) | $549 + ~$270/yr (unverified) ([Feedlot](https://www.feedlotmagazine.com/news/company_news/ranchbot-introduces-trough-direct-stand-alone-satellite-connected-water-monitoring-system/article_0e01461c-eae9-11ef-a846-9febf03c61e8.html)) | Subscription |
| Tank Toad | Solar sonar tank monitor | Cellular renewal $420/yr ([Solar Store](https://thesolarstore.com/products/satellite-tank-toad-solar-powered-satellite-tank-monitor)) | Subscription |
| Lonestar, Farmbot, Farmo, Goanna | Tank monitors | Not found | Subscription models |
| Guardian, TeleSense, OPI, Prairie Grain | Grain-bin monitoring | ~5 c/bu; remote access sometimes paid | Subscription for remote access |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Stocktank LoRa**: tank-level node and solar gateway on LoRa, local display, no cloud | Ranches pay to cut trips; $150-250/node + optional $5/mo alerts | Hobby farmer, ~$99 node + $79 gateway | Easy | ESP32/LoRa, ultrasonic or 4-20mA pressure sensor, e-paper, solar + LiPo, optional cellular gateway | 4/4/4/5/4 = **21** |
| 2 | **Fence Watch**: clamp-on fence-voltage sensor radioing to a base display | Ranches; $60/node + $10 per gateway | $59 | Easy | High-voltage divider, LoRa, e-paper | 3/4/4/5/4 = **20** |
| 3 | **Pasture Radio Ear**: local "farm dashboard" aggregating all nodes, no cloud | None (B2C only) | $149 | Easy-moderate | ESP32, LoRa, display | 2/2/4/4/5 = **17** [stated 15] |
| 4 | **Bin Probe**: wireless temp/CO2 puck for bins, no subscription | Grain operations; $40-80/probe | Same, $40-80 | Moderate | Thermistor strings, NDIR CO2, BLE/LoRa | 4/3/2/4/3 = **16** [stated 18] |
| 5 | **PhaseGuard Mini**: pump phase-loss relay with LoRa alert | Irrigation dealers, $120-200 | Not specified | Moderate (mains switching raises UL concerns) | Phase sensing, relay, LoRa | 3/3/3/3/3 = **15** [stated 18] |

### NAICS 21: Mining, Quarrying, and Oil and Gas Extraction

#### Summary
Marginal oil and gas wells and small quarries are numerous, have thin margins and are driven by compliance. Remote tank and well monitoring is a proven paid category with high incumbent prices. Hazardous-location certification is the main barrier for a solo founder (researchers' inference), so the realistic entry is a non-hazardous water or fuel tank variant.

#### Key facts
**30,746 establishments, 587,151 employees, $398.7B value added** ([QCEW 21](https://data.bls.gov/cew/data/api/2024/a/industry/21.csv)). There were about **770,000 marginal wells in 2016**, producing 11-15% of US oil and gas; a current count was not found ([EIA](https://www.eia.gov/todayinenergy/detail.php?id=27272)). MSHA counts **12,721 mines and 328,732 miners** in FY2024 ([MSHA](https://www.msha.gov/sites/default/files/Data_Reports/Charts/FY2024-MSHA-ataGlance-1-31-2025.pdf)). Key rules: EPA OOOOb/c methane rules, with most deadlines pushed to Jan 22, 2027 and reconsideration ongoing (sources conflict on dates) ([Gable Law](https://www.gablelaw.com/wp-content/uploads/2026/08/Clean-Air-Act-Pulse-Check-Where-EPAs-NSPS-OOOObc-Methane-Rules-Stand-Today.pdf)); MSHA dust rules; Class I Div 1/ATEX hazardous-location rules (no source retrieved).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Small independent oil/gas operators | Not found (over 50% of marginal-well output is from private operators, [Argus](https://www.argusmedia.com/es/news/2092308-us-stripper-wells-among-first-to-face-shutdown-rystad)) | Owner or pumper decides; oilfield supply houses and SCADA resellers |
| Quarry and aggregate operators | ~4,286 stone + 6,198 sand and gravel (2023, [NIOSH](https://wwwn.cdc.gov/niosh-mining/MMWC/Mine)) | Plant manager or safety lead; distributors |
| E&P compliance teams and leak-detection contractors | Not found | Per site; contractor LDAR ~$250/site (advocacy source, [EDF](https://www.edf.org/hXi)) |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Driving out to gauge tanks and check wells | Remote service $55/mo ([iWell](https://www.iwell.info/remote.php), vendor); legacy SCADA $2,000-5,000/well (vendor) | Pumper visits; SCADA |
| Methane LDAR compliance on marginal wells | Industry claims ~300,000 wells could shut (advocacy) ([CSU METEC](https://metec.colostate.edu/marginal-wells/)) | Contractor surveys |
| Quarry dust exposure monitoring | Not found | Periodic sampling |
| Tank overfill and spills | Not found; operators climb tanks to gauge ([Emerson](https://s1-live.emerson.com/documents/automation/case-study-oil-gas-producer-improves-spill-prevention-program-reduces-field-operating-costs-rosemount-en-74536.pdf), vendor) | Manual gauging |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| iWell | Remote well and tank service | From $55/mo (vendor) | Subscription |
| Baker Hughes SentryNet, Emerson Rosemount, Digi/Innotek OverWatch, eLynx | Tank and well monitoring | Not found | Enterprise sales cycles; lock-in (inference) |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **TankEye Lite**: solar LoRa radar tank level with high-level alarm | Low-volume well sites; $300-500/unit + optional $10/mo | Rural owners of fuel/water tanks, $149 | Moderate-hard in hazardous areas; easy for non-hazardous B2C | Radar level sensor, LoRa, solar | 4/4/3/3/2 = **16** [stated 17] |
| 2 | **Dust Tag**: optical particulate node for quarries (not a certified silica method) | Quarries, $200 | Workshops, $79 | Moderate | Optical PM sensor, LoRa | 3/3/3/4/3 = **16** [stated 15] |
| 3 | **Pumper Pager**: rugged vibration well-status node with local LED | Operators; price not specified | Not specified | Moderate | Accelerometer, LoRa, LED | 3/3/3/4/3 = **16** [stated 14] |
| 4 | **Acoustic leak finder**: handheld ultrasonic leak detector | Contractors, ~$300 | Not specified | Moderate | Ultrasonic MEMS mics, DSP | 2/3/3/3/4 = **15** [stated 13] |
| 5 | **Methane Sniff Beacon**: fixed low-cost methane sensor on LoRa for LDAR screening | LDAR contractors and operators; price not specified | Not specified | Hard (gas calibration, area ratings) | Methane sensor, LoRa | 4/3/3/2/2 = **14** [stated 15] |

### NAICS 22: Utilities

#### Summary
Utilities are heavily regulated and buy slowly. Small co-ops, municipal utilities and tens of thousands of small water systems are underserved and short of budget. On the consumer side the opportunity is household resilience, such as outage awareness, rather than selling to utilities.

#### Key facts
**33,012 establishments, 856,308 employees, $507.7B value added** ([QCEW 22](https://data.bls.gov/cew/data/api/2024/a/industry/22.csv)). US customers averaged **~11 hours of outages in 2024**, nearly double the prior-decade average ([EIA](https://www.eia.gov/todayinenergy/detail.php?id=65925)). **42,199 small water systems** make up 82% of community water systems (2016, [EPA OIG](https://19january2021snapshot.epa.gov/sites/static/files/2016-03/documents/20160322-16-p-0108_glance.pdf)). Key rules: Lead and Copper Rule Revisions, with service-line inventories due Oct 16, 2024 ([Illinois EPA](https://www.illinois.gov/news/press-release.31010.html)). NERC CIP and UL/NEC for mains devices: no source retrieved; researchers advise avoiding grid-tied and life-safety products.

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Rural co-ops and small municipal utilities | 812 co-ops + 1,958 public power (2017, [EIA](https://www.eia.gov/todayinenergy/detail.php?id=40913)) | General manager; distributors, state associations, conferences |
| Small water systems | ~42,000 (2016) | Operator or board; grant-funded; circuit riders, rural water associations |
| Rural and off-grid households | Not found | Amazon or direct (B2C) |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Outages with no local awareness | ~11 h/yr; cost per hour not found | Utility outage maps; generators |
| Small-system water loss, thin staffing | ~1 in 5 gallons lost, $6.4B/yr (unverified, startup blog citing Bluefield) | Manual rounds; SCADA described as "million-dollar-plus" ([WWD](https://www.wwdmag.com/data-scada/small-town-scada-yields-big-time-results)) |
| Lead service line inventory burden | Not found | Paper or software inventories |
| Voltage events damaging farm loads | Not found | Phase monitors |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Mission Communications | Cloud SCADA for small utilities | Not found | Price and complexity for small systems (vendor case studies) |
| High Tide Technologies | Utility monitoring | Not found | Same |
| 120Water | Lead inventory software | Not found | Software only |
| Consumer outage/power monitors | Various | Not researched | Not researched |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Pole Notice**: local-first outage and voltage-sag logger that chirps or texts | Co-ops buy in bulk for member programs, ~$50/unit | Home or farm, $79-129 | Moderate (isolated mains sensing via plug-in/clamp) | ESP32, isolated voltage sensing, e-paper | 4/3/3/4/4 = **18** [stated 17] |
| 2 | **Leak Ear**: acoustic hydrophone logger for water mains | Small water systems, $300 | Not specified | Moderate | Hydrophone, ADC, LoRa | 3/3/3/4/4 = **17** [stated 15] |
| 3 | **Tiny SCADA for Tiny Water**: LoRa tank/pump/pressure node kit for systems under 500 connections | $400/site + optional $10/mo | Not specified | Moderate | LoRa nodes, pressure and level sensors | 4/3/3/3/3 = **16** |
| 4 | **Whole-farm meter display**: CT-clamp usage display, local only | Not specified | $129 | Easy | CT clamps, ESP32, display | 2/3/3/4/4 = **16** [stated 14] |
| 5 | **LSL Field Tagger**: NFC handheld logger for lead-line inventory crews | Water systems; price not specified | None | Easy (tiny market) | NFC, handheld logger | 3/2/3/4/2 = **14** [stated 11] |

### NAICS 23: Construction

#### Summary
Money flows from owners to general contractors to specialty subcontractors through progress billing. Small trade contractors buy tools through distributors, big-box stores and online. The documented pains are tool and equipment theft, labor shortage and silica-dust compliance. Tool tracking is crowded with Milwaukee and Hilti, but cheap, brand-neutral, privacy-first jobsite sensing looks open.

#### Key facts
**944,595 establishments, 8,317,572 employees, $1,340.0B value added** ([QCEW 23](https://data.bls.gov/cew/data/api/2024/a/industry/23.csv)). **92% of firms report difficulty hiring** and 45% report delays from worker shortages ([NCCER/AGC 2025](https://www.nccer.org/newsroom/report-92-percent-of-construction-firms-struggling-to-hire-workers/)). Key rules: the OSHA silica rule sets a PEL of 50 µg/m³, and employers either follow Table 1 controls or measure exposure ([Norton Rose Fulbright](https://www.nortonrosefulbright.com/en/knowledge/publications/79722cb5/new-osha-regulations-for-construction-industry)); OSHA noise limit of 85 dBA as an 8-hour TWA ([OSHA](https://www.osha.gov/laws-regs/regulations/standardnumber/1910/1910.95AppG)).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Small trade contractors (electrical, HVAC, plumbing) | Not found | Owner decides; distributors and online |
| GCs and mid-size subs with equipment yards | Not found | Equipment or operations manager |
| Tool-heavy DIY and prosumers | Not found | Amazon (B2C) |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Labor shortage, poor jobsite visibility | Indirect; 45% report project delays | Overtime; subcontracting |
| Tool and equipment theft | ~$1B/yr (old c.2007 NER estimate, weakly sourced); avg equipment theft $30,000 (unverified, [Deep Sentinel](https://www.deepsentinel.com/?p=52807), vendor); 55% had tools stolen in the prior year ([DeWalt survey](https://wconline.com/articles/83790-dewalt-research-exposes-job-site-security-problem), vendor) | Gang boxes, ONE-KEY tags, camera services |
| Silica-dust compliance | OSHA estimate $659M/yr industry-wide; industry claimed up to $5B ([ABC](https://www.abc.org/News-Media/Newsline/report-finds-osha-underestimated-cost-of-silica-rule-by-45-billion-a-year)) | Table 1 controls, paper plans |
| Noise and heat exposure records | Not found | Paper records |
| Battery, charger and tool inventory chaos | Not found | Manual |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Milwaukee | ONE-KEY tags (Bluetooth only, phone-dependent) | 10-pack $189.99 at one retailer ([AirPinpoint](https://airpinpoint.com/blog/milwaukee-tool-tracker-one-key), competitor blog) | No GPS; brand-locked |
| Hilti | ON!Track asset management | Quote-based ([Capterra](https://www.capterra.ca/software/163550/on-track-asset-management)) | SaaS bundle |
| DeWalt | Tool Connect | Not found | Not found |
| Deep Sentinel-style services | Camera monitoring | Not found | Camera-based |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Silica Table 1 logger**: logs whether the shroud vacuum ran during cutting (a log, not an OSHA-grade measurement) | Contractors needing compliance records; $149 + report subscription | Hobbyist, $79 | Moderate | Optical PM sensor, airflow sensor, ESP32 | 4/3/4/4/3 = **18** |
| 2 | **Open jobsite theft tag**: LoRa/BLE tags with a solar gateway in the gang box, no cloud | $15/tag, no subscription or optional $5/mo alerts | $39 kit | Moderate | ESP32/Nordic, LoRa, MEMS motion sensor | 3/3/3/4/4 = **17** |
| 3 | **mmWave trailer/gang-box intrusion alarm**: no camera | $99/unit | Garages and vans, $79 | Easy-moderate | 24/60 GHz radar, LoRa | 3/3/2/5/4 = **17** |
| 4 | **Noise/heat exposure badge**: industrial-hygiene documentation, not medical | Price not specified | Not specified | Moderate | Mic, temp sensor, BLE | 3/3/3/4/3 = **16** |
| 5 | **Tool-crib shelf / battery board**: weight or RFID charge-state board | Price not specified | Not specified | Moderate | Load cells or RFID, ESP32 | 3/3/3/3/3 = **15** |

### NAICS 31-33: Manufacturing (small and mid-size shops)

#### Summary
Job shops sell parts to OEMs quote by quote. The owner or plant manager buys through industrial distributors and direct. Small shops run old machines at low utilization. Incumbent monitoring vendors are quote-priced SaaS aimed at bigger plants, which leaves room for a cheap retrofit sensor that keeps data local.

#### Key facts
**397,330 establishments, 12,784,104 employees, $2,930.1B value added** ([QCEW 31-33](https://data.bls.gov/cew/data/api/2024/a/industry/31_33.csv)). **74% of manufacturers have fewer than 20 employees** ([NAM](https://nam.org/?p=34181)). Job-shop spindle utilization is 30-45% (vendor, [JITbase](https://www.jitbase.com/blog/best-machine-monitoring-software-top-10)). Key rules: OSHA 85 dBA noise program; lockout/tagout and NFPA 70E (not sourced).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| CNC job shops, 5-50 staff | Not found | Owner or operations manager; direct and online |
| Fabrication, molding and assembly plants | Not found | Maintenance manager |
| Garage and hobby CNC/laser users | Not found | Online (B2C) |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| No visibility into spindle-on time on older machines | Utilization 30-45% (vendor) | Walk the floor; whiteboards |
| Unplanned downtime | ~$1,840 per 3-hour stop (vendor example, unverified, [Oxmaint](https://oxmaint.com/industries/manufacturing-plant/cnc-downtime-cost-calculator-guide-for-manufacturers)) | Reactive repair |
| Labor shortage and cost | Avg wage $35.19/hr ([IndustryWeek](https://www.industryweek.com/talent/article/55302062/june-jobs-report-manufacturing-loses-7000-jobs)) | Overtime |
| Input cost and supply volatility | 83.1% cite raw materials ([NAM Q2 2026](https://nam.org/wp-content/uploads/securepdfs/2026/06/NAM_2026_Q2_Outlook_Survey_Writeup.pdf)) | Not addressable by hardware |
| Noise, air quality, compressed-air waste | Not found | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Guidewheel | Clamp-on power sensors + SaaS | Formerly $15,000/yr for 10 machines; ~$32K/plant/yr (competitor-authored, unverified) ([PricingSaaS](https://pricingsaas.com/companies/guidewheel/diffs/2026W39)) | Cloud, per-plant pricing |
| MachineMetrics | Controller-data monitoring | Quote; ~$150-450/machine/mo (rival's claim) | Quote-only; aimed at larger shops |
| Scytec DataXchange | Monitoring software | $45/mo per machine (unverified) | SaaS |
| FourJaw (UK) | Retrofit monitoring | £36-90/machine/mo ([FourJaw](https://fourjaw.com/pricing)) | SaaS |
| Amper (now ECI) | Power-draw monitoring | Not found | Bundled into ERP |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Clamp-on machine monitor**: CT clamp with a shop-local dashboard | Job shops; $99/machine one-time + optional $5/mo | Hobby CNC/laser, $59 | Easy-moderate | CT clamp, ESP32 | 4/4/3/5/4 = **20** |
| 2 | **Andon/job beacon**: LoRa stack light with e-ink job badges | Shops; price not specified | Not specified | Easy | ESP32, LEDs, e-ink, LoRa | 3/3/3/5/4 = **18** |
| 3 | **Cycle-counter puck**: Hall/vibration part counter | Shops; price not specified | Not specified | Easy | Hall sensor, accelerometer | 3/3/4/5/3 = **18** |
| 4 | **Ultrasonic air/coolant leak detector** | $349 | $149 | Hard-ish (DSP) | MEMS ultrasonic mics, DSP | 3/3/2/3/5 = **16** |
| 5 | **Shop noise logger badge** | Price not specified | Not specified | Moderate | Mic, BLE | 3/3/3/4/3 = **16** |

### NAICS 42: Wholesale Trade

#### Summary
Wholesalers buy from manufacturers and resell, so their money sits in inventory. Inventory accuracy and forklift safety are real pains, but there is little sourced evidence and strong incumbents (WMS vendors, Zebra, RFID). It is the weakest of the B2B sectors for a solo hardware founder and is treated as under-researched.

#### Key facts
**637,241 establishments, 6,107,071 employees, $1,952.4B value added** ([QCEW 42](https://data.bls.gov/cew/data/api/2024/a/industry/42.csv)). The 2025 value added is up 11% on 2024, as published by the mirror and not checked against bea.gov. Merchant wholesale inventories were $901.1B (Feb 2024) ([TED Magazine](https://tedmag.com/monthly-wholesale-trade-report-march-2024/)). Key rules: OSHA 1910.178 for powered industrial trucks, the 7th most-cited standard in FY2018 ([OSHA](https://www.osha.gov/news/speeches/06112019)).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Independent distributors | Not found | Owner or operations |
| 3PL-style warehouse operations | Not found | Warehouse manager |
| Small online resellers, home inventory | Not found | Online (B2C) |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Inventory accuracy and mispicks | Not found | Scanners, WMS |
| Forklift/pedestrian incidents | ~85 deaths, 34,900 serious injuries/yr (older, unverified, [SafetyNow](https://ilt.safetynow.com/powered-industrial-trucks-forklifts-stats-and-facts/?print=pdf)) | Training, mirrors |
| Cold-chain and condition monitoring | Not researched | Not found |
| Labor cost | Not found | Not found |
| Tariff-driven cost volatility | Not found | Not addressable |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Zebra, Honeywell, Samsara | Scanners, RFID, telematics | Not found (names from researchers' background knowledge) | Not found |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Weight-sensing shelf**: load-cell bins for parts and hardware stock | Distributors and parts stores; price not specified | Maker version, $49 | Easy | Load cell, HX711, ESP32 | 3/3/3/5/4 = **18** |
| 2 | **Pick-to-light shelf strips**: local-network LED bin strips | ~$12/bin | Not specified | Moderate | ESP32, LED strips | 3/3/3/4/4 = **17** |
| 3 | **Open-protocol e-ink shelf labels** | Price not specified | Not specified | Moderate | e-ink, BLE/LoRa | 2/3/3/4/4 = **16** |
| 4 | **Trailer/dock door and temperature logger** | Price not specified | Not specified | Easy (many rivals) | Reed switch, temp sensor, LoRa | 2/3/2/5/3 = **15** |
| 5 | **Forklift pedestrian-proximity beacon**: awareness aid, not a safety device | Price not specified | None | Hard (safety-adjacent) | UWB/BLE, horn, light | 3/3/2/3/2 = **13** |

### NAICS 44-45: Retail Trade

#### Summary
Retailers buy wholesale and sell to consumers on thin margins, so shrink comes straight off profit. Independent owners buy security and IT through POS resellers, Amazon and local installers. Theft is well documented but crowded with cameras and EAS. The open space is cold-chain alarms for small grocery and convenience stores, plus camera-free sensing.

#### Key facts
**1,071,548 establishments, 15,529,520 employees, $1,810.4B value added** ([QCEW 44-45](https://data.bls.gov/cew/data/api/2024/a/industry/44_45.csv)). NRF 2026 reports shoplifting incidents **down 12.4%** in 2025, but organized retail crime is up at 40% of retailers. The sample is large chains ([NRF](https://nrf.com/media-center/press-releases/retailers-see-fraud-schemes-evolve-as-shoplifting-declines-nrf-study-finds)). Key rules: FDA Food Code 41°F cold holding drives temperature logs; PCI-DSS and state biometric laws are reasons to avoid payments, audio and cameras (researchers' background, not sourced).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Independent boutiques and specialty stores | Not found | Owner; Amazon/Shopify ecosystem |
| Small convenience, grocery and liquor chains | Not found | Owner or ops manager; POS reseller, refrigeration contractor |
| Multi-site small chains (pharmacy, phone, vape) | Not found | Loss-prevention lead; security installers |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Theft and organized-crime shrink police don't pursue | 68% of SMB retailers above 1.5% shrink (vendor-run survey, year unconfirmed, [Security Magazine](https://securitymagazine.com/articles/print/100263-54-of-smb-retailers-have-installed-security-cameras-in-the-past-year)) | Cameras (54% added), locked cases |
| Walk-in cooler failure spoilage | $18k-$47k per event (vendor, [GlacierGrid](https://www.glaciergrid.com/resources/research-and-impact/real-time-temperature-monitoring-restaurant-food-safety), [Envigilance](https://envigilance.com/temperature-monitoring/walk-in-cooler-monitoring/)) | Manual logs, cheap Bluetooth thermometers |
| Gift-card and phone scams | 42%/69% of retailers report increases (NRF) | Staff training; weakly addressable by hardware |
| Package theft | $12.8B-$15B/yr, estimates differ ~2x ([Omnisend](https://www.omnisend.com/latest-news/omnisend-study-porch-pirates-hit-nearly-1-in-3-u-s-homes-driving-12-8b-in-losses/); [SafeWise](https://www.safewise.com/research/porch-pirate-package-theft/)) | Doorbell cameras |
| Missing foot-traffic data | Not found as a documented pain | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| SensorPush | Sensor + G1 gateway | ~$50 / ~$100 (2018, outdated) | Bluetooth range in steel walk-ins (inference) |
| Govee | Wi-Fi/BT thermometers | ~$9-15 | Connection and alert failures reported ([Smart Home Explorer](https://www.smarthomeexplorer.com/reviews/temperature-&-humidity/sensorpush-g1-wifi-gateway)) |
| Kitchen Brains | ModulARM 75LC local walk-in alarm | Not found ([Restaurant Supply](https://www.restaurantsupply.com/products/kitchen-brains-75lc-we-flush-9-inch-modularm-temperature-alarm-for-walk-in-coolers-and-freezers)) | Not connected |
| Temp Stick | Wi-Fi sensor, no subscription | ~$139 (unverified) | Offline and text-alert anecdotes |
| Monnit, GlacierGrid, Envigilance | Sensors and monitoring services | Not found | Subscription service model |
| Verkada, Axon, Ring, Arlo | Cameras | Not found | Crowded; camera-based |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Walk-in Watch**: LoRa/Wi-Fi door and probe node with local buzzer, optional text | Grocery, c-store, restaurant owners; $149 + $5-10/mo alerts or one-time | Chest-freezer owners, $59-79 | Easy | ESP32-C6 or nRF, NTC/DS18B20 probe, reed switch, piezo, AA cells | 4/4/**2**/5/4 = **19** [adj from 20] |
| 2 | **Quiet Counter**: mmWave door/aisle counter, no camera | $79-129 + $5/mo dashboard | Home occupancy, $49 | Easy-moderate | LD2410/C4001 mmWave, ESP32 | 3/3/3/5/3 = **17** |
| 3 | **Back-Door Chime Pro**: staff-door-ajar and entry alert | C-stores, $59 | Door-ajar alert, $29 | Easy | Reed/IR sensor, relay | 3/3/3/5/2 = **16** |
| 4 | **Porch Plate**: weight/mmWave mat that alerts when a package lands or leaves | Small e-commerce sellers (weak) | $49-69 | Moderate (weatherproofing) | Pressure sensor or mmWave, hub | 3/2/3/4/3 = **15** |
| 5 | **Shelf Count Puck**: stock alert for high-theft items | Price not specified | Not specified | Moderate-hard | BLE, load cell | 2/2/3/3/3 = **13** |

[adj] Walk-in Watch: open space lowered from 3 to 2. Validation found local walk-in alarms (ModulARM) and subscription-free Temp Stick already on sale, so the "local buzzer, no subscription" gap is partly filled.

### NAICS 48-49: Transportation and Warehousing

#### Summary
Carriers earn per mile or per load on thin margins. Self-storage earns monthly rent per unit, and owners buy locks and gates through distributors. Cargo-theft losses jumped in 2025, but the ELD mandate makes trucking a certified-device category the founder should avoid. Self-storage is the most attractive sub-segment: it is fragmented, driven by security, and dominated by a closed, quote-only incumbent (Janus/Nokē).

#### Key facts
**353,975 establishments, 7,532,742 employees, $1,008.9B value added** ([QCEW 48-49](https://data.bls.gov/cew/data/api/2024/a/industry/48_49.csv)). 2025 cargo-theft losses were **~$725M (+60%)**, averaging $273,990 per theft ([Verisk CargoNet](https://www.verisk.com/company/newsroom/cargo-theft-losses-surge-to-estimated-$725-million-in-2025-verisk-cargonet-analysis-reveals/)). There are **50,000-58,000 self-storage facilities** ([Modern Storage Media almanac](https://digital.modernstoragemedia.com/almanac/self-storage-almanac-2025ok/section-1-industry-data)). Key rules: ELDs under 49 CFR 395 have no small-carrier exemption ([Overdrive](https://www.overdriveonline.com/fmcsa-denies-request-to-exempt-small-carriers-from-eld-rule/)); cellular devices need carrier certification, which pre-certified modules simplify (not sourced).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Independent self-storage owners | 50,000-58,000 facilities; five public REITs hold 37.6% of space ([SpareFoot](https://www.sparefoot.com/blog/self-storage-industry-statistics)) | Owner or manager; distributors (Janus/DoorKing resellers), trade shows |
| Owner-operators and small fleets | Not found | Owner; online, trucker forums, telematics reps |
| Couriers and small warehouses | Not found | Ops manager; Amazon, Grainger |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Cargo and trailer theft | $725M in 2025; $274k average | Hidden GPS ($14.99/mo), king-pin locks |
| Self-storage break-ins, shared gate codes | 57% of operators deal with repeat break-ins (survey year unstated, [Inside Self Storage](https://www.insideselfstorage.com/self-storage-industry-news/sherrifs-in-tyler-texas-investigate-self-storage-break-in-trend)); cost per incident not found | Smart locks, cameras, keypads |
| No alert when a unit door opens off-hours | Not found | Manual lock checks |
| Small-fleet telematics subscription cost | $25/vehicle/mo + $30 ELD ([Linxup](https://www.linxup.com/pricing)) | Cheaper trackers, phone apps |
| Dock temperature and door events | Not found | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Janus / Nokē | Smart locks, Smart Entry | Quote-only; one ~1,100-unit project ~$310K (~$280/unit, may include more) ([Janus](https://www.janusintl.com/hubfs/STORLOCAL-Securing%20Profits%20with%20Noke%CC%84%20Smart%20Entry%20System.pdf), vendor) | Closed, costly |
| PTI Security, OpenTech INSOMNIAC | Wired unit alarms; gateway for existing alarms | Not found | Wired retrofit cost |
| Generic door alarms | Per-door alarms | $50-250/door (StorageCafe estimate) | Batteries, false alarms |
| Linxup | Trackers, ELD | $25/vehicle/mo; asset tracker $14.99/mo | Subscription lock-in |
| Samsara, Motive | Telematics, ELD | Quote | ELD-centric |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Unit Door Sentinel**: magnet and accelerometer on each unit door reports opens and prying over LoRa to a site hub; no camera | Independent storage owners; $15-25/unit + $1/unit/mo, or per site | Tenants, $39-59 stand-alone alarm | Moderate (200+ nodes, OTA) | nRF/ESP32, SX126x LoRa, accelerometer, reed switch | 4/4/3/5/4 = **20** |
| 2 | **Gate Code Auditor**: passive Wiegand logger flagging code sharing and tailgating | $199/site + $10/mo | HOA/private gates, $79 | Moderate (many controllers) | Wiegand interface, ESP32 | 3/3/4/4/3 = **17** |
| 3 | **Trailer Whisper**: hidden LTE-M trailer tracker with BLE door sensor | Small fleets, $79 + $5-10/mo | RV/trailer owners, $59 + SIM | Moderate | nRF91/Quectel LTE-M, BLE | 4/3/2/4/3 = **16** |
| 4 | **Dock Door Pulse**: door-open and temperature logger | Small warehouses, vans; price not specified | Not specified | Easy | Reed switch, temp sensor | 2/3/3/4/3 = **15** [stated 13] |
| 5 | **Courier Drop Beacon**: BLE porch tag confirming drop time | Price not specified | Not specified | Easy (WTP unclear) | BLE tag | 2/2/3/4/3 = **14** [stated 12] |

### NAICS 51: Information

#### Summary
This is a large sector, but the slice that fits a solo hardware founder is small studios, podcasters and small server closets. Cheap alerting and studio status gear are the gaps.

#### Key facts
**300,282 establishments, 3,044,132 employees, $1,766.4B value added** ([QCEW 51](https://data.bls.gov/cew/data/api/2024/a/industry/51.csv)). Comfort cooling is not designed for constant IT loads, and closets often lack backup cooling ([Vertiv](https://www.vertiv.com/en-us/insights/articles/educational-articles/server-reliability-at-risk-how-comfort-cooling-compromises-uptime/), vendor). Key rules: Section 889 bars federal grant recipients from covered telecom gear ([eCFR 200.216](https://www.ecfr.gov/current/title-2/subtitle-A/chapter-II/part-200/subpart-C/section-200.216)). The FCC Covered List blocks new authorizations for foreign-made consumer routers (Mar 2026) and drones (Dec 2025); sources differ on exact dates ([Cooley](https://www.cooley.com/news/insight/2026/2026-03-26-fcc-moves-to-prevent-new-foreign-routers)). Broadcast rules: not found.

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Podcast and video studios, creators | Not found | Online, direct |
| Small broadcasters, church and community radio | Not found | Not found |
| SMB server rooms (often MSP-managed) | Not found | Through MSPs |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Unmonitored closet heat and water | US small-office downtime cost not found (only a UK £800-1,200/hr figure, unverified) | Cheap thermometers that don't alert on weekends ([Level1Techs](https://forum.level1techs.com/t/server-room-emergencies/199629)) |
| No automatic "recording live" signal | Not found | Manual switch by the door; users ask for OBS-linked lights ([OBS forum](https://obsproject.com/forum/threads/on-air-light.123290/)) |
| Studio room status signage | Not found | Paper signs |
| Small-broadcast tally and cue gear | Not researched | Not researched |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| APC | NetBotz temperature sensors | ~$102 wired / ~$118 wireless (undated, [CDW](https://www.cdw.com/product/apc-ap9335t-temperature-sensor/936119)) | Needs NetBotz appliance; IT-shop pricing |
| AVTECH | Room Alert | Room Alert 12S $779 ([Walmart](https://www.walmart.com/ip/Room-Alert-Power-Sensor/5150842757)); account $249.95/yr (2021) | Costly; SNMP/software |
| Vertiv | Geist Watchdog 15 | Not found | Not found |
| Temp Stick | Wi-Fi sensor | ~$149 (unverified) | Cloud-dependent |
| Orangemonkie, CBT Systems | On-air lights | Not found | Manual; not tied to record state |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Closet Sentinel**: temp/humidity/leak puck with local web UI, buzzer, battery backup, alerts via webhook or ntfy | MSPs and SMBs; $79 + optional $5/mo relay | Homelab, ~$59 | Easy | ESP32, temp/humidity sensor, leak probe, buzzer | 3/4/**2**/5/4 = **18** [adj from 19] |
| 2 | **OnAir Puck**: tally light that follows OBS, mic or DAW record state | Studio 3-pack | $59-89 | Easy | ESP32, USB, LEDs | 2/3/3/5/5 = **18** |
| 3 | **Studio door sign set**: e-ink/LED room status, local control | Price not specified | Not specified | Easy | e-ink, ESP32 | 2/3/3/5/4 = **17** |
| 4 | **Rack-door environment strip**: multi-point temp and airflow delta for 10-20U racks | Price not specified | Not specified | Moderate | Temp sensors, airflow sensor | 3/3/3/4/3 = **16** |
| 5 | **Podcast room noise-floor lamp**: shows HVAC rumble and noise level | Price not specified | Not specified | Moderate | Mic, ESP32, LED | 2/2/4/4/4 = **16** |

[adj] Closet Sentinel: open space lowered from 3 to 2. Validation found the $145-$500 band already crowded and found no evidence that buyers want local-first.

### NAICS 52: Finance and Insurance

#### Summary
Insurers already pay for leak and freeze prevention through free kits and premium discounts, which makes them a distribution channel more than an end user. Bank-branch security is regulated and incumbent-heavy. The open lane is the home-device side that insurers subsidize, and validation suggests even that is commoditized.

#### Key facts
**582,814 establishments, 6,327,482 employees, $2,687.6B value added** ([QCEW 52](https://data.bls.gov/cew/data/api/2024/a/industry/52.csv)). Water and freeze damage make up **~24-28% of homeowners claims at ~$14,000-15,400 each** (secondary sources; the primary III page was not retrieved) ([Policygenius](https://policygenius.com/homeowners-insurance/water-damage-statistics)). Key rules: insurer discounts are state-filed rating factors, and bank branch security falls under the Bank Protection Act (neither researched).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Homeowners insurers and MGAs (Hippo, Chubb, Travelers, USAA) | Not found | Loss-prevention or innovation teams; bulk kits or retail subsidies |
| Commercial/multifamily brokers and risk engineers | Not found | Recommend devices to insureds |
| Small banks and credit union branches | ~21,965 CU branches (June 2025, [CU Times](https://www.cutimes.com/amp/2025/10/27/bank-branches-are-still-shrinking-but-at-slower-pace/)) | Integrators, core-vendor channels; low fit |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Water and freeze claims | ~$14-15K average; ~1 in 60 insured homes/yr (secondary) | Free kits, discounts |
| Getting devices adopted and kept active | Hippo discounts avg $64/yr self-monitored, $91 pro-monitored (insurer self-reported) | Tie discount to device staying active |
| Frozen pipes in seasonal homes | Ice-dam claims ~$11,100 ([Guidewire](https://www.guidewire.com/de/resources/blog/industry-trends/7-top-winter-weather-risks-to-home-and-property.md)) | Thermostat alerts |
| Branch operations and security | Not researched | Not researched |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Hippo | Free smart-home kits (Kangaroo/SimpliSafe) | Free to policyholders | Data-sharing and cloud dependence (inference) |
| Chubb | WaterDefense; free Ting; StreamLabs discounts | 5-7% discount for flow shutoff (2016 release, [Chubb](https://news.na.chubb.com/2016-06-23-Chubb-Expands-Its-Water-Damage-Defense-Services-to-All-U-S-Homeowners-Insurance-Customers)) | Homeowner-focused |
| Travelers | Wyze/SmartThings sensors on Amazon | Not found | Same |
| Consumer leak sensors (Govee, YoLink, Flo) | Leak sensors and shutoffs | Govee $13-18; YoLink $15-30; Flo shutoff $429-559 (affiliate sites, [SmartHomeCompared](https://smarthomecompared.com/water-leak-sensors/goveelife-water-sensor-alarm-vs-yolink-water-leak-starter-kit)) | Commodity |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Proof-of-protection log**: device keeps signed local logs the owner can show an insurer, no cloud account | Insurers accept attestations | $60-90 | Moderate | Secure element, ESP32/nRF, sensors | 3/3/5/4/5 = **20** |
| 2 | **Insurer-grade freeze/leak node**: white-label sensor in the Vacancy Sentinel family | MGAs/insurers at wholesale | $40-80 | Easy | ESP32-C6/nRF, humidity/temp, probe pads | 4/**3**/**2**/5/4 = **18** [adj from 20] |
| 3 | **Seasonal-home freeze monitor** with cellular/LoRa gateway | Not specified | ~$100 + optional service | Moderate (carrier cert) | Pre-certified cellular module, temp | 4/3/3/3/3 = **16** |
| 4 | **Pipe-clamp temperature probe** | Not specified | Commodity pricing | Easy | Clamp probe, BLE | 3/3/2/5/3 = **16** |
| 5 | **Branch environment monitor** (closet, water) | Branches; price not specified | None | Moderate | ESP32, sensors | 2/3/3/4/2 = **14** |

[adj] Insurer-grade node: willingness to pay lowered from 4 to 3 and open space from 3 to 2. Validation found leak hardware at $13-$55 and insurers (Chubb, Hippo, Travelers) giving devices away, which depresses demand. The proof-of-protection log was not validated and keeps its score, but its demand is unproven.

### NAICS 53: Real Estate and Rental and Leasing

#### Summary
Money moves as rent and fees. Operating cost and vacancy are the profit levers, so owners buy devices that cut water loss, energy use and truck rolls. The researchers' strongest wedge was leak and freeze sensing in vacant units with a no-cloud angle for small landlords. Validation weakened it: hardware is cheap and landlord pain evidence was not found.

#### Key facts
**494,021 establishments, 2,441,949 employees, $4,234.1B value added** ([QCEW 53](https://data.bls.gov/cew/data/api/2024/a/industry/53.csv)). Value added is inflated by imputed owner-occupied rent. NMHC cites **21.4M apartments in 5+ unit buildings** (older release) ([NMHC](https://www.nmhc.org/advocacy/industry-weighs-in-on-hill-affordability-discussion)). Key rules: landlord entry usually needs 24 hours' notice, varying by state ([Nolo](https://www.nolo.com/legal-encyclopedia/free-books/renters-rights-book/chapter8-1.html)). Whether sensor data counts as "entry" is an open legal question, so designs should avoid audio, video and occupant identity.

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Multifamily owners and operators | Not found | Regional ops and maintenance directors; proptech vendors |
| Small landlords and single-family rental owners | Not found | Amazon and direct; prefer one-time purchase |
| Property management companies | Not found | Per-door platforms; want PMS integration |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Water leaks in vacant and occupied units | One building saved $300,000 on renewal (vendor anecdote); Chubb up to 8% building discount ([Habitat](https://www.habitatmag.com/Archive2/432-May-2025/Smart-Water-Leak-Detectors-Cut-Insurance-Costs-Boost-Financial-Gains)) | Weekly vacant-unit walk-throughs ([BiggerPockets](https://www.biggerpockets.com/posts/7317247)) |
| Vacant-unit HVAC and humidity waste | 4-7x energy cost (vendor, unverified, [Stratis](https://stratisiot.com/how-vacant-unit-control-in-the-summer-can-increase-your-noi/)) | Thermostat set points, staff checks |
| Turnover rekeying and lock batteries | Not found | Smart-lock codes; batteries every 4-6 months (vendor) |
| Truck rolls and unit-condition visibility | Not found | Periodic inspections |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Pro Sentry | Building leak detection | ~$75/sensor + ~$1/device/mo; ~$350 per 1-bed | Sold to buildings and insurers, not small landlords |
| Dwelo, PointCentral, Stratis IoT | Vacant-unit smart-home platforms | Not found | Platform lock-in, cloud |
| Govee, YoLink, Flo, Phyn | Consumer leak sensors and shutoffs | $13-$700 (see NAICS 52) | Commodity; no landlord fleet management |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Vacancy Sentinel**: battery leak, freeze and humidity puck, local-first | Property managers; per-door hardware + $1-2/mo dashboard | Small landlord or vacation home, $40-60 | Easy | ESP32-C6/nRF, humidity/temp, probe pads, coin/AA cells | 4/**3**/**2**/5/4 = **18** [adj from 20] |
| 2 | **Insurer-kit leak mesh**: local mesh with quiet e-ink hub matched to insurer requirements | Insurers/MGAs as discount kits | ~$100 kit | Moderate | ESP32, LoRa, e-ink | 4/**3**/**2**/4/4 = **17** [adj from 19] |
| 3 | **Offline BLE turnover lock-box** with logging | Price not specified | Not specified | Moderate (crowded) | nRF, lock mechanism | 3/4/2/4/3 = **16** |
| 4 | **Vacant-unit HVAC setback node** | Per door | Modest | Moderate | Thermostat contact or Zigbee | 3/3/2/4/3 = **15** |
| 5 | **Equipment-rental asset tracker** (LoRa tags) | Price not specified | Not specified | Moderate (pain not researched) | LoRa tags | 2/3/2/4/3 = **14** |

[adj] Ideas 1 and 2: willingness to pay lowered from 4 to 3 and open space from 3 to 2, for the same reasons as NAICS 52. The only landlord forum post found was by a vendor. One snippet suggested landlords think a loud local alarm is enough ([BiggerPockets](https://www.biggerpockets.com/forums/517/topics/1294309-water-leak-prevention-for-rental-properties)).

### NAICS 54: Professional, Scientific, and Technical Services

#### Summary
Small law, accounting, architecture and engineering offices share the same hybrid-office problems: half-empty space, meeting rooms booked but unused, and unmonitored IT closets. Each firm is too small for enterprise occupancy tools.

#### Key facts
**1,731,519 establishments, 10,901,640 employees, $2,465.2B value added** ([QCEW 54](https://data.bls.gov/cew/data/api/2024/a/industry/54.csv)). Office occupancy is at **55.1% of the pre-2020 baseline**, with a 64.4% Tuesday peak ([Kastle](https://www.kastle.com/safety-wellness/getting-america-back-to-work/)). Key rules: workplace-monitoring and biometric privacy laws were not searched.

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| 5-50 person professional firms | Not found | Office manager; online |
| Coworking and creative studios | Not found | Owner |
| MSPs reselling to those firms | Not found | Resale bundles |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Unused space and desks | Occupancy ~55% | Hot-desking |
| Ghost meeting-room bookings | 24.5-28.1% of bookings (sensor study, vendor, [Density](https://insights.density.io/hubfs/eBooks/Density-Bust%20Ghost%20Meetings.pdf)); 17% at Columbia libraries ([Columbia](https://library.tc.columbia.edu/blog/content/2024/february/inside-out-outside-in-operations-and-web-services-fall-2023-report.php)) | Teams panel check-in, which users report as flaky ([Microsoft Tech Community](https://techcommunity.microsoft.com/discussions/microsoftteams/teams-panels---check-in-issues/4252784)) |
| IT closet heat | See NAICS 51 | Cheap thermometers |
| Studio shoot-status and battery tracking | Not searched | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Joan | E-ink room signs | Joan 6 ~$549; Pro ~$710-905; €49/mo + €9.99/device (older) ([Capterra](https://www.capterra.com/p/180593/Joan/pricing/)) | Per-device licence |
| Robin | Room booking | From $99/mo (comparison pages) | Subscription |
| Density | Waffle sensor | $149 + per-sq-ft subscription (2023, [Business Wire](https://www.businesswire.com/news/home/20230510005712/en)) | Enterprise-oriented |
| Yealink | RoomSensor (PIR) | Not found | Pairs with own panels |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Room puck**: mmWave presence sensor with e-ink schedule that releases ghost bookings via Google/M365 | Small offices; $120-180/room + $3/room/mo | Home-office variant, $99 | Moderate | mmWave, e-ink, ESP32 | 4/4/3/4/4 = **19** |
| 2 | **Closet Sentinel** sold via MSPs (see NAICS 51) | $79 + optional $5/mo | ~$59 | Easy | As NAICS 51 | 3/4/**2**/5/4 = **18** [adj from 19] |
| 3 | **Desk-use counter**: under-desk mmWave/PIR logger, CSV export, no cloud | $40/desk one-time | None | Moderate | mmWave/PIR, ESP32 | 3/3/3/4/4 = **17** |
| 4 | **Privacy-first door headcount counter** with monthly email report | Price not specified | Not specified | Moderate | ToF/mmWave | 3/3/3/4/4 = **17** |
| 5 | **Shoot-live light + battery-rack monitor** for photographers | Price not specified | Not specified | Easy | ESP32, LEDs, current sensing | 2/2/4/5/4 = **17** |

The Teams thread supports demand for sensor-based release, but Microsoft said native support was "coming soon", so the gap may close. The score is unchanged.

### NAICS 55: Management of Companies and Enterprises

#### Summary
Corporate HQ and facilities buyers have the same hybrid-office problems as NAICS 54, with bigger budgets and much heavier security review. This was the least-researched sector. The researchers recommend selling through NAICS 54 channels and small facilities-management firms rather than targeting HQs directly.

#### Key facts
**100,043 establishments, 2,613,063 employees, $558.6B value added** ([QCEW 55](https://data.bls.gov/cew/data/api/2024/a/industry/55.csv)). Class A+ buildings peaked at **78.8% occupancy** in Dec 2025 ([Kastle](https://www.kastle.com/?p=11938)). Key rules: corporate procurement typically requires SOC 2 questionnaires and bans unmanaged Wi-Fi devices (researchers' inference; not sourced).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Corporate real estate and workplace teams | Not found | Enterprise procurement |
| Facilities managers at multi-site firms | Not found | Approved vendor lists |
| IT/security teams (device veto) | Not found | Security review |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Space underuse | Occupancy ~55% | Consolidation |
| Ghost bookings | See NAICS 54 | Panels |
| Multi-site closet monitoring | Not found (inferred) | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Density, Robin, Yealink, Joan, APC | As NAICS 54 and 51 | As listed there | Solo founder disadvantaged on security reviews |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Ambient room-availability wall display** | FM teams; price not specified | None | Easy | e-ink/LED, ESP32 | 2/3/3/5/4 = **17** |
| 2 | **Room puck** (as NAICS 54) | Per room | None | Moderate | As NAICS 54 | 3/3/2/4/4 = **16** |
| 3 | **Desk counter** (as NAICS 54) | Per desk | None | Moderate | As NAICS 54 | 3/3/2/4/4 = **16** |
| 4 | **Multi-site closet monitor** with simple dashboard | Price not specified | None | Moderate | As NAICS 51 | 3/4/**2**/4/3 = **16** [adj from 17] |
| 5 | **Offline floor-use "heat" display** | Price not specified | None | Moderate | mmWave, display | 2/2/3/4/4 = **15** |

[adj] Multi-site closet monitor: open space lowered from 3 to 2 on the same crowded-market evidence as Closet Sentinel.

### NAICS 56: Administrative and Support and Waste Management

#### Summary
These are large, fragmented service businesses with field crews (guards, janitorial, landscaping, pest control, waste hauling) that sell labor-hours or recurring routes. Proof that service happened is a paid software category, but it relies on phones. The best hardware gaps are cheap verification tags and bait-station or dumpster sensors, where incumbents quote prices only on request.

#### Key facts
**694,633 establishments, 9,213,984 employees, $919.9B value added** ([QCEW 56](https://data.bls.gov/cew/data/api/2024/a/industry/56.csv)). Structural pest control had **$13.4B revenue in 2025 across 16,565 firms**, 81.4% with one or two locations ([NPMA](https://www.npmapestworld.org/your-business/latest-news/us-pest-control-industry-sustains-steady-growth-with-6-increase-in-2025/)). Key rules (researchers' background, not sourced): state guard licensing; FIFRA and state tamper-resistance rules for bait stations; state notice laws for GPS tracking of employees (CT, NY, DE).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Landscaping and lawn firms | ~690,000-730,000 businesses (secondary, conflicting) ([NALP](https://www.landscapeprofessionals.org/LP/Media/landscape-industry-statistics.aspx)) | Owner; trade shows, software resellers |
| Pest control firms | 16,565 | Owner; PestWorld, pest supply distributors |
| Security guard companies | ~9,500 establishments (First Research, year unstated) | Owner; software vendors |
| Janitorial firms, waste haulers | Not found | Not found |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Proving service happened ("you didn't mow") | Lost payment per dispute; dollar figure not found | GPS trackers ($25/vehicle/mo), crew photos, route sheets ([LawnSite](https://www.lawnsite.com/threads/customer-claims-i-didnt-cut-his-grass-and-will-not-pay.503826/)) |
| Guard patrol verification and tag spoofing | Not found | NFC/QR tags + app; tags can be copied ([Miratag](https://miratag.com/en/blog/best-guard-tour-system-comparison)) |
| Manual bait-station route checks | Not found | Manual inspection |
| Overflowing or underfilled dumpsters | Extra pickup **$149-$198** each ([LA County](https://pw.lacounty.gov/epd/swims/docs/ECF/WM%20-%20Extra%20Service%20Fees%20%28Santa%20Clarita%20Valley%29%202025-2026.pdf); [ECUA](https://assets.ecua.fl.gov/images/ECUA-Sanitation-Commercial-Roll-Off-Compactor-Rates.pdf)) | Compology/Enevo; route checks |
| Restroom consumables | Not found | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| PatrolTech | Guard tour app | $29/mo for 10 checkpoints + $2 each extra ([Slashdot](https://slashdot.org/software/p/PatrolTech/)) | Phone-centric; copyable tags |
| Silvertrac | Guard management | ~$249/mo for 10 devices ([Capterra](https://capterra.com/p/135436/Silvertrac-Software/)); setup fees $842-1,404 (competitor claim) | Cost, minimums |
| Guard1 | Guard tour hardware | ~$995-1,385 packages (aggregator) | Quote-based |
| Linxup, GPS Insight | Vehicle GPS | $25/vehicle/mo | No site-level proof |
| Jobber, Aspire, LMN | Field-service software | Not found | Phone check-ins |
| Compology, Enevo | Dumpster fill sensors | Quote-only, per container per month | Small haulers priced out (inference) |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Crew Beacon Tag**: tamper-evident BLE + NFC fob per client site that logs a signed, non-clonable visit token | Landscape, janitorial, guard firms; $12-20/tag + $29/mo for 25 sites | Homeowners log cleaner/lawn visits, $25 | Easy | nRF52, NFC-A coil, secure element | **4**/**3**/3/5/4 = **19** [adj components; total unchanged] |
| 2 | **Dumpster Level Puck**: ToF/ultrasonic fill sensor on LTE-M | Small haulers, property managers; $89 + $4/mo | HOA/farm bins | Moderate-hard | nRF9160 or pre-cert LTE-M, ToF/ultrasonic | 3/4/3/3/3 = **16** [stated 17] |
| 3 | **Bait Station Check Tag**: reports lid opens and station status over BLE | Pest firms, $15-25/station | Gardeners, $29 | Moderate (tamper-resistance rules) | Reed/Hall sensor, BLE | 3/3/4/3/3 = **16** |
| 4 | **Round Keeper guard hub**: pocket key with haptic prompts, offline tour log | Price not specified | None | Moderate (competes with free apps) | nRF, haptics | 3/3/2/4/3 = **15** |
| 5 | **Restroom refill counter** | Price not specified | None | Moderate | Level sensor, BLE | 2/3/3/3/2 = **13** [stated 11] |

[adj] Crew Beacon Tag: pain raised from 3 to 4 because LawnSite has repeated threads on non-payment disputes. Willingness to pay lowered from 4 to 3 because operators already settle disputes with free phone photos and existing GPS. The total stays at 19.

### NAICS 61: Educational Services

#### Summary
Schools buy sensors for safety and facilities through district procurement, often with grants or settlement money. Vape detection is the proven category. False alarms, recurring licences and student privacy are the documented weaknesses of incumbents.

#### Key facts
**242,679 establishments, 13,195,807 employees, $353.2B value added** ([QCEW 61](https://data.bls.gov/cew/data/api/2024/a/industry/61.csv)). QCEW includes public schools; the private-only CBP count is 118,004. There are **13,318 regular districts** and 91,390 traditional public schools ([EdWeek](https://www.edweek.org/ew/issues/education-statistics/index.html)). Key rules: the amended COPPA rule took effect June 23, 2025, with compliance due April 22, 2026, and biometrics now count as personal information ([Clym](https://www.clym.io/blog/childrens-online-privacy-looks-different-this-school-year-even-without-coppa-20), secondary); FERPA. Design implication: no audio and no student identifiers.

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| K-12 districts | 13,318 | Facilities, IT or safety director; board approval; pilots in a few schools |
| Colleges and universities | ~3,931 Title IV degree-granting (uncertain reading, [NCES](https://nces.ed.gov/programs/digest/d22/tables/dt22_105.50.asp)) | Residence life, facilities |
| Makerspaces, trade schools, tutoring | Not found | Direct |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Vaping in restrooms | Median **$925/detector**, median contract $14,204 across 284 districts (vendor-analysis, [CivicIQ](https://civiciq.com/blog/school-vape-detector-contracts)) | HALO, Zeptive, Soter, Triton |
| False alarms and privacy | "Hundreds, sometimes thousands" of alerts a day in Montgomery County ([FOX 5 DC](https://www.fox5dc.com/news/high-school-vape-sensors-trigger-thousands-false-alarms-mcps-schools)); student searched after deodorant set off an alert ([NPR](https://www.npr.org/2024/09/12/nx-s1-5090006/vape-detectors-schools-ecigarettes-juul)) | Calibration; staff checks |
| Subscriptions and lock-in | Software in 204 of 284 awards; renewals ~$39-150/unit/yr | Multi-year renewals |
| Air quality and CO2 | Not researched | Not researched |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Motorola HALO | Vape/aggression sensor | $964-$3,050/unit + licence | False alarms, subscription |
| Triton | Vape sensor | ~$750-999 incl. 1 yr, then ~$110-150/yr ([Triton](https://www.tritonsensors.com/blog/3d-sense/how-much-do-vape-detectors-cost), vendor) | Subscription |
| Zeptive | Vape sensor | ~$1,100; in 195 awards | Not found |
| Soter | Vape sensor | >$12,000 + $1,500/yr per school ([WKBW](https://www.wkbw.com/news/eye-on-education/maryvale-high-school-to-install-sensors-detecting-vaping-at-school)) | Cost |
| Vape Guardian | Vape sensor | Not found | Claims false-alert fix (press release) |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Quiet-Room aerosol sensor**: PM/VOC sensing, no mic, no cloud, local alert; flat price | Districts; $300-500/unit one-time, no mandatory licence | Parents and apartment owners, $80-120 | Moderate | ESP32, Sensirion-class PM, VOC, optional mmWave | 4/4/3/4/4 = **19** |
| 2 | **Classroom CO2 and noise display**: design-led desk object | Bulk to schools | $60-90 | Easy | CO2 sensor, mic, display | 3/3/2/5/5 = **18** |
| 3 | **Makerspace tool-use and air-filter monitor** | Price not specified | Not specified | Easy-moderate | CT clamp, PM sensor | 2/3/4/5/4 = **18** |
| 4 | **Restroom occupancy counter** (mmWave, no image) | Price not specified | None | Moderate | mmWave | 3/3/3/4/4 = **17** |
| 5 | **Bell/PA hardware** | Price not specified | None | Moderate (crowded) | Audio amp, network | 2/3/2/3/2 = **12** |

Validation strengthens the pain and willingness-to-pay case for idea 1: settlement money is one-time, which suits a flat price. It also warns that false alarms are a sensing-quality problem, so a no-mic device must still out-discriminate HALO. No evidence was found that districts value no-cloud. The score is unchanged.

### NAICS 62: Health Care and Social Assistance (non-medical slice only)

#### Summary
Only childcare, social assistance and senior-living facility operations were screened; medical products are excluded. Childcare centers have very thin margins and buy cheap operational tools. Senior-living operators have compliance-driven water-temperature logging needs, which are larger budgets but close to regulation.

#### Key facts
**2,039,908 establishments, 24,311,493 employees, $2,327.2B value added** for the whole sector, mostly medical ([QCEW 62](https://data.bls.gov/cew/data/api/2024/a/industry/62.csv)). Child day care (NAICS 6244) has **79,708 establishments** (QCEW 2024; CBP 2023: 82,162) ([QCEW 6244](https://data.bls.gov/cew/data/api/2024/a/industry/6244.csv)). Child Care Aware counts 92,613 licensed centers and 98,807 family child-care homes ([FFYF](https://www.ffyf.org/resources/2025/05/new-resource-reveals-notable-changes-in-price-and-supply-of-child-care)). Key rules: CMS requires water-management programs (ASHRAE 188) for certified facilities ([Envigilance](https://envigilance.com/compliance/legionella-compliance/), vendor). Infant ratios are 3-6 per staff member ([Niskanen](https://www.niskanencenter.org/states-have-room-to-experiment-with-childcare-staffing-ratios/)). Anything resembling child supervision or life safety is excluded.

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Child care centers | ~79,700-92,600 | Director or owner; Amazon, supply catalogs |
| Family child care homes | ~98,800 | Consumer-like |
| Senior living operators | Not found (~621,000 assisted living units occupied, [Senior Housing News](https://seniorhousingnews.com/?p=49426)) | Maintenance directors; corporate vendor lists |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Rising costs, thin margins | 65% of centers raised tuition ([FFYF](https://www.ffyf.org/2026/04/16/new-survey-emphasizes-how-child-care-affordability-challenges-destabilize-both-providers-and-families/)); wages 56-68% of costs | Tuition increases |
| Staffing and ratio compliance | Not found | Manual headcounts |
| Senior-living water-temperature logging | Monitoring services "from $750/mo" (vendor) | Manual readings |
| Senior-living energy and HVAC | Not found | Not found |
| Classroom air quality | Not found | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Envigilance | Water-monitoring service | From $750/mo (vendor) | Expensive for small operators |
| Watts | Recirculation control | Not found | Not found |
| JUMO | Wireless temperature loops | Not found | Not found |
| Brightwheel, Procare | Childcare software | Not found | Software, not hardware |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Daycare room CO2/humidity/noise display**: friendly design-led object | Centers, $80-120 | Parents and home daycares, $60 | Easy | CO2, humidity, mic, display | 3/3/3/5/5 = **19** |
| 2 | **Pipe-temperature logger tag**: clamp-on probe logging loop temperatures over LoRa, with a printable log (non-safety) | Senior living, $60-120/node + optional $5-10/mo | Homeowners with recirculation, $50 | Moderate | Clamp probe, LoRa | 3/4/4/4/3 = **18** |
| 3 | **Quiet-hours noise lamp** for classrooms | Price not specified | Yes | Easy | Mic, RGB LED | 2/2/4/5/5 = **18** |
| 4 | **Kitchen fridge/freezer logger** | Price not specified | Not specified | Easy (crowded) | Temp probe | 3/4/2/5/3 = **17** |
| 5 | **Door-ajar chime** (convenience only, not life safety) | Price not specified | Not specified | Easy | Reed switch | 3/3/3/5/3 = **17** |

### NAICS 71: Arts, Entertainment, and Recreation

#### Summary
This is a membership- and ticket-driven sector. Fitness is the best-documented part and is growing; climbing gyms have flat revenue and fewer openings. Operators are small and short-staffed, and unstaffed 24/7 access is a big theme. Access control is crowded and cloud-based, so the gaps are niche, local-first hardware.

#### Key facts
**191,265 establishments, 2,952,445 employees, $321.3B value added** ([QCEW 71](https://data.bls.gov/cew/data/api/2024/a/industry/71.csv)). **81M Americans held gym memberships in 2025** ([Athletic Business](https://www.athleticbusiness.com/facilities/fitness/article/15821794/hfa-report-reveals-81m-americans-were-fitness-club-members-in-2025)). There are 574 US climbing gyms (IBISWorld estimate), and 73% of operators report a worsening economy ([Athletic Business/CBJ](https://www.athleticbusiness.com/operations/budgeting/article/15817979/study-climbing-gym-numbers-slip-in-2025-revenues-flat)). Key rules: ADA, state health-club contract laws and venue noise ordinances (not found).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Gym and studio owners | Not found | Through management-software ecosystems (Mindbody, Gymdesk) with access partners ([Athletech](https://athletechnews.com/brivo-mindbody-bring-mobile-entry-tech-to-gyms-and-studios)) |
| Climbing gym operators | 574 | Owner; trade body CBJ |
| Venues, marinas, bowling, golf, museums | Not found | Not found |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Staffing limits on hours; unstaffed access tied to payment | Not found (vendor claims only) | Kisi/Brivo access control |
| Climbing gym economic pressure | 73% report worsening conditions | Cost cutting |
| Lost keys and rekeying | $1,500 for 10 doors (vendor hypothetical) | Rekey |
| Unstaffed-hours security | Not found | Cameras |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Kisi, Brivo | Cloud access control | Not found | Cloud-based; crowded |
| Gymdesk, GymMaster, Rezerv/igloohome | Software + door integration | Not found | No same-day lockout after failed payment (Gymdesk) |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Climbing comp timer/leaderboard display** | Gyms, $199-399 one-time | Home-wall users, $79 | Moderate | ESP32, HUB75 LED or e-ink, BLE | 3/3/4/5/5 = **20** |
| 2 | **Hangboard force logger**: load-cell plate, local display, no app account | Gyms, $149 | Climbers, $99 | Moderate | HX711, load cell, nRF, e-ink | 2/4/4/4/5 = **19** |
| 3 | **Venue SPL logger/sign**: sound-level display and log as ordinance proof | Venues, $199 + log export | Practice rooms and bands, $99 | Easy | ESP32, calibrated MEMS mic | 3/3/4/5/4 = **19** |
| 4 | **Offline NFC member door reader**: validates a signed list locally | Small gyms, $120 + $5/mo sync | None | Moderate | ESP32, PN532 NFC, relay | 4/4/2/4/3 = **17** |
| 5 | **Weight-room occupancy strip**: mmWave count shown on lobby display | Gyms, $149 | None | Moderate | LD2450 mmWave, ESP32 | 3/3/3/4/4 = **17** |

### NAICS 72: Accommodation and Food Services

#### Summary
Restaurants run on thin margins and heavy compliance paperwork. Short-term rentals are a host-run market where Airbnb's 2024 indoor-camera ban created a legitimate niche for privacy-safe sensors. Restaurant operators buy through dealers and online; STR hosts buy on Amazon, direct and through PMS integrations.

#### Key facts
**793,370 establishments, 14,206,569 employees, $965.3B value added** ([QCEW 72](https://data.bls.gov/cew/data/api/2024/a/industry/72.csv)). **42% of restaurant operators were unprofitable in 2025** ([NRA](https://restaurant.org/research-and-media/media/press-releases/persistent-cost-increases-and-enduring-demand-will-shape-the-restaurant-industry-in-2026/)). There are ~2.46M STR listings and 785K hosts (2023, secondary, [Airbtics](https://airbtics.com/short-term-rental-market-report-2025-the-united-states)). Key rules: FDA Food Code requires cold food at 41°F or below and hot at 135°F or above ([Xenia](https://www.xenia.team/food-safety/food-holding-temperature), secondary). Airbnb allows decibel-only noise monitors in common areas, disclosed in the listing, with no sound recording ([Hostfully](https://www.hostfully.com/blog/airbnb-noise-monitor/)).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| STR hosts and small property managers | ~785K hosts (2023) | Amazon, direct, PMS integrations; Airbnb subsidizes Minut ([Airbnb](https://news.airbnb.com/airbnb-and-minut-collaborate-on-noise-prevention-support-for-hosts/)) |
| Independent restaurants | Not found (independents fell 2.3% in 2025, [NRN](https://www.nrn.com/restaurant-insights/restaurant-industry-faces-modest-growth-amid-cost-pressures-in-2026)) | Owner; dealers and online |
| Chains and multi-unit operators | 263,000+ chain locations | Corporate procurement (ComplianceMate, Monnit) |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Walk-in refrigeration failure | $6,550-$40,000 per incident (vendor, [GlacierGrid](https://www.glaciergrid.com/resources/use-cases/glaciergrid-skyline-case-study)) | Manual 4-hour logs, paid sensors |
| Thin margins | 42% unprofitable | Any product must pay back fast |
| STR parties and noise | ~$1,200 per party (Minut-linked, marketing); one host went from 4-5 neighbor complaints a year to zero with alerts ([STR Specialist](https://strspecialist.com/community/thread/noise-monitoring-airbnb-minut-vs-noiseaware-alternatives)) | Noise sensor + subscription |
| Temperature-log paperwork | Not found | Paper logs |
| Subscription cost of monitors | Minut price creep and billing disputes ([Trustpilot](https://www.trustpilot.com/review/minut.com?page=2)) | Tolerate or cancel |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Minut (owns NoiseAware, unverified) | Noise/occupancy sensor | $150 + $10/mo/device | Billing complaints; device useless without plan |
| NoiseAware | Noise sensor | $199 + $9/mo | Plug-in only, bulky |
| Alertify | Noise/smoke/vape sensor | $150 + $6/mo | Less polished app |
| Party Squasher, Roomonitor | Device counting; monitoring | Not found | No sound sensing; Europe-focused |
| Monnit | Food-service sensors | From $49, free basic monitoring ([Monnit](https://www.monnit.com/applications/commercial/food_services)) | Cheap competitor |
| ComplianceMate | Food-safety sensors | $650 for 2 sensors incl. 1 yr (listing inconsistent) | Cost |
| SensoScientific | Temperature monitoring | Quote | Quote-only |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Local-only STR noise + occupancy puck**: decibel-only, no audio stored, local hub, one-time price, Airbnb-compliant | Small PMs; $79-129/unit + optional $2/mo SMS relay | Hosts, $99-149 one-time | Easy-moderate | ESP32-S3, MEMS mic (on-chip dB), LD2410 mmWave, optional CO2/vape | 4/4/**2**/5/5 = **20** [adj from 21] |
| 2 | **Bar/cafe sound-level sign**: public dB display to stay under ordinance | Bars and cafes, $129 | Home studio, $79 | Easy | ESP32, I2S mic, LED matrix | 3/3/4/5/5 = **20** |
| 3 | **STR quiet-hours nudge lamp**: glows amber or red over a dB threshold, no alerts | Hosts, $89 | Apartment dwellers, $59 | Easy | ESP32, mic, RGB LED | 3/3/4/5/5 = **20** |
| 4 | **Walk-in door-ajar + temperature tag** with local siren/display | Independent restaurants; hardware + $5/mo SMS | Chest freezer owners, $35 | Easy | nRF52/ESP32, NTC probe, reed switch, e-ink | 4/3/2/5/4 = **18** |
| 5 | **Health-code temp-log display**: e-ink logger that exports the daily 41°F/135°F log | $149 + free export | None | Moderate | nRF, probe, e-ink, USB | 3/3/3/4/4 = **17** |

[adj] STR puck: open space lowered from 3 to 2. Minut reportedly owns NoiseAware and Airbnb gives hosts a free Minut sensor, and Minut already markets no audio recording, so privacy alone does not differentiate. The one-time price and the absence of cloud lock-in do. The validation note found no evidence that buyers want headcount.

### NAICS 81: Other Services (except Public Administration)

#### Summary
These are fragmented, owner-operated businesses (auto repair, laundromats, salons, car washes, churches, pet care) paid per transaction or appointment. Laundromat and car-wash electronics are locked into OEM ecosystems. Retrofit add-ons that read machine status may be open.

#### Key facts
**886,613 establishments, 4,705,257 employees, $629.7B value added** ([QCEW 81](https://data.bls.gov/cew/data/api/2024/a/industry/81.csv)). Auto repair shop counts conflict (~166K-284K) ([Orbital](https://www.withorbital.com/data/automotive-repair-industry-statistics/)). There are about **10,890 laundromat and drycleaner establishments** (CBP 2023 via [Vanta](https://vantainsights.com/industry/812310-coin-operated-laundries-drycleaners), approximate). The pet "other services" segment is worth $14.3B ([APPA](https://www.accessnewswire.com/newsroom/en/business-and-professional-services/u.s.-pet-industry-reaches-158-billion-in-2025-poised-for-continu-1165595)). Key rules: PCI, state licensing and EPA refrigerant and wash-water rules (not found).

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Laundromat owners | ~10,900 | Distributors tied to equipment makers ([Automatic Industries](https://automaticindustries.com/blog/2026/06/17/how-laundry-card-systems-and-apps-reduce-theft-vandalism/)) |
| Independent auto shops | ~166K-284K (conflicting) | Parts and tool distributors, PartsTech-style platforms |
| Pet groomers/boarding, salons, churches | Not found | Not found |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Technician shortage in auto repair | 31% call it their biggest challenge ([S&P/PartsTech](https://aftermarketinsight.spglobal.com/news/4400/partstech-report-reveals-skilled-technician-shortage-in-us-auto-industry)) | Not hardware-addressable |
| Laundromat utilities and equipment replacement | Cited by 55% and 53% ([PlanetLaundry](https://digitaleditions.walsworth.com/article/Crunching+The+Numbers/4717095/814266/article.html)) | Card systems |
| Laundromat theft and vandalism | Not found (vendor claims) | Card readers, cameras |
| Car-wash equipment downtime | Not found | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Coinamatic, Automatic Industries | Laundry card systems | Not found | OEM ecosystem |
| PartsTech, Fullbay | Shop software | Not found | Software only |
| Salon, pet and church hardware players | Not found | Not found | Not found |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Clamp-on washer/dryer cycle sensor**: retrofits any machine; status for owner and customers | Laundromats, $25-40/machine + $1/mo | "Laundry done" puck, $39 | Easy | ESP32-C3/nRF, accelerometer, CT clamp | 3/4/3/5/4 = **19** |
| 2 | **Church/venue sound-level and HVAC nudge panel** | $149 | Home studios, $79 | Easy | ESP32, mic, e-ink | 2/3/4/5/4 = **18** |
| 3 | **Kennel noise/temperature tag**: local alerts, no cameras | Boarding facilities, $79/unit | Pet crate/car, $49 | Easy | nRF/ESP32, temp sensor, mic | 3/3/3/5/4 = **18** |
| 4 | **Shop-bay air/tool-use monitor**: tallies bay utilization | Auto shops, $99 + dashboard | Garage hobbyists, $49 | Moderate | ESP32, CT, pressure sensor | 3/3/4/4/3 = **17** |
| 5 | **Salon/barber e-ink door sign**: tap-to-update "back in 10" | $79 | Home businesses, $59 | Easy | ESP32, e-ink | 2/2/3/5/4 = **16** |

### NAICS 92: Public Administration

#### Summary
Local governments are numerous and spend documented money on visitor counters for parks and libraries. Procurement is slow and bid-based. Federal grant rules (Section 889) favor trusted suppliers with compliant supply chains. Current counters cost $150 to $6,000 per unit.

#### Key facts
**139,927 establishments, 7,846,751 employees; BEA value added $3,428.6B covers all government**, not just NAICS 92 ([QCEW 92](https://data.bls.gov/cew/data/api/2024/a/industry/92.csv)). There were **91,438 local governments in 2025**, 57.7% of them school or special districts ([Census](https://cdn.www.census.gov/content/dam/Census/library/publications/2025/econ/govtorg2225.pdf)). Key rules: 2 CFR 200.216 / Section 889 bans covered telecom and surveillance gear for grant recipients, with no waivers ([Taft](https://www.taftlaw.com/news-events/law-bulletins/impact-of-section-889s-telecommunications-and-video-surveillance-equipment-prohibitions-on-federal-grant-and-loan-recipients/)). Check every module vendor's status before bidding. Procurement thresholds, cooperative contracts and Buy American rules were not found.

#### Buyers
| Segment | Count | How they buy |
|---|---|---|
| Public libraries | Not found | Library director or IT; often via consortium (e.g. Minitex cooperative pricing, [Minitex](https://minitex.umn.edu/news/library-products-cooperative-purchasing/2024-02/special-price-sentry-stand-alone-wireless-usb)) |
| Parks, recreation and trails | Not found | Regional agencies share accounts; bids |
| Public works and small municipalities | Within 91,438 local governments | Council-approved bids above local thresholds |

#### Pain points
| Pain | Cost | Current workaround |
|---|---|---|
| Trail and park visitor counting | $4,000-6,000/unit + $35/mo data + $125 battery every 2 years ([MORPC](https://morpc.org/wordpress/wp-content/uploads/2021/08/08-19-21-COG-Trail-Development-WG-Meeting-Packet.pdf); [Lake County bid](https://c.lakecountyfl.gov/ProcurementDocuments/23-752_23-752BidTabulation.pdf)) | Eco-Counter; shared units |
| Library door-count cost and accuracy | $150-800/unit; $550 called "steep" ([LIBRARYDIR](https://lists.ctc.edu/pipermail/librarydir_lists.ctc.edu/2023-February/009446.html)) | SenSource, Axis, Geovision |
| Public-works remote monitoring | Not found (inferred) | Not found |
| Meeting-room usage | Not found | Not found |

#### Existing players
| Company | Product | Price | Gap |
|---|---|---|---|
| Eco-Counter | Urban Post MULTI | $5,450 (2021 quote) + $35/mo | Price |
| SenSource | Library door counter | $149.95 wired | Wired |
| Axis, Geovision | Camera-based counters | ~$500-800 (2023 list-serv) | Camera-based |
| Chambers Electronics | Park counters | Not found | Not found |

#### Ideas
| # | Idea and pitch | B2B version | B2C version | Build | Main parts | Score P/W/O/B/F |
|---|---|---|---|---|---|---|
| 1 | **Trail/park counter**: solar, local logging, PIR/mmWave, no mic, SD export, design-led | Parks and trail agencies, $400-700 | Trail clubs, HOAs | Moderate | PIR/mmWave, solar, SD, optional LoRa | 4/4/4/3/4 = **19** |
| 2 | **Library door counter**: battery, USB report | Libraries, $150-250 | None | Easy | ToF/PIR, nRF, USB | 3/4/3/5/3 = **18** |
| 3 | **Meeting-room sign with auto-release** for city halls and libraries | Price not specified | None | Moderate | mmWave, e-ink | 3/3/3/4/4 = **17** |
| 4 | **Live capacity sign** for parks and pools, fed by counter | Price not specified | None | Moderate | Display, LoRa | 2/3/4/4/4 = **17** |
| 5 | **Public-works LoRa level/temperature sensor** (non-safety use) | Price not specified | None | Moderate | LoRa, level/temp sensors | 3/3/4/3/3 = **16** |

## Eighteen ideas clear 19 points, but five carry real-user evidence

Ranking every idea by adjusted score gives a crowded top. **Eighteen ideas score 19 or more**, and they cluster into three product families: radio sensor nodes with a local hub, sound-level devices, and design-led display objects. The scores mostly reflect how buildable and on-brand an idea is, since buildability and fit are the easiest criteria to score high without market evidence. The evidence column is the real filter.

| Rank | Idea (sector) | Score | Evidence status |
|---|---|---|---|
| 1 | Stocktank LoRa (11) | 21 | **Unproven demand.** Price gap documented: incumbents charge $400-550 + $99-420/yr ([Gallagher](https://shop.am.gallagher.com/us/en_US/animal-management/water-management/tank-level-monitor/p/G95020), [Tank Toad](https://thesolarstore.com/products/satellite-tank-toad-solar-powered-satellite-tank-monitor)). No rancher voice found. Assumes a house within LoRa range. |
| 2 | Unit Door Sentinel (48-49) | 20 | **Real-user evidence.** Self-Storage Talk operators run unit alarms that catch intruders, and complain about battery upkeep and false alarms ([SST](https://www.selfstoragetalk.com/forum/general-self-storage-forums/technology-software-and-security/208237-individual-unit-alarms), snippet only). WTP for retrofit at $50+/door unproven. |
| 3 | STR noise + occupancy puck (72) | 20 [adj] | **Real-user evidence** on price model: Trustpilot billing complaints and a 6-property host saying fees add up. Competition entrenched (Minut + Airbnb). |
| 4 | Clamp-on machine monitor (31-33) | 20 | **Partial.** Incumbent pricing is high (vendor-authored). A Practical Machinist snippet reports $25K controller unlock fees and warnings against putting old machines online, which supports local-first ([PM](https://www.practicalmachinist.com/forum/threads/is-connecting-machines-to-the-network-worth-it.449903/)). Guidewheel already does clamp-on. |
| 5 | Fence Watch (11) | 20 | Not validated |
| 6 | Proof-of-protection log (52) | 20 | Not validated; insurer acceptance unknown |
| 7 | Climbing comp timer (71); bar/cafe sound sign (72); STR quiet lamp (72) | 20 | Not validated; sign demand is the researchers' idea with no ordinance evidence |
| 8 | Crew Beacon Tag (56) | 19 [adj components] | **Strongest real-user evidence.** Repeated LawnSite threads on non-payment and crew verification ([1](https://www.lawnsite.com/threads/customer-claims-their-lawn-hasnt-been-mowed.459192/), [2](https://www.lawnsite.com/threads/how-do-you-verify-that-employee-cut-the-customers-lawn.512717/)). Must beat free phone photos. |
| 9 | Quiet-Room aerosol sensor (61) | 19 | **Strong evidence** from news and procurement: false-alarm floods, $925 median unit, one-time settlement funding. No evidence that no-cloud matters to buyers. |
| 10 | Walk-in Watch (44-45) | 19 [adj] | **Thin.** Vendor loss figures only; local alarms and no-subscription rivals exist. |
| 11 | Room puck (54) | 19 | **Partial.** Teams panel check-in bug thread; platform fix "coming soon". |
| 12 | Trail/park counter (92); daycare CO2 display (62); hangboard logger (71); venue SPL sign (71); laundry cycle sensor (81) | 19 | Not validated. The trail counter has the clearest incumbent price gap ($4-6K units). |

Read with the evidence, the shortlist is different from the score order. **Crew Beacon Tag and Unit Door Sentinel** have operators describing the problem in their own words and an existing habit of paying for a fix. The **STR puck** has customers angry about exactly the subscription model the founder would avoid, which is the clearest product-market wedge in the screen. However, it fights an incumbent that Airbnb subsidizes. The **school aerosol sensor** has the most money and the most documented dissatisfaction. It is also the hardest to win on quality, and its procurement cycles are slow. The **Stocktank** and **machine monitor** ideas score high on fit and build, but they need a few hours of forum reading before any design work. Several ideas share one hardware platform: a LoRa node, a local hub and an e-paper display. That platform covers stock tanks, unit doors, walk-ins, leak pucks and rural water tanks. Building it once lets the founder test several markets cheaply.

Three earlier favourites lost ground in validation. **Leak and freeze sensors for landlords and insurers** fell from 20 to 17-18 because hardware sells for $13-$55, insurers give devices away, and no landlord voice was found. **Closet Sentinel** fell to 18 because the $145-$500 band is crowded. **Walk-in Watch** fell to 19 because local, no-subscription alarms already exist.

## Forums the founder should read personally

Automated research hit hard limits. Reddit returned a domain error, and site-restricted searches were ignored. Airbnb Community and most of BiggerPockets were not indexed. **Practical Machinist and Self-Storage Talk returned 403 errors, and LawnSite redirected to a paywall (402).** Only search snippets of those threads were seen, and their dates are unverified. The table below lists the specific threads the notes identified, plus the communities the researchers searched but could not reach. Reading them with a normal browser, and noting dates, quotes and prices paid, is what would turn the "unproven" labels above into evidence.

| Community | What to read | Tests which idea |
|---|---|---|
| LawnSite | ["Customer claims I didn't cut his grass"](https://www.lawnsite.com/threads/customer-claims-i-didnt-cut-his-grass-and-will-not-pay.503826/); ["Customer claims their lawn hasn't been mowed"](https://www.lawnsite.com/threads/customer-claims-their-lawn-hasnt-been-mowed.459192/); ["How do you verify that employee cut the customer's lawn?"](https://www.lawnsite.com/threads/how-do-you-verify-that-employee-cut-the-customers-lawn.512717/); ["How to respond to BS customer complaints"](https://www.lawnsite.com/threads/how-to-respond-to-bs-customer-complaints.487646/) | Crew Beacon Tag: dispute frequency, dollar loss, whether photos already suffice |
| Self-Storage Talk | ["Individual Unit Alarms"](https://www.selfstoragetalk.com/forum/general-self-storage-forums/technology-software-and-security/208237-individual-unit-alarms); ["Individual door alarms"](https://www.selfstoragetalk.com/forum/general-self-storage-forums/technology-software-and-security/7195-individual-door-alarms); [fence security thread](https://www.selfstoragetalk.com/forum/general-self-storage-forums/technology-software-and-security/169-fence-security-question/page2) | Unit Door Sentinel: per-door prices paid, battery and false-alarm complaints |
| Practical Machinist | ["Is connecting machines to the network worth it"](https://www.practicalmachinist.com/forum/threads/is-connecting-machines-to-the-network-worth-it.449903/); ["Shop floor data collection"](https://www.practicalmachinist.com/forum/threads/shop-floor-data-collection.426976/); ["MTConnect: two shops share their experience"](https://www.practicalmachinist.com/forum/threads/mt-connect-two-shops-share-their-experience.252566/) | Clamp-on machine monitor: subscription resistance, local-first demand |
| Airbnb Community | Host threads on noise monitors, Minut/NoiseAware billing, party damage (no specific threads retrievable; search [community.withairbnb.com](https://community.withairbnb.com)) | STR puck: willingness to pay a higher one-time price |
| Reddit | r/airbnb_hosts (STR puck); r/landlord, r/PropertyManagement (leak sensors); r/Teachers, r/k12sysadmin (vape sensor); r/restaurateur, r/restaurantowners, r/KitchenConfidential (walk-in alarms); r/ranching, r/homestead (stock tank); r/Machinists (machine monitor); r/selfstorage (door sensor); r/sysadmin, r/msp, r/homelab (closet monitor); r/facilitiesmanagement, r/Office365 (room puck); r/CommercialCleaning, r/securityguards, r/sweatystartup (proof-of-visit); r/Truckers (trailer tracker); r/gymowner (gym access); r/AutoRepair, r/laundromat (sector 81); r/ECEProfessionals (daycare); r/podcasting (OnAir puck); r/LocalGovernment (counters); r/Construction (jobsite) | Every idea; Reddit was fully blocked |
| Other forums worth a look | [STR Specialist host thread](https://strspecialist.com/community/thread/noise-monitoring-airbnb-minut-vs-noiseaware-alternatives) (readable); [eMastercam monitoring thread](https://www.emastercam.com/forums/topic/89318-anyone-using-machine-monitoring-software/); [Level1Techs server-room thread](https://forum.level1techs.com/t/server-room-emergencies/199629); [Edugeek server-room thread](https://www.edugeek.net/forums/topic/104948-server-room-temperature-monitoring/); [Microsoft Teams panels thread](https://techcommunity.microsoft.com/discussions/microsoftteams/teams-panels---check-in-issues/4252784); [OBS on-air light thread](https://obsproject.com/forum/threads/on-air-light.123290/); Spiceworks and ranchers.net (searched, nothing current) | Closet Sentinel, room puck, OnAir puck, Stocktank |

## Conclusion

The screen shows a design pattern more than it ranks sectors. In sector after sector, the incumbent charges a monthly fee for a radio sensor and a cloud dashboard, and the documented complaints are about that fee, about devices that stop working when the plan lapses, or about false alarms. A founder who sells reliable, local-first hardware for a one-time price is attacking the business model, not the sensor. That is why the same LoRa-node-plus-hub architecture keeps scoring 19-21 across agriculture, storage, hospitality, retail and property. The trap is that the scoring rewards what this founder is good at (buildable, on-brand) more than what the market has proven. Of eighteen ideas at 19 or above, only five have any user voice behind them.

The practical implication is to sequence by evidence, not by score. Spend a weekend in the LawnSite, Self-Storage Talk, Practical Machinist and Airbnb threads above before choosing. Favour the idea where operators already pay for a worse solution: storage door alarms, guard and crew verification, and STR monitors. Prototype the shared LoRa node and hub once, so the stock-tank and walk-in variants become cheap follow-on tests rather than separate bets. Ideas resting on vendor-only pain (walk-ins, closets, ghost bookings) or on insurer channels (leak pucks) should wait until a real buyer says, in their own words, that they would pay.
