---
title: "Is Your Router Too Old? How to Check if It Still Gets Security Updates"
date: 2026-10-06
description: "Routers stop getting security fixes on a schedule set by the maker. Here is how to find yours, what eero, Netgear and TP-Link say, and what to do about it."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "routers"]
tags: ["end-of-life", "router-security", "firmware", "security-updates", "eero", "netgear", "tp-link"]
summary: "A router is unsupported once its maker stops releasing security updates, and each maker sets that date differently. eero publishes guaranteed dates (at least October 31, 2031 for eero 6 and newer models listed on its page). Netgear's policy ends security patches three years after the product's last sale date. TP-Link's page we reviewed lists end-of-service products as receiving no active support. To check yours, find the model and hardware version, look up the maker's policy, and check your firmware. If the router is unsupported, the FBI recommends replacing it, and turning off remote management in the meantime."
imageAlt: ""
takeaways:
  - "The FBI said on May 7, 2025 that routers dated 2010 or earlier likely no longer receive manufacturer updates, and that end-of-life routers with remote administration turned on were found compromised by a variant of TheMoon malware."
  - "eero's support page (checked October 6, 2026) lists guaranteed security-update end dates: at least March 11, 2030 for the original eero Pro and eero Beacon, and at least October 31, 2031 for eero 6 and newer models listed."
  - "Netgear's End of Service policy says products stop receiving firmware updates, including security updates, three years after the last sale date."
  - "A router that no longer gets updates still works. The risk is that newly found flaws are not fixed."
faq:
  - q: "What does end of life mean for a router?"
    a: "The FBI defines it this way: the manufacturer no longer sells the product and is not actively supporting the hardware, which means no more software updates or security patches. Makers use different terms, such as end of service (Netgear and TP-Link) or the end of the software security update period (eero)."
  - q: "Will my router stop working when it reaches end of support?"
    a: "No. eero's page says its devices 'will still work and can still provide wifi' after security updates end, and Netgear's policy says customers may continue to use products after end of service. What stops is the delivery of fixes for new security flaws."
  - q: "How do I know if my router is still getting updates?"
    a: "Find the exact model and hardware version, then check the manufacturer's support or lifecycle page for that model, and look at when its last firmware was released. If you cannot find a policy or any recent firmware, treat that as a warning sign and consider replacing it."
  - q: "Is a router with remote management turned on more at risk?"
    a: "The FBI's May 2025 alert said the end-of-life routers it saw compromised had remote administration turned on, and it recommends disabling remote management. Check that setting whether or not your router is old."
  - q: "Does the federal order to replace end-of-support devices apply to my home router?"
    a: "No. CISA's Binding Operational Directive 26-02, issued February 5, 2026, applies to US federal civilian executive branch agencies, not to households or contractors. It is useful as a definition of end-of-support, not as a requirement for you."
  - q: "My router came from my internet provider. Who updates it?"
    a: "We could not find a general rule that applies to every provider, so ask your provider whether it still updates your specific gateway model and for how long."
sources:
  - title: "Cyber Criminal Proxy Services Exploiting End of Life Routers (Alert I-050725-PSA)"
    publisher: "FBI Internet Crime Complaint Center (IC3)"
    url: "https://www.ic3.gov/PSA/2025/PSA250507"
    date: 2025-05-07
  - title: "BOD 26-02: Mitigating Risk From End-of-Support Edge Devices"
    publisher: "Cybersecurity and Infrastructure Security Agency (CISA)"
    url: "https://www.cisa.gov/news-events/directives/bod-26-02-mitigating-risk-end-support-edge-devices"
    date: 2026-02-05
  - title: "eero Software Security Updates"
    publisher: "eero Support"
    url: "https://support.eero.com/hc/articles/360051143272"
  - title: "NETGEAR End of Service Policy (2025)"
    publisher: "NETGEAR"
    url: "https://downloads1.netgear.com/files/netgear/pdfs/EOS-Policy-2025.pdf"
  - title: "Software and Firmware Support on End of Service Products"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/us/support/faq/4308"
    date: 2024-11-09
---

A router is "unsupported" when its maker stops releasing security updates for it, and each maker sets that date differently. Your router keeps working afterward. What changes is that flaws found later are not fixed. This guide shows how to find your router's support status, what three major makers (eero, Netgear and TP-Link) say in their own policies, and what to do if yours has run out.

This guide covers consumer routers sold in the United States. We checked each policy page on October 6, 2026, and policies can change.

## What does "end of life" mean for a router?

The FBI's May 7, 2025 alert defines it this way: "When a hardware device is end of life, the manufacturer no longer sells the product and is not actively supporting the hardware, which also means they are no longer releasing software updates or security patches for the device."

