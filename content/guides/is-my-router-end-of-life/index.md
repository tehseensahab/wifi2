---
title: "Is Your Router End of Life? How to Check and What to Do"
date: 2026-10-10
description: "An end-of-life router stops getting security updates. What the FBI warned in 2025, how Netgear and Linksys define support, and how to check yours."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "routers"]
tags: ["end-of-life", "firmware", "router-security", "fbi", "remote-management", "updates"]
summary: "A router is end of life, or out of support, when its maker stops releasing firmware, including security fixes. The FBI warned on May 7, 2025 that criminals were taking over unsupported routers and using them as proxies. To check yours, find the model and hardware version on the label, then look it up on the maker's lifecycle page. If it's unsupported, turn off remote management now and plan a replacement."
imageAlt: "Gray Ethernet port with two green status lights on a small network adapter, photographed head-on on a dark desk"
imageCredit: "Photo: Jesse Ayegba / [Unsplash](https://unsplash.com/photos/a-close-up-of-a-router-on-a-table-o-qB6ikmn8w)"
takeaways:
  - "The FBI said on May 7, 2025 that end-of-life routers were breached with variants of the TheMoon botnet, and that TheMoon \"does not require a password to infect routers.\""
  - "Netgear says EOS (End of Service) generally comes three years after a product's last sale date, and that EOS products no longer receive firmware updates, including security updates."
  - "Linksys separates End of Life (no longer manufactured, but major security updates continue for a period) from End of Support (no security updates)."
  - "The FBI's first-line mitigations are to replace end-of-life routers, apply patches, and turn off remote management."
faq:
  - q: "What does end of life mean for a router?"
    a: "It means the maker has stopped, or is about to stop, supporting the product. The exact meaning depends on the maker. Netgear's End of Service means no more firmware updates, including security updates. Linksys splits it into End of Life, when manufacturing stops but major security updates continue for a time, and End of Support, when security updates stop."
  - q: "How do I find out whether my router is end of life?"
    a: "Read the model number and hardware version from the label on the router, then look the model up on the manufacturer's end-of-life or end-of-service page. Netgear and Linksys both publish one. If you rent the router from your internet provider, ask the provider."
  - q: "Can I keep using an end-of-life router?"
    a: "It will usually keep working, but any security flaw found after support ends won't be fixed by the maker. Netgear says continuing to use an EOS product means accepting that risk. If you can't replace it yet, turn off remote management, which the FBI recommends, and keep strong, unique passwords."
  - q: "Is a router that is only a few years old at risk?"
    a: "Age alone doesn't decide it. Support periods are set by the maker and counted from different dates; Netgear counts from the last sale date, not the purchase date. A router you bought recently could already be close to its end of service if it had been on sale for a long time."
  - q: "How do I know if my router has been taken over?"
    a: "The FBI lists overheating devices, connectivity problems and settings changes the administrator doesn't recognize. If you suspect it, the FBI advises updating firmware, changing passwords and rebooting, and you can file a report at ic3.gov."
sources:
  - title: "Alert Number I-050725-PSA: End-of-Life Routers Used in Proxy Services"
    publisher: "FBI Internet Crime Complaint Center (IC3)"
    url: "https://www.ic3.gov/PSA/2025/PSA250507"
    date: 2025-05-07
  - title: "End of Service Products"
    publisher: "Netgear"
    url: "https://www.netgear.com/about/eos/"
  - title: "Linksys product end of life and end of support"
    publisher: "Linksys"
    url: "https://linksys.com/pages/linksys-product-end-of-life"
  - title: "BOD 26-02: Mitigating Risk From End-of-Support Edge Devices"
    publisher: "Cybersecurity and Infrastructure Security Agency (CISA)"
    url: "https://www.cisa.gov/news-events/directives/bod-26-02-mitigating-risk-end-support-edge-devices"
    date: 2026-02-05
---

