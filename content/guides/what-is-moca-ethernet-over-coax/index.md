---
title: "What Is MoCA? How to Use Coax Cable Instead of Ethernet"
date: 2026-10-07
description: "MoCA adapters send your home network over the coax cable already in the walls, at up to 2.5 Gbps. Here is how it works, what to buy and what to check."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "mesh-wifi"]
tags: ["moca", "ethernet-over-coax", "wired-backhaul", "coax", "home-network", "mesh-wifi"]
summary: "MoCA is a standard for sending network traffic over coaxial cable, the kind installed for cable TV. A pair of MoCA 2.5 adapters can link a router to a distant room at up to 2.5 Gbps without new wiring. It works alongside cable TV and cable internet, but not on coax used by satellite TV, and you should fit a point-of-entry filter. This is a research-based guide, not a hands-on test."
imageAlt: "Hand holding a coaxial TV cable connector near the back of a device"
imageCredit: "Generic coax connector, not a MoCA adapter. Photo: Zulfugar Karimov / [Unsplash](https://unsplash.com/photos/YAmlr-6eDMg)"
takeaways:
  - "MoCA stands for Multimedia over Coax Alliance. Its 2.5 specification, approved April 13, 2016, supports actual data rates up to 2.5 Gbps and up to 16 devices on one coax network."
  - "MoCA 2.5 adapters work with older MoCA 2.0 and 1.1 equipment, but MoCA 2.0 tops out at 1 Gbps."
  - "The MoCA Alliance says the technology is designed to coexist with TV and cable internet (DOCSIS) signals. Adapter maker goCoax says standard MoCA and satellite TV cannot share the same coax."
  - "A point-of-entry (PoE) filter, fitted where the coax enters your home, stops MoCA signals from leaking out to neighbors."
faq:
  - q: "Is MoCA as fast as Ethernet?"
    a: "It can match common home Ethernet speeds. The MoCA 2.5 specification supports actual data rates up to 2.5 Gbps, the same as the 2.5 Gbps ports on many current routers. Your result depends on the adapters, their Ethernet ports, the splitters and the condition of the coax."
  - q: "Can I use MoCA with cable internet?"
    a: "Usually yes. The MoCA Alliance says MoCA is designed to coexist with TV and DOCSIS, the technology cable internet uses. Adapter maker goCoax notes that some newer DOCSIS 3.1 modems use higher frequencies and need a splitter and filter arrangement to keep the two signals apart."
  - q: "Does MoCA work with satellite TV?"
    a: "Not on the same cable. goCoax states that normal MoCA and satellite TV cannot operate together on the same coaxial network because of interference. If satellite TV uses your coax, you would need a separate coax run or a different approach."
  - q: "Do I need a MoCA filter?"
    a: "Yes, in most homes. A point-of-entry filter blocks MoCA signals from leaving through the incoming coax line, which keeps your network private and avoids interfering with neighbors. Install it where the coax enters the home."
  - q: "How many MoCA adapters do I need?"
    a: "At least two: one next to the router and one in each room you want to connect. A MoCA 2.5 network supports up to 16 devices, so you can add an adapter in each additional room."
sources:
  - title: "MoCA Home technology"
    publisher: "MoCA Alliance"
    url: "https://mocalliance.org/technology/"
  - title: "Home Networking Gets a New Performance Standard"
    publisher: "MoCA Alliance"
    url: "https://mocalliance.org/news/rm_160416_moca-approved-specification-moca-2-5/"
    date: 2016-04-13
  - title: "MA2500D"
    publisher: "goCoax"
    url: "https://www.gocoax.com/ma2500d"
  - title: "When do I need a MoCA Filter and how do I use one in my HTEM5 MoCA network?"
    publisher: "Hitron Support"
    url: "https://ussupport.hitrontech.com/portal/en/kb/articles/when-do-i-need-a-moca-filter-and-how-do-i-use-one-in-my-moca-network"
---

MoCA is a way to send your home network over coaxial cable, the round screw-on cable installed for cable TV. If your house has coax outlets in the rooms where Wi-Fi is weak, a pair of MoCA adapters can turn that cable into a wired network link at up to 2.5 Gbps, with no new cable to run.

MoCA stands for Multimedia over Coax Alliance, the industry group that writes the specification and certifies products. This is a research-based guide. It draws on the alliance's published specifications and on documentation from two adapter makers. We have not tested MoCA adapters ourselves, and the speed figures are specification and manufacturer claims.

## How does MoCA work?

A MoCA adapter is a small box with a coax connector and an Ethernet port. One adapter sits next to your router, connected to it by Ethernet and to the wall by coax. A second adapter sits in another room, connected to that room's coax outlet. The two adapters find each other over the coax in the walls and behave like a long Ethernet cable between the two rooms.

