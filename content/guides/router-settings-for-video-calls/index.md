---
title: "Best Router Settings for Zoom and Teams Calls at Home"
date: 2026-10-14
description: "Video calls need little bandwidth but a steady connection. The router settings that help Zoom and Teams on ASUS, Google and eero, and what matters more."
authors: ["Tehseen Arbab"]
topics: ["gaming-streaming", "how-to-fixes"]
tags: ["video-calls", "work-from-home", "qos", "zoom", "microsoft-teams", "upload-speed"]
summary: "Zoom and Teams need only a few megabits per second, so freezes and robotic audio usually come from an unsteady connection, not a slow plan. Use Ethernet or a strong 5 GHz signal, leave WMM on, turn on your router's video-call priority feature if it has one, and stop large uploads from swamping the line during calls."
imageAlt: "Man on a video call at a laptop on a home desk"
imageCredit: "Photo: LinkedIn Sales Solutions / [Unsplash](https://unsplash.com/photos/6ie6OjshvWg)"
takeaways:
  - "Zoom lists 3.8 Mbps up and 3.0 Mbps down for 1080p video calls. Microsoft lists 4 Mbps each way as the best-performance figure for Teams video."
  - "Microsoft says Teams prioritizes audio over video when bandwidth runs short, and that voices sounding robotic can point to jitter or packet loss."
  - "ASUS Adaptive QoE has a Work from Home mode, Google Nest Wifi and Google Wifi can prioritize video conferencing, and eero offers a beta Optimize for Conferencing and Gaming setting."
  - "Apple recommends leaving WMM (Wi-Fi Multimedia) enabled, because it prioritizes network traffic; Microsoft also recommends QoS or WMM for Teams."
faq:
  - q: "How much internet speed do I need for Zoom or Teams?"
    a: "Less than most plans provide. Zoom lists 3.8 Mbps up and 3.0 Mbps down for 1080p calls. Microsoft's best-performance figure for Teams video is 4 Mbps each way. Add more for other people in the home who are online at the same time."
  - q: "Why does my video call freeze when my speed test is fine?"
    a: "A speed test measures peak throughput. Calls depend on a steady connection, so weak Wi-Fi signal, a busy 2.4 GHz band, or other uploads filling the line can cause freezes even on a fast plan. Microsoft says robotic-sounding voices can point to jitter or packet loss."
  - q: "Should I turn on QoS for video calls?"
    a: "If your router offers a video-call mode, it is worth trying. ASUS's Work from Home mode prioritizes apps such as Zoom and Teams, and Google Nest Wifi and Google Wifi can prioritize video conferencing. Eero's beta setting is best for connections under 500 Mbps, according to eero, and may slow some devices."
  - q: "Is Ethernet better than Wi-Fi for video calls?"
    a: "Usually, yes. A cable avoids Wi-Fi interference and signal drops. If a cable isn't practical, use the 5 GHz or 6 GHz band close to the router or a mesh point."
  - q: "Does a work VPN affect call quality?"
    a: "It can. Microsoft says routing Teams traffic through a VPN can add latency and jitter. Ask your employer's IT team whether calls bypass the VPN."
sources:
  - title: "Zoom system requirements: Windows, macOS, Linux"
    publisher: "Zoom Support"
    url: "https://support.zoom.com/hc/en/article?id=zm_kb&sysparm_article=KB0060748"
  - title: "Prepare your organization's network for Teams"
    publisher: "Microsoft Learn"
    url: "https://learn.microsoft.com/en-us/microsoftteams/prepare-network"
    date: 2026-07-09
  - title: "Learn what requirements you need to use Google Meet"
    publisher: "Google Meet Help"
    url: "https://support.google.com/meet/answer/7317473"
  - title: "[Wireless Router] How to Set Up Adaptive QoE and Bandwidth Limitation on ASUS Routers"
    publisher: "ASUS Support"
    url: "https://www.asus.com/us/support/faq/1055838/"
    date: 2026-08-13
  - title: "Set preferred activities to improve Wi-Fi performance"
    publisher: "Google Home and Nest Help"
    url: "https://support.google.com/googlenest/answer/9541371"
  - title: "Prioritize a device on your Wi-Fi network"
    publisher: "Google Home and Nest Help"
    url: "https://support.google.com/googlenest/answer/6246483"
  - title: "Here's how to maximize your wifi to work from home"
    publisher: "eero Blog"
    url: "https://blog.eero.com/working-from-home"
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102766"
    date: 2026-07-14
