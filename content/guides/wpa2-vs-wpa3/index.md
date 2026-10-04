---
title: "WPA2 vs. WPA3: Which Wi-Fi Security Setting Should You Use?"
date: 2026-10-04
description: "WPA3 protects your Wi-Fi password better than WPA2, but older devices may not connect. Here is which router setting to pick and when."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "how-to-fixes"]
tags: ["wpa3", "wpa2", "router-security", "wifi-password", "6-ghz"]
summary: "Use WPA3 Personal if every device you own can connect with it. If some can't, use the WPA2/WPA3 transitional (mixed) mode. Use WPA2 Personal with AES only when your router offers nothing newer. Avoid WEP, the original WPA and anything labeled TKIP. Whichever mode you use, a long passphrase and current firmware matter as much as the setting."
imageAlt: "Silver combination padlock resting on a white computer keyboard"
imageCredit: "Photo: Sasun Bughdaryan / [Unsplash](https://unsplash.com/photos/QP7RBa5r8HM)"
takeaways:
  - "WPA3 Personal replaces WPA2's password handshake with one called SAE, which the Wi-Fi Alliance says gives stronger protection against password guessing, even when the password is weak."
  - "Apple recommends WPA3 Personal first, then WPA2/WPA3 Transitional, then WPA2 Personal (AES). It advises against WPA/WPA2 mixed modes, WPA, WEP and TKIP."
  - "The 6 GHz band requires WPA3. If a Wi-Fi 6E or Wi-Fi 7 router's 6 GHz network won't appear, the security mode is the first thing to check."
  - "The NSA's home network guidance says to use WPA3, or WPA2/3 if some devices don't support it, with a passphrase of at least 20 characters."
faq:
  - q: "Is WPA3 better than WPA2?"
    a: "Yes. WPA3 Personal uses a handshake called SAE that the Wi-Fi Alliance says gives stronger protection against password guessing than WPA2. Cisco's documentation adds that SAE protects against offline dictionary attacks and provides forward secrecy."
  - q: "Is WPA2 still safe to use in 2026?"
    a: "WPA2 Personal with AES is still on Apple's list of acceptable settings, for cases where a more secure mode isn't possible. It depends more on a long, unique password than WPA3 does, and your devices need current updates to be protected against the 2017 KRACK attack."
  - q: "What is WPA2/WPA3 transitional or mixed mode?"
    a: "It is a router setting that lets newer devices connect with WPA3 while older devices connect with WPA2 on the same network name. Apple and the NSA both list it as the option to use when some devices don't support WPA3."
  - q: "Why won't an old device connect after I switch to WPA3?"
    a: "It probably doesn't support WPA3. Switch the router to WPA2/WPA3 transitional mode, or put the old device on a separate guest or smart-home network that uses WPA2 with AES."
  - q: "Do I need WPA3 for Wi-Fi 6E or Wi-Fi 7?"
    a: "For the 6 GHz band, yes. Cisco's WPA3 documentation states that WPA3 is mandatory for devices operating in 6 GHz and that WPA2 is not permitted there. Wi-Fi 7's Multi-Link Operation also requires WPA3-level security."
sources:
  - title: "Wi-Fi Alliance introduces Wi-Fi CERTIFIED WPA3 security"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-wpa3-security"
    date: 2018-06-25
  - title: "Security"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/discover-wi-fi/security"
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102766"
    date: 2026-07-14
  - title: "Best Practices for Securing Your Home Network"
    publisher: "National Security Agency"
    url: "https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF"
    date: 2023-02-22
  - title: "WPA3 Deployment Guide"
    publisher: "Cisco"
    url: "https://www.cisco.com/c/en/us/products/collateral/wireless/catalyst-9100ax-access-points/wpa3-dep-guide-og.html"
    date: 2025-10-06
  - title: "Faster and more secure Wi-Fi in Windows"
    publisher: "Microsoft Support"
    url: "https://support.microsoft.com/topic/26177a28-38ed-1a8e-7eca-66f24dc63f09"
  - title: "Key Reinstallation Attacks: Breaking WPA2 by forcing nonce reuse"
    publisher: "Mathy Vanhoef, imec-DistriNet, KU Leuven"
    url: "https://www.krackattacks.com/"
  - title: "Dragonblood: Analysing WPA3's Dragonfly Handshake"
    publisher: "Mathy Vanhoef and Eyal Ronen"
    url: "https://wpa3.mathyvanhoef.com/"
