---
title: "Starlink Bypass Mode: How to Use Your Own Router or Mesh"
date: 2026-11-14
description: "Starlink bypass mode turns off the Starlink router so your own router or mesh takes over. How to turn it on, what stops working, and how to undo it."
authors: ["Tehseen Arbab"]
topics: ["internet-plans-isps", "mesh-wifi"]
tags: ["starlink", "bypass-mode", "mesh-wifi", "double-nat", "router-settings"]
summary: "Bypass mode switches off the Starlink router's Wi-Fi and routing so a third-party router or mesh system runs your home network. You turn it on in the Starlink app under Settings, and the only way to turn it off again is a factory reset of the Starlink router. Kits that ship with a separate power supply don't need it: you plug your own router straight in."
imageAlt: "Satellite dish mounted on the side of a building against the sky"
imageCredit: "Photo: Rasta Gubaz / [Unsplash](https://unsplash.com/photos/-NWGWmcEwi4)"
takeaways:
  - "Starlink says bypass mode turns off the Starlink router so a third-party router connects directly, and that the Starlink router's Wi-Fi is completely disabled while it is on."
  - "You enable it in the Starlink app under Settings. The app can't switch it back off: Starlink says leaving bypass mode takes a factory reset."
  - "Gen 2 (Standard Actuated) kits need Starlink's Ethernet adapter first. Gen 3 routers have Ethernet ports on the back."
  - "Bypass mode is optional. You can also leave the Starlink router running and set your mesh system to access point mode, which TP-Link documents for Deco."
faq:
  - q: "What does Starlink bypass mode do?"
    a: "It turns off the Starlink router's Wi-Fi and routing so a third-party router connected by Ethernet runs the network. Starlink's help center says the Starlink router's Wi-Fi features are completely disabled while bypass mode is on."
  - q: "How do I turn on bypass mode on Starlink?"
    a: "Connect your own router to the Starlink router by Ethernet, open the Starlink app, go to Settings, choose Bypass Mode and enable it. On a Gen 3 router a violet light shows that bypass mode is active."
  - q: "How do I turn off Starlink bypass mode?"
    a: "Factory reset the Starlink router. Starlink's help center says the app cannot turn bypass mode off, so a reset is the only way back to the Starlink router's own Wi-Fi."
  - q: "Do I need bypass mode to use a mesh system with Starlink?"
    a: "No. You can leave the Starlink router running and put the mesh system in access point mode, which TP-Link documents for its Deco systems. Bypass mode is the cleaner choice when you want your own router to handle everything, because it avoids two routers in a row."
  - q: "Does Starlink mesh work in bypass mode?"
    a: "Not together with another brand. Starlink's mesh help text says Starlink Mesh cannot form a mesh network with third-party routers or mesh nodes, and in bypass mode the Starlink router's own Wi-Fi is off. Use your third-party system's own nodes for coverage."
sources:
  - title: "What is bypass mode?"
    publisher: "Starlink Help Center"
    url: "https://starlink.com/support/article/a0fe8d51-32f7-d2b9-d74a-801e31ad9f6a"
  - title: "Can I add a third-party router or mesh system? (Philippines-language edition)"
    publisher: "Starlink Help Center"
    url: "https://starlink.com/ph/support/article/a206a55c-0597-2d06-1408-dea7dcf24221"
  - title: "Gen 3 Router Setup Guide (Standard)"
    publisher: "Starlink"
    url: "https://api.starlink.com/public-files/Gen3RouterSetupGuideStandardGen1.pdf"
  - title: "What is Starlink Mesh? (Starlink help text)"
    publisher: "Satellite Phone Store support center"
    url: "https://support.satellitephonestore.com/hc/en-us/articles/36861846823956-Starlink-Mesh-Routers"
    date: 2025-04-24
  - title: "How do I set up my Orbi WiFi System with Starlink?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/000065995/How-do-I-set-up-my-Orbi-WiFi-System-with-Starlink"
    date: 2026-10-22
  - title: "How to Connect Your TP-Link Deco Mesh System to Starlink"
    publisher: "TP-Link"
    url: "https://www.vigi.com/eg/support/faq/3647/"
    date: 2026-04-28
  - title: "How to setup ASUS router to work with Starlink"
    publisher: "ASUS"
    url: "https://www.asus.com/us/support/FAQ/1047774/"
    date: 2024-07-22
  - title: "How to Bypass the Starlink Router"
    publisher: "DishyTech"
    url: "https://www.dishytech.com/how-to-bypass-the-starlink-router/"
    date: 2025-08-12
