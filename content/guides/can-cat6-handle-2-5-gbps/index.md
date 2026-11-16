---
title: "Can Cat 6 Handle 2.5 Gbps? Cat 5e, 6 and 6A Limits"
date: 2026-11-16T05:00:00Z
description: "Yes, Cat 6 can handle 2.5 Gbps over the full 100 meters, and so can Cat 5e. Here is what limits a multi-gig link and how to check the speed you get."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "routers"]
tags: ["ethernet-cable", "cat6", "cat5e", "cat6a", "2-5-gbps", "multi-gig", "nbase-t"]
summary: "Yes. Cat 6 handles 2.5 Gbps over the full 100-meter (328-foot) Ethernet run, and even Cat 5e does. If a 2.5 Gbps link shows 1 Gbps, the cable category is often not the cause: check the ports at both ends, the patch cords and jacks, and whether the cable is copper-clad aluminum."
imageAlt: "Blue Ethernet cable with a clear RJ45 plug resting on a network cable tester, on a green cutting mat"
imageCredit: "Photo: Gavin Allanwood / [Unsplash](https://unsplash.com/photos/a-close-up-of-a-network-tester-on-a-table--xITpL_gncA)"
takeaways:
  - "Cat 6 supports 2.5 Gbps and 5 Gbps over 100 meters (328 feet). Cat 5e supports 2.5 Gbps over 100 meters, according to Fluke Networks' summary of the IEEE 802.3bz standard."
  - "You don't need Cat 6A for 2.5 Gbps. It matters for 10 Gbps runs longer than about 55 meters (180 feet) on Cat 6, or 37 meters (121 feet) under worst-case bundling, per the TIA's TSB-155 bulletin."
  - "Multi-gig ports auto-negotiate a lower speed when they can't run the higher one, so a weak link often shows up as a lower speed, such as 1 Gbps, rather than as no connection."
  - "Check the negotiated speed in Windows (ncpa.cpl, then Status), on a Mac (System Settings > Network > Ethernet > Details > Hardware) or on your router's status page."
  - "Cable sold as Cat 6 with copper-clad aluminum (CCA) conductors is not standards-compliant, whatever the jacket says."
faq:
  - q: "Can Cat 6 handle 2.5 Gbps?"
    a: "Yes. IEEE 802.3bz, the standard behind 2.5 Gbps Ethernet over twisted pair, supports 2.5 Gbps over 100 meters of Cat 5e, and Cat 6 is rated for 5 Gbps over the same 100 meters, according to Fluke Networks. A Cat 6 run inside the normal 100-meter limit has room to spare at 2.5 Gbps."
  - q: "What Cat cable do I need for 2.5 Gbps?"
    a: "Cat 5e or better. The NBASE-T Alliance, the industry group whose specification fed into IEEE 802.3bz, says it supports 2.5 Gbps and 5 Gbps 'over 100m of Category 5e or better cabling.' Buy Cat 6 for new cable if you might move to 5 Gbps later."
  - q: "Why does my 2.5 Gbps port only connect at 1 Gbps?"
    a: "Common causes are that one end isn't a 2.5 Gbps port, or because a patch cord, jack or the cable itself can't hold the higher speed. Multi-gig ports drop to a lower speed when the cabling can't support the higher one. Swap the patch cords first, then test the device on a short cable plugged straight into the router."
  - q: "Do I need Cat 6A for a 2.5 Gbps internet plan?"
    a: "No. Cat 6A is for 10 Gbps over long runs. For a 2.5 Gbps plan, Cat 5e and Cat 6 are both rated to 100 meters at 2.5 Gbps."
  - q: "Does Ethernet link speed tell me my internet speed?"
    a: "No. The link speed is what your device's adapter and the router or switch port agreed on. TP-Link's Omada support page puts it plainly: 'It does not represent your Internet speed.' Run a speed test for that."
sources:
  - title: "IEEE 802.3bz-2016: 2.5 Gb/s and 5 Gb/s Operation, Types 2.5GBASE-T and 5GBASE-T"
    publisher: "IEEE Standards Association"
    url: "https://standards.ieee.org/ieee/802.3bz/6130/"
    date: 2016-10-18
  - title: "Will My Existing Cable Plant Support 2.5/5GBASE-T?"
    publisher: "Fluke Networks"
    url: "https://flukenetworks.com/blog/cabling-chronicles/will-my-existing-cable-plant-support-255gbase-t"
    date: 2018-01-17
  - title: "Frequently Asked Questions (NBASE-T)"
    publisher: "NBASE-T Alliance (archived by the Ethernet Alliance)"
    url: "https://archive.nbaset.ethernetalliance.org/wp-content/uploads/2019/02/FAQ_022119_v2.pdf"
    date: 2019-02-01
  - title: "Deploying 10GBASE-T with Cisco Switches: Choose the Right Cabling"
    publisher: "Cisco"
    url: "https://www3-realm.cisco.com/en/US/prod/collateral/switches/ps5718/ps6021/white_paper_c11-609513.html"
  - title: "How to Check Ethernet Speed on Windows and Mac"
    publisher: "TP-Link Omada"
    url: "https://www.omadanetworks.com/us/support/faq/2899/"
    date: 2026-07-06
  - title: "How to check the wired connection speed and network cable specifications for ASUS Wireless router?"
    publisher: "ASUS"
    url: "https://www.asus.com/support/FAQ/1044349"
    date: 2024-07-22
  - title: "Do You Know What's Printed on Your Cable Jacket?"
    publisher: "Belden"
    url: "https://fr-prod102.belden.com/blog/Do-You-Know-What-is-Printed-on-Your-Cable-Jacket"
  - title: "Tips to Identify Copper Clad Aluminium (CCA) Cables"
    publisher: "Fluke Networks"
    url: "https://de.flukenetworks.com/blog/cabling-chronicles/cca-not-worth-savings-or-risk"
    date: 2017-01-18
