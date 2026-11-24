# Fact-check record: eero-6-plus-vs-eero-7

Article: content/guides/eero-6-plus-vs-eero-7/index.md
Origin: new (commercial slot), 2026-11-24
Byline: Tehseen Arbab
Research date: 2026-11-24 (UTC)
Search Console: not used (excluded from daily runs)
Nothing physically tested.

## Research log (claim | verbatim quote | URL | date | geography | qualifications)

eero 6+ support article (https://eero.com/support/articles/eero-6-plus, undated, US site):
- Standard | "Full support for Wi-Fi 6 (IEEE802.11a/b/g/n/ac/ax)"
- Bands/MIMO/ports | "Dual-Band<br>2x2/2x2 SU-MIMO<br>2.4 GHz: 2x2<br>5 GHz: 2x2<br>2 auto-sensing 1 GbE ports"
- Channel width | "20, 40, 80, 160 MHz" ; "Supporting bandwidth channels up to 160 MHz"
- Speed | "Supports wired or wireless speeds up to 940 Mbps" ; "AX3000 rating"
- Coverage | "Covering up to 1,500 square feet"
- Devices | "the ability to handle up to 75+ simultaneous connected devices"
- Smart home | "Zigbee controller", "Thread compatible", "Matter controller"
- Role | "it can be used as either a primary router or as a mesh access point for an existing eero network."

eero 7 support article (https://eero.com/support/articles/eero-7, undated, build 2026.10.23-1):
- Standard | "Full support for Wi-Fi 7 (802.11a/b/n/ac/ax/be)" ; "BE5000 Rating"
- Bands | "Dual-Band<br>2x2/2x2 SU-MIMO<br>2.4 GHz: 2x2<br>5 GHz: 2x2<br>Two 2.5GbE ports" ; "dual-band 2.4 and 5 GHz antennas" (no 6 GHz)
- Channel width | "20, 40, 80, 160, 240 MHz"
- Speed | "The eero 7 delivers wired speeds up to 2.3 Gbps and wireless speeds up to 1.8 Gbps"
- Ports | "Each eero 7 features two auto-sensing 2.5 GbE ports"
- Coverage | "up to 2,000 sq. ft. (190 m²) of indoor coverage per unit"
- Devices | "can support 120+ devices"
- Smart home | "Zigbee-compatible smart home hub", "Thread compatible", "Supports Smart Home Hub (SHH) and is Matter compliant"
- MLO | "A new feature of the eero 7 is Multi-Link operation (MLO) support"
- Plans | "making it well suited for 2.5 Gbps internet plans."

Comparison article (https://eero.com/support/articles/eero-mesh-wifi-product-comparison, undated):
- eero 6+ "Up to 1,500 sq ft per device", "75+ devices", wired/wireless "Up to 940 Mbps"
- eero 7 "Up to 2,000 sq ft per device", "100+ devices" (CONFLICT with 120+ elsewhere), "Up to 2.3 Gbps" wired, "Up to 1.8 Gbps" wireless
- eero 6+ connectivity cell says "MU/SU-MIMO" while support article says "SU-MIMO" -> don't make MIMO claims

Shop pages (prices as shown 2026-11-24; banner "Now live: Black Friday deals on eero"):
- eero 6+ | "eero 6+ (1-pack)" / "Original price: $139.99Sale price: $94.99" ; "Ideal for internet plans up to 1 Gbps and supports 250+ devices." (CONFLICT with 75+) ; "Together, eero 6+ and two eero 6+ extenders provide up to 4,500 sq. ft of coverage." | https://www.eero.com/shop/eero-6-plus?pack=f | 2-/3-pack prices not cleanly mapped: omitted
- eero 7 | 3-pack "Previous price $399.99" / "Current price $319.99"; 2-pack "Previous price $284.99" / "Current price $229.99"; 1-pack "Previous price $169.99" / "Current price $139.99"; "industry-leading three-year warranty" | https://eero.com/shop/eero-7/buy
- eero 7 shop | "Ideal for internet plans up to 2.5 Gbps with two auto-sensing 2.5 GbE ports and wireless speeds up to 1.8 Gbps." ; "3-year warranty" | https://eero.com/shop/eero-7
- eero 6+ warranty: not found on fetched pages; omitted.

Mixing (https://eero.com/support/articles/are-all-eeros-the-same, undated):
- "All eeros are compatible with each other no matter when they were released."
- "Yes. However, every network needs a gateway eero with an Ethernet port to connect to your modem."
- "Once your gateway eero is installed, you may use any combination of eeros to set up your network."
- gateway-capable list includes eero 6+ and eero 7
- Pro 6E caveat only: combining with older generation "may result in reduced performance across your network." (not stated for eero 7) -> do not extend to eero 7

## Calculations
- eero 7 1-pack sale vs eero 6+ 1-pack sale: $139.99 - $94.99 = $45.00
- 940 Mbps cap vs 1 Gbps plan: 940 < 1,000 (eero's own figure; plan says "up to 1 Gbps")
- 2,000 - 1,500 = 500 sq ft more per unit (maker figures)

## Fact-check result (independent subagent, 2026-11-24; 4 re-fetches shared across both articles: eero 7 buy page, eero 7 shop page (prod mirror), eero 6+ buy page, eero 6+ support article; no approval errors)
- No core claim failed in either article.
- OFDMA: verified Wi-Fi Alliance definition, NETGEAR advice and defaults, TP-Link default and client-support note, ASUS path, Qualcomm/Broadcom quotes (qualified, vendor authors). Fixed: "many routers ship off" -> named two models; "often off" -> "can be off"; older-device wording softened to NETGEAR's "might want to keep it off"; H3C "executive" removed; unsourced IoT "small bursts"/cameras reasoning replaced with NETGEAR's recommendation + Wi-Fi Alliance "high demand environments"; app-managed eero/Google claim replaced with neutral "check the maker's support pages"; MU-MIMO "multiple antennas" and "many routers side by side" replaced with sourced wording / ASUS-only; TP-Link wifi6 page added to sources + table; NETGEAR source day removed (Feb 2022 only); manual inconsistency stated in body. Kept as plain explanation (no source): OFDMA changes Wi-Fi airtime, not ISP plan speed.
- eero: prices re-verified 2026-11-24 (6+ 1-pack $94.99 from $139.99; eero 7 1/2/3-pack $139.99/$229.99/$319.99 from $169.99/$284.99/$399.99; Black Friday banner). Fixed: eero 6+ warranty is "limited 1-year" (draft wrongly said none found); device-count FAQ no longer ranks models; 940 Mbps vs 1 Gbps wording corrected; description ambiguity on sq ft fixed; Pro 7/Max 7 tri-band claim removed (not in log), now links to existing guide; MLO row "Not listed"; smart-home row uses eero's exact wording; eero.com/shop/eero-7 added to sources.
- Fact-checker re-fetch also found: eero 6+ buy page says "1-year warranty"; eero 6+ support article "backed by a limited 1-year warranty".