---

Video calls need far less speed than most home plans provide. When Zoom or Teams freezes, the cause is usually an unsteady connection: weak Wi-Fi, a crowded band, or another upload filling the line. Fix those first. Then use your router's video-call priority setting if it has one.

This is a research-based guide built from Zoom's and Microsoft's published requirements and router makers' support documentation. We have not measured call quality on these routers ourselves.

## Quick answer: the settings that help most

1. **Plug in with Ethernet** if you can. If you can't, connect on 5 GHz or 6 GHz, close to the router or a mesh point.
2. **Leave WMM on.** Apple recommends it, and Microsoft recommends QoS or WMM for Teams.
3. **Turn on your router's video-call mode,** if it has one. ASUS, Google and eero all offer one (see the table below).
4. **Keep big uploads off the line during calls.** Cloud backups and large file syncs compete with your outgoing video.
5. **Fix bufferbloat** if calls break up whenever someone else is downloading. See our [bufferbloat guide]({{< relref "/guides/fix-bufferbloat-gaming-lag" >}}).

## How much bandwidth do video calls use?

| App and call type | Upload | Download | Source |
|---|---|---|---|
| Zoom, 1:1 call, 720p | 1.2 Mbps | 1.2 Mbps | Zoom |
| Zoom, group call, 720p | 2.6 Mbps | 1.8 Mbps | Zoom |
| Zoom, 1080p (1:1 or group) | 3.8 Mbps | 3.0 Mbps | Zoom |
| Zoom, audio only | 60 to 80 kbps | 60 to 80 kbps | Zoom |
| Teams video meetings, recommended (up to 1080p) | 2.5 Mbps | 4 Mbps | Microsoft |
| Teams video, best performance | 4 Mbps | 4 Mbps | Microsoft |

Zoom says it adjusts bandwidth to each participant's network. Google's Meet requirements page lists hardware and says you need a broadband connection, but gives no bandwidth figures.

The figures are per person on a call. Two people on separate 1080p Zoom calls need roughly double. Upload is the tighter limit on many cable plans, so check yours with our guide to [how much internet speed you need]({{< relref "/guides/how-much-internet-speed-do-i-need" >}}).

## Why calls freeze on a fast plan

Bandwidth alone does not guarantee a good call. Microsoft says "provisioned bandwidth alone" doesn't guarantee quality, and that calls with static, cut-outs or voices that "sound like robots" could point to jitter or packet loss. When bandwidth does run short, Microsoft says Teams prioritizes audio over video.

The common home causes:

- **Weak or crowded Wi-Fi.** Microsoft says the 2.4 GHz band is often congested by consumer devices, and that 5 GHz is better suited to real-time media. See [2.4 GHz vs. 5 GHz vs. 6 GHz]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}}).
- **A full upload.** A backup or game download on another device can push your call's traffic into a queue. That delay is bufferbloat.
- **The Wi-Fi link, not the plan.** If a wired test is fast but your laptop is slow, the problem is local. Our guide to [slow Wi-Fi on a fast connection]({{< relref "/guides/wifi-slow-but-internet-fast" >}}) walks through the checks.

## Router settings for video calls, by brand

| Router | Setting | What the maker says it does | Caveat |
|---|---|---|---|
| ASUS | Adaptive QoE, Work from Home mode | Prioritizes apps "such as Zoom, Teams" | Web interface: Adaptive QoE, then turn on QoS and choose the mode |
| Google Nest Wifi Pro, Nest Wifi, Google Wifi | Preferred activities, video conferencing | Prioritizes Meet, Zoom, Teams, Slack, GoTo Meeting and Webex | On by default; works only when a device is on a call |
| Google Nest Wifi Pro, Nest Wifi, Google Wifi | Prioritize a device | Gives one device 70% of available bandwidth | One device at a time; others share the rest |
| eero | Optimize for Conferencing and Gaming (eero Labs beta) | Queues traffic so every device keeps access | eero says it is best for connections under 500 Mbps and some devices may slow |

