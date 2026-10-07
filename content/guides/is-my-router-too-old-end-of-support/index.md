---
title: "Is Your Router Too Old? How to Check Whether It Still Gets Security Updates"
date: 2026-10-07
description: "Age alone does not tell you. What matters is whether the maker still issues security updates. Here is how to check, with Netgear and eero's published policies as examples."
authors: ["Tehseen Arbab"]
topics: ["routers", "security-privacy"]
tags: ["router-security", "end-of-life", "firmware-updates", "router-replacement", "fbi", "netgear", "eero"]
summary: "A router is too old when its manufacturer has stopped issuing security updates, which the FBI calls end of life. Age is a poor shortcut: Netgear says support generally ends three years after a model's last sale date, and eero guarantees updates until at least five years from purchase or a published per-model date, whichever is later. Find your exact model and hardware version, look it up on the maker's support pages, and replace the router if updates have ended. Meanwhile, turn off remote administration and use a long, unique admin password."
imageAlt: "Linksys Wireless-G broadband router, model WRT54GS, with two black antennas and a blue front panel, on a white background"
imageCredit: "Photo: Evan-Amos / [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Linksys-Wireless-G-Router.jpg), public domain. Illustrates an older router design only; it says nothing about Linksys's current support policy."
takeaways:
  - "The FBI's alert of May 7, 2025 says that when a router is end of life, the maker \"no longer\" releases software updates or security patches, and that routers dated 2010 or earlier likely no longer receive updates."
  - "Netgear: \"In general, EOS for NETGEAR products occurs three years after the last sale date.\" After end of service (EOS), a product no longer receives firmware updates, including security updates."
  - "eero guarantees security updates until at least five years from when you bought a device new on eero.com or Amazon, or until the date in its published table if later. Dates in that table run from March 11, 2030 to October 31, 2031."
  - "An unsupported router usually still works. The risk is that newly found security flaws will not be fixed."
faq:
  - q: "How old is too old for a router?"
    a: "There is no single age. Support ends when the manufacturer says so, and policies differ. Netgear says support generally ends three years after a model's last sale date. eero publishes a date for each model. The FBI's May 2025 alert says routers dated 2010 or earlier likely no longer receive updates, but that is a floor, not a guarantee that newer routers are supported."
  - q: "What does end of life mean for a router?"
    a: "The FBI describes it this way: the manufacturer no longer sells the product and is not actively supporting the hardware, so it is no longer releasing software updates or security patches for it."
  - q: "Will my router stop working when updates end?"
    a: "Usually not. eero states that its devices still work and still provide Wi-Fi after security updates end. The concern is security: flaws found later are not patched."
  - q: "How do I find my router's model and hardware version?"
    a: "Look at the label on the router. Netgear's end-of-service page says its model and hardware version are printed there. Support pages often distinguish hardware versions of the same model, so note both."
  - q: "Does my internet provider's router get updates?"
    a: "It depends on the provider and model. We did not review any provider's update policy. Ask your provider whether the gateway they supplied receives security updates and how long it will."
  - q: "Is replacing the router enough to be safe?"
    a: "No. The FBI also recommends applying available updates, turning off remote administration, and using strong, unique passwords of at least 16 characters. A new router with default settings and a reused password is still exposed."
sources:
  - title: "Cyber Criminal Proxy Services Exploiting End of Life Routers"
    publisher: "FBI Internet Crime Complaint Center (IC3)"
    url: "https://www.ic3.gov/PSA/2025/PSA250507"
    date: 2025-05-07
  - title: "End of Service Products and EOS Policy"
    publisher: "NETGEAR"
    url: "https://www.netgear.com/about/eos/"
  - title: "eero Software Security Updates"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/eero-software-security-updates"
  - title: "BOD 26-02: Mitigating Risk From End-of-Support Edge Devices"
    publisher: "Cybersecurity and Infrastructure Security Agency (CISA)"
    url: "https://www.cisa.gov/news-events/directives/bod-26-02-mitigating-risk-end-support-edge-devices"
    date: 2026-02-05
---

Your router is too old when its manufacturer has stopped issuing security updates for it. Age is only a rough guide, because manufacturers count support from different starting points. To check, find your router's exact model and hardware version, then look it up on the maker's support or end-of-service page. If updates have ended, plan to replace it, and tighten two settings in the meantime.

