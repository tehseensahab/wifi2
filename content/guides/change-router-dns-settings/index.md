---
title: "Should You Change Your Router's DNS? How and When It Helps"
date: 2026-10-11
description: "Changing your router's DNS can add malware blocking or privacy terms you prefer. It rarely makes the internet faster. How to choose a service and switch."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "security-privacy"]
tags: ["dns", "router-settings", "cloudflare", "google-public-dns", "quad9", "malware-blocking"]
summary: "Change your router's DNS if you want features your provider's DNS doesn't offer, mainly blocking known malicious sites or a published privacy policy you prefer. Don't expect faster downloads; DNS only affects the lookup before a connection starts. Set it once on the router and every device on the network uses it."
imageAlt: "Server racks with orange and blue network cables and green status lights"
imageCredit: "Photo: Taylor Vick / [Unsplash](https://unsplash.com/photos/M5tzZtFCOfs)"
takeaways:
  - "DNS turns website names into the numeric addresses computers use. Your provider assigns its own DNS servers by default, and Netgear notes most providers supply them automatically."
  - "Cloudflare (1.1.1.1), Google (8.8.8.8) and Quad9 (9.9.9.9) run free public DNS services. Quad9's standard service and Cloudflare's 1.1.1.2 block known malicious domains; Google's does not filter."
  - "Each publishes different log policies. Cloudflare says it deletes resolver logs within 25 hours, Google within 24 to 48 hours, and Quad9 says it does not record user IP addresses."
  - "Google warns that some providers hard-code their DNS servers into the equipment they supply, which can stop you changing it on the router."
faq:
  - q: "Will changing DNS make my internet faster?"
    a: "Usually not in a way you'd notice for downloads or streaming. DNS affects only the lookup at the start of a connection. Google says lookups can slow pages that load content from many domains, but a faster DNS server doesn't raise your connection speed."
  - q: "What is the best DNS server?"
    a: "It depends on what you want. For malware blocking, Quad9's 9.9.9.9 or Cloudflare's 1.1.1.2. For a plain resolver with no filtering, Cloudflare's 1.1.1.1 or Google's 8.8.8.8. For blocking adult content too, Cloudflare's 1.1.1.3. Compare each provider's privacy policy as well."
  - q: "Should I change DNS on the router or on each device?"
    a: "On the router, if you want every device covered, including smart TVs and other devices with no DNS setting. Change it on a single device only if that device needs something different."
  - q: "Why can't I change DNS on my provider's gateway?"
    a: "Google notes that some internet providers hard-code their DNS servers into the equipment they supply. If yours does, you can set DNS on your own router placed behind the gateway, or on individual devices."
  - q: "Is it safe to change DNS settings?"
    a: "Yes, if you write down your current settings first so you can switch back. Google recommends recording the existing addresses before you change anything."
sources:
  - title: "IP addresses"
    publisher: "Cloudflare 1.1.1.1 docs"
    url: "https://developers.cloudflare.com/1.1.1.1/ip-addresses/"
  - title: "Set up Cloudflare 1.1.1.1 resolver"
    publisher: "Cloudflare 1.1.1.1 docs"
    url: "https://developers.cloudflare.com/1.1.1.1/setup/"
  - title: "1.1.1.1 Public DNS Resolver"
    publisher: "Cloudflare 1.1.1.1 docs"
    url: "https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/"
  - title: "Get Started | Public DNS"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/docs/using"
  - title: "Your Privacy | Public DNS"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/privacy"
  - title: "Performance Benefits | Public DNS"
    publisher: "Google for Developers"
    url: "https://developers.google.com/speed/public-dns/docs/performance"
  - title: "Service Addresses & Features"
    publisher: "Quad9"
    url: "https://www.quad9.net/service/service-addresses-and-features"
  - title: "Data and Privacy Policy"
    publisher: "Quad9"
    url: "https://www.quad9.net/privacy/policy/"
  - title: "How do I set up custom DNS servers with eero?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/how-do-i-set-up-custom-dns-servers-with-eero"
  - title: "How do I set static Domain Name System servers on my NETGEAR router?"
    publisher: "Netgear Support"
    url: "https://kb.netgear.com/30510/How-do-I-set-static-Domain-Name-System-servers-on-my-NETGEAR-router"
