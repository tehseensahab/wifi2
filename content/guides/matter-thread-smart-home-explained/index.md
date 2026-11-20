---
title: "Matter vs. Thread: What's the Difference for Your Smart Home?"
date: 2026-09-28
lastmod: 2026-11-20
description: "Matter is the common language smart devices speak; Thread is a low-power mesh network some of them use. What each needs, and what to set on your router."
authors: ["Tehseen Arbab"]
topics: ["smart-home-iot", "wifi-6e-7"]
tags: ["matter", "thread", "smart-home", "thread-border-router", "ipv6", "google-home", "multi-admin"]
summary: "Matter is a smart-home standard that lets devices from different brands work with Google Home, Apple Home, Alexa and other platforms. Thread is a low-power mesh network that many battery-powered Matter devices use to connect. Matter devices can also run over Wi-Fi or Ethernet. You need a Matter hub for each platform you use, plus a Thread border router if any of your devices use Thread, and Google says your router must have IPv6 turned on."
imageAlt: "Google smart speaker next to a smart lock and bridge on a shelf"
imageCredit: "Photo: Sebastian Scholz (Nuki) / [Unsplash](https://unsplash.com/photos/Fh3Dtg6QX4Q)"
takeaways:
  - "Matter and Thread do different jobs. Matter is the common language devices and apps use; Thread is one of the networks that carries it, alongside Wi-Fi and Ethernet. Bluetooth Low Energy is used to set devices up."
  - "Thread is an IPv6-based, low-power mesh built on IEEE 802.15.4. Devices pass traffic for each other, and the network has no single point of failure."
  - "Matter devices on Thread need a Thread border router to reach your Wi-Fi network. Many smart speakers, displays, streamers and some routers include one."
  - "Google's Matter requirements include IPv6 turned on in your home Wi-Fi router and a Matter hub for Google Home; at home, commands go to devices locally over Wi-Fi or Thread without the cloud."
faq:
  - q: "What is the difference between Matter and Thread?"
    a: "Matter is an application standard: the shared language that lets a device work with Google Home, Apple Home, Alexa and others. Thread is a low-power wireless mesh network that carries Matter traffic for devices like sensors and locks. Matter can also run over Wi-Fi and Ethernet, so not every Matter device uses Thread."
  - q: "Do I need Thread to use Matter?"
    a: "No. Matter runs over Wi-Fi, Ethernet and Thread. You only need Thread, and a Thread border router, if a device you buy uses Thread."
  - q: "Do I need a new Wi-Fi router for Matter?"
    a: "Usually not. Google's requirements are a Matter-enabled hub and IPv6 turned on in your home router. A router with a built-in Thread border router, such as the Nest Wifi Pro or many eero models, can save you a separate hub for Thread devices."
  - q: "Do Matter devices work if the internet is down?"
    a: "Control from inside your home can. Google says commands from its hub go to Matter devices locally over your Wi-Fi or Thread network without connecting to the cloud. Control from away needs your hub and an internet connection, and some features may still rely on the maker's cloud."
  - q: "Can I use Matter devices with Apple Home and Google Home at the same time?"
    a: "Yes. Matter's multi-admin feature lets several platforms control the same device. Google says you need one Matter hub for each Matter-certified app you want to control the device from."
sources:
  - title: "The Connectivity Standards Alliance Unveils Matter, Formerly Known as Project CHIP"
    publisher: "Connectivity Standards Alliance"
    url: "https://csa-iot.org/newsroom/chip-is-now-matter/"
    date: 2021-05-11
  - title: "Matter FAQ"
    publisher: "Connectivity Standards Alliance"
    url: "https://csa-iot.org/all-solutions/matter/matter-faq/"
  - title: "Matter 1.4 Enables More Capable Smart Homes"
    publisher: "Connectivity Standards Alliance"
    url: "https://csa-iot.org/newsroom/matter-1-4-enables-more-capable-smart-homes/"
  - title: "Matter's latest version will try to smooth out the smart home platform's rough edges"
    publisher: "Engadget"
    url: "https://www.engadget.com/home/smart-home/matters-latest-version-will-try-to-smooth-out-the-smart-home-platforms-rough-edges-130003372.html"
  - title: "Advancing Secure, Reliable Connectivity for IoT Devices"
    publisher: "Thread Group"
    url: "https://threadgroup.org/"
  - title: "What is Thread?"
    publisher: "OpenThread (Google)"
    url: "https://openthread.io/guides/thread-primer"
  - title: "Prepare your smart home for Matter"
    publisher: "Google Nest Help"
    url: "https://support.google.com/googlenest/answer/12391458?hl=en"
  - title: "Set up, manage, and control Matter-enabled devices with Google Home"
    publisher: "Google Home Help"
    url: "https://support.google.com/googlehome/answer/13127223?hl=en"
  - title: "Connectivity on Android (Home APIs)"
    publisher: "Google Home Developers"
    url: "https://developers.home.google.com/apis/android/connectivity"
