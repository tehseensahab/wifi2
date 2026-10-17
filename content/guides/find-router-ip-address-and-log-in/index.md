---
title: "How to Find Your Router's IP Address and Log In to It"
date: 2026-10-17
description: "Find your router's IP address on a Mac or Windows PC, then log in. Login addresses and first-login rules for Netgear and ASUS, plus what to do if you lost the password."
authors: ["John Marshall"]
topics: ["how-to-fixes", "routers"]
tags: ["router-login", "ip-address", "default-gateway", "ipconfig", "netgear", "asus", "eero"]
summary: "Your router's address is the \"default gateway\" your computer reports: the Router line in macOS Wi-Fi details, or Default Gateway in the Windows ipconfig command. Type it into a browser while connected to that router. Netgear and ASUS also publish easy-to-type login names (routerlogin.net and asusrouter.com), and eero is managed in its app."
imageAlt: "MacBook on a wooden laptop stand on a desk, with a wireless keyboard and trackpad in front of it"
imageCredit: "Photo: Workperch / [Unsplash](https://unsplash.com/photos/tRjfyx6KKKw)"
takeaways:
  - "Your router's address is your computer's default gateway. On a Mac it is the Router line under System Settings, Wi-Fi, Details. On Windows, run ipconfig and read Default Gateway."
  - "Netgear says to open routerlogin.net or routerlogin.com, or the router's IP address, commonly 192.168.1.1 or 192.168.0.1. Netgear Orbi mesh systems use orbilogin.com."
  - "ASUS lists http://192.168.50.1 as an example address and http://www.asusrouter.com as its login URL. After a first setup or factory reset, ASUS requires you to create a username and password."
  - "Addresses starting with 192.168., 10. or 172.16. to 172.31. are private addresses reserved by RFC 1918. They only work inside your own network."
faq:
  - q: "What is my router's IP address?"
    a: "It is the default gateway your device reports. On a Mac, open System Settings, Wi-Fi, Details and read Router. On Windows, run ipconfig in Command Prompt and read Default Gateway. Common examples are 192.168.1.1 and 192.168.0.1, but your router may use a different address."
  - q: "Is 192.168.1.1 always the router address?"
    a: "No. Netgear says its routers commonly use 192.168.1.1 or 192.168.0.1, and ASUS uses 192.168.50.1 as its example. Other makers and internet providers use other addresses, so read the one your device reports."
  - q: "What is the default Netgear login?"
    a: "Netgear's login page says the default username is usually admin and the default password is usually password, and that the label on the bottom of the unit may list your router's credentials. If you changed them, use your own. Netgear says to change the default password after you log in."
  - q: "I forgot my router password. What now?"
    a: "Netgear says a factory reset may be needed if credentials are lost, and that a reset restores the default username and password printed on the router's label. A reset also erases your settings, including your Wi-Fi name and password."
  - q: "Why does the address I found open my internet provider's gateway instead of my own router?"
    a: "The default gateway is the first device your computer sends traffic to. If you are connected to a provider-supplied gateway, that is the address you see. If you added your own router behind it, connect to your own router's Wi-Fi or one of its LAN ports instead. See our bridge mode and double NAT guide."
sources:
  - title: "View Wi-Fi network settings (Mac): Details, IP address and Router"
    publisher: "Apple Support, Mac User Guide"
    url: "https://support.apple.com/guide/mac-help/mh11935"
  - title: "ipconfig"
    publisher: "Microsoft Learn"
    url: "https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig"
  - title: "How to Access Your NETGEAR Router Login Page"
    publisher: "NETGEAR"
    url: "https://www.netgear.com/hub/technology/router-login-page/"
    date: 2026-09-03
  - title: "[Wireless Router] How do I enter my ASUS router's setting page (Web GUI)?"
    publisher: "ASUS Support"
    url: "https://www.asus.com/support/FAQ/1005263"
    date: 2026-02-23
  - title: "Recommended settings for Wi-Fi routers and access points"
    publisher: "Apple Support"
    url: "https://support.apple.com/en-us/102766"
    date: 2026-07-14
  - title: "RFC 1918: Address Allocation for Private Internets"
    publisher: "IETF (RFC Editor)"
    url: "https://www.rfc-editor.org/rfc/rfc1918"
    date: 1996-02-01
---

Your router's address is the "default gateway" that your computer reports for the network it is on. On a Mac it is the **Router** line in the Wi-Fi details. On Windows, it is the **Default Gateway** line when you run `ipconfig`. Type that address into a web browser while you are connected to the router, and the login page should appear. Some brands also give you a name you can type instead of numbers.

This guide is based on Apple, Microsoft, Netgear and ASUS documentation. We have not logged in to these routers for this article, and menu names can differ by model and firmware.

## What is a router's IP address, and what is a default gateway?

An IP address is the number that identifies a device on a network. Your router has one on your home network, and your devices use it as the way out to the internet. A device's **default gateway** is the address it sends traffic to when the destination is outside the home network, which in a typical home is the router.

Microsoft's documentation says that run without parameters, `ipconfig` "displays Internet Protocol version 4 (IPv4) and IPv6 addresses, subnet mask, and default gateway for all adapters." Apple's Mac guide describes the same thing as "The router address for the Wi-Fi connection."

Home router addresses normally fall in the ranges the internet standard RFC 1918 reserves for private networks: 10.0.0.0 to 10.255.255.255, 172.16.0.0 to 172.31.255.255, and 192.168.0.0 to 192.168.255.255. These addresses only work inside your own network, so you must be connected to the router (by Wi-Fi or an Ethernet cable) to reach the login page.

