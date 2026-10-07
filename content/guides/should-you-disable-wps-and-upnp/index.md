---
title: "Should You Turn Off WPS and UPnP on Your Router?"
date: 2026-10-07
description: "WPS and UPnP make setup easier, and both have known security weaknesses. Here is what each does, the official advice, and what breaks without them."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "gaming-streaming"]
tags: ["wps", "upnp", "router-security", "nat-type", "port-forwarding", "gaming"]
summary: "Turn off WPS: its PIN method has a design flaw that lets someone in Wi-Fi range recover your password, and you can join devices by typing the password instead. Turn off UPnP unless something you use needs it, which the NSA recommends. Game consoles are the common exception, and port forwarding is the narrower alternative."
imageAlt: "Hands holding a game controller in front of a monitor showing a game"
imageCredit: "Photo: Sam Pak / [Unsplash](https://unsplash.com/photos/X6QffKLwyoQ)"
takeaways:
  - "WPS (Wi-Fi Protected Setup) lets devices join Wi-Fi without typing the password. A flaw published on December 27, 2011 cuts the guesses needed to crack its 8-digit PIN from 100 million to 11,000."
  - "UPnP (Universal Plug and Play) lets devices on your network open ports on the router by themselves. The NSA's home network guidance says to disable it."
  - "CISA says WPS increases the likelihood of unauthorized access, and that threat actors can use UPnP to spread malware and control devices remotely."
  - "Turning off UPnP can leave a game console with a restricted NAT type. Microsoft's Xbox support lists turning UPnP on as its first fix, with port forwarding as an alternative."
faq:
  - q: "Is WPS safe to leave on?"
    a: "No, not the PIN method. CERT's vulnerability note on WPS says an attacker within wireless range can brute force the PIN and retrieve the Wi-Fi password, and its recommended solution is to disable the feature. CISA also advises turning WPS off."
  - q: "Is the WPS button safer than the WPS PIN?"
    a: "The published flaw is in the PIN method. The button method only accepts a new device for a short time after someone presses it. Some routers let you turn off the PIN and keep the button, but many tie both to one setting. If you can't confirm the PIN is off, turn WPS off entirely."
  - q: "What happens if I turn off UPnP?"
    a: "Most browsing, streaming and video calls carry on as before. Things that need other devices on the internet to connect in to yours can be affected, mainly multiplayer games and voice chat on consoles, and some remote-access features. You can fix those with port forwarding."
  - q: "Do I need UPnP for gaming?"
    a: "Not strictly. Xbox support says you need an Open NAT type for multiplayer and party chat to work properly, and lists turning on UPnP as the first step. Opening the specific ports by port forwarding is the alternative it lists next."
  - q: "How do I connect a printer or smart device without WPS?"
    a: "Use the device's own app or control panel to choose your network and enter the Wi-Fi password. Newer devices may support Wi-Fi Easy Connect, which the Wi-Fi Alliance describes as setup by scanning a QR code."
sources:
  - title: "VU#723755: WiFi Protected Setup (WPS) PIN brute force vulnerability"
    publisher: "CERT Coordination Center, Carnegie Mellon University"
    url: "https://www.kb.cert.org/vuls/id/723755"
    date: 2011-12-27
  - title: "VU#922681: Portable SDK for UPnP Devices (libupnp) contains multiple buffer overflows in SSDP"
    publisher: "CERT Coordination Center, Carnegie Mellon University"
    url: "https://www.kb.cert.org/vuls/id/922681"
    date: 2013-01-29
  - title: "Best Practices for Securing Your Home Network"
    publisher: "National Security Agency"
    url: "https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF"
    date: 2023-02-22
  - title: "Module 5: Securing Your Home Wi-Fi"
    publisher: "Cybersecurity and Infrastructure Security Agency (CISA)"
    url: "https://www.cisa.gov/audiences/high-risk-communities/projectupskill/module5"
  - title: "Wi-Fi Protected Setup"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/discover-wi-fi/wi-fi-protected-setup"
  - title: "Wi-Fi Easy Connect"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/discover-wi-fi/wi-fi-easy-connect"
  - title: "Troubleshoot NAT errors and multiplayer game issues"
    publisher: "Xbox Support"
    url: "https://support.xbox.com/en-US/help/hardware-network/connect-network/xbox-one-nat-error"
---

Turn off WPS. Turn off UPnP too, unless something you use stops working without it. Both features exist to save you a setup step, and both have documented security weaknesses. For most homes the only real cost of switching them off is a few minutes of extra setup, and for game consoles, a port-forwarding rule.

