---
title: "160 MHz Channel Width: On or Off? What to Know"
date: 2026-11-25T04:55:00Z
description: "160 MHz on or off? Turn it on (or Auto) if your devices support it; go back to 80 MHz if radar checks keep knocking devices off or older gear won't connect."
authors: ["Tehseen Arbab"]
topics: ["routers", "how-to-fixes", "wifi-6e-7"]
tags: ["160-mhz", "channel-width", "dfs", "router-settings", "5-ghz", "netgear", "asus", "tp-link", "google-nest-wifi"]
summary: "Turn 160 MHz on, or set channel width to Auto as Apple recommends, if your phones and laptops support it and your connection stays stable. On 5 GHz, 160 MHz usually means using DFS channels shared with radar, so if devices keep dropping off after radar checks or an older device won't connect, go back to 80 MHz."
imageAlt: "White spherical weather radar dome on a steel lattice tower above a green cornfield under a blue sky with clouds"
imageCredit: "Photo: Roger Starnes Sr / [Unsplash](https://unsplash.com/photos/o--lAWssg5I)"
takeaways:
  - "160 MHz joins two 80 MHz channels into one wider channel. TP-Link says a wider channel 'allows more data to be transmitted at the same time,' but it also uses more spectrum and is more susceptible to interference."
  - "It is often off by default on 5 GHz. NETGEAR says its RAX200 'operates in 80 MHz by default' on the 5G-2 band, and D-Link says its AQUILA PRO AI router doesn't switch to the DFS channels 160 MHz needs by default."
  - "On 5 GHz, 160 MHz generally means DFS channels. When the router detects radar, ASUS and D-Link routers drop to 80 MHz, and ASUS warns clients can be disconnected for a period of time."
  - "Apple recommends setting channel width to 'Auto or all widths' for 5 GHz and 6 GHz, and 20 MHz for 2.4 GHz."
  - "On 6 GHz, Google says its routers' 6 GHz band has 160 MHz enabled by default; the on/off question is mostly about 5 GHz."
faq:
  - q: "Should 160 MHz be on or off?"
    a: "On, or Auto, if your devices support 160 MHz and your Wi-Fi stays stable afterward. Turn it off (back to 80 MHz) if devices periodically drop off, the router keeps changing channels because of radar, or an older device can no longer connect to 5 GHz."
  - q: "Why does my router keep dropping from 160 MHz to 80 MHz?"
    a: "On 5 GHz, 160 MHz usually relies on DFS channels that are shared with radar. ASUS says that if a 160 MHz device on a DFS channel connects at 80 MHz, the router has detected radar and switched to an 80 MHz channel. D-Link says its AQUILA PRO AI runs at 80 MHz until DFS becomes available again."
  - q: "Does 160 MHz make my internet faster?"
    a: "It can raise the speed of the Wi-Fi link between a supporting device and the router, which helps when Wi-Fi is the bottleneck. It cannot make your internet plan faster than what your provider delivers."
  - q: "Is 160 MHz on by default?"
    a: "Often not on 5 GHz. NETGEAR's RAX200 runs its 5G-2 band at 80 MHz by default, and D-Link's AQUILA PRO AI needs DFS turned on before it will use 160 MHz. Google says 6 GHz has 160 MHz on by default, while its 5 GHz 160 MHz mode (using the 5.9 GHz UNII-4 channel) is a setting you turn on or off in the Google Home app."
  - q: "Should I use 160 MHz on 2.4 GHz?"
    a: "No. Apple recommends 20 MHz for 2.4 GHz. 160 MHz is a 5 GHz and 6 GHz setting."
sources:
  - title: "Brief introduction of Wireless Channel, Channel Width and DFS"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/us/support/faq/4309/"
    date: 2024-11-12
  - title: "What is DFS (Dynamic Frequency Selection) and how does it work on ASUS router?"
    publisher: "ASUS"
    url: "https://www.asus.com/support/faq/1045936/"
    date: 2024-12-13
  - title: "Does the 5G-2 WiFi band of my RAX200 have 160MHz channel bandwidth enabled by default?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/000061423/Does-the-5G-2-WiFi-band-of-my-RAX200-have-160MHz-channel-bandwidth-enabled-by-default"
    date: 2025-07-07
  - title: "Is the 160MHz bandwidth over 5Ghz available by default on my D-Link Wi-Fi 6 router?"
    publisher: "D-Link"
    url: "https://www.dlink.com/en/support/faq/aquilaproai/device-configuration/wifi-connection/is-the-160mhz-bandwidth-over-5ghz-available-by-default-on-my-dlink-wifi-6-router"
  - title: "Enable better performance with 160 MHz channel using 5.9 GHz (UNII-4) (US only)"
    publisher: "Google"
    url: "https://support.google.com/googlenest/answer/12495633"
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple"
    url: "https://support.apple.com/102766"
    date: 2026-07-14
