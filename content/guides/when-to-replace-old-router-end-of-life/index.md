---
title: "Is Your Router Too Old? What End-of-Life Means and When to Replace It"
date: 2026-10-11
description: "An end-of-life router no longer gets security fixes. Here is what the FBI warned in May 2025, how to check your model, and what to do while you decide."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "routers"]
tags: ["end-of-life", "firmware", "router-security", "router-replacement", "fbi", "router-buying"]
summary: "Replace a router when its maker stops releasing security updates for it, not when it hits a certain age. The FBI warned on May 7, 2025 that end-of-life routers are being compromised, especially with remote administration on. Check your model's support page, install the newest firmware, and turn off remote management now. If the maker lists the model as end of life or end of service, plan to replace it. This is a research-based guide, not a hands-on test, and no source we found sets a universal age limit."
takeaways:
  - "End of life (EOL), also called end of service (EOS), means the maker no longer actively supports the model, including security updates."
  - "The FBI's May 7, 2025 alert said end-of-life routers were being compromised by a malware variant, and named turning off remote administration and replacing the device as protections."
  - "There is no universal age at which a router becomes unsafe. The FBI alert says routers dated 2010 or earlier likely no longer receive updates. For newer models, the maker's support page decides."
  - "Wi-Fi speed is not a security reason to upgrade. Missing security updates are."
faq:
  - q: "How long do routers get security updates?"
    a: "It depends on the maker and model. The vendor pages we were able to read did not state a fixed support period. Check the support page for your exact model and hardware version."
  - q: "How do I know if my router is end of life?"
    a: "Find the model and hardware version on the label under the router. Search the manufacturer's support site for that model plus 'end of life' or 'end of service'. Then check whether new firmware has been released for it recently. If your internet provider supplied the router, ask the provider, since we haven't verified how each provider handles updates."
  - q: "Is an old router a risk if it works fine?"
    a: "It can be. A router that works can still have unpatched flaws. The FBI alert says some end-of-life routers with remote administration turned on were found compromised, and it lists changed settings, overheating and connectivity problems as warning signs."
  - q: "Can I keep using an end-of-life router?"
    a: "Treat that as temporary. Vendors who comment on this advise replacing it. If you must keep it for now, update to the last firmware, turn off remote management and internet-facing services, and use a strong admin password."
  - q: "Do I need Wi-Fi 7 to be secure?"
    a: "No. Security comes from a supported device that receives updates, plus sound settings. A current-generation router that is supported is safer than a faster one that is not."
sources:
  - title: "End-of-Life Routers Are Being Targeted by Cyber Actors (Alert I-050725-PSA)"
    publisher: "FBI Internet Crime Complaint Center (IC3)"
    url: "https://www.ic3.gov/PSA/2025/PSA250507"
    date: 2025-05-07
  - title: "Home Network Security"
    publisher: "Cybersecurity and Infrastructure Security Agency (CISA)"
    url: "https://www.cisa.gov/news-events/news/home-network-security"
    date: 2021-02-01
  - title: "Critical Vulnerability in ASUS AiCloud Routers (AL-2025-111)"
    publisher: "Cyber Security Agency of Singapore"
    url: "https://www.csa.gov.sg/alerts-and-advisories/alerts/al-2025-111/"
    date: 2025-11-28
  - title: "TP-Link support notice for End of Service models (Archer C7(EU) V2, TL-WR841N(MS) V9, TL-WR841ND(MS) V9)"
    publisher: "TP-Link Support"
    url: "https://www.tp-link.com/us/support/faq/4308/"
    date: 2024-11-09
---

Replace a router when its maker stops releasing security updates for it, not when it reaches a certain age. A router that has reached **end of life** (EOL, also called **end of service** or EOS) is one the manufacturer no longer actively supports, which includes security updates. Any flaw found afterward stays unfixed. If your model is listed as EOL, or you can't find an update from the past few years, plan to replace it.

This guide is built from a federal alert, a federal guidance page and vendor notices. We have not tested routers for this article, and no source we found sets one age at which every router becomes unsafe.

## What did the FBI warn about?

On May 7, 2025, the FBI's Internet Crime Complaint Center (IC3) published alert I-050725-PSA about end-of-life routers. According to the alert:

- Cyber actors were using a new variant of **TheMoon**, a botnet (a network of hacked devices) first seen on compromised routers in 2014. The variant installs proxies on victim routers, which, as we read it, can let others route their traffic through your connection.
- The alert says end-of-life routers dated 2010 or earlier likely no longer receive manufacturer software updates, and that some of those with remote administration turned on were found compromised.
- The FBI's advice: replace end-of-life devices with an updated model if possible, apply available security patches and firmware updates immediately, and turn off remote management, save the change and reboot the router.
- It also recommends a long, unique, random password (16 to 64 characters), and lists warning signs including overheating, connectivity problems and changes to settings the administrator does not recognize.
- If you suspect compromise: update the device, change passwords, reboot, and report it to IC3 at ic3.gov.

The alert does not name router makers or models. It describes what happens to devices whose makers have stopped updating them, not a defect in one brand. It is also from May 2025, so it tells you what the FBI saw then, not a count of today's compromised routers.

## Why do missing updates matter?

CISA, the US cybersecurity agency, says on its Home Network Security page (released February 1, 2021) that firmware updates "enhance product performance, fix flaws, and address security vulnerabilities," and that some routers can update automatically. The reverse is the point here: when a model stops getting updates, newly found flaws are never fixed. Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) covers the settings that reduce the risk while a router is still supported.