---

Use WPA3 Personal if every device in your home can connect with it. If some can't, use your router's WPA2/WPA3 transitional mode, which some brands call mixed mode. Use WPA2 Personal with AES only when the router offers nothing newer. Avoid WEP, the original WPA, and any option with TKIP in its name.

WPA stands for Wi-Fi Protected Access. It is the security that scrambles traffic between your devices and your router and decides who is allowed to join. This guide covers the "Personal" versions, the ones that use a shared Wi-Fi password at home. "Enterprise" versions use individual logins and are meant for workplaces.

## What is the difference between WPA2 and WPA3?

The main difference is how each one handles your Wi-Fi password when a device joins.

With WPA2 Personal, a device and the router prove they know the password through a four-step exchange. Someone within radio range can record that exchange and then try password guesses against the recording on their own computer, as fast as their hardware allows. Security researchers describe this as a dictionary attack. A short or common password can fall to it.

WPA3 Personal replaces that exchange with one called Simultaneous Authentication of Equals (SAE). The Wi-Fi Alliance, the industry group that certifies Wi-Fi products, introduced WPA3 on June 25, 2018. It says SAE provides "stronger protections for users against password guessing attempts by third parties" and gives more resilient protection "even when users choose passwords that fall short of typical complexity recommendations."

| | WPA2 Personal (AES) | WPA3 Personal |
|---|---|---|
| Password exchange | Pre-shared key (PSK), four-way handshake | SAE |
| Offline password guessing from a recorded connection | Possible, so password strength is critical | Protected against, according to Cisco's documentation |
| Forward secrecy (old recorded traffic stays private if the password leaks later) | No | Yes, according to Cisco's documentation |
| Protected Management Frames | Not always on | Required |
| Works on the 6 GHz band | No | Yes, and it is required there |
| Older device support | Nearly universal | Needs a WPA3-capable device |

Protected Management Frames (PMF) guard the control messages that keep a device connected, which the Wi-Fi Alliance describes as protection from eavesdropping and forging.

The Wi-Fi Alliance now states that WPA3 is mandatory for Wi-Fi CERTIFIED devices, so current routers, phones and laptops that carry that certification support it.

## Which setting should I choose on my router?

Router menus use different labels, so look for the closest match.

| What you see in the router menu | Use it? | Notes |
|---|---|---|
| WPA3 Personal (sometimes "WPA3-SAE") | Yes, first choice | Apple calls it "the newest, most secure protocol currently available" |
| WPA2/WPA3 Transitional (sometimes "WPA2/WPA3 mixed") | Yes, if some devices can't use WPA3 | New devices use WPA3, old ones fall back to WPA2 |
| WPA2 Personal (AES) (sometimes "WPA2-PSK [AES]") | Only if nothing above is offered | Needs a long, unique password |
| WPA/WPA2 mixed, WPA Personal, anything with TKIP | No | Apple lists these as weak or deprecated |
| WEP | No | Apple lists every WEP variant as deprecated |
| None, Open, Unsecured | No | Anyone in range can join |

That order follows Apple's router guidance, dated July 14, 2026, which also says: "Don't create or join networks that use older, deprecated security protocols."

The National Security Agency's home network guidance, published in February 2023, gives the same advice from a different direction. It says to make sure your router "is capable of Wi-Fi Protected Access 3 (WPA3)," and that if you have devices that don't support WPA3, "you can select WPA2/3 instead."

## Is transitional mode as secure as WPA3 only?

No. It is a compromise, and a reasonable one for most homes.

