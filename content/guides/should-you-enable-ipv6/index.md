---
title: "Should You Enable IPv6 on Your Router?"
date: 2026-10-24T05:00:00Z
description: "Should you enable IPv6 on your router? Yes, if your internet provider supports it: it runs alongside IPv4, and Microsoft advises against disabling it."
authors: ["Tehseen Arbab"]
topics: ["routers", "how-to-fixes"]
tags: ["ipv6", "ipv4", "router-settings", "eero", "google-nest-wifi", "tp-link", "netgear", "xfinity", "att"]
summary: "Yes: if your internet provider supports IPv6, turn it on in your router and leave it on. It works alongside IPv4 rather than replacing it, Google measured just over half its users reaching it over IPv6 in March 2026, and Microsoft recommends against disabling IPv6 in Windows. Turn it off only as a temporary workaround for a specific problem, and make sure your router's firewall covers IPv6."
imageAlt: "Close-up of a computer terminal on a dark screen listing DNS servers, a local IP address and a public IP address in red and white text"
imageCredit: "Photo: Cong Long Vu / [Unsplash](https://unsplash.com/photos/terminal-window-with-system-statistics-0lMetL4QQ0c)"
takeaways:
  - "IPv6 doesn't replace IPv4 on a home connection; both run side by side (dual stack). Xfinity says it will keep supporting IPv4 while it adds IPv6."
  - "Google measured 50.10% of its users reaching it over native IPv6 on March 28, 2026, according to the Internet Society."
  - "Where IPv6 is a switch, eero puts it under Settings > Advanced networking > IPv6, Google Wifi and Nest Wifi under Wifi > Settings > Advanced Networking in the Google Home app, and TP-Link Wi-Fi routers (web interface) under Advanced > IPv6."
  - "Microsoft says it doesn't recommend disabling IPv6 in Windows because some Windows components might not function."
  - "Home IPv6 networks generally don't use NAT, so your router's firewall, not address translation, is what blocks unsolicited inbound traffic. Check that it's on."
faq:
  - q: "Is IPv6 faster than IPv4?"
    a: "Sometimes, but don't enable it expecting a speed boost. Your plan's speed is the same either way. IPv6 can avoid address translation on the provider's network, and eero cites Cloudflare data that IPv6 routing made some popular websites 10-15 percent faster (eero's post is undated), but results depend on your provider and the sites you use."
  - q: "Is IPv6 less secure than IPv4 at home?"
    a: "Not if the router's IPv6 firewall is on. IPv6 gives devices addresses that are reachable from the internet in principle, so the firewall has to block unsolicited inbound connections. The IETF's RFC 6092 recommends home gateways block unsolicited inbound connections, but it also requires a pass-everything \"transparent mode\" and allows that to be the default, so check your router's IPv6 firewall setting."
  - q: "Should I disable IPv6 for gaming?"
    a: "Not as a first step. If a game or console has problems only with IPv6 on, turning it off on the router is a reasonable temporary test. If that fixes it, report it to your provider or router maker rather than leaving IPv6 off indefinitely."
  - q: "How do I know if my internet provider supports IPv6?"
    a: "Turn IPv6 on in the router, set the connection type to automatic (or the type your provider names), restart, and look for an IPv6 address or delegated prefix on the router's internet (WAN) status page or app. If none appears, ask your provider."
  - q: "What IPv6 connection type should I pick?"
    a: "Use the automatic option your router offers: TP-Link's is Dynamic IP (SLAAC/DHCPv6) with Prefix Delegation turned on, and Netgear's is Auto Detect. Choose PPPoE only if your provider uses PPPoE, and pass-through or bridge only if another router sits in front of yours."
