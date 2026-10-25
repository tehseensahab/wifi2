# Fact-check record: what-is-cgnat

Article: content/guides/what-is-cgnat/index.md
Byline: Tehseen Arbab (owner removed John Marshall and Craig Leslie as invented authors on 2026-10-22; daily prompt bylines not used)
Research date: 2026-10-25 (UTC)
Search Console query targeted: none confirmed (GSC Wizard returned payment_required); from IDEAS.md backlog. No CGNAT post in INDEX.md; complements bridge-mode-double-nat-own-router and should-you-enable-ipv6.

## Research log (exact claim | source | date)
1. RFC 6598 / BCP 153 (April 2012): 100.64.0.0/10; "intended for use on Service Provider networks"; distinct from RFC 1918; CGN issues (console games sharing outside address, seeding "inability to open incoming ports through the CGN", geolocation, per-IP login limits, 6to4) | https://www.rfc-editor.org/rfc/rfc6598.txt
2. RFC 7021 (September 2013, Informational): NAT444; FTP sessions to servers inside the home failed; seeding failed in all four 2011 NAT444 scenarios; Xbox "Your NAT type is moderate" (2010); Xbox P2P failed with one public CGN address, later update helped some games; slight latency/jitter differences, reduced performance for large transfers/multiple video streams; tests 2010-2011 | https://www.rfc-editor.org/rfc/rfc7021.html
3. APNIC Blog, David Anderson, 2022-05-03 (adapted from Tailscale): CGNAT ISPs "tend to turn them off in the equipment they put in homes"; relays "pick up the slack when traversal fails, as it likely will for a long tail of cases" | https://blog.apnic.net/2022/05/03/how-nat-traversal-works-concerning-cgnats/
4. Tailscale docs: device addresses from 100.64.0.0/10 | https://tailscale.com/docs/concepts/tailscale-ip-addresses.md
5. DishyTech (mod 2025-08-12): Starlink CGNAT on most plans; public IPv6 per device; Starlink router firewall blocks outside traffic, no custom rules; Priority public IPv4 optional, not static | https://www.dishytech.com/does-starlink-have-port-forwarding/ , https://www.dishytech.com/can-you-get-a-static-ip-from-starlink/

Calculation: /10 -> 2^22 = 4,194,304 addresses; 100.64.0.0 + 0x3FFFFF = 100.127.255.255 (verified by fact-checker).
Not used: T-Mobile and Verizon community threads (no staff statements found), so no carrier-specific CGNAT claims were made for them.

## Fact-check result (independent subagent, 2026-10-25)
Verified: RFC 6598 facts and quotes; RFC 7021 NAT444, Xbox, seeding, dates; APNIC quotes; Tailscale range; range math.
Qualified (kept): Starlink claims via DishyTech; general IPv4/IPv6 background.
Fixed: "means CGNAT" -> "almost always means"; private-range WAN no longer stated as "not CGNAT"; FTP added to RFC 7021 quote; "every scenario" -> "all four NAT444 scenarios tested"; speed FAQ rewritten to match RFC 7021 performance findings; broken FAQ sentence fixed; unsourced "more common" double-NAT comparison removed.
Not verified: none remaining.
Image: Unsplash photo by Jordan Harrison (40XgDxBfYXM), viewed before use: numbered patch panel with blue and gray Ethernet cables. 2400x1600 cropped to 2400x1500.
Status: PASS
