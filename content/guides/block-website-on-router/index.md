---
title: "How to Block a Website on Your Router, Brand by Brand"
date: 2026-11-01T05:00:00Z
description: "How to block a website on your router: the menus for eero, ASUS, NETGEAR, TP-Link Archer and Deco, plus why blocks fail and how to make them stick."
authors: ["Tehseen Arbab"]
topics: ["security-privacy", "how-to-fixes"]
tags: ["parental-controls", "website-blocking", "url-filter", "eero", "asus", "netgear", "tp-link", "deco", "dns-over-https"]
summary: "To block a website on your router, open its parental controls or URL filter, add the site's domain (for example, example.com), and save. The menu differs by brand: eero needs eero Plus, ASUS uses Firewall > URL Filter, NETGEAR uses Block Sites, and TP-Link uses Parental Controls profiles. Blocks can fail because of browser caches, extra domains, private MAC addresses or encrypted DNS, so test after you set them."
imageAlt: "Open combination padlock resting on a white computer keyboard"
imageCredit: "Photo: Sasun Bughdaryan / [Unsplash](https://unsplash.com/photos/a-combination-lock-rests-on-a-computer-keyboard-WUJmdr8pNwk)"
takeaways:
  - "Enter a domain, not a full URL. eero, for example, won't accept https:// addresses, and blocking example.com covers its subdomains while www.example.com covers only that subdomain."
  - "eero's Block & Allow Sites is an eero Plus feature. ASUS, NETGEAR and TP-Link include basic site blocking in the router's own settings."
  - "ASUS says its URL filter can't block a site for one specific device; it applies to the whole network. NETGEAR's app, eero and TP-Link can block per profile."
  - "TP-Link says parental controls won't take effect if a device uses a private MAC address, and both eero and TP-Link say a browser cache can delay a block."
  - "Firefox ignores a network's DNS filtering signal if a user has manually turned on DNS over HTTPS, so DNS-based router blocking isn't tamper-proof."
faq:
  - q: "Can I block a website for just one device?"
    a: "On most brands, yes, by putting the device in a parental-controls profile: eero, TP-Link (Archer and Deco) and NETGEAR's Smart Parental Controls block per profile. ASUS says its URL filter doesn't support blocking a site for one specific device."
  - q: "Why does a blocked website still load?"
    a: "Common reasons: your browser or device cached the site, the site uses other domains you haven't blocked, the device uses a private MAC address so it isn't matched to its profile, or the device uses encrypted DNS, a VPN or cellular data that skips your router's filter."
  - q: "Do I need a subscription to block websites on my router?"
    a: "Not on most routers. ASUS, NETGEAR and TP-Link include site blocking in their settings. On eero, Block & Allow Sites requires eero Plus. NETGEAR's Smart Parental Controls also offers a Premium subscription; check the app for what's included on your model."
  - q: "Should I type the full web address?"
    a: "No. Enter the domain, such as example.com. eero says URLs aren't accepted, and TP-Link's Deco guide recommends entering the full domain name rather than keywords."
sources:
  - title: "What is Block & Allow Sites?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/what-is-block-and-allow-sites"
  - title: "[Wireless Router] How to set up the URL Filter - Black/White List? (Firewall)"
    publisher: "ASUS"
    url: "https://www.asus.com/us/support/FAQ/1037946"
    date: 2024-07-22
  - title: "How do I block Internet sites on my NETGEAR router from the router web interface?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/24053/How-do-I-block-Internet-sites-on-my-NETGEAR-router-from-the-router-web-interface"
    date: 2025-07-07
  - title: "How do I block or allow access to a website with NETGEAR Smart Parental Controls?"
    publisher: "NETGEAR"
    url: "https://kb.netgear.com/000062159/How-do-I-block-or-allow-access-to-a-website-with-NETGEAR-Smart-Parental-Controls"
    date: 2025-07-07
  - title: "How to configure Parental Control on TP-Link Wi-Fi Router"
    publisher: "TP-Link (VIGI mirror)"
    url: "https://vigi.com/baltic/support/faq/1124"
    date: 2025-10-21
  - title: "Troubleshooting Guide: TP-Link Router/Deco Parental Control Not Working as Expected"
    publisher: "TP-Link"
    url: "https://www.tp-link.com/us/support/faq/2643"
    date: 2026-08-25
  - title: "Configure networks to disable DNS over HTTPS"
    publisher: "Mozilla Support"
    url: "https://support.mozilla.org/en-US/kb/configuring-networks-disable-dns-over-https/revision/289782"
    date: 2024-12-01
