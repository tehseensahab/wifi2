---
title: "Dual-Band Wi-Fi 7: What You Lose Without 6 GHz"
date: 2026-10-31T04:00:00Z
description: "Dual-band Wi-Fi 7 routers skip 6 GHz, so no 320 MHz channels or 6 GHz links. You keep 4K QAM and MLO on 2.4 and 5 GHz. Here's who should care."
authors: ["Tehseen Arbab"]
topics: ["wifi-6e-7", "routers"]
tags: ["wifi-7", "dual-band", "6-ghz", "320-mhz", "mlo", "4k-qam", "eero-7", "asus-rt-be58u", "router-buying"]
summary: "A dual-band Wi-Fi 7 router has only 2.4 GHz and 5 GHz radios, so it can't use Wi-Fi 7's 320 MHz channels, which exist only in the 6 GHz band, or any MLO link that involves 6 GHz. It still gets 4K QAM and can use MLO across 2.4 and 5 GHz, with channels up to 160 MHz on 5 GHz. If your phones and laptops can't use 6 GHz anyway, or your internet plan is around 1 Gbps or less, a dual-band model gives up little you'd notice."
imageAlt: "Dense apartment blocks at dusk with lit windows, air-conditioning units and bamboo scaffolding"
imageCredit: "Photo: Raymond Yeung / [Unsplash](https://unsplash.com/photos/densely-packed-urban-buildings-with-many-lit-windows-at-night-G2CSVs4xXn8)"
takeaways:
  - "Dual-band Wi-Fi 7 routers have 2.4 GHz and 5 GHz radios only. Examples include Amazon's eero 7 and the ASUS RT-BE58U."
  - "Wi-Fi 7's headline 320 MHz channels exist only in the 6 GHz band, so a dual-band router can't offer them. On 5 GHz, the widest standard channel is 160 MHz."
  - "You keep 4K QAM and Multi-Link Operation (MLO), but MLO can only pair 2.4 GHz and 5 GHz, not the less crowded 6 GHz band."
  - "The FCC opened 1,200 MHz of 6 GHz spectrum to Wi-Fi in April 2020. A dual-band router leaves all of it unused, which matters most in crowded apartment buildings."
  - "Box ratings such as BE3600 add up each band's maximum link rate (ASUS shows 2,882 + 688 Mbps for the RT-BE58U). eero rates the eero 7 BE5000 but quotes wireless speeds 'up to 1.8 Gbps.'"
faq:
  - q: "Is a dual-band Wi-Fi 7 router real Wi-Fi 7?"
    a: "Yes. It uses the Wi-Fi 7 (802.11be) standard on 2.4 GHz and 5 GHz and can carry features such as 4K QAM and MLO. What it can't do is anything that needs the 6 GHz band, including 320 MHz channels."
  - q: "Does MLO work without 6 GHz?"
    a: "Yes, if both the router and your device support it. ASUS says the RT-BE58U's MLO combines and switches between the 2.4 GHz and 5 GHz bands, and eero lists MLO support for the dual-band eero 7. You just can't add a 6 GHz link."
  - q: "Is a tri-band Wi-Fi 6E router better than a dual-band Wi-Fi 7 router?"
    a: "It depends on your devices. If your phones and laptops support 6 GHz, a tri-band Wi-Fi 6E router gives them a band the dual-band Wi-Fi 7 router doesn't have. If they don't, the Wi-Fi 7 router's 4K QAM and MLO are the more useful extras."
  - q: "How do I tell whether a Wi-Fi 7 router has 6 GHz?"
    a: "Look for 'tri-band' or 'quad-band' and a 6 GHz entry in the spec sheet. Dual-band models list only 2.4 GHz and 5 GHz. TP-Link also advises checking the spec sheet for 320 MHz, since not every Wi-Fi 7 router lists it."
sources:
  - title: "Wi-Fi Alliance introduces Wi-Fi CERTIFIED 7"
    publisher: "Wi-Fi Alliance"
    url: "https://wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-7"
    date: 2024-01-08
  - title: "FCC Adopts New Rules For The 6 GHz Band, Unleashing 1,200 Megahertz Of Spectrum For Unlicensed Use"
    publisher: "FCC"
    url: "https://www.fcc.gov/document/fcc-opens-6-ghz-band-wi-fi-and-other-unlicensed-uses"
  - title: "FCC to open up 6 GHz band for unlicensed use"
    publisher: "IEEE Communications Society Technology Blog"
    url: "https://techblog.comsoc.org/2020/04/23/fcc-to-open-up-6-ghz-band-for-unlicensed-use-boon-for-wifi-6/"
    date: 2020-04-23
  - title: "Wi-Fi 7 features and benefits"
    publisher: "HPE Aruba Networking"
    url: "https://arubanetworking.hpe.com/techdocs/aos/wifi-design-deploy/generations/wifi7/feature-benefit/"
  - title: "Wi-Fi 7's 320 MHz channel width: is it worth the upgrade?"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/us/blog/2524/"
    date: 2026-06-23
  - title: "What are WiFi 7 320MHz channels?"
    publisher: "NETGEAR"
    url: "https://www.netgear.com/hub/network/wifi-7-320mhz-channels"
    date: 2025-12-02
  - title: "eero 7"
    publisher: "eero"
    url: "https://eero.com/support/articles/eero-7"
  - title: "RT-BE58U"
    publisher: "ASUS (New Zealand)"
    url: "https://www.asus.com/nz/networking-iot-servers/wifi-7/all-series/rt-be58u/"
