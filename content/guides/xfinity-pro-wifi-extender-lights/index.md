---
title: "Xfinity Pro WiFi Extender Lights: What They Mean"
date: 2026-11-14T05:05:00Z
description: "Xfinity Pro WiFi Extender lights: off is normal, blinking white means activating or needs attention, solid white means backup is on, solid red is an LTE error."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "internet-plans-isps"]
tags: ["xfinity", "comcast", "xfinity-pro", "pro-wifi-extender", "led-lights", "lte-backup", "battery-backup", "troubleshooting"]
summary: "On the Xfinity Pro WiFi Extender, no light is the normal state. Blinking white means it's activating or, after setup, needs attention; solid white means it's on 4G LTE backup or running on Battery Backup power; solid red means an LTE error or no LTE connection. A solid red light on the Battery Backup means the battery has failed or is nearly empty. Xfinity's troubleshooting page starts with the Xfinity app's Troubleshoot Device tool."
imageAlt: "Person in a dark sweater holding a smartphone with both hands in a bright room, with a desk and monitor in the background"
imageCredit: "Photo: Jonas Leupe / [Unsplash](https://unsplash.com/photos/person-holding-black-android-smartphone-wK-elt11pF0)"
takeaways:
  - "Light off on the Pro WiFi Extender is normal when your Xfinity Gateway shows solid white and the Battery Backup light is off (solid red on the battery means a battery failure). Xfinity's chart also shows the extender off when both it and the Battery Backup have lost power."
  - "Blinking white means the extender is activating; if it keeps blinking after activation, Xfinity's chart labels that 'needs attention.'"
  - "Solid white means the extender is in backup mode: on LTE during a network outage (gateway blinking amber), or running on battery during a power outage (gateway off)."
  - "Solid red on the extender means an LTE error or no LTE connection. Xfinity's fix for poor cellular signal is to move the extender to an elevated spot near a window."
  - "Start any fix in the Xfinity app: WiFi tab > View WiFi equipment > Pro WiFi Extender > Troubleshoot Device."
faq:
  - q: "Why is there no light on my Xfinity Pro WiFi Extender?"
    a: "If your Xfinity Gateway shows solid white and the Battery Backup light (if you have one) is off, no light is normal. A solid red Battery Backup light with the extender off means a battery failure. Xfinity's chart lists the extender as off during normal operation. If the gateway is also off, there's a power outage and the extender has no battery power."
  - q: "What does a red light on the Xfinity Pro WiFi Extender mean?"
    a: "Xfinity's chart lists solid red on the extender as 'LTE error/no connection.' Its troubleshooting page says to move the extender to an elevated position near a window if cellular signal is poor, then run the app's troubleshooter again."
  - q: "Why is my Xfinity Pro WiFi Extender blinking white?"
    a: "It's either activating or, if activation already finished, needs attention. Run the Xfinity app's Troubleshoot Device tool, and also check Xfinity's setup requirements: the gateway can't be in Bridge Mode, and first-generation Xfinity WiFi Extenders must be removed."
  - q: "What does a red light on the Battery Backup mean?"
    a: "With the extender off and the gateway solid white, it means a Battery Backup failure. During a power outage, with the extender solid white, it means the battery is nearly discharged."
  - q: "How do I reset the Xfinity Pro WiFi Extender?"
    a: "Xfinity says you can reboot the Pro WiFi Extender by holding its reset button for 15 seconds. If the Battery Backup blinks for more than 30 minutes, Xfinity says to press and hold the reset button for 10 or more seconds; its page doesn't say which device's button."
sources:
  - title: "Learn what the lights on the Xfinity Pro WiFi Extender mean"
    publisher: "Xfinity"
    url: "https://www.xfinity.com/support/articles/storm-ready-lights"
    date: 2026-10-19
  - title: "Xfinity Pro WiFi Extender troubleshooting"
    publisher: "Xfinity"
    url: "https://www.xfinity.com/support/articles/storm-ready-troubleshooting"
    date: 2026-10-19
  - title: "Activate or remove Xfinity Pro WiFi Extender using the Xfinity app"
    publisher: "Xfinity"
    url: "https://www.xfinity.com/support/articles/install-storm-ready"
    date: 2026-10-19
  - title: "Xfinity Pro WiFi Extender FAQs"
    publisher: "Xfinity"
    url: "https://www.xfinity.com/support/articles/storm-ready-faqs"
    date: 2026-11-10
---