---

Starlink bypass mode turns off the Starlink router's Wi-Fi and routing so that your own router or mesh system runs the home network. You switch it on in the Starlink app under Settings. Getting out of it takes a factory reset of the Starlink router, so decide before you flip it.

This is an explainer built from Starlink's help center and setup guide and from router makers' Starlink instructions. We have not tested these setups on a Starlink connection.

*This page replaces a short news item published on September 30, 2026 about a Starlink firmware update. We could not verify that update from Starlink's own documentation, so we removed the claim and rewrote the page from sources we could check.*

## What does Starlink bypass mode do?

Bypass mode hands the network to a third-party router. Starlink's help center says it lets you turn off the Starlink router and connect a third-party router directly to Starlink, and that the Starlink router's "WiFi features are completely disabled" once it is active.

In practice that means:

- Your own router gives out addresses, runs the firewall and broadcasts Wi-Fi.
- The Starlink router's network name disappears.
- You manage Wi-Fi settings in your own router's app, not the Starlink app.

Starlink also sets expectations. Its help article on third-party routers says it cannot guarantee performance or compatibility with third-party networking equipment, and that some Starlink app features may not work as expected with one. We read that article in its Philippines-language edition, the version Starlink's site returned to us.

## Do I need bypass mode for my Starlink kit?

It depends on which hardware you have. Starlink's bypass mode article splits it this way:

| Starlink hardware | Do you need bypass mode? | How your router connects |
|---|---|---|
| Gen 3 router (Standard kit) | Yes, to turn off the Starlink router | Ethernet port on the back of the Starlink router |
| Gen 2 router (Standard Actuated kit) | Yes | Starlink's Ethernet adapter, bought separately |
| Kits with a separate power supply (Enterprise, High Performance, Flat High Performance) | No | Plug your router into the power supply |
| Gen 1 router | No | Replace the Gen 1 router with your own |

Starlink's Gen 3 setup guide shows the two Ethernet ports behind a cover on the back of the router. TP-Link's Deco instructions confirm that the Gen 2 kit has no built-in Ethernet port.

## How do I turn on bypass mode?

1. Connect your router's internet (WAN) port to the Starlink router with an Ethernet cable. On a Gen 2 kit, fit the Ethernet adapter first.
2. Open the Starlink app and go to **Settings**.
3. Choose **Bypass Mode** and slide the toggle to enable it.
4. On a Gen 3 router, look for a violet light, which Starlink says shows the router is in bypass mode.
5. Set up your own router or mesh system as you would behind any modem.

ASUS's Starlink instructions add one detail for its routers: set the internet connection type to Automatic IP.

## What stops working in bypass mode?

- **The Starlink router's Wi-Fi.** It is fully off, so anything still joined to the old network name has to move to your router's network.
- **Starlink mesh nodes alongside another brand.** Starlink's mesh help text, as republished by a reseller, says Starlink Mesh cannot form a mesh network with third-party routers or mesh nodes.
- **Possibly parts of the Starlink app.** DishyTech reports that the app shows the router as unreachable once bypass is on. If the app also loses the dish, DishyTech's fix is a static route on your own router to 192.168.100.0/24 through 192.168.100.1 on the WAN port. ASUS documents static routes for the same purpose.

Bypass mode does not change your Starlink plan or its speed. It changes which box runs the network inside your home.

## How do I turn off Starlink bypass mode?

Factory reset the Starlink router. Starlink's help center says the app cannot turn bypass off. After the reset, the router comes back with its own Wi-Fi and you set it up again in the Starlink app.

DishyTech says the Gen 3 router's reset button is on the back, between the two Ethernet ports, and that a Gen 2 router is reset by power cycling it six times in a row.

## Should I use bypass mode or access point mode?

