---
title: "Private Wi-Fi Address: Should You Turn It Off?"
date: 2026-10-28T05:00:00Z
description: "Keep your private Wi-Fi address on in public. At home, turn it off or use Fixed on an iPhone only if IP reservations, parental controls or blocking break."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "how-to-fixes"]
tags: ["private-wifi-address", "mac-randomization", "iphone", "android", "windows", "parental-controls", "dhcp-reservation", "eero", "asus", "linksys"]
summary: "Leave your private Wi-Fi address on for public and work networks: it makes it harder for networks to track your device by its hardware address. On your home network, turn it off (or, on an iPhone with iOS 18 or later, set it to Fixed) only if a router feature that relies on a device's address, such as IP reservations, parental-control schedules or device blocking, stops working."
imageAlt: "Hand holding an iPhone showing its home screen, with blurred shoppers walking on a city street behind it"
imageCredit: "Photo: Frederik Lipfert / [Unsplash](https://unsplash.com/photos/a-person-holding-an-iphone-in-their-hand-y67dwfB2AiM)"
takeaways:
  - "A private Wi-Fi address replaces your device's hardware (MAC) address on a network. Apple says a constant address \"allows a kind of user tracking or profiling.\""
  - "On iOS 18 and later, Apple offers Off, Fixed and Rotating. Fixed keeps one private address per network; Rotating changes it every two weeks."
  - "Android 10 and later use a randomized address by default. In its default mode it stays the same for a network until a factory reset."
  - "Router features that identify devices by address can break when the address changes: eero lists IP reservations, port forwarding, pausing and blocking, and profile schedules."
  - "Try the gentle fix first. Linksys recommends Fixed over Rotating, and Apple says to update your software before deciding to turn the feature off."
faq:
  - q: "Is it safe to turn off private Wi-Fi address at home?"
    a: "On a home network you control and secure with a strong password, the privacy gain is small. eero says the protection \"may not be necessary for devices in your home.\" Keep it on for public, hotel and work networks, where tracking is the concern."
  - q: "Why does my iPhone show up as a new device on my router?"
    a: "Usually because its Wi-Fi address changed. ASUS says that after a device gets a new address, \"that device appears in device list as a newly connected device.\" Setting the network to Fixed on iOS 18 or later, or turning the private address off, stops that."
  - q: "Does forgetting a Wi-Fi network change my private address?"
    a: "On an iPhone, usually yes: Apple says forgetting a network also forgets its private address, unless you already forgot that network within the past 24 hours (iOS 18 and later; two weeks on earlier versions). On Android's default mode, no; Google says the address \"doesn't get re-randomized if you forget and re-add the Wi-Fi network.\""
  - q: "Do I need to turn it off for a DHCP reservation to work?"
    a: "Not always. A reservation ties an IP address to a device's MAC address, so it holds as long as that address doesn't change. Apple's Fixed setting and Android's default persistent mode both keep one address per network. A Rotating address will break it when the address changes, about every two weeks."
sources:
  - title: "Use private Wi-Fi addresses on Apple devices"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-nz/102509"
    date: 2025-12-09
  - title: "Manage private Wi-Fi settings on iPhone and iPad"
    publisher: "Apple Support"
    url: "https://support.apple.com/guide/platform-support/sup56da67cfd/web"
  - title: "MAC randomization behavior"
    publisher: "Android Open Source Project"
    url: "https://source.android.com/docs/core/connect/wifi-mac-randomization-behavior"
    date: 2026-10-09
  - title: "Connect to a Wi-Fi network in Windows"
    publisher: "Microsoft Support"
    url: "https://support.microsoft.com/windows/060ad2e9-526e-4f1c-9f3d-fe6a842640ed"
  - title: "What is MAC Address Randomization?"
    publisher: "eero"
    url: "https://eero.com/support/articles/what-is-mac-address-randomization"
  - title: "Why do I see my device multiple times on the device list of the ASUS Router? (Random MAC Address)"
    publisher: "ASUS"
    url: "https://www.asus.com/us/support/FAQ/1044277"
    date: 2026-02-10
  - title: "How MAC randomization affects the way Linksys sees my devices"
    publisher: "Linksys"
    url: "https://support.linksys.com/kb/article/170"
---

Keep your private Wi-Fi address turned on for public, hotel and work networks; it makes it harder for networks to track your phone or laptop across locations by its permanent hardware address. On your own home network, turn it off, or on an iPhone running iOS 18 or later set it to **Fixed**, only if a router feature that relies on recognizing a device stops working. The usual culprits are IP reservations, port forwarding, parental-control schedules and device blocking.

## What a private Wi-Fi address is

Every Wi-Fi device has a hardware address, called a MAC address, that networks use to tell devices apart. If a phone used the same address everywhere, any network it joined could recognize it. Apple's explanation: a constant address "allows a kind of user tracking or profiling that affects all devices on all Wi-Fi networks."

A private (or randomized) address replaces the hardware address with a made-up one. Apple calls it **Private Wi-Fi Address**, on many Android phones the setting is called **MAC address type**, and Windows calls it **Random hardware addresses**. They work differently in one important way: how often the address changes.

## How often the address changes

### iPhone, iPad and Mac

On iOS 18, iPadOS 18, macOS Sequoia 15 and later, Apple offers three settings per network:

- **Fixed:** "your device uses a private address, but the private address doesn't rotate." Your router sees one consistent, made-up address.
- **Rotating:** "your device uses a private address that rotates to a different private address every two weeks."
- **Off:** "your device uses its hardware MAC address."

