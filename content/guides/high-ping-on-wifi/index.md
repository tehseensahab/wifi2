---
title: "High Ping on Wi-Fi but Not Ethernet? Causes and Fixes"
date: 2026-10-21T05:00:00Z
description: "High ping on Wi-Fi but not Ethernet usually means the delay is in the wireless link, not your internet. How to confirm it and fix signal and channel causes."
authors: ["John Marshall"]
topics: ["gaming-streaming", "how-to-fixes"]
tags: ["ping", "latency", "jitter", "gaming", "wifi-troubleshooting", "intel-wifi", "channel-width"]
summary: "If your ping is low on Ethernet but high or spiky on Wi-Fi, the extra delay is usually being added between your device and your router, not by your internet provider. The usual causes are a weak signal that forces retransmissions, a crowded channel where devices wait their turn, interference, and laptop adapter settings that scan or save power. Test by pinging your router, then fix signal, channel and adapter settings, or use a cable for gaming."
imageAlt: "Man wearing a headset plays a game at a desktop PC with a mechanical keyboard in a room lit purple"
imageCredit: "Photo: Amine mouzaoui / [Unsplash](https://unsplash.com/photos/a-man-sitting-in-front-of-a-computer-monitor-W5KtfcB7kw4)"
takeaways:
  - "Ping your router's local address over Wi-Fi and then over Ethernet. If only the Wi-Fi result is high or jumpy, the problem is your wireless link, not your internet plan."
  - "Wi-Fi is a shared, half-duplex medium: Cisco notes that as a channel gets busy, even around 70% utilization, devices contend for airtime, which causes latency and collisions."
  - "A weak signal or interference causes retries, and every retry adds delay. Moving closer, switching to 5 GHz or 6 GHz, or changing channels is a good first step before adapter settings."
  - "On Intel Wi-Fi adapters, roaming aggressiveness and background scanning settings control how often the adapter looks for other access points. Intel recommends reverting roaming aggressiveness to its default (Medium) if other values don't help."
  - "If ping also jumps on Ethernet when someone is uploading or downloading, bufferbloat on your internet connection is a likely cause."
faq:
  - q: "Why is my ping higher on Wi-Fi than on Ethernet?"
    a: "Because Wi-Fi adds steps a cable doesn't have. Devices share the channel and take turns transmitting, and packets lost to weak signal or interference are resent. Each of those adds milliseconds, and they vary from moment to moment, which shows up as jitter and spikes."
  - q: "How do I tell whether high ping is my Wi-Fi or my internet?"
    a: "Ping your router's local IP address (the default gateway) from the same device over Wi-Fi, then over Ethernet. If the Wi-Fi ping to the router is high or jumpy but the wired one is steady, the Wi-Fi link is the problem. If both are steady but ping to a game server is high, look at your internet connection."
  - q: "Will a Wi-Fi 6 or Wi-Fi 7 router lower my ping?"
    a: "It can help on a busy network. The Wi-Fi Alliance says Wi-Fi 6's OFDMA shares channels to lower latency, and Wi-Fi 7's Multi-Link Operation is designed to reduce latency. Your device has to support the same features, and neither fixes a weak signal caused by distance or walls."
  - q: "Should I use 2.4 GHz or 5 GHz for gaming?"
    a: "Use 5 GHz or 6 GHz if the signal is strong where you play. Apple notes interference is less of a concern on those bands than on 2.4 GHz. Use 2.4 GHz only if it is the only band with a usable signal at that spot."
  - q: "Is a wired connection still better for online gaming?"
    a: "Yes, when you can run one. A cable removes airtime contention and wireless retries entirely. Sony, for example, tells PS Portal users to try a wired connection for the PS5 console when Remote Play struggles."
sources:
  - title: "Validate Wi-Fi Throughput Testing and Troubleshooting"
    publisher: "Cisco"
    url: "https://www.cisco.com/c/en/us/support/docs/wireless/catalyst-9800-series-wireless-controllers/221766-validate-wi-fi-throughput-testing-and.html"
    date: 2026-07-08
  - title: "Advanced Settings for Intel Wireless Adapters"
    publisher: "Intel"
    url: "https://www.intel.com/content/www/us/en/support/articles/000005585/wireless.html"
    date: 2025-02-05
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple Support"
    url: "https://support.apple.com/102766"
    date: 2026-07-14
  - title: "Wi-Fi CERTIFIED 6"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/discover-wi-fi/wi-fi-certified-6"
    date: 2026-10-21
  - title: "Wi-Fi Alliance introduces Wi-Fi CERTIFIED 7"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-7"
    date: 2024-01-08
  - title: "Status of Project IEEE 802.11bn (TGbn)"
    publisher: "IEEE 802.11 Working Group"
    url: "https://grouper.ieee.org/groups/802/11/Reports/tgbn_update.htm"
    date: 2026-10-21
  - title: "PS Portal troubleshooting"
    publisher: "PlayStation"
    url: "https://www.playstation.com/en-us/support/hardware/psportal-troubleshooting/"
    date: 2026-03-25
