---
title: "What Is a Subnet Mask? Home Network Basics Explained"
date: 2026-10-30T04:00:00Z
description: "What is a subnet mask? It tells a device which addresses are on your home network. Most homes use 255.255.255.0 (/24); what it means and when to change it."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "routers"]
tags: ["subnet-mask", "ip-address", "lan", "private-ip", "cidr", "default-gateway", "static-ip", "home-network"]
summary: "A subnet mask tells a device which part of an IP address identifies the local network and which part identifies the device. Devices use it to decide whether to talk to another device directly or send the traffic to the router. Most home routers use 255.255.255.0, also written /24, which gives 254 usable addresses, including the one the router uses."
imageAlt: "Black-and-white photo of the back of a network equipment chassis with fan modules and cables"
imageCredit: "Photo: Kvistholt Photography / [Unsplash](https://unsplash.com/photos/photo-of-computer-cables-oZPwn40zCK4)"
takeaways:
  - "A subnet mask marks which bits of an IPv4 address are the network part. With 255.255.255.0 (/24), the first three numbers are the network and the last number is the device."
  - "Devices compare a destination with their own address through the mask. If the network parts match, they send directly; if not, they send the traffic to the default gateway, usually your router."
  - "A /24 network has 256 addresses. Two are reserved (the all-zeros network address and the all-ones broadcast address), leaving 254 for routers and devices."
  - "Home networks use private address ranges set aside by RFC 1918: 10.0.0.0/8, 172.16.0.0/12 and 192.168.0.0/16."
  - "Most homes never need to change the mask. If you set a static IP, copy the mask your router uses; a wrong mask can leave the device unable to reach others."
faq:
  - q: "What subnet mask should I use at home?"
    a: "Use whatever your router already hands out, which for most home routers is 255.255.255.0 (/24). That gives 254 usable addresses, including the router's own, which is plenty for most households. Only change it if you have a specific reason, such as running out of addresses."
  - q: "What does /24 mean?"
    a: "It's CIDR (prefix length) notation. The number after the slash is how many leading bits of the address belong to the network. /24 means the first 24 of 32 bits, which is the same as the mask 255.255.255.0."
  - q: "What happens if I enter the wrong subnet mask?"
    a: "The device can misjudge which addresses are local. It may try to reach a printer or game console through the router instead of directly, or try to reach a device directly when it should go through the router. Either way, some connections fail. Copy the mask from another working device on the same network."
  - q: "Is the subnet mask the same as the default gateway?"
    a: "No. The subnet mask defines the size of your local network. The default gateway is the address of the router that devices send traffic to when the destination is outside that network. A manual IP setup needs both."
  - q: "Does IPv6 use subnet masks?"
    a: "In general, IPv6 networks are described with a prefix length in slash notation rather than a dotted mask like 255.255.255.0. This guide covers IPv4, which is where you'll see a subnet mask field."
sources:
  - title: "RFC 1918: Address Allocation for Private Internets"
    publisher: "IETF / RFC Editor"
    url: "https://www.rfc-editor.org/rfc/rfc1918"
    date: 1996-02-01
  - title: "RFC 4632: Classless Inter-domain Routing (CIDR)"
    publisher: "IETF / RFC Editor"
    url: "https://rfc-editor.org/rfc/rfc4632.html"
    date: 2006-08-01
  - title: "RFC 950: Internet Standard Subnetting Procedure"
    publisher: "IETF / RFC Editor"
    url: "https://www.rfc-editor.org/rfc/rfc950"
    date: 1985-08-01
  - title: "RFC 1122: Requirements for Internet Hosts - Communication Layers"
    publisher: "IETF / RFC Editor"
    url: "https://rfc-editor.org/rfc/rfc1122.html"
    date: 1989-10-01
  - title: "[Wireless Router] How to change LAN IP of ASUS Wireless Router?"
    publisher: "ASUS"
    url: "https://www.asus.com/us/support/FAQ/1011245"
    date: 2026-03-18
  - title: "Set a custom LAN IP"
    publisher: "Google Nest Help"
    url: "https://support.google.com/googlenest/answer/7571856"
  - title: "What are the Advanced networking settings?"
    publisher: "eero"
    url: "https://eero.com/support/articles/what-are-the-advanced-networking-settings"
  - title: "How to configure the IP address manually on the wireless clients"
    publisher: "TP-Link (Omada)"
    url: "https://www.omadanetworks.com/support/faq/41/"
    date: 2026-02-26
  - title: "Running IPconfig in Windows"
    publisher: "Kansas State University IT"
    url: "https://support.ksu.edu/TDClient/30/Portal/KB/PrintArticle?ID=69"
    date: 2024-09-04
