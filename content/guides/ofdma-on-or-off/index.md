---
title: "OFDMA: On or Off? What the Wi-Fi 6 Setting Does"
date: 2026-11-24T05:00:00Z
description: "OFDMA on or off? Turn it on if most devices are Wi-Fi 6 or newer, especially with many smart-home gadgets; leave it off if older devices start acting up."
authors: ["Tehseen Arbab"]
topics: ["routers", "how-to-fixes", "wifi-6e-7"]
tags: ["ofdma", "router-settings", "wifi-6", "netgear", "tp-link", "asus", "troubleshooting"]
summary: "Turn OFDMA on if most of your devices are Wi-Fi 6 or newer, and especially if you have many smart-home devices; NETGEAR's manual recommends it for IoT-heavy networks. Some routers ship with it off, and NETGEAR says to switch it off again if devices stop working as expected, and that homes with many older devices might want to keep it off."
imageAlt: "White smart-home devices grouped on a gray surface: a security camera, a smart plug, a motion sensor, a lit smart bulb and two round sensors"
imageCredit: "Photo: Jakub Żerdzicki / [Unsplash](https://unsplash.com/photos/a-group-of-electronic-devices-sitting-on-top-of-a-table-uxYLtGRyGKQ)"
takeaways:
  - "OFDMA is a Wi-Fi 6 feature that shares a channel between several devices at once. Wi-Fi Alliance says it raises efficiency and lowers latency for uploads and downloads, especially on busy networks."
  - "It can be off out of the box. TP-Link's Archer AX73 guide says 'It is disabled by default,' and NETGEAR's RAXE300 manual says it is disabled in both radio bands (6 GHz is listed separately as on)."
  - "NETGEAR's advice: 'Enable OFDMA if your network includes many Internet of things (IoT) devices.'"
  - "The risk is compatibility. NETGEAR says to disable OFDMA if some devices 'do not function as expected' and to consider leaving it off if you have many older devices."
  - "Your devices need to support it too. TP-Link says you get the full benefit only 'when your clients also support OFDMA.'"
faq:
  - q: "Should OFDMA be on or off?"
    a: "On, if most of your devices are Wi-Fi 6 or newer and nothing misbehaves after you enable it. NETGEAR recommends it for networks with many smart-home devices. Leave it off, or turn it back off, if older devices stop working properly."
  - q: "Is OFDMA on by default?"
    a: "It depends on the router. TP-Link's Archer AX73 guide says it is disabled by default, and NETGEAR's RAXE300 manual says it is disabled on the 2.4 and 5 GHz bands by default. Check your router's wireless settings rather than assuming."
  - q: "Does OFDMA help gaming?"
    a: "It can lower Wi-Fi latency when many devices share the network. A Qualcomm analysis published on Wi-Fi Alliance's blog calls the effect 'highly relevant' for gaming and video calls, but also says results are 'highly dependent on the traffic load.' It won't fix lag that comes from your internet connection or the game server."
  - q: "What is the difference between OFDMA and MU-MIMO?"
    a: "Both let a router serve several devices at once. OFDMA divides a channel into narrower slices for different devices; MU-MIMO, in Wi-Fi Alliance's words, 'allows more downlink data to be transferred at once.' Wi-Fi Alliance lists both as Wi-Fi CERTIFIED 6 features, and some routers, such as ASUS models, combine them in one setting."
  - q: "Can OFDMA cause Wi-Fi problems?"
    a: "It can with some devices. NETGEAR's manual says that if some devices don't work as expected after you enable OFDMA, you should disable it, and that homes with many older devices might want to keep it off."
sources:
  - title: "Wi-Fi CERTIFIED 6 delivers new Wi-Fi era"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/news-events/newsroom/wi-fi-certified-6-delivers-new-wi-fi-era"
    date: 2019-09-16
  - title: "Nighthawk AXE7800 Tri-Band WiFi 6E Router Model RAXE300 User Manual"
    publisher: "NETGEAR"
    url: "https://www.downloads.netgear.com/files/GDC/RAXE300/RAXE300_UM_EN.pdf"
  - title: "Archer AX73 V1 User Guide: Wireless Settings"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/us/user-guides/archer-ax73_v1/chapter-6-wireless-settings"
  - title: "[Wireless Router] How to do Professional Wireless settings"
    publisher: "ASUS"
    url: "https://www.asus.com/us/support/FAQ/1011438"
    date: 2025-09-12
  - title: "What is WiFi 6? (802.11ax)"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/us/wifi6/"
  - title: "Reduced latency benefits of Wi-Fi 6 OFDMA"
    publisher: "Wi-Fi Alliance (Rolf de Vegt, Qualcomm)"
    url: "https://www.wi-fi.org/beacon/rolf-de-vegt/reduced-latency-benefits-of-wi-fi-6-ofdma"
  - title: "Uplink-OFDMA, a game changer for Wi-Fi CERTIFIED networks"
    publisher: "Wi-Fi Alliance (Nitin Madan, Broadcom)"
    url: "https://www.wi-fi.org/beacon/nitin-madan/uplink-ofdma-a-game-changer-for-wi-fi-certified-networks"
