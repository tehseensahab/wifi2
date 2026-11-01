# Fact-check record: block-website-on-router

Internal record. Not published. Research date: 2026-11-01. Steps from vendor docs; not tested.

## Research log

| # | Claim | Verbatim quote | Source | Pub / effective date | Geography | Qualifications |
|---|---|---|---|---|---|---|
| 1 | eero feature needs Plus | "an eero Plus feature"; "lets you manually block or allow specific websites and domains" | https://eero.com/support/articles/what-is-block-and-allow-sites | no date | | |
| 2 | eero steps | Home tab > Profile > Block & Allow Sites > "Add Blocked Site" > Domain > toggle > Save; network-wide Home > Security & privacy > eero Plus > Network controls > Block & Allow Sites (summary) | same | | | steps summarized |
| 3 | Domain rules | example.com "Affects the entire domain"; subdomain only affects subdomain; URLs not accepted (summary) | same | | | |
| 4 | Allowed priority | "always take priority over Content Filters and Blocked Sites" | same | | | |
| 5 | Timing/cache; multiple domains | changes within seconds; caches delay minutes or hours; popular sites may need several domains (summary) | same | | | |
| 6 | ASUS steps | Firewall > URL Filter; Black List / White List; + ; Apply; asusrouter.com | https://www.asus.com/us/support/FAQ/1037946 | Last Update 2024/07/22 | US | |
| 7 | ASUS no per-device | page says ASUS routers don't support blocking a website for one specific device or exempting devices (summary) | same | | | summary; core claim, re-verify |
| 8 | NETGEAR web | routerlogin.net; ADVANCED > Security > Block Sites; alt "Settings > Content Filtering > Block Sites"; Never/Per Schedule/Always; Add Keyword; Apply | https://kb.netgear.com/24053/How-do-I-block-Internet-sites-on-my-NETGEAR-router-from-the-router-web-interface | Last Updated 07/07/2025 | | Orbi not listed |
| 9 | NETGEAR app | "Tap the Parental Controls tile." "Select the History tab." "Swipe right on a website to block." "Set as Not Allowed:"; models incl. RS100, RS200, RS300, RBK50 etc. | https://kb.netgear.com/000062159/How-do-I-block-or-allow-access-to-a-website-with-NETGEAR-Smart-Parental-Controls | Last Updated 07/07/2025 | | Premium requirement not stated |
| 10 | TP-Link Archer | Advanced > Parental Controls; Add profile; "Add one or more keywords. All websites containing the keywords will be blocked."; "Please make sure the Private MAC Address is disabled on your clients; otherwise, the parental control won't take effect."; "Only devices that have previously been connected to your router's network are listed here." | https://vigi.com/baltic/support/faq/1124 | Updated 10-21-2025 | mirror | model list incl. A7, AX3000 |
| 11 | Deco | Blocked Websites page; "Ensure you have entered the full domain name of the websites rather than the keywords"; "Add a Website"; Malicious Content Filter on Security page; add redirect domains from History; clear cache | https://www.tp-link.com/us/support/faq/2643 | Last updated August 25, 2026 | US | |
| 12 | Firefox DoH | "If a user has chosen to manually enable DoH, the signal from the network will be ignored"; "Firefox will disable DoH for the remainder of the network session." | https://support.mozilla.org/en-US/kb/configuring-networks-disable-dns-over-https/revision/289782 | 2024-12-01 | | |
| 13 | VPN/cellular bypass | general networking statement, unsourced | — | | | general knowledge |
| 14 | NETGEAR Premium exists | KB 000062159 links to "How do I start a subscription for Smart Parental Controls Premium?" | kb.netgear.com/000062159 | | | |

## Independent fact-check (2026-11-01, separate agent)
Re-fetched eero Block & Allow ("URLs aren't accepted — use FQDNs."), ASUS ("ASUS routers currently do not support website blocking on specific devices(e.g. phone, laptop)."; "Last Update : 2024/07/22"). Result: core claims VERIFIED. Removed: free-eero-features sentence, ASUS firmware note (not logged). Qualified/reworded: "exact menus" -> "menus"; NETGEAR app model scope; NETGEAR web model scope; Archer model range; Deco domain-name wording; Premium wording; "DNS-based" added to Firefox takeaway.
Totals: verified 22, qualified 6, removed 2.