---

Change your router's DNS if you want something your internet provider's DNS doesn't give you: blocking of known malicious websites, filtering for a family network, or a privacy policy you prefer. Don't change it expecting faster downloads. DNS handles the lookup before a connection starts, not the connection itself.

This is a how-to based on the DNS providers' and router makers' own documentation. We have not measured DNS speeds for this guide.

## What does DNS do?

DNS stands for Domain Name System. When you type a website name, your device asks a DNS server for the site's numeric IP address, then connects to that address. It works like a phone book lookup before the call.

By default your router uses DNS servers assigned by your internet provider, and passes them on to every device that joins your network. Netgear's support notes that "most ISPs supply DNS addresses automatically." Changing the DNS setting on the router changes it for every device that gets its settings from the router, including smart TVs and other devices with no DNS option of their own.

## Will changing DNS make my internet faster?

Not your download speed. Once the lookup finishes, the connection runs at the speed your plan and Wi-Fi allow, whichever DNS server answered.

Lookups can still add delay to page loading. Google's Public DNS documentation says "DNS lookups significantly impact website loading speed," especially on pages that pull content from many domains, and gives an example in which five lookups made up several seconds of an 11-second page load. That example is Google's own illustration, not a measurement of any particular DNS provider. Whether a different server is quicker than your provider's depends on where you are and which servers are closer, so if speed is your reason, test before and after rather than assuming.

For streaming, gaming and downloads, see [how much internet speed you need]({{< relref "/guides/how-much-internet-speed-do-i-need" >}}) and [why Wi-Fi can be slow when your internet is fast]({{< relref "/guides/wifi-slow-but-internet-fast" >}}).

## Which public DNS should I choose?

Three widely used free services, with their own published details:

| Service | Primary and secondary IPv4 | Filtering | What the provider says about logs |
|---|---|---|---|
| Cloudflare 1.1.1.1 | 1.1.1.1 and 1.0.0.1 | None | Resolver logs deleted within 25 hours; client IPs not stored in non-volatile storage; data not sold |
| Cloudflare 1.1.1.1 for Families, malware | 1.1.1.2 and 1.0.0.2 | Blocks malware | Same commitments as standard 1.1.1.1 |
| Cloudflare 1.1.1.1 for Families, malware and adult content | 1.1.1.3 and 1.0.0.3 | Blocks malware and adult content | Same commitments as standard 1.1.1.1 |
| Google Public DNS | 8.8.8.8 and 8.8.4.4 | None | Temporary logs with IP addresses deleted within 24 to 48 hours; permanent logs contain no personal information |
| Quad9 | 9.9.9.9 and 149.112.112.112 | Blocks malware; validates DNSSEC | Says it "does not collect or record user IP addresses"; run by a Swiss foundation |

All three also publish IPv6 addresses. For Cloudflare's standard service they are 2606:4700:4700::1111 and 2606:4700:4700::1001; for Google, 2001:4860:4860::8888 and 2001:4860:4860::8844.

How to choose:

- **For protection from known malicious sites,** use a filtering option: Quad9's 9.9.9.9 or Cloudflare's 1.1.1.2. Quad9 also offers 9.9.9.10 without malware blocking, which it labels "for experts only!"
- **For a family network,** Cloudflare's 1.1.1.3 adds adult-content blocking.
- **For no filtering at all,** use Cloudflare's 1.1.1.1 or Google's 8.8.8.8.
- **For privacy,** read each provider's policy in full. The summaries above are their own statements, and we have not audited them.

DNS filtering is one layer, not a security system. It only blocks domains already on the provider's lists, and devices set to use their own DNS bypass the router's setting. Pair it with the basics in our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}).

## How do I change DNS on my router?

Before you start, write down the DNS addresses your router uses now. Google recommends recording your current settings so you can switch back. Enter two addresses, a primary and a secondary from the same service, and don't use the same address in both fields.

### eero

1. Open the eero app and tap **Settings**.
2. Tap **Advanced networking**, then **DNS**.
3. Turn on **Custom DNS** and enter the IPv4 and, if you want, IPv6 addresses.
4. Tap **Save**. Eero says the network reboots to push the change to devices.

