---
title: "Is Your Router Too Old? How to Check If It Still Gets Security Updates"
date: 2026-10-12
description: "An end-of-life router no longer gets security patches. How to check your router's support status, what the FBI warned about in 2025, and what to do if it's unsupported."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "routers"]
tags: ["end-of-life-router", "router-security", "firmware", "fbi-warning", "router-replacement", "remote-management"]
summary: "A router is a security risk when its maker no longer releases firmware updates for it, not simply because it is old. Look up your exact model on the maker's support or end-of-service page. If it is unsupported, replace it; until you do, turn off remote management and use a strong, unique admin password. In May 2025 the FBI warned that criminals were using end-of-life routers, with remote administration turned on, as a proxy network."
takeaways:
  - "The FBI's May 7, 2025 alert (I-050725-PSA) said criminals were using end-of-life routers in a proxy network built on malware called TheMoon. It said routers dated 2010 or earlier likely no longer receive manufacturer updates."
  - "End of life means the maker no longer sells or actively supports the device. Netgear's policy says its products generally reach end of service three years after the last sale date, and stop receiving firmware updates, including security updates."
  - "The FBI's recommendations: replace the router if it is end of life, apply available updates, disable remote administration, and use unique random passwords of 16 to 64 characters."
  - "We have not tested any router for this guide. The FBI alert does not list affected models, and support periods differ by maker and model."
faq:
  - q: "How do I know if my router is end of life?"
    a: "Find the exact model name and hardware version on the router's label, then check the maker's support or end-of-service page for that model. If the maker publishes no policy for your model, look at the firmware download page: a long gap since the last release is a warning sign, though not proof, because we found no source that sets a rule for how long a gap means unsupported."
  - q: "Is my router unsafe just because it is old?"
    a: "Not by age alone. Support status is what matters. A router that still gets firmware updates is better protected than a newer one that does not. The FBI alert did say that routers dated 2010 or earlier likely no longer receive updates."
  - q: "What is remote administration and why turn it off?"
    a: "Remote administration (also called remote management) lets you reach the router's settings page from the internet rather than only from inside your home. The FBI said a new variant of TheMoon malware was found on end-of-life routers with remote administration turned on, and recommended disabling it."
  - q: "My internet provider gave me the router. Who is responsible for updates?"
    a: "We could not find a general rule that covers every provider, so we make no claim. Ask your provider whether it manages firmware updates on that device and how long it supports it. Our guide to buying your own router vs. using the provider's covers the trade-offs."
  - q: "Can I keep using an end-of-life router if I turn off remote access?"
    a: "It reduces one known exposure, but the FBI's guidance is to replace an end-of-life router if possible. Netgear says that continuing to use a product past end of service means accepting the risk of unsupported hardware, which may leave your network more open to attacks."
sources:
  - title: "Alert I-050725-PSA: End-of-Life Routers Exploited by Cyber Actors for Proxy Services (May 7, 2025)"
    publisher: "FBI Internet Crime Complaint Center (IC3)"
    url: "https://www.ic3.gov/PSA/2025/PSA250507"
  - title: "End of Service Products"
    publisher: "NETGEAR"
    url: "https://www.netgear.com/about/eos/"
  - title: "BOD 26-02: Mitigating Risk From End-of-Support Edge Devices (February 5, 2026)"
    publisher: "CISA"
    url: "https://www.cisa.gov/news-events/directives/bod-26-02-mitigating-risk-end-support-edge-devices"
---

Your router is a security risk if its maker no longer releases firmware updates for it. Age alone doesn't settle it: look up your exact model on the maker's support or end-of-service page. If the model is no longer supported, plan to replace it, and until you do, turn off remote management.

This is a research-based guide built on the FBI's alert and manufacturer policies. We have not tested routers for it, and the FBI alert does not name specific models.

## What does "end of life" mean for a router?

The FBI's alert defines it this way: when a device is end of life, the manufacturer no longer sells the product and is not actively supporting the hardware. In practice that means no more firmware, the software that runs the router, so newly discovered security flaws stay unpatched.

Makers use different terms. Netgear calls it end of service (EOS) and says: "Products that reach EOS no longer receive firmware updates, including important security updates." CISA, the US cybersecurity agency, uses "end of support" in a directive for federal agencies, and defines it as no longer receiving timely, supported updates from the original equipment manufacturer.

## What did the FBI warn about?

On May 7, 2025, the FBI's Internet Crime Complaint Center (IC3) issued alert I-050725-PSA. It said cyber actors were using variants of the TheMoon botnet to install proxy services on end-of-life routers, which lets them hide their identities while committing crimes. The FBI said routers dated 2010 or earlier likely no longer receive manufacturer software updates and could be compromised through known vulnerabilities.

Two details matter for home users:

- **No password was needed to infect them.** The FBI said TheMoon scans for open ports and sends a command to a vulnerable script. It then contacts a command-and-control server.
- **Some of the compromised routers had remote administration turned on.** The FBI said a new variant of TheMoon was identified on end-of-life routers with remote administration enabled.

What this does not tell you: the alert gives no list of affected models, and it describes routers found compromised, not a risk level for any particular router in your home.

## How can I check whether my router is still supported?

