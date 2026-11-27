---
title: "Nintendo Switch NAT Type: What A, B, C, D and F Mean"
date: 2026-11-27T05:00:00Z
description: "Nintendo Switch NAT type runs from A (best) to F. A and B work with most players, C can struggle, D generally reaches only Type A and F can't do peer-to-peer."
authors: ["Tehseen Arbab"]
topics: ["gaming-streaming", "how-to-fixes"]
tags: ["nat-type", "nintendo-switch", "nintendo-switch-2", "nat-type-d", "nat-type-f", "port-forwarding", "dmz", "ipv6", "gaming"]
summary: "The NAT type in your Switch's connection test grades how well your network handles peer-to-peer play, from A (best) to F (unable to complete peer-to-peer communication). Nintendo says Type A is preferred, B is compatible with most other types, C may struggle with more restrictive types, and D can generally only connect to players on Type A. The same scale and test apply to Nintendo Switch 2."
imageAlt: "Close-up of a Nintendo Switch console with a blue Joy-Con controller attached, angled against a blurred background"
imageCredit: "Photo: Enrique Vidal Flores / [Unsplash](https://unsplash.com/photos/black-nintendo-switch-esNqFltvxGE)"
takeaways:
  - "Find your grade under System Settings > Internet > Test Connection. Nintendo's scale runs from A (best for peer-to-peer) to F (unable to complete peer-to-peer communication)."
  - "A or B: you're fine for most matches. C: you may have trouble with players on stricter types. D: Nintendo says you can generally connect only to players on Type A."
  - "The other player's NAT type matters too, so a failed match with one friend isn't always your network's fault."
  - "Nintendo's first step for every grade is turning off the console's IPv6 Connection setting; for A, B and C it also has you power cycle your modem and router."
  - "For a stubborn D or F, Nintendo's own options are port forwarding (UDP 1024 through 65535 to a static IP) or a DMZ, which bypasses your router's firewall for the console."
faq:
  - q: "What is the best NAT type on Nintendo Switch?"
    a: "Type A. Nintendo says NAT type A 'is preferred and generally indicates that your network environment works well for connecting with other players.' Type B is also fine for most players: Nintendo calls it 'compatible with most other NAT types as well.'"
  - q: "Why can't I join my friend with NAT Type D?"
    a: "Nintendo says players with NAT Type D can generally only connect to players with NAT Type A. If your friend is on B or C, a D on your side can block the match. Nintendo also notes that the other player's NAT type affects the connection, so ask your friend to run the connection test too."
  - q: "What does NAT Type F mean on Switch?"
    a: "It's the bottom of Nintendo's scale: 'unable to complete peer-to-peer communication.' Online features that rely on connecting directly to other players won't work until it improves. Nintendo's steps are to turn off IPv6 Connection on the console, then contact your ISP or network administrator and your router maker about a firmware update or factory reset."
  - q: "Do Switch and Switch 2 use the same NAT types?"
    a: "Yes. Nintendo's connection test and NAT troubleshooting pages cover both consoles, and both use the A to F scale. Nintendo publishes the same port forwarding range, UDP 1024 through 65535, for each (the original Switch figure is from Nintendo UK's page)."
  - q: "Is there a NAT Type E?"
    a: "Nintendo's support pages describe types A, B, C, D and F but don't describe a Type E, so there's no official explanation of one to give."
