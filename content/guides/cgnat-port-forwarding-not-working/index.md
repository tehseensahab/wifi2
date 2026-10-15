---
title: "Port Forwarding Not Working? Check for CGNAT First"
date: 2026-10-15
description: "Carrier-grade NAT puts many customers behind one public IPv4 address, so forwarded ports can't work. How to check for it, how it differs from double NAT, and your options."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "internet-plans-isps"]
tags: ["cgnat", "port-forwarding", "nat", "ipv6", "double-nat", "remote-access"]
summary: "If port forwarding never works no matter how you set it up, your internet provider may be using carrier-grade NAT (CGNAT), which puts many customers behind shared public IPv4 addresses. Check your router's WAN address: one in 100.64.0.0 to 100.127.255.255 points to CGNAT. Then compare it with the address a what-is-my-IP site shows. Your options are to ask your provider about a public IPv4 address, use IPv6, or use a tunnel or relay."
imageAlt: "Server racks with orange and blue network cables and green status lights"
imageCredit: "Photo: Taylor Vick / [Unsplash](https://unsplash.com/photos/M5tzZtFCOfs)"
takeaways:
  - "Carrier-grade NAT (CGNAT) is NAT run by your internet provider, so your router does not get a public IPv4 address of its own. Forwarding a port on your router can't make an outside device reach you."
  - "RFC 6598 (April 2012) reserved the block 100.64.0.0/10, which is 100.64.0.0 to 100.127.255.255, for provider CGNAT. A router WAN address in that block strongly suggests CGNAT."
  - "A WAN address starting with 10., 172.16. to 172.31. or 192.168. is a different case: it usually means double NAT, with another router in front of yours."
  - "Options: ask your provider whether it offers a public IPv4 address, use IPv6 with a firewall rule, or use a service that connects out from your home. We did not verify any specific provider's policy for this article."
faq:
  - q: "What is CGNAT?"
    a: "Carrier-grade NAT is Network Address Translation performed by your internet provider. Many customers share one public IPv4 address, and the provider's equipment translates between those shared addresses and the private ones inside its network."
  - q: "How do I know if I'm behind CGNAT?"
    a: "Find the WAN or Internet address in your router's admin page or app. If it falls from 100.64.0.0 to 100.127.255.255, that is the block reserved for CGNAT. If it differs from the address a what-is-my-IP website shows for your connection, something between you and the internet is translating addresses."
  - q: "Is CGNAT the same as double NAT?"
    a: "No. Double NAT means two routers in your own home network translate addresses, usually your router behind the provider's gateway. CGNAT means the provider translates addresses before they reach you. Both stop port forwarding from working end to end, but the fixes differ."
  - q: "Can I fix CGNAT with a better router or by changing settings?"
    a: "Not on your side alone. The translation happens in your provider's network, outside your router. A router can help only with the parts you control, such as IPv6 settings."
  - q: "Does IPv6 get around CGNAT?"
    a: "It can for devices and services that support IPv6, because IPv6 does not rely on shared addresses. Home gateways are also advised to block unsolicited inbound IPv6 traffic by default (RFC 6092), so you still need to allow the traffic you want."
sources:
  - title: "RFC 6598: IANA-Reserved IPv4 Prefix for Shared Address Space"
    publisher: "Internet Engineering Task Force"
    url: "https://www.rfc-editor.org/rfc/rfc6598"
    date: 2012-04-01
  - title: "RFC 6888: Common Requirements for Carrier-Grade NATs (CGNs)"
    publisher: "Internet Engineering Task Force"
    url: "https://www.rfc-editor.org/rfc/rfc6888"
    date: 2013-04-01
  - title: "RFC 6887: Port Control Protocol (PCP)"
    publisher: "Internet Engineering Task Force"
    url: "https://www.rfc-editor.org/rfc/rfc6887"
    date: 2013-04-01
  - title: "RFC 1918: Address Allocation for Private Internets"
    publisher: "Internet Engineering Task Force"
    url: "https://www.rfc-editor.org/rfc/rfc1918"
    date: 1996-02-01
  - title: "RFC 6092: Recommended Simple Security Capabilities in Customer Premises Equipment for Providing Residential IPv6 Internet Service"
    publisher: "Internet Engineering Task Force"
    url: "https://www.rfc-editor.org/rfc/rfc6092"
    date: 2011-01-01
  - title: "How NAT traversal works"
    publisher: "Tailscale"
    url: "https://tailscale.com/blog/how-nat-traversal-works"
    date: 2020-08-21
