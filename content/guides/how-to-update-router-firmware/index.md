---
title: "How to Update Your Router's Firmware: eero, Netgear, ASUS and TP-Link"
date: 2026-10-13
description: "Step-by-step firmware updates from each maker's own support pages, how to turn on automatic updates, and what to avoid during an update."
authors: ["Tehseen Arbab"]
topics: ["how-to-fixes", "security-privacy"]
tags: ["firmware-updates", "router-security", "eero", "netgear", "asus", "tp-link", "how-to"]
summary: "Firmware is the software inside your router, and updating it is how security fixes reach you. eero updates through its app, Netgear through the Nighthawk app or routerlogin.net, ASUS through its router app or asusrouter.com, and TP-Link through its Tether app or tplinkwifi.net. Netgear, ASUS and TP-Link warn not to power off or interrupt the router mid-update. Menu names vary by model, so confirm against your model's support page."
imageAlt: "Back of a black Wi-Fi router showing four numbered Ethernet ports, a blue WAN port and a WPS button"
imageCredit: "Photo: Syced / [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:ELECOM_WRC-300FEBK_WPS_WiFi_router.jpg), CC0"
takeaways:
  - "Firmware is the router's built-in software. Netgear says its updates improve performance, add features and enhance security."
  - "The easiest method on every brand covered here is the manufacturer's phone app. Netgear and ASUS both recommend their app first."
  - "Automatic updates exist on all four brands, but where the switch is, and whether it is on by default, varies by brand and model."
  - "Never power off or interrupt the router during an update. Netgear, ASUS and TP-Link all say so."
  - "A router can only be updated if the manufacturer still releases firmware for it. If yours has reached end of service, see our guide on support periods."
faq:
  - q: "What is router firmware?"
    a: "It is the software built into the router that runs its features and security. Netgear says firmware updates improve product performance, add features and enhance security."
  - q: "How often should I update my router?"
    a: "As soon as a security update is available, which is why automatic updates are worth turning on where your router offers them. None of the four makers covered here publishes a fixed schedule; eero says it releases updates on a rolling basis."
  - q: "Will updating my router erase my settings?"
    a: "Not necessarily, but ASUS recommends restoring factory defaults after a firmware update and then running its Quick Internet Setup again, and TP-Link recommends backing up your configuration or writing down changed settings first. Follow your maker's guidance for your model."
  - q: "Can I update over Wi-Fi?"
    a: "TP-Link says not to upgrade over a wireless connection unless the device has no Ethernet port, and Netgear's manual method starts with an Ethernet connection. Use a cable for manual updates when you can."
  - q: "What if my router has no update available?"
    a: "It may be current, or it may no longer be supported. Check the maker's support page for your exact model, and see our guide on how long routers get security updates."
  - q: "What if the update fails or the router won't start?"
    a: "Do not keep power cycling it. Follow the maker's recovery instructions for your model, or contact its support. We have not tested recovery procedures."
sources:
  - title: "How do eeroOS updates work?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/how-do-eeroos-updates-work"
  - title: "How do I check my eeroOS version?"
    publisher: "eero Support"
    url: "https://eero.com/support/articles/how-do-i-check-my-eeroos-version"
  - title: "How do I update the firmware on my NETGEAR router?"
    publisher: "NETGEAR Support"
    url: "https://kb.netgear.com/000058238/How-do-I-upgrade-firmware-using-the-Nighthawk-app"
    date: 2025-09-02
  - title: "How do I manually update the firmware on my NETGEAR router?"
    publisher: "NETGEAR Support"
    url: "https://kb.netgear.com/23960"
    date: 2025-07-07
  - title: "How do I update my router's firmware using the Check button?"
    publisher: "NETGEAR Support"
    url: "https://kb.netgear.com/000038662/How-do-I-update-my-router-s-firmware-using-the-check-button"
    date: 2025-07-07
  - title: "[Wireless Router] How to update the firmware of your router to the latest version? (WebGUI)"
    publisher: "ASUS Support"
    url: "https://www.asus.com/us/support/FAQ/1008000"
    date: 2026-02-23
  - title: "How to Update Firmware on TP-Link Wi-Fi Routers"
    publisher: "TP-Link Support (US)"
    url: "https://www.tp-link.com/us/support/faq/2139"
    date: 2026-04-23