---

**Turn OFDMA on if most of your devices are Wi-Fi 6 or newer, and especially if your home has lots of smart-home gadgets.** NETGEAR's RAXE300 manual says, "Enable OFDMA if your network includes many Internet of things (IoT) devices." Some routers, including TP-Link's Archer AX73 and NETGEAR's RAXE300, ship with it switched off, so you may need to enable it yourself. The catch is compatibility: NETGEAR says to disable OFDMA again if some devices "do not function as expected," and that homes with many older devices "might want to keep OFDMA disabled."

This guide is based on Wi-Fi Alliance material and NETGEAR, TP-Link and ASUS support documents. We have not tested OFDMA on specific routers.

## What does OFDMA do?

OFDMA stands for orthogonal frequency division multiple access. It is one of the features Wi-Fi Alliance listed when it launched Wi-Fi CERTIFIED 6 on Sept. 16, 2019, describing it as a feature that "effectively shares channels to increase network efficiency and lower latency for both uplink and downlink traffic."

The basic idea: instead of giving the whole channel to one device for each transmission, the router splits the channel into narrower slices and serves several devices in the same transmission. H3C, quoted in that Wi-Fi Alliance announcement, describes it as technology "which divides the WLAN channel into multiple narrower subchannels." TP-Link's Wi-Fi 6 page uses a delivery-truck analogy: with Wi-Fi 5, each truck "could only deliver one parcel to one device at a time," while with OFDMA "each truck can deliver multiple parcels to multiple devices simultaneously."

That makes OFDMA a Wi-Fi efficiency feature. It changes how your router shares airtime between devices; it does not change the speed of your internet plan.

### Where OFDMA helps most

NETGEAR specifically recommends OFDMA for networks with many IoT devices, such as smart plugs, speakers and sensors. Wi-Fi Alliance's launch description also ties the benefit to "high demand environments," meaning many devices sharing the network.

Latency is the other benefit. In a post on Wi-Fi Alliance's blog, Qualcomm's Rolf de Vegt writes that "Reductions in network latencies are some of the major benefits of OFDMA" and that the effect is "highly relevant for real-time applications such as gaming and voice/video calling." For a home scenario, Qualcomm's analysis found OFDMA "delivers a downlink latency reduction of up to 40% and an uplink latency reduction of up to 63%." Treat those as a chip maker's own upper-bound figures, not a promise: the same post says "The latency achieved in practice is highly dependent on the traffic load."

## Should OFDMA be on or off?

| Your situation | Setting | Why |
|---|---|---|
| Most devices are Wi-Fi 6 or newer | **On** | TP-Link says the full benefit comes only when clients also support OFDMA |
| Many smart-home (IoT) devices | **On** | NETGEAR recommends enabling OFDMA for IoT-heavy networks |
| Some devices stop working properly after you enable it | **Off** | NETGEAR's troubleshooting advice |
| Many older (pre-Wi-Fi 6) devices | **Consider leaving it off** | NETGEAR says such homes "might want to keep OFDMA disabled" |
| You want a faster internet plan speed | **No effect** | OFDMA changes how Wi-Fi airtime is shared, not what your ISP delivers |

Change one setting at a time. If you switch OFDMA, [MU-MIMO](/guides/mu-mimo-on-or-off/) and [Wi-Fi 7 mode](/guides/wifi-7-mode-on-or-off/) together, you won't know which one fixed or caused a problem. Give the network a day of normal use before judging.

## Is OFDMA on by default?

Not always, and that is the main reason this setting is worth checking.

- **TP-Link (Archer AX73 v1):** the user guide says OFDMA "enables multiple users to transmit data simultaneously" and "It is disabled by default."
- **NETGEAR (Nighthawk RAXE300):** the February 2022 manual says, "By default, OFDMA is disabled in both radio bands, even when AX WiFi is enabled." The same section also says "OFDMA in 6 GHz is enabled by default," so the manual is inconsistent; on this tri-band model the 6 GHz band appears to be the exception. NETGEAR's MU-MIMO setting on the same router, by contrast, "is enabled by default."
- **ASUS:** the Professional wireless settings FAQ lists an "OFDMA / MU-MIMO" option for each band but doesn't state a default, and notes that "Some features may vary due to different models and different firmware versions."

These are single-model documents. Your router may use different defaults or labels, so open its wireless settings and look.

## How to turn OFDMA on or off

### NETGEAR

