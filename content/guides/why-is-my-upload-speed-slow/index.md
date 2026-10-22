---
title: "Why Is My Upload Speed So Slow? Causes and Fixes"
date: 2026-10-19
description: "Slow upload is often built into your plan, especially on cable and 5G home internet. Here's how to check, how to test properly, and what to fix at home."
authors: ["Tehseen Arbab"]
topics: ["internet-plans-isps", "how-to-fixes"]
tags: ["upload-speed", "speed-test", "cable-internet", "fiber", "5g-home-internet", "troubleshooting"]
summary: "Upload speed is usually slow because the plan was built that way: many cable and 5G home internet plans send far less than they receive, while fiber plans such as AT&T Fiber are symmetrical. Check your plan's upload figure first, then run a wired speed test with any VPN off. If a wired test matches the plan but Wi-Fi doesn't, the problem is in your home; if both fall well short, contact your provider."
imageAlt: "Smartphone on a tripod showing a live-streaming app with a LIVE NOW banner over a man holding a camera"
imageCredit: "Photo: Detail .co / [Unsplash](https://unsplash.com/photos/5MRJkV_la-w)"
takeaways:
  - "Look up your plan's upload speed before troubleshooting. Many plans are asymmetrical by design: T-Mobile, for example, lists typical 5G Home Internet upload speeds of 12 to 55 Mbps, against typical downloads that range from 133 to 498 Mbps depending on plan and gateway."
  - "Fiber is often symmetrical. AT&T says its fiber service delivers equal upload and download speeds."
  - "The FCC's benchmark for fixed broadband is 100 Mbps down and 20 Mbps up; it set that figure in March 2024 and kept it in its August 2026 report."
  - "Test with a wired computer and any VPN turned off. If the wired result matches your plan but Wi-Fi doesn't, the bottleneck is in your home network."
  - "Cameras and backups add up. Ring's guidance is about 2 Mbps of upload per 1080p camera and 15 Mbps per 4K camera."
faq:
  - q: "Why is my upload speed so much lower than my download speed?"
    a: "Usually because your plan is built that way. Many cable and 5G home internet plans have much lower upload than download speeds: T-Mobile, for example, lists typical 5G Home Internet uploads of 12 to 55 Mbps. On cable, CableLabs lists DOCSIS 3.1 upstream capacity at 1 to 2 Gbps, shared across many homes, versus up to 6 Gbps for DOCSIS 4.0. Fiber plans are often symmetrical; AT&T says its fiber delivers equal upload and download speeds."
  - q: "What is a good upload speed?"
    a: "The FCC's benchmark for fixed home broadband includes at least 20 Mbps of upload. Ring's guidance puts a 1080p camera at about 2 Mbps of upload, so what's enough depends on how many calls, cameras and backups run at once."
  - q: "Can my router or Wi-Fi cause slow upload speeds?"
    a: "Yes. Test with a computer plugged into the router by Ethernet, then over Wi-Fi from the same spot and from where you usually work. If only the Wi-Fi tests are slow, look at signal, router placement and the band you're on."
  - q: "Does a VPN slow down upload speed?"
    a: "It can. Ring tells customers to turn off any VPN before running a speed test, so you're measuring your connection rather than the VPN's route. Test with it on and off to see the difference."
  - q: "When should I call my internet provider about slow upload?"
    a: "When a wired test, with the VPN off and nothing else uploading, falls well short of your plan's upload speed. Ring suggests contacting your provider if a test next to the router shows less than 60% of the speed you pay for."
