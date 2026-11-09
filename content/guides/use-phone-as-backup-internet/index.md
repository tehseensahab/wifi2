---
title: "How to Use Your Phone as Backup Internet for Your Router"
date: 2026-11-09T05:05:00Z
description: "How to use your phone as backup internet for your router: USB tethering on ASUS and GL.iNet, eero Hotspot Backup, failover settings and data-plan limits."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "routers", "internet-plans-isps"]
tags: ["backup-internet", "usb-tethering", "personal-hotspot", "dual-wan", "failover", "asus", "gl-inet", "eero"]
summary: "Plug your phone into the router's USB port and turn on USB tethering (Android) or Personal Hotspot (iPhone); supported ASUS and GL.iNet routers can then use it as a backup connection and fail over to it automatically. eero routers can't use USB, but eero Hotspot Backup can join your phone's Wi-Fi hotspot with eero Plus or a qualifying ISP or Ring subscription. Check your carrier's hotspot allowance first."
imageAlt: "Hand holding a gray iPhone with a small USB-C accessory plugged into its port"
imageCredit: "Photo: Matúš Gocman / [Unsplash](https://unsplash.com/photos/BNecSx2aUq8)"
takeaways:
  - "Your phone can act as your home's backup internet in two ways: plugged into the router's USB port (tethering) or as a Wi-Fi hotspot the router joins."
  - "ASUS supports USB tethering on specific Wi-Fi 6 models and firmware; its Android guide says Dual WAN turns on automatically. Set it to Failover so the phone is used only when the main line drops."
  - "GL.iNet routers list Tethering as an interface in Multi-WAN, which fails over by priority and switches back when the main connection returns."
  - "eero Hotspot Backup uses your phone's Wi-Fi hotspot, not USB, and needs eero Plus or a qualifying ISP or Ring subscription."
  - "Carriers can limit or charge for tethering, and you pay for the data. Limit backup to the devices that need it."
faq:
  - q: "Can I plug my phone into my router for internet?"
    a: "On some routers, yes. ASUS supports USB tethering on specific Wi-Fi 6 (802.11ax) models with certain firmware versions, and GL.iNet routers with a USB port support it in firmware 4. Many routers, including eero, don't accept a phone over USB."
  - q: "Is USB tethering better than a Wi-Fi hotspot for backup internet?"
    a: "USB tethering avoids a second Wi-Fi link in the house and keeps the phone in one place next to the router. A Wi-Fi hotspot works with routers that have no USB tethering support, such as eero with Hotspot Backup. Speed depends mainly on your cellular signal and plan either way."
  - q: "Will my router switch back to the main internet automatically?"
    a: "It depends on the router. GL.iNet's Multi-WAN switches back when a higher-priority link returns. ASUS reverts to the primary WAN only if you enable the failback option in Dual WAN settings."
  - q: "Does using my phone as backup internet cost extra?"
    a: "It can. Google and GL.iNet both note that some carriers limit or charge extra for tethering, and Apple says Personal Hotspot needs a carrier that supports it. eero says you're responsible for data charges. Check your plan's hotspot allowance."
  - q: "Do I need an iPhone or Android for USB tethering to a router?"
    a: "Either can work. ASUS and GL.iNet both publish steps for iPhone (Personal Hotspot, then tap Trust when prompted) and Android (turn on USB tethering)."
sources:
  - title: "Plug, Share & Surf: Turn Your ASUS Router into a 4G/5G Hotspot Instantly (4G / 5G Auto Mobile Tethering)"
    publisher: "ASUS"
    url: "https://www.asus.com/us/support/FAQ/1050074"
    date: 2026-03-03
  - title: "How to set up a smartphone to share the network to the router (USB Tethering)?"
    publisher: "ASUS"
    url: "https://asus.com/support/faq/1045247"
    date: 2024-07-11
  - title: "Dual WAN introduction and setup - Failover and Load Balance"
    publisher: "ASUS"
    url: "https://www.asus.com/support/FAQ/1011719"
    date: 2025-08-13
  - title: "Internet: Tethering"
    publisher: "GL.iNet"
    url: "https://docs.gl-inet.com/router/en/4/interface_guide/internet_tethering/"
  - title: "Multi-WAN"
    publisher: "GL.iNet"
    url: "https://docs.gl-inet.com/router/en/4/interface_guide/multi-wan/"
  - title: "How do I set up and manage eero Hotspot Backup?"
    publisher: "eero"
    url: "https://eero.com/support/articles/how-do-i-set-up-and-manage-eero-hotspot-backup"
  - title: "Share a mobile connection by hotspot or tethering on Android"
    publisher: "Google"
    url: "https://support.google.com/android/answer/9059108?hl=en"
  - title: "How to set up a Personal Hotspot on your iPhone or iPad"
    publisher: "Apple"
    url: "https://support.apple.com/kb/ht4517"
    date: 2026-05-07