In transitional mode, the router accepts both WPA2 and WPA3 connections under one network name and one password. Any device that joins with WPA2 gets WPA2's protection, not WPA3's. And because the password is shared, a weak password remains exposed to the offline guessing described above through those WPA2 connections.

There is also a known attack on the mode itself. In April 2019, researchers Mathy Vanhoef and Eyal Ronen published a set of WPA3 weaknesses they named Dragonblood. One of them was a downgrade attack: an attacker sets up a fake WPA2-only copy of a network and pushes WPA3-capable devices to try connecting to it, which captures enough to start guessing the password offline. The researchers worked with the Wi-Fi Alliance on fixes, and patches were published. Newer versions of WPA3 include a feature called Transition Disable, which Cisco describes as protection against exactly this kind of downgrade. Whether your router and devices have it depends on their firmware.

What this means in practice:

- If every device you own supports WPA3, choose WPA3 only.
- If you need transitional mode, use a long passphrase. It closes most of the gap.
- Another option is to keep your main network on WPA3 and put older devices on a guest or smart-home network that uses WPA2 with AES. The NSA guidance recommends separating your primary, guest and smart-home networks anyway.

## Is WPA2 still safe?

WPA2 Personal with AES is still acceptable when you have no better option. Apple keeps it on its recommended list for that case. Two conditions apply.

**Your password has to carry more weight.** Because WPA2 allows offline guessing, a short or reused password is the weak point. The NSA guidance says to use "a strong passphrase with a minimum length of twenty characters." Several unrelated words strung together are easy to type and hard to guess.

**Your devices need their updates.** In 2017, security researcher Mathy Vanhoef disclosed KRACK, a weakness in WPA2's four-way handshake. He wrote that the flaw was "in the Wi-Fi standard itself," so "any correct implementation of WPA2 is likely affected." It was fixed through software updates to devices and routers. His guidance at the time still stands: changing your Wi-Fi password does not fix it; installing updates does. A phone, laptop or router that stopped receiving updates before 2018 may still be exposed.

WPA3 is not flawless either, as Dragonblood showed. But the researchers who found those flaws wrote that, with vendors mitigating the attacks, WPA3 "will still be an improvement over WPA2."

## Do I need WPA3 for 6 GHz, Wi-Fi 6E and Wi-Fi 7?

Yes, for the 6 GHz band. Cisco's WPA3 deployment guide, updated October 6, 2025, states that "WPA3 is mandatory for all Wi-Fi 6E devices operating in 6 GHz band" and that "WPA2 is not permitted in 6 GHz operation." Protected Management Frames are mandatory there too. That guide is written for business networks, but the requirement comes from the Wi-Fi Alliance and applies to home routers as well.

Two practical effects:

- If you own a Wi-Fi 6E or Wi-Fi 7 router and the 6 GHz network doesn't show up, check that security is set to WPA3 or WPA2/WPA3 transitional. The 6 GHz band can't run on WPA2 alone.
- Wi-Fi 7's Multi-Link Operation, which lets a device use more than one band at once, has stricter security requirements still. According to the same Cisco guide, a device that doesn't meet them can't connect as MLO-capable.

For what those bands and features do, see our guides to [the 2.4, 5 and 6 GHz bands]({{< relref "/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi" >}}) and [Wi-Fi 6E versus Wi-Fi 7]({{< relref "/guides/wifi-6e-vs-wifi-7" >}}).

## How do I check what I'm using now?

**On a Windows 11 PC:** open Settings, go to Network & internet, then Wi-Fi, and open your network's properties. That is where Microsoft points users for connection details; look for the security type in the list. The exact wording can differ between Windows versions.

**On the router:** open the router's app or admin page and look under wireless or Wi-Fi settings for "Security," "Authentication" or "Encryption." This is also where you change it. Menu names vary by brand.

## How do I switch to WPA3 without breaking things?

