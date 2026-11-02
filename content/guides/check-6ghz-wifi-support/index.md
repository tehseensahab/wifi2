---
title: "Does My Device Support 6 GHz Wi-Fi? How to Check"
date: 2026-11-02T04:35:00Z
description: "Does your device support 6 GHz Wi-Fi? It needs Wi-Fi 6E or Wi-Fi 7 hardware, plus Windows 11 on PCs. How to check iPhone, iPad, Mac, Windows and Android."
authors: ["Tehseen Arbab"]
topics: ["wifi-6e-7", "how-to-fixes"]
tags: ["6-ghz", "wifi-6e", "wifi-7", "iphone", "windows-11", "android", "intel"]
summary: "Your device can use 6 GHz Wi-Fi only if its Wi-Fi hardware is Wi-Fi 6E or Wi-Fi 7, and on a PC only with Windows 11 and an up-to-date driver. Apple publishes a list of 6 GHz-capable models; on Windows, a quick check in Settings shows the band you're on. A plain Wi-Fi 6 device can't see 6 GHz networks at all."
imageAlt: "Laptop on a stand, a large monitor, a tablet with keyboard and a smartphone on a white desk, all with blank screens"
imageCredit: "Photo: Jakub Żerdzicki / [Unsplash](https://unsplash.com/photos/a-desk-with-two-laptops-and-a-phone-on-it-z0xdapnPMJ8)"
takeaways:
  - "A device needs Wi-Fi 6E or Wi-Fi 7 hardware to use 6 GHz. Intel says Wi-Fi 6 or older devices do not support the 6 GHz band."
  - "On iPhone, 6 GHz support starts with iPhone 15 Pro, but Apple excludes iPhone 15, iPhone 15 Plus, iPhone 16e and iPhone 17e. Macs need a MacBook Pro, iMac, Mac mini, Mac Studio or Mac Pro introduced in 2023 or later, a MacBook Air with M3 or later, or MacBook Neo."
  - "Windows PCs need Windows 11 and a 6 GHz-capable adapter with a current driver. NETGEAR reports Microsoft won't add 6 GHz to Windows 10."
  - "On Windows 11, Settings > Network & internet > Wi-Fi > your network's properties shows the band in use under Network band (channel)."
  - "Region matters: Apple and TP-Link both say 6 GHz isn't available everywhere. The US opened 1,200 MHz of 6 GHz spectrum to Wi-Fi."
faq:
  - q: "Does Wi-Fi 6 support 6 GHz?"
    a: "No. Despite the name, Wi-Fi 6 runs on 2.4 GHz and 5 GHz only. Intel's support article says Wi-Fi 6 or lower devices do not support the 6 GHz band; you need Wi-Fi 6E or Wi-Fi 7."
  - q: "Does iPhone 15 support 6 GHz Wi-Fi?"
    a: "Only the Pro models. Apple's Wi-Fi 6E article lists iPhone 15 Pro and iPhone 15 Pro Max or later, and specifically excludes iPhone 15 and iPhone 15 Plus. iPhone 16e and iPhone 17e are excluded too."
  - q: "Can Windows 10 use 6 GHz Wi-Fi?"
    a: "No. NETGEAR's support article says Microsoft is not backporting 6 GHz support to Windows 10, so a PC needs Windows 11, even if its Wi-Fi card is a Wi-Fi 6E model."
  - q: "My laptop has a Wi-Fi 6E card but can't see the 6 GHz network. Why?"
    a: "Check three things: you're on the latest Windows 11, the Wi-Fi driver is current (Intel lists version 22.70.0 or later for its Wi-Fi 6E cards), and the laptop maker has enabled the band. Intel notes the system manufacturer may not enable 6 GHz on every platform, and a manually installed card should be validated by the PC maker."
  - q: "How do I check an Android phone?"
    a: "Look up your exact model's official spec sheet and check whether it lists Wi-Fi 6E or Wi-Fi 7 with 6 GHz. Android menus differ by phone maker, so your model's official spec sheet is the most reliable source."
