---
title: "Wi-Fi Channel Width: Should You Use 20, 40, 80 or 160 MHz?"
date: 2026-10-16
description: "What Wi-Fi channel width means, why 160 MHz on 5 GHz depends on radar-sharing (DFS) channels in the US, and which setting to use on each band."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "routers"]
tags: ["channel-width", "160-mhz", "dfs", "5-ghz", "router-settings"]
summary: "Leave 2.4 GHz at 20 MHz and leave 5 GHz and 6 GHz on Auto, as Apple recommends. A 160 MHz channel on 5 GHz needs eight adjacent 20 MHz channels, and in the US every such block overlaps radar-shared (DFS) channels. A router on one of these channels must leave it if it detects radar, so ASUS says a 160 MHz setting can drop to 80 MHz. Try 160 MHz only if your devices support it and you can live with occasional fallbacks."
imageAlt: "Close-up of a black Wi-Fi router with several tall antennas"
imageCredit: "Photo: dlxmedia.hu / [Unsplash](https://unsplash.com/photos/43ak6tfF4Ss)"
takeaways:
  - "Channel width is how much radio spectrum one Wi-Fi channel uses. TP-Link says wider channels allow more data but 'consume more of the available spectrum' and are 'more susceptible to interference.'"
  - "Apple's router guidance (published July 14, 2026): 20 MHz on 2.4 GHz; Auto or all widths on 5 GHz and 6 GHz."
  - "FCC rules require radar detection on 5.25 to 5.35 GHz and 5.47 to 5.725 GHz. A device must stop transmitting on a channel within 10 seconds of detecting radar, and the channel is off limits for at least 30 minutes."
  - "By our channel arithmetic, the two possible US 5 GHz 160 MHz blocks, channels 36 to 64 and 100 to 128, both include DFS channels."
faq:
  - q: "What channel width should I use on 2.4 GHz?"
    a: "Apple recommends 20 MHz on 2.4 GHz. TP-Link notes that at 20 MHz the channels 1, 6 and 11 do not overlap in the US."
  - q: "What channel width should I use on 5 GHz?"
    a: "Apple recommends Auto, or all widths, on 5 GHz and 6 GHz. That lets the router and each device negotiate the width that works."
  - q: "Why does my router drop from 160 MHz to 80 MHz?"
    a: "ASUS says that when a router set to 160 MHz is on a DFS channel and detects radar on that channel, it switches to an 80 MHz channel. If you have confirmed your device supports 160 MHz, radar detection is one cause to check."
  - q: "What is DFS?"
    a: "Dynamic Frequency Selection. It is a requirement that lets Wi-Fi share certain 5 GHz channels with radar systems by detecting radar and moving off the channel."
  - q: "Is 160 MHz worth it?"
    a: "It can raise the maximum link speed for a device that supports it and is close to the router, but the gain is not guaranteed. We have not tested it, so measure with a speed test before and after."
sources:
  - title: "Brief introduction of Wireless Channel, Channel Width and DFS"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/us/support/faq/4309/"
    date: 2024-11-12
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102766"
    date: 2026-07-14
  - title: "What is DFS (Dynamic Frequency Selection) and how does it work on ASUS router?"
    publisher: "ASUS"
    url: "https://www.asus.com/us/support/FAQ/1045936/"
    date: 2024-12-13
  - title: "47 CFR 15.407, General technical requirements (U-NII devices)"
    publisher: "eCFR"
    url: "https://www.ecfr.gov/current/title-47/chapter-I/subchapter-A/part-15/subpart-E/section-15.407"
---

For most people, the best Wi-Fi channel width setting is the default. Apple recommends 20 MHz on 2.4 GHz and Auto (all widths) on 5 GHz and 6 GHz. A wider setting, 160 MHz, can raise the top speed of a link, but on the 5 GHz band in the US it depends on radar-sharing channels, so it can fall back to a narrower channel. This is a research-based guide built from TP-Link, ASUS and Apple documentation and the FCC's rules; we have not run our own speed tests.

## What is channel width?

Channel width is the amount of radio spectrum a Wi-Fi channel uses, measured in megahertz (MHz). TP-Link says 20 MHz is the standard width for most networks on both 2.4 GHz and 5 GHz, and that wider channels are made by bonding (combining) adjacent 20 MHz channels: two make 40 MHz, four make 80 MHz and eight make 160 MHz. A wider channel can carry more data at once, in the same way a wider road carries more traffic. The cost, in TP-Link's words, is that "wider channels consume more of the available spectrum, and wireless transmissions are more susceptible to interference."

## Which width should you use on each band?

| Band | Recommended setting | Why | Source |
|---|---|---|---|
| 2.4 GHz | 20 MHz | The band is small and crowded; at 20 MHz, channels 1, 6 and 11 do not overlap in the US | Apple; TP-Link |
| 5 GHz | Auto (all widths) | Router and device agree on a width that works | Apple |
| 6 GHz | Auto (all widths) | Same reasoning; the band has more room (see below) | Apple |

Our [guide to 2.4, 5 and 6 GHz bands]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}}) explains the bands; if you are chasing a specific problem, start with [why Wi-Fi is slow when your internet is fast]({{< relref "/guides/wifi-slow-but-internet-fast" >}}).