The reason this can share a cable with other services is frequency. Different signals travel on the same coax at different frequencies, the way radio stations share the air. The MoCA Alliance gives the technology's overall operating range as 400 MHz to 1,675 MHz. Adapter maker goCoax says its MoCA 2.5 adapter works in the 1,125 to 1,675 MHz band, and describes cable internet's typical upper limit as 1,002 MHz. MoCA sits above it.

To your router and devices, a MoCA link looks like Ethernet. There are no network names or Wi-Fi passwords involved.

## How fast is MoCA?

| Version | Data rate in the specification | Notes |
|---|---|---|
| MoCA 2.0 | Up to 1 Gbps | Older adapters |
| MoCA 2.5 | Up to 2.5 Gbps | Approved April 13, 2016; up to 16 devices per network |

The MoCA Alliance describes both figures as "actual data rates." MoCA 2.5 is "backward interoperable with MoCA 2.0 and MoCA 1.1," so mixed equipment will connect. Expect a link that involves an older device to run at the older device's speed.

Three things decide what you get in practice:

- **The adapter's Ethernet port.** A MoCA 2.5 adapter with a 1 Gbps Ethernet port can't deliver more than 1 Gbps to the device plugged into it. For multi-gigabit speeds, look for a 2.5 Gbps Ethernet port. The goCoax MA2500D, for example, lists one 2.5GbE port.
- **Shared capacity.** Adapters on the same coax share one network, so heavy use in two rooms at once generally divides what is available.
- **The coax itself.** Old splitters, damaged cable and long runs reduce performance. We have no measured figures for how much, so treat 2.5 Gbps as a ceiling and not a promise.

For most homes this is academic. A plan of 1 Gbps or less fits comfortably inside a MoCA 2.5 link. See [how much internet speed you need]({{< relref "/guides/how-much-internet-speed-do-i-need" >}}) if you are sizing a plan.

## Will MoCA work in my home?

Check four things before buying.

| Question | What to look for | Why |
|---|---|---|
| Is there a coax outlet near the router and in the target room? | A threaded coax wall plate in each place | Each adapter needs a coax connection |
| Are those outlets connected to each other? | Outlets that feed from the same splitter, often in a basement, garage or outside box | Adapters only see each other on the same coax network |
| What else uses the coax? | Cable TV or cable internet is fine; satellite TV is not | goCoax says normal MoCA and satellite TV "cannot operate together on the same coaxial network due to interference" |
| What modem do you have? | Check whether it is a DOCSIS 3.1 model | goCoax says some newer modems use higher frequencies and need "a 2-way splitter" and "a PoE filter to separate DOCSIS and MoCA signals" |

The MoCA Alliance says the technology is "designed to co-exist with legacy services such as TV, DOCSIS, and cellular (4G/5G) technologies." DOCSIS is the technology cable internet providers use.

If your internet arrives by fiber or a 5G gateway and the coax in your walls carries nothing, MoCA is the simplest case: the cable is yours to use.

Splitters matter too. MoCA signals reach 1,675 MHz, so every splitter between your adapters has to pass frequencies that high. An old splitter rated only to about 1,000 MHz can block or weaken the link. This follows from the frequency range above; check the rating printed on each splitter.

## What do I need to buy?

- **Two or more MoCA 2.5 adapters.** One for the router end, one for each room. Choose adapters with a 2.5 Gbps Ethernet port if any of your equipment has 2.5 Gbps ports.
- **A point-of-entry (PoE) filter.** Check whether your adapter kit includes one before buying it separately.
- **Short Ethernet cables.** One per adapter. Our [Ethernet cable guide]({{< relref "/guides/ethernet-cable-cat5e-vs-cat6-vs-cat6a" >}}) covers which category to use.
- **Possibly new splitters,** if yours don't pass MoCA frequencies.

We have left prices out because we only publish a price with the date we checked it.

## Why do I need a point-of-entry filter?

Coax leaves your house. Without a filter, MoCA signals can travel back out along the incoming line. Hitron, which makes MoCA adapters, puts it this way: "MoCA filters block MoCA signals from leaking out of the home's coaxial cabling," and without one, signals can "interfere with neighboring MoCA networks or cable TV signals."

The filter is a small barrel-shaped connector. Hitron's instructions are to install it "at the point where the coaxial cable enters your home," on the incoming line, ahead of the first splitter.

There is a security reason as well. The MoCA 2.5 specification added "Enhanced Privacy" with longer passwords, and the alliance describes a security feature called MoCASec for link privacy. Even so, a filter is the simple way to keep your network's signals inside your own walls in the first place. Note that this "PoE" means point of entry. It is unrelated to Power over Ethernet, which shares the abbreviation.