---

If your ping is fine on Ethernet but high or spiky on Wi-Fi, the extra delay is usually being added on the wireless hop between your device and your router, not by your internet provider. The usual causes are a weak signal that forces packets to be resent, a busy channel where your device has to wait its turn, interference from nearby networks, and laptop adapter settings that scan for other networks or save power. Confirm it by pinging your router, then work through signal, channel and adapter fixes below. For competitive gaming, a cable is still the most reliable answer.

This is a research-based troubleshooting guide built on documentation from Cisco, Intel, Apple, Sony, the Wi-Fi Alliance and the IEEE. Your exact numbers will depend on your home, your router and your device.

## Step 1: Prove it's the Wi-Fi

Run two short tests from the same computer, one over Wi-Fi and one plugged in with a cable.

1. **Find your router's address.** On Windows, run `ipconfig` and note the "Default Gateway" (often something like 192.168.1.1). On a Mac, it's under System Settings > Network > your connection > Details > TCP/IP > Router.
2. **Ping the router 100 times.** Windows: `ping -n 100 192.168.1.1`. Mac: `ping -c 100 192.168.1.1`. Use your own gateway address.
3. **Repeat over Ethernet** and compare the average and the maximum.

How to read it:

- **Wi-Fi ping to the router is high or jumpy, wired is steady:** the wireless link is the problem. Keep reading.
- **Both are steady, but ping to a game server is high:** the delay is beyond your home network. Distance to the server and your provider's routing matter more than Wi-Fi.
- **Ping jumps on both when someone else is downloading or uploading:** that's queueing on your internet connection, known as bufferbloat. Our [bufferbloat guide]({{< relref "/guides/fix-bufferbloat-gaming-lag" >}}) covers the fix.

Look at the spread, not just the average. A few readings far above the rest are the spikes you feel in a game, even when the average looks fine.

## Why Wi-Fi adds delay that a cable doesn't

**Devices share the air and take turns.** Cisco's Wi-Fi troubleshooting guide describes Wi-Fi as "a half-duplex medium that has some management overhead" and a "shared medium." Devices on the same channel generally take turns to transmit. Cisco notes that "when channel utilization approaches 100%—or even 70%—clients contend for medium access, resulting in latency and collisions." Nearby networks on the same channel compete for that airtime too.

**Weak signal means resends.** When signal is weak, more transmissions fail and have to be sent again. Cisco suggests checking for 802.11 retries, noting that "a high retry percentage indicates RF issues." Every retry is time your game packet spends waiting. Cisco also points to "weak signal strength at the edge of your coverage" as a cause of poor performance.

**Interference.** Cisco names another access point on the same channel as a cause of interference and suggests narrower channel widths as one fix.

None of this happens on a cable, which is why the same device can show a steady ping wired and a ragged one wireless.

## Step 2: Fix the signal first

Distance and walls are common causes, and they cost nothing to test.

- **Move closer, or move the router.** A stronger signal means fewer failed transmissions to resend. Get the router out of cabinets and off the floor.
- **Use 5 GHz or 6 GHz when the signal is strong.** Apple's router guidance says interference is "less of a concern" on 5 GHz and 6 GHz. 2.4 GHz reaches farther but is more crowded. Our [band comparison]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}}) explains the trade-offs.
- **Pause big downloads on other devices** while you play. Sony suggests pausing downloads on other Wi-Fi devices in its PS Portal troubleshooting steps.

## Step 3: Clean up the router's channel settings

Apple publishes recommended router settings for Apple devices, and they're a sensible baseline for any home network:

- **Channel: Auto,** and if you have more than one router or access point, give each a different channel, "especially if they are close to each other."
- **Channel width:** 20 MHz on 2.4 GHz, which Apple says "helps to avoid performance and reliability issues," and Auto on 5 GHz and 6 GHz. Apple notes wider channels are faster but more prone to interference.
- **WMM: on.** Apple warns that disabling WMM "can affect the performance and reliability of devices on the network."
- **Turn on every band** your router supports, and avoid deprecated security modes, which Apple says "reduce network reliability and performance."