1. **Find the exact model and hardware version.** It is usually printed on the label on the bottom or back. Support can differ between hardware versions.
2. **Search the maker's site for its end-of-service or end-of-support list.** Netgear publishes one at netgear.com/about/eos. Other makers vary; look under support or product lifecycle for your model.
3. **Read the policy, not just the list.** Netgear says that, in general, end of service occurs three years after the product's last sale date, and that the last sale date may apply to a specific model in a particular country or region. So a router can still be supported years after you bought it, and a router bought recently can be near the end if it was already being phased out.
4. **Check the firmware download page and your router's admin page.** If the last firmware release is years old, treat that as a warning. This is our rule of thumb, not a standard, and a long gap does not prove the router is unsupported. Ask the maker if the answer isn't clear.
5. **If the router belongs to your internet provider,** ask the provider about firmware updates on that device.

### An example (hypothetical)

A maker stops selling a router model on June 1, 2024. Under a policy like Netgear's three-years-after-last-sale rule, end of service would fall on June 1, 2027. A router bought in 2022 would then have been supported for about five years from purchase. This is only arithmetic to show how a policy works; actual dates for real models are on the maker's list.

## What should I do if my router is end of life?

The FBI's recommendations, in the order that makes sense for most homes:

1. **Replace it.** The FBI: "If the router is at end of life, replace the device with an updated model if possible." Our guides to [Wi-Fi router vs. mesh]({{< relref "/guides/wifi-router-vs-mesh" >}}) and [Wi-Fi 6E vs. Wi-Fi 7]({{< relref "/guides/wifi-6e-vs-wifi-7" >}}) help you choose, and [buying your own vs. renting]({{< relref "/guides/buy-your-own-router-vs-isp-equipment" >}}) covers the provider-equipment question.
2. **Apply any available updates.** The FBI advises immediately applying available security patches and firmware updates.
3. **Disable remote management.** The FBI says to disable remote management or remote administration, save the change and reboot the router.
4. **Use a strong, unique admin password.** The FBI recommends unique, random passwords of 16 to 64 characters. See our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) for the other settings worth changing, including [WPS and UPnP]({{< relref "/guides/should-you-disable-wps-and-upnp" >}}).
5. **If you suspect a problem,** the FBI says to update the firmware, change the password and reboot, and you can file a complaint with IC3.

Steps 2 to 4 reduce risk on a router that can't be replaced right away. They don't make an unsupported router supported.

### Getting rid of the old router

Netgear's guidance before disposal: factory reset the device, unregister it from your MyNETGEAR account, turn off Remote Access in the Netgear genie app if you enabled it, then recycle it through an e-waste service. For other brands, check the maker's instructions.

## Why does this matter beyond home users?

In February 2026, CISA issued Binding Operational Directive 26-02, which requires US federal civilian agencies to inventory and decommission end-of-support edge devices (including routers) on set deadlines. It applies to federal agencies, not to households or private businesses. We mention it only as evidence that regulators treat unsupported network equipment as a security problem; it doesn't set a rule for your home router.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| FBI alert I-050725-PSA was issued May 7, 2025 and concerns end-of-life routers used for proxy services via TheMoon variants | [FBI IC3](https://www.ic3.gov/PSA/2025/PSA250507) | Verified |
| Routers dated 2010 or earlier likely no longer receive manufacturer updates | [FBI IC3](https://www.ic3.gov/PSA/2025/PSA250507) | Qualified: the FBI says "likely"; no model list is given |
| End of life: manufacturer no longer sells or actively supports the hardware | [FBI IC3](https://www.ic3.gov/PSA/2025/PSA250507) | Verified |
| TheMoon needs no password, scans for open ports and contacts a command-and-control server; a new variant was found on end-of-life routers with remote administration on | [FBI IC3](https://www.ic3.gov/PSA/2025/PSA250507) | Verified; the alert describes routers found compromised, not a risk rate |
| FBI recommendations: replace EOL routers, apply updates, disable remote administration and reboot, use unique random passwords of 16-64 characters, update/change password/reboot if suspicious, report to IC3 | [FBI IC3](https://www.ic3.gov/PSA/2025/PSA250507) | Verified |
| Netgear: EOS generally occurs three years after the last sale date (which may be specific to a model, country or region); EOS products get no firmware updates, including security updates | [NETGEAR EOS page](https://www.netgear.com/about/eos/) | Qualified: applies to Netgear only; other makers' periods differ |
| Netgear disposal steps (factory reset, unregister, disable Remote Access, recycle) and risk statement | [NETGEAR EOS page](https://www.netgear.com/about/eos/) | Verified |
| CISA BOD 26-02 issued February 5, 2026; defines end of support; applies to federal civilian agencies | [CISA](https://www.cisa.gov/news-events/directives/bod-26-02-mitigating-risk-end-support-edge-devices) | Verified; not applicable to households |
| Example end-of-service date (June 1, 2027) | Our arithmetic on a hypothetical date | Verified arithmetic; hypothetical |

## Bottom line

Check your router by model, not by age. If the maker has ended support, replace it, and in the meantime turn off remote management, install any last update and set a long unique admin password. If your provider supplied the router, ask the provider how it is updated.
