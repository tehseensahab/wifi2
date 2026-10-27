---
title: "Thread Border Router: Do You Need One, and What Has One?"
date: 2026-10-27T05:00:00Z
description: "You need a Thread border router to set up Thread devices in the Google Home app or control them away from home. Many speakers, hubs and routers have one."
authors: ["Tehseen Arbab"]
topics: ["smart-home-iot", "mesh-wifi"]
tags: ["thread", "matter", "thread-border-router", "homepod", "apple-tv", "google-nest", "amazon-echo", "eero", "smart-home"]
summary: "A Thread border router connects a Thread smart-home network to your Wi-Fi and the internet. You need one if you buy Thread devices and want to control them remotely or run automations, and Google's app requires one for setup. You may already own one: Apple lists HomePod and Apple TV models as Thread-enabled home hubs, and Google and Amazon list Nest Hubs, the Nest Wifi Pro, Google TV Streamer, many Echo speakers and many eero routers as border routers."
imageAlt: "A dark gray HomePod mini smart speaker on a wooden table, with a blurred object in the foreground"
imageCredit: "Photo: Michael Soledad / [Unsplash](https://unsplash.com/photos/a-speaker-sitting-on-top-of-a-wooden-table-eqKBsh9qgrQ)"
takeaways:
  - "A Thread border router is the bridge between a Thread network and your Wi-Fi. Google describes it as the bridge a Thread network needs \"to connect to your Wi-Fi network and the internet.\""
  - "You need one for remote control and automations of Thread devices, and Google's Home app needs one to set up a Thread device at all."
  - "You probably don't need to buy one separately. Google and Amazon list Thread border routers among their speakers, displays, streaming boxes and routers, and Apple lists Thread-enabled HomePod and Apple TV hubs."
  - "Apple says Thread-capable iPhones (iPhone 15 Pro and later on iOS 18) can pair Thread accessories, but for automations, notifications and remote control Apple points you to a Thread-enabled home hub or a third-party Thread border router."
  - "Thread 1.4 allows credential sharing, which chipmaker Espressif says is mandatory for 1.4 border routers, so border routers from different brands can join one network instead of starting separate ones. Support is still rolling out."
faq:
  - q: "Is my Wi-Fi router a Thread border router?"
    a: "Usually not, unless it says so. Google lists the Nest Wifi Pro (Wi-Fi 6E) as a Thread border router, and Amazon lists most current eero models. Check your router's spec page for \"Thread border router\"."
  - q: "Can I have more than one Thread border router?"
    a: "Yes. A home can easily have several, such as a HomePod mini and a Nest Hub. Whether they share one Thread network depends on the brands and their software. Thread 1.4's credential sharing is meant to let them join one network, but not every device supports it yet."
  - q: "Does my phone count as a Thread border router?"
    a: "Not according to Apple and Google's support pages. Apple says a Thread-capable iPhone can pair Thread accessories, and Google says an Android phone can join an existing Thread network without a dedicated border router, but neither company describes the phone as a border router."
  - q: "Do Matter devices need a Thread border router?"
    a: "Only Matter devices that use Thread. Matter devices that connect over Wi-Fi or Ethernet don't need one. Check the box or listing: it will say Thread or Wi-Fi."
  - q: "Which Apple TV is a Thread border router?"
    a: "Apple lists these as Thread-enabled home hubs: the Apple TV 4K (3rd generation) Wi-Fi + Ethernet model and the Apple TV 4K (2nd generation). It also lists HomePod (2nd generation) and HomePod mini."
