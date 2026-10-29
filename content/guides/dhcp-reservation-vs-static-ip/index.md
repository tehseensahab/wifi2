---
title: "DHCP Reservation vs. Static IP: Which Should You Use?"
date: 2026-10-29T04:00:00Z
description: "For most home devices, a DHCP reservation beats a static IP: the router hands out the same address every time. Set a static IP only outside the DHCP pool."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "routers"]
tags: ["dhcp-reservation", "static-ip", "ip-address", "dhcp", "printers", "port-forwarding", "asus", "netgear", "tp-link", "google-nest-wifi", "eero"]
summary: "Use a DHCP reservation for printers, NAS boxes, cameras and game consoles on a home network: you set it once in the router, and the device keeps getting the same address automatically. Set a static IP on the device itself only when it can't use a reservation, and pick an address outside the router's DHCP pool so nothing else gets it."
imageAlt: "Black Epson inkjet printer with a colorful print on its top tray, sitting on a metal shelf"
imageCredit: "Photo: Emiliano Vittoriosi / [Unsplash](https://unsplash.com/photos/a-printer-sitting-on-top-of-a-table-I8sWaXL5ezo)"
takeaways:
  - "A DHCP reservation is set in the router: Google describes it as your network assigning \"the same IP address to a specific device whenever that device connects.\""
  - "A static IP is typed into the device itself. Microsoft says it \"must be a unique address in the range of addresses that are available for your network.\""
  - "If you set a static IP, keep it outside the router's DHCP pool. Otherwise the router can hand the same address to another device and cause a conflict."
  - "Rules differ by brand: ASUS says a reserved address must be inside its DHCP pool, and TP-Link says it must be on the same subnet as the router's LAN address."
  - "A reservation is tied to the device's MAC address, so it can break if a phone or laptop changes its private Wi-Fi address; eero lists IP reservations among the features MAC randomization affects."
faq:
  - q: "Is a DHCP reservation the same as a static IP?"
    a: "Not quite. Both give a device a fixed address, but a reservation is stored in the router and delivered automatically through DHCP, while a static IP is typed into the device's own network settings. Google's help page uses the term \"static IP\" loosely for a reserved address, which is part of why the two get confused."
  - q: "Should I use a reservation for a printer?"
    a: "Usually, yes. A printer that keeps the same address is easier for computers to find, and a reservation does that without touching the printer's network menus. NETGEAR suggests reserved addresses for \"computers or servers that need permanent IP settings to work correctly.\""
  - q: "Why didn't my device get its reserved address right away?"
    a: "A device keeps its current address until it next asks the router for one. NETGEAR says to reboot the device or force a DHCP release and renew. Google says you may need to disconnect and reconnect the device. TP-Link's steps end with rebooting the router."
  - q: "Can I set reservations if my router is in bridge or access point mode?"
    a: "Not on that router. Reservations live in whichever device runs DHCP for your network, usually the main router or ISP gateway. eero, for example, lists IP reservations and port forwarding among the features you lose in bridge mode."
  - q: "What happens to my reservations if I replace my router?"
    a: "They stay behind with the old router. A reservation is a setting in the router that hands out addresses, so a new router starts without it. Recreate the reservations on the new router, using the same addresses if other devices or port-forwarding rules depend on them."
sources:
  - title: "RFC 2131: Dynamic Host Configuration Protocol"
    publisher: "IETF / RFC Editor"
    url: "https://rfc-editor.org/rfc/rfc2131.html"
    date: 1997-03-01
  - title: "Set DHCP IP reservation or a Static IP address for a device"
    publisher: "Google Nest Help"
    url: "https://support.google.com/googlehome/answer/6274660?hl=en"
  - title: "How do I reserve an IP address on my NETGEAR router?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/25722/How-do-I-reserve-an-IP-address-on-my-NETGEAR-router"
    date: 2025-07-07
  - title: "How to configure Address Reservation on TP-Link wireless router"
    publisher: "TP-Link (Omada Networks support mirror)"
    url: "https://www.omadanetworks.com/us/support/faq/182/"
    date: 2026-09-17
  - title: "[Wireless Router] How to manually assign LAN IP around the DHCP list?"
    publisher: "ASUS"
    url: "https://www.asus.com/us/support/FAQ/1000906"
    date: 2026-09-09
  - title: "How to change the IP address of a network adapter"
    publisher: "Microsoft Learn"
    url: "https://learn.microsoft.com/ar-sa/troubleshoot/windows-server/networking/change-ip-address-network-adapter"
    date: 2026-02-12
  - title: "Use DHCP or a manual IP address on Mac"
    publisher: "Apple Support"
    url: "https://support.apple.com/guide/mac-help/mchlp2718/mac"
  - title: "What advanced features does eero support?"
    publisher: "eero"
    url: "https://eero.com/support/articles/what-advanced-features-does-eero-support"
  - title: "What features do I lose if I put my eeros in bridge mode?"
    publisher: "eero"
    url: "https://eero.com/support/articles/what-features-do-i-lose-if-i-put-my-eeros-in-bridge-mode"
  - title: "What is MAC Address Randomization?"
    publisher: "eero"
    url: "https://eero.com/support/articles/what-is-mac-address-randomization"
  - title: "MAC randomization behavior"
    publisher: "Android Open Source Project"
    url: "https://source.android.com/docs/core/connect/wifi-mac-randomization-behavior"
    date: 2026-10-09
  - title: "Is it okay to set my access point to obtain an IP address and reserve it on the router?"
    publisher: "EnGenius"
    url: "https://doctorengenius.engeniustech.com/en/articles/6708950-since-static-ip-addressing-is-recommended-in-most-access-point-deployments-is-it-okay-if-i-set-my-access-point-to-obtain-an-ip-address-and-reserve-it-on-the-router-setting"
    date: 2022-11-04