## How do I set it up?

1. **Fit the PoE filter** where the coax enters the home.
2. **Connect the first adapter by the router.** Coax from the wall to the adapter, Ethernet from the adapter to a LAN port on the router. If a cable modem needs the same wall outlet, use a splitter, or the adapter's pass-through coax port if it has one.
3. **Connect the second adapter in the other room.** Coax from the wall to the adapter, Ethernet from the adapter to your device, switch or mesh unit.
4. **Wait for the link light.** Most adapters have a status light that shows a MoCA connection. If it stays off, the two outlets may not be on the same coax network, or a splitter may be blocking the signal.
5. **Set up the security option** if your adapters offer one, following the maker's instructions.
6. **Test the speed** on a computer wired to the far adapter.

## Is MoCA a good way to connect a mesh system?

Yes, where Ethernet isn't available. A mesh unit connected through a MoCA adapter is using wired backhaul as far as the mesh system is concerned. That takes the unit-to-unit traffic off Wi-Fi, which is the main benefit of cabling a mesh system. Our guide to [wired and wireless backhaul]({{< relref "/guides/mesh-wifi-wired-vs-wireless-backhaul" >}}) explains each brand's cabling rules, and they apply here too.

| | Ethernet cable | MoCA over coax | Wireless backhaul |
|---|---|---|---|
| New wiring needed | Yes, unless jacks exist | No, if coax outlets exist | No |
| Top speed | Depends on cable and ports; 1 to 10 Gbps | Up to 2.5 Gbps (MoCA 2.5 specification) | Depends on the Wi-Fi link between units |
| Extra hardware | None | Two or more adapters, a filter | None |
| Affected by walls and distance | No | No | Yes |
| Works with satellite TV on the same cable | Not applicable | No | Not applicable |

If you have Ethernet jacks in the right rooms, use those. If you have coax in the right rooms, MoCA is the next best option. If you have neither, see [mesh picks for large houses]({{< relref "/guides/best-mesh-wifi-for-large-house" >}}) for systems suited to wireless-only homes.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| MoCA 2.5 was approved on April 13, 2016, supports actual data rates up to 2.5 Gbps and up to 16 nodes, and is backward interoperable with MoCA 2.0 and 1.1 | [MoCA Alliance press release, April 13, 2016](https://mocalliance.org/news/rm_160416_moca-approved-specification-moca-2-5/) | Verified; a specification figure, not a measured home speed |
| MoCA 2.0 offers actual data rates up to 1 Gbps | [MoCA Alliance press release, April 13, 2016](https://mocalliance.org/news/rm_160416_moca-approved-specification-moca-2-5/) | Verified |
| MoCA operates between 400 MHz and 1,675 MHz and is designed to coexist with TV, DOCSIS and cellular signals | [MoCA Alliance, technology page](https://mocalliance.org/technology/) | Verified as the alliance's own description |
| A MoCA 2.5 adapter operates at 1,125 to 1,675 MHz, above cable internet's typical 1,002 MHz upper limit, and has a 2.5GbE port | [goCoax MA2500D product page](https://www.gocoax.com/ma2500d) | Qualified: one manufacturer's specifications; other adapters differ |
| Standard MoCA and satellite TV cannot share the same coax; some DOCSIS 3.1 modems need a splitter and PoE filter arrangement | [goCoax MA2500D product page](https://www.gocoax.com/ma2500d) | Qualified: a manufacturer's compatibility note; check your own modem and TV service |
| A point-of-entry filter blocks MoCA signals from leaving the home and belongs where the coax enters | [Hitron Support](https://ussupport.hitrontech.com/portal/en/kb/articles/when-do-i-need-a-moca-filter-and-how-do-i-use-one-in-my-moca-network) | Verified from manufacturer documentation as of October 7, 2026 |
| MoCA 2.5 added Enhanced Privacy with longer passwords | [MoCA Alliance press release, April 13, 2016](https://mocalliance.org/news/rm_160416_moca-approved-specification-moca-2-5/) | Verified |
| Splitters must pass frequencies up to 1,675 MHz | Our reasoning from the frequency ranges above | Qualified: an inference, not a tested result |

## Bottom line

MoCA turns coax you already have into a wired network link. It suits homes with coax outlets in the right rooms and no easy way to run Ethernet. Buy MoCA 2.5 adapters with Ethernet ports that match your equipment, fit a point-of-entry filter, and confirm nothing on that coax is satellite TV. If the link light comes on and a wired speed test looks right, you have the next best thing to Ethernet.