## What does "end of life" mean for a router?

A router is a small computer running software called firmware. Security researchers and criminals keep finding flaws in that software, and the manufacturer fixes them with firmware updates. When a model reaches end of life, those fixes stop.

The FBI's Internet Crime Complaint Center explained it in an alert dated May 7, 2025: when a device is end of life, "the manufacturer no longer sells the product and is not actively supporting the hardware, which also means they are no longer releasing software updates or security patches for the device."

The same alert says "routers dated 2010 or earlier likely no longer receive software updates issued by the manufacturer and could be compromised by cyber actors exploiting known vulnerabilities." It describes end-of-life routers breached with variants of a malware botnet called TheMoon, which lets criminals install proxies on victims' routers so they can conduct crimes anonymously. The alert says some of the affected routers had remote administration turned on.

Read the 2010 line carefully. It is an example of devices that likely no longer get updates, not a statement that a router made in 2011 or later is supported.

## Why is the router's age a poor guide?

Because the clock usually starts when the model stops being sold, not when you bought yours. The two manufacturers below show how different the rules are.

| | Netgear | eero |
|---|---|---|
| Policy | "In general, EOS for NETGEAR products occurs three years after the last sale date" | Guaranteed security updates until at least five years after you bought the device new on eero.com or Amazon, or until the date in eero's table if later |
| What starts the clock | The last date Netgear expects the product to be sold by authorized sellers | Your purchase from eero.com or Amazon, or a per-model date |
| Bought somewhere else | Same model-level rule | Supported until at least the table date for your model |
| After the date | No more firmware updates, including security updates | eero says it strives to keep providing updates as long as it can; this is not a guarantee |
| Device still works? | Not addressed on the page we read | Yes, eero says it "can still provide wifi" |

Sources: Netgear's End of Service page and eero's Software Security Updates page, both read on October 7, 2026. Neither page showed an on-page date, so policies may change. Other manufacturers have their own rules, which we did not review.

### A worked example

This example is hypothetical. It shows the arithmetic, not a real product. Suppose a Netgear router model was last sold on January 1, 2024. Under the "in general, three years" rule, its end of service would fall around January 1, 2027. Someone who bought it in 2022 and someone who bought it in 2023 would reach that date together, even though one owns an older unit. "Generally" matters: Netgear's wording is not a promise for every product, and the actual date for your model is on its list.

For eero, the table currently runs from March 11, 2030 (eero Pro and eero Beacon) to October 31, 2031 (for example eero 6, eero Pro 6E, eero 7 and eero Pro 7). These are minimum dates for support, and eero's page covers devices currently available for purchase.

## How do you check your router?

1. **Find the model and hardware version.** Both are printed on the label on the router, according to Netgear. Write down the exact model name and any "version" or "HW" number.
2. **Look up the maker's end-of-service or support page.** Netgear has a searchable end-of-service product list and offers alerts through a MyNETGEAR account. eero publishes a table of dates. For other brands, search the maker's support site for "end of life," "end of service" or "security updates" with your model name.
3. **Check for a firmware update.** Log in to the router's admin page or app and look for a firmware or software update option. The FBI advises applying "any available security patches and/or firmware updates" immediately.
4. **Look at when your firmware was last updated.** If the latest available version is years old and the maker's page says the model is discontinued, treat that as a warning sign. This is our rule of thumb, not an official test.
5. **If your internet provider supplied the router,** ask them whether it receives security updates and for how long. We did not review provider policies.

## What should you do if updates have ended?

The FBI's recommendation is direct: "If the router is at end of life, replace the device with an updated model if possible." Until you can:

- **Turn off remote management.** The FBI says to log in to the router settings, disable remote management or remote administration, save the change, and reboot the router.
- **Use a strong, unique admin password.** The FBI specifies passwords that are "unique and random" with at least 16 and no more than 64 characters, and advises against reusing them.
- **Watch for signs of infection.** The FBI lists overheating, connectivity problems and changed settings you do not recognize as commonly observed signs. These can have innocent causes too, so treat them as a reason to look closer.
- **If you suspect compromise,** the FBI advises applying any updates, changing your password and rebooting the router.

Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) walks through these settings, and our [WPA2 vs. WPA3 guide]({{< relref "/guides/wpa2-vs-wpa3" >}}) covers the Wi-Fi encryption setting. Putting smart devices on a separate network also limits how far a problem can spread, as we explain in our [guest network guide]({{< relref "/guides/guest-wifi-network-smart-home-devices" >}}).