This is an explainer based on US government security guidance and published vulnerability notes. We have not tested routers for it.

## What is WPS, and what is wrong with it?

WPS stands for Wi-Fi Protected Setup. The Wi-Fi Alliance, the industry group that certifies Wi-Fi products, says it was "designed to ease the setup of security-protected Wi-Fi networks in home and small office environments." In practice it lets a device join your Wi-Fi without anyone typing the password, usually by pressing a button on the router or entering an 8-digit PIN.

The PIN is the problem. On December 27, 2011, the CERT Coordination Center at Carnegie Mellon University published a vulnerability note on a flaw reported by researcher Stefan Viehböck. The router checks the 8-digit PIN in two halves and tells the other side when the first half is right. The last digit is a checksum, a digit calculated from the others. Together those reduce the number of guesses needed from 100 million to 11,000.

CERT's note says an attacker within wireless range can "brute force the WPS PIN and retrieve the password for the wireless network, change the configuration of the access point, or cause a denial of service." A long Wi-Fi password does not help, because the attack goes around it.

CERT's recommended solution was to disable the feature. The Cybersecurity and Infrastructure Security Agency (CISA) says the same in its home Wi-Fi guidance: WPS "increases the likelihood that a threat actor could gain unauthorized access to your Wi-Fi network."

### Is the button safer than the PIN?

The published flaw concerns the PIN. The button method opens a short window after someone physically presses it, so an attacker would need to be in range at that moment.

Whether you can keep the button and lose the PIN depends on your router. Some have separate settings, and many have a single WPS switch that controls both. The CERT note is from 2011 and router firmware has changed since, but you can't easily verify how your own router handles repeated PIN attempts. If you can't confirm the PIN method is off, turn WPS off altogether.

### What do I use instead?

Type the password, or scan it. Many phones can share a Wi-Fi password by QR code, and printers and smart devices can be joined through their own apps or control panels. The Wi-Fi Alliance also has a newer setup method, Wi-Fi Easy Connect, which works by "scanning a product quick response (QR) code." Whether you can use it depends on both the router and the device supporting it.

## What is UPnP, and what is wrong with it?

UPnP stands for Universal Plug and Play. On a home router, it lets a device on your network ask the router to open a port, which is a numbered doorway for incoming connections from the internet. A game console might open ports so other players can connect to it. The device asks, the router agrees, and you never see a prompt.

That convenience is also the weakness. The router does not check whether the request is a good idea. Any device or program on your network can ask, including one that is infected or badly made.

Three official sources address it:

- The National Security Agency (NSA), in home network guidance published in February 2023: "Disable Universal Plug-n-Play (UPnP). These measures help close holes that may enable an attacker to compromise your network."
- CISA: "Threat actors can use UPnP to spread malware to devices in your network and control them remotely."
- CERT, in a note published January 29, 2013, on flaws found by security firm Rapid7 in a widely used UPnP software library: "A remote, unauthenticated attacker may be able to execute arbitrary code on the device or cause a denial of service." One of its suggested workarounds was to disable UPnP.

That 2013 flaw was in one software library, and CERT's note lists a fixed version of it. It is here as an example of the kind of problem UPnP has had, not as a current threat to your specific router. The NSA and CISA advice is the reason to act.

## What breaks if I turn them off?

| Feature | If you turn it off | How to work around it |
|---|---|---|
| WPS | Devices can't join by button or PIN | Enter the Wi-Fi password, share it by QR code, or use the device's app |
| UPnP | Devices can't open router ports by themselves | Add a port-forwarding rule for the device that needs one |

Turning off WPS breaks nothing that is already connected. Devices that joined by WPS should stay joined, because they store the password once connected.

Turning off UPnP is the one that can bite. Web browsing, streaming and video calls generally start from your device and reach outward, so they don't need incoming ports. Multiplayer gaming and voice chat on consoles are different, because other players' consoles need to connect in.

Xbox support explains the symptom: you can sign in, but "can't hear your friends online within a game or a party" or can't host or join a multiplayer game. It says "You need your NAT type to be Open to resolve this issue." NAT (Network Address Translation) is how your router shares one internet address among all your devices, and the NAT type is the console's measure of how easily others can reach it. The first fix Xbox lists is "Turn on UPnP." The next ones it lists are opening ports with port forwarding, then a "perimeter network (also known as DMZ)."

## Which should I choose for gaming: UPnP or port forwarding?

