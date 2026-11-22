---
title: "What DOCSIS Version Is My Modem? How to Check"
date: 2026-11-22T05:00:00Z
description: "What DOCSIS version is my modem? Read the model number on the label, then check the maker's spec page. Steps for NETGEAR, ARRIS SURFboard and Xfinity."
authors: ["Tehseen Arbab"]
topics: ["internet-plans-isps", "how-to-fixes"]
tags: ["docsis", "docsis-3-1", "docsis-3-0", "cable-modem", "netgear", "arris", "surfboard", "xfinity"]
summary: "The fastest way to check your modem's DOCSIS version is to read the model number on the label on the bottom or back of the modem, then look that model up on the maker's spec page. The modem's status page at 192.168.100.1 and your provider's device lookup (Xfinity calls it My Device Info) are the backup checks."
imageAlt: "Rack-mounted network units with rows of capped round RF connectors and red indicator lights"
imageCredit: "Photo: Valentin Lacoste / [Unsplash](https://unsplash.com/photos/server-rack-filled-with-network-and-electronic-equipment-UpkcO_xS5k0)"
takeaways:
  - "Read the model number on the modem's label, not the retail box: NETGEAR says box numbers 'might not be device specific.' ARRIS says SURFboard labels are on the bottom or back."
  - "Search the exact model number on the maker's site. The spec sheet names the DOCSIS version: the SURFboard S34 page lists 'DOCSIS Technology | DOCSIS 3.1,' and the NETGEAR CM3000 data sheet names DOCSIS 3.1."
  - "NETGEAR cable modems and the ARRIS SURFboard SB8200 and S33 open a status page at http://192.168.100.1. NETGEAR's default login is admin / password; on the SURFboard SB8200 the password is 'password' or the last 8 digits of the serial number."
  - "A channel count like 32x8 doesn't prove DOCSIS 3.0 on its own: DOCSIS 3.1 modems list the same 32x8 channels plus separate OFDM / OFDMA channels."
  - "If it turns out to be DOCSIS 3.0, NETGEAR lists 1 Gbps down and 200 Mbps up as the standard's not-guaranteed maximum. For a gigabit plan, look at a DOCSIS 3.1 modem your provider lists."
faq:
  - q: "What DOCSIS is my modem?"
    a: "Find the model number on the label on the bottom or back of the modem, then search that exact model on the maker's website. The spec page lists the DOCSIS version. Don't rely on the retail box: NETGEAR says box numbers might not be device specific."
  - q: "How do I check DOCSIS version on 192.168.100.1?"
    a: "Type http://192.168.100.1 into a browser on a device connected to the modem. On NETGEAR modems, log in with admin and the default password password, then open Cable Connection. If the page lists OFDM or OFDMA channels, that points to a DOCSIS 3.1 modem. If it doesn't, check the model's spec sheet, because status pages differ by model."
  - q: "Is my modem DOCSIS 3.0 if it says 32x8?"
    a: "Not necessarily. 32x8 is a channel count. DOCSIS 3.1 modems such as the ARRIS SURFboard S34 and NETGEAR CM3000 also list 32 downstream x 8 upstream channels, plus two OFDM downstream and two OFDMA upstream channels. Check the spec sheet for the word DOCSIS 3.1."
  - q: "Does Xfinity tell me my modem's DOCSIS version?"
    a: "Xfinity's approved-modem page doesn't mention DOCSIS. It points you to My Device Info, where you sign in or enter your address to see whether your device works with your service. Xfinity says your modem must work with Xfinity and support your internet speed."
  - q: "Do I need to replace a DOCSIS 3.0 modem?"
    a: "Only if your provider no longer supports it or your plan is near its limits. NETGEAR gives DOCSIS 3.0's maximum as 1 Gbps down and 200 Mbps up, and says those maximums are not guaranteed. On a gigabit plan or faster, a DOCSIS 3.1 modem your provider lists is the usual upgrade."