sources:
  - title: "18 Years Later, IPv6 Reaches Majority"
    publisher: "Internet Society Pulse"
    url: "https://pulse.internetsociety.org/en/blog/2026/04/18-years-later-ipv6-reaches-majority/"
    date: 2026-04-21
  - title: "Google hits 50% IPv6"
    publisher: "APNIC Blog"
    url: "https://blog.apnic.net/2026/04/28/google-hits-50-ipv6/"
    date: 2026-04-28
  - title: "What is Internet Protocol, version 6 (IPv6)?"
    publisher: "Xfinity Support"
    url: "https://www.xfinity.com/support/articles/all-ip-xfinity-fiber-only-network"
    date: 2026-08-31
  - title: "IPv6 deployment for home networking"
    publisher: "Comcast"
    url: "https://corporate.comcast.com/comcast-voices/ipv6-deployment-2"
    date: 2012-04-25
  - title: "IPv6 and AT&T Internet services"
    publisher: "AT&T Support"
    url: "https://www.att.com/support/article/internet/KM1148998/about:blank"
    date: 2023-02-27
  - title: "What is IPv6?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/what-is-ipv6"
    date: 2026-10-24
  - title: "Introducing IPv6 support for eero networks"
    publisher: "eero Blog"
    url: "https://blog.eero.com/introducing-ipv6-support-eero-networks"
  - title: "IPv6 (Google Wifi and Nest Wifi)"
    publisher: "Google Nest Wifi Help"
    url: "https://support.google.com/wifi/answer/6361450"
    date: 2026-10-24
  - title: "How to Set Up IPv6 on TP-Link Wi-Fi Routers"
    publisher: "TP-Link"
    url: "https://www.omadanetworks.com/us/support/faq/1525/"
    date: 2026-04-23
  - title: "How do I set up an IPv6 Internet connection on my NETGEAR router?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/24006/How-do-I-set-up-an-IPv6-Internet-connection-on-my-NETGEAR-router"
    date: 2025-07-07
  - title: "Guidance for configuring IPv6 in Windows for advanced users"
    publisher: "Microsoft Learn"
    url: "https://learn.microsoft.com/ro-ro/troubleshoot/windows-server/networking/configure-ipv6-in-windows"
    date: 2026-02-12
  - title: "RFC 6092: Recommended Simple Security Capabilities in Customer Premises Equipment (CPE) for Providing Residential IPv6 Internet Service"
    publisher: "IETF / RFC Editor"
    url: "https://www.rfc-editor.org/rfc/rfc6092.html"
    date: 2011-01-01
---

Yes. If your internet provider supports IPv6, turn it on in your router and leave it on. IPv6 runs alongside IPv4 on home connections rather than replacing it, so enabling it adds a second way for your devices to reach sites that support it without taking anything away. Google's measurements first showed more than half its users reaching it over IPv6 in March 2026, and Microsoft recommends against disabling IPv6 in Windows. The two cases for turning it off are a specific problem that goes away without it, and a router whose IPv6 firewall you can't confirm is working.

## What IPv6 is, and why your router may have it switched off

IPv6 is the newer version of the Internet Protocol, the addressing system every device online uses. The older IPv4 has too few addresses for every device: Xfinity's support page notes that the global free pool of IPv4 addresses ran out in early 2011. IPv6 has, in Xfinity's words, "a pool of nearly unlimited IP addresses."

The switch is gradual. Xfinity says both protocols will run side by side for years and that it will keep supporting IPv4 while adding IPv6. Google's measure of users reaching it over IPv6 passed the halfway point this year: the Internet Society reported 50.10% on March 28, 2026, and APNIC's blog marked the milestone in April.

On a home network, that means dual stack: each device has an IPv4 address and one or more IPv6 addresses, and uses whichever works for the site it is reaching. If your router has IPv6 turned off, everything still works over IPv4; you just aren't using IPv6 where it's available.

Makers' help pages often don't say whether IPv6 is on out of the box; eero and Google both describe it as a setting you switch on, without stating the default.

## Does your internet provider support it?

Your router can only offer IPv6 to devices if your provider assigns it. Among the largest US providers:

- **Xfinity (Comcast)** began rolling out IPv6 for home networks in 2012 and its current support page says it supports IPv6 alongside IPv4.
- **AT&T** says that with IPv6-capable equipment, "In most cases, your devices and apps will use IPv6 without any extra action," and lists its BGW320, BGW210, NVG599 and NVG510 gateways as IPv6-capable. That page was last updated February 27, 2023. If you use your own router behind AT&T's gateway, AT&T says to check with the router's manufacturer for IPv6 compatibility.

For other providers, the quickest check is to turn IPv6 on in your router and see whether it gets an address, as below.

## How to turn on IPv6

Menu names vary by brand and firmware version; these are the makers' current instructions.

### eero

In the eero app, go to **Settings > Advanced networking > IPv6** and tap the toggle. eero says your network restarts automatically when you change it, so expect a short drop. Global IPv6 addresses depend on your provider supporting them, and eero's blog says IPv6 works in both Gateway and Bridge mode.

### Google Wifi and Nest Wifi

In the Google Home app, open **Favorites > Wifi > Settings > Advanced Networking**, turn on **IPv6** and tap **Save**. Google's help page lists several limits:

- Your provider must also supply IPv4; Google's routers don't support IPv6-only connections.
- They don't support transition protocols such as 6to4 or 6rd.
- Background connection tests can switch IPv6 off if the provider's IPv6 isn't working reliably, and try to restore it later.
- If your provider hands out only a /64 prefix, IPv6 won't be available on the guest network.

### TP-Link Wi-Fi routers