An end-of-life router is one whose maker no longer releases firmware for it, including security fixes. It usually keeps working, which is why people don't notice. To check yours, find the model number and hardware version on the label, look the model up on the maker's lifecycle page, and if it is unsupported, turn off remote management today and plan a replacement.

This is a research-based guide built on the FBI's public advisory, a federal directive and two manufacturers' published policies. We did not test any router for this article.

## Why does an unsupported router matter?

Firmware is the software that runs your router. When researchers find a flaw in it, the maker ships a fix as a firmware update. Once the maker stops doing that, newly discovered flaws stay open for as long as you use the router.

The FBI described what that looks like in practice. In a public service announcement dated May 7, 2025 (alert number I-050725-PSA), it said cyber actors were using end-of-life routers as proxies, meaning relays that hide the real source of criminal activity behind an ordinary home internet connection. The FBI said:

- End-of-life routers were breached using variants of TheMoon, a botnet, which is a network of compromised devices controlled remotely.
- TheMoon "does not require a password to infect routers." It scans for open ports and sends a command to a vulnerable script.
- Routers with remote administration turned on were among those identified as compromised by a new variant.
- Routers dated 2010 or earlier "likely no longer receive software updates issued by the manufacturer."

Two limits are worth stating. The advisory is from May 2025, and we found no newer FBI advisory on this subject when preparing this article. And it describes old routers, not every router that has passed its support date.

## What do "end of life" and "end of service" mean?

There is no single industry definition. Each maker sets its own, and the stages differ.

| Maker | Term | What the maker says it means |
|---|---|---|
| Netgear | End of Service (EOS) | Generally occurs three years after the last sale date. Products "no longer receive firmware updates, including important security updates." |
| Linksys | End of Life (EOL) | The product is no longer manufactured. Major security updates are available for a period. |
| Linksys | End of Support (EOS) | The last date the product is supported. Security updates are not available after it. |

Source details are in the fact-check table below. Two practical points follow from these definitions:

- **The clock may start before you bought the router.** Netgear counts from the last date the product was sold, not from your purchase date. A router bought late in its sales life has less support time left than its age suggests.
- **"Still supported" can mean "security fixes only."** Linksys says EOL products get major security updates but not other updates.

We could not load the lifecycle pages for TP-Link or eero when preparing this guide, so we don't describe their policies here. Check your own maker's page directly.

## How do I check whether my router is supported?

1. **Find the model and hardware version.** Both are normally printed on the label on the router's underside or back. Some models have more than one hardware version, and support can differ between them.
2. **Look it up on the maker's lifecycle page.** Netgear publishes an [End of Service products page](https://www.netgear.com/about/eos/). Linksys has a [lookup by SKU or model number](https://linksys.com/pages/linksys-product-end-of-life). For other brands, search the maker's support site for "end of life" or "end of support" plus your model.
3. **Check the latest firmware date.** On the maker's support page for your model, look at when the newest firmware was released. This is our rule of thumb, not a manufacturer standard: if the newest firmware is several years old and the maker publishes no support end date, treat the router as likely unsupported and ask the maker.
4. **If your provider supplied the router,** ask the provider whether it still receives updates. We did not verify any provider's update policy for this article, so don't assume a provider-supplied gateway is covered.

## What should I do if my router is out of support?

In order of urgency:

1. **Turn off remote management** (also called remote administration), the setting that lets you reach the router's admin page from the internet. The FBI's instruction is to "disable remote management/remote administration, save the change, and reboot the router." Netgear gives the same first step before retiring a router.
2. **Install any firmware that is still offered.** The FBI recommends applying patches and updates promptly.
3. **Use a long, unique admin password.** The FBI recommends strong, unique, random passwords of 16 to 64 characters and no reuse. Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) covers this and nine other settings, and our guide to [WPS and UPnP]({{< relref "/guides/should-you-disable-wps-and-upnp" >}}) covers two more services that attackers target.
4. **Replace it.** Both the FBI and Netgear advise replacement. Netgear's guidance for a retired router is to disable Remote Access first, factory reset it, unregister it from your account and recycle it as electronic waste.