sources:
  - title: "Use Wi-Fi 6E networks with Apple devices"
    publisher: "Apple Support"
    url: "https://support.apple.com/102285"
    date: 2026-10-27
  - title: "Wi-Fi and Ethernet specifications for Apple devices"
    publisher: "Apple Platform Deployment"
    url: "https://support.apple.com/guide/deployment/dep268652e6c"
  - title: "Faster and more secure Wi-Fi in Windows"
    publisher: "Microsoft Support"
    url: "https://support.microsoft.com/topic/26177a28-38ed-1a8e-7eca-66f24dc63f09"
  - title: "Does my Microsoft Windows PC support 6 GHz WiFi?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/000064414/Does-my-Microsoft-Windows-PC-support-6-GHz-WiFi"
    date: 2025-07-07
  - title: "Intel Wi-Fi 6E (Gig+) products: 6 GHz requirements"
    publisher: "Intel"
    url: "https://www.intel.com/content/www/us/en/support/articles/000059385.html"
    date: 2025-02-06
  - title: "Intel Wi-Fi 6E AX210 Adapter Cannot Connect to a 6 GHz Band"
    publisher: "Intel"
    url: "https://www.intel.com/content/www/us/en/support/articles/000087538.html"
    date: 2024-01-30
  - title: "Can't find or connect to 6GHz Wi-Fi?"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/uk/support/faq/3092"
    date: 2026-09-14
  - title: "Wi-Fi 6E: Wi-Fi in the 6 GHz band (2021)"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/node/37285"
---

Your device supports 6 GHz Wi-Fi only if its Wi-Fi hardware is Wi-Fi 6E or Wi-Fi 7. A plain Wi-Fi 6 device can't use the band at all, and a Windows PC also needs Windows 11 and a current driver. The fastest checks: compare your Apple device against Apple's published list; on Windows, check your adapter's model and open one Settings page to see which band you're on; and read your Android phone's official spec sheet.

This guide is based on Apple, Microsoft, Intel, NETGEAR, TP-Link and Wi-Fi Alliance documentation. It's worth checking before you pay extra for a router with 6 GHz, because a 6 GHz radio does nothing for devices that can't connect to it.

## The short rule: Wi-Fi 6E or Wi-Fi 7

The Wi-Fi Alliance describes Wi-Fi 6E devices as ones that "extend the benefits that Wi-Fi 6 already provides in the 2.4 and 5 GHz bands to 6 GHz." The naming trips people up: "Wi-Fi 6" alone means no 6 GHz. Intel puts it bluntly: "Wi-Fi 6 (or lower) devices do not support the 6 GHz band." Intel says all its Wi-Fi 7 products support 6 GHz, but not every Wi-Fi 7 product does; some Wi-Fi 7 routers skip the band, as we explain in [Dual-Band Wi-Fi 7: What You Lose Without 6 GHz]({{< relref "/guides/dual-band-wifi-7" >}}).

Hardware is only the first requirement. The operating system, driver and your country's rules also have to allow it. In the US, the Wi-Fi Alliance notes, the FCC "approved use of 1200 MHz in the 6 GHz band for unlicensed technologies."

## iPhone and iPad

Apple's support article "Use Wi-Fi 6E networks with Apple devices" (published October 27, 2026) lists which models can join Wi-Fi 6E or Wi-Fi 7 networks:

| Device | Supports 6 GHz (per Apple) | Not supported |
|---|---|---|
| iPhone | iPhone 15 Pro, iPhone 15 Pro Max or later; iPhone Duo | iPhone 15, iPhone 15 Plus, iPhone 16e, iPhone 17e, and anything older than iPhone 15 Pro |
| iPad | iPad Pro 11-inch (4th generation), iPad Pro 12.9-inch (6th generation) or later; iPad Air with M2 or later; iPad mini with A17 Pro or later | Earlier iPad Pro, Air and mini models; Apple doesn't list the standard iPad |
| Mac | MacBook Pro, iMac, Mac mini, Mac Studio and Mac Pro introduced in 2023 or later; MacBook Air with M3 or later; MacBook Neo | MacBook Air with M2 or earlier; older Macs |
| Other | Apple TV 4K (4th generation) or later; HomePod mini 2 or later; HomeView | Earlier models |

Use that support article as the source of truth. Apple's separate Wi-Fi specifications table in its deployment guide isn't consistent for iPhone 15: it shows the model with and without a 6 GHz row in different places, while the support article excludes it.

**How to check on the device:** Apple says a "Wi-Fi 6E mode" setting appears in your network's details in Wi-Fi settings, and only "when your supported device is connected to a Wi-Fi 6E or Wi-Fi 7 network." Seeing the setting tells you the device supports 6 GHz and has joined a Wi-Fi 6E or Wi-Fi 7 network. If you don't see it while connected to a 6 GHz-capable router, either your device isn't on Apple's list or the router's 6 GHz band isn't on.

To find your model, go to Settings > General > About on iPhone or iPad, or Apple menu > About This Mac.

## Mac

The model list is in the table above. Apple's deployment guide shows the difference within one product line: the M2 MacBook Air tops out at 802.11ax on 5 GHz with no 6 GHz entry, while the M3 MacBook Air adds an "ax@6 GHz" row. So two MacBook Airs that look the same can differ here.

## Windows PCs

A Windows PC needs three things: Windows 11, a Wi-Fi 6E or Wi-Fi 7 adapter, and an up-to-date driver.