---

Matter and Thread solve different problems. Matter is a smart-home standard, a common language that lets a plug, lock or sensor from one brand work with Google Home, Apple Home, Alexa and other platforms. Thread is a low-power wireless mesh network that many battery-powered devices use to send that language around your home. Matter devices can also connect over Wi-Fi or Ethernet, so a Matter device doesn't always use Thread. What you need at home is a Matter hub for your platform, a Thread border router if any devices use Thread, and IPv6 turned on in your router.

This is an explainer built from Connectivity Standards Alliance, Thread Group and Google documentation. We have not tested Matter or Thread devices ourselves.

## What is the difference between Matter and Thread?

| | Matter | Thread |
|---|---|---|
| What it is | Smart-home application standard: how devices and apps talk to each other | Low-power wireless mesh network that carries data between devices |
| Who runs it | Connectivity Standards Alliance (CSA) | Thread Group |
| Runs over | Wi-Fi, Ethernet and Thread; Bluetooth Low Energy for setup | IEEE 802.15.4 radios, using IPv6 |
| Typical devices | Most kinds of smart-home device, mains-powered or battery-powered | Low-power and battery-powered devices |
| What you need | A Matter hub for each platform you use | A Thread border router to link Thread to your Wi-Fi network |
| Works with | Google Home, Apple Home, Amazon Alexa, SmartThings and other Matter platforms | Whichever app controls the device, often through Matter |

When the CSA announced Matter in May 2021, it said the standard would run on Ethernet (802.3), Wi-Fi (802.11) and Thread (802.15.4), with Bluetooth Low Energy for commissioning, the setup step that adds a device to your network. Its Matter FAQ says that because Matter runs over existing technologies, many existing products can gain Matter support through software updates.

## What is Thread, and why do smart devices use it?

Thread is a mesh network for small, low-power devices. The Thread Group describes it as a secure, low-power mesh designed to support large numbers of devices with no single point of failure. Google's OpenThread primer, written for developers, says Thread is IPv6-based, runs on IEEE 802.15.4 mesh networks, encrypts all communications, and lets low-power devices sleep and run on battery power for years.

Google's Matter help page lists the practical benefits it sees for Thread devices: they communicate faster than devices that use Wi-Fi, battery-powered Thread devices last longer than battery-powered Wi-Fi ones, and the mesh can reroute around a device that goes offline. Those are Google's claims; we haven't measured them.

Thread is a separate network from your Wi-Fi. It needs a **Thread border router** to connect it to your home network and the internet. Our guide to [Thread border routers](/guides/thread-border-router/) lists which Apple, Google, Amazon and eero devices have one.

## What do I need to use Matter?

Using Google Home as the example, Google lists these requirements:

1. **A Matter-enabled hub for Google Home,** such as a Nest speaker or display. Some hubs, including the Nest Hub (2nd gen), Nest Hub Max, Nest Wifi Pro and Google TV Streamer, also work as Thread border routers.
2. **IPv6 turned on in your home Wi-Fi router.** Google says IPv6 on the Wi-Fi network lets Matter devices on Thread and Wi-Fi communicate. Our guide to [whether you should enable IPv6](/guides/should-you-enable-ipv6/) shows how to check.
3. **A phone with Bluetooth Low Energy 4.2 or later,** used to add the device to your network.
4. **A Matter-certified device.** Google says to look for the Matter logo on the package.

