# Fact-check record: reset-router

Article: content/guides/reset-router/index.md
Origin: new troubleshooting topic (gap: no reboot/reset guide in INDEX.md)
Byline: Tehseen Arbab
Research date: 2026-11-04 (UTC)
Search Console: not used (excluded from daily runs)

## Research log (claim | verbatim quote | URL | date | geography | qualifications)

### NETGEAR
- Reboot keeps settings | "All of your WiFi settings are saved when you reboot your router." | https://kb.netgear.com/000061793/How-do-I-power-cycle-or-reboot-my-NETGEAR-router | Last Updated 07/07/2025 | global
- Power cycle | "Power off your router by pressing the Power On/Off button." "Wait 30 seconds." "Power on your router by pressing the Power On/Off button." | same
- Reset as next step | "If rebooting your router doesn't solve your problem, you might want to try a factory reset." | same
- Factory reset erases | "A factory reset deletes all personalized settings including your user name, password" (plus SSID and security settings per fetch) | https://kb.netgear.com/9665/How-do-I-perform-a-factory-reset-on-my-NETGEAR-router | Last Updated 07/07/2025
- Steps | "Verify that your router's Power light is on." "Use a paper clip or similar object to press and hold the Restore Factory Settings or Reset button for seven seconds." | same
- Default login | User Name "admin" and Password "password" | same | applies to NETGEAR routers per KB; newer models may print credentials on label (not stated) -> article attributes to NETGEAR KB
- When needed | reset "is necessary when you cannot recover your password." | same
- Subscriptions | "manually reactivate Armor or Smart Parental Controls (SPC) services after performing a factory reset." | same
- Cable modem | "press and hold the Reset button for about seven seconds." "Factory default settings are restored." remove USB drive first | https://kb.netgear.com/000038536/How-do-I-reset-my-NETGEAR-cable-modem-or-modem-router | Last Updated 07/07/2025

### TP-Link
- Button | "press and hold the Reset or WPS/Reset button for more than 10 seconds." "Release when the SYS LED changes from slow-flash to quick-flash." "Make sure the router stays powered on during this process." | https://www.tp-link.com/us/support/faq/497/ | Last updated April 17, 2026 | US
- Irreversible | "A factory reset cannot be undone, so it's worth taking a moment to prepare." | same
- Web | "Advanced > System/System Tools > Backup and Restore", Factory Restore | same
- Backup | "If you backed up your configuration file before the reset, you can reload it from the same Backup and Restore page." | same

### ASUS
- Button | "press and hold the RESET button for 5-10 seconds until your power LED light starts to flash." | https://www.asus.com/us/support/faq/1000925/ | Last Update 2026/02/23 | US
- Web | "Click [Administration] > [Restore/Save/Upload Setting] tab." then Restore | same
- Erases | "All current settings will be deleted and the router will be restored to its factory default settings." | same
- ISP info | if your Internet connection needs an account, password or special settings, "save the information in advance or ask your Internet Service Provider (ISP) first." | same

### eero
- Reboot | "restarting your eero by unplugging it, waiting 30 seconds, and plugging it back in"; app: Home tab, tap eero, "Restart" | https://eero.com/support/articles/215473703-How-do-I-reboot-or-reset-my-eero | undated (release tag 2026.10.30)
- Gateway | "If you restart your gateway eero, it'll take your eero network offline." | same
- Soft reset | hold until LED "flashes yellow (no longer than 8 seconds)"; "saves its logs and advanced settings such as IP reservations and port forwarding configurations." | same
- Hard reset | hold until LED "flashes red (approximately 15 seconds)"; "A hard reset will factory reset your eero, clear all user data and logs, and remove the eero from your network." | same
- Ring Alarm Pro | "Hard resetting a Ring Alarm Pro will also hard reset the Ring Alarm platform. This will reset all Ring configuration options along with connected Z-wave devices." | same

### Xfinity
- Restart | app: WiFi > Troubleshoot > "Restart your Gateway" (rented gateways); manual: unplug, wait one minute, plug back in; "The restart process takes up to 12 minutes." | https://www.xfinity.com/support/articles/troubleshooting-your-cable-modem | Published 2026-06-26, modified 2026-08-31 | US
- Factory reset | "A factory reset will erase your custom settings (like WiFi name and password) and return the device to its original setup."; hold Reset 30 seconds; default WiFi name/password on label at bottom; covers rented XB2 and XB3; own equipment -> contact manufacturer | https://www.xfinity.com/support/articles/factory-reset-xfinity-gateway | Published 2025-10-24, modified 2026-08-31 | US

### Added after fact-check (from original fetch results / re-fetch)
- ASUS LEDs | "The LEDs go off while the router restarts. Wait until they turn on again, which means the reset is done." (fetch summary of https://www.asus.com/us/support/faq/1000925/) | Qualified (fetch summary)
- Xfinity reset details | "Locate the small Reset hole on the back of the gateway." "Press and hold the button with a paperclip or pin for 30 seconds." "The lights flash, then turn solid when the gateway is ready." (fetch summary of https://www.xfinity.com/support/articles/factory-reset-xfinity-gateway) | Qualified (fetch summary)
- eero (re-fetch by checker) | reboot by "pushing the reset button once"; "powered on for at least 90 seconds" and "has an internet connection before resetting and/or rebooting"; soft reset "keeps the eero on your network." | eero reboot/reset article | Verified

## Independent fact-check (separate subagent, 2026-11-04)
Re-fetched: eero reboot/reset article (OK). No approval errors.
Verified: all NETGEAR, TP-Link, ASUS, eero, Xfinity steps, hold times, dates.
Qualified: ASUS internet settings (inferred from "All current settings will be deleted" + save-ISP advice) -> reworded; NETGEAR SSID/security erased (fetch summary); general framing lines.
Not verified -> fixed: "fix most router problems" (summary reworded); modem restart-order negative claim (removed); intro/After contradiction about reconnecting (reworded); ASUS and Xfinity LED details (logged above from fetch output, kept).
Table row port forwarding: added eero soft-reset exception.
Removed claims: modem/router restart order statement.
