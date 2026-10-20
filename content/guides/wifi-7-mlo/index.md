---
title: "Wi-Fi 7 MLO Explained: Should You Turn It On?"
date: 2026-10-20T05:30:00Z
description: "Wi-Fi 7 MLO links a device to your router over more than one band, if both support it. What it does, which modes exist, what it breaks and when to turn it on."
authors: ["Craig Leslie"]
topics: ["wifi-6e-7", "how-to-fixes"]
tags: ["wifi-7", "mlo", "multi-link-operation", "802.11be", "wpa3", "eero", "asus", "router-settings"]
summary: "Multi-Link Operation (MLO) lets a Wi-Fi 7 device link to a Wi-Fi 7 router over more than one band, either at the same time or by switching quickly between them. It only works when both ends support it, and PCWorld reports that most MLO devices, Windows PCs especially, use a mode that switches bands rather than combining them. Turn it on if your main devices are Wi-Fi 7; turn it off if older devices stop connecting."
imageAlt: "A white Wi-Fi router with four tall antennas lit by blue and pink light"
imageCredit: "Photo: Jakub Żerdzicki / [Unsplash](https://unsplash.com/photos/a-white-laptop-computer-sitting-on-top-of-a-table-4kdGXUOKwcI)"
takeaways:
  - "MLO is a Wi-Fi 7 feature that the Wi-Fi Alliance says lets a device transmit and receive on more than one link at the same time."
  - "Both the router and the device must support MLO. Wi-Fi 6 and Wi-Fi 6E devices can still join, one band at a time, unless the security settings MLO turns on block them."
  - "ASUS describes two MLO modes, STR and eMLSR, and says which one is used depends on the client device."
  - "Turning MLO on can switch your network to WPA3 or GCMP-256 encryption, which some older devices can't use. eero and ASUS both warn about this."
  - "MLO can't make your internet plan faster. eero says it only helps the router use the speed your provider already delivers."
faq:
  - q: "What does MLO do in Wi-Fi 7?"
    a: "It lets a Wi-Fi 7 device connect to a Wi-Fi 7 router over more than one band, such as 5 GHz and 6 GHz, instead of just one. Depending on the mode, the device either uses the bands at the same time or switches quickly to whichever is clearer."
  - q: "Should I turn MLO on or off?"
    a: "Turn it on if your router supports it and your main phones and laptops are Wi-Fi 7. Turn it off, or put older gear on a separate network, if devices that don't support WPA3 start failing to connect."
  - q: "Does my iPhone support MLO?"
    a: "Apple's Wi-Fi specifications page, dated September 17, 2026, says its models with the N1 wireless chip support Wi-Fi 7 and MLO. That list starts with the iPhone 17, iPhone Air and iPhone 17 Pro and includes newer iPhones, some iPads and the latest MacBooks. The same page lists the iPhone 16 family as 802.11ax and doesn't claim MLO for it."
  - q: "Does Windows support MLO?"
    a: "Wi-Fi 7 features on Windows, MLO among them, need Windows 11 version 24H2 or later, a Wi-Fi 7 adapter and an up-to-date driver. PCWorld reports that most Windows PCs use the band-switching form of MLO rather than combining bands."
  - q: "Will MLO make my internet faster?"
    a: "No. MLO works between your router and your device. eero says it won't increase your ISP speed; it can only help your network use the speed you already pay for."
sources:
  - title: "Wi-Fi Alliance unveils Wi-Fi CERTIFIED 7"
    publisher: "Wi-Fi Alliance"
    url: "https://wi-fi.org/media-content/wi-fi-alliance-unveils-wi-fi-certified-7"
    date: 2024-01-08
  - title: "What is Multi-Link Operation (MLO)?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/what-is-multi-link-operation-mlo"
    date: 2026-10-20
  - title: "[Wi-Fi 7 Wireless Router] What is MLO (Multi-Link Operation) and how it works?"
    publisher: "ASUS"
    url: "https://www.asus.com/support/FAQ/1053342"
    date: 2025-03-26
  - title: "Wi-Fi specifications for Apple devices"
    publisher: "Apple Platform Deployment"
    url: "https://support.apple.com/guide/deployment/dep268652e6c"
    date: 2026-09-17
  - title: "Microsoft brings Wi-Fi 7 support to Windows 11"
    publisher: "Windows Central"
    url: "https://www.windowscentral.com/software-apps/windows-11/microsoft-brings-wi-fi-7-support-to-windows-11-with-latest-preview-build-coming-to-everyone-later-this-year"
    date: 2024-02-22
  - title: "How to unlock Wi-Fi 7's full speed in Windows 11"
    publisher: "PCWorld"
    url: "https://www.pcworld.com/article/2824823/how-to-unlock-wi-fi-7s-full-blistering-speed-in-windows-11.html"
    date: 2025-07-21
  - title: "Wi-Fi 7 MLO (Multi-Link Operation) explained"
    publisher: "Dong Knows Tech"
    url: "https://dongknows.com/wi-fi-7-mlo-multi-link-operation-explained/"
  - title: "The Disappointing Truth About Wi-Fi 7"
    publisher: "RTINGS.com"
    url: "https://www.rtings.com/router/learn/research/wifi-7-mlo"
