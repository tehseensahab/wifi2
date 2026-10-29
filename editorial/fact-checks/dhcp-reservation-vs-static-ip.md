# Fact-check record: dhcp-reservation-vs-static-ip

Internal record. Not published. Research date: 2026-10-29.

## Research log

| # | Claim | Verbatim quote | Source | Pub / effective date | Geography | Qualifications |
|---|---|---|---|---|---|---|
| 1 | Google reservation definition | "your Wi-Fi network assigns the same IP address to a specific device whenever that device connects to your network." | https://support.google.com/googlehome/answer/6274660?hl=en | no date | global | |
| 2 | Google may need reconnect | "You may need to disconnect this device from your Wi-Fi network and reconnect it before it is assigned the reserved IP." | same | | | |
| 3 | Google app path | Advanced Networking > DHCP IP reservations > add; choose device; "Enter a static IP address" (fetch summary of steps) | same | | | steps paraphrased by fetch |
| 4 | RFC 2131 manual allocation | "a client's IP address is assigned by the network administrator, and DHCP is used simply to convey the assigned address to the client." | https://rfc-editor.org/rfc/rfc2131.html | March 1997 | standard | |
| 5 | RFC servers should check | "When allocating a new address, servers SHOULD check that the offered network address is not already in use; e.g., the server may probe the offered address with an ICMP Echo Request." | same, sec 3.1 | | | |
| 6 | RFC client should probe | "the client SHOULD probe the newly received address, e.g., with ARP." | same, sec 2.2 | | | |
| 7 | NETGEAR reservation purpose | "that device is always assigned the same IP address each time it accesses the router's DHCP server"; "might want to assign reserved IP addresses to computers or servers that need permanent IP settings to work correctly." | https://kb.netgear.com/25722/How-do-I-reserve-an-IP-address-on-my-NETGEAR-router | Last Updated 07/07/2025 | | |
| 8 | NETGEAR path | "ADVANCED > Setup > LAN Setup"; some models "Settings > Setup > LAN Setup"; Address Reservation section | same | | | |
| 9 | NETGEAR renew | "reboot the computer, or access its IP configuration to force a DHCP release and renew." | same | | | |
| 10 | TP-Link reservation def | "When you specify a reserved IP address for a PC in the LAN, the PC will always receive the same IP address" | https://www.omadanetworks.com/us/support/faq/182/ | Sept 17, 2026 | US mirror | TP-Link FAQ on Omada mirror |
| 11 | TP-Link subnet rule | "must be on the same subnet with the LAN IP, and it cannot be a reserved IP address"; example 192.168.0.2 to 192.168.0.254 for LAN IP 192.168.0.1 | same | | | |
| 12 | TP-Link path + reboot | "Advanced > Network > DHCP Server > Address Reservation"; click Reboot "all the settings would take effect" | same | | | |
| 13 | ASUS inside pool | "Please make sure the IP address needs to be in the IP pool of your DHCP server." | https://www.asus.com/us/support/FAQ/1000906 | Last Update 2026/09/09 | US | |
| 14 | ASUS max | "The DHCP server page will show the maximum number of manually assigned IPs." "For example, Max Limit is 128." | same | | | |
| 15 | ASUS path | "Go to [Advanced Settings] > [LAN] > [DHCP server]" | same | | | |
| 16 | Microsoft static IP unique | "This IP address must be a unique address in the range of addresses that are available for your network." | https://learn.microsoft.com/ar-sa/troubleshoot/windows-server/networking/change-ip-address-network-adapter | updated 2026-02-12 | | English body on ar-sa locale; Control Panel path, "Internet Protocol (TCP/IP)" |
| 17 | Microsoft conflict error | "The static IP address that was just configured is already in use on the network. Please reconfigure a different IP address." | same | | | |
| 18 | Apple manual | "If your ISP or administrator gave you an IP address, choose Manually, then enter the address in the IP address field." Steps: Details > TCP/IP > Configure IPv4 | https://support.apple.com/guide/mac-help/mchlp2718/mac | | | |
| 19 | eero bridge mode loses | "IP reservations and port forwarding" | https://eero.com/support/articles/what-features-do-i-lose-if-i-put-my-eeros-in-bridge-mode | | | |
| 20 | eero Reservations & Port Forwarding | "With this setting, you can assign IP reservations and port forwarding rules for devices on your eero network." | https://eero.com/support/articles/what-advanced-features-does-eero-support | | | |
| 21 | EnGenius static outside pool | "If you assign a local static IP that is in the DHCP lease pool, the DHCP service will not know it"; "you want to assign them outside the DHCP lease pool"; "static IP addressing is recommended in most access point deployments" (from question) | https://doctorengenius.engeniustech.com/en/articles/6708950-... | Nov 4, 2022 | | vendor FAQ |
| 22 | eero: MAC randomization affects IP reservations | "IP reservations and port forwarding" (listed as affected features) | https://eero.com/support/articles/what-is-mac-address-randomization | verified 2026-10-28 (private-wifi-address record #18) | US | |
| 23 | Android 10+ randomizes by default | "For devices running Android 10 or higher, the framework uses a randomized MAC address by default." | https://source.android.com/docs/core/connect/wifi-mac-randomization-behavior | last updated 2026-10-09 | global | verified 2026-10-28 (private-wifi-address record #11) |
| 24 | Reservation screens ask for MAC | NETGEAR: enter "the IP address and the device's MAC address"; TP-Link: MAC address field "could be uppercase or lowercase" | NETGEAR KB 25722; TP-Link FAQ 182 | | | |

## Independent fact-check (2026-10-29)

Separate subagent; 5 re-fetches (ASUS 1000906, Google 6274660, Adorama RS300, NETGEAR RS200, B&H RS100), all succeeded, no approval errors.
- NOT VERIFIED and fixed: "prevents most address conflicts" (reworded); TP-Link "default LAN address" (now "TP-Link's example"); "Google Nest Wifi and Google Wifi" product names (now "Google routers managed in the Google Home app"); MAC/private-address claims (sourced to eero + AOSP, unsourced printer sentence removed).
- QUALIFIED and adjusted: EnGenius quote attributed to the FAQ's premise; Apple quote completed; Microsoft row marked Qualified; table row on pool rules made brand-specific.
- Reasoning kept as stated (no source needed): reservations don't move to a new router; switched-off device won't answer a probe.
