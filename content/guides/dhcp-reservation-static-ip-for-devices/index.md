---
title: "DHCP Reservation vs. Static IP: Give a Device a Fixed Address"
date: 2026-10-17
description: "How a DHCP reservation keeps a printer, camera or NAS on the same IP address. Netgear and ASUS steps, and why phone privacy MAC addresses can break a reservation."
authors: ["Craig Leslie"]
topics: ["how-to-fixes", "routers"]
tags: ["dhcp-reservation", "static-ip", "ip-address", "mac-address", "private-wifi-address", "netgear", "asus"]
summary: "A DHCP reservation tells your router to always hand the same IP address to one device, identified by its MAC address. It is usually easier to manage than setting a static address on the device itself. Phones and laptops that use a different, private MAC address on each Wi-Fi network need that address, not the hardware one, in the reservation."
imageAlt: "Close-up of a TP-Link five-port gigabit desktop switch with yellow and red Ethernet cables plugged in and green status lights lit"
imageCredit: "Photo: User_Pascal / [Unsplash](https://unsplash.com/photos/vE5AKQRUs7c)"
takeaways:
  - "By default, home routers use DHCP (Dynamic Host Configuration Protocol) to lend each device an address for a limited time. RFC 2131 calls this dynamic allocation, so a device's address can change."
  - "Netgear says a reservation ties a device's MAC address to an IP address, and the device gets it the next time it contacts the router's DHCP server. Rebooting the device or renewing its lease applies it sooner."
  - "ASUS says the address you reserve must be inside the router's DHCP pool, and its web interface cannot edit a rule: delete it and create a new one."
  - "Apple's Private Wi-Fi Address feature gives an iPhone, iPad or Mac a different MAC address for each network. Android 10 and later does similarly. Apple's page does not say how this affects reservations, so check which MAC address the router sees."
faq:
  - q: "What is a DHCP reservation?"
    a: "A setting in your router that always gives one device the same IP address. The router recognizes the device by its MAC address. The device keeps asking for an address automatically, so you don't change anything on the device."
  - q: "What is the difference between a DHCP reservation and a static IP?"
    a: "With a reservation, the router assigns the fixed address. With a static IP, you type the address into the device itself. ASUS describes both methods and says a device using a static IP must match the address bound in the router. Reservations are easier to track because the list is in one place."
  - q: "Does the IP address have to be inside the DHCP pool?"
    a: "On ASUS routers, yes: ASUS says the address must be inside the router's DHCP pool. Netgear's article doesn't address the pool, so check the LAN settings page of your router and follow its maker's instructions."
  - q: "Why didn't my device get its reserved address?"
    a: "Netgear says the address is applied the next time the device contacts the DHCP server, so reboot the device or renew its lease. Also check that the MAC address in the reservation is the one the device uses on this network. Apple devices can use a different private address per Wi-Fi network."
  - q: "Do I need a reservation for every device?"
    a: "No. It is mainly useful for devices you reach by address, such as a printer, network storage, or a camera or hub, and for devices where other settings are tied to an address. Most phones, TVs and laptops work fine with automatic addresses. This is our recommendation, not a manufacturer requirement."
sources:
  - title: "RFC 2131: Dynamic Host Configuration Protocol"
    publisher: "IETF (RFC Editor)"
    url: "https://www.rfc-editor.org/rfc/rfc2131"
    date: 1997-03-01
  - title: "How do I reserve an IP address on my NETGEAR router?"
    publisher: "NETGEAR Support"
    url: "https://kb.netgear.com/25722/How-do-I-reserve-an-IP-address-on-my-NETGEAR-router"
    date: 2025-07-07
  - title: "[Wireless Router] How to manually assign LAN IP around the DHCP list?"
    publisher: "ASUS Support"
    url: "https://www.asus.com/us/support/FAQ/1000906"
    date: 2026-09-09
  - title: "Use private Wi-Fi addresses on Apple devices"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102509"
    date: 2025-12-05
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102766"
    date: 2026-07-14
  - title: "Find or change your Android device network settings"
    publisher: "Google Android Help"
    url: "https://support.google.com/android/answer/9654714"
  - title: "RFC 1918: Address Allocation for Private Internets"
    publisher: "IETF (RFC Editor)"
    url: "https://www.rfc-editor.org/rfc/rfc1918"
    date: 1996-02-01