sources:
  - title: "How can I find my NETGEAR device's model number?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/10727/How-can-I-find-my-NETGEAR-device-s-model-number?article=10727"
    date: 2025-07-07
  - title: "How to Find the Model and Serial Number"
    publisher: "ARRIS / SURFboard (Vantiva) Consumer Support"
    url: "https://arris.my.salesforce-sites.com/consumers/kA5Qi0000003RgdKAE"
  - title: "How do I obtain the cable connection information from a NETGEAR cable modem or modem router?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/30007/How-do-I-obtain-the-cable-connection-information-from-a-NETGEAR-cable-modem-modem-router"
    date: 2025-07-07
  - title: "How do I view the firmware version of my cable modem or modem router?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/25477/How-do-I-view-the-firmware-version-of-my-cable-modem-or-modem-router"
    date: 2025-07-07
  - title: "SB8200 Web Manager Access"
    publisher: "ARRIS / SURFboard (Vantiva) Consumer Support"
    url: "https://arris.secure.force.com/consumers/articles/General_FAQs/SB8200-Web-Manager-Access"
  - title: "S33 Device Status"
    publisher: "ARRIS / SURFboard (Vantiva) Consumer Support"
    url: "https://arris.secure.force.com/consumers/articles/General_FAQs/S33-Device-Status"
  - title: "Approved cable modems"
    publisher: "Xfinity"
    url: "https://www.xfinity.com/support/articles/list-of-approved-cable-modems"
    date: 2026-09-02
  - title: "What is the difference between DOCSIS 3.0 and 3.1?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/000060401/What-is-the-difference-between-DOCSIS-3-0-and-3-1"
    date: 2025-07-07
  - title: "DOCSIS 3.1 modems built for the fastest ISP speeds"
    publisher: "NETGEAR"
    url: "https://www.netgear.com/home/wifi/modems/docsis31/"
  - title: "DOCSIS 4.0 Technology"
    publisher: "CableLabs"
    url: "https://www.cablelabs.com/technologies/docsis-4-0-technology"
    date: 2026-10-27
  - title: "S34 SURFboard DOCSIS 3.1 Cable Modem"
    publisher: "SURFboard (Vantiva)"
    url: "https://www.surfboard.com/products/cable-modems/S34/"
  - title: "Nighthawk CM3000 data sheet"
    publisher: "NETGEAR"
    url: "https://www.downloads.netgear.com/files/GDC/CM3000/CM3000_TS.pdf"
---