---

Multi-Link Operation (MLO) is the Wi-Fi 7 feature that lets a device connect to your router over more than one band at once, for example 5 GHz and 6 GHz together, instead of being stuck on one. It only works when both the router and the device support it, and PCWorld reports that most MLO devices use a mode that hops between bands rather than combining them. So expect a steadier connection more than a faster one. Turn MLO on if your router offers it and your main devices are Wi-Fi 7; turn it off, or move older gear to a separate network, if devices start failing to connect.

This explainer draws on the Wi-Fi Alliance, router makers' support pages, Apple's and Microsoft's device documentation, and independent coverage. We have not measured MLO ourselves.

## What is MLO?

Before Wi-Fi 7, a phone or laptop joined one band at a time. It could move from 5 GHz to 2.4 GHz as you walked away from the router, but it couldn't use both. When the Wi-Fi Alliance launched Wi-Fi CERTIFIED 7 in January 2024, it said MLO "allows a device to transmit and receive simultaneously on more than one link." It gave two ways that can help: combining bands or channels for more capacity, and sending a time-sensitive packet on whichever link is free soonest.

eero's version of the same idea: MLO "enables your Wi-Fi 7 devices to simultaneously send or receive data across multiple wifi frequency bands and channels." eero also notes that MLO isn't tied to 6 GHz, so a dual-band Wi-Fi 7 router can use it across 2.4 and 5 GHz.

## The two MLO modes you'll see

Router settings and spec sheets mention modes with unfriendly names. ASUS's MLO FAQ names the two that matter:

- **STR (Simultaneous Transmit and Receive).** ASUS says devices in this mode "manage multiple Wi-Fi connections on different channels or frequencies simultaneously." Because bands are used at once, this is the mode that can add capacity.
- **eMLSR (enhanced Multi-Link Single Radio).** ASUS says this mode focuses on optimizing how multi-link connections are set up and recovered, which helps when conditions change quickly. Dong Knows Tech describes it as letting a device switch dynamically among the available bands.

ASUS says its routers support both, but "it will base on client devices supported modes." In other words, your phone or laptop decides. Independent reviewer Dong Ngo of Dong Knows Tech reports that common Wi-Fi 7 laptop cards such as Intel's BE200 use eMLSR and that this mode "does not increase data rates." PCWorld likewise says Windows PCs usually support only the single-radio variant. ASUS notes that most phones that do support STR currently pair the 2.4 GHz and 5 GHz bands.

## What you need for MLO to work

| Requirement | What to check |
|---|---|
| A Wi-Fi 7 router with MLO in its firmware | eero lists MLO on the eero 7, eero Pro 7, eero Max 7, eero PoE 7 and eero Outdoor 7 with current firmware. ASUS's FAQ, last updated March 2025, lists minimum firmware for the GT-BE96, RT-BE96U, GT-BE98 and GT-BE98 Pro; newer ASUS models aren't covered there. |
| A Wi-Fi 7 device that supports MLO | eero says devices without MLO support can't use multiple bands. Wi-Fi 6 and 6E devices still connect, one band at a time. |
| iPhone, iPad or Mac | Apple's specifications page, dated September 17, 2026, says models with its N1 wireless chip, starting with the iPhone 17, iPhone Air and iPhone 17 Pro, support Wi-Fi 7 and MLO. It lists a maximum channel width of 160 MHz on 5 and 6 GHz. It lists the iPhone 16 family as 802.11ax. |
| Windows PC | Windows 11 version 24H2 or later, a Wi-Fi 7 adapter and a current driver. PCWorld cites Intel's driver notes saying Wi-Fi 7 features on its BE200, BE201 and BE202 cards start with 24H2. |
| Matching network settings | PCWorld notes MLO needs the same network name and password across the bands it combines. |

Not sure whether your router or devices are Wi-Fi 7 at all? Our [Wi-Fi 6E vs. Wi-Fi 7]({{< relref "/guides/wifi-6e-vs-wifi-7" >}}) guide explains what to look for on the box.

## What turning on MLO can break

The most common side effect is security, not speed.

- **Older devices may drop off.** eero says that when 6 GHz is present and MLO is on, WPA3 is enabled by default on the MLO bands, and that this affects other bands on the network too. Devices that don't support WPA3 "may have difficulty connecting." ASUS uses GCMP-256 encryption for its MLO networks and warns that it may be incompatible with some legacy devices. Our [WPA2 vs. WPA3]({{< relref "/guides/wpa2-vs-wpa3" >}}) guide explains the difference.
- **Mixed mesh systems.** eero recommends turning MLO off if your network mixes Wi-Fi 7 and older eero units. ASUS says that with MLO on, an AiMesh node that doesn't support MLO won't broadcast 6 GHz.
- **A network restart.** eero says enabling MLO reboots the whole network, which takes about two minutes.
- **Battery and power.** eero notes that using more and wider channels at once may use more energy, and that some phones use fewer bands to save power, which could limit their maximum throughput.

