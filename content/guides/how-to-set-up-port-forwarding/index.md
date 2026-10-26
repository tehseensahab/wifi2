---
title: "How to Set Up Port Forwarding on Your Router"
date: 2026-10-26T05:00:00Z
description: "How to set up port forwarding: reserve the device's IP, add the rule in your router's settings, test from outside. Steps for eero, Nest, Deco, Netgear, ASUS."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "routers"]
tags: ["port-forwarding", "ip-reservation", "dhcp", "nat", "cgnat", "eero", "google-nest-wifi", "tp-link-deco", "netgear", "asus"]
summary: "To set up port forwarding, give the device a fixed address with a DHCP reservation, then add a rule in your router's app or web page that sends an external port to that device's internal port, and test it from a network outside your home. It only works if your main router has a public internet (WAN) address; behind CGNAT, a T-Mobile 5G gateway or a second router you don't control, the rule has nothing to open."
imageAlt: "Rows of blue Ethernet cables with white labels plugged into network switches with small yellow status lights"
imageCredit: "Photo: Scott Rodgerson / [Unsplash](https://unsplash.com/photos/PSpf_XgOM5w)"
takeaways:
  - "Every rule points at a device's local IP address, so reserve that address first. Netgear's support article says the server device \"must always have the same IP address.\""
  - "Each brand puts the setting in a different place: eero and Deco in their apps, Google Nest Wifi in the Google Home app, Netgear and ASUS in the web interface."
  - "Routers list ports for some common services; for anything else, get the port numbers and protocol (TCP, UDP or both) from the device or game's maker."
  - "Port forwarding needs a public WAN address on your router. ASUS says it \"will not function properly\" behind multi-layer NAT, and T-Mobile says its gateways can't enable port forwarding."
  - "Test from outside your network, such as a phone on cellular data, not from a device on your own Wi-Fi."
faq:
  - q: "Do I need a static IP address for port forwarding?"
    a: "You need a fixed local address for the device, not a static public address from your provider. A DHCP reservation in your router does that: Google describes it as your network assigning \"the same IP address to a specific device.\" A changing public address is a separate issue; Dynamic DNS handles that."
  - q: "What's the difference between the external and internal port?"
    a: "The external port is the one people connect to on your public address; the internal port is the one the device listens on at home. They can be the same. On a Deco, TP-Link says a blank Internal Port automatically matches the External Port. Google says that for a port range in its app, the internal and external ranges must be the same."
  - q: "Why doesn't my port forward work?"
    a: "Common causes include a WAN address that isn't public (CGNAT or a second router in front), a device whose local IP changed, the wrong protocol, or testing from inside your own network. Check the router's WAN address first; if it's private or in the 100.64 to 100.127 range, the rule can't help on its own."
  - q: "Is port forwarding safe?"
    a: "It exposes one service on one device to the whole internet, so treat it as a door you've chosen to open. Forward only the ports a device's maker lists, keep that device's software updated, and delete rules you no longer use."
  - q: "Can I port forward on a mesh system in access point mode?"
    a: "No, the forwarding has to happen on whatever device is doing the routing. TP-Link lists Port Forwarding and Address Reservation among the features unavailable when a Deco is in Access Point mode, so set the rule on the upstream router instead."
sources:
  - title: "How do I set up port forwarding?"
    publisher: "eero"
    url: "https://eero.com/support/articles/how-do-i-set-up-port-forwarding"
  - title: "Port forwarding or port opening"
    publisher: "Google Home and Nest Help"
    url: "https://support.google.com/googlehome/answer/6274503?hl=en"
  - title: "Set DHCP IP reservation or a Static IP address for a device"
    publisher: "Google Home and Nest Help"
    url: "https://support.google.com/googlehome/answer/6274660?hl=en-CA"
  - title: "How to Set Up Port Forwarding on Your Deco"
    publisher: "TP-Link (support FAQ 1797)"
    url: "https://www.vigi.com/lk/support/faq/1797/"
    date: 2026-04-17
  - title: "How to configure Address Reservation on a Deco"
    publisher: "TP-Link (support FAQ 1795)"
    url: "https://vigi.com/cl/support/faq/1795"
    date: 2026-04-20
  - title: "How to Set Up Deco in Access Point Mode"
    publisher: "TP-Link (support FAQ 1842)"
    url: "https://www.omadanetworks.com/us/support/faq/1842/"
    date: 2026-04-17
  - title: "How do I set up port forwarding to a local server on my NETGEAR router?"
    publisher: "NETGEAR Support"
    url: "https://kb.netgear.com/24289/How-do-I-set-up-port-forwarding-to-a-local-server-on-my-NETGEAR-router"
    date: 2025-07-07
  - title: "How do I reserve an IP address on my NETGEAR router?"
    publisher: "NETGEAR Support"
    url: "https://kb.netgear.com/25722/How-do-I-reserve-an-IP-address-on-my-NETGEAR-router"
    date: 2025-07-07
  - title: "How do I configure port forwarding on my Orbi WiFi System?"
    publisher: "NETGEAR Support"
    url: "https://kb.netgear.com/31069/How-do-I-configure-port-forwarding-on-my-Orbi-system"
    date: 2025-07-07
  - title: "How to set up Virtual Server/Port Forwarding Rules on ASUS Router?"
    publisher: "ASUS Support (FAQ 1037906)"
    url: "https://www.asus.com/support/FAQ/1037906"
    date: 2025-09-26
  - title: "How to set up Virtual Server/ Port Forwarding on ASUS Router? (older firmware)"
    publisher: "ASUS Support (FAQ 114093)"
    url: "https://www.asus.com/us/support/FAQ/114093/"
    date: 2025-09-18
  - title: "Connect your Devices to T-Mobile Internet"
    publisher: "T-Mobile Support"
    url: "https://www.t-mobile.com/support/home-internet/connect"