---

Updating your router's firmware is the most direct way to get security fixes onto it, and on most routers it takes a few minutes. This guide gives the steps from eero's, Netgear's, ASUS's and TP-Link's own support pages, shows where to turn on automatic updates, and lists what each maker says not to do. Firmware is the software built into the router.

This is a how-to based on those support pages, which we checked on October 13, 2026. We have not run these updates ourselves, and menu names differ between models and firmware versions, so use your model's support page if your screen does not match.

## Before you start

1. **Confirm the router is still supported.** An update can only be installed if the maker still releases one. See [how long routers get security updates]({{< relref "/guides/how-long-do-routers-get-security-updates" >}}).
2. **Use the right file for the right model.** For manual updates, match the model and hardware version on the router's label. TP-Link warns that wrong firmware "may damage your device and void the warranty" and that firmware for the US and EU differ.
3. **Plan for a short outage.** eero says a software update can take 15 to 20 minutes, with about 90 seconds of downtime when its devices reboot. Netgear says its manual update takes about two minutes. Pick a time when no one is on a call or in a game.
4. **Note your settings.** TP-Link recommends backing up the configuration or writing down changed settings. ASUS recommends restoring factory defaults after an update, which erases custom settings, so note them first.
5. **Do not interrupt the update.** Netgear says not to close the browser, load a new page or turn off the router. ASUS and TP-Link also say not to turn the router off.

## eero

eero says updates are released on a rolling basis and reach customers' networks within a few weeks of a new version's public release, so yours may not update the day a version appears.

**Check and install manually:** open the eero app, tap **Settings** (bottom right), then **Software updates**. If an update is available the app says so; tap **Install now**. The eeros reboot, and your network goes briefly offline. Every eero you want to update must be powered on and online.

**Set a preferred time:** Settings, **Software updates**, **Preferred update time**, then pick a window (choose AM or PM). eero says that otherwise it can update automatically overnight. You can also turn on notifications under Settings, **Notifications**, for a 12-hour or 15-minute reminder before an update and a message when it finishes.

**Check the installed version:** tap the **Home** tab, tap the eero's name, then look under **Software updates**.

## Netgear (Nighthawk and Orbi)