## Why is 160 MHz on 5 GHz complicated in the US?

Because of radar. FCC rules (47 CFR 15.407) require Wi-Fi equipment operating in the 5.25 to 5.35 GHz and 5.47 to 5.725 GHz ranges to use Dynamic Frequency Selection (DFS), which means detecting radar and moving off the channel. The rules say:

- A device may start using a DFS channel only if it detects no radar within a 60-second check.
- After radar is detected, all transmissions must cease on the channel within 10 seconds.
- A channel flagged for radar is unavailable for at least 30 minutes.

A 160 MHz channel is eight adjacent 20 MHz channels. Using the standard channel numbering (the center frequency in MHz is 5000 plus five times the channel number), the US 5 GHz channels that make an eight-channel block are:

| 160 MHz block | Approximate span | Overlaps DFS range? |
|---|---|---|
| Channels 36 to 64 | 5,170 to 5,330 MHz | Yes: channels 52 to 64 are inside 5.25 to 5.35 GHz |
| Channels 100 to 128 | 5,490 to 5,650 MHz | Yes: inside 5.47 to 5.725 GHz |

This table is our own arithmetic from the FCC's DFS ranges, not a figure from a manufacturer. It means a 160 MHz channel on 5 GHz in the US always involves DFS. The 149 to 165 channels are not DFS, but they span only about 100 MHz, too narrow for 160 MHz. The 6 GHz band has no such problem: the Wi-Fi Alliance says it has room for up to seven 160 MHz channels (see our [Wi-Fi 6 vs. 6E guide]({{< relref "/guides/wifi-6-vs-wifi-6e" >}})).

## What happens when a router detects radar?

ASUS explains the behavior on its routers. When a router lands on a DFS channel, it first runs a channel availability check, during which 5 GHz is unavailable but 2.4 GHz works. ASUS says the check "will take 1~10 minutes," depending on the country or region; the FCC text above sets 60 seconds as the check period, and we did not confirm which applies to a specific model. If the router is set to 160 MHz and detects radar on its channel, ASUS says it "automatically switches to a channel in the 80MHz bandwidth."

In practice: a connection that is fast most of the time but briefly stalls, or a device that reports 80 MHz when you set 160, may be a DFS event. It is not necessarily a fault.

## Should you turn on 160 MHz?

Try it only if all of these are true:

1. **Your devices support it.** A router can offer 160 MHz, but each phone, laptop or TV must support it too. Check the device specifications.
2. **The device is close to the router.** Wider channels help most where the signal is already strong. For weak rooms, see [how to find and fix Wi-Fi dead zones]({{< relref "/guides/find-and-fix-wifi-dead-zones" >}}).
3. **You can tolerate fallbacks.** On a DFS channel the router may move or narrow the channel.

Then measure. Run a speed test next to the router at your current setting, change one setting, and test again. If the result is not clearly better, or calls and games stall, switch back to Auto. Our [router settings for video calls]({{< relref "/guides/router-settings-for-video-calls" >}}) guide covers stability-first settings.

One more setting note: TP-Link says channel 165 can only be used with a 20 MHz width.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| 20 MHz is standard on 2.4 and 5 GHz; wider channels bond adjacent channels, use more spectrum and are more susceptible to interference; channels 1, 6, 11 don't overlap at 20 MHz in the US; channel 165 needs 20 MHz | [TP-Link FAQ 4309, updated November 12, 2024](https://www.tp-link.com/us/support/faq/4309/) | Verified; the "two, four, eight channels" breakdown is simple arithmetic on 20 MHz building blocks |
| Apple recommends 20 MHz on 2.4 GHz and Auto or all widths on 5 and 6 GHz, with channel selection on Auto | [Apple Support, published July 14, 2026](https://support.apple.com/en-us/102766) | Verified |
| DFS applies in 5.25 to 5.35 and 5.47 to 5.725 GHz; 60-second availability check; stop within 10 seconds; 30-minute non-occupancy | [47 CFR 15.407(h), eCFR](https://www.ecfr.gov/current/title-47/chapter-I/subchapter-A/part-15/subpart-E/section-15.407) | Verified as read October 16, 2026 |
| US 5 GHz 160 MHz blocks are channels 36 to 64 and 100 to 128, both overlapping DFS ranges | Our calculation from the FCC ranges above and standard channel numbering | Qualified: our arithmetic, not a manufacturer statement; channel availability can vary by router and region setting |
| Channel availability check "will take 1~10 minutes" depending on country or region; 5 GHz unavailable during it; 160 MHz falls back to 80 MHz on radar | [ASUS FAQ 1045936, updated December 13, 2024](https://www.asus.com/us/support/FAQ/1045936/) | Verified for ASUS routers; other brands may differ |
| The 6 GHz band has room for up to seven 160 MHz channels | [Wi-Fi Alliance, as cited in our Wi-Fi 6 vs. 6E guide](https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-delivers-wi-fi-6e-certification-program) | Verified |

## Bottom line

Use 20 MHz on 2.4 GHz and Auto on 5 GHz and 6 GHz unless you have a measured reason to change. Treat 160 MHz on 5 GHz as an experiment: it can help a nearby, compatible device, but in the US it relies on radar-shared channels where your router may have to step down to 80 MHz.
