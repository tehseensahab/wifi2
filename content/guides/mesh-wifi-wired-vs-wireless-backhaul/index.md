---
title: "Wired vs. Wireless Backhaul for Mesh Wi-Fi: How to Set It Up"
date: 2026-10-05
description: "Backhaul is the link between your mesh units. Here is how wired and wireless backhaul differ, how to cable a mesh system, and the mistakes to avoid."
authors: ["Tehseen Arbab"]
topics: ["mesh-wifi", "how-to-fixes"]
tags: ["mesh-wifi", "backhaul", "ethernet-backhaul", "moca", "eero", "deco", "orbi"]
summary: "Backhaul is the connection between mesh units. Wired backhaul uses an Ethernet cable, so the units stop spending Wi-Fi capacity talking to each other. Use it wherever you can run a cable; coax outlets with MoCA adapters are an alternative. If you can't wire anything, place units closer together and prefer a system with a third band. This is a research-based guide from manufacturer documentation, not a hands-on test."
imageAlt: "Ethernet cables plugged into the ports of a network switch on a wooden desk"
imageCredit: "Photo: Jonathan / [Unsplash](https://unsplash.com/photos/SwVkmowt7qA)"
takeaways:
  - "Backhaul is the link that carries traffic between mesh units. It can be wireless, wired with Ethernet, or a mix of both in one home."
  - "TP-Link says wired backhaul gives lower latency and no bandwidth loss from a wireless hop. Eero says Ethernet connections maximize speeds and reduce wireless interference."
  - "eero, TP-Link Deco, Netgear Orbi, ASUS AiMesh and Google Nest Wifi all support wired backhaul, but the cabling rules differ. Google requires every point to be wired downstream of the main router."
  - "Check for Ethernet ports before you plan cabling: eero Beacons, eero 6 Extenders and Google Nest Wifi points have none."
faq:
  - q: "What is backhaul in a mesh Wi-Fi system?"
    a: "Backhaul is the connection between the mesh units themselves, as opposed to the connection between a unit and your phone or laptop. Everything a far unit sends or receives travels over the backhaul to reach the main router."
  - q: "Is wired backhaul better than wireless backhaul?"
    a: "For performance, yes. A cable takes the unit-to-unit traffic off the airwaves. TP-Link describes the result as lower latency and no bandwidth loss from a wireless hop. Wireless backhaul is easier to install and can work well when units are close together with few walls between them."
  - q: "Can I mix wired and wireless backhaul?"
    a: "Yes, on the systems we checked. TP-Link says you can mix wired and wireless backhaul in the same Deco network, and eero says wired and wireless eeros can be part of one mixed network."
  - q: "Can I use a network switch for mesh backhaul?"
    a: "Usually. eero, TP-Link and Netgear all document connecting units through an Ethernet switch. An unmanaged gigabit switch is the simplest choice. TP-Link warns that some switches, mainly certain D-Link models, do not pass the traffic Deco units use to find each other."
  - q: "What if my house has no Ethernet wiring?"
    a: "Check for coax (cable TV) outlets. MoCA adapters send network traffic over coax, and the MoCA Alliance says the technology delivers real-world speeds up to 2.5 Gbps. Otherwise, use wireless backhaul and place units closer together."
sources:
  - title: "Can I connect my eeros with Ethernet?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/can-i-connect-my-eeros-with-ethernet"
  - title: "Ethernet Backhaul for Deco: Setup, Benefits and Troubleshooting"
    publisher: "TP-Link Support"
    url: "https://www.tp-link.com/us/support/faq/1794/"
  - title: "What is Ethernet backhaul and how do I set it up on my Orbi WiFi System?"
    publisher: "Netgear Support"
    url: "https://kb.netgear.com/000051205/What-is-Ethernet-backhaul-and-how-do-I-set-it-up-on-my-Orbi-WiFi-System"
  - title: "[AiMesh] What is Ethernet Backhaul Mode/Backhaul Connection Priority in AiMesh System and how to set up in different scenarios?"
    publisher: "ASUS Support"
    url: "https://www.asus.com/support/faq/1044184/"
  - title: "Hardwire Nest Wifi Pro, Nest Wifi, or Google Wifi with Ethernet"
    publisher: "Google Nest Help"
    url: "https://support.google.com/googlenest/answer/7215624?hl=en"
  - title: "Deco BE85 (Deco 7 Elite BE22000) product page"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/us/deco-mesh-wifi/product-family/deco-be85/"
  - title: "MoCA technology"
    publisher: "MoCA Alliance"
    url: "https://mocalliance.org/technology/"
  - title: "Wi-Fi Alliance introduces Wi-Fi CERTIFIED 7"
    publisher: "Wi-Fi Alliance"
    url: "https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-7"
    date: 2024-01-08
