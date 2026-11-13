---
title: "Device Not Connecting to the Closest eero? How to Fix It"
date: 2026-11-13T05:00:00Z
description: "Device not connecting to the closest eero? Each device decides when to roam. Check Client Steering, eero placement and signal bars before you worry."
authors: ["Tehseen Arbab"]
topics: ["mesh-wifi", "how-to-fixes"]
tags: ["eero", "roaming", "client-steering", "trueroam", "mesh-wifi", "sticky-client", "troubleshooting"]
summary: "A phone or laptop stuck on a distant eero is usually normal: eero says different devices have different thresholds for when to roam, and some get a stronger signal from an eero farther away. If speeds are fine, leave it. If they aren't, make sure Client Steering is on, move the eeros into the open and closer together, and check the device's signal bars in the eero app."
imageAlt: "Silhouette of a man looking down at a phone in his hand in a softly lit orange hallway"
imageCredit: "Photo: Aurelien Thomas / [Unsplash](https://unsplash.com/photos/a-man-standing-in-a-hallway-using-a-cell-phone-3hsXEkXlfjU)"
takeaways:
  - "The device makes the final call on which eero to use. eero says 'different devices have different thresholds for when to roam between eeros,' and some devices may have a stronger connection to an eero farther away."
  - "If the device is performing as usual, eero says there's no need to worry. Act only if you see slow speeds, buffering or dropouts."
  - "Client Steering, on by default, encourages devices to switch to the nearest eero, but eero says it doesn't guarantee they will. Find it under Settings > Advanced networking > Client steering."
  - "eero's placement fixes: keep eeros away from other electronics, out of cabinets, and closer to the gateway or another eero. For wireless setups, eero recommends no more than 50 feet between units."
  - "In the eero app, tap a device on the Devices tab to see which eero and band it's using; eero says devices with 1 or 2 bars should roam to the closest eero as you move."
faq:
  - q: "Why does my phone connect to the farthest eero?"
    a: "Your phone, not the eero, decides when to switch. eero says different devices have different roaming thresholds, and some devices may have a stronger wireless connection to an eero farther away. Apple, for example, says iPhones and iPads stay on their current access point until the signal weakens to about -70 dBm, and only then look for a stronger one."
  - q: "Should Client Steering be on or off on eero?"
    a: "On, for this problem. eero's own fix for devices that don't connect to the closest eero starts with making sure Client Steering is enabled, and it's on by default. eero says it encourages devices to switch to the nearest eero and to use 5 GHz (or 6 GHz on supported models), but doesn't guarantee it."
  - q: "How do I see which eero my device is connected to?"
    a: "Open the eero app, go to the Devices tab and tap the device's name. eero says that view shows which eero and which frequency the device is using; the bars next to each device show connection strength."
  - q: "Do I need to turn on eero TrueRoam?"
    a: "No. eero says of TrueRoam, 'you don't have to configure it or even turn it on.' The roaming-related setting in the app is Client Steering, under Settings > Advanced networking."
  - q: "How far apart should eeros be?"
    a: "eero says that for the best experience when wireless, eeros should be no more than 50 feet from another eero, and that this can vary by home. Wired eeros can be spaced more flexibly."
sources:
  - title: "Why doesn't my device connect to the closest eero?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/why-doesnt-my-device-connect-to-the-closest-eero"
  - title: "What advanced features does eero support?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/what-advanced-features-does-eero-support"
  - title: "How do I check the connection strength of my wireless devices?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/how-do-i-check-the-connection-strength-of-my-wireless-devices"
  - title: "How much distance should there be between eeros?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/how-much-distance-should-there-be-between-eeros"
  - title: "How eero's software makes all the difference"
    publisher: "eero"
    url: "https://eero.com/blog/articles/truemesh-trueroam-truechannel"
    date: 2025-06-29
  - title: "Wi-Fi roaming support in Apple devices"
    publisher: "Apple Support"
    url: "https://support.apple.com/102002"
    date: 2024-09-25
---

If your phone or laptop stays on a far-away eero instead of the one in the room, it's usually not a fault. With eero, the device makes the final call on when to switch: eero says "different devices have different thresholds for when to roam between eeros," and "some devices may have a stronger wireless connection to an eero farther away." If the device is working normally, eero's advice is that "there's no need to worry." If you're seeing slow speeds or dropouts, check that Client Steering is on, get your eeros into the open and closer together, and look at the device's signal bars in the eero app.

This guide is based on eero's and Apple's support documentation. We haven't measured roaming behavior on our own network.

## Why devices stick to a distant eero

Moving between eeros is called roaming. eero says its TrueMesh software lets devices "seamlessly transition between eeros as you move between rooms." The network can encourage a move, but the device chooses when to make it, and each phone, laptop and smart speaker uses its own rules.