**On the Xfinity Pro WiFi Extender, no light is the normal state, blinking white means it's activating or needs attention, solid white means it's in backup mode during an outage, and solid red means it has an LTE error or no LTE connection.** The extender's light only makes sense next to your Xfinity Gateway's light (and the Battery Backup's, if you have one), so the table below shows all three, as Xfinity lists them on its [lights support page](https://www.xfinity.com/support/articles/storm-ready-lights), last updated October 19, 2026.

This guide is based on Xfinity's support pages for the Pro WiFi Extender, which is included with Xfinity Pro. We haven't tested the device ourselves. For what Xfinity Pro costs and whether it's worth it, see our [Xfinity Storm-Ready WiFi guide](/guides/xfinity-storm-ready-wifi/).

## Xfinity Pro WiFi Extender light chart

| What's happening | Pro WiFi Extender | Xfinity Gateway | Battery Backup |
|---|---|---|---|
| Activation | Blinking white | Solid white | Blinking white |
| After activation: needs attention | Blinking white | Solid white | Off |
| Normal operation | Off | Solid white | Off |
| Battery Backup failure | Off | Solid white | Solid red |
| LTE error or no LTE connection | Solid red | Solid white | Off |
| Network outage (on LTE backup) | Solid white | Blinking amber | Off |
| Power outage, running on battery | Solid white | Off | Solid white |
| Power outage, battery nearly empty | Solid white | Off | Solid red |
| Power outage, extender and battery offline | Off | Off | Off |

Source: [Xfinity](https://www.xfinity.com/support/articles/storm-ready-lights). If you don't have the optional Battery Backup, ignore that column.

Xfinity's lights page doesn't say what to do for each light. The fixes below come from its [troubleshooting page](https://www.xfinity.com/support/articles/storm-ready-troubleshooting) and setup page, matched to the lights.

## Light off

If the gateway shows solid white and the extender is dark, nothing is wrong: Xfinity lists the extender light as off in normal operation.

If the gateway is off too, you have a power outage. With a working Battery Backup, the extender would show solid white. All three lights off means the extender and battery are both offline. Xfinity says a fully charged Battery Backup "can keep the extender powered for up to four hours during a power outage." Xfinity describes power-outage backup only with that optional battery; our [power outage guide](/guides/internet-power-outage/) covers other ways to stay online.

## Blinking white

**During setup**, blinking white on the extender and Battery Backup with a solid white gateway is the activation pattern. Xfinity activates the extender in the Xfinity app: sign in with the primary or manager Xfinity ID, then go to **Services > Activate More Devices > Pro WiFi Extender > Get Started**.

**After setup**, a blinking white extender with the Battery Backup off is what Xfinity's chart labels "needs attention." Xfinity's lights page doesn't say what triggers it. Start with the app's troubleshooter, then check the setup requirements on Xfinity's [activation page](https://www.xfinity.com/support/articles/install-storm-ready):

- "Make sure your Xfinity Gateway is not in Bridge Mode."
- "Remove any 1st Generation Xfinity WiFi Extenders from your network."
- If your Wi-Fi network has no password, Xfinity says to change its security mode from open to protected.

Xfinity's FAQ adds that the extender "works with Xfinity Gateways XB8, XB9, and XB10 devices" and "is not compatible with home networks that have more than one active Xfinity WiFi Gateway or modem." Our [XB10 vs. XB8 guide](/guides/xfinity-xb10-vs-xb8/) explains how to tell which gateway you have.

## Solid white

Solid white on the extender means it's in backup mode:

- **Gateway blinking amber:** Xfinity's network is down, and the extender "automatically switches to a 4G LTE cellular connection to help keep your home online," according to Xfinity's [FAQ](https://www.xfinity.com/support/articles/storm-ready-faqs).
- **Gateway off, Battery Backup solid white:** the power is out and the battery is powering the extender; backup internet then depends on LTE coverage.
- **Gateway off, Battery Backup solid red:** the power is out and the battery is nearly discharged.

Xfinity's FAQ says LTE backup is available "in areas with supported cellular coverage."

## Solid red on the extender

Xfinity lists this as "LTE error/no connection": the extender can't use its cellular backup. In this state Xfinity's chart shows the gateway solid white, as in normal operation, so the problem is with the backup link, not necessarily your main connection.

Xfinity's fix for weak cellular signal: "move your Pro WiFi Extender close to an elevated position near a window," then run the troubleshooter again.

## Solid red on the Battery Backup

- **Extender off, gateway solid white:** Xfinity's chart calls this a Battery Backup failure.
- **During a power outage:** the battery is nearly empty.

Xfinity's troubleshooting page also covers two battery problems: if the battery is "not 100% charged 24 hours after activation," check that the wiring is correct. If the Battery Backup is "blinking for more than 30 minutes, press and hold the reset button" for 10 or more seconds (Xfinity doesn't specify which device's button). When you remove the battery, Xfinity says its cord plugs into "the round red port on the back of the Extender."

## How to fix most Pro WiFi Extender problems

1. **Run the app's troubleshooter.** Xfinity says to "open the Xfinity app and go to WiFi tab > View WiFi equipment > Pro WiFi Extender > Troubleshoot Device."
2. **Fix placement.** Xfinity's guidance pulls in two directions, so aim for a spot that works for both Wi-Fi and cellular signal:
   - "Place the device near a window to ensure a strong cellular signal" and "at least one room away from the gateway to avoid interference."
   - For Wi-Fi coverage, "place it in a room that is roughly halfway between your gateway and an area without coverage."
   - If Wi-Fi signal is low, "move the Pro WiFi Extender closer to the Xfinity Gateway."
   Our [extender placement guide](/guides/wifi-extender-placement-guide/) explains the trade-off in more detail.
3. **Reboot it.** Xfinity says that "if necessary, reboot the Pro WiFi Extender by holding the reset button for 15 seconds."
4. **Contact Xfinity.** "If you experience other issues with your Pro WiFi Extender, please contact us for help." Xfinity says the extender "is included with Xfinity Pro."

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Light chart for extender, gateway and Battery Backup in nine situations | [Xfinity lights page](https://www.xfinity.com/support/articles/storm-ready-lights) (updated Oct. 19, 2026) | Verified |
| Troubleshoot Device path; placement advice; battery charge, blinking and reset steps; 15-second reboot | [Xfinity troubleshooting page](https://www.xfinity.com/support/articles/storm-ready-troubleshooting) (updated Oct. 19, 2026) | Verified |
| Activation steps; no Bridge Mode; remove first-generation extenders; open network must be protected | [Xfinity activation page](https://www.xfinity.com/support/articles/install-storm-ready) (updated Oct. 19, 2026) | Verified |
| Works with XB8, XB9, XB10; not with more than one active gateway or modem; LTE switchover; four-hour battery; LTE coverage limits | [Xfinity FAQ](https://www.xfinity.com/support/articles/storm-ready-faqs) (updated Nov. 10, 2026) | Verified |
