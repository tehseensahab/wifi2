---
title: "Bridge Mode and Double NAT: Own Router With an ISP Gateway"
date: 2026-10-12
description: "Plugging your own router or mesh into a provider gateway can create double NAT. What that means, when it matters, and how bridge or AP mode fixes it."
authors: ["Tehseen Arbab"]
topics: ["routers", "how-to-fixes"]
tags: ["bridge-mode", "double-nat", "access-point-mode", "isp-gateway", "mesh-wifi", "nat"]
summary: "If you plug your own router or mesh system into your internet provider's gateway, both devices may route traffic, which is called double NAT. It often works fine for browsing, but can cause console NAT warnings and confusing settings. The usual fix is to put the provider's gateway in bridge mode so only your router routes. If the gateway can't be bridged, put your own router in access point mode instead."
imageAlt: "Gray Ethernet cable with an RJ45 plug on a light gray background"
imageCredit: "Photo: Claudio Schwarz / [Unsplash](https://unsplash.com/photos/w0aMCZIW6Qc)"
takeaways:
  - "NAT (Network Address Translation) lets your devices share one public internet address. Double NAT means two routers in a row are each doing it."
  - "Xfinity says bridge mode turns off its gateway's routing and leaves the modem on, so your own router takes over. Only one device can be connected to the gateway in bridge mode."
  - "Netgear, TP-Link and eero all recommend bridging a provider's modem-router combo when you add their router or mesh. If that isn't possible, Netgear says to turn off the gateway's Wi-Fi and put its router in AP mode."
  - "Bridging costs features. Xfinity says you lose network management and its WiFi Extenders, and eero says its advanced features stop working when the eero itself is bridged."
faq:
  - q: "What is double NAT?"
    a: "It is when two routers in a row both perform Network Address Translation, creating two separate home networks. It usually happens when you plug your own router into a provider gateway that is still acting as a router."
  - q: "Is double NAT bad?"
    a: "Often it causes no visible problem for browsing and streaming. It can cause trouble with game consoles, which may report a double NAT warning, and with features that need devices to reach each other or accept incoming connections. TP-Link says it can cause connectivity and performance issues."
  - q: "What is the difference between bridge mode and access point mode?"
    a: "Bridge mode usually refers to the provider's gateway: it turns off its router so it acts only as a modem. Access point (AP) mode usually refers to your own router or mesh: it turns off its routing so it only provides Wi-Fi, leaving the gateway in charge. Use one or the other, not both."
  - q: "What do I lose with bridge mode on an Xfinity gateway?"
    a: "Xfinity says you can still use its app to manage your account, but you can't manage and personalize your network or use WiFi Extenders, and Xfinity CyberSecure isn't available. If you already activated WiFi Extenders, you can't enable bridge mode."
  - q: "How do I know if I have double NAT?"
    a: "Look at your router's internet (WAN) address in its app or admin page. If it starts with 192.168., 10. or 172.16. to 172.31., it is receiving a private address from another router, which usually means double NAT. Xbox consoles also report Double NAT detected in their network settings."
sources:
  - title: "Use Bridge Mode on your wireless gateway"
    publisher: "Xfinity Support"
    url: "https://www.xfinity.com/support/articles/wireless-gateway-enable-disable-bridge-mode"
  - title: "What is NAT?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/what-is-nat"
  - title: "What is bridge mode?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/what-is-bridge-mode"
  - title: "How do I fix problems caused by my NETGEAR Orbi or Nighthawk router connected to an ISP gateway?"
    publisher: "Netgear Support"
    url: "https://kb.netgear.com/000033729/"
  - title: "Does Deco Work with an Existing Router?"
    publisher: "TP-Link Support"
    url: "https://www.tp-link.com/us/support/faq/1432/"
  - title: "Troubleshoot NAT errors and multiplayer game issues"
    publisher: "Xbox Support"
    url: "https://support.xbox.com/en-US/help/hardware-network/connect-network/xbox-one-nat-error"
  - title: "RFC 1918: Address Allocation for Private Internets"
    publisher: "Internet Engineering Task Force"
    url: "https://www.rfc-editor.org/rfc/rfc1918"
    date: 1996-02-01
---

