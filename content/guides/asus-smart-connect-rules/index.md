---
title: "ASUS Smart Connect Rules Explained: What Each Setting Does"
date: 2026-11-19T05:00:00Z
description: "ASUS Smart Connect rules: leave the defaults unless one device keeps switching bands. What the steering trigger, STA selection and bounce detect settings do."
authors: ["Tehseen Arbab"]
topics: ["routers", "how-to-fixes"]
tags: ["asus", "smart-connect", "band-steering", "wifi-bands", "asuswrt"]
summary: "Leave ASUS Smart Connect rules at their defaults unless a specific device keeps bouncing between bands or won't connect; ASUS itself recommends the default settings when there are no special requirements. The rules decide when the router steers a device (Steering Trigger Condition), which devices it moves (STA Selection Policy), where they go (Interface Select and Qualify Procedures) and how often a device can be moved (Bounce Detect)."
imageAlt: "A hand holding a smartphone with a blank, glowing screen in a dark room lit in teal and orange"
imageCredit: "Photo: Jakub Żerdzicki / [Unsplash](https://unsplash.com/photos/a-person-holding-a-cell-phone-in-their-hand-nKGlH6_PDxk)"
takeaways:
  - "ASUS says that if there are no special requirements, it is recommended to use the default Smart Connect settings, and the Smart Connect Rule page has a Default button to restore them."
  - "The four rule groups work as filters and a destination: Steering Trigger Condition and STA Selection Policy decide when and which device is steered, Interface Select and Qualify Procedures picks the target band, and Bounce Detect limits how often a device can be moved."
  - "Smart Connect Rules are only in the router's web interface, not the ASUS Router app, and some models don't offer them at all."
  - "ASUS warns that a phone's own Wi-Fi band preference can make the Smart Connect rules ineffective."
  - "If a device won't connect, check the VHT setting: ASUS says an 802.11n-only device can't connect if VHT is set to AC only."
faq:
  - q: "Should I change the ASUS Smart Connect rules?"
    a: "Usually not. ASUS says that if there are no special requirements, it is recommended to use the default settings. Change them only to fix a specific problem, such as a device that keeps switching bands, and note the original values first. The Default button on the Smart Connect Rule page restores them."
  - q: "What does Bounce Detect do on an ASUS router?"
    a: "It limits how often the router can move one device between bands. ASUS's example: if a device is steered twice within 60 seconds, it stays on its current band for 180 seconds. The settings are Window Time, Counts and Dwell Time."
  - q: "Where are the Smart Connect Rules on an ASUS router?"
    a: "ASUS says to open the Smart Connect Rule page in Network Tools, or click the Smart Connect Rule link on the Wireless > General page. Its guide describes that page only for firmware earlier than 3.0.0.6.102_35404 and does not say where it is in the newer interface. The rules are only in the web interface, not the app."
  - q: "Why is ASUS Smart Connect not moving my phone to 5 GHz?"
    a: "ASUS says a mobile device's built-in Wi-Fi network preferences may render the Smart Connect rules ineffective."
  - q: "Is ASUS Smart Connect the same as band steering?"
    a: "Yes. ASUS describes Smart Connect as steering clients between the router's bands, and the rule page itself refers to band steering being triggered."
sources:
  - title: "[Wireless Router] How to configure the Smart Connect in ASUS Router?"
    publisher: "ASUS Support (FAQ 1012132)"
    url: "https://asus.com/support/FAQ/1012132"
    date: 2024-12-09
  - title: "RT-AC5300 User Manual (E15858, Revised Edition V3, August 2019), section 4.9 Smart Connect"
    publisher: "ASUS"
    url: "https://dlcdnets.asus.com/pub/ASUS/wireless/RT-AC5300/E15858_RT-AC5300_UM_v3_WEB.pdf"
  - title: "[Wireless Router] How to improve compatibility of IoT device with ASUS WiFi 6 (802.11ax) router?"
    publisher: "ASUS Support (FAQ 1042475)"
    url: "https://www.asus.com/support/faq/1042475/"
    date: 2024-07-22
---

Leave your ASUS router's Smart Connect rules at their defaults unless one specific device keeps bouncing between bands or won't connect. ASUS's own guidance is that "if there are no special requirements, it is recommended to use the default settings," and the rule page has a Default button if you need to undo changes. The rules control when the router steers a device to another band, which devices it moves, where it sends them and how often one device can be moved.

