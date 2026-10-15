---
title: "How to Find and Fix Wi-Fi Dead Zones at Home"
date: 2026-10-15
description: "Map weak spots room by room, then fix them in order of cost: move the router, clear obstacles, change the channel, and add wired or mesh coverage last."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "mesh-wifi"]
tags: ["dead-zones", "router-placement", "wifi-coverage", "interference", "mesh-wifi", "signal-strength"]
summary: "Walk the house with your phone and run a speed test in each room to find where Wi-Fi drops off. Most dead zones come from distance, dense walls or metal, or a router hidden in a cabinet or basement. Move the router to a central, raised, open spot first. If a room is still weak, add a wired connection or a mesh point placed halfway to the dead zone, not inside it."
imageAlt: "Bright hallway with open doors leading to a room with a plant"
imageCredit: "Photo: Clay Banks / [Unsplash](https://unsplash.com/photos/wKrfpXTN07Q)"
takeaways:
  - "Apple rates metal as having very high interference potential, and plaster, concrete and bulletproof glass as high. Wood, glass and many synthetic materials are low."
  - "Eero recommends placing mesh units halfway between the main unit and a dead zone, not in the dead zone itself, and about 20 to 30 feet apart."
  - "Google recommends keeping each Wi-Fi point no more than two rooms from the router or another point, off the ground and in the open."
  - "Moving the router costs nothing and often helps most. Wired backhaul, MoCA or powerline come before buying more wireless hardware."
faq:
  - q: "What causes Wi-Fi dead zones?"
    a: "Distance from the router, dense building materials such as plaster, brick, concrete and metal, and a router placed in a cabinet, a corner or a basement. Interference from microwave ovens, cordless phones and neighboring networks can make weak areas worse."
  - q: "How do I find dead zones in my house?"
    a: "Take a phone or laptop to each room and run a speed test in the same spot, ideally at the same time of day. Note the result and the signal bars. Rooms where speed falls sharply or the connection drops are your dead zones."
  - q: "Should I put a mesh point or extender in the dead zone?"
    a: "No. Eero says to place units halfway between the main unit and the dead zone. A unit inside the dead zone gets the same weak signal and passes it on."
  - q: "Can changing the Wi-Fi channel fix a dead zone?"
    a: "It can help if interference is the problem rather than distance. Apple suggests changing the channel or letting the router scan for the least congested one."
  - q: "What signal strength counts as weak?"
    a: "If your router or app shows dBm, ASUS classes -20 to -70 dBm as good, -71 to -80 dBm as fair and -81 dBm or lower as weak. Numbers closer to zero are stronger."
sources:
  - title: "Resolve Wi-Fi and Bluetooth issues caused by wireless interference"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102319"
    date: 2025-04-23
  - title: "Where should I place my eeros?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/where-should-i-place-my-eeros"
  - title: "Where to place your Wifi devices"
    publisher: "Google Home Help"
    url: "https://support.google.com/googlehome/answer/7183150"
  - title: "[Wireless Router] How to configure the Smart Connect in ASUS Router?"
    publisher: "ASUS Support"
    url: "https://www.asus.com/us/support/faq/1012132/"
    date: 2024-12-09
---

To fix a Wi-Fi dead zone, first find out where the signal actually falls off. Walk the house with a phone and run a speed test in each room. Then work through the fixes from cheapest to most expensive: move the router, clear obstacles, change the channel, and only then add a wired link or a mesh point.

This is a research-based guide built from Apple, eero, Google and ASUS documentation. We have not mapped coverage in a test home.

## Step 1: Map your weak spots

You don't need special tools.

1. **Pick one device,** ideally the phone or laptop you use most.
2. **Run a speed test in each room,** standing where you'd normally use the device. Note the download speed and the signal bars.
3. **Repeat at a busy time,** such as the evening, to catch interference from neighbors' networks.
4. **Check the router's app.** Mesh apps often show connection quality per device or per unit. Google suggests running a mesh test after moving a point.

If your router or app shows signal strength in dBm, ASUS gives these bands: -20 to -70 dBm is good, -71 to -80 dBm is fair, and -81 dBm or lower is weak.

A room that is slow on every device is a coverage problem. If one device is slow everywhere, the device is the problem. Our [slow Wi-Fi guide]({{< relref "/guides/how-to-fix-slow-wifi" >}}) covers that test, and our guide to [slow Wi-Fi on a fast connection]({{< relref "/guides/wifi-slow-but-internet-fast" >}}) explains the difference between Wi-Fi and plan speed.

## Step 2: Move the router

Placement is the free fix. The guidance from eero and Google lines up:

- **Central.** Eero suggests moving the modem and main unit "out of your basement and into a more centralized location."
- **Raised.** Eero recommends a height halfway between floor and ceiling. Google suggests a shelf or TV stand, ideally at eye level.
- **In the open.** Eero says not to put units inside a media console or cabinet. Google says to avoid objects that physically block the signal.
- **Away from heat.** Eero says direct sunlight and incandescent bulbs can hurt performance.

If your provider's cable or fiber outlet is in a corner, a longer Ethernet cable between the modem and the router can let you move the router without moving the outlet.

## Step 3: Check what's in the way

Some materials block Wi-Fi far more than others. Apple's interference guide rates them:

| Interference potential | Materials (Apple) |
|---|---|
| Low | Wood, glass, many synthetic materials |
| Medium | Water, bricks, marble |
| High | Plaster, concrete, bulletproof glass |
| Very high | Metal |

Eero adds that older homes with plaster, lath or chicken wire in the walls are "particularly hard" for Wi-Fi, and that placing units near doors can help because wood is easier for the signal to pass through. Mirrors, aquariums, refrigerators and metal furniture are also on eero's list of things to keep units away from.

## Step 4: Reduce interference

Interference can turn a weak area into a dead one. Apple lists microwave ovens, cordless phones, fluorescent lights, wireless video cameras and power cables as common sources. Its suggestions:

- **Change the Wi-Fi channel,** or let the router scan for the least congested one.
- **Move devices to 5 GHz** where the router supports it, which takes them off the busier 2.4 GHz band.
- **Reduce the number of active devices** on the same band.

5 GHz and 6 GHz are faster but reach less far through walls than 2.4 GHz. See [2.4 GHz vs. 5 GHz vs. 6 GHz]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}}) for the trade-off.

## Step 5: Add coverage, wired first

If a room is still weak after moving the router, you need a second access point. Wired links are more reliable than wireless ones, so check these first:

| Option | Best when | Guide |
|---|---|---|
| Ethernet to a mesh point or access point | You can run a cable | [Ethernet cable guide]({{< relref "/guides/ethernet-cable-cat5e-vs-cat6-vs-cat6a" >}}) |
| MoCA | There's a coax outlet in or near the room | [What is MoCA]({{< relref "/guides/what-is-moca-ethernet-over-coax" >}}) |
| Powerline | There's no coax or Ethernet, only power outlets | [Are powerline adapters worth it?]({{< relref "/guides/are-powerline-adapters-worth-it" >}}) |
| Mesh Wi-Fi | Several rooms are weak, or no wired option works | [Wi-Fi router vs. mesh]({{< relref "/guides/wifi-router-vs-mesh" >}}) |
| Extender | One room, on a budget | [Extender placement]({{< relref "/guides/wifi-extender-placement-guide" >}}) |

For wireless units, placement matters as much as the hardware:

- **Halfway, not in the dead zone.** Eero says: "Don't place eeros directly in dead zones. Instead, place them halfway between your gateway eero and dead zones."
- **Spacing.** Eero suggests 20 to 30 feet apart, and no more than 50 feet. Google says no more than two rooms from the router or another point.
- **Line of sight** between units helps, according to both eero and Google.

Homes with thick walls may need more units, eero says. Or connect them by cable; see [wired vs. wireless mesh backhaul]({{< relref "/guides/mesh-wifi-wired-vs-wireless-backhaul" >}}).

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Material interference ratings: wood, glass and synthetics low; water, brick, marble medium; plaster, concrete, bulletproof glass high; metal very high. Interference sources and fixes, including channel changes and 5 GHz | [Apple Support 102319, April 23, 2025](https://support.apple.com/en-us/102319) | Verified as of October 15, 2026 |
| Eero: centralize the gateway; halfway height; not in cabinets; avoid heat; 20 to 30 feet apart, no more than 50; place halfway to dead zones; plaster and lath walls hard for Wi-Fi; near doors helps | [eero Support](https://eero.com/support/articles/where-should-i-place-my-eeros) | Verified as of October 15, 2026 |
| Google: no more than two rooms from the router or another point; off the ground, in the open; line of sight helps; run a mesh test after moving | [Google Home Help 7183150](https://support.google.com/googlehome/answer/7183150) | Verified as of October 15, 2026 |
| ASUS signal bands: -20 to -70 dBm good, -71 to -80 fair, -81 or lower weak | [ASUS FAQ 1012132](https://www.asus.com/us/support/faq/1012132/) | Verified; ASUS's own classification, used here as a rough guide |

## Bottom line

Find the dead zones before buying anything. Most homes get the biggest improvement from moving the router somewhere central, raised and open. If a room is still weak, connect a second access point by cable, MoCA or powerline, or place a mesh point halfway between the router and the weak room.
