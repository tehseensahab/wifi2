---
title: "How to Change the DNS Server on Your Router: Cloudflare, Google or Quad9?"
date: 2026-10-08
description: "Changing your router's DNS server takes a few minutes. Here are the exact addresses for Cloudflare, Google and Quad9, how their privacy policies differ, and how to undo the change."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "security-privacy"]
tags: ["dns", "cloudflare-1-1-1-1", "google-public-dns", "quad9", "router-settings", "dns-filtering"]
summary: "DNS (Domain Name System) turns website names into the numeric addresses computers connect to, and your router normally uses your internet provider's DNS service. You can swap it for Cloudflare (1.1.1.1), Google (8.8.8.8) or Quad9 (9.9.9.9) in your router's settings: write down the old values, enter two new addresses, save, and test. Quad9's recommended addresses and Cloudflare's 1.1.1.2 and 1.1.1.3 pairs block known malicious sites; Cloudflare's standard 1.1.1.1 does not. We did not test speed, and some provider-supplied routers lock the setting."
imageAlt: "Laptop open on a desk showing a code editor, with a smartphone, a second phone and a monitor around it"
imageCredit: "Generic desk photo, not a DNS settings screen. Photo: Mahmudul Hasan / [Unsplash](https://unsplash.com/photos/laptop-screen-displays-code-with-surrounding-tech-devices-LIVNlRn1a0s)"
takeaways:
  - "Every address below was read from the provider's own documentation on October 8, 2026. Cloudflare's standard resolver is 1.1.1.1 and 1.0.0.1; Google's is 8.8.8.8 and 8.8.4.4; Quad9's recommended pair is 9.9.9.9 and 149.112.112.112."
  - "Google's instructions say to write down your existing DNS addresses before changing them, and to enter at least two addresses."
  - "Google also warns that some ISPs hard-code DNS into the equipment they supply. If your router is one of those, set DNS on each device instead."
  - "The three providers describe logging differently: Cloudflare says logs are deleted within 25 hours, Google says temporary logs are deleted within 24 to 48 hours, and Quad9 says it does not collect or record user IP addresses."
faq:
  - q: "Will changing DNS make my internet faster?"
    a: "We can't say. We did not run speed tests, and none of the three providers' documentation we read promises a speed gain for every home. DNS only affects the lookup step before a connection starts, not your plan's download speed. If pages feel slow, see our guide on slow Wi-Fi when the internet is fast."
  - q: "Is it safe to change my router's DNS server?"
    a: "It is a normal setting and reversible, if you write down the original values first, as Google's instructions advise. The provider you choose will see your DNS lookups, so read its privacy terms. Changing DNS does not encrypt your traffic or work like a VPN."
  - q: "Which DNS server blocks malware?"
    a: "Per the providers' pages: Quad9's recommended addresses (9.9.9.9) block malicious domains, and Cloudflare's 1.1.1.2 addresses block malware. Cloudflare's standard 1.1.1.1 and Google's 8.8.8.8 are not described as filtering. No filter catches everything, so keep your devices updated."
  - q: "Why can't I change DNS on my ISP's router?"
    a: "Google's documentation says some ISPs hard-code their DNS servers into the equipment they provide, in which case you cannot configure the router to use another DNS service. You can set DNS on each computer or phone instead, or ask your ISP whether the setting can be unlocked."
  - q: "Should I use the primary and secondary addresses?"
    a: "Yes. Google says that for the most reliable DNS service you should configure at least two DNS addresses, and not use the same address twice. Each provider below lists a pair for that reason."
sources:
  - title: "1.1.1.1 IP addresses"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/ip-addresses/"
  - title: "Public DNS resolver privacy"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/"
    date: 2026-05-06
  - title: "Get Started: Configure your network settings to use Google Public DNS"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/docs/using"
  - title: "Google Public DNS: Your Privacy"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/privacy"
  - title: "Service addresses and features"
    publisher: "Quad9"
    url: "https://quad9.net/service/service-addresses-and-features/"
  - title: "Quad9 Data and Privacy Policy, version 1.1"
    publisher: "Quad9"
    url: "https://quad9.net/privacy/policy/"
    date: 2026-06-24
---

You can change the DNS server your router uses in a few minutes, from its admin page: write down the current values, enter two new addresses, save, and test. DNS stands for Domain Name System. It is the lookup service that turns a name like example.com into the numeric address your device connects to. Unless you change it, your router normally uses the DNS service run by your internet provider.