Apple Home and Amazon Alexa have their own hub devices. Google notes you need one Matter hub for each Matter-certified app you want to control a device from.

## Does Matter work without the internet?

At home, largely yes. Google says that when you're home, its hub sends commands directly to Matter devices over your Wi-Fi or Thread network without connecting to the cloud. Controlling devices while you're away still needs the hub and an internet connection, and some features depend on the device maker's own service, so check each product.

## Can several apps control the same Matter device?

Yes. That's Matter's multi-admin feature. Google says it lets different platforms control the same devices, so one person can use Apple Home and another Google Home for the same lights. The CSA says Matter 1.4 added Enhanced Multi-Admin to improve that experience. Matter 1.4 also introduced certification for home routers and access points that combine a Wi-Fi access point with a Thread border router.

## How should I set up my router for Matter?

- **Turn on IPv6** if it's off, as Google requires.
- **Keep the hub and Matter devices on the same network.** Google's developer documentation defines local control as a controller on the same Wi-Fi network as the device. Moving Matter devices to a guest network can cut off local control; our [guest network guide](/guides/guest-wifi-network-smart-home-devices/) explains which devices are safe to move.
- **Check the band for Wi-Fi devices.** Many smart devices only work on 2.4 GHz; our guide to [smart devices that won't connect on 2.4 GHz](/guides/smart-home-device-wont-connect-2-4-ghz/) covers setup by router brand.
- **Fix coverage, not just settings.** Wi-Fi Matter devices drop off in weak rooms like any other device; see [Wi-Fi router vs. mesh](/guides/wifi-router-vs-mesh/) and our [router hardening checklist](/guides/router-hardening-checklist/) for the security side.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Matter runs on Ethernet, Wi-Fi and Thread, with Bluetooth LE for commissioning | [CSA, May 11, 2021](https://csa-iot.org/newsroom/chip-is-now-matter/) | Verified |
| Many existing products can be updated to Matter via software because it runs over existing technologies | [CSA Matter FAQ](https://csa-iot.org/all-solutions/matter/matter-faq/) | Verified |
| Matter 1.4 adds Enhanced Multi-Admin and certification for routers/access points combining Wi-Fi and a Thread border router | [CSA Matter 1.4](https://csa-iot.org/newsroom/matter-1-4-enables-more-capable-smart-homes/), [Engadget](https://www.engadget.com/home/smart-home/matters-latest-version-will-try-to-smooth-out-the-smart-home-platforms-rough-edges-130003372.html) quoting the CSA | Verified |
| Thread: secure, low-power mesh with no single point of failure, built for many devices | [Thread Group](https://threadgroup.org/) | Verified |
| Thread: IPv6-based, IEEE 802.15.4 mesh; all communications encrypted; low-power devices can run on battery for years | [OpenThread primer](https://openthread.io/guides/thread-primer) | Verified |
| Google's stated Thread benefits: faster than Wi-Fi devices, longer battery life, mesh rerouting | [Google Nest Help](https://support.google.com/googlenest/answer/12391458?hl=en) | Qualified: manufacturer's claims, not independently measured |
| Google hubs with Thread: Nest Hub (2nd gen), Nest Hub Max, Nest Wifi Pro, Google TV Streamer; IPv6 bridges Thread and Wi-Fi Matter devices | [Google Nest Help](https://support.google.com/googlenest/answer/12391458?hl=en) | Verified |
| Requirements: IPv6 on the home router, Matter hub, phone with BLE 4.2+, Matter logo; local commands without the cloud; one hub per Matter app; multi-admin | [Google Home Help](https://support.google.com/googlehome/answer/13127223?hl=en) | Verified |
| Local control means a controller on the same Wi-Fi network as the device | [Google Home Developers](https://developers.home.google.com/apis/android/connectivity) | Verified |

## Bottom line

Matter decides whether a device will work with your app; Thread is one way that device connects. Check the box for the Matter logo, check whether the device uses Wi-Fi or Thread, and make sure you have a hub for your platform, a Thread border router if needed, and IPv6 turned on in your router.