| Option | What it opens | Trade-off |
|---|---|---|
| UPnP on | Whatever any device on your network asks for | Easiest; against NSA advice |
| Port forwarding | Only the ports you list, to the one device you name | A few minutes of setup; much narrower |
| DMZ for the console | Everything, to one device | Avoid unless nothing else works; it exposes that device fully |

Port forwarding is the better fit for a household that wants UPnP off. You give the console a fixed address on your network, then forward the ports the console maker lists to that address. The exact ports are on each console maker's support site.

If you decide to keep UPnP on for a console, reduce the exposure in other ways. Keep the router's firmware current, and put smart home devices on a separate network so they can't use UPnP on your main one. Our guide to [guest networks for smart home devices]({{< relref "/guides/guest-wifi-network-smart-home-devices" >}}) covers how.

One note for gamers: an Open NAT type helps you connect to other players. It does not reduce lag. For that, see [our bufferbloat guide]({{< relref "/guides/fix-bufferbloat-gaming-lag" >}}).

## How do I turn them off?

Menu names vary by brand, so look for the closest match in your router's app or admin page.

1. **Open the router's settings** in its app or by browsing to its admin address.
2. **Find WPS.** It is usually under wireless or Wi-Fi settings, sometimes under advanced settings. Turn it off, and if there is a separate PIN option, turn that off too.
3. **Find UPnP.** It is usually under advanced, network or NAT settings. Turn it off.
4. **Save, then test.** Check that devices still connect, and run the network test on any game console. On Xbox this is under Settings, General, Network settings.
5. **Add port forwarding** only for a device that now has a problem.
6. **While you are there, turn off remote management.** The NSA guidance says to "disable the ability to perform remote administration on the routing device."

Your router or mesh system may not have a WPS setting at all. If you can't find one, check the maker's support pages before assuming WPS is on.

For the rest of the settings worth changing, see our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}). For the security mode itself, see [WPA2 vs. WPA3]({{< relref "/guides/wpa2-vs-wpa3" >}}).

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| A WPS PIN design flaw, published December 27, 2011 and reported by Stefan Viehböck, reduces brute-force attempts from 100 million to 11,000 and lets an attacker in range retrieve the Wi-Fi password; the recommended solution was to disable WPS | [CERT/CC VU#723755](https://www.kb.cert.org/vuls/id/723755) | Verified; the note dates from 2011 to 2012, and we can't confirm how any current router model behaves |
| CISA says WPS increases the likelihood of unauthorized access and that threat actors can use UPnP to spread malware and control devices remotely | [CISA, Securing Your Home Wi-Fi](https://www.cisa.gov/audiences/high-risk-communities/projectupskill/module5) | Verified |
| The NSA advises disabling UPnP and remote administration on home routers | [NSA, Best Practices for Securing Your Home Network, February 2023](https://media.defense.gov/2023/Feb/22/2003165170/-1/-1/0/CSI_BEST_PRACTICS_FOR_SECURING_YOUR_HOME_NETWORK.PDF) | Verified |
| A UPnP library flaw published January 29, 2013 allowed remote, unauthenticated code execution; Rapid7 reported it | [CERT/CC VU#922681](https://www.kb.cert.org/vuls/id/922681) | Qualified: a historical example in one library, with a fixed version listed; not a statement about current routers |
| Wi-Fi Protected Setup was designed to ease setup of secured Wi-Fi networks in homes and small offices | [Wi-Fi Alliance](https://www.wi-fi.org/discover-wi-fi/wi-fi-protected-setup) | Verified |
| Wi-Fi Easy Connect sets devices up by scanning a QR code | [Wi-Fi Alliance](https://www.wi-fi.org/discover-wi-fi/wi-fi-easy-connect) | Verified; availability depends on router and device support |
| Xbox needs an Open NAT type for multiplayer and party chat; its listed fixes are turning on UPnP, then port forwarding, then a DMZ | [Xbox Support, checked October 7, 2026](https://support.xbox.com/en-US/help/hardware-network/connect-network/xbox-one-nat-error) | Verified |
| The button method is less exposed than the PIN, and port forwarding is narrower than UPnP | Our reasoning from how each feature works | Qualified: an assessment, not a tested result |

## Bottom line

WPS saves you typing a password once and leaves a known weakness in place, so turn it off. UPnP is off in the NSA's recommended setup, so turn that off too and see whether anything complains. If a game console does, forward its ports instead of switching UPnP back on. Neither change takes more than a few minutes, and both are easy to reverse.
