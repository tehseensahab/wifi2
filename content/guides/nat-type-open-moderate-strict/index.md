---
title: "NAT Type Open vs. Moderate vs. Strict: What It Means"
date: 2026-11-26T05:00:00Z
description: "NAT type Open, Moderate or Strict tells you who your console can connect to. Open usually reaches anyone; Strict often only reaches Open players."
authors: ["Tehseen Arbab"]
topics: ["gaming-streaming", "how-to-fixes"]
tags: ["nat-type", "strict-nat", "moderate-nat", "open-nat", "xbox", "playstation", "upnp", "port-forwarding", "double-nat", "gaming"]
summary: "Your NAT type describes how easily other players can reach your console or PC through your router. Microsoft's Xbox multiplayer networking documentation says Open NAT can usually connect to any player, Moderate to Open or Moderate players, and Strict frequently has problems unless the other player is on Open. PlayStation shows a similar scale as Type 1, 2 and 3; game publishers' support pages say Type 1 or 2 is what to aim for."
imageAlt: "Three Xbox wireless controllers, one black and two white, lying side by side on a wooden slatted shelf"
imageCredit: "Photo: Abhinav Bhardwaj / [Unsplash](https://unsplash.com/photos/a-group-of-game-controllers-PiIlL3byFLE)"
takeaways:
  - "Open: Microsoft says players with Open NAT 'can usually connect to any other player.'"
  - "Moderate: usually connects to players on Open or Moderate NAT (Microsoft); Activision says it can't connect to players on Strict."
  - "Strict: 'frequently' has connection problems unless the other player is on Open NAT, per Microsoft. Expect trouble joining friends, hosting or using in-game chat."
  - "PlayStation uses Type 1, 2 and 3 for roughly the same scale; Activision maps them to Open, Moderate and Strict. Type 1 or 2 is fine for most players."
  - "Common fixes, in order: turn on UPnP (eero, NETGEAR), avoid two routers in a row (NETGEAR prefers bridge mode over DMZ), then forward ports (eero)."
faq:
  - q: "Is Moderate NAT bad?"
    a: "Not for most games. Moderate NAT can usually connect to Open and Moderate players. The limit is players on Strict NAT: Activision says Strict NATs can only connect with players using Open NAT, so a Strict player usually can't connect with you on Moderate."
  - q: "What is the best NAT type for gaming?"
    a: "Open (Type 1 on PlayStation's numbering in Activision's mapping). Activision says an Open/Type 1 NAT 'will provide the best connection quality.' On PlayStation, Team17 calls Type 2 'ideal' for online gaming, and NETGEAR counts both Type 1 and Type 2 as an open NAT."
  - q: "Does NAT type affect ping or download speed?"
    a: "It doesn't change your internet plan's download speed. It affects whether other players can connect to you, which can show up as failed joins, long lobby waits or no party chat. Activision says port forwarding 'can improve connection speed, lobby wait times, and overall gameplay, particularly for a host.'"
  - q: "Is it safe to turn on UPnP to fix Strict NAT?"
    a: "eero recommends it as the first fix, and NETGEAR says UPnP is on by default on its gaming routers and should stay on in most cases. It does let devices open ports on their own, which is a trade-off; our guide to disabling WPS and UPnP covers when that matters."
  - q: "Why is my NAT still Strict after turning on UPnP?"
    a: "A frequent cause is double NAT: two routers in a row, such as an ISP gateway plus your own router. NETGEAR advises putting the ISP device in modem or bridge mode rather than using DMZ; port forwarding is the other route. If your ISP uses carrier-grade NAT (CGNAT), router settings alone generally can't make you Open."