If a neighbor's network sits on your channel, picking a quieter one by hand can help. Our guide on [how to change your Wi-Fi channel]({{< relref "/guides/how-to-change-wifi-channel" >}}) shows how to check.

## Step 4: Check your laptop's Wi-Fi adapter settings

Spikes that recur at a regular rhythm may come from the adapter's periodic background scans, which Intel says are on by default. On Windows PCs with Intel Wi-Fi, these settings live in Device Manager > Network adapters > your Intel adapter > Advanced. Intel documents what each one does:

- **Roaming aggressiveness** sets "the signal strength threshold at which the WiFi adapter starts scanning for another candidate AP." The default is Medium. Intel describes the lowest setting as scanning for a new access point only when the current signal is very weak, which can mean fewer scans if your PC doesn't move.
- **Global BG scan blocking** controls the adapter's periodic background scans for other access points. Intel's default is Never; "On Good RSSI" scans only when the signal is low. Intel advises against changing it if you move around with the laptop during the day.
- **Throughput Booster** is off by default. Intel warns that when it's on, "the throughput for other clients in the same network may be negatively impacted," so leave it off on a shared network.
- **U-APSD** is a power-saving mode, off by default, that Intel says can have interoperability issues with some access points.

Intel doesn't publish how much any of these affects ping, so treat them as experiments: change one, rerun the 100-ping test, and keep it only if the spikes improve. For roaming aggressiveness, Intel recommends reverting to the default (Medium) if other values don't help. Other adapter brands use different names, and some don't expose these settings.

## Will a newer router help?

On a busy network, possibly. The Wi-Fi Alliance says Wi-Fi 6's OFDMA "effectively shares channels to increase network efficiency and lower latency." For Wi-Fi 7, it says Multi-Link Operation lets devices use multiple links at once for "increased throughput, reduced latency, and improved reliability." Our [Wi-Fi 7 MLO explainer]({{< relref "/guides/wifi-7-mlo" >}}) covers when that works in practice. Both ends need to support the feature, and no standard fixes a signal that's too weak because of distance or walls.

Lower latency is one of the stated goals of the next standard. The IEEE's 802.11bn project (expected to be called Wi-Fi 8) aims to reduce 95th-percentile latency by 25% compared with Wi-Fi 7. That is a design goal, not a measured result, and final IEEE approval is projected for 2028.

## When to stop tuning and run a cable

If ping to your router is still jumpy after you've improved signal and channels, the simplest fix is a wire for the device that cares most: a gaming PC or console. Sony's PS Portal troubleshooting page tells users to "try using a wired connection for your PS5 console" for Remote Play. If running Ethernet isn't practical, MoCA or powerline adapters can carry a wired connection over existing cables.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Wi-Fi is a shared, half-duplex medium; at high channel utilization (even 70%) clients contend, causing latency and collisions; high retries indicate RF issues; same-channel APs cause interference | [Cisco Wi-Fi throughput troubleshooting](https://www.cisco.com/c/en/us/support/docs/wireless/catalyst-9800-series-wireless-controllers/221766-validate-wi-fi-throughput-testing-and.html) | Qualified: enterprise documentation; the radio behavior applies to home Wi-Fi too |
| Intel roaming aggressiveness, background scan blocking, Throughput Booster and U-APSD definitions and defaults | [Intel advanced adapter settings](https://www.intel.com/content/www/us/en/support/articles/000005585/wireless.html) | Verified; Intel doesn't quantify latency effects |
| Apple's recommended channel, width, WMM and band settings | [Apple Support 102766](https://support.apple.com/102766) | Verified |
| Wi-Fi 6 OFDMA lowers latency; Wi-Fi 7 MLO aims at reduced latency | [Wi-Fi Alliance Wi-Fi 6](https://www.wi-fi.org/discover-wi-fi/wi-fi-certified-6), [Wi-Fi Alliance Wi-Fi 7 launch](https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-7) | Verified as Wi-Fi Alliance statements |
| 802.11bn target: 25% lower 95th-percentile latency vs. Wi-Fi 7; final approval projected 2028 | [IEEE TGbn status](https://grouper.ieee.org/groups/802/11/Reports/tgbn_update.htm) | Qualified: design target and projected timeline |
| Sony advises a wired PS5 connection and pausing downloads for PS Portal Remote Play | [PlayStation PS Portal troubleshooting](https://www.playstation.com/en-us/support/hardware/psportal-troubleshooting/) | Verified |
