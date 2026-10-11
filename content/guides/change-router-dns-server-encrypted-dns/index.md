---
title: "Should You Change Your Router's DNS Server? Cloudflare vs. Google vs. Quad9"
date: 2026-10-11
description: "What a DNS server does, what changing it can and can't do, and the exact Cloudflare, Google and Quad9 settings, with Cloudflare's and Google's own logging statements."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "how-to-fixes"]
tags: ["dns", "encrypted-dns", "doh", "cloudflare-1-1-1-1", "google-public-dns", "quad9", "router-settings"]
summary: "Changing your DNS server is optional. It can add malware blocking (Cloudflare 1.1.1.2, Quad9) or move your lookups away from your internet provider's resolver, but it will not hide your browsing from your provider and none of the provider pages we reviewed make a speed claim. Set it on the router to cover every device, unless your provider's gateway locks the setting. Encrypted DNS (DoH or DoT) is set per device or browser, and on some systems it is not available at all. This is a research-based guide from the providers' own documentation, not a hands-on test."
takeaways:
  - "DNS (Domain Name System) turns a site name into an IP address. By default your router asks your internet provider's DNS server. You can point it at another one."
  - "Cloudflare's 1.1.1.1 has no filtering; 1.1.1.2 blocks known malware and phishing; 1.1.1.3 also blocks adult content. Quad9's recommended addresses (9.9.9.9) block malware and validate DNSSEC. Google's addresses are 8.8.8.8 and 8.8.4.4."
  - "Cloudflare says it deletes public resolver logs within 25 hours. Google says its temporary logs, the only ones holding your IP address and your query together, are deleted within 24 to 48 hours."
  - "Changing DNS does not hide which sites you visit from your internet provider. It changes who sees your lookups, not who carries your traffic."
faq:
  - q: "Will changing my DNS make my internet faster?"
    a: "We found no speed claim or measured result in the providers' documentation we reviewed, so we can't promise it. DNS lookups happen before a page loads, so a slow resolver can delay the first moment of a page load, but it does not change your download speed. If your plan tests at the speed you pay for, a DNS change is unlikely to be the fix for slow Wi-Fi."
  - q: "Is it safe to use Google, Cloudflare or Quad9 DNS?"
    a: "All three publish privacy statements, summarized above. Safe is a judgment about whom you trust with your lookups. Your internet provider already sees them by default. The practical risks are different: a mistyped address can break all browsing, and a filtering variant can block a site you need."
  - q: "What is the difference between DNS, DoH and DoT?"
    a: "DNS is the lookup. DoH (DNS over HTTPS, RFC 8484) and DoT (DNS over TLS) are ways to send that lookup encrypted. Cloudflare's documentation says DoH uses port 443, the normal HTTPS port."
  - q: "Can I set this on my router and cover every device?"
    a: "Usually, yes, for plain DNS. Google's documentation says some provider-supplied equipment hard-codes its DNS servers and can't be changed, in which case you set it per device. Google also says routers have no DoT support in the base OS, so encrypted DNS is generally set on each device or browser."
  - q: "Does changing DNS work with a VPN?"
    a: "A VPN normally uses its own DNS. Google notes that Android's Private DNS setting has no effect while a VPN or DNS-changer app is active. Treat your VPN's DNS setting as the one that applies."
sources:
  - title: "Get started: Using Google Public DNS"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/docs/using"
    date: 2024-09-03
  - title: "Privacy and Security: Google Public DNS"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/privacy"
    date: 2024-09-03
  - title: "1.1.1.1 IP addresses"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/ip-addresses/"
  - title: "Public Resolver privacy"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/"
    date: 2026-05-06
  - title: "DNS over HTTPS"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/encryption/dns-over-https/"
  - title: "Service addresses and features"
    publisher: "Quad9"
    url: "https://quad9.net/service/service-addresses-and-features/"
  - title: "RFC 8484: DNS Queries over HTTPS (DoH)"
    publisher: "IETF"
    url: "https://www.rfc-editor.org/rfc/rfc8484"
    date: 2018-10-01
  - title: "Secure DNS Client over HTTPS (DoH) on Windows Server 2022"
    publisher: "Microsoft Learn"
    url: "https://learn.microsoft.com/en-us/windows-server/networking/dns/doh-client-support"
    date: 2025-04-25
  - title: "Use secure DNS in Chrome"
    publisher: "Google Chrome Help"
    url: "https://support.google.com/chrome/answer/10468685"
---

Changing your DNS server is optional, and for most homes it is a small tweak, not a fix. It can add a layer of malware blocking or move your lookups away from your internet provider's resolver. It will not hide which sites you visit from your provider, and none of the provider pages we reviewed promise faster browsing. If you want to try it, set it on your router so every device follows, and keep a note of your old settings so you can undo it.