People change it for two reasons we can support from the providers' own documentation: to choose a service with different privacy terms, or to choose one that blocks known malicious websites. We did not test whether any of them is faster in your home, and we make no speed claim. This is a research-based guide; all addresses and policies were read from the providers' pages on October 8, 2026.

## Which DNS addresses should you use?

These are IPv4 addresses, the familiar four-number format. Enter the first in the primary (preferred) field and the second in the secondary (alternate) field.

| Provider and option | Primary | Secondary | Blocks known malicious sites? |
|---|---|---|---|
| Cloudflare, standard | 1.1.1.1 | 1.0.0.1 | No; Cloudflare describes it as having no content filtering |
| Cloudflare, "Block malware" | 1.1.1.2 | 1.0.0.2 | Yes, malware |
| Cloudflare, "Block malware and adult content" | 1.1.1.3 | 1.0.0.3 | Yes, malware and adult content |
| Google Public DNS | 8.8.8.8 | 8.8.4.4 | Not described as filtering on the page we read |
| Quad9, recommended | 9.9.9.9 | 149.112.112.112 | Yes |
| Quad9, unfiltered ("for experts only") | 9.9.9.10 | 149.112.112.10 | No |

IPv6 is the newer, longer address format. If your router has separate IPv6 DNS fields, the providers publish IPv6 equivalents on their pages: for example, Cloudflare's standard pair is 2606:4700:4700::1111 and 2606:4700:4700::1001, Google's is 2001:4860:4860::8888 and 2001:4860:4860::8844, and Quad9's recommended pair is 2620:fe::fe and 2620:fe::9. Google notes that some routers need the full eight-field form of its IPv6 addresses. If your router leaves IPv6 DNS at its default, lookups over IPv6 may still go to your provider's service. That is our reading of how the fields work, not something the providers state, so check after changing.

## How do you change DNS on your router?

Menu names differ by brand, so these steps follow the generic process in Google's instructions.

1. **Open the router's admin page.** Enter its IP address in a browser. Google lists 192.168.0.1 and 192.168.1.1 as common defaults. If neither works, look up the default gateway in your computer's network settings, or use the router's app if it has one.
2. **Sign in.** Use the router's admin password, not your Wi-Fi password.
3. **Find the DNS settings.** Look under Internet, WAN or Network settings.
4. **Write down the current values.** Google says to keep them for backup, which is also how you undo the change.
5. **Enter two addresses** from the table above, from one provider.
6. **Save, then restart your browser.** Some routers also need a reboot.
7. **Test.** Load a few sites you use, and check that other devices, such as a TV or smart speaker, still connect.

To undo it, put your old values back, or set the fields to automatic if that is what they were.

## Why might the setting be locked?

Google's documentation warns that some ISPs hard-code their DNS servers into the equipment they provide, and if your router is one of those, you cannot configure it to use Google Public DNS. The same limit would apply to other providers. Two things to try:

- **Set DNS on each device** (computer, phone) in its own network settings, as Google suggests.
- **Ask your ISP** whether the DNS setting can be unlocked or changed on its gateway. We did not verify what any specific ISP allows.

## How do the three providers handle your data?

Whichever provider you choose will see the domain names your devices look up, because that is what DNS is. These are the providers' own statements about logging. We cannot verify how they carry them out.

| | Cloudflare (1.1.1.1) | Google Public DNS | Quad9 |
|---|---|---|---|
| IP addresses | Says it will not retain the source IP in non-volatile storage, except randomly sampled packets from at most 0.05% of traffic used for troubleshooting and attack mitigation | Temporary logs store your IP address and your DNS query | Says it does not collect or record user IP addresses; holds them in memory only for the microseconds to milliseconds needed to answer |
| Deletion timing | Says it deletes its logs and truncated IP addresses within 25 hours | Says temporary logs are subject to deletion within 24 to 48 hours, and may be kept longer to resolve security and abuse issues | Does not state a retention period for its counters, and says they may be kept in permanent archives |
| Longer-term data | May keep aggregated data indefinitely | Permanent logs are a sample with the IP address removed, replaced by city- or region-level location; no retention period stated | Counters with no personal information, per Quad9 |
| Page date | Page header: last updated May 6, 2026 | No date on the page | Policy version 1.1, June 24, 2026 |

