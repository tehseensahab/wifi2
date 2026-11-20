---
title: "Router Hardening Checklist: 10 Settings to Secure Your Router"
date: 2026-09-25
lastmod: 2026-11-20
description: "Ten router settings the NSA and FTC say to change: admin password, updates, WPA3, remote management, WPS and UPnP, guest network, firewall and reboots."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "routers"]
tags: ["router-security", "wpa3", "firmware", "upnp", "wps", "remote-management", "nsa", "ftc"]
summary: "Change the router's admin password, turn on automatic firmware updates, use WPA3 (or WPA2/WPA3) with a long passphrase, and turn off remote management, WPS and UPnP. Then put guests and smart devices on a separate network, confirm the firewall is on, and reboot the router weekly. Every item here comes from NSA or FTC home-network guidance, and a router that no longer gets updates should be replaced."
imageAlt: "Network router with blue Ethernet cables plugged in and status lights on"
imageCredit: "Photo: Albert Stoynov / [Unsplash](https://unsplash.com/photos/dyUp7WPu5q4). Generic hardware, not a specific model discussed here."
takeaways:
  - "Start with access: change the default admin username and password, and sign out of the admin page when you finish (FTC)."
  - "Keep firmware current, preferably with automatic updates, and replace the router when it reaches end of life for support (NSA)."
  - "Use WPA3 Personal, or a WPA2/WPA3 mode for older devices, with a passphrase of at least 20 characters (NSA); avoid WEP and old WPA (FTC)."
  - "Turn off remote management, WPS and UPnP, put guests and smart devices on their own network, keep the firewall on, and reboot weekly (NSA and FTC)."
faq:
  - q: "What is the most important router security setting?"
    a: "Start with the admin password and firmware updates. The FTC says to change the router's default admin username and password, and the NSA says to keep router firmware patched, preferably through automatic updates. A router that no longer gets updates should be replaced."
  - q: "Should I turn off UPnP and WPS?"
    a: "The FTC says to turn off both, because these convenience features can weaken security. The NSA also says to disable UPnP. Some game consoles use UPnP for an Open NAT type; our WPS and UPnP guide covers that trade-off."
  - q: "Why does the NSA say to reboot the router weekly?"
    a: "The NSA says malicious implants have been reported to infect home routers without persistence, so a regular reboot can remove them. It recommends scheduling weekly reboots of your router, phones and computers."
  - q: "Does a VPN secure my home network?"
    a: "No. A VPN encrypts traffic between your device and the VPN server. It does not change your router's settings, so an old firmware version or a weak admin password stays a problem."
  - q: "Should I buy my own router instead of using my provider's?"
    a: "The NSA suggests considering a router you own, connected to your provider's modem or gateway, for more control over security settings. Our guide to buying your own router covers the costs and compatibility checks."
sources:
  - title: "Best Practices for Securing Your Home Network"
    publisher: "National Security Agency (NSA), Cybersecurity Information Sheet PP-23-0270"
    url: "https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF"
    date: 2023-02-22
  - title: "How To Secure Your Home Wi-Fi Network"
    publisher: "Federal Trade Commission (FTC) Consumer Advice"
    url: "https://consumer.ftc.gov/articles/how-secure-your-home-wi-fi-network"
    date: 2022-12-01
---

To harden a home router, change its admin password, turn on automatic firmware updates, use WPA3 (or a WPA2/WPA3 mode) with a long passphrase, and turn off remote management, WPS and UPnP. Then separate guests and smart devices onto their own network, check the firewall is on, and reboot the router weekly. The checklist below is drawn from the NSA's home-network guidance and the FTC's Wi-Fi security advice, in the order we'd do it.

This is an explainer built from NSA and FTC guidance. Setting names vary by brand, so look for the closest match in your router's app or admin page.

## What should I change on my router first?

| # | Setting | What to do | Who recommends it |
|---|---|---|---|
| 1 | Admin password | Change the default admin username and password | FTC; NSA says enable strong authentication |
| 2 | Firmware updates | Install updates, turn on automatic updates | NSA, FTC |
| 3 | Wi-Fi security | WPA3 Personal, or WPA2/WPA3; not WEP or WPA | NSA, FTC |
| 4 | Wi-Fi passphrase | At least 20 characters | NSA |
| 5 | Remote management | Off | NSA, FTC |
| 6 | WPS | Off | FTC |
| 7 | UPnP | Off, unless something you rely on needs it | NSA, FTC |
| 8 | Guest and smart-device network | Separate network for visitors and IoT devices | NSA, FTC |
| 9 | Firewall | Confirm it is on | FTC; NSA says your router should support basic firewall features and NAT |
| 10 | Reboots | Schedule a weekly reboot | NSA |

## 1. How do I change my router's admin password?

Your router has two passwords: the Wi-Fi password your devices use, and the admin password that controls the router itself. The FTC says to change the default admin username and password to unique values, and to sign out of the administrator account once you finish making changes. The NSA's guidance says to enable strong authentication on your router. Store the new password in a password manager.

The NSA also suggests making configuration changes only from inside your home network, which pairs with turning off remote management (step 5).

## 2. Is my router's firmware up to date?

Firmware updates fix security flaws. The NSA says to keep the router patched, "preferably through automatic updates," and that routers should be replaced when they reach end of life for support. The FTC suggests checking for newer router software and registering the router so you get update notices.