---

A DHCP reservation makes your router give one device the same IP address every time. Use it for things you reach by address, such as a printer, a network storage drive or a camera. You set it once in the router's admin page, and the device itself keeps using automatic settings. You can also type a static address into the device, but the router-side method keeps all your fixed addresses in one list.

This guide is based on RFC 2131 and Netgear, ASUS, Apple and Google documentation. We have not tested these settings on every router, and menu names vary by model and firmware. You'll need your router's admin page, which our guide to [finding your router's address and logging in]({{< relref "/guides/find-router-ip-address-and-log-in" >}}) covers.

## What DHCP does, and why addresses change

Every device on your network needs an IP address. Routers hand them out using **DHCP**, the Dynamic Host Configuration Protocol. RFC 2131, the DHCP standard, describes three ways to allocate an address:

- **Automatic:** the server assigns a permanent address.
- **Dynamic:** the server assigns an address "for a limited period of time," and can reuse it when it is no longer needed.
- **Manual:** the network administrator picks the address, and DHCP just delivers it to the device.

Home routers typically use dynamic allocation. The standard says a client "acquires a lease for a network address for a fixed period of time," so a device's address can change when its lease ends or the device reconnects. Apple recommends a DHCP lease time of 8 hours for home and office networks, and says a network should have only one DHCP server. A DHCP reservation is the router-side version of the manual approach: the router still delivers the address, but you chose it.

## When a fixed address helps

Our view, based on how these features work: it helps when something refers to a device by its address. Examples are a printer that computers were set up to find by address, network storage or a camera you reach directly, or a rule on your router that is tied to an address. For phones, TVs and laptops that simply connect to the internet, automatic addresses are fine, and a long reservation list is more to maintain.

## Reservation vs. static IP

| | DHCP reservation | Static IP on the device |
|---|---|---|
| Where you set it | In the router | In the device's network settings |
| Device setting | Stays on automatic | Fixed address typed in |
| Tracking | One list in the router | Spread across devices |
| Main risk | MAC address in the reservation doesn't match the device | Device and router settings disagree |

ASUS describes both methods in its FAQ. For the router method it says a device in the binding list should usually be set to obtain an IP address automatically, and that if a device uses a static IP, the address must match the one bound in the router.

## How to set a reservation

Before you start, note two things. First, find the device's **MAC address**, a hardware identifier written as six pairs of characters, such as 12:34:56:AA:BC:DE. Most routers can show it in their list of connected devices. Second, pick an address from your network's private range. RFC 1918 reserves 10.0.0.0 to 10.255.255.255, 172.16.0.0 to 172.31.255.255 and 192.168.0.0 to 192.168.255.255 for private networks, and your router's own range is one block of these.

**Netgear** (per Netgear's article, last updated July 7, 2025):

1. Connect to the router and go to routerlogin.net. Log in as admin.
2. Choose **Advanced, Setup, LAN Setup**. On some models it is **Settings, Setup, LAN Setup**.
3. In the **Address Reservation** section, click **Add**.
4. Enter an IP address from the router's LAN subnet (Netgear's example is 192.168.1.x) and the device's MAC address. If the device is already connected, you can copy the MAC address from the **Attached Devices** page.
5. Click **Apply**. The reservation appears in the table.

Netgear says the address isn't assigned right away: the device gets it the next time it contacts the DHCP server. Reboot the device, or release and renew its IP configuration, to apply it sooner.

**ASUS web interface** (per ASUS FAQ, updated September 9, 2026):

1. Go to your router's LAN address or http://www.asusrouter.com and log in.
2. Choose **Advanced Settings, LAN, DHCP Server** and note the DHCP IP pool.
3. Set **Enable Manual Assignment** to **Yes**.
4. Pick the device from the list, or enter its MAC address in the colon-separated format. Enter the IP address you want. The DNS field is optional.
5. Click the **+** icon, then **Apply**, and check that the rule shows the right MAC and IP address.

**ASUS Router app:** ASUS says to go to **Settings, LAN, IP Binding, IP Binding List**, tap **+**, and either select the device or enter its MAC address and IP address manually.

Points specific to ASUS, from the same FAQ: the IP address you assign must fall inside the router's DHCP pool; the web interface cannot edit an existing rule, so you delete the rule, apply, and create a new one (the app can edit directly); and the number of manual assignments is capped (the FAQ's example screen shows a maximum of 128, so check your own model).