---

**Turn 160 MHz on, or set channel width to Auto, if your phones and laptops support it and your Wi-Fi stays stable afterward.** A 160 MHz channel is twice as wide as the usual 80 MHz one, and TP-Link says a wider channel "allows more data to be transmitted at the same time, resulting in higher data rates." The catch is on 5 GHz: 160 MHz generally means using DFS channels shared with radar, and when the router detects radar it drops to 80 MHz or changes channel, which ASUS says can disconnect devices "for a period of time." If that keeps happening, or an older device can't connect, go back to 80 MHz.

This guide is based on support documents from TP-Link, ASUS, NETGEAR, D-Link, Google and Apple. We have not tested 160 MHz on specific routers.

## What does 160 MHz channel width do?

Channel width is how much radio spectrum one Wi-Fi channel uses. TP-Link's explainer describes 160 MHz as two 80 MHz channels combined: VHT160 "allows two VHT80 channels to be bound to one 160MHz channel."

A wider channel can carry more data at once, so a device that supports 160 MHz can connect at a higher link rate. TP-Link also lists the cost: "wider channels consume more of the available spectrum," and the page adds that they are more susceptible to interference. In practice, a channel that covers more spectrum has more room to overlap with neighbors' networks, which matters most in apartment buildings.

Two limits are worth keeping in mind:

- **It only helps devices that support it.** A device that can't use 160 MHz usually connects at a narrower width and gets no benefit; Google notes some older devices aren't compatible with its 160 MHz mode at all.
- **It speeds up Wi-Fi, not your internet plan.** A faster Wi-Fi link helps when Wi-Fi is the bottleneck, for example copying files between devices at home or using a multi-gig plan. It can't make your plan faster than what your provider delivers. If your speed test over Wi-Fi already matches your plan, 160 MHz won't change that.

## Should 160 MHz be on or off?

| Your situation | Setting | Why |
|---|---|---|
| Your devices support 160 MHz and Wi-Fi stays stable | **On, or Auto** | Apple recommends "Auto or all widths" on 5 GHz and 6 GHz |
| Devices periodically drop off, or the 5 GHz channel keeps changing | **Off (80 MHz)** | Radar detection on DFS channels forces a channel change; ASUS says clients can be disconnected |
| An older device can't see or join the 5 GHz network | **Off (80 MHz)** | Google says some older 5 GHz devices "aren't compatible with the 160 MHz channel mode" (its UNII-4 setting) |
| Lots of nearby networks and interference | **Try 80 MHz** | TP-Link says wider channels are more susceptible to interference; ASUS doesn't recommend DFS channels where interference is heavy |
| 2.4 GHz band | **20 MHz** | Apple's recommendation for 2.4 GHz |
| 6 GHz band | **Leave the default** | Google says 6 GHz has 160 MHz enabled by default on its routers |

## Is 160 MHz on by default?

On 5 GHz, often not. Two examples from maker support pages:

- **NETGEAR RAX200 (North American model):** "the 5G-2 WiFi band of your RAX200 operates in 80 MHz by default," which NETGEAR says is to balance "optimal WiFi performance and coverage." You have to turn 160 MHz on in the router's web interface.
- **D-Link AQUILA PRO AI:** "the router does not switch to DFS channels by default," and D-Link says "you must enable the DFS function in order to switch to 160MHz."

Google's routers handle the two bands differently (its help page doesn't name models). Google says "The 6 GHz band automatically has 160 MHz channel bandwidth enabled by default," while 160 MHz on 5 GHz is a setting with its own on and off steps (more on that below).

Other routers may differ, so check your own router's wireless settings rather than assuming.

## Why 160 MHz and DFS go together

In the 5 GHz band, some channels are shared with radar systems. TP-Link says "Channels that are typically in U-NII-2A and U-NII-2C require the utilization of DFS," which stands for Dynamic Frequency Selection. A router using those channels has to listen for radar and move off the channel if it hears any.

On the NETGEAR and D-Link routers covered here, turning on 160 MHz means using those DFS channels. NETGEAR says "Enabling 160 MHz channel bandwidth forces the 5G-2 band to operate in DFS channels" on the RAX200, adding that you "might be unable to manually select a WiFi channel." D-Link puts it the same way: "using 160MHz channels requires the network to run with Dynamic Frequency Selection channels (DFS)."

### What happens when radar is detected

- **ASUS:** if radar is detected while the router is using a 160 MHz DFS channel, "it automatically switches to a channel in the 80MHz bandwidth." Before using a DFS channel, the router runs a Channel Availability Check that "would take 1-10 minutes depending on the country."
- **D-Link:** "if a network using 160MHz channels encounters a DFS strike, the network will dynamically switch to 80MHz operation until DFS becomes available again."
- **Effect on devices:** ASUS says the channel change "will cause connected WiFi clients to be disconnected from the network for a period of time."