This guide explains each rule group in plain words, using ASUS's support article and the Smart Connect section of an ASUS router manual. It is research-based: we have not tested these settings on our own hardware, and we don't recommend specific threshold numbers, because ASUS's guide doesn't recommend any. For the bigger question of whether to use one network name at all, see our guide to [band steering, on or off](/guides/what-is-band-steering/).

## What is an ASUS Smart Connect rule?

Smart Connect is ASUS's name for band steering: the router puts its bands under one network name and moves devices between them. In the manual for its tri-band RT-AC5300, ASUS says "Smart Connect is designed to automatically steer clients to one of three radios." The Smart Connect Rule page lets you change the conditions behind those moves. ASUS says the router "comes with a default trigger condition setting" and that "depending on your networking environment, you may need to customize the trigger condition."

Two limits apply before you start:

- **Not every model has it.** ASUS says "some models do not support the advanced settings of Smart Connect," and if you don't see Smart Connect Rules after turning Smart Connect on, your model doesn't support them.
- **Web interface only.** ASUS says the ASUS Router app does not support the advanced Smart Connect settings; they are "only available in Web GUI."

## What does each Smart Connect rule setting do?

ASUS sums up the page this way: items (1) and (2) "represent the filter conditions," item (3) "specifies the band to switch to when those conditions are met," and item (4) "aims to minimize" switching between bands. The table below puts each group in plain words. Field names are as ASUS's RT-AC5300 manual lists them; the fields on your model can differ.

| Rule group | Settings inside it (RT-AC5300 manual) | What it does, in plain words |
|---|---|---|
| (1) Steering Trigger Condition | Bandwidth Utilization, Enable Load Balance, RSSI, PHY Rate Less / PHY Rate Greater, VHT | The test for whether steering should start at all, based on how busy a band is, how strong a device's signal is or how fast its link is |
| (2) STA Selection Policy | Not detailed in our sources; ASUS's FAQ applies its VHT options to items 1 to 3 | Once steering is triggered, picks which connected device ("STA", or station) gets moved |
| (3) Interface Select and Qualify Procedures | Target Band (first and second choice) | Where the chosen device is sent |
| (4) Bounce Detect | Window Time, Counts, Dwell Time | How often one device may be moved before the router leaves it alone |

### Steering Trigger Condition

ASUS's support article defines it as "the condition to check if steering needs to be triggered or not." The RT-AC5300 manual explains the individual fields:

- **Bandwidth Utilization:** "When bandwidth use exceeds this percentage, steering will be initiated."
- **Enable Load Balance:** turns load balancing on or off. The manual says Broadcom's documentation "does not indicate how balancing is done."
- **RSSI:** a signal-strength test. "If the received signal level of any associated client meets this criteria, steering will be triggered."
- **PHY Rate Less / PHY Rate Greater:** "These controls determine STA link rates that trigger band steering." The PHY rate is the link rate between the device and the router, not your internet speed.
- **VHT:** decides how 802.11ac and older devices are treated. The options are All, AC only and Not-allowed (non-AC devices only).

### STA Selection Policy

ASUS's article says that once band steering is triggered, the router follows the STA Selection Policy "to pick up client/STA steered to the most appropriate band." In short, the trigger condition decides whether to steer, and this policy decides which device to steer.

### Interface Select and Qualify Procedures

This is the destination. ASUS says "once a trigger condition is reached, the client device steers to the target band," and the manual says "the Target Band controls specify first and second choice of steering targets."

### Bounce Detect

This is the setting most worth understanding if a device keeps bouncing between bands. The manual says "each client can be steered N Counts within the Window Time," and "when the Count limit is hit, the client will not be steered again for Dwell Time." ASUS's support article gives an example: "if the device is steered twice with 60 seconds, the device will remain connected in the current band for 180 seconds."

## When should you change the Smart Connect rules?

Only when there is a specific, repeatable problem. These are the cases ASUS's own documents point to:

| Symptom | What ASUS's documents point to | Try this first |
|---|---|---|
| An older or 802.11n-only device can't connect | ASUS: if a device "only supports 802.11n, but selects AC only in VHT, the device will not be able to connect" | Set VHT back to All, or press Default |
| A phone ignores steering and stays on one band | ASUS: a mobile device's built-in Wi-Fi preferences "may render the smart connect rule ineffective" | Check the phone's own Wi-Fi settings before changing router rules |
| A device keeps switching bands | Bounce Detect exists "to prevent possible client/STA bounce back issues" | Restore defaults first; our suggestion: then change one Bounce Detect value at a time |
| A smart-home device won't join | ASUS's IoT guide for its Wi-Fi 6 routers says to turn off Smart Connect and pick the band for the device | Split the bands instead of tuning rules (see below) |