---

For almost every device on a home network, use a **DHCP reservation**: you set it once in your router, and the router gives that device the same IP address every time it connects. Set a **static IP** on the device itself only when the device can't get a reservation, for example because you can't change your router's settings, and when you do, choose an address outside the range your router hands out automatically. That one rule avoids the most common cause of address conflicts: two devices ending up with the same address.

## What each one is

Your router runs a DHCP server, the service that gives every phone, laptop and smart plug an IP address when it joins the network. Most of those addresses are temporary leases, which is why a device's address can change after a restart.

**A DHCP reservation** tells the router: whenever this specific device asks, give it this specific address. Google's definition: "your Wi-Fi network assigns the same IP address to a specific device whenever that device connects to your network." The router recognizes the device by its MAC (hardware) address: NETGEAR's and TP-Link's reservation screens both ask for it. The DHCP standard itself, RFC 2131, describes this as manual allocation, where "a client's IP address is assigned by the network administrator, and DHCP is used simply to convey the assigned address to the client."

**A static IP** is set in the device's own network settings instead of the router. The device stops asking the router for an address and uses the one you typed in, along with a subnet mask, gateway (your router's address) and DNS servers. Apple's Mac help puts it simply: "If your ISP or administrator gave you an IP address, choose Manually, then enter the address in the IP address field."

One source of confusion: router makers often call a reservation a "static IP" in their apps. Google's help page, for instance, walks you through choosing a device and entering "a static IP address" while making a reservation. In this guide, "static IP" means the address is configured on the device.

## Side by side

| | DHCP reservation | Static IP on the device |
|---|---|---|
| Where you set it | Router or mesh app | Each device's network settings |
| Address range | Inside the pool on ASUS; same subnet on TP-Link (rules vary by brand) | Should be outside the DHCP pool |
| Survives a router replacement | No, recreate it on the new router | Yes, but it may not match the new router's subnet |
| Breaks if the device's MAC address changes | Yes | No |
| Risk of address conflicts | Low: the router keeps track | Higher if the address is inside the DHCP pool |
| Works without the router's DHCP server | No | Yes |

## Why a reservation is the safer default

The router keeps the whole address list in one place. When it reserves an address for your printer, it knows not to give that address to anything else, and every reservation can be seen and changed from one screen.

A static IP set on a device is invisible to the router's DHCP server. If you pick an address inside the pool the router hands out, the router may later give the same address to a phone or TV. EnGenius explains it in its support FAQ: "If you assign a local static IP that is in the DHCP lease pool, the DHCP service will not know it." Its advice is to assign static addresses "outside the DHCP lease pool."

RFC 2131 does tell DHCP servers that they "SHOULD check that the offered network address is not already in use," for example with a ping, and tells devices to check a new address too. That's a safety net, not a guarantee, and a device that's switched off when the check runs won't answer it. On Windows, Microsoft lists the result when you do collide: "The static IP address that was just configured is already in use on the network. Please reconfigure a different IP address."

## When a static IP still makes sense

- **You can't change the router's settings**, for example on some ISP-managed or building-provided networks. A static IP outside the pool, if you know the pool, is the workaround.
- **The device must work even if DHCP doesn't**, such as a network switch, access point or home server that other devices depend on. Static addressing is a common choice for network infrastructure; an EnGenius support FAQ starts from the premise that "static IP addressing is recommended in most access point deployments."
- **The device rotates its MAC address and you can't turn that off**, since a reservation keyed to the old MAC address won't match.

For printers, cameras, game consoles, NAS boxes and smart-home hubs on a typical home network, a reservation does the job with less risk.

## Brand rules that trip people up

Router makers don't all handle reservations the same way. Check these before you pick an address:

- **ASUS** says the reserved address "needs to be in the IP pool of your DHCP server," and that the DHCP Server page shows the maximum number of manual assignments (it gives 128 as an example). Its menu path is Advanced Settings > LAN > DHCP Server.
- **TP-Link** says the reserved IP "must be on the same subnet with the LAN IP." In TP-Link's example, with a LAN address of 192.168.0.1, that means 192.168.0.2 to 192.168.0.254. The setting is under Advanced > Network > DHCP Server > Address Reservation, and TP-Link's steps end with a router reboot.
- **NETGEAR** puts it under ADVANCED > Setup > LAN Setup (or Settings > Setup > LAN Setup on some models), in the Address Reservation section. The device picks up its new address the next time it contacts the router; NETGEAR says to "reboot the computer, or access its IP configuration to force a DHCP release and renew."
- **Google** routers managed in the Google Home app handle it under Wifi > Network settings > Advanced Networking > DHCP IP reservations. Google says, "You may need to disconnect this device from your Wi-Fi network and reconnect it before it is assigned the reserved IP."
- **eero** lists reservations under Reservations & Port Forwarding in the eero app, but not in bridge mode: eero lists "IP reservations and port forwarding" among the features you lose there.

That last point applies to any brand. If your router or mesh system is in bridge or access point mode, the device actually running DHCP is your ISP's gateway or another router, so make the reservation there. Our guide to [bridge mode and double NAT]({{< relref "/guides/bridge-mode-double-nat-own-router" >}}) explains how to tell which device is in charge.

## Watch out for private Wi-Fi addresses

A reservation matches a device by its MAC address. Many phones, tablets and laptops use a private, randomized MAC address instead (Android 10 and later do so by default, according to Google), and eero lists IP reservations among the router features that MAC randomization can affect. If the address changes, the reservation stops matching. For a phone you want to reserve an address for, use a fixed private address or turn the feature off for your home network only. Our [private Wi-Fi address guide]({{< relref "/guides/private-wifi-address" >}}) covers the settings on iPhone, Android and Windows.

## How to set a static IP if you need one

First, find your router's DHCP pool in its LAN or DHCP settings, and choose an address in the same subnet but outside that range. Then:

**Windows (Control Panel):** open the network connection's Properties, select the Internet Protocol (TCP/IP) entry for IPv4, click Properties, choose **Use the following IP address**, and fill in the IP address, subnet mask, default gateway and DNS servers. Microsoft's instruction is that the address "must be a unique address in the range of addresses that are available for your network."

**Mac:** open System Settings > Network, click your connection, click Details, click TCP/IP, then set **Configure IPv4** to Manually and enter the address, subnet mask and router.

Write the address down, along with the pool range. If you later change routers or the router's subnet, a device with a static IP won't follow along on its own.

## Where this matters next

Most people set up a reservation because something else depends on a stable address, usually port forwarding for a game console, camera or server. Our [port forwarding guide]({{< relref "/guides/how-to-set-up-port-forwarding" >}}) picks up from here. If your new address never seems to stick, check the [list of connected devices]({{< relref "/guides/see-who-is-connected-to-my-wifi" >}}) to confirm the device is appearing under the MAC address you reserved.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Reservation definition; Google Home app path; may need to reconnect | [Google Nest Help](https://support.google.com/googlehome/answer/6274660?hl=en) | Verified |
| Manual allocation in the DHCP standard; servers and clients should check an address isn't in use | [RFC 2131](https://rfc-editor.org/rfc/rfc2131.html) | Verified |
| NETGEAR menu path; reserved addresses for devices needing permanent settings; reboot or release/renew | [NETGEAR](https://kb.netgear.com/25722/How-do-I-reserve-an-IP-address-on-my-NETGEAR-router) | Verified |
| TP-Link: same subnet as LAN IP; 192.168.0.2 to .254 example; menu path; reboot | [TP-Link (Omada mirror)](https://www.omadanetworks.com/us/support/faq/182/) | Verified |
| ASUS: reserved IP must be in the DHCP pool; maximum shown on the page (128 example); menu path | [ASUS](https://www.asus.com/us/support/FAQ/1000906) | Verified |
| Windows static IP fields; unique address requirement; conflict error message | [Microsoft Learn](https://learn.microsoft.com/ar-sa/troubleshoot/windows-server/networking/change-ip-address-network-adapter) | Qualified (Windows Server troubleshooting article) |
| Mac manual IP steps | [Apple Support](https://support.apple.com/guide/mac-help/mchlp2718/mac) | Verified |
| MAC randomization affects IP reservations | [eero](https://eero.com/support/articles/what-is-mac-address-randomization) | Verified |
| Android 10 and later randomize MAC addresses by default | [Android Open Source Project](https://source.android.com/docs/core/connect/wifi-mac-randomization-behavior) | Verified |
| eero Reservations & Port Forwarding setting | [eero](https://eero.com/support/articles/what-advanced-features-does-eero-support) | Verified |
| eero loses IP reservations and port forwarding in bridge mode | [eero](https://eero.com/support/articles/what-features-do-i-lose-if-i-put-my-eeros-in-bridge-mode) | Verified |
| Static IPs inside the DHCP pool aren't known to the DHCP service; assign outside the pool | [EnGenius](https://doctorengenius.engeniustech.com/en/articles/6708950-since-static-ip-addressing-is-recommended-in-most-access-point-deployments-is-it-okay-if-i-set-my-access-point-to-obtain-an-ip-address-and-reserve-it-on-the-router-setting) | Qualified (vendor FAQ, 2022) |
