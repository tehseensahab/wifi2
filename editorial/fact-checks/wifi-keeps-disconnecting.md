# Fact-check record: wifi-keeps-disconnecting

Article: content/guides/wifi-keeps-disconnecting/index.md
Byline: Craig Leslie
Research date: 2026-10-18 (UTC). Research log compiled by a research agent; key sources listed below.

## Research log (summary)

Claim | Source | Date | Geography | Notes
1. Test another device; ping default gateway via ipconfig; power management (Allow the computer to turn off this device to save power); Wireless Adapter Settings > Power Saving Mode > Maximum Performance; Uninstall device + "Attempt to remove the driver"; forget network; Network reset paths (Win 11/10) | https://support.microsoft.com/help/10741 | updated 2026-09-28 | Global, Win 10/11 |
2. Pixel: test another device; safe mode test; Adaptive connectivity > Auto-switch to mobile network | https://support.google.com/pixelphone/answer/6183600 | no date | Global |
3. Apple: other devices offline -> possible outage, contact ISP; Airplane Mode; Connectivity Assist off; remove VPN/security apps; try 5 GHz; Reset Network Settings "only if other solutions fail" | https://support.apple.com/en-us/111786 | Oct 5, 2026 | Global |
4. Connectivity Assist "uses cellular data to improve your connection when Wi-Fi is slow or unusable" | https://support.apple.com/en-us/127686 | Sept 14, 2026 | Global |
5. Samsung Intelligent Wi-Fi > Switch to mobile data: "your device will switch to mobile data whenever the Wi-Fi connection is unstable" | https://www.samsung.com/us/support/answer/ANS10002546/ | 2026-04-17 meta | US |
6. eero: weak signal can cause drop; randomized MAC "can change over time" -> turn off Private Wi-Fi Address / Use device MAC; paused/blocked devices; profile-less new devices limited | https://eero.com/support/articles/why-is-my-device-offline | no date | US |
7. Netgear: weak signal; different names per band; common/default name | https://kb.netgear.com/000063823/ | 07/07/2025 | US |
8. ASUS 1012132: phone band preference "may render the smart connect rule ineffective or lead to frequent disconnections" | https://rog.asus.com/us/support/FAQ/1012132 | 2024/12/09 | US |
9. TP-Link 722: Smart Connect compatibility problems; outdated firmware wireless instability; appliances interference | https://www.tp-link.com/us/support/faq/722/ | Apr 17, 2026 | US |
10. 47 CFR 15.407(h): 60 s channel availability check; cease within 10 s; 30 min non-occupancy | https://www.ecfr.gov/current/title-47/chapter-I/subchapter-A/part-15/subpart-E | current as of 10/15/2026 | US |
11. TP-Link 763 DFS: clients "will encounter disconnection" then restored | https://www.tp-link.com/support/faq/763/ | Sept 15, 2026 | Global | EU 10-minute figure NOT used.
12. ASUS 1045936 DFS: clients disconnected for a period; 2.4 GHz works; untick "Auto select channel including DFS channels" | https://rog.asus.com/us/support/FAQ/1045936 | 2024/12/13 | US |
13. ASUS 1030641: firmware up to date; keep away from microwaves, refrigerators, cordless phones, power boxes | https://asus.com/support/faq/1030641 | 2026/02/23 | Global |
14. Apple 102319 interference sources; Bluetooth shares 2.4 GHz | https://support.apple.com/en-us/102319 | Apr 23, 2025 | Global |
15. TP-Link 3032: overheating common trigger for reboots; Auto Reboot schedule | https://www.tp-link.com/us/support/faq/3032/ | May 12, 2026 | US |
16. Xfinity overheating placement | https://www.xfinity.com/support/articles/prevent-gateway-overheating | modified Aug 28, 2026 | US |
17. Netgear wireless schedule | https://kb.netgear.com/24102/ | 07/07/2025 | US |
18. Apple 102766: WPA3 Personal or WPA2/WPA3 Transitional for compatibility; automatic firmware updates | https://support.apple.com/102766 | July 14, 2026 | Global |
19. Google Nest: legacy WPA2 devices may have issues with WPA3 transition mode | https://support.google.com/googlehome/answer/6309220 | no date | Global |
20. ASUS 1042500: some older devices cannot use WPA3; switch to WPA2-Personal | https://www.asus.com/support/faq/1042500/ | 2025/03/31 | Global |
21. Xfinity outage: app, outage map, text OUT to 266278 | https://www.xfinity.com/support/articles/check-service-outage | modified Aug 31, 2026 | US |
22. Netgear power cycle: wait 2 minutes; modem first | https://kb.netgear.com/19755/ | 07/07/2025 | US |
23. Intel: "You can resolve many issues by updating an out-of-date driver" | https://www.intel.com/content/www/us/en/support/articles/000005585.html | 02/2025 | Global |

## Not sourced (not used)
- DHCP pool exhaustion causing drops.
- Overheating causing Wi-Fi drops specifically (only reboots/performance).

## Fact-check result (independent agent, 2026-10-18)

Totals: ~50 claims checked. 33 VERIFIED, 15 QUALIFIED, 3 NOT VERIFIED (all fixed).
Changes applied after review:
- Apple misquote "may" -> "might be a service outage".
- Intel quote replaced with verified text from Intel article 000046115 ("You can remedy many problems by updating drivers and software.").
- Removed "starts the same way"/"first" (MS and Apple don't lead with the other-device test).
- Added Netgear's contrary view (separate band names listed as a cause) wherever band steering off is suggested.
- Softened: "Most routers" -> "Many"; private-address default; Netgear schedule limited to Nighthawk; DFS "minute or so" -> "short time"; takeaway "weak" -> "slow or unstable"; "Router makers disagree" -> Apple/Google/ASUS give different advice; FAQ "every few minutes" reworded.
- Ping interpretation now follows Microsoft's wording; Netgear 5-minute modem wait and ASUS 160 MHz step added; Pixel framing clarified (Google says turn on; off-to-test is our advice).
- Fixed five source titles and added missing sources (ASUS 1012132/1045936/1042500, TP-Link 722, Xfinity overheating, Netgear 19755/24102, Intel).
Cover: reused in-repo Unsplash photo LR_wX_klOPM (Stephen Phillips); this run's sandbox could not download from unsplash.com.
