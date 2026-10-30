# Fact-check record: what-is-a-subnet-mask

Internal record. Not published. Research date: 2026-10-30.

## Research log

| # | Claim | Verbatim quote | Source | Pub / effective date | Geography | Qualifications |
|---|---|---|---|---|---|---|
| 1 | Mask definition | "a 32-bit mask that selects the network number and subnet number fields of the corresponding IP address" | https://rfc-editor.org/rfc/rfc1122.html sec 3.3.1.1 | Oct 1989 | standard | |
| 2 | Local decision | "then the destination is on the corresponding connected network"; "the datagram is to be transmitted directly to the destination host" | same | | | |
| 3 | Remote via gateway | "If not, then the destination is accessible only through a gateway." | same | | | |
| 4 | Host 0/-1 not permitted | "IP addresses are not permitted to have the value 0 or -1 ... <Host-number>, <Network-number>, or <Subnet-number> fields." | https://rfc-editor.org/rfc/rfc1122 sec 3.2.1.3 | Oct 1989 | | exceptions for special cases |
| 5 | Directed broadcast | "{ <Network-number>, -1 }" "Directed broadcast to the specified network." | same | | | |
| 6 | CIDR notation | "followed by a decimal value between 0 and 32 that describes the number of significant bits." | https://rfc-editor.org/rfc/rfc4632.html sec 3.1 | Aug 2006 | | |
| 7 | /24 bits | "the most significant 24 bits are ones and the least significant 8 bits are zeros." | same | | | |
| 8 | /16 mask | "with an implied network mask of 255.255.0.0, is defined as the prefix 172.16.0.0/16" | same | | | |
| 9 | Private ranges | "10.0.0.0 - 10.255.255.255 (10/8 prefix)"; "172.16.0.0 - 172.31.255.255 (172.16/12 prefix)"; "192.168.0.0 - 192.168.255.255 (192.168/16 prefix)" | https://www.rfc-editor.org/rfc/rfc1918 | Feb 1996, BCP 5 | | |
| 10 | No global meaning | "Because private addresses have no global meaning, routing information about private networks shall not be propagated on inter-enterprise links" | same | | | |
| 11 | RFC 950 mask | "a bit-mask with bits set in the fields corresponding to the IP network number"; recommends contiguous subnet bits | https://www.rfc-editor.org/rfc/rfc950 | Aug 1985 | | background only |
| 12 | ASUS defaults | "For ASUS routers, the default LAN IP is 192.168.1.1 or 192.168.50.1"; "The default value is 255.255.255.0." | https://www.asus.com/us/support/FAQ/1011245 | Last Update 2026/03/18 | US | |
| 13 | ASUS path | LAN > LAN IP; edit IP Address / Subnet Mask; "Click Apply to save the setting." | same | | | steps via fetch summary |
| 14 | Google steps | Wi-Fi settings > Advanced Networking > LAN; Router LAN IP (address + subnet mask); DHCP address pool; Save | https://support.google.com/googlenest/answer/7571856 | | | |
| 15 | Google migration | "we'll automatically migrate existing DHCP IP reservations and port forwarding rules to the new subnet."; "your connected devices will briefly disconnect from Wi-Fi." | same | | | |
| 16 | eero location | Advanced networking > Network services > DHCP & NAT; "Here, you can review or change your network's DHCP range" | https://eero.com/support/articles/what-are-the-advanced-networking-settings | no date | | page doesn't list masks |
| 17 | TP-Link example | "LAN IP 192.168.0.1, IP range 192.168.0.xx (xx=2--253), subnet mask 255.255.255.0, and default gateway 192.168.0.1." | https://www.omadanetworks.com/support/faq/41/ | Updated 02-26-2026 | | |
| 18 | Mac path | "Click the Apple menu > System Settings > Network > Wi-Fi." Details > TCP/IP; enter "IP address, Subnet mask, and Router (the default gateway)" | same | | | TP-Link guide, Qualified |
| 19 | iPhone path | tap info icon next to network; "scroll down and tap Configure IP" | same | | | page says "WLAN"; US iOS label is Wi-Fi |
| 20 | Windows ipconfig | "Type ipconfig /all in the command prompt and then press Enter."; Subnet Mask; Default Gateway "The router or switch that the network connection goes through." | https://support.ksu.edu/TDClient/30/Portal/KB/PrintArticle?ID=69 | Modified 9/4/24 | | university IT, Qualified |

Calculations: /24 = 2^8 = 256 (254 usable); /23 = 2^9 = 512 (510); /22 = 2^10 = 1,024 (1,022); /16 = 2^16 = 65,536 (65,534); 255.255.254.0 = /23, 255.255.252.0 = /22.

Skipped: learn.microsoft.com tcpip-addressing-and-subnetting (PROVENANCE_REQUIRED approval timeout; also reached via support.microsoft.com/kb/164015 redirect).

## Independent fact-check (2026-10-30)

All calculations recomputed correct. Applied: "254 usable addresses, including the router's"; IPv6 FAQ framed as general background; NAT explanation separated from the RFC 1918 quote; iPhone path matched to source (Configure IP); eero bullet limited to DHCP range; "usual" -> "common" symptom; Windows step uses `ipconfig /all` as sourced. No claims removed; none NOT VERIFIED remain.