Other terms mean roughly the same thing:

- **End of service (EOS)** is the term Netgear and TP-Link use for the stage when security updates stop.
- **End of support** is the term in the Cybersecurity and Infrastructure Security Agency's (CISA) directive for federal agencies, which defines it as hardware and software that "no longer receive timely, supported updates from the original equipment manufacturer, including patches for CVEs, security updates, software fixes (hotfixes), and defects." A CVE is a publicly numbered record of a known security flaw. That directive, BOD 26-02 of February 5, 2026, applies to federal civilian agencies, not to households.

## Why does an unsupported router matter?

An unsupported router is not automatically hacked. The risk is that a flaw discovered after support ends stays open.

The FBI's alert gives a real example. It says cyber criminals used variants of a botnet called TheMoon to turn end-of-life routers into proxies, which relay traffic so that criminals can hide who they are. According to the FBI, some end-of-life routers "with remote administration turned on" were found compromised by a new variant. The FBI describes TheMoon as not needing a password to infect a router: it "scans for open ports and sends a command to a vulnerable script." The alert says routers dated 2010 or earlier likely no longer receive software updates.

The FBI lists these signs of infection: overheating, connectivity problems, and changes to settings the administrator does not recognize. Those signs can have other causes, so they are a prompt to check, not proof.

Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) says the same in one line: if your router no longer receives updates, replace it.

## What do eero, Netgear and TP-Link say?

The three policies work differently, so compare them carefully.

| Maker | How the policy defines support | What we confirmed on October 6, 2026 |
|---|---|---|
| eero | Guaranteed security updates until at least five years from when you bought the device new on eero.com or Amazon.com, or until the date in its table if later. Devices bought elsewhere are supported at least until the table date. | The page lists dates by model: at least March 11, 2030 for eero Pro and eero Beacon, April 28, 2030 for eero (2nd Generation), July 14, 2030 for eero Pro 6, and October 31, 2031 for eero 6, 6+, Pro 6E, Max 7, eero 7, eero Pro 7 and other listed models. |
| Netgear | End of service occurs three years after the last sale date. For those three years Netgear may provide critical bug fixes and security patches "as determined by NETGEAR." | The policy document is titled "EOS Policy 2025." It says products at end of service no longer receive firmware updates, including security updates. |
| TP-Link | Products at end of service are "no longer receiving active support, including security updates." | The page, updated November 9, 2024, names three routers (Archer C7(EU) V2, TL-WR841N(MS) V9, TL-WR841ND(MS) V9) that received patched firmware on November 8, 2024, and recommends upgrading to newer hardware. |

**eero.** The page also says that "we strive to provide software security updates for as long as we can (subject to technical and other limitations)" after those dates, and that the dates are not a guarantee of how long a device will last. The table covers devices currently available on eero.com and Amazon.com. If your eero model is not listed, contact eero.

**Netgear.** The "last sale date" is the last day Netgear reasonably expects the product to be available through authorized sellers. For one year after it, Netgear "may provide" software updates and feature enhancements. For three years after it, Netgear "may provide critical bug fixes and security patches as determined by NETGEAR." After three years the product reaches end of service. Here is a hypothetical example, not a real product: if a router's last sale date were March 1, 2023, its end of service would be March 1, 2026. The policy has exceptions: products sold through carriers or network operators may be supported by them instead, and some enterprise products have different terms. The policy says the last sale date can be limited to a particular SKU in a particular country or region, and that Netgear keeps a list of products that have reached it on its website.

**TP-Link.** The TP-Link page we reviewed does not explain how to find out whether another model has reached end of service, so check your model's page on TP-Link's US support site. TP-Link's advice on that page includes avoiding the remote management function and managing the router through its Tether app instead.

**ASUS and others.** We could not confirm a general US security-update policy for ASUS routers. The ASUS security-update duration page we found (last updated September 3, 2026) is labeled "only for Singapore," so we did not use its dates. If you own an ASUS or other router, look for the maker's lifecycle or security advisory page for your exact model and region.

## How do you check your own router?

Menu names vary by brand, so use these steps as a guide.

1. **Find the exact model and hardware version.** The model name and a version (often written V1, V2 and so on) are usually printed on the label on the device or shown in its app or admin page. Policies and patches can differ by version.
2. **Find the firmware version and when it was released.** The router's admin page or app shows the installed firmware. Compare it with the latest firmware on the maker's download page for your model and region. If no new firmware has appeared for a long time, that is a warning sign. We have no standard cutoff, so treat it as a prompt to check the maker's policy rather than as proof.
3. **Look up the maker's policy for your model.** Search the maker's support site for "end of service," "end of life" or "security update period."
4. **Apply any available update**, then switch on automatic updates if your router offers them.
5. **Turn off remote management** unless you truly need it, then save and reboot. This is the FBI's advice, and TP-Link gives similar advice for its older models. Our [hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) has the full set of settings.
6. **If you rent the router from your internet provider,** ask the provider whether it still updates that model.