Two recent examples show what vendors and agencies say about this:

- **TP-Link, November 2024.** A TP-Link support notice covering the Archer C7(EU) V2, TL-WR841N(MS) V9 and TL-WR841ND(MS) V9 says those products reached End of Service and no longer receive active support, including security updates. TP-Link still released patched firmware for them, urged users to install it, advised using the Tether app instead of remote management, and recommended upgrading to newer hardware. That is a notable case: a vendor patched models it no longer supports, but a user can't count on that happening.
- **ASUS AiCloud, November 28, 2025.** Singapore's Cyber Security Agency published alert AL-2025-111 about CVE-2025-59366, a critical flaw (CVSSv4.0 score 9.2 out of 10) in AiCloud, ASUS's remote-access feature, affecting several firmware series. For routers that are end of life, the agency advised upgrading to a supported router and, as a precaution, turning off internet-accessible services including AiCloud, WAN remote access, port forwarding, DDNS (dynamic DNS), VPN server, DMZ, port triggering and FTP. This is a Singapore agency's alert about a flaw in ASUS's feature, and the page doesn't name models.

## How do you check whether your router is end of life?

1. **Find the model and hardware version** on the label on the bottom or back. Some makers list different support for different hardware versions, such as V2 and V9 in the TP-Link notice.
2. **Search the maker's support site** for your model plus "end of life" or "end of service."
3. **Check the firmware download page.** Look at the date of the newest firmware. We don't know of a rule for how old is too old, but a model with no new firmware for years and a newer successor on sale is a warning sign.
4. **Install the latest firmware** now, whatever you decide.
5. **Look at the settings.** Turn off remote management (also called remote access or remote administration), and any service you don't use that is reachable from the internet. Watch for settings you didn't change.
6. **If your internet provider supplied the router**, ask the provider whether it updates and replaces the unit. We haven't verified each provider's policy.

We looked for a stated support period in the vendor pages we could read and did not find a general one. Don't assume a number of years. Look up your model.

## Replace now, soon, or later?

| Your situation | What it suggests | Why |
|---|---|---|
| Maker lists the model as EOL or EOS | Replace, and secure it in the meantime | The maker isn't actively supporting it, so new flaws stay unfixed |
| Newest firmware is years old and the model has a successor on sale | Treat as likely unsupported; confirm with the maker, then plan to replace | A warning sign, not proof |
| Maker is still releasing firmware, or the router updates automatically | Keep it | It is supported |
| Router is slow but supported | Fix speed separately | See [why Wi-Fi is slow when the internet is fast]({{< relref "/guides/wifi-slow-but-internet-fast" >}}) |
| Provider-supplied gateway | Ask the provider | We can't tell you its policy |

## What should you look for in the replacement?

- **A published support or update commitment.** Prefer a maker that states how long it will provide security updates for the model. Not every maker does.
- **Automatic updates.** Check the product page or app for an automatic update option. CISA notes that some routers offer one. For single-router or mesh choices, see our [router vs. mesh guide]({{< relref "/guides/wifi-router-vs-mesh" >}}).
- **The Wi-Fi standard is a secondary question.** A faster standard doesn't make a router safer. If you're also weighing speed, see our [Wi-Fi 6E vs. Wi-Fi 7 guide]({{< relref "/guides/wifi-6e-vs-wifi-7" >}}). Set WPA3 or WPA2 with AES as in our [WPA2 vs. WPA3 guide]({{< relref "/guides/wpa2-vs-wpa3" >}}).

We do not list prices here. We only publish a price with the date we checked it.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| The FBI published alert I-050725-PSA on May 7, 2025 about TheMoon malware variants targeting end-of-life routers, and advised replacing them, updating firmware and turning off remote administration | [FBI IC3 alert](https://www.ic3.gov/PSA/2025/PSA250507) | Qualified: describes activity as of May 2025 and names no makers or models |
| The alert says routers dated 2010 or earlier likely no longer receive updates | [FBI IC3 alert](https://www.ic3.gov/PSA/2025/PSA250507) | Qualified: "likely," and a statement about 2010-or-earlier devices only |
| CISA's Home Network Security page (February 1, 2021) says to check the maker's site for the latest firmware and that some routers update automatically | [CISA](https://www.cisa.gov/news-events/news/home-network-security) | Qualified: page is from 2021 |
| TP-Link says three named models reached End of Service and no longer receive active support including security updates, yet released patched firmware and recommended upgrading | [TP-Link notice, updated November 2024](https://www.tp-link.com/us/support/faq/4308/) | Qualified: applies to the named models only; page date format is ambiguous but firmware is dated November 8, 2024 |
| Singapore's CSA alert AL-2025-111 (November 28, 2025) concerns CVE-2025-59366 (CVSSv4.0 9.2) in ASUS AiCloud and advises EOL users to move to a supported router and disable internet-facing services | [CSA alert](https://www.csa.gov.sg/alerts-and-advisories/alerts/al-2025-111/) | Qualified: a Singapore agency's alert; no models named on the page |
| There is no universal age at which a router becomes unsafe | Our analysis of the sources above | Qualified: an editorial conclusion from what the sources do and do not say |

## Bottom line

Don't ask how old your router is. Ask whether its maker still updates it. Look up the exact model, install the newest firmware, and turn off remote management today. If the model is end of life or the updates have clearly stopped, replace it with a router from a maker that states how long it will support it.