When you plug your own router or mesh system into the gateway your internet provider supplied, you can end up with two routers doing the same job, which is called double NAT. It often goes unnoticed, but it can trigger game console warnings and make some features misbehave. The fix is to let only one device route: put the provider's gateway in bridge mode, or, if it can't be bridged, put your own router in access point mode.

This is a how-to based on Xfinity, eero, Netgear and TP-Link support documentation. We have not tested these setups ourselves, and menu names vary between models.

## What is double NAT?

NAT stands for Network Address Translation. Your internet provider gives your home one public address. Your router hands each device a private address, and NAT translates between the two so all your devices can share the connection. Eero describes it as a way for several devices to share one public IP address.

A provider gateway is a single box that combines a modem and a router. If you connect your own router behind it, and both keep routing, traffic is translated twice: that is double NAT. Eero describes it as two routers performing NAT, which creates two separate networks.

## Does double NAT cause problems?

Sometimes. Web browsing, streaming and video calls usually work, because those connections start from your device. Problems show up with things that need devices to reach each other or accept connections from outside:

- **Game consoles.** Xbox support lists "Double NAT detected" as one of the errors that can stop party chat and multiplayer from working.
- **Two networks with the same name.** Eero warns that running two networks with the same Wi-Fi name at once "will lead to technical complications." Devices can join the gateway's Wi-Fi and lose sight of devices on yours.
- **General reliability.** TP-Link says double NAT can cause "connectivity and performance issues."
- **Port forwarding.** With two routers, a port has to be opened on both, which is easy to get wrong.

Eero also points out that double NAT has one upside: it lets you set up a new system quickly without changing the provider's equipment. Some setups start that way and fix it afterward.

## How do I check whether I have double NAT?

Open your own router's app or admin page and find its internet (WAN) address. If it begins with **192.168.**, **10.** or anything from **172.16.** to **172.31.**, your router is getting a private address from the device in front of it, which usually means double NAT. Those three ranges are reserved for private networks by RFC 1918, the internet standard that defines them. Treat this as a strong hint rather than proof: some providers run their own network-level NAT, which can also leave your router without a public address.

On an Xbox, Xbox support says the NAT type and any "Double NAT detected" message appear under Profile & system, Settings, General, Network settings.

## How do I fix it: bridge mode or access point mode?

Pick one device to do the routing.

| Option | What you change | Best when | What you give up |
|---|---|---|---|
| Bridge mode on the provider's gateway | The gateway stops routing and acts only as a modem; your router takes over | The gateway supports it and you don't need its extra features | The gateway's network features, such as its app controls and extenders |
| Access point mode on your router or mesh | Your router stops routing and only provides Wi-Fi; the gateway keeps routing | The gateway can't be bridged | Some of your router's features, which manufacturers disable in AP mode |
| Leave double NAT in place | Nothing | Everything already works and you don't game online | Possible console warnings and port-forwarding hassle |

The router makers' own guidance leans toward bridging the gateway:

- **Eero** recommends putting the modem-router combo in bridge mode for the best performance and access to all eero features.
- **TP-Link** recommends bridge mode on a combined modem-router to avoid double NAT when adding Deco.
- **Netgear** prefers bridge mode on the provider gateway. If that isn't possible, it says "you must turn its WiFi off and put your Orbi or Nighthawk router in AP mode," and notes that "some router features are disabled in AP mode."

## How do I put an Xfinity gateway in bridge mode?

Xfinity documents these steps for its gateways:

1. On a device connected to your home network, go to the Admin Tool at **http://10.0.0.1**. You may need to allow Admin Tool access in the Xfinity app first.
2. Sign in with the username **admin** and the password on the sticker on the gateway, unless you changed it.
3. Go to **Gateway**, then **At a Glance**.
4. Next to **Bridge Mode**, click **Enable**, then **OK** at the warning. The gateway may restart.
5. Connect your own router to any Ethernet port on the gateway.

Things Xfinity says to know first:

- Only one device can be connected to the gateway while it is in bridge mode.
- You can still use the Xfinity app to manage your account, but not to manage and personalize your network or use WiFi Extenders.
- Xfinity CyberSecure isn't available in bridge mode, and you can't enable bridge mode if you have already activated WiFi Extenders.
- Bridge mode doesn't turn off the Xfinity WiFi Home Hotspot feature on gateways that have it.
- To turn bridge mode off later, the device you use must be connected to the gateway by Ethernet.