---

Yes, Cat 6 can handle 2.5 Gbps, over the full 100-meter (328-foot) length allowed for an Ethernet run. So can Cat 5e. The 2.5 Gbps standard was designed to run on the Cat 5e and Cat 6 cabling already installed in many buildings, so a multi-gig internet plan or a router with a 2.5 Gbps port does not, by itself, mean rewiring. If your link shows 1 Gbps instead of 2.5 Gbps, the cable category is often not the reason; check the ports, patch cords, jacks and cable quality first.

This guide is based on the IEEE standard, the industry group that developed 2.5 Gbps Ethernet, and the cable-test and networking makers cited below. We have not tested cable runs ourselves.

## What Cat cable do I need for 2.5 Gbps?

Cat 5e or better. 2.5 Gbps and 5 Gbps Ethernet over copper come from IEEE 802.3bz, published on October 18, 2016 and since folded into the main IEEE 802.3 standard, which covers "balanced twisted-pair transmission media used in structured cabling." The NBASE-T Alliance, the industry group whose NBASE-T specification fed into the IEEE standard, says it "supports 2.5 Gbps and 5 Gbps rates over 100m of Category 5e or better cabling." Fluke Networks, which makes the testers installers use to certify cable, summarizes the standard as "2.5 Gbps over 100 meters of Category 5e cabling or 5 Gbps over 100 meters of Category 6 cabling."

| Cable | 2.5 Gbps | 5 Gbps | 10 Gbps |
|---|---|---|---|
| Cat 5e | 100 m | Only in "defined use cases" (Fluke) | Not covered in our sources |
| Cat 6 | 100 m | 100 m | About 55 m typical; 37 m in worst-case bundling |
| Cat 6A | 100 m | 100 m | 100 m |

Cat 6A is included under the NBASE-T Alliance's "Category 5e or better" wording for 2.5 and 5 Gbps. The 10 Gbps row comes from Cisco's cabling guide, which says "the IEEE standard lists 55 meters as the typical expected 10GBASE-T reach" on Cat 6, while the TIA's TSB-155 bulletin says that "under worst-case bundling conditions, the reach may be limited to 37 meters." Not every vendor page agrees: an ASUS router FAQ lists Cat 6 at 10 Gbps over 100 meters and calls its figures "only a theoretical value." For 2.5 Gbps, none of this matters. Cat 6 is rated for twice that speed at full length.

## Can Cat 6 handle 2.5 Gbps on a long run?

Yes, up to the 100-meter (328-foot) limit. The caution that does apply to long runs is alien crosstalk, which is interference between neighboring cables. Fluke says it "is a limiting factor in 2.5GBASE-T and 5GBASE-T applications" and that Cat 5e and Cat 6 "do not include alien crosstalk specifications." The risk is highest in long runs bundled tightly with other cables, such as a home's wiring closet. Fluke also mentions limiting 2.5 and 5 Gbps links to channels shorter than 50 meters as one option, and that "testing is really the only way to truly know if your links will work properly." In a house, the practical test is to plug in and check the negotiated speed, described below.

## Why does my 2.5 Gbps port only connect at 1 Gbps?

Multi-gig ports adjust down rather than fail. The NBASE-T FAQ says the chips "auto-negotiate the optimal network speed," which "allows link partners to choose a lower speed when the available cabling is not able to support" the higher one. So a marginal link usually works, just at 1 Gbps. Work through these in order:

1. **Both ends need 2.5 Gbps ports.** A link runs at the speed of the slower port. A 2.5 Gbps router port connected to a laptop, console or switch with a 1 Gbps port will show 1 Gbps on any cable. Check the device's spec sheet, not just the router's.
2. **Swap the patch cords.** The short cables at each end count toward the channel. ASUS's troubleshooting advice is to swap in another cable or device to see whether the problem is the cable or the unit.
3. **Test without the wall run.** Put the device next to the router on a short cable you know is Cat 5e or better. If it now shows 2.5 Gbps, the problem is in the wall run, its jacks or its terminations.
4. **Check the jacks and terminations.** Every part of the run counts, including the wall jacks and how the cable was terminated in them.
5. **Check what the cable actually is.** See the next section.