sources:
  - title: "Frequently Asked Questions: 5G Home Internet"
    publisher: "T-Mobile"
    url: "https://www.t-mobile.com/home-internet/faq"
    date: 2026-10-19
  - title: "AT&T Fiber"
    publisher: "AT&T"
    url: "https://att.com/fiber"
    date: 2026-10-19
  - title: "2024 Section 706 Report (FCC 24-27)"
    publisher: "FCC"
    url: "https://docs.fcc.gov/public/attachments/FCC-24-27A1.pdf"
    date: 2024-03-18
  - title: "Did the FCC Answer the Broadband Deployment Question Congress Asked?"
    publisher: "Benton Institute for Broadband & Society"
    url: "https://www.benton.org/blog/did-fcc-answer-broadband-deployment-question-congress-asked"
  - title: "Federal Communications Commission: Broadband Labeling Requirements"
    publisher: "Akin Gump"
    url: "https://www.akingump.com/en/insights/alerts/federal-communications-commission-broadband-labeling-requirements"
  - title: "DOCSIS 4.0 Technology"
    publisher: "CableLabs"
    url: "https://www.cablelabs.com/technologies/docsis-4-0-technology"
    date: 2026-10-19
  - title: "Understanding wifi recommendations for Ring devices"
    publisher: "Ring"
    url: "https://ring.com/support/articles/92bd2/Test-Your-Wifi-Connections"
    date: 2026-10-19
---

Upload speed is usually slow because your internet plan was built that way. Many cable and 5G home internet plans send data far more slowly than they receive it; fiber plans are more often symmetrical, with equal upload and download speeds. So the first step is to find your plan's upload figure. If a wired speed test matches it, your connection is working as sold, and the fix is a different plan or less competition for the upload you have. If a wired test falls well short, the problem is your equipment or your provider.

Upload is the data you send: your camera on a video call, photos backing up to the cloud, a live stream, footage from security cameras. Download is the data you receive. This guide covers how to tell which kind of "slow upload" you have and what to do about each. It draws on provider, FCC and manufacturer documentation.

## Step 1: Check what upload speed your plan includes

Internet ads lead with download speed, so many people never see their upload figure. Look for it on your provider's website, your bill or the broadband label for your plan. FCC rules require providers to show labels that include typical download and upload speeds and latency.

What you'll typically find depends on the technology:

| Connection | Upload vs. download | Example from a provider or standards body |
|---|---|---|
| Fiber | Often equal | AT&T says its fiber "delivers equal upload and download speeds" |
| 5G home internet | Much lower upload | T-Mobile lists typical upload of 12 to 55 Mbps; typical download ranges run from 133 to 498 Mbps depending on plan and gateway |
| Cable (DOCSIS) | Usually lower upload | CableLabs lists DOCSIS 3.1 upstream capacity at 1 to 2 Gbps, against up to 6 Gbps for DOCSIS 4.0 |

The CableLabs figures are network capacity in the specifications, shared across many homes, not the speed of any plan; CableLabs says deployed performance varies. By those figures, DOCSIS 4.0 has three to six times the upstream capacity of DOCSIS 3.1. Our [DOCSIS 3.0 vs. 3.1 vs. 4.0 guide]({{< relref "/guides/docsis-3-0-vs-3-1-vs-4-0-cable-modem" >}}) covers what each modem generation supports.

For context, the FCC's benchmark for fixed home broadband is 100 Mbps download and 20 Mbps upload. It adopted that figure on March 14, 2024, and its 2026 broadband report, released August 14, 2026, kept it while dropping the FCC's longer-term goal of 1 Gbps down and 500 Mbps up.

T-Mobile's ranges also show how wide "typical" can be: for its main plans and latest gateway, it says 25% of customers see speeds below the range and 25% see speeds above it.

## Step 2: Test your upload properly

A single phone test over Wi-Fi tells you little. To find where the bottleneck is:

1. **Stop other uploads.** Pause cloud photo and file backups and, if you can, anything else sending data, such as cameras or a game console uploading clips.
2. **Turn off any VPN.** Ring's own speed-test instructions start with this step. A VPN sends your traffic through another server, so you'd be testing that route instead of your connection.
3. **Test wired.** Plug a computer into the router with an Ethernet cable and run a speed test.
4. **Test over Wi-Fi in two places.** Once near the router, then where you usually work or where the device that uploads sits. Ring suggests testing next to the router and again where its device is installed.
5. **Compare with your plan.** Ring tells customers to contact their provider if the test next to the router shows less than 60% of the speed they pay for.

Then read the results:

| Result | What it points to |
|---|---|
| Wired upload roughly matches your plan, and so does Wi-Fi near the router | Your connection works as sold. Your plan's upload may be too small for what you do. |
| Wired matches the plan, Wi-Fi is much slower | Your home Wi-Fi: signal, placement or the device |
| Wired upload is well below your plan too | Your modem, router or provider |
| Slow only with the VPN on | The VPN |