---

You can use your phone as backup internet for your whole home by connecting it to your router as a second internet source. On routers that support it, such as some ASUS models on supported firmware and GL.iNet routers, you plug the phone into the router's USB port and turn on USB tethering (Android) or Personal Hotspot (iPhone); once you set the router to fail over, it switches to the phone when your main connection fails. On routers without USB tethering, such as eero, the router can instead join your phone's Wi-Fi hotspot, which eero calls Hotspot Backup and which needs eero Plus or a qualifying ISP or Ring subscription. Either way, check your carrier's hotspot allowance before an outage, because the backup runs on your phone plan's data.

This guide covers the setup steps from ASUS, GL.iNet, eero, Apple and Google, and the settings that decide whether the switch happens on its own. If you'd rather have a dedicated cellular backup that doesn't tie up your phone, see our [best dual WAN router guide](/guides/best-dual-wan-router/) and [eero Signal 4G vs. 5G comparison](/guides/eero-signal-4g-vs-5g/).

## Two ways to connect your phone

**USB tethering.** The phone plugs into the router's USB port and acts as its internet connection. GL.iNet's definition: "Using a USB cable to share network from your smartphone to the router is called Tethering." The phone stays put next to the router. Google's advice for tethering is to "plug in your devices while tethering," and to turn tethering off when you're done, to save battery.

**Wi-Fi hotspot.** The phone creates a Wi-Fi network and the router connects to it as a client. This works on routers that don't take a phone over USB, but the phone has to stay within Wi-Fi range of the router with its hotspot turned on.

Which one you use depends on your router. Check the maker's support pages for "USB tethering," "mobile tethering" or "hotspot backup" before you rely on it.

## Before you start: check your phone plan

Tethering uses your phone plan's data, and not every plan allows it. Google's Android help says, "Some mobile carriers limit or charge extra for tethering. We recommend checking with your carrier," and GL.iNet's documentation says the same. Apple says Personal Hotspot "requires a wireless carrier that supports Personal Hotspot" and notes that extra fees may apply.

Your carrier's hotspot allowance may be smaller than your phone's own data allowance, and a whole house of devices can use it up fast. Plan to limit backup to the devices that need it, such as work laptops, and pause cloud backups and streaming while you're on it.

## ASUS routers: USB tethering with Dual WAN

ASUS calls the feature 4G/5G Auto Mobile Tethering. Its US support article says it is "available for specific 802.11ax models with certain firmware versions," listing firmware between 3.0.0.4.388.23000 and 3.0.0.4.388.29999, firmware beyond 3.0.0.4.388.31900, and 3.0.0.4.386 firmware beyond build 69019. ASUS doesn't name the models, so update your router's firmware first and check for the feature.

**Set up the phone:**

1. **iPhone:** turn on Personal Hotspot, then plug the iPhone into the router's USB port. ASUS says: "Tap 'Trust' if you receive an alert that says Trust this computer?"
2. **Android:** plug the phone into the router's USB port, then turn on USB tethering in the phone's network settings. On many Android phones, Google's steps are: swipe down from the top of the screen, "Touch and hold Hotspot," then "Turn on USB tethering." Menu names vary by phone maker.
3. When it works, ASUS says, "Upon the availability of your backup WAN, you shall see the hotspot icon" in the router's interface.

ASUS's older tethering guide for Android says that "once setup is applied, Dual WAN is automatically enabled." Dual WAN is what decides how the phone is used.

**Make it a backup, not a second line:**

1. In the router's web interface, go to **WAN > Dual WAN**. ASUS's path is "Go to WAN > Dual WAN > Switch the button on [Enable Dual WAN] to ON (Default is OFF)."
2. Make sure your normal connection (WAN) is the primary WAN and USB is the secondary WAN.
3. Choose **Failover** mode. ASUS: "Select Failover mode to use a secondary WAN for backup network access." Avoid Load Balance for a phone, since it spreads everyday traffic across your phone's data.
4. Turn on **Allow Failback**. ASUS says the connection "will revert to the Primary WAN if failback has been enabled." Without it, the router can stay on your phone after the main line comes back.

ASUS says that in Failover mode the router detects an outage "by periodically sending DNS queries." Our [best dual WAN router guide](/guides/best-dual-wan-router/) covers ASUS's Dual WAN in more detail.

## GL.iNet routers: Tethering and Multi-WAN

GL.iNet's firmware 4 documentation covers tethering for both phone types:

1. **iPhone:** go to Settings > Personal Hotspot and turn on "Allow Others to Join," then plug the phone into the router. GL.iNet notes that "a system dialog will appear asking whether to trust the device"; tap Trust.
2. **Android:** turn on USB tethering in your phone's hotspot settings (GL.iNet notes the exact steps vary by brand), then plug it in.
3. In the router's admin panel, open **INTERNET**, find the **Tethering** section and click **Connect**.

Use a USB cable that supports data transfer, not a charge-only cable.

GL.iNet handles backup through Multi-WAN. "There are two modes for Multi-WAN: Failover and Load Balance," the documentation says, and Tethering appears in the interface list. In Failover mode, each connection has a priority. If the active link fails, the router moves to the next available interface with the highest priority, and it switches back automatically when the higher-priority link returns. Put your main Ethernet WAN at the top and Tethering below it. GL.iNet warns that raising the detection sensitivity "may lead to network disconnection, please adjust it with caution," so leave it at the default unless failover is too slow. If you use a GL.iNet router on the road too, our [best travel router guide](/guides/best-travel-router/) covers the models.

## eero: Hotspot Backup over Wi-Fi

eero routers don't use a USB-connected phone. eero says plainly: "USB and Ethernet based backup internet sources are not supported." Instead, eero Hotspot Backup connects to your phone's Wi-Fi hotspot or another nearby Wi-Fi network.

Requirements, per eero:

- An eero Plus subscription "or qualifying ISP or Ring subscription, all sold separately." Our [Is eero Plus worth it? guide](/guides/is-eero-plus-worth-it/) covers what else it includes.
- The eero app at version 6.25.1 or later and eeroOS 6.13.0 or later.
- A network not running in bridge mode, and not on TKIP Wi-Fi encryption.

To set it up, turn on your phone's hotspot (Personal Hotspot on iPhone, Hotspot in Android's quick settings), then add it in the eero app. Under the Home tab, **Security & privacy > eero Hotspot Backup > Devices with access** lets you "uncheck any devices that you don't want to switch to backup internet in the event of an outage." That's the easiest way to keep a smart TV from eating your hotspot data.

eero is clear about limits: "eero does not guarantee zero disruption and brief network downtime may occur during failover," and the "customer is responsible for applicable data charges."

## Tips that make phone backup work

- **Test it before you need it.** Unplug the cable from your modem or ONT and confirm the router switches to the phone, then plug it back in and confirm it switches back.
- **Keep the phone charged.** Don't count on the router's USB port to keep the phone topped up; keep a charger with it, especially for a Wi-Fi hotspot.
- **Check the signal where the router is.** The router's spot may not be where your phone gets its best cellular signal. If it isn't, a longer USB data cable or a Wi-Fi hotspot placed elsewhere can help.
- **Remember the router's power.** During a power outage, phone backup only helps if the router itself has power. Our [best UPS for router and modem guide](/guides/best-ups-for-router/) covers keeping it on.
- **Expect slower, variable speeds.** Speed depends on your cellular signal and plan, and eero notes that high-bandwidth activities such as 4K streaming may perform differently on a phone hotspot.

## Bottom line

If your router supports USB tethering, it's the tidiest phone backup: plug the phone in, set the connection to Failover with failback turned on, and test it once. If it doesn't, a Wi-Fi hotspot backup such as eero's does the same job without a cable, but it needs a subscription. Either way, your data plan is the real limit, so treat a phone as a short-term bridge through outages, not a second home internet line.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| ASUS Auto Mobile Tethering on specific 802.11ax models with listed firmware; iPhone and Android steps; Trust prompt | [ASUS FAQ 1050074](https://www.asus.com/us/support/FAQ/1050074) (updated Mar. 3, 2026) | Verified |
| ASUS: Dual WAN enabled automatically after tethering setup | [ASUS FAQ 1045247](https://asus.com/support/faq/1045247) (updated Jul. 11, 2024) | Qualified: older Android guide |
| ASUS Dual WAN path, Failover, failback, DNS-query detection | [ASUS FAQ 1011719](https://www.asus.com/support/FAQ/1011719) (updated Aug. 13, 2025) | Verified |
| GL.iNet tethering steps and Multi-WAN failover by priority | [GL.iNet Tethering](https://docs.gl-inet.com/router/en/4/interface_guide/internet_tethering/); [GL.iNet Multi-WAN](https://docs.gl-inet.com/router/en/4/interface_guide/multi-wan/) | Verified |
| eero Hotspot Backup requirements, no USB, data charges, failover downtime | [eero Support](https://eero.com/support/articles/how-do-i-set-up-and-manage-eero-hotspot-backup) | Verified |
| Carriers may limit or charge for tethering | [Google Android Help](https://support.google.com/android/answer/9059108?hl=en); [GL.iNet Tethering](https://docs.gl-inet.com/router/en/4/interface_guide/internet_tethering/); [Apple Support](https://support.apple.com/kb/ht4517) | Verified |