## What should you look for in a replacement?

Check whether the manufacturer states a support period before you buy. eero does, with a dated table. Netgear's policy ties support to the last sale date, so ask how long a model has been on sale. A router that has been on shelves for years has less support left than a newly launched one, even when the box is new.

For picks by home size, see our guides to the [best Wi-Fi router for a large house]({{< relref "/guides/best-wifi-router-for-large-house" >}}) and [Wi-Fi 6E vs. Wi-Fi 7]({{< relref "/guides/wifi-6e-vs-wifi-7" >}}). Support length is a separate question from speed, so weigh both.

## Does the US government take this seriously?

The Cybersecurity and Infrastructure Security Agency (CISA) issued Binding Operational Directive 26-02 on February 5, 2026. It requires federal civilian agencies to replace end-of-support edge devices, a category that explicitly includes routers, on a schedule: listed devices whose end-of-support date falls on or before the 12-month mark within 12 months, and all identified end-of-support edge devices within 18 months. It defines end-of-support devices as hardware, firmware and software versions that "no longer receive timely, supported updates from the original equipment manufacturer."

This directive applies to federal agencies, not to homes or private businesses. It shows how the government treats unsupported routers inside its own networks. It is not a rule you must follow, and we do not claim it sets a deadline for your router.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| End of life means the maker no longer sells or actively supports the product, and no longer releases updates or patches | [FBI IC3 alert, May 7, 2025](https://www.ic3.gov/PSA/2025/PSA250507) | Verified |
| Routers dated 2010 or earlier likely no longer receive updates; TheMoon variants breached end-of-life routers; some had remote administration on | [FBI IC3 alert, May 7, 2025](https://www.ic3.gov/PSA/2025/PSA250507) | Verified; the alert gives an example age, not a safe-after date |
| FBI recommends replacing end-of-life routers, applying updates, disabling remote administration, and using unique passwords of 16 to 64 characters | [FBI IC3 alert, May 7, 2025](https://www.ic3.gov/PSA/2025/PSA250507) | Verified |
| Signs of router malware include overheating, connectivity problems and unrecognized setting changes | [FBI IC3 alert, May 7, 2025](https://www.ic3.gov/PSA/2025/PSA250507) | Verified as the FBI's "commonly identified" signs |
| Netgear EOS generally occurs three years after the last sale date; EOS products get no firmware updates; model and hardware version are on the product label | [NETGEAR End of Service](https://www.netgear.com/about/eos/) | Verified as of October 7, 2026; page carries no on-page date |
| eero guarantees updates until at least five years from purchase new on eero.com or Amazon, or the table date if later; devices still work after updates end | [eero Software Security Updates](https://eero.com/support/articles/eero-software-security-updates) | Verified as of October 7, 2026; page carries no on-page date |
| eero table dates run from March 11, 2030 to October 31, 2031 | [eero Software Security Updates](https://eero.com/support/articles/eero-software-security-updates) | Verified for devices listed there as currently available |
| CISA BOD 26-02 issued February 5, 2026; applies to federal civilian agencies; covers routers; 12- and 18-month decommission deadlines | [CISA BOD 26-02](https://www.cisa.gov/news-events/directives/bod-26-02-mitigating-risk-end-support-edge-devices) | Verified; does not apply to home users |
| Netgear worked example (last sale January 1, 2024, EOS about January 1, 2027) | Our arithmetic on Netgear's "three years" wording | Qualified: hypothetical, and "in general" is Netgear's wording |
| Checking whether firmware is years old is a warning sign | Our judgment | Qualified: rule of thumb, not an official test |

## Bottom line

Do not judge a router by how many years you have owned it. Judge it by whether its maker still issues security updates, and find that out from the exact model and hardware version on its label. If updates have ended, replace it when you can. Until then, turn off remote management and use a long, unique admin password.