## What should you do if your router is unsupported?

The FBI's recommendation: "If the router is at end of life, replace the device with an updated model if possible." Until you replace it:

- Install any security patches still available.
- Disable remote management, save the setting and reboot.
- Use a unique, random password of at least 16 characters (the FBI's range is 16 to 64) for the router's admin login.
- If anything looks off, update, change the password and reboot. If you think you are a victim, the FBI asks you to file a complaint at ic3.gov.

When you shop for a replacement, check the maker's published support period before you buy, since policies differ widely. See our guides on [Wi-Fi 6E versus Wi-Fi 7]({{< relref "/guides/wifi-6e-vs-wifi-7" >}}), [mesh versus a single router]({{< relref "/guides/wifi-router-vs-mesh" >}}) and [WPA2 versus WPA3]({{< relref "/guides/wpa2-vs-wpa3" >}}). Older devices that cannot use WPA3 are one more reason to look at newer hardware.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| The FBI defines end of life as no longer sold, not actively supported, and no longer receiving updates or patches | [FBI IC3 alert I-050725-PSA, May 7, 2025](https://www.ic3.gov/PSA/2025/PSA250507) | Verified |
| The FBI says routers dated 2010 or earlier likely no longer receive updates; end-of-life routers with remote administration on were compromised by a TheMoon variant; TheMoon scans for open ports and does not need a password | [FBI IC3 alert I-050725-PSA, May 7, 2025](https://www.ic3.gov/PSA/2025/PSA250507) | Qualified: the FBI's statement about routers "dated 2010 or earlier" is a general estimate ("likely"), not a rule for every model |
| The FBI recommends replacing end-of-life routers, applying patches, disabling remote management and using passwords of 16 to 64 characters | [FBI IC3 alert I-050725-PSA, May 7, 2025](https://www.ic3.gov/PSA/2025/PSA250507) | Verified |
| CISA BOD 26-02 (February 5, 2026) defines end-of-support as devices no longer receiving timely, supported updates from the original manufacturer, and applies to federal civilian agencies, not contractors | [CISA BOD 26-02](https://www.cisa.gov/news-events/directives/bod-26-02-mitigating-risk-end-support-edge-devices) | Qualified: the page was retrieved by our tools only through a text summary because direct downloads were blocked |
| eero guarantees security updates until at least five years from purchase new on eero.com or Amazon.com, or the table date if later; devices still work afterward | [eero Support](https://support.eero.com/hc/articles/360051143272) | Qualified: the page is undated; contents as retrieved October 6, 2026 |
| eero table dates: March 11, 2030 (eero Pro, Beacon); April 28, 2030 (eero 2nd Gen); July 14, 2030 (Pro 6); October 31, 2031 (eero 6, 6+, Pro 6E, Max 7, eero 7, Pro 7 and other listed models) | [eero Support](https://support.eero.com/hc/articles/360051143272) | Qualified: the page is undated; dates are "at least through" minimums, and the page can change |
| Netgear: end of service occurs three years after the last sale date; critical bug fixes and security patches may be provided during those three years, as Netgear determines; products then stop receiving firmware updates, including security updates | [NETGEAR End of Service Policy](https://downloads1.netgear.com/files/netgear/pdfs/EOS-Policy-2025.pdf) | Qualified: carrier-sold and enterprise products can have different terms; the document shows no publication date beyond its "2025" title |
| TP-Link: end-of-service products are no longer receiving active support, including security updates; three named routers received patched firmware on November 8, 2024; TP-Link recommends upgrading and avoiding remote management | [TP-Link FAQ 4308, updated November 9, 2024](https://www.tp-link.com/us/support/faq/4308) | Qualified: describes those three products and advice as of that page's date |
| ASUS's security-update duration page we found (last updated September 3, 2026) is labeled as applying only to Singapore, so no US dates are given | [ASUS support FAQ 1051375](https://www.asus.com/support/FAQ/1051375) | Qualified: we state only that we could not confirm a US policy |
| The worked Netgear date example (March 1, 2023 plus three years is March 1, 2026) | Arithmetic on the Netgear policy | Qualified: hypothetical, not a real product |

## Bottom line

A router that no longer gets security updates still works, but newly found flaws stay open. Find your router's model and hardware version, check the maker's policy for that model, and make sure remote management is off. If the router is unsupported, plan to replace it, as the FBI advises. When you buy the next one, check the maker's published support period first. Look for a stated end date, as eero publishes, or a stated policy, as Netgear does.