Use bypass mode when you want your own router in full control. Use access point mode when you would rather keep the Starlink router and app as they are.

| | Bypass mode | Mesh in access point mode |
|---|---|---|
| Starlink router | Wi-Fi and routing off | Stays on and keeps routing |
| Your router or mesh | Runs the whole network | Adds Wi-Fi coverage only |
| Two routers in a row (double NAT) | Avoided | Avoided |
| Undo | Factory reset the Starlink router | Switch the mesh back in its app |
| Documented by | Starlink, NETGEAR, TP-Link, ASUS | TP-Link (for Deco) |

NETGEAR's Orbi instructions, last updated October 22, 2026, say bypass mode isn't required but recommend it to avoid potential issues. TP-Link's Deco instructions offer both routes for Gen 2 kits. Our [bridge mode and double NAT guide]({{< relref "/guides/bridge-mode-double-nat-own-router" >}}) explains why two routers in a row cause trouble.

Bypass mode will not get around carrier-grade NAT. If you need inbound connections for a game server or cameras, read our [CGNAT explainer]({{< relref "/guides/what-is-cgnat" >}}) first.

## Which router or mesh should I use with Starlink?

Any router or mesh system that takes an Ethernet internet connection can sit behind Starlink. For picks by home size and setup, see our guide to the [best mesh Wi-Fi for Starlink]({{< relref "/guides/best-mesh-wifi-for-starlink" >}}). If you are covering a big home, the [best mesh Wi-Fi for a large house]({{< relref "/guides/best-mesh-wifi-for-large-house" >}}) guide compares systems by layout.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Bypass mode turns off the Starlink router so a third-party router connects directly; Wi-Fi features are completely disabled; enabled in the app under Settings; the app cannot turn it off; exit by factory reset; violet light on Gen 3 | [Starlink Help Center](https://starlink.com/support/article/a0fe8d51-32f7-d2b9-d74a-801e31ad9f6a) | Verified as of November 14, 2026 |
| Gen 2 router needs an Ethernet adapter; kits with a power supply connect a third-party router directly; Gen 1 router is replaced directly | [Starlink Help Center](https://starlink.com/support/article/a0fe8d51-32f7-d2b9-d74a-801e31ad9f6a) | Verified as of November 14, 2026 |
| Starlink does not guarantee performance or compatibility with third-party equipment; some app features may not work as expected | [Starlink Help Center, Philippines-language edition](https://starlink.com/ph/support/article/a206a55c-0597-2d06-1408-dea7dcf24221) | Qualified: our translation of a non-English edition |
| Gen 3 router has two Ethernet ports behind a cover | [Starlink Gen 3 setup guide](https://api.starlink.com/public-files/Gen3RouterSetupGuideStandardGen1.pdf) | Verified |
| Starlink Mesh cannot mesh with third-party routers or nodes | [Starlink help text via Satellite Phone Store](https://support.satellitephonestore.com/hc/en-us/articles/36861846823956-Starlink-Mesh-Routers) | Qualified: reseller copy of Starlink help text |
| NETGEAR says bypass mode isn't necessary but recommends it for Orbi | [NETGEAR, updated October 22, 2026](https://kb.netgear.com/000065995/How-do-I-set-up-my-Orbi-WiFi-System-with-Starlink) | Verified |
| TP-Link offers bypass mode or Deco access point mode; Gen 2 has no built-in Ethernet port | [TP-Link, updated April 28, 2026](https://www.vigi.com/eg/support/faq/3647/) | Verified; covers Gen 2 kits only |
| ASUS: Automatic IP on the WAN port; static routes to keep the Starlink app working | [ASUS, updated July 22, 2024](https://www.asus.com/us/support/FAQ/1047774/) | Verified |
| App shows the router as unreachable; static route to 192.168.100.0/24; reset button location; Gen 2 reset by six power cycles | [DishyTech](https://www.dishytech.com/how-to-bypass-the-starlink-router/) | Qualified: third-party report |

## Bottom line

Use bypass mode when you want your own router or mesh system to run everything behind Starlink, and accept that undoing it means a factory reset. If you only want more coverage and are happy with the Starlink app, leave bypass off and run your mesh system in access point mode.