That is the main practical reason to turn 160 MHz off. If your laptop or TV regularly drops off Wi-Fi for a while and comes back, and your router's log shows radar or DFS events, 80 MHz on a non-DFS channel may be more reliable even though its peak speed is lower. ASUS also offers a simple tell: if a device that supports 160 MHz shows an 80 MHz connection on a DFS channel, the router has detected radar.

### The 5.9 GHz (UNII-4) exception on Google routers

Google offers a different route to 160 MHz in the US. Its support page says "The 5.9 GHz band, also known as UNII-4, enables access to a 160 MHz channel that is permitted in the US only." Google warns that "some older 5 GHz-capable client devices aren't compatible with the 160 MHz channel mode" and suggests checking with your device's maker. The page doesn't name which Google router models offer the setting.

## How to turn 160 MHz on or off

Menu names vary, but the setting is usually in the 5 GHz wireless settings, sometimes labeled "Channel bandwidth" or "Channel width."

- **NETGEAR (RAX200 example):** log in at routerlogin.net, select **Wireless**, and under the 5GHz-2 section choose the mode "Up to 4800 Mbps," which NETGEAR's article uses to enable 160 MHz. Other NETGEAR models label this differently.
- **ASUS:** go to **Wireless > General** and select the 5 GHz band. ASUS's DFS article tells you to "uncheck [160MHz] channel bandwidth" to stop using it.
- **D-Link (AQUILA PRO AI):** log in at 192.168.200.1, open **Advanced Settings**, and enable **DFS channel**; D-Link says that is what lets the router switch to 160 MHz.
- **Google:** in the Google Home app, go to **Wi-Fi > Network settings > Advanced networking** and turn on **Use 160 MHz channel for maximum performance on 5 GHz**. Follow the same steps and tap **Off** to disable it.

After changing it, reconnect your main devices and run a speed test on each. If nothing got faster, or something got less stable, there's no reason to keep it on.

## Related settings

160 MHz is one of several 5 GHz options you'll find in the same menu. Our guides to [changing your Wi-Fi channel](/guides/how-to-change-wifi-channel/), [2.4 GHz vs. 5 GHz vs. 6 GHz](/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi/), [OFDMA](/guides/ofdma-on-or-off/) and [MU-MIMO](/guides/mu-mimo-on-or-off/) cover the others. If you have Wi-Fi 6E or Wi-Fi 7 devices, Google says the 6 GHz band on its routers already uses 160 MHz by default.

## Bottom line

If your router and devices support 160 MHz, turn it on or set Auto and see whether speeds improve. If devices start dropping off for a while at a time, or an older device can't connect, go back to 80 MHz: a stable connection beats a wider one that keeps getting interrupted by radar checks.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| 160 MHz binds two 80 MHz channels; wider channels give higher data rates but use more spectrum and are more susceptible to interference | [TP-Link FAQ 4309, updated Nov. 12, 2024](https://www.tp-link.com/us/support/faq/4309/) | Verified |
| U-NII-2A and U-NII-2C channels require DFS | [TP-Link FAQ 4309](https://www.tp-link.com/us/support/faq/4309/) | Verified |
| RAX200 5G-2 band runs at 80 MHz by default; 160 MHz forces DFS channels | [NETGEAR KB 000061423, updated July 7, 2025](https://kb.netgear.com/000061423/Does-the-5G-2-WiFi-band-of-my-RAX200-have-160MHz-channel-bandwidth-enabled-by-default) | Verified (one model, North American SKUs) |
| D-Link: 160 MHz requires DFS, DFS is off by default, network drops to 80 MHz after a DFS strike | [D-Link AQUILA PRO AI FAQ](https://www.dlink.com/en/support/faq/aquilaproai/device-configuration/wifi-connection/is-the-160mhz-bandwidth-over-5ghz-available-by-default-on-my-dlink-wifi-6-router) | Verified (one model; undated) |
| ASUS: radar detection moves a 160 MHz DFS channel to 80 MHz; check takes 1-10 minutes; clients can be disconnected | [ASUS FAQ 1045936, updated Dec. 13, 2024](https://www.asus.com/support/faq/1045936/) | Verified |
| Google: 160 MHz via 5.9 GHz (UNII-4) is US-only; some older devices aren't compatible; 6 GHz has 160 MHz on by default | [Google Nest Help](https://support.google.com/googlenest/answer/12495633) | Verified (undated; models not named) |
| Apple: 20 MHz on 2.4 GHz; Auto or all widths on 5 GHz and 6 GHz | [Apple Support 102766, published July 14, 2026](https://support.apple.com/102766) | Verified |