On the RAXE300, NETGEAR's manual lets you "enable Orthogonal Frequency-Division Multiple-Access (OFDMA) for each radio band independently." Sign in to the router's web interface, then on the **BASIC Home** page select **Wireless** and select or clear the **Enable OFDMA** check box for each band (on the RAXE300 the 6 GHz box is labeled **Enable OFDMA in 6GHz**), then save the change. Menu names vary by model, so check your own router's manual if the option isn't there.

### TP-Link

On the Archer AX73 v1, go to **Advanced > Wireless > Wireless Settings** and enable or disable **OFDMA**. TP-Link notes that "only when your clients also support OFDMA, can you fully enjoy the benefits."

### ASUS

ASUS puts the option under **Wireless > Professional**, where it says "we provide several functions for each band." Look for **OFDMA / MU-MIMO** on each band's tab. Because the choices differ by model and firmware, pick the option that enables OFDMA, apply it, and watch for devices that drop off.

### Other brands

Some app-managed mesh systems may not show an OFDMA setting. If yours doesn't, check the maker's support pages before assuming the feature is missing.

## OFDMA vs. MU-MIMO

Both features let a router serve several devices at once, and some routers, such as ASUS models, combine them in one setting.

- **OFDMA** splits a channel into narrower slices so several devices share one transmission. Wi-Fi Alliance describes it as working for "both uplink and downlink traffic."
- **MU-MIMO** lets the router transmit to several devices at the same time. Wi-Fi Alliance's 2019 launch list described it as allowing "more downlink data to be transferred at once."

Uplink OFDMA matters for devices sending data back to the router. Broadcom's Nitin Madan, writing on Wi-Fi Alliance's blog, says "Uplink-OFDMA reduces collisions and overhead, improving the performance of the network." For more on the other setting, see [MU-MIMO: On or Off?](/guides/mu-mimo-on-or-off/)

## If you're shopping for a router

OFDMA arrived with Wi-Fi 6, so it isn't a feature to shop for on its own. It matters more that your router has enough coverage for the house. If you're upgrading a busy, multi-device home, start with our guides to the [best Wi-Fi router for a large house](/guides/best-wifi-router-for-large-house/) and [Wi-Fi 6 vs. Wi-Fi 6E](/guides/wifi-6-vs-wifi-6e/).

## Bottom line

If your router offers OFDMA and most of your devices are Wi-Fi 6 or newer, turn it on, especially in a home full of smart-home gadgets. If an older laptop, camera or plug starts misbehaving afterward, turn it off again; that is what NETGEAR advises.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| OFDMA is a Wi-Fi CERTIFIED 6 feature that shares channels to raise efficiency and lower latency, uplink and downlink | [Wi-Fi Alliance, Sept. 16, 2019](https://www.wi-fi.org/news-events/newsroom/wi-fi-certified-6-delivers-new-wi-fi-era) | Verified |
| NETGEAR: enable OFDMA for IoT-heavy networks; disable if devices misbehave; consider off with many older devices | [NETGEAR RAXE300 manual, Feb. 2022](https://www.downloads.netgear.com/files/GDC/RAXE300/RAXE300_UM_EN.pdf) | Verified |
| NETGEAR RAXE300 default: off on 2.4 and 5 GHz; 6 GHz described as on | [NETGEAR RAXE300 manual](https://www.downloads.netgear.com/files/GDC/RAXE300/RAXE300_UM_EN.pdf) | Qualified (one model; manual is internally inconsistent) |
| TP-Link Archer AX73: disabled by default; full benefit only if clients support OFDMA | [TP-Link Archer AX73 v1 user guide](https://www.tp-link.com/us/user-guides/archer-ax73_v1/chapter-6-wireless-settings) | Verified (one model) |
| ASUS: OFDMA / MU-MIMO option under Wireless > Professional; features vary by model and firmware | [ASUS FAQ 1011438, updated Sept. 12, 2025](https://www.asus.com/us/support/FAQ/1011438) | Verified |
| Home-scenario latency reductions of up to 40% (downlink) and 63% (uplink) | [Qualcomm post on Wi-Fi Alliance blog](https://www.wi-fi.org/beacon/rolf-de-vegt/reduced-latency-benefits-of-wi-fi-6-ofdma) | Qualified (vendor analysis; depends on traffic load) |
| Wi-Fi 5 vs. OFDMA delivery-truck analogy; works for uploads and downloads | [TP-Link Wi-Fi 6 page](https://www.tp-link.com/us/wifi6/) | Verified (marketing page) |
| Uplink OFDMA reduces collisions and overhead | [Broadcom post on Wi-Fi Alliance blog](https://www.wi-fi.org/beacon/nitin-madan/uplink-ofdma-a-game-changer-for-wi-fi-certified-networks) | Qualified (vendor author) |
