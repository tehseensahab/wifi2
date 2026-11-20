---
title: "How to Fix Bufferbloat: Test It, Then Turn On SQM"
date: 2026-09-22
lastmod: 2026-11-20
description: "Bufferbloat is lag when your connection is busy. Test latency under load, then turn on SQM or smart queues at about 90% of your measured speed."
authors: ["Tehseen Arbab"]
topics: ["gaming-streaming", "how-to-fixes"]
tags: ["bufferbloat", "latency", "sqm", "qos", "gaming", "eero", "openwrt"]
summary: "Bufferbloat is the lag you get when a busy connection makes your game or call wait behind a long queue of other data. Test it with a speed test that measures latency while downloading and uploading, not just idle ping. The fix is a router feature called SQM (smart queue management): turn it on and, where your router asks, set it to about 90% of your measured speeds, then test again."
imageAlt: "Two people holding game controllers while playing a soccer game on a TV"
imageCredit: "Photo: JESHOOTS.COM / [Unsplash](https://unsplash.com/photos/eCktzGjC-iU)"
takeaways:
  - "Bufferbloat is extra delay from data queuing in network equipment when the connection is busy. The IETF calls queue buildup in network devices 'one major source of delay.'"
  - "A normal speed test's ping is measured idle. To spot bufferbloat you need latency measured during the download and upload, which Cloudflare's and Waveform's tests both report."
  - "The fix is active queue management, usually sold as SQM or smart queues. OpenWrt's guide says to set download and upload to 90% of your measured speeds; eero's SQM is a single switch."
  - "SQM can cost some top speed. eero warns some devices may see slower performance, and a 90% setting caps throughput below your plan."
faq:
  - q: "What is bufferbloat?"
    a: "Bufferbloat is the extra lag that appears when your internet connection is busy. Data waits in an oversized queue in your router, modem or provider's equipment, and your game or call packets wait behind it. Idle ping can look fine while ping under load jumps."
  - q: "How do I know if I have bufferbloat?"
    a: "Run a test that measures latency while the connection is loaded, such as Cloudflare's speed test or Waveform's bufferbloat test, on a wired computer with nothing else running. If latency during the download or upload is much higher than idle latency, you have bufferbloat."
  - q: "Will a faster internet plan fix bufferbloat?"
    a: "Not reliably. A faster plan can make the line fill up less often, but the queue still builds whenever something uses all of it. Queue management on the router addresses the cause."
  - q: "Is QoS the same as SQM?"
    a: "Not exactly. QoS usually means giving some apps or devices priority or bandwidth limits. SQM combines traffic shaping with active queue management to keep delay low for everything. Some routers sell both under one gaming or QoS menu."
  - q: "Does SQM slow down my internet?"
    a: "It can lower your top speed a little, because you set it below your measured speed so the router controls the queue. eero also says some devices may see slower performance with SQM on. Whether that trade is worth it depends on how much the lag bothers you."
sources:
  - title: "RFC 7567: IETF Recommendations Regarding Active Queue Management (BCP 197)"
    publisher: "IETF / RFC Editor"
    url: "https://www.rfc-editor.org/rfc/rfc7567.html"
    date: 2015-07-01
  - title: "RFC 8290: The Flow Queue CoDel Packet Scheduler and Active Queue Management Algorithm"
    publisher: "IETF / RFC Editor"
    url: "https://www.rfc-editor.org/rfc/rfc8290.html"
    date: 2018-01-01
  - title: "How does Cloudflare's Speed Test really work?"
    publisher: "Cloudflare Blog"
    url: "https://blog.cloudflare.com/how-does-cloudflares-speed-test-really-work/"
  - title: "Bufferbloat and Internet Speed Test"
    publisher: "Waveform"
    url: "https://www.waveform.com/tools/bufferbloat"
  - title: "SQM (Smart Queue Management)"
    publisher: "OpenWrt Wiki"
    url: "https://openwrt.org/docs/guide-user/network/traffic-shaping/sqm"
  - title: "What is Smart Queue Management (SQM)?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/what-is-smart-queue-management-sqm"
  - title: "SQM"
    publisher: "GL.iNet Docs"
    url: "https://docs.gl-inet.com/router/en/4/interface_guide/sqm/"
  - title: "What is Smart Queue?"
    publisher: "Firewalla Help Center"
    url: "https://help.firewalla.com/hc/en-us/articles/360056976594"
  - title: "[Adaptive QoS] Introduction and settings of QoS on ASUS Router"
    publisher: "ASUS Support"
    url: "https://www.asus.com/us/support/FAQ/1010935/"
  - title: "Configuring CoDel Limiters for Bufferbloat"
    publisher: "Netgate Docs (pfSense)"
    url: "https://docs.netgate.com/pfsense/en/latest/recipes/codel-limiters.html"
