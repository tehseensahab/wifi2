---
title: "WiFi glossary"
description: "Plain-English definitions of the WiFi, router, and home internet terms you'll see on boxes, in apps, and in our reviews."
layout: static
updated: 2026-10-02
---
Jump to: [Basics](#basics) · [WiFi standards and bands](#wifi-standards-and-bands) · [Speed and performance](#speed-and-performance) · [Internet service](#internet-service) · [Mesh and wiring](#mesh-and-wiring) · [Security](#security) · [Smart home](#smart-home)

## Basics

**Router.** The box that creates your home network and shares one internet connection with all your devices. Most also broadcast WiFi.

**Modem.** The box that connects your home to your internet provider's line (cable, DSL, or fiber). A router plugs into it.

**Gateway.** A modem and router in one box, often rented from your internet provider.

**Access point.** A device that adds WiFi coverage to a wired network. Mesh nodes are a type of access point.

**SSID.** Your WiFi network's name.

**Ethernet.** A wired network connection. It is faster and more stable than WiFi for devices that stay put, like TVs, consoles, and desktops.

## WiFi standards and bands

**WiFi 6 (802.11ax).** The WiFi standard that improved performance on busy networks with many devices. Works on 2.4 GHz and 5 GHz.

**WiFi 6E.** WiFi 6 extended to the 6 GHz band, which has more room and less interference.

**WiFi 7 (802.11be).** The newest standard. It adds wider 320 MHz channels on 6 GHz and Multi-Link Operation (MLO), which lets a device use more than one band at once. You need WiFi 7 devices to get the full benefit.

**2.4 GHz.** The band with the longest range but the lowest speeds and the most interference. Many smart-home devices only use 2.4 GHz.

**5 GHz.** Faster than 2.4 GHz with shorter range. The workhorse band for most phones and laptops.

**6 GHz.** The newest band, used by WiFi 6E and WiFi 7. It's fast and uncrowded, but it has the shortest range and struggles with walls.

**Channel width.** How much of a band a connection uses, measured in MHz. Wider channels are faster but more prone to interference.

**DFS channels.** Some 5 GHz channels are shared with weather and aircraft radar. Routers must move off them if radar is detected, which can cause brief drops.

**Band steering.** A router feature that moves devices to the best band automatically.

**MU-MIMO and OFDMA.** Features that let a router talk to several devices at the same time instead of taking turns. They help most in busy homes.

**Beamforming.** A technique that focuses the WiFi signal toward a device instead of spreading it evenly.

## Speed and performance

**Mbps and Gbps.** Megabits and gigabits per second, the unit for internet and WiFi speed. 1 Gbps is 1,000 Mbps. Downloads in your browser often show MB/s (megabytes); divide Mbps by 8 to compare.

**Download and upload.** Download is data coming to you (streaming, browsing). Upload is data you send (video calls, cloud backups, posting videos).

**Latency (ping).** How long data takes to make a round trip, in milliseconds (ms). Lower is better, especially for gaming and calls.

**Jitter.** How much latency varies from moment to moment. High jitter makes calls choppy.

**Bufferbloat.** Lag caused when a busy connection makes data wait in a long queue. See our [bufferbloat guide](/guides/fix-bufferbloat-gaming-lag/).

**QoS and SQM.** Quality of Service settings prioritize some traffic. Smart queue management (SQM) keeps latency low for everything when the connection is busy.

**Signal strength (dBm, RSSI).** How strong the WiFi signal is at a device. Numbers closer to zero are stronger: -50 dBm is excellent, -80 dBm is weak.

**Dead zone.** A spot in your home where WiFi is too weak to use.

**Speed test.** A tool that measures your download, upload, and latency. Test with a wired laptop first to separate internet problems from WiFi problems.

## Internet service

**ISP.** Internet service provider, such as Xfinity, Spectrum, AT&T, Verizon, T-Mobile, or Google Fiber.

**Fiber.** Internet delivered over fiber-optic lines. Usually the fastest and most consistent, with uploads as fast as downloads.

**Cable.** Internet delivered over the same coax lines as cable TV. Fast downloads, slower uploads, and shared with your neighborhood.

**5G home internet (fixed wireless).** Internet delivered over a cellular network to a gateway in your home.

**ONT.** The optical network terminal: the small box that converts a fiber line into an Ethernet connection for your router.

**Data cap.** A monthly limit on how much data you can use before extra charges or slower speeds.

**Broadband label.** A standardized label, required by the FCC, that shows a plan's monthly price, fees, and typical speeds.

**CGNAT.** When your provider shares one public IP address among many customers. It can interfere with hosting game servers or remote access.

## Mesh and wiring

**Mesh WiFi.** A system of two or more units (nodes) that work together to cover a whole home under one network name.

**Node or satellite.** A unit in a mesh system that isn't connected directly to the modem.

**Backhaul.** The connection between mesh nodes. It can be wireless or wired (Ethernet). Wired backhaul is faster and more reliable.

**Tri-band.** A router or mesh node with three radios, often used to give mesh backhaul its own band.

**Extender (repeater).** A device that picks up your WiFi and rebroadcasts it. Simpler and cheaper than mesh, but usually slower.

**MoCA.** A way to run an Ethernet connection over the coax cable already in many US homes.

**Multi-gig (2.5GbE, 10GbE).** Ethernet ports faster than 1 Gbps. Useful if your internet plan is faster than 1 Gbps or you use wired mesh backhaul.

**Cat5e, Cat6.** Ethernet cable types. Cat5e handles 1 Gbps and, at typical home lengths, 2.5 Gbps; Cat6 or better is a safer choice for 10 Gbps runs.

## Security

**WPA3.** The newest WiFi security standard. Use it if all your devices support it, or WPA2/WPA3 mixed mode if some don't.

**WPA2-AES.** The older but still acceptable security setting. Avoid WEP, WPA, and TKIP.

**WPS.** A push-button or PIN setup feature. Convenient, but a known weak spot. Turn it off.

**Guest network.** A separate network for visitors and smart-home devices that keeps them away from your computers and phones.

**Firmware.** The software that runs your router. Keep it updated. See our [router hardening checklist](/guides/router-hardening-checklist/).

**UPnP.** A feature that lets devices open ports on your router automatically. Handy for some games and risky if you don't need it.

**Port forwarding.** Manually letting outside traffic reach a device on your network, such as a game server or camera.

**DNS.** The internet's address book: it turns website names into addresses. Some DNS services can block malicious sites.

**VPN.** A service that encrypts traffic between your device and the VPN provider. Useful on public WiFi; it doesn't secure your router.

## Smart home

**Matter.** A smart-home standard that lets devices work with Apple Home, Google Home, Amazon Alexa, and SmartThings. See our [Matter and Thread guide](/guides/matter-thread-smart-home-explained/).

**Thread.** A low-power wireless network for smart-home devices like sensors and locks.

**Thread border router.** A device, often a smart speaker or streaming box, that connects a Thread network to your home network.

**IoT.** Internet of Things: smart plugs, cameras, thermostats, and other connected gadgets.
