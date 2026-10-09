---
title: "What Is DNS, and Should You Change Your Router's DNS Server?"
date: 2026-10-09
description: "DNS turns website names into addresses. Compare Google, Cloudflare and Quad9 public DNS, their logging policies, and how to change DNS on your router."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "security-privacy"]
tags: ["dns", "router-settings", "cloudflare-1-1-1-1", "google-public-dns", "quad9", "dns-filtering"]
summary: "DNS is the lookup that turns a site name into an address. Your router uses your internet provider's DNS server by default. Switching to Google (8.8.8.8), Cloudflare (1.1.1.1) or Quad9 (9.9.9.9) takes a few minutes in the router's settings and applies to every device, but none of the three publishes a speed guarantee, and some providers lock the setting. Pick one for its filtering and logging policy, not for a promised speed boost. This is a research-based guide, not a hands-on test."
imageAlt: "Close-up of an Ethernet port with two green status lights on a small gray adapter sitting on a dark wooden surface"
imageCredit: "Photo: Jesse Ayegba / [Unsplash](https://unsplash.com/photos/a-close-up-of-a-router-on-a-table-o-qB6ikmn8w)"
takeaways:
  - "Google Public DNS uses 8.8.8.8 and 8.8.4.4. Cloudflare's standard resolver uses 1.1.1.1 and 1.0.0.1. Quad9's malware-blocking service uses 9.9.9.9 and 149.112.112.112. Each provider recommends entering two addresses."
  - "Changing DNS on the router applies to every device on the network, according to Cloudflare. Google warns that some internet providers hard-code their DNS servers into their equipment, which blocks the change."
  - "The three differ in filtering and logging. Cloudflare's standard resolver doesn't filter. Quad9's 9.9.9.9 blocks malicious domains, and its 9.9.9.10 does not. Google says temporary logs holding IP addresses are deleted within 24 to 48 hours; Cloudflare says it deletes its resolver logs within 25 hours."
  - "None of the pages we read promises faster browsing. DNS affects the lookup before a page loads, not the download itself, so expect little change in speed tests."
faq:
  - q: "Will changing my DNS make my internet faster?"
    a: "Not in the sense of a higher speed-test result. DNS only handles the name lookup, which happens before a page or app starts loading. A slow resolver can add delay to that first step, but none of the Google, Cloudflare or Quad9 pages we reviewed gives a measured speed improvement, and we have not tested any."
  - q: "What DNS settings should I use?"
    a: "For unfiltered lookups, Cloudflare lists 1.1.1.1 and 1.0.0.1, and Google lists 8.8.8.8 and 8.8.4.4. For lookups that block known malicious domains, Quad9 lists 9.9.9.9 and 149.112.112.112, and Cloudflare lists 1.1.1.2 and 1.0.0.2. Enter at least two addresses; Google says two give the most reliable service."
  - q: "Is it safe to use a public DNS server?"
    a: "It moves trust from your internet provider to the DNS company, since it sees the domain names your devices look up. Google, Cloudflare and Quad9 each publish a privacy statement. Compare retention before you choose. CISA, the US cybersecurity agency, lists all three as examples of encrypted DNS services in guidance written for highly targeted individuals."
  - q: "What if my router won't let me change DNS?"
    a: "Google notes some internet providers hard-code their DNS servers into their equipment. If your provider's gateway locks the setting, you can set DNS on each device, or on your own router connected behind the gateway. We haven't tested specific provider gateways."
  - q: "Does changing DNS hide my browsing from my internet provider?"
    a: "No. Your provider still carries your traffic and sees the addresses you connect to. Encrypted DNS (DNS over HTTPS or DNS over TLS) keeps the lookups themselves from being read in transit. Entering plain IP addresses on a router doesn't turn encryption on."
  - q: "Should I use a filtered or an unfiltered resolver?"
    a: "Filtered services such as Quad9's 9.9.9.9 and Cloudflare's 1.1.1.2 block lookups for domains they list as malicious. That adds a layer of protection, not a guarantee. If a legitimate site is blocked or you need unfiltered results, Quad9 offers 9.9.9.10 and Cloudflare offers 1.1.1.1."
sources:
  - title: "Get started with Google Public DNS"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/docs/using"
    date: 2024-09-03
  - title: "Google Public DNS Privacy Statement"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/privacy"
    date: 2024-09-03
  - title: "1.1.1.1 IP addresses"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/ip-addresses/"
  - title: "1.1.1.1 for Families (setup)"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/setup/"
  - title: "Set up 1.1.1.1 on a router"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/setup/router/"
  - title: "Public DNS Resolver privacy"
    publisher: "Cloudflare Docs"
    url: "https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/"
  - title: "Quad9 documentation"
    publisher: "Quad9"
    url: "https://docs.quad9.net/"
  - title: "Quad9 services"
    publisher: "Quad9"
    url: "https://docs.quad9.net/services/"
  - title: "Mobile Communications Best Practice Guidance, version 2.0"
    publisher: "Cybersecurity and Infrastructure Security Agency (CISA)"
    url: "https://www.cisa.gov/sites/default/files/2025-12/guidance-mobile-communications-best-practices_508c.pdf"
    date: 2025-11-24