---

If you have set up port forwarding correctly and outside connections still never reach your device, your internet provider may be running carrier-grade NAT (CGNAT). With CGNAT your router does not own a public IPv4 address, so there is nothing for the outside world to connect to, and no router setting can change that. You can check in about two minutes, and there are three practical ways around it.

This guide is a research-based explanation built on the internet standards documents (RFCs) that define CGNAT and on one vendor's technical write-up. We have not tested these setups on any provider's network. We tried to read Starlink's and T-Mobile's official support pages for provider-specific details, but could not access them, so we say nothing about what any named provider does. Ask your provider.

## What is CGNAT, and why does it break port forwarding?

NAT (Network Address Translation) lets many devices share one public address. Your router normally does this: it holds the single public IPv4 address your provider gave you, and your devices use private addresses behind it. Port forwarding tells the router, "send anything arriving on port X to this device."

With CGNAT, the provider adds a second layer of this inside its own network. Many customers share a public IPv4 address, and your router gets a shared or private address instead. A forwarding rule on your router can't help, because the outside world connects to the provider's shared address and the provider's equipment decides where traffic goes.

The standards body that wrote the CGNAT requirements, the IETF, is direct about the cost. RFC 6888 (April 2013) says CGNs "introduce substantial limitations in communications" between subscribers and the rest of the internet, and that some applications "may not function at all" in that environment. It also notes that some games and peer-to-peer applications need a specific filtering behavior from the NAT to work.

Providers use CGNAT because public IPv4 addresses are scarce. RFC 6598 (April 2012) notes that public IPv4 space is too scarce for every provider to get a unique allocation.

## How do I check whether I'm behind CGNAT?

1. **Find your router's WAN address.** Open the router's admin page or app and look under Internet, WAN or Status. This is the address your router gets from the provider side.
2. **Compare it with your public address.** Search "what is my IP" in a browser on a device on your network, and note the address it shows.
3. **Read the result with this table.**

| What your router's WAN address looks like | Likely meaning | Source |
|---|---|---|
| 100.64.0.0 to 100.127.255.255 | CGNAT. This is the block reserved for provider CGNAT, 100.64.0.0/10. | RFC 6598 |
| 10.x.x.x, 172.16.x.x to 172.31.x.x, or 192.168.x.x | A private address, which usually means another router or gateway is in front of yours (double NAT). Sometimes a provider uses private space for CGNAT. | RFC 1918 |
| A public address that matches what the what-is-my-IP site shows | Your router likely has the public address itself, so CGNAT is unlikely. | Our reasoning |
| A public address that does not match | Something between your router and the internet is translating addresses. Ask your provider. | Our reasoning |

The address block 100.64.0.0/10 is the "/10" notation for 4,194,304 addresses starting at 100.64.0.0. In dotted form the range ends at 100.127.255.255, which is why the second number in the address (64 to 127) is the quick tell.

Two limits on this check. First, RFC 6598 says the block is meant for the links between provider CGN equipment and customer equipment, but a provider could still use other ranges, so an address outside it doesn't prove there is no CGNAT. Second, if you see a private address because you plugged your own router behind the provider's gateway, that is the double NAT case, covered in our [bridge mode and double NAT guide]({{< relref "/guides/bridge-mode-double-nat-own-router" >}}). Fix that first. Putting the gateway in bridge mode removes your own layer of NAT but does not remove the provider's.

## What are my options?

**1. Ask your provider about a public IPv4 address.** This is the most direct fix if you need to host something or accept connections. Whether a provider offers it, on which plans and at what cost, varies, and we did not verify it for any provider. Ask for a public (not shared) IPv4 address, and ask whether it is static or can change.

