---
title: "Mid-Split vs. High-Split: Cable Upload Upgrades Explained"
date: 2026-11-28T05:00:00Z
description: "Mid-split vs. high-split: cable upgrades that widen upload spectrum from 5-42 MHz to 5-85 MHz (mid) or 5-204 MHz (high). What changes and which modem you need."
authors: ["Tehseen Arbab"]
topics: ["internet-plans-isps", "how-to-fixes"]
tags: ["mid-split", "high-split", "cable-internet", "upload-speed", "docsis-3-1", "cable-modem", "xfinity", "spectrum"]
summary: "Mid-split and high-split are cable network upgrades that give upload more of the line's frequencies: 5-85 MHz for mid-split and 5-204 MHz for high-split, up from 5-42 MHz. More upload spectrum lets cable companies sell faster upload tiers, but only if your modem supports the same split. According to Light Reading, Comcast has focused mostly on mid-split and Spectrum on high-split."
imageAlt: "Wooden utility pole with a transformer, a street light arm and many overhead lines crossing against a blue sky with white clouds"
imageCredit: "Photo: Greg Rosenke / [Unsplash](https://unsplash.com/photos/a-telephone-pole-with-a-sky-background-2OrOt0QyNDk)"
takeaways:
  - "A cable line splits its frequencies between upload and download. For North America, CableLabs defines sub-split (low-split) upload as 5-42 MHz, mid-split as 5-85 MHz and high-split as 5-204 MHz."
  - "More upload spectrum lets providers sell faster upload tiers. Comcast's data (published December 2024, tiers on sale in April 2024): its 1,200 Mbps plan came with a 35 Mbps upload tier (median 40 Mbps) on sub-split plant and a 200 Mbps tier (median 208 Mbps) on mid-split."
  - "Your modem must support the split your provider uses. NETGEAR: 'Your modem and ISP must both support a frequency split for you to be able to use it.'"
  - "Comcast (Xfinity) has focused mostly on mid-split and Charter (Spectrum) on high-split, according to Light Reading's November 10, 2026 report."
  - "Xfinity says owned modems 'should work for service tier speeds available before the recent upgrade'; for the new upload speeds you need a device certified for its upgraded network."
faq:
  - q: "What is the difference between mid-split and high-split?"
    a: "How much of the cable line is used for upload. Mid-split uses 5-85 MHz for upload and starts download above 108 MHz. High-split extends upload to 204 MHz and starts download at 258 MHz. High-split leaves room for more upload capacity than mid-split."
  - q: "Do I need a new modem for mid-split or high-split?"
    a: "Possibly. NETGEAR says your modem and your provider must both support the split. Xfinity says owned modems should keep working at the speeds offered before the upgrade, but you need a device certified for its upgraded network to get the new upload speeds."
  - q: "Does a DOCSIS 3.1 modem support high-split?"
    a: "Not every one. The DOCSIS 3.1 specification added high-split, but individual modems list their own upstream range. For example, the ARRIS SURFboard S34, a DOCSIS 3.1 modem, switches between 5-42 MHz and 5-85 MHz (low and mid-split), while NETGEAR markets the CM3000 for both mid-split and high-split."
  - q: "How do I know if my area has the mid-split or high-split upgrade?"
    a: "Neither Xfinity nor Spectrum publishes a split-by-address lookup that we found. The practical sign is that your provider offers faster upload tiers at your address. Xfinity says new upload speeds in its upgraded markets range from 75 to 200 Mbps, with symmetrical X-Class tiers above that in limited areas; ask your provider which modems are certified for them."
  - q: "Is high-split available yet?"
    a: "Yes, in some places. Light Reading, reporting on an Ookla study on November 10, 2026, says only 13% of the Charter cities Ookla tracked were upgraded as of Q2 2026, but in Spectrum's high-split markets saw median upload speeds rise about elevenfold, to about 223.60 Mbps. NETGEAR's support article, last updated July 2025, still says no ISP uses high-split, so treat that line as out of date."
