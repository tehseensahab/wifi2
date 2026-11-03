# Fact-check record: best-ups-for-router

Article: content/guides/best-ups-for-router/index.md
Origin: editorial/IDEAS.md idea #3 (2026-11-02), narrowed to UPS buying guide
Byline: Tehseen Arbab
Research date: 2026-11-03 (UTC)
Search Console: not used (excluded from daily runs)

## Research log (claim | verbatim quote | URL | date | geography | qualifications)
- APC runtime chart (models BE425M, BE600M1, BE850G2, in that order): "Internet modem and router (10 watts) 2.3 hours 4.3 hours 5.9 hours"; "Entry level PC (40 watts) 45 minutes 67 minutes 90 minutes"; "Notebook computer + network gateway (80 watts) 18 minutes 30 minutes 41 minutes"; "Midrange PC with 20" LCD + Notebook + network gateway (180 watts) 5.8 minutes 10 minutes 14.8 minutes"; "Output Capacity 425 VA, 255 Watts 600 VA, 330 Watts 850 VA, 450 Watts" | https://images.salsify.com/image/upload/s--6wmQwTH1--/b30b95c3d4c710f2921ec6d1d8f1fc8d36257bdc.pdf | undated | US 120V line
- BE600M1 data sheet: "Rated power in VA 600 VA" "Max Configurable Power (Watts) 330 W" "Waveform Type Stepped approximation to a sinewave" "Battery Type Lead-Acid battery" "Typical recharge time 10 h" "Topology Standby" "Warranty 3 years repair or replace"; outlets "5 NEMA 5-15R" and "2 NEMA 5-15R surge" | https://www.mouser.com/datasheet/2/357/1/BE600M1_document-1559837.pdf | Jan 18, 2022
- B&H BE600M1: Price $83.99; "In Stock"; Battery backup and surge 5 x NEMA 5-15R; Surge only 2 x NEMA 5-15R | https://www.bhphotovideo.com/c/product/1259544-REG/apc_be600m1_back_ups_600va_ups.html | checked 2026-11-03 | US
- CyberPower CP1500PFCLCD: "1500VA / 1000W" "Sine Wave" "Line Interactive" Outlets battery & surge "6", surge-only "6", total "12"; "Runtime at Full Load" "2.5 min"; "Runtime at Half Load" "10 min"; "3 Year Limited Warranty"; "$274.95 MSRP" | https://www.cyberpowersystems.com/product/ups/pfc-sinewave/cp1500pfclcd/ | undated | US. B&H page for it failed (client_error).
- BGE50ML: "Run a router, modem and other low-power devices for 3 to 5 hours during a power outage." Li-ion. "Sorry, this product is no longer available, please contact us for a replacement." | https://www.apcguard.com/BGE50ML.asp
- BGE90M: "4.5 hours of network power" ; "Sorry, this product is no longer available, Please contact us for a replacement."; datasheet: "Maintenance-free, sealed lead-acid battery" | https://www.apcguard.com/BGE90M.asp ; https://cdn.blueally.com/apcguard/datasheets/back-ups-connect/bge90m-ds.pdf
- Xfinity: backup battery for Voice modem supports voice service only (does not mention internet); phone and alarm "up to 24 hours"; published Apr 3 2025, last modified Aug 31 2026 | https://www.xfinity.com/support/articles/power-outages-and-digital-voice-service
- FCC 2015 order: providers must "offer at least one technical solution capable of supporting at least 8 hours of uninterrupted 911 service"; within three years also "a technical solution capable of supporting 24 hours of uninterrupted 911 service"; applies to "facilities-based, fixed voice service that is not line-powered by the providers"; Federal Register Oct 16, 2015 | https://www.govinfo.gov/link/fr/80/62485

## Fact-check result (independent subagent, 2026-11-03; re-fetched CyberPower CP1500PFCLCD and B&H BE600M1)
- Verified: APC runtime chart (all 12 values), BE600M1 data sheet specs, B&H $83.99 in stock and 5+2 outlets (re-fetched 2026-11-03), CyberPower specs/runtime/MSRP, BGE50ML/BGE90M no longer available, Xfinity 24 hours, FCC 8h/24h voice-only.
- Calculations: 258/30 = 8.6-fold drop vs 8x load (fixed from "nine-fold"); 5.9 - 4.3 = 1.6 h (verified); "bigger UPS doesn't add hours in proportion" contradicted (BE600M1->BE850G2 runtime +37% vs VA +42%; BE425M->BE600M1 +87% vs +41%) and removed.
- Fixed: heading no longer says "lithium" (BGE90M is lead-acid; data sheet added to sources); FAQ "laptop or switch" -> "laptop"; Xfinity FAQ no longer says "not internet"; CyberPower low-load runtime wording; "built to let a PC shut down" softened; FCC scope wording ("facilities-based ... fixed ... not line-powered"); provider-network backup sentence softened; APCGuard described as an online store selling APC products.
- Price recheck: B&H BE600M1 $83.99, In Stock, re-fetched by fact-checker 2026-11-03. CP1500PFCLCD retailer price not available (B&H client_error); MSRP only, labeled.
- No hands-on testing; guide states it.
