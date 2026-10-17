---
title: "How to See Who's Connected to Your Wi-Fi (and Block Them)"
date: 2026-10-17
description: "Find the device list in your router's app, identify unknown entries and block what you don't recognize. Steps for eero, Google, Netgear and ASUS."
authors: ["Craig Leslie"]
topics: ["security-privacy", "how-to-fixes"]
tags: ["connected-devices", "wifi-security", "block-device", "mac-address", "eero", "google-nest-wifi", "netgear", "asus"]
summary: "Your router keeps a list of every device on your network. Open it in the router's app or admin page, match each entry to a device you own, and block anything you can't identify. Unfamiliar entries are often your own phones and laptops using private Wi-Fi addresses, so check those first. If a stranger really is on your network, block them and change your Wi-Fi password."
imageAlt: "Person using a smartphone"
imageCredit: "Photo: Christian Wiediger / [Unsplash](https://unsplash.com/photos/70ku6P7kgmc)"
takeaways:
  - "Every router app or admin page has a device list: Devices on eero and Google Nest Wifi, Attached Devices on Netgear, and Clients under Network Map on ASUS."
  - "Apple devices use a different private Wi-Fi address on each network by default, so an iPhone or Mac may not match the hardware address printed on it."
  - "Eero says blocking a device disconnects it and stops it rejoining, even with the correct password. ASUS can block a client's internet access."
  - "If you find a device you don't own, block it, then change your Wi-Fi password and check that your network uses WPA2 or WPA3."
faq:
  - q: "How can I see what devices are on my Wi-Fi?"
    a: "Open your router's app or admin page and find the device list. On eero, it's Devices; in the Google Home app, Wi-Fi then Devices; on Netgear, Attached Devices at routerlogin.net; on ASUS, Network Map then Clients."
  - q: "Why do I see devices I don't recognize?"
    a: "Often they're yours. Smart plugs, TVs and speakers may show only a manufacturer or a generic name, and Apple devices use private Wi-Fi addresses by default. Turn devices off one at a time, or check each device's Wi-Fi settings, to match entries."
  - q: "How do I kick someone off my Wi-Fi?"
    a: "Block the device in your router's app or admin page, then change your Wi-Fi password so anyone who knew the old one can't reconnect from another device."
  - q: "Can my neighbor use my Wi-Fi without the password?"
    a: "A network secured with WPA2 or WPA3 requires the password to join. If someone unexpected is connected, the password may have been shared or guessed, or WPS may be turned on."
  - q: "Will changing my Wi-Fi password disconnect my devices?"
    a: "Yes. Every device will need the new password, so plan to reconnect phones, laptops and smart home devices afterward."
sources:
  - title: "How do I block or remove unwanted devices on my network?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/how-do-i-block-unwanted-devices-on-my-network"
  - title: "View devices connected to your network and review data usage"
    publisher: "Google Home Help"
    url: "https://support.google.com/googlehome/answer/6263633"
  - title: "How do I view the devices on my network from my Nighthawk router?"
    publisher: "Netgear Support"
    url: "https://kb.netgear.com/24230/How-do-I-view-the-devices-that-are-connected-to-my-network-from-my-Nighthawk-router"
    date: 2025-07-07
  - title: "[Wireless Router] How to check the information of devices connected to ASUS router?"
    publisher: "ASUS Support"
    url: "https://www.asus.com/support/FAQ/1005513"
  - title: "Use private Wi-Fi addresses on Apple devices"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102509"
---

Your router keeps a list of every device on your network. Open it in the router's app or admin page, match each entry to something you own, and block anything you can't identify. If a stranger really is connected, block them and change your Wi-Fi password.

This guide is based on eero, Google, Netgear, ASUS and Apple support documentation. It is not a hands-on test.

## Step 1: Open your router's device list

| Router | Where to look | What it shows |
|---|---|---|
| eero | eero app: Devices on the Home tab, or the Devices tab | Each device, with options to pause or block |
| Google Nest Wifi, Google Wifi | Google Home app: Home, Wi-Fi, then Devices at the top | Devices used in the last 30 days, with data used by each |
| Netgear | routerlogin.net, then Attached Devices | Name, IP address, MAC address and status, split into wired and wireless |
| ASUS | Web interface: Network Map, then the Clients icon; or the ASUS Router app | Name, IP and MAC address, band, signal strength and connection time |
| Provider's gateway | The provider's app or the gateway's admin page | Varies by provider |