These steps are for TP-Link routers managed in a web browser; Deco mesh systems use the Deco app, whose menus differ. Log in at tplinkwifi.net and go to **Advanced > IPv6**, then turn on the IPv6 toggle. TP-Link offers four connection types: **Dynamic IP (SLAAC/DHCPv6)**, which it says is often used by cable providers, with "Get IPv6 Connection" set to Auto and Prefix Delegation enabled; **PPPoE**, if your provider uses it; **Pass-Through (Bridge)**, if another router sits in front of the TP-Link; and **Static IP**, if your provider gave you a fixed IPv6 address.

### Netgear

These steps are for Netgear routers managed in a web browser; Orbi and Nighthawk app menus differ. Log in at routerlogin.net and go to **ADVANCED > Advanced Setup > IPv6**. If you don't know your provider's connection type, Netgear says to choose **Auto Detect**. Netgear also offers a **6to4 Tunnel** for providers without IPv6; on a connection that has native IPv6, use Auto Detect or your provider's type instead.

### Check that it worked

After the router restarts, look on its internet (WAN) status page or in its app for an IPv6 address or delegated prefix. eero shows them under each eero's **IP addresses** screen, and per device in the Devices list. If no IPv6 address appears, your provider may not offer it on your plan or in your area; ask them before changing other settings.

## Is IPv6 safe to turn on?

Yes, with one thing to check. Home IPv6 networks generally don't use NAT; Google's help page notes that "IPv6 networks don't use NAT for port forwarding." Under IPv4, NAT has the side effect of hiding devices behind one public address. With IPv6, each device can have its own public address, so the router's firewall is what stops unsolicited inbound connections.

The IETF's RFC 6092, an informational guide for home gateways published in January 2011, says unsolicited inbound transport traffic should not be forwarded into the home network unless an inside device asked for it. The same document also tells gateways to offer a "transparent mode" that passes all inbound traffic and allows that mode to be the default. So look for an IPv6 firewall setting in your router and make sure it's on. On many routers, opening IPv6 ports for a game or a server is a separate setting from IPv4 port forwarding.

Our [router hardening checklist](/guides/router-hardening-checklist/) covers the other settings worth checking while you're in there.

## When turning IPv6 off makes sense

Turning IPv6 off on the router is a reasonable short-term test if a site, app, game or device fails only when IPv6 is on. If that fixes it, the cause is usually your provider's IPv6 service or a firmware bug, so report it and plan to turn IPv6 back on once it's fixed.

Don't disable it inside Windows. Microsoft says, "We don't recommend that you disable IPv6 or IPv6 components or unbind IPv6 from interfaces. If you do, some Windows components might not function." Its advice for people who want IPv4 used first is the "Prefer IPv4 over IPv6" prefix-policy setting instead.

If a slow or unreliable connection is what sent you here, IPv6 is unlikely to be the cause in most homes. Start with [why your Wi-Fi is slow when your internet is fast](/guides/wifi-slow-but-internet-fast/), and if you've recently changed DNS servers, see [our DNS guide](/guides/change-router-dns-settings/) for setting IPv6 DNS to match.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| 50.10% of users reached Google over native IPv6 on March 28, 2026 | [Internet Society Pulse](https://pulse.internetsociety.org/en/blog/2026/04/18-years-later-ipv6-reaches-majority/) | Verified |
| Google's measurement passed 50% (graph as of April 23, 2026) | [APNIC Blog](https://blog.apnic.net/2026/04/28/google-hits-50-ipv6/) | Verified |
| Xfinity supports IPv4 while adding IPv6; IPv4 free pool ran out in early 2011 | [Xfinity Support](https://www.xfinity.com/support/articles/all-ip-xfinity-fiber-only-network) | Verified |
| Comcast began rolling out IPv6 for home networking in 2012 | [Comcast](https://corporate.comcast.com/comcast-voices/ipv6-deployment-2) | Verified |
| AT&T: IPv6 used without extra action on IPv6-capable equipment; gateway models | [AT&T Support](https://www.att.com/support/article/internet/KM1148998/about:blank) | Qualified (page last updated February 27, 2023) |
| eero menu path, restart, ISP requirement | [eero Support](https://eero.com/support/articles/what-is-ipv6) | Verified |
| Google Wifi/Nest Wifi menu path and limits | [Google Nest Wifi Help](https://support.google.com/wifi/answer/6361450) | Verified |
| TP-Link and Netgear menu paths and connection types | [TP-Link](https://www.omadanetworks.com/us/support/faq/1525/), [NETGEAR](https://kb.netgear.com/24006/How-do-I-set-up-an-IPv6-Internet-connection-on-my-NETGEAR-router) | Verified |
| Microsoft recommends not disabling IPv6; prefer IPv4 over IPv6 instead | [Microsoft Learn](https://learn.microsoft.com/ro-ro/troubleshoot/windows-server/networking/configure-ipv6-in-windows) | Verified |
| RFC 6092 inbound filtering guidance and transparent mode | [RFC 6092](https://www.rfc-editor.org/rfc/rfc6092.html) | Verified |
