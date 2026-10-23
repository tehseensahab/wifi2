# Fact-check record: use-old-router-as-access-point

Article: content/guides/use-old-router-as-access-point/index.md
Byline: Tehseen Arbab (the 2026-10-22 owner change removed John Marshall and Craig Leslie as invented authors, so the daily prompt's bylines were not used)
Research date: 2026-10-23 (UTC)
Search Console query targeted: none confirmed (GSC Wizard returned payment_required); from editorial/IDEAS.md idea #1

## Research log
1. Netgear KB 20927 (updated 2025-07-07): https://kb.netgear.com/20927/How-do-I-change-my-NETGEAR-router-to-AP-mode — menu paths, AP Mode, default "Get dynamically from existing router", fixed IP "(not recommended)", connection drops after Apply, finish basic setup first.
2. Netgear KB 26765 (updated 2025-07-07): https://kb.netgear.com/26765/Disabled-Features-on-the-Router-when-set-to-AP-Mode — grayed-out feature list.
3. ASUS FAQ 1015009 (updated 2026-03-03): https://www.asus.com/us/support/FAQ/1015009 — wired connection to primary router; WAN or LAN port to main LAN; 100 m; DHCP on primary; Automatic IP; firewall/IP sharing/NAT disabled by default; Device Discovery Utility.
4. TP-Link FAQ 1384 (updated 2026-06-04): https://tp-link.com/support/faq/1384/ — manual method; example 192.168.2.11, DHCP .100-.199; disable DHCP; reboot; LAN-to-LAN.
5. TP-Link roaming troubleshooting (undated, Omada business APs): https://www.tp-link.com/us/document/13229 — same SSID and security method; clients may refuse to roam.
6. FBI IC3 PSA I-050725-PSA (2025-05-07): https://www.ic3.gov/PSA/2025/PSA250507 — EOL router proxy warning; replace if possible.

## Fact-check result (independent subagent, 2026-10-23)
Verified: all Netgear, ASUS, TP-Link FAQ 1384 and FBI claims and dates; TP-Link roaming quotes (scope noted in article).
Qualified -> fixed: Netgear step 5 reworded to Netgear's wording (computer loses connection); login step added; "works the same way on most routers" -> "same idea applies"; step-1 example IP aligned to 192.168.2.x; "DHCP still on" -> "most likely still on"; bridge mode -> "wireless repeater mode" in FAQ; undated TP-Link roaming source date removed; "if possible" added to FBI takeaway; research-based disclosure line added.
Not verified -> reframed: "leave WAN port empty" now presented as our advice and noted in the sources table.
Editorial (no source): factory reset, channel separation, troubleshooting list, no ISP speed gain.
Image: Unsplash photo by Manuel Luikenga, viewed before use: black Ethernet cables in lit ports on a gray network device. 2400x1600, used as-is.
Status: PASS