---

To set up port forwarding, first give the device a fixed local address with a DHCP reservation, then add a rule in your router's app or web page that sends an external port to that device's internal port and protocol, and finally test it from a network outside your home. It only works if your main router has a public internet (WAN) address, though. If your provider uses carrier-grade NAT, or there's another router in front of yours, the rule has nothing to open, so check that first.

## Before you start: check that port forwarding can work

Port forwarding opens a path from the internet to your router. If something upstream is also doing NAT, traffic never reaches your router to be forwarded.

1. **Find your router's WAN address** in its app or web page (internet, WAN or status screen).
2. **If it starts with 100.64 through 100.127**, you're almost certainly behind CGNAT. Our [CGNAT explainer](/guides/what-is-cgnat/) covers the workarounds; a router rule won't fix it.
3. **If it's 192.168.x.x, 10.x.x.x or 172.16.x.x to 172.31.x.x**, another device in front of your router is doing NAT, often your provider's gateway. TP-Link's Deco instructions say that in this case "there is another NAT device connected to the WAN port of your main Deco," and you have to open the ports on that device too. The cleaner fix is bridge mode; see our [bridge mode and double NAT guide](/guides/bridge-mode-double-nat-own-router/).

ASUS states the requirement plainly: the router needs a public WAN IP, and behind multi-layer NAT, "Port Forwarding will not function properly under such environment."

On **T-Mobile 5G Home Internet**, T-Mobile's support page says its "gateways do not have the ability to enable and disable NAT/port forwarding," and tells customers to "refer to the manufacturer or developer if NAT or port forwarding is needed." As we read it, adding your own router behind the gateway doesn't change that, because the gateway still sits in front.

### Get the port numbers and protocol

Routers offer presets for some common services, but for a game console, camera or server, the device's maker is the place to get the ports. Google's help page says some devices suggest ports and others let you choose, and to check the device's manual or contact its maker if you don't know. Note whether the service uses **TCP, UDP or both**. eero and Google ask you to pick; on other routers it can be part of the service you choose.

## Step 1: Reserve the device's IP address

A forwarding rule points at a local address such as 192.168.1.50. If the device gets a different address next week, the rule points at nothing. Netgear's instructions say "the server device must always have the same IP address," and make reserving one a step before creating the rule.

A DHCP reservation does this without changing anything on the device. Google describes it as your network assigning "the same IP address to a specific device." Where to find it:

| Router | Where the reservation lives |
|---|---|
| eero | eero app: Settings > Advanced networking > Reservations & port forwarding (the port rule is added to the reservation) |
| Google Nest Wifi / Google Wifi | Google Home app: Wifi > Network settings > Advanced Networking > DHCP IP reservations |
| TP-Link Deco | Deco app: More > Advanced > Address Reservation |
| Netgear (Nighthawk and similar) | routerlogin.net: ADVANCED > Setup > LAN Setup > Address Reservation (some models: Settings > Setup > LAN Setup) |

On eero the reservation and the port rule are one step, as shown below.

## Step 2: Add the forwarding rule

### eero

In the eero app, go to **Settings > Advanced networking > Reservations & port forwarding**. Under IPv4 Reservations & Port Forwards, add an IP reservation for the device, choose **Open a port**, then enter the port or range and the protocol. eero's article says you can "open a specific port or a range of ports (enter the starting port, a dash, then the ending port)" and "select a protocol: TCP, UDP, or both." IPv6 rules go under IPv6 Firewall Rules on the same screen.

### Google Nest Wifi and Google Wifi

In the Google Home app, open Wifi settings, then **Advanced Networking > Port management > Add**. Pick the IPv4 tab (port forwarding) or IPv6 tab (port opening), select the device, and enter the ports. For IPv4 you set an internal and an external port; Google notes that for a range, "internal and external ranges need to be the same," which isn't required for a single port. Choose TCP, UDP or TCP/UDP and save. Google adds that in most cases UPnP sets these up automatically, so a manual rule is for devices that need one.