---

To fix bufferbloat, turn on your router's SQM (smart queue management) or smart queue feature. Where it asks for your speeds, set them to about 90% of what a wired speed test measures, then test again. First confirm bufferbloat is the problem: run a speed test that measures latency while it downloads and uploads, and compare that with idle latency. A big jump under load is bufferbloat.

This is a research-based guide built from IETF standards and router makers' documentation. We have not measured bufferbloat on specific routers ourselves.

## What is bufferbloat?

Bufferbloat is the extra delay that appears when your connection is busy. When someone uploads a video or a console starts a large download, more data arrives than the line can send at once, so it waits in a queue. If that queue is long, your game or call packets wait in it too. Idle ping can look fine, then jump when the line fills.

The IETF's guidance on active queue management, RFC 7567, says "one major source of delay is the buildup of queues in network devices." It recommends that network devices implement some active queue management (AQM): software that keeps queues short instead of letting them fill. OpenWrt's documentation describes bufferbloat as undesirable latency that arises when your router buffers too much data, and says it is most evident when the connection is heavily loaded.

## How do I test for bufferbloat?

You need a test that measures latency while the connection is busy. Cloudflare's speed test records idle latency first, then sends small requests during the download and upload to measure what it calls loaded latency, the round-trip time while your connection is busy. Waveform's bufferbloat test also measures latency at idle, during the download and during the upload.

1. **Plug a computer into the router with Ethernet,** so Wi-Fi isn't part of the result.
2. **Pause other traffic.** Stop large downloads, cloud backups and streaming on other devices.
3. **Run the test** at Cloudflare's speed test or Waveform's bufferbloat test.
4. **Compare the numbers.** Look at latency during download and during upload against idle latency.
5. **Write down your download and upload speeds.** You'll need them for the fix.

| What you see | What it means | Next step |
|---|---|---|
| Loaded latency close to idle | Little or no bufferbloat | Look elsewhere: Wi-Fi, the game server or your route to it |
| Latency jumps during upload | Upload queue is filling | Turn on SQM |
| Latency jumps during download | Download queue is filling | Turn on SQM |
| Wired test fine, Wi-Fi lags | Wi-Fi link, not your internet line | See our [high ping on Wi-Fi guide](/guides/high-ping-on-wifi/) |

If upload is where it spikes, our guide to [why upload speed is slow](/guides/why-is-my-upload-speed-slow/) explains why uploads are often the narrow part of a cable connection.

## How do I fix bufferbloat?

Turn on active queue management in your router. Different makers name it differently:

| Router or firmware | Setting | What its maker says |
|---|---|---|
| eero | SQM: Settings, Advanced networking, Network services, SQM | Can "help reduce latency" for voice calls, video calls and online gaming; some devices may see slower performance; not available in bridge mode |
| OpenWrt | SQM QoS package | Set download and upload to 90% of measured speeds; Cake is the preferred algorithm, fq_codel a faster but less thorough option |
| GL.iNet | Flow control, then SQM | Manages traffic to minimize latency and bufferbloat |
| Firewalla | Smart Queue | Turning it on turns on AQM to decrease latency (bufferbloat) |
| pfSense | FQ_CODEL limiters | Can help alleviate bufferbloat; most results should reach an A or higher after setup, Netgate says |
| ASUS | Adaptive QoS or Adaptive QoE, Bandwidth Limiter | Prioritizes app types and caps per-device bandwidth; ASUS's guide does not describe it as bufferbloat control |

The steps are similar on most routers that ask for speeds:

1. **Find the setting.** Look for SQM, Smart Queue, QoS or AQM.
2. **Enter your speeds at about 90% of what you measured.** OpenWrt's guide uses 90%.
3. **Save, then run the same test again.** Loaded latency should be much closer to idle.
4. **Adjust in small steps.** If latency is still high, lower the speeds a little. If it's already low, you can try nudging them up.

Why set it below your real speed? A queue builds wherever the slowest link is. If your router sends data slightly slower than the line can carry it, the queue forms in the router, where SQM can keep it short, instead of in the modem or your provider's equipment, where you can't control it.

The algorithms behind SQM are published standards. RFC 8290 describes FQ-CoDel, which mixes packets from many connections so a big transfer can't hold up small, time-sensitive packets behind it.

## What if my router has no SQM?

Check your router's app or manual for SQM, smart queues, QoS or "gaming" settings first. Our guide to [whether you need a gaming router](/guides/do-you-need-a-gaming-router/) explains what the gaming-branded features do. If there's nothing, you have three options:

- **Use priority or bandwidth limits.** ASUS-style QoS can cap the device that floods the line, such as a PC running cloud backups.
- **Schedule the big transfers.** Move backups and console downloads to overnight.
- **Replace the router** with one whose maker documents SQM or AQM, or one that runs OpenWrt.

## Does a faster plan or Wi-Fi 7 fix bufferbloat?

Not by itself. A faster plan fills up less often, but whenever something uses the whole line, the queue builds again. A newer Wi-Fi standard changes the wireless link inside your home, not the queue at your internet connection. If lag only happens on Wi-Fi and not on a cable, that's a different problem; see [Wi-Fi slow but internet fast](/guides/wifi-slow-but-internet-fast/). For video calls, our [router settings for Zoom and Teams](/guides/router-settings-for-video-calls/) guide covers the rest of the checklist.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Queue buildup in network devices is a major source of delay; devices should implement some AQM; no specific algorithm required by default | [RFC 7567](https://www.rfc-editor.org/rfc/rfc7567.html) | Verified |
| FQ-CoDel mixes packets from multiple flows and reduces head-of-line blocking from bursty traffic | [RFC 8290](https://www.rfc-editor.org/rfc/rfc8290.html) | Verified (Experimental RFC) |
| Cloudflare measures idle latency first, then loaded latency during download and upload | [Cloudflare Blog](https://blog.cloudflare.com/how-does-cloudflares-speed-test-really-work/) | Verified |
| Waveform measures latency at idle and during download and upload | [Waveform](https://www.waveform.com/tools/bufferbloat) | Qualified: the tool's page did not load for our fetch; confirmed from its published description |
| Bufferbloat definition; set SQM to 90% of measured speed; Cake preferred, fq_codel faster but less comprehensive | [OpenWrt Wiki](https://openwrt.org/docs/guide-user/network/traffic-shaping/sqm) | Verified from the page text; the wiki blocks automated fetches |
| eero SQM path, latency claim, slower performance on some devices, not in bridge mode | [eero Support](https://eero.com/support/articles/what-is-smart-queue-management-sqm) | Verified |
| GL.iNet SQM location and purpose | [GL.iNet Docs](https://docs.gl-inet.com/router/en/4/interface_guide/sqm/) | Verified |
| Firewalla Smart Queue turns on AQM to decrease bufferbloat | [Firewalla Help](https://help.firewalla.com/hc/en-us/articles/360056976594) | Verified |
| pfSense FQ_CODEL limiters help bufferbloat; most results reach A or higher | [Netgate Docs](https://docs.netgate.com/pfsense/en/latest/recipes/codel-limiters.html) | Verified |
| ASUS Adaptive QoS prioritizes app types; Bandwidth Limiter caps per-device speeds | [ASUS Support](https://www.asus.com/us/support/FAQ/1010935/) | Verified |

## Bottom line

Test before you change anything: wired, quiet network, and look at latency during download and upload rather than idle ping. If it jumps, turn on SQM or smart queues, set them to about 90% of your measured speeds, and test again. A faster plan or a gaming-branded router doesn't fix the queue itself; this setting does.