**With the Nighthawk app (Netgear's easiest method):** connect your phone to the router's Wi-Fi, open the app, sign in if asked, enter the router's admin user name and password, tap your router, scroll to **CHECK FOR UPDATES**, and tap **UPDATE** if new firmware is available. Netgear says the admin password is the one you set when you set up the router, and that the default user name is "admin."

**With a web browser:** connect to the router's network and go to routerlogin.net, then sign in. Click **ADVANCED > Administration** (or **Settings > Administration**), then **Firmware Update** or **Router Update**. Click **Check**; if new firmware is available, click **Yes** or **Upgrade**. Netgear says the router updates and restarts and that the process can take a few minutes.

**Turn on automatic updates:** Netgear's support article says to go to routerlogin.net (Nighthawk) or orbilogin.net (Orbi), sign in, select **ADVANCED > Administration > Router Update**, scroll to **Router Auto Firmware Update**, select **Enable**, and click **Apply**. The same article says you can select **Disable** to turn it off. That article lists specific models, so if yours is not listed, check your model's page.

**Manual file update:** if you want a specific version, Netgear says to connect your computer by Ethernet, download the firmware for your model from Netgear Support, unzip it, then in **Administration** choose **Firmware Update** or **Router Update**, browse to the file ending in .img or .chk, and click **Upload**.

## ASUS

ASUS recommends using the ASUS Router app, and its support page also describes three web methods. Sign in at asusrouter.com.

- **Automatic:** go to **Administration > Firmware Upgrade**, enable **Auto Firmware Upgrade**, and set a time. ASUS recommends choosing a time when you are not using the network.
- **From the web interface:** a pop-up appears at the upper right if new firmware is available; click **Update now**, which opens **Administration > System**, then **Firmware Upgrade**.
- **Manual file:** download the firmware for your model from ASUS, unzip it, go to **Administration > Firmware Upgrade**, click **Upload**, and choose the file. ASUS recommends this if you have not updated in a while or the router cannot reach ASUS's servers.

ASUS also says that when a version contains important fixes, it can become a "required" version that the router upgrades to automatically. After updating, ASUS recommends restoring factory defaults and running its Quick Internet Setup again. That wipes your custom settings, which is why we suggest noting them first.

## TP-Link

TP-Link's steps depend on whether your router supports TP-Link Cloud service, which its page says you can check on its Cloud Compatibility list.

- **Cloud-supported routers:** TP-Link says to click the **Update** icon in the upper right corner of the web page at tplinkwifi.net, or use the Tether app under **More > System > Firmware Update**. No file download is needed.
- **Routers without Cloud support:** download the firmware for your hardware version from TP-Link's site for your country, extract the ZIP file, sign in at tplinkwifi.net, go to **Advanced > System > Firmware Upgrade**, browse to the .bin file, and click **Upgrade**. TP-Link says not to upgrade over Wi-Fi unless the device has no Ethernet port.

We did not find an automatic-update switch described on the TP-Link page we checked, so we cannot say how to turn one on for a given model. Use the Cloud update icon or Tether where available.

## Other brands and provider gateways

These steps cover only the four brands named. If your router is a gateway supplied by your internet provider, the provider may manage its updates, so ask the provider before trying to change it. See our guide on [using your own router versus provider equipment]({{< relref "/guides/buy-your-own-router-vs-isp-equipment" >}}).

## After the update

- Confirm the router came back online and that your Wi-Fi network name and password are as you expect.
- Check the firmware version in the app or admin page to confirm it changed.
- If you restored defaults, re-enter your settings. Our [router hardening checklist]({{< relref "/guides/router-hardening-checklist" >}}) lists the settings worth reviewing, and [WPA2 vs. WPA3]({{< relref "/guides/wpa2-vs-wpa3" >}}) explains the security mode choice.
- Turn on automatic updates where your router offers them, so you do not have to remember.

## Fact-check notes

| Important claim | Source | Verification |
|---|---|---|
| eero updates roll out over a few weeks; app path Settings, Software updates; Install now; reboot and brief outage; preferred update time; notifications; 15 to 20 minute updates with about 90 seconds of downtime | [eero Support, checked October 13, 2026](https://eero.com/support/articles/how-do-eeroos-updates-work) and [version check page](https://eero.com/support/articles/how-do-i-check-my-eeroos-version) | Verified |
| Netgear app steps; browser steps via routerlogin.net, ADVANCED > Administration, Check; do not interrupt | [NETGEAR Support, last updated September 2, 2025](https://kb.netgear.com/000058238/How-do-I-upgrade-firmware-using-the-Nighthawk-app) | Verified; the page applies to listed models |
| Netgear Router Auto Firmware Update setting under ADVANCED > Administration > Router Update; Enable or Disable, Apply | [NETGEAR Support, last updated July 7, 2025](https://kb.netgear.com/000038662/How-do-I-update-my-router-s-firmware-using-the-check-button) | Verified; applies to the models listed on that page |
| Netgear manual update: Ethernet, download, .img or .chk file, about two minutes | [NETGEAR Support, last updated July 7, 2025](https://kb.netgear.com/23960) | Verified |
| ASUS app recommended; Auto Firmware Upgrade under Administration; update pop-up; manual update; required firmware versions; factory reset recommended after updates | [ASUS Support, last updated February 23, 2026](https://www.asus.com/us/support/FAQ/1008000) | Verified; example screens use an RT-AX88U |
| TP-Link Cloud routers: Update icon or Tether; non-Cloud routers: Advanced > System > Firmware Upgrade, .bin file; hardware version, region and no-power-off warnings; avoid updating over Wi-Fi | [TP-Link Support (US), last updated April 23, 2026](https://www.tp-link.com/us/support/faq/2139) | Verified |
| No TP-Link automatic-update switch described | Absence on the TP-Link page above | Qualified: absence on the page we checked, not a statement from TP-Link |
| Firmware updates improve performance, add features and enhance security | [NETGEAR Support](https://kb.netgear.com/000058238/How-do-I-upgrade-firmware-using-the-Nighthawk-app) | Verified (Netgear's statement) |

## Bottom line

Use your maker's app if it has one, turn on automatic updates where your router offers them, and never interrupt an update once it starts. If no update ever appears, check whether your model is still supported, because that is the problem an update cannot fix.