sources:
  - title: "XboxLiveNetworkAccessKind Enum"
    publisher: "Microsoft Learn"
    url: "https://learn.microsoft.com/en-us/uwp/api/windows.networking.xboxlive.xboxlivenetworkaccesskind?view=winrt-26100"
    date: 2023-05-10
  - title: "Port Forward and NAT FAQ"
    publisher: "Activision Support"
    url: "https://support.activision.com/articles/en_US/FAQ/Port-Forward-and-NAT-FAQ"
    date: 2019-11-21
  - title: "How do I fix Xbox NAT issues with eero?"
    publisher: "eero"
    url: "https://eero.com/support/articles/how-do-i-fix-xbox-nat-issues-with-eero"
  - title: "Updated NAT Guide for XR Routers"
    publisher: "NETGEAR"
    url: "https://www.netgear.com/hub/network/updated-nat-guide-for-xr-routers/"
    date: 2025-06-18
  - title: "NAT Types Explained"
    publisher: "Team17 Support"
    url: "https://support.team17.com/en/articles/318456-nat-types-explained"
    date: 2025-05-12
  - title: "Someone told me to change my NAT Type for my PlayStation"
    publisher: "The Behemoth Support"
    url: "https://support.thebehemoth.com/hc/en-us/articles/205462745-Someone-told-me-to-change-my-NAT-Type-Network-Settings-or-Ports-for-my-PlayStation-Can-you-help"
---

**Your NAT type tells you how easily other players can reach your console or PC through your router. Open NAT can usually connect to anyone, Moderate NAT can usually connect to Open and Moderate players, and Strict NAT frequently has trouble connecting to anyone not on Open NAT.** That's how Microsoft describes the three types in its Xbox multiplayer networking documentation. If you see Strict, expect trouble joining friends, hosting matches or using in-game chat; if you see Moderate, you can usually still connect to most players.

PlayStation shows a similar scale as NAT Type 1, 2 or 3. Activision maps those to Open, Moderate and Strict, though sources differ on labels: NETGEAR counts both Type 1 and Type 2 as an open NAT.

## What each NAT type means

As general background: your router uses network address translation (NAT) to share one public IP address among the devices in your home. Unsolicited traffic from the internet, such as another player trying to start a peer-to-peer session with you, has to find its way through that translation. Your NAT type is your console's report on how well that works.

| Xbox / PC | PlayStation (Activision's mapping) | Who you can connect to |
|---|---|---|
| Open | Type 1 | Usually any other player |
| Moderate | Type 2 | Usually players on Open or Moderate |
| Strict | Type 3 | Often only players on Open |

The connection column follows Microsoft's definitions for its Xbox Live multiplayer networking API (and Activision's mapping of PlayStation types):

- **Open:** "Players behind these network address translation (NAT) types can usually connect to any other player."
- **Moderate:** "Players behind these NAT types can usually connect to others behind **Open** or **Moderate** types."
- **Strict:** "Players behind this NAT type frequently experience connectivity problems with others unless those players are behind **Open** type devices."

Activision's support FAQ puts it more bluntly: "Strict/Type 3 NATs can only connect with gaming consoles or PCs using Open/Type 1 NAT," and "an Open/Type 1 NAT will provide the best connection quality."

Note the hedges in Microsoft's wording ("usually," "frequently"). NAT type predicts trouble; it doesn't guarantee it.

### What about PlayStation Type 2?

Type 2 is a common result for a PlayStation connected through a home router; The Behemoth describes it as "connected to the Internet via a router." Team17's support guide calls NAT Type 2 "ideal when setting up your PlayStation for online gaming," and The Behemoth's support page tells players to "make sure your NAT is type 1 or 2." Type 1, per The Behemoth, means "connected directly to the Internet," which is unusual for home setups. Type 3 is the one to fix: Team17 warns that with it, "it is unlikely you will be able to host any lobbies or connect via in-game chat or VoIP."

## What Strict or Moderate NAT feels like

Typical symptoms are connection failures, not slow downloads:

- You can't join a specific friend's game or party, but can join others.
- You can't host a lobby, or matchmaking takes much longer.
- Voice chat works with some players and not others.

NAT type doesn't change your download speed. If games connect but play badly, see our guide to [high ping on Wi-Fi](/guides/high-ping-on-wifi/) instead.