If drops continue with default rules, the cause may not be steering at all. Our guide to [why Wi-Fi keeps disconnecting](/guides/wifi-keeps-disconnecting/) covers the other usual suspects.

## How do I open the Smart Connect Rule page?

ASUS's guide splits routers into two web interfaces by firmware version. ASUS says "Interface 1" applies to firmware 3.0.0.6.102_35404 and later, and "Interface 2" to firmware earlier than that.

ASUS's guide gives the Smart Connect Rule location without tying it to a firmware version; because it doesn't describe a rule page for the newer interface, these steps apply to firmware earlier than 3.0.0.6.102_35404 (Interface 2):

1. Sign in to the router's web interface from a browser (the rules are not in the app).
2. Go to **Wireless > General** and make sure **Enable Smart Connect** is on. (On ExpertWiFi models: **Settings > Wireless > General**.)
3. Open the **Smart Connect Rule** page in **Network Tools**, or click the **Smart Connect Rule** link on the Wireless General page.
4. Make your change and click **Apply** (ASUS's step). Our suggestion: change one setting at a time.

On firmware 3.0.0.6.102_35404 and later (Interface 1), ASUS's guide only describes turning Smart Connect on or off under **Network > Main network profile**; it does not show where the Smart Connect Rule page is in that interface. If you can't find it, your model may not support the advanced settings.

## How do I restore the default Smart Connect rules?

ASUS's answer: "Click [Default] button in Smart Connect Rule page to restore the settings." Do this before any other troubleshooting if you, or a previous owner, have changed the rules and you don't know the original values.

## When should you stop tuning and split the bands?

If the problem is one device that needs one band, splitting the network is simpler than editing steering rules. For smart-home gear, ASUS's IoT compatibility guide for its Wi-Fi 6 routers says to "turn off [Enable Smart Connect] and select the [Band] for your network devices." On the newer interface, ASUS says you turn Smart Connect off by giving each band its own name and password under **Network > Main network profile**.

Splitting the bands means you choose the band for each device yourself. Our [2.4 GHz vs. 5 GHz vs. 6 GHz guide](/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi/) explains which band suits which device, and our [smart device setup guide](/guides/smart-home-device-wont-connect-2-4-ghz/) covers devices that only work on 2.4 GHz. If your home is big enough that devices keep roaming between weak signals, better coverage may help more than steering rules: see our picks for the [best Wi-Fi router for a large house](/guides/best-wifi-router-for-large-house/).

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| ASUS recommends default Smart Connect settings when there are no special requirements; Default button restores them | [ASUS FAQ 1012132](https://asus.com/support/FAQ/1012132) (last update 2024-12-09) | Verified |
| Rule groups (1)–(4) and what each does; Bounce Detect example (twice in 60 seconds, 180 seconds) | [ASUS FAQ 1012132](https://asus.com/support/FAQ/1012132) | Verified |
| Field-level definitions (Bandwidth Utilization, Load Balance, RSSI, PHY Rate, VHT, Target Band, Window Time, Counts, Dwell Time) | [ASUS RT-AC5300 user manual](https://dlcdnets.asus.com/pub/ASUS/wireless/RT-AC5300/E15858_RT-AC5300_UM_v3_WEB.pdf) (August 2019) | Qualified: from one model's manual; fields can differ by model |
| Rules are web-only, some models lack them; phone preferences can override them; 802.11n devices fail with VHT set to AC only | [ASUS FAQ 1012132](https://asus.com/support/FAQ/1012132) | Verified |
| Interface 1 / Interface 2 firmware split at 3.0.0.6.102_35404 and the menu paths | [ASUS FAQ 1012132](https://asus.com/support/FAQ/1012132) | Qualified: ASUS doesn't tie the rule-page location to a firmware interface |
| For IoT devices on ASUS Wi-Fi 6 routers, turn off Smart Connect and select the band | [ASUS FAQ 1042475](https://www.asus.com/support/faq/1042475/) (last update 2024-07-22) | Verified |