On an ASUS router, open the router's web interface, go to Adaptive QoE, switch on QoS, pick Work from Home and apply. ASUS also offers a Bandwidth Limiter that caps a chosen device. It says any limit should be lower than your provider's maximum speed, or it won't take effect.

On Google Nest Wifi or Google Wifi, open the Google Home app, then Wi-Fi, Network settings and Preferred activities. To prioritize a single laptop instead, open Wi-Fi, then Devices, choose the laptop and pick a duration.

On eero, open the Discover tab in the eero app, tap eero Labs and turn on Optimize for Conferencing and Gaming.

If your router has none of these, check its QoS or traffic-priority settings, and make sure WMM is enabled. Apple says disabling WMM "can affect the performance and reliability of devices on the network."

## Other settings worth checking

- **One network name across bands.** Apple recommends a single name for all bands. If you split bands, make sure the work laptop joins 5 GHz or 6 GHz.
- **2.4 GHz channel width.** Apple recommends 20 MHz on 2.4 GHz and Auto on 5 GHz and 6 GHz.
- **Work VPN.** Microsoft says routing Teams traffic through a VPN can add "extra latency and jitter." That setting belongs to your employer, so ask its IT team whether calls bypass the VPN.

## When to change hardware instead

If the room you work in has a weak signal, settings won't fix it. Run a cable, use [MoCA over existing coax]({{< relref "/guides/what-is-moca-ethernet-over-coax" >}}), or add a mesh point with a [wired backhaul]({{< relref "/guides/mesh-wifi-wired-vs-wireless-backhaul" >}}). If your provider's gateway lacks priority settings, our guide to [buying your own router]({{< relref "/guides/buy-your-own-router-vs-isp-equipment" >}}) covers what to check before you switch.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Zoom bandwidth: 720p 1:1 at 1.2 Mbps; 720p group at 2.6 up and 1.8 down; 1080p at 3.8 up and 3.0 down; audio at 60 to 80 kbps | [Zoom system requirements](https://support.zoom.com/hc/en/article?id=zm_kb&sysparm_article=KB0060748) | Verified as of October 14, 2026 |
| Teams video meetings: 2.5 Mbps up and 4 Mbps down recommended; 4 Mbps each way for best performance; audio is prioritized over video when bandwidth runs short | [Microsoft Learn, updated July 9, 2026](https://learn.microsoft.com/en-us/microsoftteams/prepare-network) | Verified as of October 14, 2026 |
| Microsoft: robotic-sounding voices could be jitter or packet loss; 2.4 GHz often congested; 5 GHz better for real-time media; use QoS or WMM; VPN can add latency and jitter | [Microsoft Learn](https://learn.microsoft.com/en-us/microsoftteams/prepare-network) | Verified; Microsoft's guidance is written for organizations, applied here to home use |
| Google's Meet requirements page gives no bandwidth figures | [Google Meet Help](https://support.google.com/meet/answer/7317473) | Verified as of October 14, 2026 |
| ASUS Work from Home mode prioritizes apps such as Zoom and Teams; Bandwidth Limiter limits must be below the provider's maximum | [ASUS FAQ 1055838, updated August 13, 2026](https://www.asus.com/us/support/faq/1055838/) | Verified as of October 14, 2026 |
| Google preferred activities cover video conferencing apps and are on by default; a prioritized device gets 70% of bandwidth, one device at a time | [Google 9541371](https://support.google.com/googlenest/answer/9541371), [Google 6246483](https://support.google.com/googlenest/answer/6246483) | Verified as of October 14, 2026 |
| eero's Optimize for Conferencing and Gaming is a beta best for connections under 500 Mbps and may slow some devices | [eero Blog](https://blog.eero.com/working-from-home) | Qualified: the post is undated, and eero Labs features can change |
| Apple recommends WMM enabled, one name for all bands, 20 MHz on 2.4 GHz | [Apple Support, July 14, 2026](https://support.apple.com/en-us/102766) | Verified as of October 14, 2026 |

## Bottom line

A video call needs about 4 Mbps in each direction at most, so a faster plan rarely fixes a bad call. Get the work device onto Ethernet or a strong 5 GHz or 6 GHz signal, leave WMM on, switch on your router's video-call priority, and stop other uploads from crowding the line.
