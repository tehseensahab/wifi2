# Fact-check record: high-ping-on-wifi

Article: content/guides/high-ping-on-wifi/index.md
Byline: John Marshall
Research date: 2026-10-21 (UTC)
Search Console query targeted: none confirmed (GSC Wizard connector returned payment_required); from editorial/IDEAS.md idea #2

## Research log

- Cisco "Validate Wi-Fi Throughput Testing and Troubleshooting" (Rev 2.0, 2026-07-08): "Since Wi-Fi is a shared medium..."; "This is because Wi-Fi is a half-duplex medium that has some management overhead"; "When channel utilization approaches 100%—or even 70%—clients contend for medium access, resulting in latency and collisions."; "Perform an over-the-air capture to analyze 802.11 retries. A high retry percentage indicates RF issues."; "weak signal strength at the edge of your coverage"; "another AP—either rogue or managed—uses the same channel, which causes interference"; fixes include narrower channel widths | https://www.cisco.com/c/en/us/support/docs/wireless/catalyst-9800-series-wireless-controllers/221766-validate-wi-fi-throughput-testing-and.html
- Intel article 000005585 (last reviewed 2025-02-05): Roaming aggressiveness "alters the signal strength threshold at which the WiFi adapter starts scanning for another candidate AP", default Medium, revert to default if no help; Global BG scan blocking: periodic scans by default, options Always/Never(default)/On Good RSSI, advise against changing for users who move; Throughput Booster default Disabled, "the throughput for other clients in the same network may be negatively impacted when this feature is enabled"; U-APSD default Disabled, interoperability issues with some APs reducing RX throughput; MIMO power save | https://www.intel.com/content/www/us/en/support/articles/000005585/wireless.html
- Apple 102766 (2026-07-14): 20 MHz for 2.4 GHz "helps to avoid performance and reliability issues"; Auto widths 5/6 GHz; wider channels more prone to interference; Channel Auto; multiple routers different channels "especially if they are close to each other"; enable all bands; WMM enabled, "Disabling WMM can affect the performance and reliability of devices on the network"; interference "less of a concern" in 5 and 6 GHz; deprecated security modes "reduce network reliability and performance" | https://support.apple.com/102766
- Wi-Fi Alliance Wi-Fi 6 page: OFDMA "effectively shares channels to increase network efficiency and lower latency" | https://www.wi-fi.org/discover-wi-fi/wi-fi-certified-6
- Wi-Fi Alliance Wi-Fi 7 launch (2024-01-08): MLO "allows devices to transmit and receive data simultaneously over multiple links" for "increased throughput, reduced latency, and improved reliability" | https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-7
- IEEE TGbn status: objectives "reducing latency by 25% for the 95th percentile of the latency distribution" vs EHT; final WG/EC approval projected Mar 2028; RevCom/SASB May 2028 | https://grouper.ieee.org/groups/802/11/Reports/tgbn_update.htm
- PlayStation PS Portal troubleshooting (2026-03-25): "For Remote Play connections, try using a wired connection for your PS5® console."; "Pause any downloads running on devices connected to your Wi-Fi." | https://www.playstation.com/en-us/support/hardware/psportal-troubleshooting/
- Ping commands and Windows ipconfig / macOS Router path: standard OS usage, not separately sourced.
- Researched but not used: no Microsoft document links WLAN AutoConfig background scanning to ping spikes; no authoritative AWDL source; Xbox wireless troubleshooting page returned no text (JavaScript); no FCC MBA gaming latency thresholds found.

## Fact-check result (independent subagent, 2026-10-21)

Verified (10): all Cisco, Apple, Intel, Wi-Fi Alliance, IEEE TGbn and PlayStation quotes are verbatim and correctly attributed; IEEE projected 2028 approval; title (53 chars).
Qualified -> fixed (10): Intel revert-to-default advice limited to roaming aggressiveness (takeaway and body); "lower setting scans less often" rewritten to Intel's own description; "only one device can transmit at a time" -> "generally take turns" (consistent with OFDMA); neighbors' networks line no longer attributed to Cisco; "biggest factors" -> "common causes", "helps more than any setting" -> "good first step"; "main target of next standard" -> "one of the stated goals", 802.11bn "expected to be called Wi-Fi 8"; regular-rhythm spikes tied to Intel's default periodic scans as "may"; bufferbloat takeaway hedged; description/summary/lead "usually"; Sony added to source list in intro. Also "On Good RSSI" description corrected to "scans only when the signal is low".
Not verified: none.
Image: Unsplash photo W5KtfcB7kw4 (Amine mouzaoui, free license), viewed before use: man with headset at a gaming PC, purple lighting. 2400x1600, no crop.
Status: PASS