If DNS settings are grayed out, eero says to turn off eero Plus filters, Advanced Security and Ad Blocking first, under **Home**, **Security & privacy**, **Network Controls**.

### Netgear

1. Browse to **routerlogin.net** and sign in.
2. Go to **BASIC**, then **Internet**.
3. Under **Domain Name Server (DNS) Address**, select **Use These DNS Servers**.
4. Enter the **Primary DNS** and **Secondary DNS**, then click **Apply**.

### Other routers and provider gateways

Google notes that "every router uses a different user interface for configuring DNS server settings." Look in the router's app or admin page for DNS under Internet, WAN or advanced network settings.

Some provider gateways won't let you change DNS. Google warns that "some ISPs hard-code their DNS servers into the equipment they provide." If that's your situation, set DNS on your own router placed behind the gateway, or on individual devices. Our guide to [buying your own router vs. using your provider's]({{< relref "/guides/buy-your-own-router-vs-isp-equipment" >}}) covers that setup.

## How do I check it worked?

After the change, restart a device or reconnect it to Wi-Fi so it picks up the new settings, then:

- **Visit a few sites** to confirm they load. If nothing loads, recheck the addresses for typos.
- **Check the device's network details** for the DNS servers it received. Some routers hand out their own address and forward lookups to your chosen servers; eero does this with some features turned on, so you may see the router's address instead.
- **If you chose a filtering service,** the provider may offer a way to confirm you're using it. Quad9, for example, links to a tool for searching blocked domains.

If something breaks, enter the addresses you wrote down, or switch the router back to getting DNS automatically.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Cloudflare's standard resolver uses 1.1.1.1 and 1.0.0.1, with IPv6 2606:4700:4700::1111 and ::1001 | [Cloudflare docs](https://developers.cloudflare.com/1.1.1.1/ip-addresses/) | Verified as of October 11, 2026 |
| 1.1.1.2/1.0.0.2 block malware and 1.1.1.3/1.0.0.3 block malware and adult content, with the same privacy commitments | [Cloudflare docs](https://developers.cloudflare.com/1.1.1.1/setup/) | Verified as of October 11, 2026 |
| Cloudflare deletes resolver logs within 25 hours, doesn't store client IPs in non-volatile storage and doesn't sell users' personal data | [Cloudflare privacy commitments](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/) | Qualified: the provider's own statement; we have not audited it |
| Google Public DNS uses 8.8.8.8 and 8.8.4.4; some ISPs hard-code DNS into their equipment; record current settings first | [Google Public DNS, Get Started](https://developers.google.com/speed/public-dns/docs/using) | Verified as of October 11, 2026 |
| Google deletes temporary logs with IP addresses within 24 to 48 hours; permanent logs contain no personal information | [Google Public DNS privacy](https://developers.google.com/speed/public-dns/privacy) | Qualified: the provider's own statement |
| DNS lookups can slow page loading; Google's example attributes several seconds of an 11-second load to five lookups | [Google Public DNS, Performance Benefits](https://developers.google.com/speed/public-dns/docs/performance) | Qualified: an illustrative example, not a measurement of any provider |
| Quad9 uses 9.9.9.9 and 149.112.112.112 with malware blocking and DNSSEC; 9.9.9.10 has no blocking | [Quad9 service addresses](https://www.quad9.net/service/service-addresses-and-features) | Verified as of October 11, 2026 |
| Quad9 says it does not collect or record user IP addresses and is run by a Swiss foundation | [Quad9 privacy policy](https://www.quad9.net/privacy/policy/) | Qualified: the provider's own statement |
| eero custom DNS steps and the requirement to turn off eero Plus filters first | [eero Support](https://eero.com/support/articles/how-do-i-set-up-custom-dns-servers-with-eero) | Verified as of October 11, 2026 |
| Netgear static DNS steps; most providers supply DNS automatically | [Netgear Support](https://kb.netgear.com/30510/How-do-I-set-static-Domain-Name-System-servers-on-my-NETGEAR-router) | Verified as of October 11, 2026 |

## Bottom line

Changing your router's DNS is quick, reversible and covers every device on the network. Do it for malware or content filtering, or for a privacy policy you prefer, and pick the service by those features. Don't do it to fix slow speeds; check your plan and Wi-Fi for that. Write down your current settings before you start.