---

A dual-band Wi-Fi 7 router has only 2.4 GHz and 5 GHz radios. That means it can't use Wi-Fi 7's widest channels, 320 MHz, which exist only in the 6 GHz band, and its Multi-Link Operation (MLO) can't include a 6 GHz link. It still gets Wi-Fi 7's 4K QAM and can run MLO across 2.4 and 5 GHz. If your phones and laptops don't support 6 GHz, or your internet plan is around 1 Gbps or less, you give up little you'd notice. If you live in a crowded building and own 6 GHz devices, pay for a tri-band model.

This is a research-based explainer. It draws on the Wi-Fi Alliance, the FCC, and router makers' published specifications. We have not tested these routers.

## What "dual-band Wi-Fi 7" means

Wi-Fi 7 is the standard (IEEE 802.11be). The band count is a separate question: how many radio frequency ranges the router broadcasts on.

- **Dual-band:** 2.4 GHz and 5 GHz.
- **Tri-band:** usually 2.4 GHz, 5 GHz and 6 GHz (some older tri-band designs use two 5 GHz radios instead, so check the spec sheet).
- **Quad-band:** 2.4 GHz and 6 GHz plus two 5 GHz radios, or a similar split.

Cheaper Wi-Fi 7 routers are often dual-band. Two current examples:

- **Amazon eero 7:** eero's spec page describes "dual-band 2.4 and 5 GHz antennas," 2x2 on each band, and does not mention 6 GHz.
- **ASUS RT-BE58U:** ASUS sells it as a "dual-band WiFi 7" router with speeds "up to 3600 Mbps."

Both are legitimately Wi-Fi 7. The question is which Wi-Fi 7 features depend on 6 GHz.

## What you lose without 6 GHz

### 320 MHz channels

When the Wi-Fi Alliance launched Wi-Fi CERTIFIED 7 on January 8, 2024, it listed 320 MHz channels first among the new features, saying they "double today's widest channel size." It also said they are "available in countries that make the 6 GHz band available to Wi-Fi."

TP-Link is blunter: "320 MHz channels are exclusive to the 6 GHz band in Wi-Fi 7," and "the 5 GHz band supports a maximum channel width of 160 MHz." HPE Aruba's Wi-Fi 7 design guide says the same: "320 MHz is optional and only supported in 6 GHz."

So most dual-band Wi-Fi 7 routers top out at 160 MHz on 5 GHz, the same width a good Wi-Fi 6 router offers. ASUS lists "ultrawide 160 MHz channels" for the RT-BE58U. eero's spec table for the eero 7 lists channel widths of "20, 40, 80, 160, 240 MHz"; eero doesn't explain the 240 MHz entry, but 320 MHz isn't on the list, and no dual-band router can use it.

How much does that cost you at home? Less than the marketing suggests. Wider channels raise the peak link rate between router and device, but you only see that if your internet plan or local file transfers are fast enough to use it, and the device is close to the router. Aruba also notes that there are few 320 MHz channels to go around: at most three non-overlapping ones where the full 6 GHz band is available, and fewer in some deployments. NETGEAR's band guide likewise lists "up to 3x 320Mhz Channels" in 6 GHz.

### The 6 GHz band itself

On April 23, 2020, the FCC voted to open 1,200 MHz of spectrum, 5.925 to 7.125 GHz, to unlicensed use such as Wi-Fi. Only devices that support 6 GHz (Wi-Fi 6E or Wi-Fi 7 with a 6 GHz radio) can use it. NETGEAR says 320 MHz Wi-Fi 7 "uses a portion of the wide 6 GHz band to reduce congestion."

A dual-band router leaves that spectrum unused. In a detached house with few neighbors, that often matters less, because 5 GHz tends to be less crowded. In an apartment building where many neighbors' routers share 2.4 and 5 GHz, a 6 GHz phone or laptop on a tri-band router has room the dual-band router can't offer. The trade-off is range: 6 GHz carries a shorter distance through walls than 5 GHz (see our [guide to the 2.4, 5 and 6 GHz bands]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}})).

### 6 GHz links in MLO

MLO lets a Wi-Fi 7 device connect over more than one link at once. Aruba describes it as letting devices "transmit and/or receive over more than one link or band at a time," and its examples pair 6 GHz with 2.4 or 5 GHz. A dual-band router can still do MLO, but only with 2.4 GHz and 5 GHz. Because 2.4 GHz is slower and often crowded, a 2.4 + 5 GHz pairing likely helps reliability more than peak speed. Our [Wi-Fi 7 MLO explainer]({{< relref "/guides/wifi-7-mlo" >}}) covers the modes and what your devices need.