**Windows 10 won't work.** NETGEAR's support article says "Microsoft recently announced that they are not backporting 6 GHz support to Windows 10," so "if your PC uses Windows 10, you can't use 6 GHz WiFi until you upgrade to Windows 11." Intel's requirements also call for "Microsoft Windows 11, including the latest updates."

**Step 1: check the adapter.** Microsoft's support page says to open Command Prompt or Terminal, type `netsh wlan show drivers`, and look at "Radio types supported." An `802.11ax` entry means Wi-Fi 6 or 6E, so it doesn't settle 6 GHz by itself. Note the adapter name at the top of the output and look it up on the maker's site. Intel says "all Intel Wi-Fi 6E (Gig+) and Intel Wi-Fi 7 products support the new 6 GHz band"; its AX210 is a Wi-Fi 6E model.

**Step 2: update the driver.** Intel lists driver version 22.70.0 or later for its Wi-Fi 6E adapters and 23.10.0 or later for Wi-Fi 7. Wi-Fi 7 features also need Windows 11 version 24H2 or later, according to both Intel and Microsoft.

**Step 3: check the band you're actually on.** Microsoft's path is Settings > Network & internet > Wi-Fi > your network's properties, then look at "Network band (channel)." If it says 6 GHz, you're connected on 6 GHz. Microsoft says that if it lists two bands, such as 5 GHz and 6 GHz, MLO (Multi-Link Operation) is supported on that connection; our [Wi-Fi 7 MLO guide]({{< relref "/guides/wifi-7-mlo" >}}) explains what that means.

**If the card supports 6E but you still can't see the network:** Intel says to confirm with the PC maker, because the band may not be enabled on every platform, and a card you installed yourself should be one your system maker has "validated and approved."

## Android phones and tablets

There's no single list for Android, and settings menus vary by phone maker. The reliable check is your exact model's official spec sheet from the manufacturer: look for "Wi-Fi 6E" or "Wi-Fi 7" together with 6 GHz. TP-Link's support article gives a rough rule of thumb: "Client devices manufactured before 2020 likely don't support 6GHz Wi-Fi." If your spec sheet doesn't say, ask the device maker.

## Still can't connect? Check the region and the router

- **Region:** TP-Link notes that "regulators in some regions have not approved the 6 GHz band," and Apple says 6 GHz features "are not available in all regions." Apple also says Wi-Fi 6E isn't available in mainland China. A device sold for another region may have 6 GHz disabled or limited.
- **Router:** your router has to broadcast a 6 GHz network. Some combine all bands under one name, so you may not see a separate "6G" network. Our [2.4 GHz vs. 5 GHz vs. 6 GHz guide]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}}) explains when 6 GHz helps, and [Wi-Fi 6 vs. Wi-Fi 6E]({{< relref "/guides/wifi-6-vs-wifi-6e" >}}) covers whether it's worth paying for.

## Is it worth buying a 6 GHz router?

Count your 6 GHz-capable devices first. If only one phone qualifies, a 6 GHz router mostly helps that phone. If your main laptop, phone and streaming box all qualify, and they sit within range of the router (6 GHz generally has shorter range than 5 GHz), a 6 GHz router is more likely to pay off.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Apple model list for 6E/7, exclusions, Wi-Fi 6E mode setting, regional note | [Apple Support](https://support.apple.com/102285) | Verified |
| iPhone 15 inconsistency; M2 vs. M3 MacBook Air rows; mainland China note | [Apple Platform Deployment](https://support.apple.com/guide/deployment/dep268652e6c) | Verified |
| `netsh wlan show drivers` check; Network band (channel) path; MLO note; Wi-Fi 7 from Windows 11 24H2 | [Microsoft Support](https://support.microsoft.com/topic/26177a28-38ed-1a8e-7eca-66f24dc63f09) | Verified |
| No 6 GHz on Windows 10; Windows 11 required | [NETGEAR](https://kb.netgear.com/000064414/Does-my-Microsoft-Windows-PC-support-6-GHz-WiFi) | Qualified (NETGEAR reporting Microsoft's position) |
| All Intel Wi-Fi 6E and Wi-Fi 7 products support 6 GHz; driver versions; OEM enablement | [Intel](https://www.intel.com/content/www/us/en/support/articles/000059385.html) | Verified |
| Wi-Fi 6 or lower can't use 6 GHz; OEM validation for self-installed cards | [Intel](https://www.intel.com/content/www/us/en/support/articles/000087538.html) | Verified |
| Pre-2020 devices likely lack 6 GHz; regional approval | [TP-Link](https://www.tp-link.com/uk/support/faq/3092) | Verified |
| Wi-Fi 6E definition; FCC approved 1,200 MHz | [Wi-Fi Alliance](https://www.wi-fi.org/node/37285) | Verified |