Netgear's article says nothing about the DHCP pool, and we can't tell you whether Netgear models differ from ASUS here. Look at the DHCP range on your router's LAN settings page and follow your maker's instructions. We did not verify reservation steps for eero from eero's own documentation, so we leave them out.

## Why phones and laptops can break a reservation

A reservation matches a device by its MAC address. Many phones and laptops now use a different address on each Wi-Fi network, to make it harder for network operators to track a device.

Apple says its **Private Wi-Fi Address** feature lets a device use "a different Wi-Fi (MAC) address for each network." With iOS 18, iPadOS 18 and macOS Sequoia 15 and later, there are three settings: **Off** (the hardware MAC address), **Fixed** (the private address stays the same, and the default for WPA2 or stronger security) and **Rotating** (the address changes every 2 weeks, and the default for weak-security or open networks). You change it per network: on an iPhone, open Settings, Wi-Fi, tap the More Info button next to the network, then choose Private Wi-Fi Address.

Google says Android 10 and later devices have a second, randomized MAC address for each network, separate from the Wi-Fi MAC address in About phone. You find it under Settings, Network & internet, Internet, the settings icon next to your network, then Randomized MAC address.

Neither page says how this affects DHCP reservations, so this part is our reasoning, not a vendor statement: a reservation entered with a device's hardware MAC address will not match if the device connects with a private one. The practical check is to enter the address your router actually lists for that device on your network, and use Fixed or Off rather than Rotating if you want it to stay constant. Rotating would change the address every two weeks, which would break a reservation.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| DHCP allocation types are automatic, dynamic and manual; a client acquires a lease for a fixed period | [RFC 2131, March 1997](https://www.rfc-editor.org/rfc/rfc2131) | Verified |
| Apple recommends an 8-hour DHCP lease time for home and office networks; only one DHCP server per network | [Apple Support 102766, July 14, 2026](https://support.apple.com/en-us/102766) | Verified |
| Netgear: reservation steps, menu names, MAC from Attached Devices, applied at the next DHCP contact, reboot or renew | [Netgear KB 25722, updated July 7, 2025](https://kb.netgear.com/25722/How-do-I-reserve-an-IP-address-on-my-NETGEAR-router) | Verified as of October 17, 2026; Netgear's page says nothing on the DHCP pool |
| ASUS: web and app steps; IP must be inside the DHCP pool; web interface can't edit rules; MAC format; static IP must match the binding; example cap of 128 | [ASUS FAQ 1000906, updated September 9, 2026](https://www.asus.com/us/support/FAQ/1000906) | Qualified: the cap shown is the FAQ's example; screens vary by firmware |
| Apple Private Wi-Fi Address: per-network address; Off, Fixed, Rotating; Fixed is the default for WPA2 or stronger, Rotating (every 2 weeks) for weak or open networks | [Apple Support 102509, December 5, 2025](https://support.apple.com/en-us/102509) | Verified; applies to iOS 18, iPadOS 18, macOS Sequoia 15 and later |
| Android 10 and later has a separate randomized MAC address per network, found under Settings, Network & internet, Internet | [Google Android Help](https://support.google.com/android/answer/9654714) | Qualified: the page shows no date, and menu names vary by phone |
| Effect of private addresses on reservations | Our analysis | Not a vendor claim: neither Apple nor Google addresses reservations |
| Private ranges 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 | [RFC 1918](https://www.rfc-editor.org/rfc/rfc1918) | Verified |

## Bottom line

Reserve addresses only for devices you reach by address, using the router's reservation list and the MAC address the router sees for that device. Keep the address inside the DHCP pool on ASUS routers, and check your own router's guidance on others. If a phone or laptop is on the list, use a fixed or off private-address setting so the MAC doesn't change.