If the in-wall run still won't hold 2.5 Gbps after that, an electrician or low-voltage installer can test it, or you can use another path to the room, such as [MoCA over your coax](/guides/what-is-moca-ethernet-over-coax/).

## How can I tell what Ethernet cable is in my wall?

Read the print on the cable jacket. Belden, a cable maker, explains that jacket print typically includes the category, such as "CAT 5E," "CAT 6" or "CAT 6A"; the wire gauge (AWG); a fire rating, such as CMR for riser cable or CMP for plenum cable; and a safety listing such as UL. Look for it where the cable is visible, such as behind a wall plate, in a closet or in an attic.

The category alone doesn't prove the cable meets it. Copper-clad aluminum (CCA) cable uses aluminum conductors with a copper coating, and a jacket print alone won't tell you that. Fluke says CCA cables are "non-standards compliant" and "often do not have a valid UL safety listing." Its tips for spotting CCA: the box or spool is lighter than solid copper, because "aluminum is lighter than copper," and scraping a conductor reveals "silver colored aluminum beneath the copper cladding." If you're buying new cable, choose solid copper; our [Cat 5e vs. Cat 6 vs. Cat 6A guide](/guides/ethernet-cable-cat5e-vs-cat6-vs-cat6a/) covers what to buy.

## How do I check my Ethernet link speed?

The link speed is what your device and the router or switch port agreed on. TP-Link's Omada support page says the figure "does not represent your Internet speed," so use it to check the cable and ports, and a speed test for your plan.

- **Windows:** Press the Windows key + R, type `ncpa.cpl`, right-click **Ethernet** (or Local Area Connection) and select **Status**. The **Speed** shown is the link speed.
- **Mac:** Choose **Apple menu > System Settings**, click **Network**, select the Ethernet service, click **Details**, then **Hardware**.
- **ASUS router:** In the web interface, go to **Network Map > Status**. ASUS says the **Ethernet ports** section shows the speed of wired connections to the WAN and LAN ports. Other brands show this on a status or port page in their app or web interface.

A reading of 2.5 Gbps (or 2500 Mbps) means the two ends negotiated the full rate. If speeds still disappoint, a speed test to a device on the same network, or a cable tester, shows whether the link holds up.

## When should I upgrade to Cat 6A?

Only when you need 10 Gbps over a long run. For a 2.5 Gbps or 5 Gbps router, switch or internet plan, Cat 6 already covers the full 100 meters. If you're opening walls anyway and want to be ready for 10 Gbps runs longer than about 55 meters, Cat 6A is the cable rated for that. Before paying for any multi-gig upgrade, check whether your plan and devices can use it; our guide to [whether you need a multi-gig router](/guides/do-you-need-a-multi-gig-router/) walks through that, and a wired connection between mesh units is covered in our [wired vs. wireless backhaul guide](/guides/mesh-wifi-wired-vs-wireless-backhaul/).

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| IEEE 802.3bz defines 2.5 and 5 Gb/s Ethernet over twisted-pair structured cabling; published October 18, 2016; now superseded (folded into IEEE 802.3) | [IEEE Standards Association](https://standards.ieee.org/ieee/802.3bz/6130/) | Verified |
| 2.5 Gbps over 100 m of Cat 5e; 5 Gbps over 100 m of Cat 6; 5 Gbps on Cat 5e only in defined use cases; alien crosstalk is a limiting factor; testing is the only sure check | [Fluke Networks, Jan. 17, 2018](https://flukenetworks.com/blog/cabling-chronicles/will-my-existing-cable-plant-support-255gbase-t) | Verified (test-equipment maker's summary of the standard) |
| 2.5 and 5 Gbps over 100 m of Cat 5e or better; ports auto-negotiate a lower speed when cabling can't support the higher one | [NBASE-T Alliance FAQ, Feb. 2019](https://archive.nbaset.ethernetalliance.org/wp-content/uploads/2019/02/FAQ_022119_v2.pdf) | Verified |
| 10 Gbps on Cat 6: 55 m typical, 37 m worst case (TSB-155); Cat 6A 100 m | [Cisco cabling white paper](https://www3-realm.cisco.com/en/US/prod/collateral/switches/ps5718/ps6021/white_paper_c11-609513.html) | Qualified (undated; vendor summary of IEEE and TIA documents) |
| Windows and Mac steps to see link speed; link speed is not internet speed | [TP-Link Omada FAQ 2899, updated July 6, 2026](https://www.omadanetworks.com/us/support/faq/2899/) | Verified |
| ASUS router port speeds under Network Map > Status; swap cables to isolate a fault | [ASUS FAQ 1044349, updated July 22, 2024](https://www.asus.com/support/FAQ/1044349) | Verified |
| Jacket print shows category, AWG, fire rating (CMR, CMP) and safety listing | [Belden](https://fr-prod102.belden.com/blog/Do-You-Know-What-is-Printed-on-Your-Cable-Jacket) | Verified (undated) |
| CCA cable is not standards-compliant; lighter than copper; scraping reveals aluminum | [Fluke Networks, Jan. 18, 2017](https://de.flukenetworks.com/blog/cabling-chronicles/cca-not-worth-savings-or-risk) | Verified |