sources:
  - title: "If you see a 'Thread Border Router Required' or 'Needs Thread Network' alert on your iPhone or iPad"
    publisher: "Apple Support"
    url: "https://support.apple.com/102078"
    date: 2026-01-13
  - title: "How Google products use Thread in a smart home"
    publisher: "Google Nest Help"
    url: "https://support.google.com/googlenest/answer/9249088?hl=en"
  - title: "Connect Thread smart home devices with your Android device"
    publisher: "Android Help"
    url: "https://support.google.com/android/answer/16335330?hl=en"
  - title: "Thread support"
    publisher: "Amazon Developer (Alexa+ smart home docs)"
    url: "https://developer.amazon.com/docs/alexaplus/smarthome/thread-support"
    date: 2026-10-22
  - title: "Thread Group Q1 2025 Newsletter"
    publisher: "Thread Group"
    url: "https://threadgroup.org/newsroom/newsletters/q1-2025"
    date: 2025-04-09
  - title: "Thread Credential Sharing"
    publisher: "Espressif Developer Portal"
    url: "https://developer.espressif.com/blog/2026/01/thread-credential-sharing/"
    date: 2026-01-06
  - title: "Apple and Google update streaming devices with Thread 1.4 support"
    publisher: "T3"
    url: "https://www.t3.com/home-living/smart-home/apple-and-google-update-streaming-devices-with-thread-1-4-support-heres-what-it-means-for-your-smart-home"
    date: 2026-06-30
---

You need a Thread border router if you own Thread smart-home devices and want to control them from outside your home, run automations, or set them up in the Google Home app. The border router is the bridge between the low-power Thread network those devices use and your Wi-Fi and the internet. You may not need to buy one: Google and Amazon list Thread border routers among Nest Hub displays, the Nest Wifi Pro, Google TV Streamer, many Echo speakers and many eero routers, and Apple lists HomePod and Apple TV models as Thread-enabled home hubs.

## What a Thread border router does

Thread is a low-power mesh network for small smart-home devices such as sensors, locks, plugs and bulbs. Those devices talk to each other over Thread, not Wi-Fi, so your Wi-Fi devices and the internet can't reach them without a bridge. Google's help page puts it this way: "A Thread network needs a bridge to connect to your Wi-Fi network and the internet." That bridge is the border router.

Google says the border router also lets you control Thread devices from your phone when you're away, and that the Google Home app requires one to set up a Thread device. For background on how Thread fits with Matter, see our [Matter and Thread explainer]({{< relref "/guides/matter-thread-smart-home-explained" >}}).

## Do you need one?

You need one if both of these are true:

1. You've bought, or plan to buy, a device that uses **Thread**. Many Matter devices use Thread, but some use Wi-Fi instead; the box or listing says which.
2. You want remote control, automations or notifications, or you use the Google Home app. Apple says you can "use a compatible third-party Thread border router" or a Thread-enabled Apple home hub for remote control, automations and notifications.