---

Backhaul is the connection between the units of a mesh Wi-Fi system. Wired backhaul means the units are joined by Ethernet cable. Wireless backhaul means they talk to each other over Wi-Fi. If you can run a cable between units, wired backhaul is the better choice. If you can't, wireless backhaul still works, and placement decides how well.

This is a research-based guide. It draws on the manufacturers' own setup documentation for five mesh systems. We have not tested these systems ourselves, and the performance statements below are the manufacturers' claims, labeled as such.

## What is backhaul?

A mesh system has a main router, connected to your modem, and one or more extra units placed around the home. Brands call the extra units nodes, satellites or points.

Each unit does two jobs. It talks to your devices, such as phones, laptops and TVs. And it passes their traffic back to the main router. That second link, unit to unit, is the backhaul. When you stream video in a far bedroom, the data goes from the internet to the main router, across the backhaul to the bedroom unit, and then to your TV.

A weak backhaul limits everything behind it. A unit can show full signal bars on your phone and still be slow, because its own link back to the router is poor.

## How do wired and wireless backhaul differ?

| | Wireless backhaul | Wired (Ethernet) backhaul |
|---|---|---|
| What carries unit-to-unit traffic | Wi-Fi | Ethernet cable |
| Installation | Plug in and place | Needs a cable run to each wired unit |
| Affected by walls and distance | Yes | No |
| Uses Wi-Fi capacity that devices could use | Yes | No |
| Speed limit | The Wi-Fi link between units | The slowest Ethernet port, switch or cable in the path |
| Where units can go | Within good Wi-Fi range of another unit | Anywhere a cable reaches |

### Wireless backhaul

With wireless backhaul, a unit receives data over Wi-Fi and sends it on over Wi-Fi. That traffic competes for airtime with your devices unless the system keeps it apart.

Some three-band (tri-band) systems reserve one band for backhaul. ASUS's documentation, for example, says that on its tri-band AiMesh routers the second 5 GHz band is "a dedicated backhaul by default." A two-band system has no spare band, so backhaul and devices share.

Wi-Fi 7 adds another approach, Multi-Link Operation (MLO), which the Wi-Fi Alliance says lets devices "transmit and receive data simultaneously over multiple links." Some Wi-Fi 7 mesh systems apply it to the link between units. TP-Link, for example, says its Deco BE85 combines "wired and wireless backhaul with the power of Wi-Fi 7 Multi-Link Operation." How each brand does this varies, so check the specific model.

Wireless backhaul depends on placement. Each unit needs a strong signal from the unit it connects to, so a unit placed in the dead zone itself has a poor backhaul.

### Wired backhaul

With wired backhaul, an Ethernet cable carries the unit-to-unit traffic. TP-Link says of its Deco systems that this gives "lower latency and no bandwidth loss from a wireless hop." Eero says Ethernet connections "maximize your internet speeds and reduce wireless interference." Netgear says Ethernet backhaul "can improve your Orbi WiFi system's performance if your router and satellites are placed very far apart."

There is a second benefit on some systems. Once the units are cabled, the band that was reserved for backhaul can serve your devices. ASUS says that with its Ethernet Backhaul Mode turned on, that second 5 GHz band "has been opened to end devices."

Wired backhaul also frees you to place a unit where coverage is needed, such as a detached office or a basement, even if no Wi-Fi signal reaches it.

## Can I mix wired and wireless backhaul?

Yes, on the systems we checked. TP-Link says: "You can mix wired and wireless backhaul in the same network." Eero says units without Ethernet ports "can be part of a mixed network of wired and wireless eeros."

