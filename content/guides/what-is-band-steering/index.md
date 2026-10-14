---
title: "What Is Band Steering, and Should You Turn It Off?"
date: 2026-10-14
description: "Band steering puts all your Wi-Fi bands under one name and nudges devices to the best one. When to leave it on, when to turn it off, and how on each brand."
authors: ["Tehseen Arbab"]
topics: ["routers", "how-to-fixes"]
tags: ["band-steering", "smart-connect", "wifi-bands", "netgear", "asus", "tp-link", "eero"]
summary: "Band steering, often called Smart Connect, combines your router's 2.4 GHz, 5 GHz and 6 GHz bands under one network name and moves dual-band devices to the band it judges best. Most homes should leave it on: Apple recommends one name for all bands. Turn it off only for a specific problem, such as a 2.4 GHz-only device that won't set up, and turn it back on afterward."
imageAlt: "Back of a white Wi-Fi router with two antennas and an Ethernet cable plugged in"
imageCredit: "Photo: Compare Fibre / [Unsplash](https://unsplash.com/photos/hXVVNB6Qctg)"
takeaways:
  - "Netgear, ASUS and TP-Link call band steering Smart Connect. It puts every band under a single network name and lets the router help pick the band for each device."
  - "Apple recommends one name for all bands, and warns that devices might not connect reliably if bands have different names."
  - "Eero and Google Nest Wifi always use one name. Eero says there is no way to permanently separate its bands, though it can hide 5 and 6 GHz temporarily."
  - "Turning band steering off helps mainly when a 2.4 GHz-only smart device won't set up. ASUS also warns that a phone's own band-preference settings can make steering ineffective."
faq:
  - q: "What does band steering do?"
    a: "It broadcasts all of the router's bands under one network name and password, then nudges devices that support more than one band toward the band the router judges best. Older 2.4 GHz-only devices simply stay on 2.4 GHz."
  - q: "Is band steering the same as Smart Connect?"
    a: "In practice, yes. Netgear, ASUS and TP-Link use the name Smart Connect for the feature. Google calls it band steering. Eero uses one network name for all bands but doesn't offer an on/off setting."
  - q: "Should I turn off band steering?"
    a: "Usually not. Apple recommends a single network name across bands. Turn it off only to fix a specific problem, such as a smart plug that only supports 2.4 GHz and fails during setup."
  - q: "Does band steering slow down my Wi-Fi?"
    a: "It shouldn't. The goal is to move capable devices to the faster 5 GHz or 6 GHz bands. If a device keeps switching bands or drops off, check for a firmware update and try the router's default steering settings before turning the feature off."
  - q: "Can I separate the bands on eero or Google Nest Wifi?"
    a: "Not permanently. Eero says there is no way to permanently separate its bands, but you can hide 5 and 6 GHz for 30 minutes. Google's help page describes a single network name across bands and no setting to split them."
sources:
  - title: "What is Smart Connect and how do I enable or disable it on my NETGEAR router?"
    publisher: "Netgear Support"
    url: "https://kb.netgear.com/25346/What-is-Smart-Connect-and-how-do-I-enable-or-disable-it-on-my-Nighthawk-router"
    date: 2025-07-07
  - title: "[Wireless Router] How to configure the Smart Connect in ASUS Router?"
    publisher: "ASUS Support"
    url: "https://www.asus.com/us/support/faq/1012132/"
    date: 2024-12-09
  - title: "TP-Link Smart Connect: What It Is and How to Enable It on Your Router"
    publisher: "TP-Link"
    url: "https://www.omadanetworks.com/en/support/faq/2595/"
    date: 2026-04-28
  - title: "Can I set my eeros to use the 2.4, 5, or 6 GHz frequency?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/can-i-set-my-eeros-to-use-the-2-4-5-or-6-ghz-frequency"
  - title: "How Nest Wifi, Nest Wifi Pro, and Google Wifi 2.4, 5 GHz, and 6 GHz bands work"
    publisher: "Google Home and Nest Help"
    url: "https://support.google.com/googlenest/answer/6293481"
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102766"
    date: 2026-07-14
  - title: "Prepare your organization's network for Teams"
    publisher: "Microsoft Learn"
    url: "https://learn.microsoft.com/en-us/microsoftteams/prepare-network"
    date: 2026-07-09
  - title: "Wi-Fi Agile Multiband"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/discover-wi-fi/wi-fi-agile-multiband"
---

Band steering puts your router's 2.4 GHz, 5 GHz and, on newer routers, 6 GHz bands under one network name, then nudges each device that supports more than one band toward the band the router judges best. Leave it on unless you have a specific problem. The usual reason to turn it off is a smart plug or camera that only supports 2.4 GHz and fails during setup. Turn it back on afterward.

This is an explainer based on router makers' and Apple's support documentation. It is not a hands-on test.

## What band steering does

Without band steering, a dual-band router broadcasts two networks, such as "Home" and "Home-5G," and you pick one on each device. With it, you see a single name.

The router then helps decide which band each device uses:

- **Netgear** says Smart Connect "automatically chooses the best WiFi band for your device."
- **TP-Link** says Smart Connect assigns each device to the band "that provides the fastest speed" and balances load across bands. Devices that only support 2.4 GHz stay on 2.4 GHz.
- **Google** says Nest Wifi and Google Wifi steer devices to "the band with the best performance for each device," and that devices pick a band based on compatibility, security, signal strength and distance from a Wi-Fi point.
- **ASUS** lets you adjust the rules on many models: when steering is triggered, which band a device is sent to, and a "bounce detect" limit that keeps a device on one band for a while if it has been moved too often.