You don't need one for Wi-Fi-only smart devices, or for Matter devices that connect over Wi-Fi or Ethernet. Those talk to your router directly. If a Wi-Fi device won't join, our guide to [smart devices that won't connect]({{< relref "/guides/smart-home-device-wont-connect-2-4-ghz" >}}) covers the usual 2.4 GHz problem.

### What about your phone?

Phones can do part of the job, but they aren't border routers. Apple's support page says you can pair Thread accessories with a Thread-enabled iPhone (iPhone 15 Pro, iPhone 15 Pro Max or later) running iOS 18 or later, but for automations, notifications and remote control it points you to a Thread-enabled home hub or a compatible third-party border router. Google says an Android phone "can join an existing Thread network even if you don't have a dedicated Thread border router at home," and the page doesn't say the phone can act as a border router.

## Which devices are Thread border routers?

These are the devices each company lists on its own support or developer pages, checked October 27, 2026. Older or similarly named models aren't included unless they're named.

| Ecosystem | Devices listed as Thread border routers or Thread-enabled hubs |
|---|---|
| Apple | Apple TV 4K (3rd generation) Wi-Fi + Ethernet; Apple TV 4K (2nd generation); HomePod (2nd generation); HomePod mini |
| Google | Google Home Speaker (2026); Nest Hub (2nd gen); Nest Hub Max; Nest Wifi Pro (Wi-Fi 6E); Google TV Streamer (4K) |
| Amazon Echo | Echo (4th Gen); Echo Dot Max (2025 release); Echo Hub; Echo Plus (2nd Gen); Echo Show 21; Echo Show 15 (2nd Gen); Echo Show 11 (2025 release); Echo Show 10 (3rd Gen); Echo Show 8 (3rd Gen, 2025 release); Echo Studio (1st Gen and newer, 2025 release) |
| Amazon eero | eero 6 and eero 6+; eero 7; eero Beacon; eero Max 7; eero Outdoor 7; eero PoE 6; eero PoE gateway; eero Pro; eero Pro 6E and eero Pro 6; eero Pro 7 |

Apple's list is titled as Thread-enabled Apple devices rather than border routers, and it also includes the iPhone 15 Pro and later, which Apple describes only as able to pair accessories. A few more details matter when you're checking your own devices:

- **Apple TV:** Apple lists only the Wi-Fi + Ethernet version of the 3rd-generation Apple TV 4K, plus the 2nd generation. If yours isn't one of those, it isn't on Apple's list.
- **Amazon's Thread versions:** Amazon says its devices "support Thread version 1.1 or 1.3," with only the Echo (4th Gen) listed under 1.1. Its page was last modified on October 22, 2026.
- **Google's credentials:** Google says Thread credentials are "typically generated and shared automatically," and that on Android they sync to your Google Account by default.

If you're replacing an older Google mesh system and want to keep a border router in the house, our [Nest Wifi replacement guide]({{< relref "/guides/google-nest-wifi-replacement" >}}) covers the options.

## Mixing brands: one Thread network or several?

Homes can end up with border routers from more than one company, such as a HomePod mini and an Echo. That can leave you with separate Thread networks instead of one shared mesh. Espressif, which makes chips used in Thread devices, describes Thread 1.4's credential sharing as a way of "avoiding network fragmentation," so new devices and border routers join an existing network instead of starting another.

The Thread Group says Thread 1.4, released in September 2024, "allows device manufacturers to implement features like credential sharing." Espressif's January 2026 post says "Credentials Sharing is a mandatory feature for Thread 1.4 Border Routers" and says Samsung SmartThings supports it. Support from the bigger ecosystems is still arriving: T3 reported on June 30, 2026, that Thread 1.4 "first arrived on compatible Apple TV models through the tvOS 27 developer beta" and that the Google TV Streamer got it in a separate update. Neither Apple's nor Google's support pages cited here mention Thread 1.4, so treat cross-brand sharing as a work in progress.

The practical advice: if you're starting out, keep your Thread devices in one ecosystem's app where you can, and add border routers from that same ecosystem.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Apple's Thread-enabled devices; Thread iPhones pair accessories on iOS 18; home hub or third-party border router needed for automations and remote control | [Apple Support, Jan. 13, 2026](https://support.apple.com/102078) | Qualified (Apple labels the list "Thread-enabled," not "border routers") |
| Border router definition; Google border-router list; Google Home app requires one; credentials shared automatically | [Google Nest Help](https://support.google.com/googlenest/answer/9249088?hl=en) | Verified |
| Android phones can join an existing Thread network without a border router | [Android Help](https://support.google.com/android/answer/16335330?hl=en) | Verified |
| Echo and eero border-router list; Thread 1.1 and 1.3 versions | [Amazon Developer, modified Oct. 22, 2026](https://developer.amazon.com/docs/alexaplus/smarthome/thread-support) | Verified |
| Thread 1.4 released September 2024 with credential sharing | [Thread Group, Apr. 9, 2025](https://threadgroup.org/newsroom/newsletters/q1-2025) | Verified |
| Credential sharing mandatory for Thread 1.4 border routers; SmartThings supports it | [Espressif, Jan. 6, 2026](https://developer.espressif.com/blog/2026/01/thread-credential-sharing/) | Qualified (chipmaker's description) |
| Thread 1.4 in tvOS 27 developer beta and on Google TV Streamer | [T3, June 30, 2026](https://www.t3.com/home-living/smart-home/apple-and-google-update-streaming-devices-with-thread-1-4-support-heres-what-it-means-for-your-smart-home) | Qualified (press report) |