---

A subnet mask tells a device which part of an IP address identifies your local network and which part identifies the device itself. Your phone or laptop uses it to decide whether another address is on the same network, so it can talk to it directly, or somewhere else, so it has to send the traffic to your router. Most home routers use **255.255.255.0**, also written **/24**, which gives 254 usable addresses, including the router's. You rarely need to change it, but you do need to enter it correctly if you set a static IP.

## How a subnet mask works

An IPv4 address such as 192.168.1.25 is really 32 bits, written as four numbers from 0 to 255. The subnet mask is another 32-bit number laid over it. Wherever the mask has a 1, that bit belongs to the network part of the address; wherever it has a 0, it belongs to the device (host) part.

RFC 1122, the Internet standard for how hosts behave, describes the mask as "a 32-bit mask that selects the network number and subnet number fields of the corresponding IP address."

With the common home mask, it looks like this:

| | First number | Second | Third | Fourth |
|---|---|---|---|---|
| IP address | 192 | 168 | 1 | 25 |
| Subnet mask | 255 | 255 | 255 | 0 |
| Meaning | network | network | network | device |

A 255 in the mask means all eight bits of that number are network bits; a 0 means all eight are device bits. So with 255.255.255.0, every address from 192.168.1.0 to 192.168.1.255 is on the same local network.

## Why it matters: direct or through the router

Every time a device sends something, it checks whether the destination is local. RFC 1122 spells out the test: if the destination's bits picked out by the mask match the device's own, "then the destination is on the corresponding connected network" and the data is sent "directly to the destination host." If they don't match, "the destination is accessible only through a gateway."

On a home network, that gateway is your router, which is why manual IP settings ask for a **default gateway** as well as a mask. Using the example above:

- Your laptop at 192.168.1.25 prints to a printer at 192.168.1.40. The first three numbers match, so it sends directly.
- Your laptop opens a website at a public address. The first three numbers don't match, so it sends the traffic to the router at, say, 192.168.1.1, which forwards it to the internet.

This is also why a wrong mask causes odd problems. If a device thinks the local network is smaller or larger than it really is, it may send traffic to the router that should go directly, or try to reach a device directly that it can't. A common symptom is that some things work and others, often printers, game consoles or file shares, don't.

## Slash notation: what /24 means

You'll often see the same information written as a slash and a number, such as 192.168.1.0/24. This is CIDR notation, from RFC 4632. It describes the prefix as an address "followed by a decimal value between 0 and 32 that describes the number of significant bits." In other words, the number after the slash counts the 1s at the start of the mask.

For a /24, RFC 4632 explains that "the most significant 24 bits are ones and the least significant 8 bits are zeros," which is 255.255.255.0. Its own /16 example has "an implied network mask of 255.255.0.0."

| Prefix | Subnet mask | Addresses | Usable for devices |
|---|---|---|---|
| /24 | 255.255.255.0 | 256 | 254 |
| /23 | 255.255.254.0 | 512 | 510 |
| /22 | 255.255.252.0 | 1,024 | 1,022 |
| /16 | 255.255.0.0 | 65,536 | 65,534 |

The address count is 2 raised to the number of device bits: a /24 leaves 8 bits, and 2⁸ is 256.

### Why 254, not 256

Two addresses in every network are reserved. RFC 1122 says IP addresses "are not permitted to have the value 0 or -1" (all zeros or all ones) in the host part, apart from special cases. The all-ones address is the network's broadcast address, which RFC 1122 lists as "Directed broadcast to the specified network." On 192.168.1.0/24, that means 192.168.1.0 identifies the network and 192.168.1.255 is the broadcast address, leaving 192.168.1.1 through 192.168.1.254 for the router and your devices.

## The private ranges your home network uses

Home networks use private addresses that aren't routed on the public internet. RFC 1918 (February 1996) set aside three blocks for this:

- 10.0.0.0 to 10.255.255.255 (10.0.0.0/8)
- 172.16.0.0 to 172.31.255.255 (172.16.0.0/12)
- 192.168.0.0 to 192.168.255.255 (192.168.0.0/16)

RFC 1918 notes that "private addresses have no global meaning." In practice, that's why your router translates them to its public address when you go online. A home router usually takes a /24 slice of one of these blocks, for example 192.168.1.0/24 or 192.168.50.0/24. ASUS, for example, says its default LAN address is "192.168.1.1 or 192.168.50.1" with a default mask of 255.255.255.0.