---

Changing your router's DNS server takes a few minutes, applies to every device at home, and can add filtering against known malicious sites. It does not raise your internet speed. If you try it, pick the service for its filtering and logging policy and keep your old settings written down so you can undo it.

This is a research-based guide built from the providers' own documentation and one US government guidance document. We have not benchmarked any DNS service, and none of the pages we reviewed publishes a measured speed advantage.

## What is DNS?

DNS stands for Domain Name System. It is the lookup that turns a name you type, like a website's address, into the numeric IP address a device needs to connect. The server that answers those lookups is called a resolver.

Your devices ask the resolver set on your router. By default that is usually your internet provider's resolver, assigned automatically when the router connects. You can replace it with a "public" resolver run by another company. Because the resolver sees which names your devices ask for, choosing one is a privacy and filtering decision as much as a technical one.

## Which public DNS services can you use?

These are the services the three companies document for ordinary use. Addresses come from each provider's own pages, checked on October 9, 2026.

| Service | IPv4 addresses | Filtering |
|---|---|---|
| Google Public DNS | 8.8.8.8 and 8.8.4.4 | None stated on the setup page |
| Cloudflare 1.1.1.1 (standard) | 1.1.1.1 and 1.0.0.1 | None: "fast, private DNS lookups with no content filtering" |
| Cloudflare malware blocking | 1.1.1.2 and 1.0.0.2 | Blocks malware domains |
| Cloudflare malware and adult content blocking | 1.1.1.3 and 1.0.0.3 | Blocks malware and adult content |
| Quad9 (recommended) | 9.9.9.9 and 149.112.112.112 | Blocks domains tied to malware, phishing and scams |
| Quad9 without threat blocking | 9.9.9.10 and 149.112.112.10 | None |

IPv6 addresses exist for all of them (for example, Google's 2001:4860:4860::8888 and Cloudflare's 2606:4700:4700::1111). Use them only if your connection supports IPv6; the provider pages list the full set. When Cloudflare's filtered services block a domain, they return the address 0.0.0.0, so the site simply fails to load.

Quad9 also lists 9.9.9.11 and 9.9.9.12, variants that add a feature called EDNS Client Subnet (ECS). Quad9 describes 9.9.9.11 as offering "better CDN performance". We don't cover these further because the pages we reviewed don't explain the privacy trade-off in enough detail for us to say who should use them.

## How do their privacy policies compare?

A resolver sees the domain names your household looks up, so retention matters. These are the providers' own statements; we can't verify that they are followed.

| Provider | What it says about logs | Source date |
|---|---|---|
| Google | Temporary logs, the only logs that hold both your IP address and your query, are subject to deletion within 24 to 48 hours. Google says it may keep some information from them longer for security and abuse issues. Permanent logs are a sample with IP addresses replaced by a city or region-level location. | Updated September 3, 2024 |
| Cloudflare | Deletes its public resolver logs within 25 hours, and says client IPs are not stored in non-volatile storage. Aggregated statistics may be kept indefinitely. Randomly sampled packets from "at most 0.05% of all traffic" may be captured for troubleshooting and attack mitigation. | Undated page, read October 9, 2026 |
| Quad9 | States it "will never log/record enduser IP addresses. Ever." It is based in Switzerland. | Undated page, read October 9, 2026 |

These statements aren't like for like. They describe different kinds of logs, so don't read "25 hours" against "24 to 48 hours" as a ranking. Read each full statement if privacy is your main reason for switching.

## Should you change it?

It makes sense in some situations and not in others.

| Your situation | Reasonable choice | Why |
|---|---|---|
| You want a layer of blocking against known malicious sites on every device, including smart devices | A filtered service (Quad9 9.9.9.9 or Cloudflare 1.1.1.2) | Filtering happens at the lookup, so it covers devices that can't run security software. It is not a complete defense. |
| You don't want your internet provider to see your DNS lookups | A public resolver with encryption, if your router supports it | A plain IP-address entry shifts who sees the lookups but doesn't encrypt them |
| Your provider's default DNS seems unreliable | Try a public resolver and compare | We can't say which will work better for you |
| Everything works and you have no filtering need | Leave it | There is no documented speed gain to chase |
| Your router doesn't allow DNS changes | Change it per device, or use your own router | Some provider equipment locks the setting, Google notes |

Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) lists DNS filtering as optional step 10, for the same reason.

## How do you change DNS on your router?

Menus differ by brand, so these are the steps all three providers' documentation share.

1. **Open the router's admin page.** Use the address printed on the router or in its app. Cloudflare gives 192.168.1.1 and 192.168.0.1 as common examples.
2. **Log in with the admin password.** If you never changed the default password, do that first; our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) covers it.
3. **Find the DNS settings.** Cloudflare says these may sit under WAN, IPv6, IP or Internet, depending on the maker.
4. **Write down the current addresses** before changing anything. Cloudflare advises saving them in case you need to restore them.
5. **Enter two addresses** from the table, a primary and a secondary. Google recommends configuring at least two.
6. **Save, then restart your browser or reconnect a device** and load a few sites to confirm everything still works.