This makes a partial upgrade worthwhile. Wiring only the unit that serves your home office, or the one farthest from the router, improves that unit and leaves less wireless traffic for the others to share.

## How do I set up wired backhaul?

The general steps are the same across brands. Then check the brand-specific rule in the table below.

1. **Confirm your units have Ethernet ports.** Some don't. Eero says its Beacons and eero 6 Extenders have no Ethernet ports, and Google says Nest Wifi points "don't have Ethernet ports and can't be hardwired."
2. **Update the firmware on every unit.** Netgear tells Orbi owners to do this before setting up Ethernet backhaul. ASUS's Ethernet Backhaul Mode needs firmware version 386 or later.
3. **Set the system up wirelessly first, if your brand says so.** TP-Link's instructions are to add all Deco units in the app first, then connect the cables.
4. **Run the cable.** Connect the main router to each unit, directly or through a switch. Eero specifies Cat5e, Cat6 or Cat6a cable; our [Ethernet cable guide]({{< relref "/guides/ethernet-cable-cat5e-vs-cat6-vs-cat6a" >}}) explains which to buy.
5. **Let the system switch over.** On Deco, TP-Link says no extra app configuration is needed, and the Wi-Fi backhaul between cabled units "disconnects automatically." ASUS has you turn on Ethernet Backhaul Mode, and warns that every node must be cabled first or a node "might lose its uplink connection."
6. **Check the result in the app.** Most mesh apps show how each unit is connected. Confirm it says wired or Ethernet before you tidy the cables away.

### Cabling layouts

There are three common ways to cable a mesh system. Not every brand documents all three.

- **Star.** Each unit has its own cable back to the main router.
- **Switch.** The main router connects to an Ethernet switch, and the units connect to the switch.
- **Daisy chain.** The router connects to unit one, unit one connects to unit two, and so on.

| System | Layouts the manufacturer documents | Rule to know |
|---|---|---|
| eero | Through a switch, or daisy chain | The gateway eero stays connected to the modem; Beacons and eero 6 Extenders can't be wired |
| TP-Link Deco | Direct to the main Deco, or through a switch | Set up wirelessly first; avoid creating a network loop |
| Netgear Orbi | Star, daisy chain, or through a switch | Update firmware first; use switch ports at least as fast as the Orbi's ports |
| ASUS AiMesh | Cabled nodes with Ethernet Backhaul Mode | Cable every node before turning the mode on |
| Google Nest Wifi and Google Wifi | Modem to router to point, or modem to router to switch to points | Every point must be "wired downstream from the Wifi router"; Nest Wifi points can't be wired |

Google's rule catches people out. The order has to be modem, then the main Wifi router, then any switch, then the points. A point plugged into equipment that sits ahead of the main router will not join the mesh correctly.

## What mistakes should I avoid?

- **A slow link in the chain.** Wired backhaul is only as fast as its slowest part. Netgear's Orbi article notes that the Ethernet ports on the models it covers are rated at 1 Gbps and says to use switch ports of 1 Gbps or faster. If your internet plan and mesh units support multi-gigabit speeds, the switch and cables need to as well.
- **The wrong switch.** A basic unmanaged switch is the safe choice. TP-Link warns that "some switches, mainly the D-Link switches, will not forward packets based on IEEE 1905.1 protocol," which Deco units rely on to find each other over Ethernet.
- **A network loop.** A loop forms when there are two cabled paths between the same pieces of equipment. TP-Link's guidance stresses avoiding loops. Give each unit one cabled path back to the router.
- **Assuming it worked.** If a cable is damaged or in the wrong port, the system may quietly stay on wireless backhaul. Check the app.

## What if I can't run Ethernet?

**Use the coax already in the walls.** Our [MoCA guide]({{< relref "/guides/what-is-moca-ethernet-over-coax" >}}) covers this in full. Many US homes have coaxial cable outlets from cable TV. MoCA (Multimedia over Coax Alliance) adapters send network traffic over that cable, with one adapter at the router and one at each mesh unit. The MoCA Alliance says the technology "delivers real world home networking speeds up to 2.5 Gbps." That figure is the alliance's own claim; results depend on the adapters and the condition of your wiring. From the mesh system's point of view, a MoCA link is an Ethernet connection.