Reading the table: Cloudflare and Quad9 make no-IP-retention commitments; Google says IP addresses sit in short-lived temporary logs. These are different promises, not a ranking. Cloudflare's page also carries an older date (March 27, 2024) in its body text, so treat the May 6, 2026 header date as the page's most recent revision. Quad9 notes that a separate policy applies to anomalous conditions such as suspected attacks, which we did not review.

## Which one should you pick?

Our assessment, based on the documentation above and not on testing:

- **You want blocking of known malicious sites with no extra setup:** Quad9's recommended addresses, or Cloudflare's 1.1.1.2 pair. Filters work from lists of known bad domains, so a brand-new malicious site can get through. This does not replace updating your devices; see our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}), where DNS filtering is one of ten settings.
- **You want no filtering:** Cloudflare's 1.1.1.1 or Google's 8.8.8.8. Filtering can occasionally block a site you want, and an unfiltered service avoids that.
- **Logging is your main concern:** compare the logging table above. Cloudflare and Quad9 state they do not retain source IP addresses (Cloudflare with a sampling exception), and Google says its temporary logs hold them for 24 to 48 hours. Pick the statement you are comfortable relying on.
- **Slow pages are the real problem:** DNS is only the lookup step. Start with [why Wi-Fi is slow when the internet is fast]({{< relref "/guides/wifi-slow-but-internet-fast" >}}) and [how to fix slow Wi-Fi]({{< relref "/guides/how-to-fix-slow-wifi" >}}).

A DNS change does not encrypt your traffic, and it is not a VPN. It only changes which service answers name lookups.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Cloudflare's standard resolver is 1.1.1.1 and 1.0.0.1; "Block malware" is 1.1.1.2 and 1.0.0.2; "Block malware and adult content" is 1.1.1.3 and 1.0.0.3; IPv6 pairs as listed | [Cloudflare Docs, 1.1.1.1 IP addresses](https://developers.cloudflare.com/1.1.1.1/ip-addresses/) | Verified, October 8, 2026 |
| Google Public DNS is 8.8.8.8 and 8.8.4.4, with IPv6 2001:4860:4860::8888 and ::8844; some routers need the full IPv6 form | [Google, Configure your network settings](https://developers.google.com/speed/public-dns/docs/using) | Verified, October 8, 2026 |
| Quad9's recommended addresses are 9.9.9.9 and 149.112.112.112 (malware blocking: yes); unfiltered is 9.9.9.10 and 149.112.112.10 | [Quad9, service addresses](https://quad9.net/service/service-addresses-and-features/) | Verified, October 8, 2026 |
| Google says to record your original DNS values, to enter at least two addresses, and that some ISPs hard-code DNS into supplied equipment | [Google, Configure your network settings](https://developers.google.com/speed/public-dns/docs/using) | Verified; applies to the steps as Google describes them |
| Cloudflare says it deletes logs and truncated IPs within 25 hours and does not retain source IPs in non-volatile storage, apart from sampled packets from at most 0.05% of traffic | [Cloudflare Docs, privacy](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/) | Qualified: Cloudflare's own statement; page header date May 6, 2026, with an older date in its body text |
| Google says temporary logs hold your IP address and query and are deleted within 24 to 48 hours, with possible longer retention for security and abuse | [Google, Your Privacy](https://developers.google.com/speed/public-dns/privacy) | Qualified: Google's own statement; the page shows no date and no retention period for permanent logs |
| Quad9 says it does not collect or record user IP addresses, and states no retention period for its counters | [Quad9, Data and Privacy Policy v1.1, June 24, 2026](https://quad9.net/privacy/policy/) | Qualified: Quad9's own statement for normal conditions; a separate policy covers anomalous conditions, not reviewed |
| Which provider is best for you, and that filters miss new malicious sites | Our reasoning | Qualified: an assessment, not a tested result; we ran no speed or blocking tests |

## Bottom line

Write down your current DNS values, then enter two addresses from one provider, save and test. Choose Quad9's recommended pair or Cloudflare's 1.1.1.2 pair if you want known-malicious-site blocking, and Cloudflare's 1.1.1.1 or Google's 8.8.8.8 if you do not. If the setting is locked, set DNS on each device instead. Treat the providers' logging statements as their promises, read them against your own comfort, and expect no speed change unless you measure one.