---

To block a website on your router, sign in to its app or web settings, find the parental controls or URL filter, add the site's domain (such as example.com) to the block list, and save. Then test it on the device you're trying to block, because a cached page or a second domain can make the block look broken. The exact menu depends on your router's brand; the steps for eero, ASUS, NETGEAR, TP-Link Archer and TP-Link Deco are below, taken from each maker's support pages.

Router-level blocking covers every device on your Wi-Fi without installing anything on them. It doesn't follow a phone onto cellular data, and a determined user can get around it (see [why blocks fail](#why-a-blocked-site-still-loads)). Menus can differ by model and firmware; if yours doesn't match, search your maker's support site for your model number.

## Before you start: what to type

- **Use the domain, not the URL.** Type `example.com`, not `https://www.example.com/page`. eero says URLs aren't accepted, and TP-Link tells Deco users to enter "the full domain name of the websites rather than the keywords."
- **Know what the entry covers.** On eero, blocking `example.com` "affects the entire domain," including subdomains, while `www.example.com` covers only that one subdomain.
- **Expect more than one domain.** eero warns that popular sites may need several domains blocked. TP-Link suggests checking a profile's History page to find the related domains a site redirects to.

## eero (eero app, needs eero Plus)

eero calls this **Block & Allow Sites**, and it's "an eero Plus feature."

**For one person's devices:**

1. On the **Home** tab, tap the person's **Profile**.
2. Tap **Block & Allow Sites**.
3. Tap **Add Blocked Site**, enter the domain, and turn on the toggle.
4. Tap **Save**.

**For the whole network:** go to **Home > Security & privacy > eero Plus > Network controls > Block & Allow Sites** and add the domain the same way.

eero says allowed sites "always take priority over Content Filters and Blocked Sites," and changes usually apply within seconds, though caches can delay them by minutes or hours. To decide whether Plus is worth paying for, see [Is eero Plus worth it?]({{< relref "/guides/is-eero-plus-worth-it" >}}).

## ASUS (web settings: Firewall > URL Filter)