**Improve the wireless backhaul.** If cabling isn't possible:

- Move units closer to the main router. A unit should sit where the signal from the router is still strong, roughly partway toward the weak area, not inside it.
- Reduce the walls and floors between units. Stairwells and open doorways help.
- If you are buying, a tri-band system leaves more room for backhaul than a dual-band one. Our [mesh picks for large houses]({{< relref "/guides/best-mesh-wifi-for-large-house" >}}) covers which systems suit wireless-only homes.

If you are not sure a mesh system is what you need, start with [Wi-Fi router vs. mesh]({{< relref "/guides/wifi-router-vs-mesh" >}}). And if a far room is still slow after cabling, the cause may be the device or its band, which [our slow Wi-Fi checklist]({{< relref "/guides/how-to-fix-slow-wifi" >}}) helps you find.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| eero units can be connected by Ethernet through a switch or by daisy chain, using Cat5e, Cat6 or Cat6a cable; Beacons and eero 6 Extenders have no Ethernet ports | [eero Support](https://eero.com/support/articles/can-i-connect-my-eeros-with-ethernet) | Verified from manufacturer documentation as of October 5, 2026 |
| Ethernet connections "maximize your internet speeds and reduce wireless interference" | [eero Support](https://eero.com/support/articles/can-i-connect-my-eeros-with-ethernet) | Qualified: a manufacturer's claim; not tested by us |
| Deco Ethernet backhaul gives "lower latency and no bandwidth loss from a wireless hop"; wired and wireless backhaul can be mixed; Wi-Fi backhaul between cabled units disconnects automatically | [TP-Link Support FAQ 1794](https://www.tp-link.com/us/support/faq/1794/) | Qualified: a manufacturer's description of its own product; not tested by us |
| Some switches, mainly D-Link models, do not forward IEEE 1905.1 packets used by Deco | [TP-Link Support FAQ 1794](https://www.tp-link.com/us/support/faq/1794/) | Qualified: TP-Link's statement; it does not list specific models |
| Orbi supports star, daisy-chain and switch layouts; firmware should be updated first; ports on the covered models are rated at 1 Gbps | [Netgear Support](https://kb.netgear.com/000051205/What-is-Ethernet-backhaul-and-how-do-I-set-it-up-on-my-Orbi-WiFi-System) | Qualified: port speeds differ between Orbi models, so check yours |
| On ASUS tri-band AiMesh routers the second 5 GHz band is a dedicated backhaul by default and is opened to devices in Ethernet Backhaul Mode; firmware 386 or later is required | [ASUS Support FAQ 1044184](https://www.asus.com/support/faq/1044184/) | Verified from manufacturer documentation as of October 5, 2026 |
| Google points must be wired downstream of the main Wifi router; Nest Wifi points have no Ethernet ports | [Google Nest Help](https://support.google.com/googlenest/answer/7215624?hl=en) | Verified from manufacturer documentation as of October 5, 2026 |
| MoCA delivers real-world home networking speeds up to 2.5 Gbps over coax | [MoCA Alliance](https://mocalliance.org/technology/) | Qualified: the industry alliance's own figure; depends on adapters and wiring |
| Wi-Fi 7's Multi-Link Operation lets devices transmit and receive over multiple links at once | [Wi-Fi Alliance press release, January 8, 2024](https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-introduces-wi-fi-certified-7) | Verified; how mesh brands use it for backhaul varies by model |
| TP-Link Deco BE85 combines wired and wireless backhaul with Multi-Link Operation | [TP-Link US product page](https://www.tp-link.com/us/deco-mesh-wifi/product-family/deco-be85/) | Qualified: a manufacturer's product claim; not tested by us |

## Bottom line

Backhaul is the part of a mesh system you don't see, and it sets the limit for every unit beyond the main router. Cable it where you can, even if that is only one unit. Follow your brand's layout rule, use a plain gigabit or faster switch, and confirm in the app that the units report a wired connection. Where cabling isn't possible, try coax with MoCA adapters, and failing that, move the units closer together.