The fastest way to find your modem's DOCSIS version is to read the model number on the label on the bottom or back of the modem, then search that exact model on the maker's website: the spec page states "DOCSIS 3.0" or "DOCSIS 3.1." If the label is worn or the spec page is gone, open the modem's status page at http://192.168.100.1, or check the model with your provider's device lookup (Xfinity's is called My Device Info).

This guide is based on NETGEAR and ARRIS SURFboard support articles, maker spec sheets, CableLabs and Xfinity's support documentation. It applies to cable modems and cable gateways.

## What DOCSIS version is my modem? Four ways to check

| Method | What you need | What it tells you |
|---|---|---|
| 1. Model number on the label | The modem in front of you | The exact model and version suffix (not the box) |
| 2. Maker's spec page for that model | The model number | The DOCSIS version, stated on the spec sheet |
| 3. Modem status page (192.168.100.1) | A device connected to the modem | OFDM / OFDMA channel rows, if the page shows channel types |
| 4. Your provider's device lookup | Your provider account or address | Whether the modem works with your plan; Xfinity's page doesn't mention DOCSIS |

### 1. Read the model number on the label

1. Turn the modem over or look at the back panel. ARRIS says SURFboard model and serial numbers "are located on the label on the bottom or back of the device." NETGEAR says its model number and version number "are printed on the product label."
2. Write down the full model, including any version suffix. NETGEAR says the model number and version number are "always used together."
3. Ignore the box. NETGEAR's advice: "Do not use numbers printed on retail boxes because these numbers might not be device specific."

An ARRIS support article says SURFboard model numbers begin with "G", "SB", "SBG", "SBR", "SVG", "S33", "TG", "TM" or "W". That list doesn't include every current model, such as the S34.

### 2. Look up the exact model on the maker's spec page

Search the model number plus the maker's name and open the official product page or data sheet. Both makers state the version plainly in their specs. The ARRIS SURFboard S34 page lists "DOCSIS Technology | DOCSIS 3.1," and the NETGEAR CM3000 data sheet calls it "Engineered for Today's Fastest DOCSIS 3.1 Cable Internet Speeds."

Don't assume that similar model numbers share a DOCSIS version. Check the exact model and version suffix from the label.

### 3. Check the modem's status page at 192.168.100.1

1. Connect a computer or phone to the modem, either by Ethernet or through the Wi-Fi router plugged into it.
2. Type **http://192.168.100.1** into the browser's address bar. NETGEAR documents this address for its cable modems, and ARRIS documents it for the SURFboard SB8200 and S33.
3. Log in if asked:
   - **NETGEAR:** NETGEAR says "The user name is admin. The default password is password." Select **Cable Connection** to see the cable connection information, or **ADVANCED** to see the firmware version.
   - **ARRIS SURFboard SB8200:** ARRIS gives the default user name as admin and the password as "password or last 8 digit of the serial number." The **Status** page "Provides the current operational status of the cable modem."
   - **ARRIS SURFboard S33:** click **Device Status**. ARRIS says it shows the "firmware version and Internet connection status."
4. Look for **OFDM** (download) or **OFDMA** (upload) channel rows. NETGEAR describes DOCSIS 3.1 as using "OFDM channel technology," and SURFboard's S34 spec sheet labels its OFDM channels "DOCSIS 3.1 channels." In our reading, OFDM rows on the status page point to a DOCSIS 3.1 modem.

If you don't see OFDM rows, that alone doesn't prove the modem is DOCSIS 3.0. Status pages differ by model: ARRIS describes the S33's Device Status page as showing "firmware version and Internet connection status," not channel types. Go back to methods 1 and 2.

If the default login doesn't work, don't reset the modem just to read its status page; the label and spec page give you the answer without changing anything. If you do need a reset, check your model's manual first, and see our [router reset guide](/guides/reset-router/) for how resets work.

### 4. Check with your cable provider

Your provider's lookup answers a different question: does this modem work on your plan? Xfinity says: "Your modem must work with Xfinity and support your internet speed." Its approved-modem page sends you to **My Device Info**, where you "Sign in for personalized results" or, "If you don't sign in, enter your address." For gigabit plans, Xfinity adds: "Your device must support Gigabit speeds."

Xfinity's page doesn't mention DOCSIS versions, so use it to confirm compatibility and the maker's spec page to confirm the version. For other providers, use their own approved-device list.

## Why "32x8" doesn't tell you the DOCSIS version

A channel count such as 32x8 (32 download channels, 8 upload channels) also appears on DOCSIS 3.1 modems, so on its own it isn't proof of DOCSIS 3.0. The ARRIS SURFboard S34, a DOCSIS 3.1 modem, lists "32 downstream x 8 upstream DOCSIS 3.0 bonded channels" alongside "2 downstream x 2 upstream OFDM DOCSIS 3.1 channels." NETGEAR's CM3000 data sheet lists "32 downstream and 8 upstream SC-QAM channels" plus "2 OFDM Downstream channels and 2 OFDMA Upstream channels."

The tell is the OFDM / OFDMA line or the words "DOCSIS 3.1" on the spec sheet. A spec sheet that lists only an SC-QAM channel count such as 32x8 and no OFDM channels points to a DOCSIS 3.0 modem, but confirm the version line before you buy a replacement.

## What your DOCSIS version means for your plan

| Version | Maximum download | Maximum upload | What it means for you |
|---|---|---|---|
| DOCSIS 3.0 | 1 Gbps | 200 Mbps | No headroom on a gigabit plan; check your provider still supports it |
| DOCSIS 3.1 | 10 Gbps | 1 Gbps | Headroom above 1 Gbps; the modem's own ports and your provider's list set the real limit |
| DOCSIS 4.0 | Up to 10 Gbps | Up to 6 Gbps | Specification maximums; you only need it if your provider offers DOCSIS 4.0 service |

DOCSIS 3.0 and 3.1 figures are from NETGEAR, which says they "are maximum speeds and are not guaranteed." DOCSIS 4.0 figures are from CableLabs, which says its numbers "are based on specifications; deployed network performance will vary across implementations." Your plan, the provider's network and the modem's own ports set the real ceiling: a single 1 Gbps Ethernet port can't pass more than 1 Gbps, whatever the modem's DOCSIS version. For the full comparison, see our [DOCSIS 3.0 vs. 3.1 vs. 4.0 guide](/guides/docsis-3-0-vs-3-1-vs-4-0-cable-modem/).

## My modem is DOCSIS 3.0. What next?

1. **Compare it with your plan.** If your plan is well below 1 Gbps down and your provider still lists the modem, you don't have to replace it. NETGEAR says a DOCSIS 3.1 modem "is backward compatible, so it works on your current plan," so a DOCSIS 3.1 modem your provider lists will also work on your current plan.
2. **Check that your provider still supports the model.** At Xfinity, use My Device Info.
3. **If you upgrade, buy a model your provider lists.** Our [best modem for Xfinity guide](/guides/best-modem-for-xfinity/) covers current DOCSIS 3.1 options, and [NETGEAR CM3000 vs. ARRIS S34](/guides/netgear-cm3000-vs-arris-s34/) compares two 2.5 Gbps models.
4. **Decide whether owning makes sense.** Our guide on [whether to buy your own modem](/guides/should-i-buy-my-own-modem/) covers rental fees, voice service and support.
5. **Check your router too.** A new modem won't fix slow Wi-Fi. On a plan faster than 1 Gbps, your router needs a 2.5 Gbps (or faster) WAN port to match a modem's 2.5 Gbps port; for large homes, see our [best Wi-Fi router for a large house guide](/guides/best-wifi-router-for-large-house/). Not sure which box does what? Read [modem vs. router vs. gateway](/guides/modem-vs-router-vs-gateway/).

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| NETGEAR model and version number are on the product label; don't use box numbers | [NETGEAR KB 10727, updated July 7, 2025](https://kb.netgear.com/10727/How-can-I-find-my-NETGEAR-device-s-model-number?article=10727) | Verified |
| SURFboard model and serial number are on the label on the bottom or back; model number prefixes | [ARRIS consumer support](https://arris.my.salesforce-sites.com/consumers/kA5Qi0000003RgdKAE) | Verified (undated) |
| NETGEAR status page at http://192.168.100.1; admin / password; Cable Connection; ADVANCED shows firmware | [NETGEAR KB 30007](https://kb.netgear.com/30007/How-do-I-obtain-the-cable-connection-information-from-a-NETGEAR-cable-modem-modem-router) and [KB 25477](https://kb.netgear.com/25477/How-do-I-view-the-firmware-version-of-my-cable-modem-or-modem-router), updated July 7, 2025 | Verified |
| SB8200 and S33 address; SB8200 default login and Status page; S33 Device Status contents | [SB8200 Web Manager Access](https://arris.secure.force.com/consumers/articles/General_FAQs/SB8200-Web-Manager-Access), [S33 Device Status](https://arris.secure.force.com/consumers/articles/General_FAQs/S33-Device-Status) | Verified (undated; model-specific) |
| Xfinity: modem must work with Xfinity and support your speed; My Device Info by sign-in or address; Gigabit devices must support Gigabit | [Xfinity, modified Sept. 2, 2026](https://www.xfinity.com/support/articles/list-of-approved-cable-modems) | Verified |
| DOCSIS 3.0: 1 Gbps / 200 Mbps; DOCSIS 3.1: 10 Gbps / 1 Gbps; not guaranteed | [NETGEAR KB 000060401, updated July 7, 2025](https://kb.netgear.com/000060401/What-is-the-difference-between-DOCSIS-3-0-and-3-1) | Verified |
| DOCSIS 3.1 uses OFDM; backward compatible | [NETGEAR DOCSIS 3.1 page](https://www.netgear.com/home/wifi/modems/docsis31/) | Verified (undated) |
| DOCSIS 4.0: up to 10 Gbps down, 6 Gbps up; specification figures | [CableLabs](https://www.cablelabs.com/technologies/docsis-4-0-technology) | Verified |
| S34 and CM3000 list 32x8 channels plus 2x2 OFDM / OFDMA | [SURFboard S34](https://www.surfboard.com/products/cable-modems/S34/), [CM3000 data sheet](https://www.downloads.netgear.com/files/GDC/CM3000/CM3000_TS.pdf) | Verified |
| OFDM rows on a status page indicate DOCSIS 3.1; missing rows don't prove 3.0 | Our reading of the NETGEAR and ARRIS pages above | Qualified (status pages vary by model) |