## What you keep

- **4K QAM.** The Wi-Fi Alliance says 4K QAM "achieves 20% higher transmission rates than 1024 QAM," the top encoding in Wi-Fi 6 and 6E. It isn't tied to 6 GHz, and ASUS lists it for the RT-BE58U. It helps most when a device has a strong signal close to the router.
- **MLO on 2.4 and 5 GHz.** ASUS says the RT-BE58U's MLO works by "intelligently combining and switching between the 2.4 GHz and 5 GHz bands," and eero says the eero 7 adds "Multi-Link operation (MLO) support." ASUS adds that "supported MLO modes and bands may vary by device."
- **Up to 160 MHz channels on 5 GHz** (the eero 7 also lists a 240 MHz width), similar to many Wi-Fi 6 routers.
- **Everything outside the radio.** Ports, mesh support, security updates and the app aren't decided by the band count. The eero 7 has two 2.5 GbE ports, for example.

## Ignore the big number on the box

Wi-Fi 7 routers are sold with class ratings such as BE3600 or BE5000. These are built from the maximum link rates of the router's bands, not what a single device gets. An ASUS product image for the RT-BE58U shows 2,882 Mbps on 5 GHz and 688 Mbps on 2.4 GHz, which add up to 3,570 Mbps, rounded to the BE3600 figure. eero sells the eero 7 with a "BE5000 Rating" but states its wireless speeds as "up to 1.8 Gbps." Neither figure is a measurement of real-world throughput, and neither is your internet speed.

## Who should buy which

| Your situation | Dual-band Wi-Fi 7 is fine | Pay for tri-band (with 6 GHz) |
|---|---|---|
| Internet plan | Around 1 Gbps or less | Multi-gig plan you want to use over Wi-Fi |
| Your devices | Few or none support 6 GHz | Recent phones or laptops that support 6 GHz |
| Where you live | House with few nearby networks | Apartment or dense neighborhood with crowded 5 GHz |
| Budget | Want Wi-Fi 7 features at the lowest price | Willing to pay more for the extra band |

If you're comparing a dual-band Wi-Fi 7 router with a tri-band Wi-Fi 6E router at a similar price, our [Wi-Fi 6E vs. Wi-Fi 7 guide]({{< relref "/guides/wifi-6e-vs-wifi-7" >}}) walks through that choice. For apartment picks, see our [best router for an apartment]({{< relref "/guides/best-router-for-apartment" >}}).

## How to check before you buy

1. Look at the band list on the spec sheet, not just the Wi-Fi 7 logo. If it shows only 2.4 GHz and 5 GHz, it's dual-band.
2. Look for 320 MHz. TP-Link warns that "not all Wi-Fi 7 routers explicitly list 320 MHz as a feature, so check the spec sheet before buying."
3. Check your devices. Your phone's or laptop's specifications will say whether it supports 6 GHz (often listed as Wi-Fi 6E or Wi-Fi 7 with 6 GHz). If none do, a 6 GHz radio would go unused for now.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Wi-Fi CERTIFIED 7 launched Jan. 8, 2024; 320 MHz channels need 6 GHz; 4K QAM 20% over 1024 QAM | [Wi-Fi Alliance](https://wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-7) | Verified |
| 320 MHz only in 6 GHz; 5 GHz max 160 MHz | [TP-Link](https://www.tp-link.com/us/blog/2524/), [HPE Aruba](https://arubanetworking.hpe.com/techdocs/aos/wifi-design-deploy/generations/wifi7/feature-benefit/) | Verified |
| Number of 320 MHz channels; MLO band examples | [HPE Aruba](https://arubanetworking.hpe.com/techdocs/aos/wifi-design-deploy/generations/wifi7/feature-benefit/), [NETGEAR](https://www.netgear.com/hub/network/wifi-7-320mhz-channels) | Verified |
| FCC opened 1,200 MHz at 5.925–7.125 GHz on April 23, 2020 (date from secondary source) | [FCC](https://www.fcc.gov/document/fcc-opens-6-ghz-band-wi-fi-and-other-unlicensed-uses), [IEEE ComSoc](https://techblog.comsoc.org/2020/04/23/fcc-to-open-up-6-ghz-band-for-unlicensed-use-boon-for-wifi-6/) | Verified |
| eero 7 bands, channel widths, MLO, BE5000, 1.8 Gbps, 2.5 GbE ports | [eero](https://eero.com/support/articles/eero-7) | Verified (manufacturer specs) |
| RT-BE58U dual-band, 3600 Mbps, 160 MHz, 4K QAM, 2.4 + 5 GHz MLO | [ASUS](https://www.asus.com/nz/networking-iot-servers/wifi-7/all-series/rt-be58u/) | Qualified (New Zealand product page) |