eero also says plainly that MLO "is still being developed and tested" and that behavior varies by device maker.

## Does MLO help mesh backhaul?

It can, with limits. Some mesh systems use MLO on the link between units, not just to your devices. ASUS says that in an AiMesh system only the first node can use MLO backhaul, and only with the same router model. Dong Knows Tech reports that MLO backhaul generally needs units of the same model and a star layout, where each satellite connects straight to the main router; in a daisy chain, the second hop doesn't get it. If you can run a cable, a wired link is still simpler and more predictable; see our guide to [wired vs. wireless backhaul]({{< relref "/guides/mesh-wifi-wired-vs-wireless-backhaul" >}}).

## What MLO won't do

MLO works between your router and your devices. It can't make your internet plan faster: eero says it won't increase your ISP speed and can only help the network use the throughput your provider delivers. Independent testing has also tempered expectations. RTINGS.com summarizes its own MLO testing, in a research article last updated February 18, 2026, as revealing "shallow implementations and marketing that oversells the hardware."

## Should you turn MLO on?

| Your situation | What to do |
|---|---|
| Wi-Fi 7 router, and your main phones and laptops are Wi-Fi 7 with MLO support | Turn it on and check that everything reconnects |
| Many older smart home devices, printers or streaming sticks | Leave it off, or keep them on a separate network without MLO |
| Mesh system mixing Wi-Fi 7 and older units | Leave it off; eero recommends this for mixed eero networks |
| Devices fail to connect after turning it on | Turn it off, or turn off WPA3 for legacy devices where your router allows it |
| You want faster internet | MLO won't change your plan's speed |

## How to turn MLO on or off

- **eero:** in the eero app, go to Settings > Advanced networking > Wireless > Multi-link operation. eero lists app version 6.50 and recent firmware as requirements.
- **ASUS:** in the web interface or ASUS Router app, open Network > Main network profile > Advanced Settings and turn on Multi-Link Operation (MLO). ASUS also lets you create a separate MLO network, which keeps older devices on your main network untouched.

## Bottom line

MLO is one of Wi-Fi 7's headline features, but it only pays off when both ends support it. PCWorld reports that most MLO devices today use the band-switching mode rather than combining bands. If your devices are Wi-Fi 7, turn it on and watch for anything that drops off. If you rely on older gear, leaving it off, or giving MLO its own network, costs you little.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| MLO lets a device transmit and receive on more than one link at the same time; can combine links or pick the soonest-available one | [Wi-Fi Alliance](https://wi-fi.org/media-content/wi-fi-alliance-unveils-wi-fi-certified-7) | Verified |
| eero MLO: supported models, not tied to 6 GHz, WPA3 default with 6 GHz, legacy-device warning, network reboot, mixed-network advice, won't raise ISP speed, menu path | [eero Support](https://eero.com/support/articles/what-is-multi-link-operation-mlo) | Verified |
| ASUS: STR and eMLSR modes; mode depends on client; supported models and firmware; GCMP-256; AiMesh MLO backhaul limits; menu path | [ASUS FAQ 1053342](https://www.asus.com/support/FAQ/1053342) | Verified |
| Apple N1-chip models support Wi-Fi 7 and MLO; 160 MHz maximum listed | [Apple Platform Deployment](https://support.apple.com/guide/deployment/dep268652e6c) | Verified (page dated September 17, 2026) |
| Wi-Fi 7 on Windows needs Windows 11 24H2, Wi-Fi 7 hardware and a current driver | [Windows Central](https://www.windowscentral.com/software-apps/windows-11/microsoft-brings-wi-fi-7-support-to-windows-11-with-latest-preview-build-coming-to-everyone-later-this-year); [PCWorld](https://www.pcworld.com/article/2824823/how-to-unlock-wi-fi-7s-full-blistering-speed-in-windows-11.html) | Qualified: reported by publications citing Microsoft and Intel |
| Intel BE200-class cards use the single-radio mode, which doesn't raise data rates | [Dong Knows Tech](https://dongknows.com/wi-fi-7-mlo-multi-link-operation-explained/); [PCWorld](https://www.pcworld.com/article/2824823/how-to-unlock-wi-fi-7s-full-blistering-speed-in-windows-11.html) | Qualified: independent reporting |
| MLO backhaul generally needs same-model units and a star layout | [Dong Knows Tech](https://dongknows.com/wi-fi-7-mlo-multi-link-operation-explained/) | Qualified: independent reporting |
| RTINGS describes "shallow implementations and marketing that oversells the hardware" | [RTINGS.com](https://www.rtings.com/router/learn/research/wifi-7-mlo) | Qualified: summary line only |