## How to find the address on a Mac

Apple's Mac guide gives these steps:

1. Choose Apple menu, then **System Settings**, then click **Wi-Fi** in the sidebar.
2. Click **Details** next to your connected network.
3. Read the **Router** line. Apple describes it as "The router address for the Wi-Fi connection."

Menu names can differ on older macOS versions. Apple's page also lists the **IP address** line, which is your Mac's own address, not the router's. Don't mix the two up.

## How to find the address on Windows

Run `ipconfig`, the built-in command Microsoft documents:

1. Open **Command Prompt** (search for "cmd" in the Start menu).
2. Type `ipconfig` and press Enter.
3. Find the adapter you are using, usually named for Wi-Fi or Ethernet, and read **Default Gateway**.

If you see several adapters, use the one that has an IPv4 address and a Default Gateway value. Adapters that are disconnected or virtual may show nothing. Microsoft's separate page on finding your IP address points to Settings, Network & internet, then your Wi-Fi or Ethernet connection for the IPv4 address, but it does not describe where to find the gateway there, so we recommend `ipconfig`.

## What about phones?

We could not confirm exact iPhone or Android menu paths for the router address from Apple's or Google's own documentation, so we don't give steps for them. Use a Mac or Windows PC if you have one. Some routers, such as eero, are managed in a phone app instead, as covered below.

## How to log in, by brand

Apple's router-settings page says only that you should "use the configuration webpage or app provided by the router's manufacturer," so the right method depends on the brand.

| Brand | How to open the login page | Notes |
|---|---|---|
| Netgear | Go to routerlogin.net or routerlogin.com, or enter the router's IP address, commonly 192.168.1.1 or 192.168.0.1 | Orbi mesh systems use orbilogin.com. Netgear's page says the default username is usually admin and the default password usually password, and to check the label on the bottom of the unit |
| ASUS | Enter the router's LAN IP address, such as http://192.168.50.1, or go to http://www.asusrouter.com | On a first login, or after a factory reset, ASUS says you must first create a login username and password. If you don't know the IP address, ASUS points to its Device Discovery utility |
| eero | Managed in the eero app | We could not load eero's support site on the day of writing, so we make no claims about a web login. Our [bridge mode guide]({{< relref "/guides/bridge-mode-double-nat-own-router" >}}) cites eero's app menus |

Other brands: look for the address and credentials on the router's label or in its printed instructions, and use the address you found above.

## If you forgot the router password

Netgear's page says a factory reset may be needed if credentials are lost, and that a reset restores the default username and password printed on the router's label. A factory reset also erases your settings, such as your Wi-Fi name and password, so you will have to set the router up again. ASUS says that after a reset you must create a new username and password before you can use the web interface.

Because the Netgear default password is widely known, Netgear tells you to change it after logging in. Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) covers that and nine other settings.

## When the address opens the wrong device

The default gateway is whichever device your computer is connected through. If your internet provider gave you a combined modem and router, and you plugged your own router behind it, your computer may point at one or the other depending on how it is connected. Connect to the router you want to manage, then look up the gateway again. If you are unsure which device you are behind, see [bridge mode and double NAT]({{< relref "/guides/bridge-mode-double-nat-own-router" >}}).

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Mac: System Settings, Wi-Fi, Details shows IP address and Router ("The router address for the Wi-Fi connection") | [Apple Mac User Guide](https://support.apple.com/guide/mac-help/mh11935) | Verified as of October 17, 2026; menu names may differ on older macOS versions |
| `ipconfig` without parameters displays IPv4 and IPv6 addresses, subnet mask and default gateway | [Microsoft Learn: ipconfig](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig) | Verified as of October 17, 2026 |
| Windows Settings path lists the IPv4 address; the page does not describe the default gateway | [Microsoft Support: find your IP address](https://support.microsoft.com/en-us/windows/how-to-find-your-ip-address-in-windows-f21a9bbc-c582-55cd-35e0-73431160a1b9) | Verified; the page shows no publication date |
| Netgear: routerlogin.net or .com, or IP commonly 192.168.1.1 or 192.168.0.1; Orbi uses orbilogin.com; default admin / password; factory reset if credentials are lost; change the default password | [NETGEAR, updated September 3, 2026](https://www.netgear.com/hub/technology/router-login-page/) | Verified as of October 17, 2026; applies to Netgear routers, and some models may differ |
| ASUS: http://192.168.50.1 (example) or http://www.asusrouter.com; Device Discovery utility; create username and password on first login or after reset | [ASUS FAQ 1005263, updated February 23, 2026](https://www.asus.com/support/FAQ/1005263) | Verified as of October 17, 2026 |
| Apple tells users to use the router maker's web page or app to change settings | [Apple Support 102766, July 14, 2026](https://support.apple.com/en-us/102766) | Verified |
| Private ranges: 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 | [RFC 1918, February 1996](https://www.rfc-editor.org/rfc/rfc1918) | Verified |
| iPhone, Android and eero login steps | Not covered | Not published: we could not confirm them from official documentation |

## Bottom line

Read the address from your computer (Router on a Mac, Default Gateway in `ipconfig` on Windows), type it into a browser while connected to that router, or use the brand's own name such as routerlogin.net or asusrouter.com. If you can't log in, a factory reset is the last resort, and it erases your settings.