**2. Use IPv6.** IPv6 is the newer address format; unlike IPv4, it does not rely on customers sharing addresses. If your provider gives you IPv6 and the service you want to reach supports it, outside devices can connect to a device's IPv6 address directly. Two caveats. Both ends need IPv6. And RFC 6092 (January 2011) recommends that home gateways do not forward unsolicited inbound traffic by default, so you will usually have to create an allow rule in the router's IPv6 firewall for the specific device and port. Check that your router supports IPv6 and has it turned on; menus vary.

**3. Connect outward instead of inward.** CGNAT mainly blocks connections that start from outside. Connections that start from inside work. Remote-access tools such as VPN-style "overlay" networks use this. Tailscale's technical write-up (August 21, 2020, from a company that sells such a service) says that, aside from port mapping protocols, its techniques work in a CGNAT environment, with direct connections often possible using a technique where each device learns its public address from an outside server, with a relay server as a last-resort fallback when a direct connection fails. It notes that relayed traffic can add some latency and may reduce bandwidth. Other vendors' services work differently; check each one's documentation and pricing.

**A technical option that isn't dependable.** There is a standard, the Port Control Protocol (PCP, RFC 6887, April 2013), that lets a device ask a NAT to open an inbound mapping, and it was designed with CGNAT in mind. Whether a provider's CGNAT supports it is up to the provider. Tailscale's write-up says protocols of this kind can't be relied on to be present.

## Do I need to worry about security if I open something up?

Yes. Getting inbound access makes a device reachable from the internet. RFC 6092 itself cautions that a gateway's filtering is not a substitute for security on the devices behind it. Open the specific port for one device, keep that device updated, and use strong passwords. Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) covers the basics, and our guide to [WPS and UPnP]({{< relref "/guides/should-you-disable-wps-and-upnp" >}}) explains why automatic port opening is a trade-off.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| RFC 6598 (April 2012) reserves 100.64.0.0/10 as Shared Address Space for Carrier-Grade NAT use, to number links between CGN and customer equipment | [RFC 6598](https://www.rfc-editor.org/rfc/rfc6598) | Verified as of October 15, 2026 |
| 100.64.0.0/10 spans 100.64.0.0 to 100.127.255.255 and holds 4,194,304 addresses (2^22) | Our arithmetic from the /10 prefix | Verified by calculation |
| Public IPv4 space is too scarce for every provider to get a unique allocation | [RFC 6598](https://www.rfc-editor.org/rfc/rfc6598) | Verified |
| CGNs "introduce substantial limitations in communications"; some applications "may not function at all"; some games and peer-to-peer applications need endpoint-independent filtering | [RFC 6888, April 2013](https://www.rfc-editor.org/rfc/rfc6888) | Verified |
| Private IPv4 ranges are 10/8, 172.16/12 and 192.168/16 | [RFC 1918, February 1996](https://www.rfc-editor.org/rfc/rfc1918) | Verified |
| Home IPv6 gateways should not forward unsolicited inbound traffic by default; gateway filtering is not a substitute for host security | [RFC 6092, January 2011](https://www.rfc-editor.org/rfc/rfc6092) | Qualified: Informational recommendations, and products vary; the RFC also allows a transparent mode that may be default |
| PCP lets a host control how incoming packets are translated and forwarded, and is designed for CGNs and small NATs | [RFC 6887, April 2013](https://www.rfc-editor.org/rfc/rfc6887) | Verified; whether a provider supports it is not established |
| Tailscale says direct connections usually work behind CGNAT without port forwarding, with relays as fallback that can add latency | [Tailscale, August 21, 2020](https://tailscale.com/blog/how-nat-traversal-works) | Qualified: vendor source, 2020; applies to Tailscale's approach |
| A WAN address in 100.64.0.0/10 suggests CGNAT; a private WAN address usually means double NAT; matching public addresses suggest no CGNAT | Our reasoning from RFC 6598 and RFC 1918 | Qualified: an inference, not a certainty; providers may use other ranges |
| Provider-specific policies (public IP availability, price, port forwarding) | Not covered | Not stated in this article; official provider pages were inaccessible to us |

## Bottom line

If port forwarding fails despite correct settings, look at your router's WAN address before changing anything else. An address between 100.64.0.0 and 100.127.255.255 means your provider is doing the translating, and the fix has to come from a public IPv4 address from your provider, IPv6, or a connect-outward service. If the address is private but outside that range, look for double NAT in your own home first.