1. Open `http://www.asusrouter.com` (or your router's LAN IP) and sign in.
2. Go to **Firewall** and choose the **URL Filter** tab.
3. Turn the URL Filter on and set the list type to **Black List** (block the listed sites) or **White List** (allow only listed sites).
4. Enter the address, click **+**, then **Apply**.

The catch: ASUS's FAQ (last updated July 22, 2024) says its routers don't support blocking a website for one specific device, or exempting particular devices from the URL filter. Treat it as a whole-network block.

## NETGEAR Nighthawk (web settings: Block Sites)

1. Go to `www.routerlogin.net` and sign in as admin.
2. Open **ADVANCED > Security > Block Sites**. Some models use **Settings > Content Filtering > Block Sites** instead.
3. Under **Keyword Blocking**, choose **Per Schedule** or **Always**.
4. Type a keyword or domain, click **Add Keyword**, and click **Apply**.

NETGEAR's article (last updated July 7, 2025) lists many Nighthawk routers, such as the R7000, RAX50 and XR1000. It doesn't list Orbi systems.

## NETGEAR Orbi and Nighthawk app (Smart Parental Controls)

On models managed with the Orbi or Nighthawk app, including Orbi systems and the RS100, RS200 and RS300, NETGEAR's knowledge base describes per-profile blocking in the app:

1. Open the **Orbi** or **Nighthawk** app and tap **Parental Controls**.
2. Pick the profile, then open its **History** tab.
3. Swipe right on a website and choose **Set as Not Allowed**.

Because this works from history, the person's device needs to have visited the site first. NETGEAR's article doesn't say whether this needs a paid Smart Parental Controls tier; check the app on your model.

## TP-Link Archer (web settings or app: Parental Controls)

1. Sign in to your router and go to **Advanced > Parental Controls**.
2. Click **Add** to create a profile for a family member and add their devices.
3. At the blocked-content step, add keywords. TP-Link says "all websites containing the keywords will be blocked."
4. Save the profile.

Two cautions from TP-Link's guide (updated October 21, 2025), which covers many Archer models, including the A7 and AX3000: turn off the private MAC address on the profile's devices, "otherwise, the parental control won't take effect," and only devices that have already joined your network show up in the list. Our [private Wi-Fi address guide]({{< relref "/guides/private-wifi-address" >}}) explains how that setting works and when to turn it off. A broad keyword can block more than you mean to: "news" would catch every domain containing it.

## TP-Link Deco (Deco app)

In the Deco app, open **Parental Controls**, select the person's profile, and go to its **Blocked Websites** page. Tap **Add a Website** and enter the full domain name. TP-Link's troubleshooting page (updated August 25, 2026) says to confirm the Malicious Content Filter is turned on under Security if blocking doesn't work, to add redirect domains from the profile's History page, and to clear the browser cache before testing again.

## Why a blocked site still loads

| Cause | What to do |
|---|---|
| Browser or device cache | Clear the browser cache, or restart the device. eero and TP-Link both list this. |
| The site uses other domains | Block the parent domain, and add redirect domains from the profile's history. |
| Device uses a private (random) MAC address | Turn it off for your network so the device matches its profile (TP-Link). |
| Encrypted DNS (DNS over HTTPS) | Check the browser's secure DNS setting; see below. |
| VPN or cellular data | A VPN hides which sites a device visits from your router, and cellular data skips your router entirely. Use the device's own parental controls too. |

On encrypted DNS: Mozilla's support page says Firefox checks for network filtering and parental controls and turns its automatic DNS over HTTPS off when it finds them. But "if a user has chosen to manually enable DoH, the signal from the network will be ignored." In other words, a router block works against casual browsing, not against someone who changes their browser settings. For stronger controls, pair router blocking with device-level parental controls; our [parental controls router guide]({{< relref "/guides/best-router-for-parental-controls" >}}) compares what each brand offers, and [How to see who's connected to your Wi-Fi]({{< relref "/guides/see-who-is-connected-to-my-wifi" >}}) helps you find every device to put in a profile.

## Sources and verification

| Important claim | Source | Status |
|---|---|---|
| eero Block & Allow Sites steps; eero Plus required; domain rules; allowed sites take priority | [eero Support](https://eero.com/support/articles/what-is-block-and-allow-sites) | Verified |
| ASUS URL Filter steps; no per-device blocking | [ASUS](https://www.asus.com/us/support/FAQ/1037946) | Verified |
| NETGEAR Block Sites steps and model scope | [NETGEAR](https://kb.netgear.com/24053/How-do-I-block-Internet-sites-on-my-NETGEAR-router-from-the-router-web-interface) | Verified |
| NETGEAR app blocking via History tab; models | [NETGEAR](https://kb.netgear.com/000062159/How-do-I-block-or-allow-access-to-a-website-with-NETGEAR-Smart-Parental-Controls) | Verified (Premium requirement not stated) |
| TP-Link Archer keyword blocking; private MAC caution | [TP-Link (VIGI mirror)](https://vigi.com/baltic/support/faq/1124) | Verified |
| Deco Blocked Websites; full domain names; troubleshooting steps | [TP-Link](https://www.tp-link.com/us/support/faq/2643) | Verified |
| Firefox ignores network signal when DoH is manually enabled | [Mozilla](https://support.mozilla.org/en-US/kb/configuring-networks-disable-dns-over-https/revision/289782) | Verified |