Cloudflare says that setting 1.1.1.1 on a router "applies the DNS setting to every device on your network." Some devices have their own DNS settings that override the router, such as a phone using Android's Private DNS.

### What about phones and laptops?

Google's setup page describes per-device options. On an iPhone you can enter DNS servers for one Wi-Fi network, and Google notes this applies to that network and not to cellular data. On Android 9 or later, the setting is Private DNS, which uses DNS over TLS (encrypted lookups): enter the provider hostname `dns.google` for Google. Google says this setting has no effect while a VPN or third-party DNS app is active.

CISA's Mobile Communications Best Practice Guidance, version 2.0 (November 24, 2025), is written mainly for highly targeted individuals such as senior government, military or political figures. For them it recommends encrypted DNS from providers such as Cloudflare's 1.1.1.1, Google's 8.8.8.8 and Quad9's 9.9.9.9 on iOS, and Private DNS with one of those resolvers on Android. That's guidance for a specific high-risk audience, not a general rule for everyone.

## What can go wrong?

- **The router won't save the setting, or it reverts.** Google notes some internet providers hard-code DNS into their equipment.
- **A site stops loading after you pick a filtered service.** The resolver may be blocking it. Switch to an unfiltered address, such as Quad9's 9.9.9.10 or Cloudflare's 1.1.1.1, to test.
- **Mixing resolvers.** If you enter a filtered primary and an unfiltered secondary, lookups may fall back to the unfiltered one. Use two addresses from the same filtered service.
- **Expecting more speed.** DNS only affects the lookup. Slow Wi-Fi, a busy connection or a distant server are different problems; see [why Wi-Fi is slow when your internet is fast]({{< relref "/guides/wifi-slow-but-internet-fast" >}}).

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Google Public DNS IPv4 addresses are 8.8.8.8 and 8.8.4.4; Google recommends configuring at least two addresses; some providers hard-code DNS | [Google Public DNS setup, updated September 3, 2024](https://developers.google.com/speed/public-dns/docs/using) | Verified as of October 9, 2026 |
| On Android 9 or later, Google's setup uses Private DNS with hostname dns.google; it has no effect with a VPN or third-party DNS app active; the iOS setting applies only to that Wi-Fi network | [Google Public DNS setup](https://developers.google.com/speed/public-dns/docs/using) | Verified as of October 9, 2026 |
| Cloudflare's standard resolver uses 1.1.1.1 and 1.0.0.1 and has no content filtering | [Cloudflare 1.1.1.1 IP addresses](https://developers.cloudflare.com/1.1.1.1/ip-addresses/) | Verified as of October 9, 2026 |
| Cloudflare malware blocking uses 1.1.1.2 and 1.0.0.2; malware and adult content uses 1.1.1.3 and 1.0.0.3; blocked domains return 0.0.0.0 | [Cloudflare setup](https://developers.cloudflare.com/1.1.1.1/setup/) | Verified as of October 9, 2026 |
| Setting 1.1.1.1 on a router applies to every device; common router steps and the advice to save existing addresses | [Cloudflare router guide](https://developers.cloudflare.com/1.1.1.1/setup/router/) | Verified as of October 9, 2026 |
| Quad9 9.9.9.9 and 149.112.112.112 block malicious domains; 9.9.9.10 and 149.112.112.10 do not; 9.9.9.11 is described as "for better CDN performance" | [Quad9 services](https://docs.quad9.net/services/) | Verified as of October 9, 2026 |
| Quad9 says it "will never log/record enduser IP addresses" and is based in Switzerland | [Quad9 documentation](https://docs.quad9.net/) | Qualified: the provider's own statement, undated page |
| Google keeps temporary logs with IPs and queries and deletes them within 24 to 48 hours, and may keep some data longer for security and abuse | [Google Public DNS privacy, updated September 3, 2024](https://developers.google.com/speed/public-dns/privacy) | Qualified: the provider's own statement |
| Cloudflare deletes public resolver logs within 25 hours; samples at most 0.05% of traffic for troubleshooting; aggregated data may be kept indefinitely | [Cloudflare resolver privacy](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/) | Qualified: the provider's own statement, undated page |
| CISA v2.0 (November 24, 2025) recommends encrypted DNS from Cloudflare, Google or Quad9 on iOS, and Private DNS on Android, for highly targeted individuals | [CISA Mobile Communications Best Practice Guidance](https://www.cisa.gov/sites/default/files/2025-12/guidance-mobile-communications-best-practices_508c.pdf) | Qualified: written for a high-risk audience |
| What DNS is, that changing it doesn't raise speed-test results, and that plain IP entry on a router does not encrypt lookups | Our explanation, consistent with the sources above | Qualified: explanation, not a tested result |

## Bottom line

Change your DNS if you want filtering on every device or a different logging policy, not to speed up downloads. Write down your current settings, enter two addresses from the same service, and test a few sites afterward. If your provider's equipment blocks the change, the per-device options still work.