Other providers' gateways may work differently. Check your provider's help pages.

## When would I bridge my own router instead?

Usually, you wouldn't; it's the provider's gateway you bridge. But eero lists cases where its own system may need to be bridged and the provider's equipment kept as the router: if your provider is AT&T U-verse and its equipment provides Wi-Fi and addressing, if your provider requires PPPoE (a login-based connection type), or if your provider requires a specific MAC address that matches its own equipment. Eero notes that eero Pro 6 and eero 6 now support PPPoE.

Eero says that in bridge mode you "won't be able to manage your network's advanced features through the eero App," and that eero Plus features including Advanced Security, Ad Blocking and Content Filters don't work properly. To set it, eero's path is Settings, Advanced networking, DHCP & NAT, then switch from Automatic to Bridge.

## A setup checklist

1. **Decide which device routes.** Usually your own router, with the gateway bridged.
2. **Bridge the gateway** or, if it can't be bridged, set your router to AP mode. Not both.
3. **If you can't bridge, turn off the gateway's Wi-Fi.** TP-Link advises against giving the gateway and your system the same network name.
4. **Wire correctly.** TP-Link says not to connect more than one Deco directly to the existing router in Router mode, because it can create a network loop.
5. **Check the result.** Your router's WAN address should now be a public address, not one starting with 192.168., 10. or 172.16 to 31. Run the network test on any game console.

If you are still deciding whether to keep renting the gateway at all, see [buying your own router vs. using your provider's]({{< relref "/guides/buy-your-own-router-vs-isp-equipment" >}}). For console NAT types, see our [WPS and UPnP guide]({{< relref "/guides/should-you-disable-wps-and-upnp" >}}) and [gaming router guide]({{< relref "/guides/do-you-need-a-gaming-router" >}}). For choosing the system you'll plug in, see [router vs. mesh]({{< relref "/guides/wifi-router-vs-mesh" >}}).

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Xfinity bridge mode turns off routing and leaves the modem on; steps via 10.0.0.1, Gateway, At a Glance; one connected device only; no network management, extenders or CyberSecure; hotspot stays on | [Xfinity Support, checked October 12, 2026](https://www.xfinity.com/support/articles/wireless-gateway-enable-disable-bridge-mode) | Verified |
| NAT lets devices share one public IP address; double NAT is two routers performing NAT; eero recommends bridging the modem-router combo; same-name networks cause complications | [eero Support, What is NAT?](https://eero.com/support/articles/what-is-nat) | Verified as of October 12, 2026 |
| eero lists AT&T U-verse, PPPoE and MAC address requirements as cases for bridging eero; features lost; menu path | [eero Support, What is bridge mode?](https://eero.com/support/articles/what-is-bridge-mode) | Verified as of October 12, 2026 |
| Netgear prefers bridging the ISP gateway, otherwise gateway Wi-Fi off and router in AP mode; some features disabled in AP mode | [Netgear Support](https://kb.netgear.com/000033729/) | Verified as of October 12, 2026 |
| TP-Link recommends bridge mode to avoid double NAT, warns of connectivity and performance issues and network loops, and advises against matching network names | [TP-Link Support FAQ 1432](https://www.tp-link.com/us/support/faq/1432/) | Verified as of October 12, 2026 |
| Xbox lists "Double NAT detected" and shows NAT type under Network settings | [Xbox Support](https://support.xbox.com/en-US/help/hardware-network/connect-network/xbox-one-nat-error) | Verified as of October 7, 2026 |
| 10.0.0.0/8, 172.16.0.0/12 and 192.168.0.0/16 are private address ranges | [RFC 1918](https://www.rfc-editor.org/rfc/rfc1918) | Verified |
| A private WAN address on your router usually indicates double NAT | Our explanation | Qualified: some providers run network-level (carrier-grade) NAT, which can also leave your router without a public address |

## Bottom line

Two routers in a row works, but it isn't tidy. Bridge the provider's gateway so your own router does the routing, and accept that the gateway's extra features go away. If the gateway can't be bridged, turn off its Wi-Fi and put your router in AP mode. Then check your router's WAN address and your console's NAT type to confirm the fix.
