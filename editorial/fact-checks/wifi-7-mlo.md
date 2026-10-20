# Fact-check record: wifi-7-mlo

Article: content/guides/wifi-7-mlo/index.md
Byline: Craig Leslie
Research date: 2026-10-20 (UTC)
Search Console query targeted: none confirmed (GSC connector unavailable); from editorial/IDEAS.md idea #2

## Research log

1. Wi-Fi Alliance: MLO "allows a device to transmit and receive simultaneously on more than one link"; aggregation, or choose soonest-available link for latency-sensitive packet; announced day before CES 2024 opening | https://wi-fi.org/media-content/wi-fi-alliance-unveils-wi-fi-certified-7 | Jan 2024 | global |
2. eero MLO: quote "enables your Wi-Fi 7 devices to simultaneously send or receive data across multiple wifi frequency bands"; models PoE 7, Max 7, Pro 7, eero 7, Outdoor 7; firmware v7.7.1 (Max 7) / v7.7.3; app 6.50; not tied to 6 GHz; WPA3 default with 6 GHz affects other bands; legacy "may have difficulty connecting"; reboot ~2 min; "is still being developed and tested"; won't increase ISP speed; more energy; some phones use fewer bands; disable when mixing Wi-Fi 7 and non-Wi-Fi 7 eeros; menu path | https://eero.com/support/articles/what-is-multi-link-operation-mlo | checked 2026-10-20 | US |
3. ASUS FAQ 1053342 (last update 2025/03/26): STR, eMLSR; "it will base on client devices supported modes"; GT-BE96, RT-BE96U, GT-BE98, GT-BE98 Pro firmware; AES+GCMP256; non-MLO node won't broadcast 6 GHz; only first Wi-Fi 7 node MLO backhaul, same model; separate MLO network; menu path | https://www.asus.com/support/FAQ/1053342 | 2025-03-26 | global |
4. Apple (page dated 2026-09-17): N1 models "support Wi-Fi 7 in the 2.4 GHz, 5 GHz, and 6 GHz bands and Multi-Link Operation (MLO)"; iPhone 17, Air, 17 Pro listed; 160 MHz max | https://support.apple.com/guide/deployment/dep268652e6c | 2026-09-17 | global |
5. Windows Central (2024-02-22): Windows 11 24H2 first version with Wi-Fi 7; needs Wi-Fi 7 AP and PC hardware | windowscentral URL | 2024 | — | secondary
6. PCWorld (2025-07-21): same SSID/password for MLO; Windows PCs usually MLSR (BE200, BE201); Intel driver docs: Wi-Fi 7 features from 24H2 | pcworld URL | 2025 | — | secondary
7. Dong Knows Tech: eMLSR "does not increase data rates"; BE200 eMLSR; MLO backhaul star topology, same models | dongknows URL | — | — | independent
8. RTINGS meta description: "Our testing reveals shallow implementations and marketing that oversells the hardware." last modified 2026-02-18 | rtings URL | — | — | body not readable

## Fact-check result (independent subagent, 2026-10-20)

Verified: Wi-Fi Alliance quote and Jan 2024 launch; eero MLO models, firmware, app version, WPA3 behavior, reboot, mixed-network advice, ISP-speed statement, menu path; ASUS modes quote, models/firmware, GCMP-256, AiMesh limits, separate MLO network; Apple N1 MLO statement and 160 MHz; PCWorld and Windows Central Windows 11 24H2 points; Dong Knows Tech eMLSR and backhaul points; RTINGS summary line.
Qualified -> fixed: "most phones and laptops" claim now attributed to PCWorld ("most MLO devices", Windows PCs usually) and ASUS's note that phones with STR pair 2.4+5 GHz added; eMLSR description now uses ASUS's own wording plus Dong Knows Tech; eero quote completed ("bands and channels"); "caps their top speed" -> "could limit maximum throughput"; ASUS model list dated (March 2025); iPhone FAQ notes newer N1 models and that Apple lists iPhone 16 as 802.11ax; Wi-Fi 6/6E takeaway reconciled with WPA3 warning; description no longer says bands are always used at once; RTINGS date added; "Wi-Fi 7 node" -> "node" per ASUS; "most practical new idea" superlative removed.
Not verified -> removed: claim that Apple marketed iPhone 16 as Wi-Fi 7 (not in our sources).
Image: Unsplash title says laptop but photo viewed before use shows a white four-antenna router; Unsplash description "Smart home wireless network router device". Alt text describes the photo as seen. Cropped to 2400x1600 landscape.
Status: PASS
