---
title: "Bufferbloat explained: why games lag when someone uploads"
date: 2026-09-22
description: "Why your ping spikes when the network is busy, how to test for it, and how to fix it with smart queue management."
author: "Marcus Reyes"
topics: ["gaming-streaming", "how-to-fixes"]
tags: ["bufferbloat", "latency", "qos", "gaming"]
summary: "Bufferbloat is the lag you get when a busy connection makes data wait in a long queue. Test it with a speed test that measures latency under load, then turn on your router's smart queue or SQM feature and set it a little below your real speed. Wiring your console or PC also removes WiFi from the equation."
imageAlt: "Gaming console connected to a router with an Ethernet cable on a TV stand"
sample: true
faq:
  - q: "Is bufferbloat the same as a slow connection?"
    a: "No. Your speed can be high while latency under load is bad. A bufferbloat test measures the delay when the line is busy."
  - q: "Will a faster plan fix bufferbloat?"
    a: "Sometimes it hides it, but it doesn't fix the cause. The fix is managing the queue on your router."
  - q: "What is QoS?"
    a: "Quality of Service is a router feature that prioritizes some traffic. Smart queue management, often called SQM, goes further by keeping delay low for everything."
  - q: "Does WiFi 7 fix lag?"
    a: "Not by itself. Bufferbloat happens at the connection to your internet provider, so a faster WiFi standard won't remove it."
sources:
  - title: "Bufferbloat test"
    publisher: "Waveform"
    url: "https://www.waveform.com/tools/bufferbloat"
  - title: "Speed test with latency under load"
    publisher: "Cloudflare"
    url: "https://speed.cloudflare.com/"
  - title: "What is bufferbloat?"
    publisher: "Bufferbloat.net"
    url: "https://www.bufferbloat.net/"
---

If your game or video call gets choppy whenever someone uploads a video or a device starts a big update, you may have bufferbloat. It is one of the most common causes of lag on otherwise fast connections, and it can often be fixed with one router setting.

## What is bufferbloat?

Your router sends data to your internet provider through a connection with a fixed speed. When that connection fills up, extra data waits in a queue. If the queue is long, everything behind it waits too, including your game packets. That wait is bufferbloat, and it shows up as latency spikes.

## How do you test for it?

1. Plug a computer into your router with Ethernet so WiFi doesn't affect the result.
2. Close other apps, then run a bufferbloat test such as Waveform's or Cloudflare's speed test.
3. Look at latency under load, not just the download number. A big jump from your idle ping means bufferbloat.

If you're not sure whether your slowdown is WiFi or your plan, see our [slow WiFi test guide]({{< relref "how-to-fix-slow-wifi" >}}).

## How do you fix it?

1. **Find the setting.** Look for Smart Queue, SQM, Adaptive QoS, or similar in your router's app. Names differ by brand, and not every router has one.
2. **Set the speeds a little below your real speeds.** Use 85% to 95% of your tested download and upload speeds. This keeps the queue in your router, where it can be managed.
3. **Run the test again.** Latency under load should be much closer to your idle ping.
4. **Wire what you can.** Consoles and PCs that stay put should use Ethernet.

## Which routers help?

Look for a router that lists smart queue management or SQM, or one that supports third-party firmware such as OpenWrt. When we review routers like the [Asus RT-BE92U]({{< relref "asus-rt-be92u-review" >}}), we check where the QoS controls live and how easy they are to find.

## What if it's your WiFi?

If the wired test is fine but WiFi spikes, the cause is probably distance, interference, or the band your device is using. Try the free fixes in our guide to [why WiFi is slow when your internet is fast]({{< relref "wifi-slow-but-internet-fast" >}}).