The device still has the last word on which band it joins. Routers influence that choice. The Wi-Fi Alliance's Agile Multiband program exists to support this kind of information exchange between access points and devices, so that band and channel decisions can be made with better information.

## What each brand calls it

| Router | Name | Can you turn it off? | Where |
|---|---|---|---|
| Netgear | Smart Connect | Yes | routerlogin.net, Wireless (or Settings, Setup, Wireless Setup) |
| ASUS | Smart Connect | Yes, by giving each band its own name | Network, Main network profile (newer firmware) or Wireless, General (older firmware) |
| TP-Link | Smart Connect | Yes | tplinkwifi.net, Advanced, Wireless; or Tether app, Wi-Fi Settings |
| eero | Single network name for all bands | No; 5 and 6 GHz can be hidden for 30 minutes | eero app |
| Google Nest Wifi, Google Wifi | Band steering | No setting described | Google Home app |

Netgear says Smart Connect "might or might not be disabled by default," depending on the model. Check your router if you're not sure which mode you're in.

## Why most homes should leave it on

- **Apple recommends one name.** Its router guidance says to use a single network name for all bands and warns that with different names, "devices might not connect reliably." On Wi-Fi 6E networks, Apple devices flag the network as having limited compatibility if the names differ.
- **It helps on mesh systems.** Eero says its single network name lets devices "seamlessly roam" across its mesh.
- **It moves capable devices off 2.4 GHz.** Microsoft's Teams network guidance recommends band steering to move dual-band devices to 5 GHz, which it says is better suited to real-time media. See [2.4 GHz vs. 5 GHz vs. 6 GHz]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}}) for the trade-offs between bands.

## When turning it off can help

- **A 2.4 GHz-only device won't set up.** TP-Link suggests separating the bands when smart home devices that support only 2.4 GHz struggle to connect. On eero, hide the 5 and 6 GHz bands for 30 minutes instead. Our [2.4 GHz smart device guide]({{< relref "/guides/smart-home-device-wont-connect-2-4-ghz" >}}) has the steps for each brand.
- **A device keeps dropping or switching bands.** ASUS says a phone's own Wi-Fi band-preference settings may make Smart Connect ineffective "or lead to frequent disconnections." Check the device's settings first.
- **An old device can't connect at all.** On ASUS routers, setting the steering rule to allow only 802.11ac (Wi-Fi 5) devices means 802.11n-only devices "will not be able to connect." Restoring the default rules fixes this.

Before turning band steering off for good, try the simpler fixes. ASUS recommends its default steering settings "if there are no special requirements." Update the router's firmware, and check whether the device simply has a weak signal. Our [slow Wi-Fi guide]({{< relref "/guides/how-to-fix-slow-wifi" >}}) covers how to tell.

## How to turn it off, and what changes

- **Netgear:** sign in at routerlogin.net, open Wireless, uncheck Enable Smart Connect, then click Apply.
- **ASUS:** on newer firmware, give each band its own network name and password. On older firmware, turn off Enable Smart Connect under Wireless, then General.
- **TP-Link:** in tplinkwifi.net, go to Advanced, then Wireless, and switch off Smart Connect. In the Tether app, go to More, Wi-Fi Settings, then 2.4GHz & 5GHz Network.

Once the bands have separate names, each device stays on the band you choose. That means you manage it: a laptop on the 2.4 GHz name stays there even when 5 GHz would be faster. If you split the bands only for a setup, switch Smart Connect back on afterward.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Netgear Smart Connect combines bands under one name and chooses the best band; default varies by model; steps to enable or disable | [Netgear KB 25346, updated July 7, 2025](https://kb.netgear.com/25346/What-is-Smart-Connect-and-how-do-I-enable-or-disable-it-on-my-Nighthawk-router) | Verified as of October 14, 2026 |
| ASUS Smart Connect has trigger, selection and bounce-detect rules; defaults recommended; phone band preferences can cause disconnections; AC-only rule blocks 802.11n devices; menu paths | [ASUS FAQ 1012132, updated December 9, 2024](https://www.asus.com/us/support/faq/1012132/) | Verified as of October 14, 2026 |
| TP-Link Smart Connect assigns the fastest band and balances load; suggests separating bands for 2.4 GHz-only smart devices | [TP-Link FAQ 2595, updated April 28, 2026](https://www.omadanetworks.com/en/support/faq/2595/) | Verified as of October 14, 2026 |
| Eero uses a single name so devices roam; bands can't be permanently separated; 5 and 6 GHz can be hidden for 30 minutes | [eero Support](https://eero.com/support/articles/can-i-set-my-eeros-to-use-the-2-4-5-or-6-ghz-frequency) | Verified as of October 14, 2026; an older eero page gave 10 minutes, so check the app |
| Google steers devices to the best band, uses one name across bands, and devices choose based on compatibility, security, signal strength and distance | [Google 6293481](https://support.google.com/googlenest/answer/6293481) | Verified as of October 14, 2026 |
| Apple recommends one name for all bands and warns that separate names may cause unreliable connections | [Apple Support, July 14, 2026](https://support.apple.com/en-us/102766) | Verified as of October 14, 2026 |
| Microsoft recommends band steering to move dual-band devices to 5 GHz for Teams | [Microsoft Learn](https://learn.microsoft.com/en-us/microsoftteams/prepare-network) | Verified; written for organizations |
| Wi-Fi Agile Multiband supports information exchange between access points and devices for band and channel decisions | [Wi-Fi Alliance](https://www.wi-fi.org/discover-wi-fi/wi-fi-agile-multiband) | Verified; the page does not list which routers support it |

## Bottom line

Band steering is the right default for most homes. Leave it on, keep your router's firmware current, and switch it off only long enough to fix a specific device problem, such as a 2.4 GHz-only smart plug that won't set up.