1. **Update the router's firmware first.** WPA3 support and its fixes arrive through firmware.
2. **Choose WPA2/WPA3 transitional mode** and save. Most devices reconnect on their own.
3. **Check your older devices.** Printers, smart plugs, older TVs and game consoles are the usual holdouts. If something can't reconnect, "forget" the network on that device and join again.
4. **Set a long passphrase** while you are in the menu, if yours is short. You will have to re-enter it on every device, so do this once.
5. **Move to WPA3 only later,** once everything has connected reliably for a few weeks and you have confirmed each device supports it. If a device drops off, go back to transitional mode.

If a device can't connect in transitional mode either, it likely needs an old protocol such as WPA with TKIP. Don't lower the whole network's security for it. Put it on a separate guest network, or replace it.

Security mode is one setting among several. Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) covers the admin password, automatic updates, WPS and remote management.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| WPA3 was introduced on June 25, 2018; WPA3 Personal uses SAE for stronger protection against password guessing, including with weaker passwords; it works with WPA2 devices through a transitional mode | [Wi-Fi Alliance press release, June 25, 2018](https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-wpa3-security) | Verified |
| WPA3 is mandatory for Wi-Fi CERTIFIED devices, and Protected Management Frames are required for new certified devices | [Wi-Fi Alliance, Security](https://www.wi-fi.org/discover-wi-fi/security) | Verified |
| Apple recommends WPA3 Personal, then WPA2/WPA3 Transitional, then WPA2 Personal (AES), and advises against WPA/WPA2 mixed modes, WPA, WEP, TKIP and open networks | [Apple Support, July 14, 2026](https://support.apple.com/en-us/102766) | Verified |
| NSA guidance: use a WPA3-capable router, WPA2/3 if devices need it, a passphrase of at least 20 characters, and separate primary, guest and smart-home networks | [NSA, Best Practices for Securing Your Home Network, February 2023](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| SAE protects against offline dictionary attacks and provides forward secrecy | [Cisco WPA3 Deployment Guide, updated October 6, 2025](https://www.cisco.com/c/en/us/products/collateral/wireless/catalyst-9100ax-access-points/wpa3-dep-guide-og.html) | Qualified: a vendor's technical description; depends on patched, correct implementations |
| WPA3 is mandatory on the 6 GHz band and WPA2 is not permitted there; MLO requires Wi-Fi 7's security requirements | [Cisco WPA3 Deployment Guide, updated October 6, 2025](https://www.cisco.com/c/en/us/products/collateral/wireless/catalyst-9100ax-access-points/wpa3-dep-guide-og.html) | Qualified: a vendor's description of Wi-Fi Alliance requirements, written for business networks |
| KRACK (2017) affected WPA2's four-way handshake in the standard itself; it is fixed by updates, not by changing the password | [Mathy Vanhoef, krackattacks.com](https://www.krackattacks.com/) | Verified |
| The Dragonblood researchers expect WPA3 to remain an improvement over WPA2 | [Mathy Vanhoef and Eyal Ronen, Dragonblood](https://wpa3.mathyvanhoef.com/) | Qualified: the authors' stated expectation, conditional on vendors applying fixes |
| Dragonblood (April 2019) found flaws in WPA3's SAE handshake, including a downgrade attack against transitional mode; patches were published | [Mathy Vanhoef and Eyal Ronen, Dragonblood](https://wpa3.mathyvanhoef.com/) | Qualified: whether a given router or device has the fixes depends on its firmware |
| Windows 11 shows Wi-Fi connection details under Settings, Network & internet, Wi-Fi, network properties | [Microsoft Support](https://support.microsoft.com/topic/26177a28-38ed-1a8e-7eca-66f24dc63f09) | Qualified: Microsoft documents the menu path; field names can differ by Windows version |

## Bottom line

WPA3 Personal is the right setting when all your devices support it, and WPA2/WPA3 transitional mode is the right setting when they don't. Plain WPA2 with AES is a fallback, and it leans hard on a long password and updated devices. If you use the 6 GHz band, WPA3 is not optional. Pick the strongest mode your devices can all join, set a passphrase of 20 characters or more, and keep the router's firmware current.
