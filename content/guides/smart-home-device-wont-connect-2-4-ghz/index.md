---
title: "Smart Device Won't Connect to Wi-Fi? Use the 2.4 GHz Band"
date: 2026-10-08
description: "Many smart plugs, cameras and bulbs only work on 2.4 GHz. Why setup fails on modern routers, and how to connect them on eero, Google, Netgear and TP-Link."
authors: ["Tehseen Arbab"]
topics: ["smart-home-iot", "how-to-fixes"]
tags: ["smart-home", "2-4-ghz", "band-steering", "smart-connect", "setup", "troubleshooting"]
summary: "Many smart home devices can only use the 2.4 GHz band, and setup can fail when your router combines all bands under one network name. Temporarily hide the 5 GHz band (eero has a button for this), or move your phone farther from the router so it switches to 2.4 GHz, then run setup again. Splitting the bands into separate names permanently works too, but Apple warns it can make other devices connect less reliably."
imageAlt: "Smart speaker and smartphone charging on a white table, plugged into a power strip below a wall outlet"
imageCredit: "Photo: Thomas Kolnowski / [Unsplash](https://unsplash.com/photos/_CyM94V3Ydc)"
takeaways:
  - "Google says some smart home devices \"can only use the 2.4 Ghz band and do not support 5 and 6 Ghz.\" Eero says the same of many smart home and IoT devices."
  - "Most current routers broadcast one network name for all bands and steer each device to a band. That is usually helpful, but it can trip up a 2.4 GHz-only device during setup."
  - "Eero's app can pause the 5 and 6 GHz bands temporarily, and devices that join during the pause stay connected afterward. Netgear and TP-Link let you turn off Smart Connect to give each band its own name."
  - "Apple recommends one name for all bands and says separate names can make devices connect less reliably, so use a temporary fix first."
faq:
  - q: "Why won't my smart plug connect to my Wi-Fi?"
    a: "The most common reason is that the plug only supports 2.4 GHz while your phone, which runs the setup, is on 5 GHz. Other common causes are a mistyped password, the plug being too far from the router, or a security setting the device doesn't support."
  - q: "How do I connect a 2.4 GHz device to a dual-band router?"
    a: "Get your phone onto 2.4 GHz for setup. On eero, use Settings, Troubleshooting, My device won't connect, My device is 2.4 GHz only, then pause 5 GHz and 6 GHz. On Google Nest Wifi, Google suggests moving farther from the router until your phone switches to 2.4 GHz. On Netgear and TP-Link, you can turn off Smart Connect to get a separate 2.4 GHz network name."
  - q: "Will the device stay connected after the 5 GHz band comes back?"
    a: "On eero, yes. Eero says devices that connected while the 5 and 6 GHz bands were hidden stay connected after the bands return. A 2.4 GHz-only device keeps using 2.4 GHz under the same network name."
  - q: "Should I split my Wi-Fi into separate 2.4 GHz and 5 GHz names?"
    a: "Only if temporary fixes don't work. TP-Link and Kasa suggest it for devices that struggle with a combined network, but Apple recommends a single name for all bands and says separate names can make devices connect less reliably."
  - q: "What router settings help older smart devices connect?"
    a: "TP-Link's Kasa support suggests WPA2 with AES encryption, a 2.4 GHz channel of 1, 6 or 11, and a 20 MHz channel width. Apple also recommends 20 MHz for 2.4 GHz."
sources:
  - title: "How Nest Wifi, Nest Wifi Pro, and Google Wifi 2.4, 5 GHz, and 6 GHz bands work"
    publisher: "Google Nest Help"
    url: "https://support.google.com/googlenest/answer/6293481"
  - title: "How do I temporarily hide the 5 and 6 GHz bands?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/how-do-i-temporarily-hide-the-5-and-6-ghz-bands"
  - title: "Can I set my eeros to use the 2.4, 5, or 6 GHz frequency?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/can-i-set-my-eeros-to-use-the-2-4-5-or-6-ghz-frequency"
  - title: "What is Smart Connect and how do I enable or disable it on my NETGEAR router?"
    publisher: "Netgear Support"
    url: "https://kb.netgear.com/25346/What-is-Smart-Connect-and-how-do-I-enable-or-disable-it-on-my-Nighthawk-router"
  - title: "TP-Link Smart Connect: What It Is and How to Enable It on Your Router"
    publisher: "TP-Link Support"
    url: "https://www.omadanetworks.com/en/support/faq/2595/"
  - title: "Is Your Kasa Device Not Connecting? Troubleshooting Setup Issues"
    publisher: "TP-Link Support"
    url: "https://www.omadanetworks.com/en/support/faq/2229/"
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102766"
    date: 2026-07-14