If you suspect a router is already compromised, the FBI says to update the firmware, change passwords and reboot, and to report it at ic3.gov. The signs it lists are overheating, connectivity problems and settings changes you don't recognize. These signs can have other causes, so they are a reason to investigate, not proof.

## How do I avoid buying a router that is soon unsupported?

This is our advice rather than a regulatory requirement. Before you buy, find the maker's published support policy for that product line. Favor a maker that states a minimum security-update period. Be wary of a model that has been on sale for years, because for makers that count from the last sale date, such as Netgear, the clock may already be running. Our [router buying guide]({{< relref "/guides/best-wifi-router-for-large-house" >}}) and [Wi-Fi 6E vs. Wi-Fi 7 guide]({{< relref "/guides/wifi-6e-vs-wifi-7" >}}) cover which models and standards fit which homes. Also confirm your Wi-Fi security mode; see [WPA2 vs. WPA3]({{< relref "/guides/wpa2-vs-wpa3" >}}).

## Does this apply to government networks too?

Yes, in a different form. On February 5, 2026, the Cybersecurity and Infrastructure Security Agency (CISA) issued Binding Operational Directive 26-02, which orders US federal civilian agencies to update supported edge devices and decommission unsupported ones on set deadlines. CISA defines edge devices as technology on the boundary of an agency's network, including routers. The directive applies to those agencies, not to households or contractors, and it does not create a legal duty for you. We cite it because it shows that unsupported network gear is being treated as a security risk at the federal level.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| The FBI said on May 7, 2025 that end-of-life routers were breached with variants of TheMoon, that it needs no password, and that routers dated 2010 or earlier likely get no manufacturer updates | [FBI IC3, I-050725-PSA, May 7, 2025](https://www.ic3.gov/PSA/2025/PSA250507) | Verified. The advisory covers older routers; we found no newer FBI advisory |
| The FBI's mitigations: replace end-of-life routers, apply patches, disable remote management and reboot, use 16 to 64 character unique passwords | [FBI IC3, I-050725-PSA](https://www.ic3.gov/PSA/2025/PSA250507) | Verified |
| The FBI lists overheating, connectivity problems and unrecognized settings changes as signs, and asks victims to report at ic3.gov | [FBI IC3, I-050725-PSA](https://www.ic3.gov/PSA/2025/PSA250507) | Verified. Signs can have other causes |
| Netgear EOS generally occurs three years after the last sale date; EOS products get no firmware updates, including security updates | [Netgear, End of Service Products](https://www.netgear.com/about/eos/) | Verified as of October 10, 2026. Netgear says "in general," so individual products may differ |
| Netgear advises replacing, and, for a retired router, disabling Remote Access, factory resetting, unregistering and recycling | [Netgear, End of Service Products](https://www.netgear.com/about/eos/) | Verified as of October 10, 2026 |
| Linksys defines EOL as no longer manufactured with major security updates available, and EOS as the last supported date with no security updates after | [Linksys, product end of life](https://linksys.com/pages/linksys-product-end-of-life) | Verified as of October 10, 2026. The page shows no publication date; dates vary by model |
| CISA BOD 26-02 (February 5, 2026) applies to federal civilian agencies, not contractors, and defines edge devices to include routers | [CISA, BOD 26-02](https://www.cisa.gov/news-events/directives/bod-26-02-mitigating-risk-end-support-edge-devices) | Verified. Not binding on households |
| Checking firmware age as a rule of thumb; asking your provider; choosing makers with stated support periods | Our suggestions | Qualified: editorial advice, not a manufacturer or regulator requirement |

## Bottom line

A router that no longer gets security updates keeps working while its risk grows. Look up your model on the maker's lifecycle page, and if it is unsupported, turn off remote management first and replace it when you can. Check the maker's support policy before you buy the next one.