Earlier versions have a simple on/off switch. Apple sets new networks to Fixed by default when they use WPA2 or stronger security, and to Rotating when security is weak or missing.

A Fixed address can still change. Apple says resetting network settings gives a device "a different private address the next time it joins the network," and forgetting a network also forgets its private address, unless you last forgot that network less than 24 hours earlier (two weeks on versions before iOS 18).

### Android

Google's Android documentation says: "For devices running Android 10 or higher, the framework uses a randomized MAC address by default." In its default, persistent mode, the address is tied to the network profile and "remains the same until a factory reset." Google adds that it "doesn't get re-randomized if you forget and re-add the Wi-Fi network."

Android 12 and later also have a non-persistent mode that re-randomizes, for example when "the current randomized MAC for the network profile was generated more than 24 hours ago." Google says it is used only for certain networks, such as those set up by an app that requests it. Phone makers can change these menus, so your settings may look different.

### Windows

If your Wi-Fi hardware supports it, Windows 11 and Windows 10 have a **Random hardware addresses** switch, either for all networks or for one network. Microsoft says it can "make it harder for people to track you when your device scans for networks and connects."

## What breaks when the address changes

Your router remembers devices by their address. When the address changes, the router sees a stranger. Router makers list the features that stop working:

| Router maker | Features it says are affected |
|---|---|
| eero | IP reservations and port forwarding; new device notifications; device nicknames; pausing and blocking devices; profile assignment and schedules |
| ASUS | Parental-control content filters, schedules and internet blocking; manually assigned IPs; MAC and IP binding; wireless MAC filter |
| Linksys | Parental-control schedules; MAC filtering; Instant-Privacy (an iOS device may not reconnect) |

ASUS sums it up: "Any MAC related features will be affected." Linksys gives a practical example for parental controls: a scheduled block fails because "the device keeps getting online during the scheduled time."

You'll also see more unknown entries in your router's device list. ASUS says a device with a new address "appears in device list as a newly connected device." Our guide to [seeing who's connected to your Wi-Fi]({{< relref "/guides/see-who-is-connected-to-my-wifi" >}}) covers how to tell those apart from real intruders.

Note what's on these lists: features that rely on recognizing a device. A private address doesn't stop the internet working for most people. Apple says that if a device can't join a network or reach the internet, "you should install the latest software updates. Then try again before you decide whether to turn this feature off."

## When to turn it off (and when Fixed is enough)

**Leave it on** for coffee shops, airports, hotels, and any network you don't run. eero calls randomization "a good way to protect your privacy in public places."

**Use Fixed (or Android's default) at home** if you just want your router to recognize your devices. Linksys recommends Fixed because it "will use a unique, non-rotating MAC address," and says Rotating is "NOT recommended" if you use parental controls or MAC filtering. A Fixed address is enough for a DHCP reservation or a port-forwarding rule to keep working, as long as you don't reset network settings or forget the network. Our [port forwarding guide]({{< relref "/guides/how-to-set-up-port-forwarding" >}}) explains why the reservation comes first.

**Turn it off** for a device on your home network when:

- A parental-control schedule or block on a child's device keeps getting around the rules.
- You use MAC filtering or an allow list on your router.
- A device keeps losing its reserved IP address or showing up as new.
- An older Apple device only offers on or off, and you need a stable address.

eero says the protection "may not be necessary for devices in your home." On a network you control and secure yourself, there's less to protect against. The trade-off is small at home and larger anywhere else, so change it per network, not everywhere.

## How to change it

**iPhone or iPad:** Open Settings > Wi-Fi, tap the More Info button next to your network, then set **Private Wi-Fi Address** to Off, Fixed or Rotating (iOS 18 and later) or switch it off on earlier versions.

**Mac:** Open System Settings > Wi-Fi, click Details next to your network, then choose from the **Private Wi-Fi Address** menu.

**Android:** Settings > Network and Internet > Wi-Fi, tap the gear next to your home network, tap **MAC address type**, then choose **Device MAC** (ASUS's steps; menu names vary by phone maker).

**Windows 11:** Settings > Network & internet > Wi-Fi > Manage known networks, pick your network, and set **Random hardware addresses**.

After you change it, the device may reconnect and appear in your router's list under its new address. Delete the old entry and redo any reservation or parental-control assignment for that device. If a device still drops off your network after this, see our guide to [why Wi-Fi keeps disconnecting]({{< relref "/guides/wifi-keeps-disconnecting" >}}).

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Off, Fixed and Rotating options; Rotating changes every two weeks; tracking rationale; update before turning off | [Apple Support](https://support.apple.com/en-nz/102509) | Verified |
| Resetting network settings gives a new private address; private addresses can interfere with systems that rely on device identification | [Apple Support](https://support.apple.com/guide/platform-support/sup56da67cfd/web) | Verified |
| Android 10+ randomizes by default; persistent address lasts until factory reset and survives forgetting the network; non-persistent mode conditions | [Android Open Source Project](https://source.android.com/docs/core/connect/wifi-mac-randomization-behavior) | Verified |
| Windows Random hardware addresses setting and purpose | [Microsoft Support](https://support.microsoft.com/windows/060ad2e9-526e-4f1c-9f3d-fe6a842640ed) | Verified |
| eero features affected; useful in public, may not be necessary at home | [eero](https://eero.com/support/articles/what-is-mac-address-randomization) | Verified |
| ASUS features affected; device appears as new; Android steps | [ASUS](https://www.asus.com/us/support/FAQ/1044277) | Verified |
| Linksys recommends Fixed over Rotating; parental-control schedules fail | [Linksys](https://support.linksys.com/kb/article/170) | Verified |
