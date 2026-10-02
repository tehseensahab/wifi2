---
title: "Router hardening checklist: 10 settings to change in 15 minutes"
date: 2026-09-25
description: "Ten changes that make your router harder to attack, in plain English and in order of importance."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "routers"]
tags: ["router-security", "wpa3", "firmware"]
summary: "Most router attacks succeed because of weak admin passwords, old firmware, or services you never use. Change the admin password, turn on automatic updates, use WPA3 or WPA2 with AES, and put smart-home gear on a guest network. A VPN protects traffic on your device but does not secure your router."
imageAlt: "Network router with blue Ethernet cables plugged in and status lights on"
imageCredit: "Photo: Albert Stoynov / [Unsplash](https://unsplash.com/photos/dyUp7WPu5q4)"
sample: true
faq:
  - q: "Does a VPN secure my home network?"
    a: "No. A VPN encrypts traffic between your device and the VPN provider. It does not fix an out-of-date router or a weak admin password."
  - q: "Should I hide my WiFi network name (SSID)?"
    a: "Hiding it adds little protection and can make devices harder to connect. A strong password and WPA3 or WPA2 with AES do much more."
  - q: "How often should I update router firmware?"
    a: "Turn on automatic updates if your router offers them. If not, check every few months. If the maker no longer publishes updates for your model, plan to replace it."
  - q: "What is the easiest win if I only have five minutes?"
    a: "Change the router's admin password and make sure firmware is current."
sources:
  - title: "Secure Our World"
    publisher: "Cybersecurity and Infrastructure Security Agency (CISA)"
    url: "https://www.cisa.gov/secure-our-world"
  - title: "Wi-Fi Security"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/security"
---

Your router is the front door to your home network. These ten changes take about 15 minutes, and they are in order of importance. Settings names vary by brand, so look for the closest match in your router's app or admin page.

## The checklist

1. **Change the router admin password.** This is separate from your WiFi password. Use a long, unique password and store it in a password manager.
2. **Install updates and turn on automatic updates.** Firmware updates fix security problems. If your router no longer receives updates, replace it.
3. **Use WPA3, or WPA2 with AES.** Avoid the older WEP and WPA settings, and avoid "TKIP." If a device can't connect on WPA3, a mixed WPA2/WPA3 mode is a reasonable compromise.
4. **Set a long WiFi password.** A passphrase of several random words is easy to type and hard to guess.
5. **Turn off WPS.** The push-button and PIN setup feature is convenient and a known weak spot.
6. **Turn off remote management.** Unless you deliberately use it, you don't need to reach your router's admin page from the internet.
7. **Use a guest network for visitors and smart-home gear.** This keeps cameras, plugs, and TVs away from the laptops and phones that hold your private data.
8. **Review connected devices.** Remove anything you don't recognize and change your WiFi password if something looks wrong.
9. **Check for risky services you don't use.** UPnP, port forwarding, and remote file sharing should be off unless you need them.
10. **Consider DNS filtering.** Many routers let you choose a DNS service that blocks known malicious sites.

## What does a VPN do?

A VPN encrypts your connection from your device to the VPN provider, which is useful on public WiFi. It doesn't secure your router, and it won't protect you from a weak admin password. Treat it as an extra, not a replacement for the checklist.

## What about smart-home devices?

Put them on a guest network and keep their apps updated. Our guide to [Matter and Thread]({{< relref "matter-thread-smart-home-explained" >}}) explains how smart-home devices connect to your network.

## When is it time to replace the router?

Replace your router when the maker stops releasing security updates, or if it can't use WPA3 and you have devices that do. If you're shopping, our [guide to picking a router for a large house]({{< relref "best-wifi-router-for-large-house" >}}) has current picks and notes on FCC rules.