## Step 3: Fix what you found

### If your plan's upload is simply too low

Add up what your household sends at the same time. Ring's guidance gives a sense of scale for cameras: about 1 Mbps of upload for a 720p device, 2 Mbps for 1080p, 2.5 Mbps for 1536p, 10 Mbps for 2K and 15 Mbps for 4K. Three 1080p cameras uploading at once would use about 6 Mbps by that measure, which is a large share of a plan with 10 Mbps of upload. Our guide to [how much internet speed you need]({{< relref "/guides/how-much-internet-speed-do-i-need" >}}) has figures for video calls and other uses.

If the total is close to your plan's upload, the options are a higher tier, a different technology if one is available at your address (AT&T, for example, says its fiber has equal upload and download speeds), or scheduling large uploads such as backups for overnight.

### If uploads make everything else lag

When an upload fills your connection, video calls and games can stutter even though downloads look fine. That's often bufferbloat: data queues up in the router or modem and delays everything behind it. Our [bufferbloat guide]({{< relref "/guides/fix-bufferbloat-gaming-lag" >}}) explains how to test for it and which router settings, such as smart queue management, help.

### If only Wi-Fi uploads are slow

The problem is between your device and the router, not your internet connection. Try the same fixes as for slow Wi-Fi in general: move closer or move the router to a central spot, use the 5 GHz or 6 GHz band near the router, and update the device's Wi-Fi drivers. Our guide to [why Wi-Fi is slow when the internet is fast]({{< relref "/guides/wifi-slow-but-internet-fast" >}}) walks through it. For a device that uploads constantly, such as a desktop PC used for streaming, a wired connection removes Wi-Fi from the equation.

### If even wired uploads fall short

Restart the modem and router, then test again. Check that your modem supports your plan; on cable, the DOCSIS guide linked above lists the upload limits Netgear gives for each modem generation, and your provider's list of approved modems shows what it supports. If a wired test with nothing else running still falls well short of your plan, contact your provider with your test results, including the time and whether the test was wired.

## Bottom line

Start with your plan's upload number, not your router settings. Many plans, especially on cable and 5G home internet, are built with slow upload, and no setting changes that. If your wired results match your plan, the fix is a different plan or less competition for upload; if Wi-Fi alone is slow, fix your home network; if wired results fall short too, take it to your provider.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| T-Mobile 5G Home Internet typical upload 12 to 55 Mbps; typical download 133 to 498 Mbps depending on plan and gateway; 25% of customers below and 25% above the ranges | [T-Mobile FAQ](https://www.t-mobile.com/home-internet/faq) | Verified as of October 19, 2026 |
| AT&T Fiber "delivers equal upload and download speeds" | [AT&T Fiber](https://att.com/fiber) | Verified as of October 19, 2026; AT&T says speeds are based on a wired connection and may vary |
| FCC fixed broadband benchmark of 100 Mbps down / 20 Mbps up, adopted March 14, 2024 | [FCC 24-27](https://docs.fcc.gov/public/attachments/FCC-24-27A1.pdf) | Verified |
| 2026 report, released August 14, 2026, kept 100/20 and dropped the 1 Gbps / 500 Mbps long-term goal | [Benton Institute](https://www.benton.org/blog/did-fcc-answer-broadband-deployment-question-congress-asked) | Qualified: summary of the FCC report by the Benton Institute |
| Broadband labels must include typical upload and download speeds and latency | [Akin Gump summary of FCC rules](https://www.akingump.com/en/insights/alerts/federal-communications-commission-broadband-labeling-requirements) | Qualified: law-firm summary |
| DOCSIS 3.1 upstream capacity 1 to 2 Gbps; DOCSIS 4.0 up to 6 Gbps upstream; deployed performance varies | [CableLabs](https://www.cablelabs.com/technologies/docsis-4-0-technology) | Verified |
| Ring per-device upload guidance; turn off VPN before testing; test near router and at device; contact provider if a test next to the router is below 60% of plan | [Ring Support](https://ring.com/support/articles/92bd2/Test-Your-Wifi-Connections) | Verified as of October 19, 2026 |