### TP-Link Deco

In the Deco app, go to **More > Advanced > NAT Forwarding > Port Forwarding** and tap the + icon. Choose a service type, tap **Internal IP** to pick the device, then enter the External Port and Internal Port and save. TP-Link says a blank Internal Port automatically uses the External Port number.

### Netgear routers and Orbi

Sign in at routerlogin.net (Orbi: orbilogin.com) and go to **ADVANCED > Advanced Setup > Port Forwarding/Port Triggering**. Leave **Port Forwarding** selected, pick a service from the Service Name list, enter the device's address in Server IP Address and click **Add**. If your service isn't listed, Netgear's article says to create a custom service first.

### ASUS

On ASUS firmware 3.0.0.4.384.40000 or later, open the web interface and go to **WAN > Virtual Server/Port Forwarding**. Turn on **Enable Port Forwarding**, click **Add profile**, and fill in External Port, Internal Port and Internal IP Address (plus an optional Source IP field). A quick-select list fills in ports for common services. ASUS warns: "Please avoid port conflicts as they will lead to rule failures." Older firmware uses a different screen, covered in ASUS FAQ 114093.

## Step 3: Test from outside your network

Testing from a laptop on your own Wi-Fi tells you little. ASUS and TP-Link both describe the same test: from a device on a different network, connect to your router's WAN address and the external port. A phone with Wi-Fi turned off, on cellular data, works for this. If the service answers (a web page loads, a camera app connects, a game reports an open NAT type), the rule works.

If it fails, check in this order:

1. **Is the device's service running and listening?** ASUS's test starts by confirming the device on your network has the port open.
2. **Did its local IP change?** Compare it with the reservation.
3. **Is the protocol right?** A UDP-only game won't work with a TCP rule.
4. **Is the WAN address public?** Go back to the first section.

## When to use something other than port forwarding

- **Mesh in access point or bridge mode:** the rule belongs on whatever is routing. TP-Link lists Port Forwarding and Address Reservation among the features unavailable in Deco Access Point mode, so add them on the main router.
- **Games and consoles:** many set up their own forwards through UPnP. Our [WPS and UPnP guide](/guides/should-you-disable-wps-and-upnp/) covers the trade-off of leaving it on.
- **IPv6:** if your provider supports it, you open a port in the router's IPv6 firewall instead of forwarding one; eero and Google both have a separate IPv6 section for this. See [should you enable IPv6](/guides/should-you-enable-ipv6/).
- **Remote access to your own devices:** if you're behind CGNAT, a relay-based remote-access tool is often easier than asking for a public IP.

Each forward exposes one service on one device to the internet. Open only the ports a device's maker lists, keep that device updated, and delete rules you no longer use.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| eero menu path; port ranges with a dash; TCP, UDP or both; IPv6 Firewall Rules | [eero Support](https://eero.com/support/articles/how-do-i-set-up-port-forwarding) | Verified |
| Google Home app path; IPv4 forwarding vs IPv6 opening; range rule; UPnP sets most up automatically | [Google Help](https://support.google.com/googlehome/answer/6274503?hl=en) | Verified |
| DHCP reservation assigns the same IP to a device; Google Home path | [Google Help](https://support.google.com/googlehome/answer/6274660?hl=en-CA) | Verified |
| Deco port forwarding path; blank Internal Port matches External; private WAN means another NAT device | [TP-Link FAQ 1797](https://www.vigi.com/lk/support/faq/1797/) | Verified |
| Deco Address Reservation path | [TP-Link FAQ 1795](https://vigi.com/cl/support/faq/1795) | Verified |
| Port Forwarding and Address Reservation unavailable in Deco Access Point mode | [TP-Link FAQ 1842](https://www.omadanetworks.com/us/support/faq/1842/) | Verified |
| Netgear path; server must always have the same IP | [NETGEAR KB 24289](https://kb.netgear.com/24289/How-do-I-set-up-port-forwarding-to-a-local-server-on-my-NETGEAR-router), [KB 31069](https://kb.netgear.com/31069/How-do-I-configure-port-forwarding-on-my-Orbi-system) | Verified |
| Netgear Address Reservation path | [NETGEAR KB 25722](https://kb.netgear.com/25722/How-do-I-reserve-an-IP-address-on-my-NETGEAR-router) | Verified |
| ASUS path and fields (firmware 3.0.0.4.384.40000+); public WAN IP needed; port conflicts; outside test | [ASUS FAQ 1037906](https://www.asus.com/support/FAQ/1037906), [ASUS FAQ 114093](https://www.asus.com/us/support/FAQ/114093/) | Verified |
| T-Mobile gateways can't enable port forwarding | [T-Mobile Support](https://www.t-mobile.com/support/home-internet/connect) | Verified |