Our guide to [whether your router still gets security updates](/guides/is-my-router-still-getting-security-updates/) shows how to check Netgear, ASUS, TP-Link and eero models. Google mesh owners can check our [Google Wifi and Nest Wifi support status](/guides/google-nest-wifi-support-status/) guide.

## 3 and 4. Which Wi-Fi security setting and password should I use?

Use WPA3 Personal if your router and devices support it, or a mixed WPA2/WPA3 mode if some older devices can't connect. The FTC lists WPA3 Personal or WPA2 Personal and says to avoid the older WPA and WEP options. The NSA says to use a passphrase of at least 20 characters. Several random words strung together reach that length and are easier to type than a jumble of symbols.

The NSA and FTC both also say to change the default network name (SSID) to something unique. Our [WPA2 vs. WPA3 guide](/guides/wpa2-vs-wpa3/) explains the modes and which devices struggle with WPA3.

## 5. Should I turn off remote management?

Yes, unless you deliberately use it. Remote management lets someone change router settings over the internet. The NSA says to disable remote administration on the router, and the FTC says to turn off the remote control feature so settings can't be changed from outside your home.

## 6 and 7. Should I turn off WPS and UPnP?

The FTC says to turn off both WPS and UPnP, which it describes as convenience features that can weaken security. The NSA says to disable UPnP. WPS is the push-button or PIN shortcut for joining Wi-Fi; UPnP lets devices on your network open ports in the router automatically.

Turning off UPnP can affect some game consoles' NAT type. Our guide to [whether to disable WPS and UPnP](/guides/should-you-disable-wps-and-upnp/) covers what breaks and how to open specific ports instead with [port forwarding](/guides/how-to-set-up-port-forwarding/).

## 8. Should smart devices be on a separate network?

The NSA says your wireless network should be segmented between your primary Wi-Fi, guest Wi-Fi and an IoT network, which keeps less secure devices from talking directly to your more secure ones. The FTC recommends a separate guest network with its own name and password for visitors. Our guide to [putting smart home devices on a guest network](/guides/guest-wifi-network-smart-home-devices/) covers what that can break and how to test it.

## 9. Is my router's firewall on?

The FTC says to confirm the router's built-in firewall is turned on. The NSA says the router you use should support basic firewall capabilities and network address translation (NAT), which helps keep devices inside your home from being scanned from the internet. Look for a Firewall or Security page in your router's settings to confirm.

## 10. Why reboot the router every week?

The NSA says "malicious implants have been reported to infect home routers without persistence," meaning a restart clears them. It recommends scheduling weekly reboots of your router, phones and computers. Check your router's app or admin page for a scheduled-reboot option, and pick an hour when nobody is online. Our [router reset guide](/guides/reset-router/) explains the difference between restarting and a factory reset.

## What else is worth doing?

- **Review connected devices.** Remove anything you don't recognize, and change the Wi-Fi password if something looks wrong. See [how to see who's connected to your Wi-Fi](/guides/see-who-is-connected-to-my-wifi/).
- **Consider a router you own.** The NSA suggests a personally owned router connected to your provider's modem or gateway gives you more control over security settings. Our guide to [buying your own router vs. using your provider's](/guides/buy-your-own-router-vs-isp-equipment/) covers the trade-offs.
- **Consider filtering DNS.** Some public DNS services block known malicious domains. Our guide to [changing your router's DNS](/guides/change-router-dns-settings/) compares them. This isn't in the NSA or FTC lists; treat it as an extra.

## When should I replace my router?

Replace it when the maker stops releasing security updates. The NSA says routers should be replaced when they reach end of life for support, and recommends a router capable of WPA3. If you're shopping for a bigger home, see our [best Wi-Fi router for a large house](/guides/best-wifi-router-for-large-house/) guide.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| Change default admin username and password; sign out of the admin account; change default network name | [FTC](https://consumer.ftc.gov/articles/how-secure-your-home-wi-fi-network) | Verified |
| Use WPA3 Personal or WPA2 Personal; avoid WPA and WEP | [FTC](https://consumer.ftc.gov/articles/how-secure-your-home-wi-fi-network) | Verified |
| Check for router software updates and register the router | [FTC](https://consumer.ftc.gov/articles/how-secure-your-home-wi-fi-network) | Verified |
| Turn off remote management, WPS and UPnP; set up a guest network; confirm the firewall is on | [FTC](https://consumer.ftc.gov/articles/how-secure-your-home-wi-fi-network) | Verified |
| Enable strong authentication; patch firmware, preferably automatically; replace at end of life | [NSA](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| WPA3 or WPA2/3 with a passphrase of at least 20 characters; change the default SSID | [NSA](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| Disable remote administration and UPnP; make configuration changes from inside the network | [NSA](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| Segment primary, guest and IoT networks; router should support basic firewall and NAT | [NSA](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| Weekly reboots because implants have infected routers without persistence | [NSA](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| Consider a personally owned router connected to the provider's equipment | [NSA](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| NSA does not mention WPS; FTC does | Both documents | Verified |

## Bottom line

One session in your router's settings covers most of this list: new admin password, automatic updates, WPA3 with a long passphrase, and remote management, WPS and UPnP turned off. Add a guest network for smart devices and a weekly reboot, and replace the router once its maker stops sending updates.