sources:
  - title: "Band Splits 101: Splitting Our Way to 10G"
    publisher: "CableLabs"
    url: "https://www.cablelabs.com/blog/band-splits-splitting-our-way-to-10g"
    date: "2021-12-09"
  - title: "What is mid/high-split technology?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/000066051/What-is-mid-high-split-technology"
    date: "2025-07-07"
  - title: "Mid-Split / High-Split"
    publisher: "Broadband Library"
    url: "https://broadbandlibrary.com/mid-split-high-split/"
    date: "2021-11-20"
  - title: "Comcast Network Management (Detailed Measurement Results)"
    publisher: "Xfinity"
    url: "https://www.xfinity.com/networkmanagement"
    date: "2024-12-18"
  - title: "Devices certified for enhanced speeds required in recently upgraded areas"
    publisher: "Xfinity"
    url: "https://www.xfinity.com/support/articles/upgraded-areas-leased-equipment-required-for-upload-speeds"
    date: "2026-08-30"
  - title: "Upstream speeds rev up where cable has done the 'splits' – study"
    publisher: "Light Reading"
    url: "https://www.lightreading.com/cable-technology/upstream-speeds-accelerate-where-cable-has-done-the-splits-study"
    date: "2026-11-10"
  - title: "When is our Network Evolution coming to you?"
    publisher: "Spectrum Community"
    url: "https://community.spectrum.net/discussion/177269/high-split-what-is-it-and-when-is-our-network-evolution-coming-to-you"
---

**Mid-split and high-split are upgrades to cable internet networks that hand more of the cable line's frequencies to upload. Traditional cable (sub-split, or low-split) uploads on 5 to 42 MHz; mid-split widens that to 5 to 85 MHz and high-split to 5 to 204 MHz. More upload spectrum lets your provider sell much faster upload speeds, but you only get them if your modem supports the same split.** According to Light Reading, Comcast (Xfinity) has focused mostly on mid-split upgrades and Charter (Spectrum) on high-split.

This guide explains what changes on the line, what speeds the upgrades have delivered so far, and when you need a new modem. It is based on CableLabs, provider and modem-maker documentation, checked on November 28, 2026.

## What "split" means on a cable line

A cable line carries upload and download traffic on the same coax, separated by frequency. Low frequencies carry upload; everything above a guard gap carries download. The "split" is where that boundary sits. CableLabs, the cable industry's research lab, defines the three North American options:

| Split | Upload (upstream) | Download (downstream) starts |
|---|---|---|
| Sub-split (low-split) | 5-42 MHz | 54 MHz |
| Mid-split | 5-85 MHz | Above 108 MHz |
| High-split | 5-204 MHz | 258 MHz |

