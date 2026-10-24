# Fact-check record: should-you-enable-ipv6

Article: content/guides/should-you-enable-ipv6/index.md
Byline: Tehseen Arbab (owner removed John Marshall and Craig Leslie as invented authors on 2026-10-22; daily prompt bylines not used)
Research date: 2026-10-24 (UTC)
Search Console query targeted: none confirmed (GSC Wizard returned payment_required); new explainer (no IPv6 post in INDEX.md)

## Research log (exact claim | source | date)
1. Internet Society Pulse, published 2026-04-21: "50.10% on 28 March 2026" native IPv6 access to Google | https://pulse.internetsociety.org/en/blog/2026/04/18-years-later-ipv6-reaches-majority/
2. APNIC Blog, George Michaelson, 2026-04-28: Google IPv6 reached 50% for first time; graph as at 23 April 2026; metric = proportion of users accessing Google over IPv6 | https://blog.apnic.net/2026/04/28/google-hits-50-ipv6/
3. Xfinity support "What is IPv6?" (published 2025-04-16, modified 2026-08-31): "IPv6 is supposed to replace the old version, IPv4"; "a pool of nearly unlimited IP addresses"; both run side by side for years; IANA ran out of global IPv4 free pool early 2011; Xfinity keeps supporting IPv4 while adding IPv6 | https://www.xfinity.com/support/articles/all-ip-xfinity-fiber-only-network
4. Comcast corporate, Jason Livingood, 2012-04-25: production rollout of IPv6 home networking support; dual stack | https://corporate.comcast.com/comcast-voices/ipv6-deployment-2
5. AT&T KM1148998 (updated 2023-02-27): "In most cases, your devices and apps will use IPv6 without any extra action"; BGW320, BGW210, NVG599, NVG510 IPv6-capable; third-party equipment: contact manufacturer. Page title references DSL. | https://www.att.com/support/article/internet/KM1148998/about:blank
6. eero "What is IPv6?": Settings > Advanced networking > IPv6 toggle; network restarts; global IPv6 requires ISP support; IP addresses screen per eero and device; default state not stated | https://eero.com/support/articles/what-is-ipv6
7. eero blog (undated): IPv6 works in Gateway or Bridge mode; cites Cloudflare: IPv6 routing made websites 10-15 percent faster | https://blog.eero.com/introducing-ipv6-support-eero-networks
8. Google Wifi help 6361450: Favorites > Wifi > Settings > Advanced Networking > IPv6 > Save; ISP, devices, OS, apps must support; no IPv6-only; no 6to4/6rd; background tests may disable IPv6; /64 prefix -> no guest IPv6; "IPv6 networks don't use NAT for port forwarding" | https://support.google.com/wifi/answer/6361450
9. TP-Link FAQ 1525 (updated 2026-04-23): tplinkwifi.net, Advanced > IPv6 toggle; Dynamic IP (SLAAC/DHCPv6) Auto + Prefix Delegation, often cable ISPs; PPPoE; Pass-Through (Bridge); Static IP | https://www.omadanetworks.com/us/support/faq/1525/
10. Netgear KB 24006 (updated 2025-07-07): routerlogin.net, ADVANCED > Advanced Setup > IPv6; Auto Detect if unsure; 6to4 Tunnel if ISP lacks IPv6 | https://kb.netgear.com/24006/How-do-I-set-up-an-IPv6-Internet-connection-on-my-NETGEAR-router
11. Microsoft Learn configure-ipv6-in-windows (updated 2026-02-12): "We don't recommend that you disable IPv6 or IPv6 components or unbind IPv6 from interfaces. If you do, some Windows components might not function."; recommends "Prefer IPv4 over IPv6" prefix policies | https://learn.microsoft.com/ro-ro/troubleshoot/windows-server/networking/configure-ipv6-in-windows
12. RFC 6092 (January 2011, Informational): section 2.3 unsolicited inbound transport traffic not forwarded unless solicited; REC-49 transparent mode MAY be default | https://www.rfc-editor.org/rfc/rfc6092.html

## Fact-check result (independent subagent, 2026-10-24)
Verified (13): ISOC 50.10% on 2026-03-28; APNIC 50% milestone; Xfinity quotes and 2011 IPv4 exhaustion; Comcast 2012 rollout; AT&T quote and gateway models (page dated 2023-02-27, kept Qualified); eero menu path, restart, ISP dependency, Gateway/Bridge; Google Wifi path and limits and NAT quote; TP-Link FAQ 1525 types; Netgear KB 24006; Microsoft quote and Prefer IPv4 advice; RFC 6092 section 2.3 and REC-49; FAQ connection-type answer.
Qualified -> fixed (10): description no longer says turning IPv6 off "rarely fixes anything"; "just over half" -> first passed half in March 2026; "the internet passed halfway" -> Google's measure; eero/Cloudflare claim limited to "some popular websites" and post undated; RFC 6092 FAQ answer now says transparent mode may be the default; "IPv6 doesn't use NAT" -> "Home IPv6 networks generally don't use NAT"; TP-Link and Netgear steps scoped to web-interface routers (Deco/Orbi app menus differ); default-on claim reworded; IPv6 port-forwarding line softened; "rarely the cause" softened.
Not verified: none.
Note: Microsoft source is the ro-ro Learn URL (article body in English); no en-us Learn URL came back in search. support.microsoft.com/kb/929852 is the legacy English KB link but was not fetched, so it was not substituted.
Image: Unsplash photo by Cong Long Vu (0lMetL4QQ0c), viewed before use: terminal on a dark screen listing DNS, local IP and public IP lines. Original 2400x3600 portrait, cropped to 2400x1500 landscape around the network lines.
Status: PASS