If your internet provider gives your router a shared address too, that's a different issue; our guide to [CGNAT]({{< relref "/guides/what-is-cgnat" >}}) explains it.

## How to find your subnet mask

- **Windows:** open Command Prompt and run `ipconfig /all`. Look for **Subnet Mask** and **Default Gateway** under your Wi-Fi or Ethernet adapter.
- **Mac:** go to Apple menu > System Settings > Network > Wi-Fi, click **Details** next to your network, then **TCP/IP**. That's where the IP address, subnet mask and router are set.
- **iPhone:** open Settings > Wi-Fi, tap the info (i) button next to your network and and look under IPv4 Address (tap Configure IP to change it).
- **Router:** look in the LAN settings of the router's app or web page. That's the value every device on your network should be using.

## When to change it (and when not to)

Most households should leave the mask alone. A /24 gives 254 addresses, which covers a lot of phones, laptops and smart home devices.

There are a few cases where you'll deal with it:

- **Setting a static IP.** You must enter the mask and gateway yourself. Use the same mask your router uses, and pick an address that's in the same network but not already in use. TP-Link's example uses router address 192.168.0.1, mask 255.255.255.0 and gateway 192.168.0.1, with devices in 192.168.0.2 to 192.168.0.253. A [DHCP reservation]({{< relref "/guides/dhcp-reservation-vs-static-ip" >}}) is usually simpler, because the router hands out the right mask automatically.
- **Running out of addresses.** If you have more than about 250 devices, which is rare at home, a larger network such as /23 doubles the space.
- **Avoiding a clash with another router.** If you add a second router behind your provider's gateway, the two shouldn't use the same local range. Using [bridge mode]({{< relref "/guides/bridge-mode-double-nat-own-router" >}}) or giving each router a different range avoids confusion.

### Changing the LAN subnet on your router

The setting is usually called **LAN IP** or **LAN settings**:

- **ASUS:** in the web interface, go to LAN > LAN IP, change the IP Address or Subnet Mask field, and click Apply (ASUS FAQ, updated March 18, 2026).
- **Google Nest Wifi and Google Wifi:** in the Google Home app, go to Wi-Fi settings > Advanced networking > LAN, set the router's LAN IP and subnet mask, adjust the DHCP address pool and tap Save. Google says it will "automatically migrate existing DHCP IP reservations and port forwarding rules to the new subnet," and that connected devices "will briefly disconnect from Wi-Fi."
- **eero:** eero's help page says you can review or change the network's DHCP range under Advanced networking > Network services > DHCP & NAT; it doesn't describe the mask options.

Expect devices to drop off and reconnect after a change, and any device with a manually set IP to stop working until you update it. If you change the router's own address, you'll also need the new address to reach its settings.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Mask selects the network and subnet fields; local/remote decision; otherwise via gateway | [RFC 1122](https://rfc-editor.org/rfc/rfc1122.html) | Verified |
| Host part can't be all zeros or all ones; all-ones is directed broadcast | [RFC 1122](https://rfc-editor.org/rfc/rfc1122.html) | Verified |
| Prefix length is the number of significant bits; /24 bit layout; /16 = 255.255.0.0 | [RFC 4632](https://rfc-editor.org/rfc/rfc4632.html) | Verified |
| Address counts for /24, /23, /22, /16 | Calculated (2 to the power of the host bits) | Verified |
| Private ranges 10/8, 172.16/12, 192.168/16; no global meaning | [RFC 1918](https://www.rfc-editor.org/rfc/rfc1918) | Verified |
| ASUS default LAN IP and mask; how to change them | [ASUS](https://www.asus.com/us/support/FAQ/1011245) | Verified |
| Google custom LAN IP steps; reservations migrated; devices briefly disconnect | [Google Nest Help](https://support.google.com/googlenest/answer/7571856) | Verified |
| eero DHCP & NAT location in the app | [eero](https://eero.com/support/articles/what-are-the-advanced-networking-settings) | Verified |
| Mac and iPhone menu paths; TP-Link example values | [TP-Link](https://www.omadanetworks.com/support/faq/41/) | Qualified (TP-Link guide, not Apple's) |
| Windows ipconfig shows subnet mask and default gateway | [Kansas State University](https://support.ksu.edu/TDClient/30/Portal/KB/PrintArticle?ID=69) | Qualified (university IT guide) |