sources:
  - title: "How to Use the Internet Connection Test"
    publisher: "Nintendo Support (Americas)"
    url: "https://en-americas-support.nintendo.com/app/answers/detail/a_id/22462/~/how-to-use-the-internet-connection-test"
  - title: "Unable to Connect With Others Online (Errors During Match-Making Process)"
    publisher: "Nintendo Support (Americas)"
    url: "https://en-americas-support.nintendo.com/app/answers/detail/a_id/22541/"
  - title: "NAT Related Troubleshooting on Nintendo Switch 2 and Nintendo Switch"
    publisher: "Nintendo Support (Americas)"
    url: "https://en-americas-support.nintendo.com/app/answers/detail/a_id/22455/p/989/c/875"
  - title: "How to Set Up a Router's Port Forwarding for Nintendo Switch 2"
    publisher: "Nintendo Support (Americas)"
    url: "https://en-americas-support.nintendo.com/app/answers/detail/a_id/68445"
  - title: "How to Set Up a Router's Port Forwarding for a Nintendo Switch Console"
    publisher: "Nintendo UK"
    url: "https://www.nintendo.co.uk/Support/Nintendo-Switch/How-to-Set-Up-a-Router-s-Port-Forwarding-for-a-Nintendo-Switch-Console-1498000.html"
  - title: "How to Place a Nintendo Switch Console into a Router's DMZ"
    publisher: "Nintendo Australia"
    url: "https://nintendo.com/au/support/articles/how-to-place-a-nintendo-switch-console-into-a-routers-dmz"
  - title: "Troubleshooting Issues Related to NAT"
    publisher: "Nintendo Australia"
    url: "https://nintendo.com/au/support/articles/troubleshooting-issues-related-to-nat"
---

**Your Nintendo Switch NAT type is a letter grade for how well your home network handles direct, peer-to-peer connections with other players. Nintendo's scale runs from A, "best for peer-to-peer communication," to F, "unable to complete peer-to-peer communication."** Type A or B is fine for most online play. Type C may have trouble with players on stricter types. Type D, Nintendo says, can generally connect only to players on Type A. The same scale, test and fixes apply to Nintendo Switch 2.

Xbox and PlayStation use different labels (Xbox uses Open, Moderate and Strict; PlayStation uses Type 1 to 3); our [NAT Type Open vs. Moderate vs. Strict guide](/guides/nat-type-open-moderate-strict/) covers those. This page sticks to what Nintendo says about its own consoles.

## How to check your NAT type on Switch

On Switch or Switch 2, go to the **HOME Menu > System Settings > Internet > Test Connection**. Nintendo says the test begins as soon as you select it.

The results list Connection Name, SSID, Internet Connection, Global IP Address, NAT Type, Download Speed and Upload Speed. "Success" next to Internet Connection means the console reached Nintendo's services. The NAT Type line is the one this guide is about.

Run the test again after every change you make below, so you know which step helped.

## What each Switch NAT type means

| NAT type | What Nintendo says | What to expect |
|---|---|---|
| A | "Preferred"; works well for connecting with other players | Few NAT-related problems |
| B | "Compatible with most other NAT types" | Fine for most matches |
| C | May have difficulty with "some users with more restrictive NAT types" | Occasional failed joins |
| D | "Can only connect to players with NAT Type A" (generally) | Many matches with friends fail |
| F | "Unable to complete peer-to-peer communication" | Peer-to-peer play doesn't work |

Nintendo's support pages describe these five grades and don't describe a Type E.

Two points from Nintendo are easy to miss:

- **The other player counts too.** "Both your NAT type and the NAT type any player you are attempting to connect with can affect the connection process." If matches fail with one friend but not others, ask that friend to run the test.
- **A good grade doesn't rule out other problems.** For players on A, B or C who still get dropped or can't join, Nintendo's troubleshooting page points to latency and connection speed, and has players check that the test shows a download speed of at least 3 Mbps.

## How to fix NAT Type C, D or F on Switch

Nintendo's steps start the same way for every grade: turn off IPv6. Power cycling is part of its steps for A, B and C, and it's a harmless step to try for D or F too. Work down the list and re-test after each one.

### 1. Turn off IPv6 on the console

Nintendo lists this first for every NAT type. Go to **System Settings > Internet > Internet Settings**, select your network, choose **Change Settings** and switch **IPv6 Connection** off. This changes the console's setting only, not your router's. (For background on IPv6 at the router, see [Should you enable IPv6 on your router?](/guides/should-you-enable-ipv6/))

### 2. Power cycle the modem and router

Nintendo's method: unplug the modem and router (or your combined gateway), wait 30 seconds, plug the modem back in and wait for its lights to settle, then plug the router back in and wait again. Nintendo notes that a modem with a backup battery needs the battery removed before it will power cycle.

### 3. On Wi-Fi, get closer; on Ethernet, simplify

For Types A, B and C, Nintendo's next steps depend on the connection:

- **Wireless:** move the console within 10 to 15 feet of the router, and move metal objects and other electronics away from both.
- **Wired:** try connecting directly to the modem to bypass other devices, restart the modem and try a different Ethernet cable. A Switch dock without a LAN port needs a USB LAN adapter for this.

### 4. For Type D or F, check your router and ISP

For D and F, Nintendo skips the Wi-Fi tips and sends players to their ISP or network administrator, and to their router maker for a firmware update or factory reset. A D or F result usually reflects how your router or ISP handles traffic rather than Wi-Fi signal strength, which is likely why Nintendo doesn't suggest moving closer for these grades.

Two common causes to rule out, as general background:

- **Two routers in a row** (an ISP gateway plus your own router) means two layers of NAT. Nintendo Australia's NAT troubleshooting page notes that a router and a gateway "both handle NAT." Our guide to [bridge mode and double NAT](/guides/bridge-mode-double-nat-own-router/) explains how to remove one layer.
- **Carrier-grade NAT** at your ISP can't be fixed from your router. See [What is CGNAT?](/guides/what-is-cgnat/)

### 5. Port forwarding or DMZ (last resort)

Nintendo's support sites publish router instructions for both:

- **Port forwarding.** Nintendo's range for Nintendo Switch 2 is "port 1024 through 65535," with the protocol set to UDP. Nintendo UK's page for the original Switch gives the same range and protocol. Nintendo's Switch 2 page first has you give the console a fixed (static) IP address so the rule keeps pointing at it. Our [port forwarding guide](/guides/how-to-set-up-port-forwarding/) shows where the setting lives on common routers, and [DHCP reservation vs. static IP](/guides/dhcp-reservation-vs-static-ip/) explains the router-side alternative to typing an IP into the console.
- **DMZ.** Nintendo's Australian support page says a DMZ lets the console "communicate directly to the internet" and "bypass the network firewall features of your router." That is a bigger opening than a port rule.

Forwarding 1024 through 65535 also covers nearly every port number. Nintendo's own caveat is that "it is up to each consumer to determine what security needs they have for their own networks." If you use either option, point it only at the Switch's fixed IP address, and remove the rule if your grade doesn't improve.

Nintendo's NAT pages don't mention UPnP. Many routers use UPnP to open ports for games automatically; whether to leave it on is covered in [Should you disable WPS and UPnP?](/guides/should-you-disable-wps-and-upnp/)

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| Test path; result fields; NAT scale A (best) to F (unable to complete peer-to-peer) | [Nintendo: How to Use the Internet Connection Test](https://en-americas-support.nintendo.com/app/answers/detail/a_id/22462/~/how-to-use-the-internet-connection-test) | Verified |
| Type A preferred; B compatible with most; C may struggle; D generally connects only to A; 3 Mbps check; Wi-Fi and wired steps; D/F steps (ISP, router maker) | [Nintendo: Unable to Connect With Others Online](https://en-americas-support.nintendo.com/app/answers/detail/a_id/22541/) | Verified |
| Other player's NAT type matters; IPv6 Connection off path | [Nintendo: NAT Related Troubleshooting](https://en-americas-support.nintendo.com/app/answers/detail/a_id/22455/p/989/c/875) | Verified |
| Switch 2 port forwarding: UDP 1024 through 65535, static IP first, security caveat | [Nintendo: Port Forwarding for Nintendo Switch 2](https://en-americas-support.nintendo.com/app/answers/detail/a_id/68445) | Verified |
| Original Switch: same range and protocol | [Nintendo UK: Port Forwarding for Nintendo Switch](https://www.nintendo.co.uk/Support/Nintendo-Switch/How-to-Set-Up-a-Router-s-Port-Forwarding-for-a-Nintendo-Switch-Console-1498000.html) | Qualified (UK page; a US version didn't come up) |
| DMZ bypasses the router's firewall; static IP first; router and gateway "both handle NAT" | [Nintendo Australia: NAT troubleshooting](https://nintendo.com/au/support/articles/troubleshooting-issues-related-to-nat) and [DMZ setup](https://nintendo.com/au/support/articles/how-to-place-a-nintendo-switch-console-into-a-routers-dmz) | Qualified (Australian pages) |