This guide is built from the providers' own documentation, read on October 11, 2026. We have not benchmarked these services, and we link the pages so you can check for changes.

## What does a DNS server do?

**DNS** (Domain Name System) is the lookup that turns a name like `example.com` into the numeric **IP address** your device actually connects to. A **resolver** is the DNS server that answers that lookup. By default your router passes lookups to your internet provider's resolver. Changing the DNS setting tells it to ask a different resolver, such as Cloudflare's, Google's or Quad9's.

DNS happens before a page loads and carries very little data. That is why it can affect the first moment of a page load but not your download speed. If pages are slow only on Wi-Fi, start with our guides on [why Wi-Fi is slow when the internet is fast]({{< relref "/guides/wifi-slow-but-internet-fast" >}}) and [how to fix slow Wi-Fi]({{< relref "/guides/how-to-fix-slow-wifi" >}}).

## What are the Cloudflare, Google and Quad9 DNS addresses?

These are the IPv4 addresses as listed by each provider on October 11, 2026. Enter both the primary and secondary. Google advises using two different addresses and never the same one twice.

| Provider and option | What the provider says it does | Primary / secondary (IPv4) |
|---|---|---|
| Cloudflare 1.1.1.1 | Standard lookups, no content filtering | 1.1.1.1 / 1.0.0.1 |
| Cloudflare 1.1.1.2 | Blocks known malware and phishing | 1.1.1.2 / 1.0.0.2 |
| Cloudflare 1.1.1.3 | Blocks malware and adult content | 1.1.1.3 / 1.0.0.3 |
| Google Public DNS | Standard public resolver | 8.8.8.8 / 8.8.4.4 |
| Quad9 recommended | Malware blocking and DNSSEC validation | 9.9.9.9 / 149.112.112.112 |
| Quad9 without blocking | No malware blocking, DNSSEC validation; labeled "for experts only" | 9.9.9.10 / 149.112.112.10 |

IPv6 addresses are listed on each provider's page. Quad9 states that DNSSEC validation is enabled on all of its addresses. **DNSSEC** (DNS Security Extensions) is a way for a resolver to check that an answer was not forged on the way. Quad9 also advises entering every address listed for the service you choose, so a failure on one path doesn't leave you unprotected.

"Blocks known malware" means a list-based filter. It reduces exposure to known bad domains and does not replace antivirus or a patched router. A filtering option can also block a site you need, in which case switch to the unfiltered address to test.

## What do the providers say about logging?

This is the main reason to prefer one over another, and the statements differ in detail.

| Provider | Statement | Source date |
|---|---|---|
| Cloudflare | Deletes public resolver logs within 25 hours. Source IP addresses are not kept in non-volatile storage, except randomly sampled packets from at most 0.05% of traffic for troubleshooting and attack mitigation. Says it won't sell or share users' personal data or use it for ads. Aggregated data may be kept indefinitely. | Page header May 6, 2026 (body text dated March 27, 2024) |
| Google | Temporary logs, the only logs storing your IP address together with your query, are subject to deletion within 24 to 48 hours. Permanent logs replace the IP with a city or region and, Google says, contain no personal information. Says it doesn't correlate Public DNS logs with other personal information, except for security and abuse. | September 3, 2024 |

We did not review Quad9's privacy statement for this article, so we make no claim about its logging. These are the providers' own statements; we haven't audited them. The comparison is also not like for like: the two companies describe their logs in different terms.

## How do you change DNS on the router?

1. **Note your current DNS settings** first, or take a screenshot, so you can revert.
2. **Open your router's admin page or app** and look for "DNS" under Internet, WAN or LAN settings. Names vary. Google's guide says to replace the existing addresses with the new ones, save, restart your browser, and test.
3. **Enter a primary and secondary** from the table. Don't mix filtered and unfiltered addresses, because the router may use either at any time.
4. **Test.** Reload a few sites. If nothing loads, revert.

If your internet provider's equipment hard-codes its DNS servers, Google says you can't change them on the router and have to set DNS on each connected computer instead. We haven't verified which providers lock the setting, so check your own gateway.

## Is encrypted DNS (DoH or DoT) worth turning on?

Normal DNS lookups travel unencrypted, so anyone along the path can read them. **DoH** (DNS over HTTPS) wraps the lookup in encryption using the same port as web traffic. It is defined in RFC 8484, a Proposed Standard published in October 2018. **DoT** (DNS over TLS) does the same using TLS, the encryption behind HTTPS. Quad9 lists both for its services, for example `https://dns.quad9.net/dns-query` for DoH and `tls://dns.quad9.net` for DoT.

Where you can set it, as documented by the vendors:

- **Chrome:** the "Use secure DNS" setting is on in automatic mode by default and falls back to an unencrypted lookup if it has trouble. If you choose a custom provider, Chrome doesn't fall back. It isn't available on managed devices or with parental controls on.
- **Windows:** Microsoft's documentation, written for Windows Server 2022, says the DNS client supports DoH when the configured DNS server is on a built-in list. Cloudflare, Google and Quad9 are on it. Settings include "Encrypted only", which fails if the server can't do DoH, and "Encrypted preferred", which silently falls back to plain text. We did not test Windows 11 and haven't verified that its screens match.
- **Android 9 or later:** Google says Private DNS uses DoT, with `dns.google` as the hostname. It has no effect while a VPN or DNS-changer app is active.
- **Routers and base macOS, Windows and ChromeOS:** Google says its DoT isn't supported natively on those, so don't assume your router can encrypt DNS.
- **iPhone:** Google says the DNS change on iOS applies only to the specific Wi-Fi network, not other networks or cellular data.

### What encrypted DNS does not do

This part is our analysis, not a provider claim. Encryption stops other parties on the path from reading your lookups. It doesn't remove the resolver from the picture, since the resolver sees every query. Your internet provider can still see the IP addresses your devices connect to, so encrypted DNS doesn't make browsing private from it. A VPN changes who sees your traffic, and our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) explains why a VPN doesn't secure the router itself.

## Which option should you choose?

| If you want | Reasonable choice | Why |
|---|---|---|
| To try a change with no filtering | Cloudflare 1.1.1.1 or Google 8.8.8.8 | Both are plain resolvers; compare the logging statements above |
| Basic protection from known malicious domains | Cloudflare 1.1.1.2 or Quad9 9.9.9.9 | Both state that they block known malware |
| Adult-content blocking for a household | Cloudflare 1.1.1.3 | The only option here with that stated filter. It is not a substitute for parental controls |
| To avoid changing anything | Keep your provider's DNS | It works, and the change is optional |
| Encrypted lookups on one device | Set DoH in the browser or OS | Router-level encryption isn't generally available |

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Cloudflare's standard, malware-blocking and family resolvers use 1.1.1.1/1.0.0.1, 1.1.1.2/1.0.0.2 and 1.1.1.3/1.0.0.3 | [Cloudflare Docs: IP addresses](https://developers.cloudflare.com/1.1.1.1/ip-addresses/) | Verified as of October 11, 2026 |
| Google Public DNS uses 8.8.8.8 and 8.8.4.4; some provider equipment hard-codes DNS; Android Private DNS uses `dns.google`; iOS change applies to one Wi-Fi network | [Google: Using Google Public DNS, updated September 3, 2024](https://developers.google.com/speed/public-dns/docs/using) | Qualified: page is from 2024 |
| Quad9's recommended service is 9.9.9.9 / 149.112.112.112 with malware blocking, DNSSEC validation on all addresses, and DoH/DoT hostnames as listed | [Quad9 service addresses](https://quad9.net/service/service-addresses-and-features/) | Verified as of October 11, 2026 |
| Cloudflare deletes public resolver logs within 25 hours and says it won't sell or share users' personal data | [Cloudflare Docs: Public Resolver privacy](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/) | Qualified: the provider's own statement; page header dated May 6, 2026, body dated March 27, 2024 |
| Google's temporary logs, which hold IP and query together, are deleted within 24 to 48 hours; permanent logs have the IP replaced with a location | [Google: Public DNS privacy, updated September 3, 2024](https://developers.google.com/speed/public-dns/privacy) | Qualified: the provider's own statement, not audited |
| DoH is specified in RFC 8484, a Proposed Standard from October 2018 | [IETF RFC 8484](https://www.rfc-editor.org/rfc/rfc8484) | Verified |
| Cloudflare's DoH uses port 443 | [Cloudflare Docs: DNS over HTTPS](https://developers.cloudflare.com/1.1.1.1/encryption/dns-over-https/) | Verified as of October 11, 2026 |
| Chrome's secure DNS is on in automatic mode by default, falls back to unencrypted lookups in that mode, and doesn't fall back with a custom provider | [Chrome Help](https://support.google.com/chrome/answer/10468685) | Verified as of October 11, 2026 |
| Windows Server 2022 supports DoH for servers on a known list that includes Cloudflare, Google and Quad9 | [Microsoft Learn, updated April 25, 2025](https://learn.microsoft.com/en-us/windows-server/networking/dns/doh-client-support) | Qualified: documents Windows Server 2022, not Windows 11 |
| Encrypted DNS doesn't hide connected IP addresses from your internet provider | Our analysis | Qualified: explanation, not a provider claim |

## Bottom line

Leave your DNS alone unless you have a reason. Good reasons are wanting known-malware blocking at the router (Cloudflare 1.1.1.2 or Quad9 9.9.9.9) or preferring a resolver whose logging statement you like better than your provider's. Set it on the router, enter two matching addresses, test, and keep your old settings handy. Treat encrypted DNS as a per-device extra, and don't expect it to make your browsing private from your internet provider.