---

If a smart plug, camera or bulb won't finish setup, the likely reason is the Wi-Fi band. Many smart home devices only work on 2.4 GHz, while your phone, which runs the setup app, is probably on 5 GHz. Get the phone onto 2.4 GHz for a few minutes, by pausing the 5 GHz band or moving farther from the router, then run setup again.

This is a how-to guide based on the router makers' own support documentation. We have not tested these steps on every router, and menu names change between app versions.

## Why do smart home devices need 2.4 GHz?

Wi-Fi uses three bands: 2.4 GHz, 5 GHz and, on newer routers, 6 GHz. Many smart home devices have a radio for 2.4 GHz only. Google's support page says some smart home devices "can only use the 2.4 Ghz band and do not support 5 and 6 Ghz," and eero says many smart home and IoT devices require 2.4 GHz. (IoT stands for Internet of Things, the umbrella term for connected household devices.)

The 2.4 GHz band also reaches farther. TP-Link's Kasa support notes that it "typically provides a longer range than the 5 GHz band," which suits devices placed in garages, porches and far corners. Our [Wi-Fi bands guide]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}}) explains the trade-offs.

## Why does setup fail on a modern router?

Most current routers broadcast one network name (SSID) for all bands and decide which band each device uses. This is called band steering. Netgear and TP-Link call their version Smart Connect, and eero and Google work this way by default.

For everyday use that is helpful. Setup is where it can go wrong, because your phone may sit on 5 GHz while the device can only use 2.4 GHz. Google says you "may need to connect your phone to the 2.4 GHz band manually" to set up a 2.4 GHz-only device.

The fix is to get the phone, and so the device, onto 2.4 GHz for the length of the setup.

## How do I connect a 2.4 GHz device on my router?

| Router | What the maker documents | Is it temporary? |
|---|---|---|
| eero | Pause the 5 and 6 GHz bands from the app's Troubleshooting menu | Yes; the bands come back automatically |
| Google Nest Wifi, Nest Wifi Pro, Google Wifi | Move away from the router until your phone switches to 2.4 GHz | Yes |
| Netgear (Nighthawk and others with Smart Connect) | Turn off Smart Connect to get separate band names | No, until you turn it back on |
| TP-Link (Smart Connect) | Turn off Smart Connect, then use the 2.4 GHz network name | No, until you turn it back on |

### eero

Eero has a built-in option for exactly this:

1. Open the eero app and tap **Settings**.
2. Scroll down and tap **Troubleshooting**.
3. Tap **My device won't connect**, then **My device is 2.4 GHz only**.
4. Tap **Pause 5 GHz and 6 GHz**.
5. Run the device's setup while the pause is on.

The bands turn back on by themselves. Eero's two support articles give different durations: one says the pause lasts "for up to 10 minutes," the other says 30 minutes. Start setup right away to be safe. Eero says devices that connect during the pause stay connected after the bands return, and that there is no way to permanently split eero's bands into separate names.

### Google Nest Wifi and Google Wifi

Google's system uses one network name, and its help page doesn't describe a way to switch off 5 GHz. It suggests two approaches:

- Use your phone's own settings to pick the 2.4 GHz band, if your phone allows it. Check the phone's manual.
- Otherwise, "move farther away from your router and point until your phone moves to the 2.4 GHz band," then continue setup. This works because 2.4 GHz reaches farther than 5 GHz.

### Netgear

Netgear says Smart Connect "combines your NETGEAR router's WiFi bands into a single WiFi network name," and that it "might or might not be disabled by default" depending on the model. Turning it off gives each band its own name, such as NETGEARWIFI for 2.4 GHz and NETGEARWIFI-5G for 5 GHz. To turn it off, sign in at routerlogin.net, open the Wireless page (some models use Settings, Setup, Wireless Setup), clear **Enable Smart Connect**, and click **Apply**.

### TP-Link

TP-Link says that with Smart Connect on, "both bands share the same network name (SSID) and password," and suggests turning it off for devices that struggle with that. In the web interface it is under Advanced, Wireless, Wireless Settings. In the Tether app it is under More, Wi-Fi Settings, 2.4GHz & 5GHz.

## Should I keep the bands split permanently?

Usually not. The advice differs between manufacturers, and the difference matters:

- TP-Link's Kasa support recommends using "a different network name (SSID) for the 5 GHz band than for the 2.4 GHz band" when setting up its devices.
- Apple recommends one name for all bands and warns: "If you give your 2.4 GHz, 5 GHz, or 6 GHz bands different names, devices might not connect reliably to your network."

A temporary fix, like eero's pause or Google's move-farther-away approach, avoids the conflict. If your router only offers a permanent split, here is one approach to test. It is our suggestion, not a manufacturer instruction: keep your original network name on the 2.4 GHz band and give 5 GHz a new name. Devices already set up on 2.4 GHz should keep connecting, and you can move phones and laptops to the 5 GHz name.

Be aware that if you later turn Smart Connect back on and the network name changes, devices set up on the old name may need setting up again.

## What else can stop a smart device from connecting?

If the band isn't the problem, check these:

- **The password.** Re-type it carefully; setup apps rarely show which character is wrong.
- **Distance.** Do setup near where the device will live, and make sure the signal is reasonable there.
- **Security settings.** Some older devices don't support WPA3. Kasa's support suggests WPA2 with AES. A WPA2/WPA3 mixed mode lets both old and new devices connect; see [WPA2 vs. WPA3]({{< relref "/guides/wpa2-vs-wpa3" >}}).
- **Channel settings.** Kasa's support suggests a 2.4 GHz channel of 1, 6 or 11 and a 20 MHz channel width. Apple also recommends 20 MHz for 2.4 GHz, saying it "helps to avoid performance and reliability issues."
- **The phone.** Kasa's support suggests trying a different phone, and making the phone forget any saved network profile before reconnecting.

## Where should smart devices live once they're connected?

Consider a guest or IoT network. Separating smart devices from your laptops and phones is what the NSA recommends, and it works the same way for 2.4 GHz-only devices, as long as that network includes 2.4 GHz. Our guide to [putting smart home devices on a guest network]({{< relref "/guides/guest-wifi-network-smart-home-devices" >}}) covers the setup and what can break. For Matter and Thread devices, which can connect differently, see [Matter and Thread, explained]({{< relref "/guides/matter-thread-smart-home-explained" >}}).

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Some smart home devices can only use 2.4 GHz; Google suggests connecting the phone to 2.4 GHz manually or moving farther from the router until it switches | [Google Nest Help](https://support.google.com/googlenest/answer/6293481) | Verified as of October 8, 2026 |
| eero's app can pause the 5 and 6 GHz bands from Settings, Troubleshooting; devices that connect during the pause stay connected; eero bands can't be permanently split | [eero Support, hide 5 and 6 GHz](https://eero.com/support/articles/how-do-i-temporarily-hide-the-5-and-6-ghz-bands) and [eero Support, frequencies](https://eero.com/support/articles/can-i-set-my-eeros-to-use-the-2-4-5-or-6-ghz-frequency) | Verified; eero's two articles give different pause lengths, 10 and 30 minutes |
| Netgear Smart Connect combines bands into one name, may or may not be on by default, and can be turned off from the Wireless settings | [Netgear Support](https://kb.netgear.com/25346/What-is-Smart-Connect-and-how-do-I-enable-or-disable-it-on-my-Nighthawk-router) | Verified as of October 8, 2026 |
| TP-Link Smart Connect shares one name and password across bands and can be turned off in the web interface or Tether app | [TP-Link Support](https://www.omadanetworks.com/en/support/faq/2595/) | Verified as of October 8, 2026 |
| Kasa support recommends separate band names, WPA2 with AES, channel 1, 6 or 11, and 20 MHz width, and says 2.4 GHz typically reaches farther | [TP-Link Kasa Support](https://www.omadanetworks.com/en/support/faq/2229/) | Verified as of October 8, 2026 |
| Apple recommends one name for all bands, warns separate names can reduce reliability, and recommends 20 MHz for 2.4 GHz | [Apple Support, July 14, 2026](https://support.apple.com/en-us/102766) | Verified |
| The NSA advises separating primary, guest and IoT networks | [NSA, Best Practices for Securing Your Home Network, February 2023](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| Keeping the original name on 2.4 GHz when splitting bands should keep existing devices connected | Our suggestion | Qualified: reasoning, not a manufacturer instruction or a tested result |

## Bottom line

A smart device that won't connect usually needs 2.4 GHz while your phone is on 5 GHz. Use a temporary fix first: eero's pause button, or moving farther from a Google router. On Netgear and TP-Link, turning off Smart Connect works but changes your network permanently, so weigh it against Apple's advice to keep one name. Once the device is connected, a guest or IoT network is a good place for it.