Google's list includes devices that "used the network within the last 30 days, including ones not currently connected," so an entry there doesn't mean the device is online now. Netgear notes a device's IP address can change when it rejoins, while its MAC address "does not change." Eero says devices that haven't connected in seven days drop off its list automatically.

## Step 2: Identify unfamiliar devices

Most unknown entries turn out to be your own devices. Work through them:

- **Smart home gear.** Plugs, bulbs, TVs, speakers and printers often show a manufacturer name or a string of letters and numbers. ASUS's client details include the manufacturer, which helps.
- **Phones and laptops with private addresses.** Apple says its devices identify themselves "to each network using a different Wi-Fi address" and may rotate it. On networks secured with WPA2 or stronger, Apple devices use a fixed private address by default; on weak or open networks, it rotates every two weeks. So the MAC address in your router's list may not match the one printed on the device. On an iPhone, open Settings, Wi-Fi, then tap the More Info button next to your network to see the address it uses.
- **Turn things off one at a time.** If you still can't place an entry, switch off or disconnect devices one by one and watch which entry goes offline.
- **Rename what you've identified** in the router's app, so the next check is quicker.

## Step 3: Block what you don't recognize

- **eero:** find the device under Devices, open it, tap the more options icon in the top-right corner, then tap Block device. Eero says blocking "disconnects the device and prevents it from rejoining your network, even if the correct password is entered." Blocking isn't available when eero is in bridge mode.
- **ASUS:** in the web interface, click the device under Network Map, Clients, turn on Block Internet Access and click Apply. In the app, open the device and tap Block. ASUS says a blocked device "cannot connect to the Internet."
- **Netgear:** the Attached Devices list shows whether each device is Allowed or Blocked. Look for access control settings on your model to block a device.
- **Google Nest Wifi and Google Wifi:** Google's device-list help page doesn't cover blocking. If you can't block an unknown device, change your Wi-Fi password instead.

## Step 4: Change your Wi-Fi password if someone got in

Blocking stops one device. If someone outside your household had the password, they can connect again from another device, so change it. Every device in your home will need the new password afterward.

While you're in the settings:

- **Use WPA3, or WPA2/WPA3 mixed mode,** if your router offers it. See [WPA2 vs. WPA3]({{< relref "/guides/wpa2-vs-wpa3" >}}).
- **Turn off WPS,** which lets devices join without the password. See [should you turn off WPS and UPnP]({{< relref "/guides/should-you-disable-wps-and-upnp" >}}).
- **Give visitors a guest network** instead of your main password. See [guest networks for smart home devices]({{< relref "/guides/guest-wifi-network-smart-home-devices" >}}).
- **Change the router's admin password** too, and work through our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}).

If your router no longer gets security updates, see [is my router still getting security updates]({{< relref "/guides/is-my-router-still-getting-security-updates" >}}).

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| eero: find devices on the Home or Devices tab; Block device stops rejoining even with the correct password; not available in bridge mode; inactive devices drop off after 7 days | [eero Support](https://eero.com/support/articles/how-do-i-block-unwanted-devices-on-my-network) | Verified as of October 17, 2026 |
| Google: Home, Wi-Fi, Devices; list covers the last 30 days, including offline devices; page doesn't cover blocking | [Google Home Help 6263633](https://support.google.com/googlehome/answer/6263633) | Verified as of October 17, 2026 |
| Netgear: Attached Devices at routerlogin.net shows name, IP, MAC and Allowed or Blocked status; IP can change, MAC doesn't | [Netgear KB 24230, updated July 7, 2025](https://kb.netgear.com/24230/How-do-I-view-the-devices-that-are-connected-to-my-network-from-my-Nighthawk-router) | Verified; the article doesn't give blocking steps |
| ASUS: Network Map, Clients; details include manufacturer, band and signal; Block Internet Access | [ASUS FAQ 1005513](https://www.asus.com/support/FAQ/1005513) | Verified; the page shows no update date, and app menu names may vary |
| Apple devices use a different private address per network; Fixed by default on WPA2 or stronger, Rotating every two weeks on weak or open networks | [Apple Support 102509](https://support.apple.com/en-us/102509) | Verified as of October 17, 2026 |

## Bottom line

Check your router's device list every so often and name what you recognize. Most unknown entries are your own gear, especially Apple devices using private addresses. If something truly isn't yours, block it and change your Wi-Fi password.