Source: [CableLabs, Band Splits 101](https://www.cablelabs.com/blog/band-splits-splitting-our-way-to-10g).

Mid-split more than doubles the upload spectrum of a sub-split line (80 MHz of range instead of 37 MHz). High-split gives upload more than five times the range of sub-split (199 MHz). Those are widths of spectrum, not speeds; how much speed a provider sells from them is its own decision.

Moving the split isn't a setting a provider flips. CableLabs says that for most cable operators, a move to mid-split or high-split "will require switching out signal amplifiers and other legacy equipment," because the amplifiers along the line use filters to keep upload and download frequencies apart. That's one reason upgrades tend to roll out area by area.

## What the upgrades do to upload speeds

The clearest before-and-after figures come from Comcast's own network disclosures. Its measurement table (published December 18, 2024) lists the same download plans on both kinds of plant, with medians measured to the cable modem gateway:

| Download plan | Sub-split: upload tier / median | Mid-split: upload tier / median |
|---|---|---|
| 300 Mbps | 20 / 23 Mbps | 100 / 114 Mbps |
| 1,000 Mbps | 20 / 23 Mbps | 100 / 114 Mbps |
| 1,200 Mbps | 35 / 40 Mbps | 200 / 208-209 Mbps |

Source: [Xfinity network management page](https://www.xfinity.com/networkmanagement). Medians are peak and off-peak; they measure the connection to the gateway, not Wi-Fi speeds on your devices. Comcast notes the table lists tiers on sale as of April 9, 2024, and some aren't available in all markets.

On the 1,200 Mbps download plan, the mid-split version (200 Mbps upload tier) had a median upload about five times that of the sub-split version (35 Mbps tier). Xfinity's current support article puts it more broadly: "The new upload speeds in enhanced markets are up to 5–10 times faster than before, ranging from 75–200 Mbps."

For high-split, the most recent independent figure we found is second-hand. Light Reading reported on November 10, 2026 that in a study of US and Canadian Speedtest data (Q2 2024 to Q2 2026), Ookla "found that median upload speed rose about eleven-fold, to about 223.60 Mbit/s in Spectrum's high-split markets," while legacy networks "barely moved." We could not read Ookla's report directly, so treat those numbers as Ookla's, reported by Light Reading.

If you're not sure how much upload you actually need, see our guide to [what counts as a good upload speed](/guides/good-upload-speed/).

## Who uses which split

- **Comcast (Xfinity): mostly mid-split.** Light Reading writes that "Comcast is largely focused on mid-splits" for its cable network upgrades. The Xfinity support article we cite doesn't use the word "mid-split"; it talks about "enhanced markets" and "recently upgraded areas."
- **Charter (Spectrum): high-split.** Light Reading says Spectrum "is pushing ahead with a multi-phase HFC network plan focused on high-split upgrades." In a May 2025 post on Spectrum's community site, an employee moderator wrote that 50% of the current Spectrum network will be upgraded to symmetrical and multi-gig service by the end of 2026, with the rest set to support symmetrical service by the end of 2027. That's a target, not a completion date, and the post doesn't say which split it uses.
- **Cox (now part of Charter): furthest along.** Light Reading, summarizing Ookla's data, says Cox had 77% of its cities upgraded as of Q2 2026, versus 13% for Charter.

One source to read with care: NETGEAR's support article on splits, last updated July 7, 2025, says high-split "is not currently used by any ISPs but is expected to be used in the future." Light Reading's 2026 reporting on Spectrum's high-split markets shows that line is out of date.

## Do you need a new modem?

Possibly, and this is where most of the confusion comes from. NETGEAR puts it plainly: "Your modem and ISP must both support a frequency split for you to be able to use it." A modem built for 5-42 MHz upload can't transmit on the extra spectrum a mid-split or high-split line opens up.

What that means in practice:

- **With Xfinity, your current modem should keep working at the old upload speeds.** Xfinity says: "If you own your own modem, eMTA or gateway, they should work for service tier speeds available before the recent upgrade." To move to the faster tiers, Xfinity says you need to "purchase a device certified to work on our upgraded network," and it keeps the list of certified retail devices at xfinity.com/support/devices.
- **Xfinity's symmetrical X-Class tiers rule out owned modems.** The same article describes X-Class as equally fast upload and download "above 200 Mbps," "available in limited areas," and says "customer-owned modems are not currently compatible with X-Class speeds."
- **DOCSIS 3.1 is the baseline, but check the split.** Light Reading notes that, depending on the speed tier, customers "might also require a new cable modem or gateway based on DOCSIS 3.1, DOCSIS 3.1+ or DOCSIS 4.0." The DOCSIS 3.1 specification allows high-split, but a DOCSIS 3.1 label alone doesn't guarantee a modem supports it: the ARRIS SURFboard S34 switches between 5-42 MHz and 5-85 MHz (low and mid-split), while NETGEAR sells the CM3000 for both mid-split and high-split. Our [NETGEAR CM3000 vs. ARRIS S34 comparison](/guides/netgear-cm3000-vs-arris-s34/) covers both. To see which DOCSIS version you have now, use our guide on [what DOCSIS version your modem is](/guides/what-docsis-is-my-modem/).

Look for the upstream frequency range on a modem's data sheet (sometimes listed as the "diplexer" range). If it tops out at 85 MHz, the modem can do mid-split but not high-split.

## How to tell if your area has been upgraded

We didn't find a split-by-address lookup from Xfinity or Spectrum. The practical checks:

1. **Look at the upload speeds offered at your address.** If your provider now sells upload tiers well above the 20-35 Mbps upload tiers Comcast lists for its sub-split plans, your area has likely been upgraded.
2. **Check whether your modem is certified for the new tiers.** For Xfinity, compare your model with the certified device list; if it isn't on it, expect to stay on the pre-upgrade speed tiers.
3. **Run a wired speed test after any change.** Plug a computer into the modem or router with Ethernet so Wi-Fi limits don't hide the result. If upload is still slow on a wired test, our guide to [why your upload speed is slow](/guides/why-is-my-upload-speed-slow/) walks through the other causes.

For more on how cable modem generations differ, see [DOCSIS 3.0 vs. 3.1 vs. 4.0](/guides/docsis-3-0-vs-3-1-vs-4-0-cable-modem/).

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Sub-split 5-42 MHz up / 54 MHz down; mid-split 5-85 / above 108 MHz; high-split up to 204 / 258 MHz | [CableLabs](https://www.cablelabs.com/blog/band-splits-splitting-our-way-to-10g) | Verified |
| Moving the split requires replacing amplifiers and other legacy equipment | [CableLabs](https://www.cablelabs.com/blog/band-splits-splitting-our-way-to-10g) | Verified |
| Comcast median uploads on sub-split vs. mid-split plant (300, 1,000, 1,200 Mbps plans) | [Xfinity network management](https://www.xfinity.com/networkmanagement) | Verified (Comcast data, published Dec. 2024; tiers as of April 9, 2024) |
| Upgraded-market upload speeds 75-200 Mbps; owned modems keep pre-upgrade tiers; certified device needed; owned modems not compatible with X-Class | [Xfinity support](https://www.xfinity.com/support/articles/upgraded-areas-leased-equipment-required-for-upload-speeds) | Verified |
| Spectrum high-split median upload up about elevenfold to about 223.60 Mbps; Comcast mid-split focus; Spectrum high-split focus; Cox 77% and Charter 13% of cities upgraded (Q2 2026); DOCSIS 3.1 or newer modem may be needed | [Light Reading on Ookla study](https://www.lightreading.com/cable-technology/upstream-speeds-accelerate-where-cable-has-done-the-splits-study) | Qualified (secondary report of Ookla data) |
| Spectrum target: 50% of network symmetrical/multi-gig by end of 2026, rest symmetrical by end of 2027 | [Spectrum Community (employee moderator)](https://community.spectrum.net/discussion/177269/high-split-what-is-it-and-when-is-our-network-evolution-coming-to-you) | Qualified (company target, May 2025 community post; split not named) |
| Modem and ISP must both support the split; high-split "not currently used by any ISPs" (July 2025) | [NETGEAR KB](https://kb.netgear.com/000066051/What-is-mid-high-split-technology) | Qualified (status as of July 2025; now out of date) |
| ARRIS S34 switches between 5-42 and 5-85 MHz; NETGEAR markets the CM3000 for mid- and high-split | [ARRIS S34 data sheet](https://webcdn.cox.com/content/dam/cox/residential/support/internet/print_media/Arris_S34_DataSheet.pdf) and [NETGEAR CM3000 page](https://www.netgear.com/hub/technology/mid-high-split-modem-cm3000/), via our [CM3000 vs. S34 comparison](/guides/netgear-cm3000-vs-arris-s34/) | Verified (Nov. 22, 2026) |
| DOCSIS 3.1 specification introduced high-split | [Broadband Library](https://broadbandlibrary.com/mid-split-high-split/) | Verified |