## How to move from Strict to Moderate or Open

Work through these in order. Each step solves a more stubborn cause.

### 1. Check that UPnP is on

UPnP lets your console ask the router to open the ports a game needs. eero says, "If your Xbox shows a 'Strict' or 'Moderate' NAT type, UPnP will resolve most connection problems." In the eero app it's under **Settings > Advanced networking > UPnP**. NETGEAR says that on its gaming routers "UPnP will be enabled" by default and "you should keep this enabled in most cases."

UPnP is a trade-off, since devices on your network can open ports through it without asking you. Our [WPS and UPnP guide](/guides/should-you-disable-wps-and-upnp/) explains when to leave it on.

After changing it, restart the console and run its network test again.

### 2. Remove double NAT

If you have an ISP gateway (a modem with its own router) and your own router or mesh system behind it, your traffic is translated twice, and UPnP on your router generally can't open ports on the ISP's box. NETGEAR's advice is to check whether the ISP device has "Modem or Bridge Mode as this is preferable over DMZ mode." Our guide to [bridge mode and double NAT](/guides/bridge-mode-double-nat-own-router/) walks through it.

### 3. Forward ports to the console

If UPnP doesn't get you there, open the ports by hand. eero's Xbox list is:

- UDP: 88, 500, 3544, 4500
- TCP: 80
- UDP and TCP: 3074, 53

eero says to "set an IP reservation for your Xbox, then forward each port," so the forwarding rule keeps pointing at the right device. Games and PlayStation use different ports; check the game publisher's support page. Our [port forwarding guide](/guides/how-to-set-up-port-forwarding/) covers the steps for most routers.

### 4. Check for CGNAT

Some ISPs put many customers behind carrier-grade NAT. Then the address on your router's WAN page isn't a public one, and router settings alone can't make your NAT Open. See [What is CGNAT?](/guides/what-is-cgnat/) for how to tell and what your options are.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Definitions of Open, Moderate and Strict NAT (hedged: "usually," "frequently") | [Microsoft Learn, XboxLiveNetworkAccessKind](https://learn.microsoft.com/en-us/uwp/api/windows.networking.xboxlive.xboxlivenetworkaccesskind?view=winrt-26100) | Verified (scoped to the Xbox Live Multiplayer Networking API; updated 2023) |
| Open/Moderate/Strict = Type 1/2/3; Strict/Type 3 connects only to Open/Type 1; Open gives best connection quality; port forwarding can improve lobby wait times | [Activision Port Forward and NAT FAQ](https://support.activision.com/articles/en_US/FAQ/Port-Forward-and-NAT-FAQ) | Verified |
| UPnP resolves most Strict/Moderate Xbox NAT problems; app path; Xbox port list; IP reservation | [eero support](https://eero.com/support/articles/how-do-i-fix-xbox-nat-issues-with-eero) | Verified |
| UPnP on by default and should stay on; prefer modem/bridge mode over DMZ; PS4 Type 1 or 2 = open NAT | [NETGEAR NAT guide for XR routers](https://www.netgear.com/hub/network/updated-nat-guide-for-xr-routers/) | Verified (NETGEAR gaming routers) |
| PlayStation Type 2 "ideal"; Type 3 unlikely to host lobbies or use in-game chat | [Team17 NAT Types Explained](https://support.team17.com/en/articles/318456-nat-types-explained) | Verified |
| Type 1 = connected directly to the internet; aim for Type 1 or 2 | [The Behemoth support](https://support.thebehemoth.com/hc/en-us/articles/205462745-Someone-told-me-to-change-my-NAT-Type-Network-Settings-or-Ports-for-my-PlayStation-Can-you-help) | Qualified (game publisher summarizing PlayStation documentation) |
| How NAT, double NAT and CGNAT work in general | General background; see our [CGNAT](/guides/what-is-cgnat/) and [double NAT](/guides/bridge-mode-double-nat-own-router/) guides | Qualified (general explanation) |
