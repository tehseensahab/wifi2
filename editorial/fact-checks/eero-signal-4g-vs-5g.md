# Fact-check record: eero-signal-4g-vs-5g

Internal record. Not published. Research date: 2026-11-01. Nothing tested.

## Research log

| # | Claim | Verbatim quote | Source | Pub / effective date | Geography | Qualifications |
|---|---|---|---|---|---|---|
| 1 | Similar speeds both models | "you'll experience similar backup speeds with either version." (fetch summary adds: some customers in certain areas may see speed advantages with 5G RedCap) | https://eero.com/support/articles/eero-signal | no date (©2026) | US | advantage sentence is summary, not verbatim |
| 2 | 4G cheaper, same core | "The 4G LTE version provides the same core backup functionality at a more affordable price." | same | | | |
| 3 | 5G falls back to LTE | "In areas where 5G RedCap isn't yet available, eero Signal 5G will automatically use 4G LTE networks." | same | | | |
| 4 | Model numbers | 4G LTE RG4U/RG4W; 5G RG5W (fetch summary) | same | | | summary |
| 5 | Typical speeds | "most customers will typically experience download speeds of 11-48 Mbps, upload speeds of 3-27 Mbps"; latency 50-100 ms (summary); Broadband Facts "11-48 Mbps," "3-27 Mbps," "50-100 ms" | same; https://www.eero.com/legal/network-management-statement?lang=en-us | NMS release tag 2026.10.27 | US | NMS body text has typos (114-48 etc.) |
| 6 | No battery | "eero Signal does not include a battery; it will not work in the event of a power outage unless you have a backup battery." | support | | | |
| 7 | 6 months Plus | "New eero Signal purchases include a 6-month eero Plus subscription." | support | | | |
| 8 | Plus 100 support price | "You can upgrade to eero Plus 100 for 50% off ($99) during setup or anytime in your first year." "Your subscription automatically renews at $199 per year after that." | support | | | |
| 9 | Plus 100 shop price | "get your first year of eero Plus 100 with 100 GB of backup data per month for $99.99"; "auto-renews at $199.99 a year"; annual Plus "$99.99 a year"; annual Plus 10 GB/year | https://eero.com/shop/eero-signal | checked 2026-11-01 | US | shop shows no device prices today |
| 10 | Monthly incompatible | "monthly subscription plans are incompatible with eero Signal" (verified 2026-10-31 run, same support page; today's summary: "Monthly eero Plus plans are incompatible with eero Signal") | support | | | |
| 11 | eSIM | "use the best cellular backup connection available through an included multicarrier eSIM." | support | | | |
| 12 | NAT only | "eero Signal cannot be used with a bridged eero network." "To utilize eero Signal, make sure your network is in NAT mode." | support | | | |
| 13 | Compatible eeros | eero 6, eero 6 Extender, eero Pro 6, eero 6+, eero Pro 6E, eero PoE 6, eero 7, eero Pro 7, eero Max 7, eero PoE 7, eero PoE Gateway; ISP eeros contact ISP (summary) | support | | | list from summary |
| 14 | Backup order | "If you have several backup options, your network uses them in this order:" main internet, eero Signal, Ring Alarm Pro, eero Internet Backup (summary) | support | | | |
| 15 | Placement | higher up, near exterior wall (summary) | support | | | |
| 16 | ~1 minute failover; hiccups | "Quick connection hiccups may not activate cellular backup."; main connection offline about a minute (summary) | https://eero.com/support/articles/how-do-i-troubleshoot-eero-signal | | | |
| 17 | LEDs | Solid Aqua: "Using cellular backup"; Solid Yellow/Orange: "eero Signal does not have an associated data plan or has consumed all available data for the period" | troubleshoot | | | |
| 18 | Device data controls | Internet > Backup usage > Devices (summary); heavy uses list | troubleshoot | | | |
| 19 | No min speed; congestion | "particular minimum speeds are not guaranteed"; "Our Underlying Carriers manage the networks that provide eero Signal connectivity, not eero."; "Users may experience reduced speeds during times of network congestion." | NMS | | | |
| 20 | RedCap | Release 17; 20 MHz; "up to 226 Mbps in downlink and up to 120 Mbps in uplink." | https://www.3gpp.org/news-events/partner-news/redcap-gsa-article01 | 2025-08-05 | global | theoretical |
| 21 | Hotspot Backup | "a nearby mobile hotspot or wifi network as a backup"; "up to eight backup wireless connections including wireless hotspots or nearby wifi networks"; "a feature of eero Plus" | https://eero.com/support/articles/what-is-eero-hotspot-backup | | | |
| 22 | Launch | Sept 3, 2025 release; 4G "$99.99"; 5G "$199"; 4G "available in the US via eero.com and Amazon.com early next year" | https://press.aboutamazon.com/devices/2025/9/eero-expands-offerings-for-homes-businesses-and-professional-installers-with-eero-signal-and-eero-poe-7 | 2025-09-03 | US | not current prices; not used as prices in article |
| 23 | 4G shipped | "now available via Amazon for $99" (update) | https://9to5mac.com/2026/02/12/eero-signal-announcement-features/ | 2026-02-12 | US | context only |
| 24 | Calc | 10 GB × 8,000 Mb/GB = 80,000 Mb ÷ 20 Mbps = 4,000 s = 66.7 min ≈ 67 min | calculated | | | decimal GB |

## Notes
- eero.com/shop/eero-signal/buy (device prices) returned PROVENANCE_REQUIRED today; device prices omitted.

## Independent fact-check (2026-11-01, separate agent)
Re-fetched: "While some customers in certain areas may experience speed advantages with 5G RedCap, in most cases, you'll experience similar backup speeds with either version."; latency "50-100 milliseconds"; RG4U/RG4W, RG5W; compatible list (PoE 6 / PoE 7 "provided they are powered via USB-C"); troubleshoot: "stay offline up to a minute"; shop prices confirmed; "At this time, monthly subscription plans are incompatible with eero Signal."
Removed: app notification on backup start/return (not verified); "offers more data" (not verified); "modem needs power". Reworded: "about a minute" -> "up to a minute"; "in most cases" added to description; backup-order naming; coverage-map claim; HD streaming.
Totals: verified 24, qualified 6, removed 3.