Apple publishes its rules, which gives a sense of how cautious a device can be. Apple's [roaming support page](https://support.apple.com/102002) (published September 25, 2024) says an iPhone or iPad stays on its current access point "until the received signal strength indicator (RSSI) exceeds –70 dBm," which in practice means until the signal weakens past that level. Only then does it scan for a better one, and it switches only if the candidate is "8 dB stronger" while the device is sending data or "12 dB stronger if the device is idle." So a phone can stay on a weaker eero for a while even when a closer one would be faster. Other device makers set their own thresholds.

That's also why a device can seem to "pick" the far eero after you walk in: it may simply have joined that unit earlier and hasn't crossed its own threshold yet.

## First, check whether it's actually a problem

1. Open the eero app and go to the **Devices** tab. The bars next to each device show its connection strength.
2. Tap the device's name to see which eero and which band it's connected to.
3. Read the bars the way eero does: "4 bars: Excellent, stable connection with maximum speeds"; "2 bars: Acceptable connection, but you may experience buffering or slower speeds"; "1 bar: Poor connection with slower speeds, buffering, and interruptions."

eero says "devices with 1-2 bars should automatically roam to the closest eero as you move." If a device sits on a farther eero with 3 or 4 bars and works fine, there's nothing to fix.

## How to fix it

### 1. Make sure Client Steering is on

eero's first fix is to "ensure Client Steering is enabled." The feature is on by default, but it's worth checking if you or a past troubleshooting attempt turned it off:

1. In the eero app, tap the **Settings** tab.
2. Tap **Advanced networking**.
3. Tap **Client steering** and make sure it's on.

eero says Client Steering "attempts to 'steer'" dual-band devices to 5 GHz and, when you move between rooms, "encourages your devices to seamlessly switch to the nearest eero." On networks with an eero Pro 6E, Pro 7, Max 7 or PoE 7, it can also nudge compatible devices onto 6 GHz. eero is clear about the limit: it "does not guarantee that a device will choose the 5 GHz or 6 GHz bands nor the closest eero to you, but helps to favor that preference."

Steering is related to band steering on other routers; our [band steering guide](/guides/what-is-band-steering/) explains when turning that kind of feature off helps and when it doesn't.

### 2. Move the eeros into the open

eero's other fixes are all about placement:

- "If the eero is surrounded by other electronics, put some distance between them."
- "If the eero is in a cabinet or cubby, move it to a more open area."
- "Move the eero closer to your Gateway eero or another eero in your network."

For wireless setups, eero says "eeros should be no more than 50 feet from another eero," though "depending on your home, this can vary." If eeros are wired together with Ethernet, the spacing is more flexible; our [TrueMesh explainer](/guides/eero-truemesh/) covers wired backhaul.

### 3. Run a Coverage Scan

eero says, "If devices consistently show low connection strength, run a Coverage Scan in the app." If the scan shows a weak area, a better-placed or additional eero is the lasting fix.

### 4. Reconnect the device

If one device is stuck after you've moved, turning its Wi-Fi off and back on makes it pick an eero again from where it is now, which usually means a stronger one nearby, rather than holding the old link until it crosses its roaming threshold. It's a quick check, not a permanent fix: if you have to do it often, go back to placement.

## What about TrueRoam?

TrueRoam is eero's name for its roaming technology. eero's [blog](https://eero.com/blog/articles/truemesh-trueroam-truechannel) says it "connects you to the best available eero as you move between floors, rooms, and buildings," and is "designed to always run in the background, measuring the connection quality of each device and performing roaming assistance when necessary." There's no TrueRoam switch: "you don't have to configure it or even turn it on." In the app, Client Steering is the setting that relates to roaming.

## When it's something else

If a device drops off Wi-Fi entirely rather than just staying on a far eero, see our guide to [why Wi-Fi keeps disconnecting](/guides/wifi-keeps-disconnecting/). And if your home is simply too big for the eeros you have, our [best mesh Wi-Fi for a large house](/guides/best-mesh-wifi-for-large-house/) guide covers systems by layout.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Devices have different roaming thresholds; may have a stronger link to a farther eero; no need to worry if performing as usual; placement fixes | [eero support](https://eero.com/support/articles/why-doesnt-my-device-connect-to-the-closest-eero) | Verified |
| Client Steering: on by default, steers to 5 GHz/6 GHz and nearest eero, no guarantee, app path | [eero support](https://eero.com/support/articles/what-advanced-features-does-eero-support) | Verified |
| Devices tab bars, tap device to see eero and band, 1-2 bars should roam, Coverage Scan | [eero support](https://eero.com/support/articles/how-do-i-check-the-connection-strength-of-my-wireless-devices) | Verified |
| No more than 50 feet between wireless eeros; can vary | [eero support](https://eero.com/support/articles/how-much-distance-should-there-be-between-eeros) | Verified |
| TrueRoam runs in the background, needs no setup | [eero blog](https://eero.com/blog/articles/truemesh-trueroam-truechannel) | Qualified (maker description) |
| iPhone/iPad roam trigger -70 dBm; 8 dB / 12 dB rule | [Apple Support](https://support.apple.com/102002) | Verified (Apple devices only) |
