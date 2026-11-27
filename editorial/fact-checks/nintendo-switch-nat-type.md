# Fact-check record: nintendo-switch-nat-type

Article: content/guides/nintendo-switch-nat-type/index.md
Byline: Tehseen Arbab
Date: 2026-11-27
Checker: independent subagent (did not write the draft); 2 re-fetches (Nintendo Americas 22541, Nintendo AU NAT troubleshooting). No approval errors.

## Result
- Verified (16): A-to-F scale and F wording; A/B/C/D definitions; test path, fields, "Success"; no Type E described; other player's NAT matters; 3 Mbps check; Wi-Fi (10-15 ft) and wired steps incl. USB LAN adapter; power-cycle method incl. backup battery; IPv6 path; D/F steps (ISP, router maker); Switch 2 UDP 1024-65535, static IP, security caveat; no UPnP on Nintendo pages.
- Qualified and fixed (8): Sources table row attribution (D/F steps moved to 22541 row); static-IP step limited to the Switch 2 page; DMZ attributed to Nintendo Australia; Switch 1 range attributed to Nintendo UK; D/F cause sentence reworded as analysis; Xbox/PlayStation label sets attributed per platform; CGNAT kept as labeled background.
- Not verified, rewritten (2): power cycling is not in Nintendo's D/F path (takeaway and intro now say A, B and C only); "both handle NAT" quote is from Nintendo Australia, not the US NAT page.

## Research log

| # | Claim | Verbatim quote | Source URL | Date | Geo / qualification |
|---|---|---|---|---|---|
| S1 | NAT type is a result of the Switch connection test; scale A (best) to F | "This will range from A (best for peer-to-peer communication) to F (unable to complete peer-to-peer communication)." | https://en-americas-support.nintendo.com/app/answers/detail/a_id/22462/~/how-to-use-the-internet-connection-test | undated | US; same text on 22541 |
| S2 | Test path: HOME Menu > System Settings > Internet > Test Connection; same for Switch 2 and Switch | Path: HOME Menu, "System Settings" icon, "Internet", "Test Connection." Test "will begin immediately after selecting this option." | same as S1 | undated | US; covers Switch 2 and Switch |
| S3 | Test fields | Connection Name, SSID, Internet Connection, Global IP Address, NAT Type, Download Speed, Upload Speed | same as S1 | undated | US |
| S4 | "Success" meaning | "If **Success** is displayed, it indicates the console was able to connect with Nintendo's services." | same as S1 | undated | US |
| S5 | Type A preferred | "NAT type A is preferred and generally indicates that your network environment works well for connecting with other players." | https://en-americas-support.nintendo.com/app/answers/detail/a_id/22541/ | undated | US; Switch 2 and Switch |
| S6 | Type B compatible with most | B is "compatible with most other NAT types as well." | same as S5 | undated | US |
| S7 | Type C difficulty with more restrictive | "Users with NAT type C network environments may have difficulty connecting to some users with more restrictive NAT types." | same as S5 | undated | US |
| S8 | Type D only connects with A | "Generally, players with NAT Type D can only connect to players with NAT Type A." | same as S5 | undated | US |
| S9 | Type F | NAT F is "not optimal for peer-to-peer connections"; page says it generally means network restricting communication and makes connecting with other players impossible (paraphrase by fetcher; exact "impossible" wording not quoted) | same as S5 | undated | US; QUALIFIED: use the S1 quote "unable to complete peer-to-peer communication" as the verbatim anchor |
| S10 | A/B/C: latency may cause matchmaking timeouts; check download >= 3 Mbps | fetcher: with A or B (and C), latency may cause matchmaking to time out; "Check whether download speed is 3Mbps or higher" (paraphrase of decision tree) | same as S5 | undated | US; QUALIFIED paraphrase |
| S11 | Wireless steps for A/B/C: turn off IPv6, move within 10-15 ft of router, move metal/electronics away, power cycle | fetcher summary of decision tree: "Move the console within 10 to 15 feet of the router" | same as S5 | undated | US; QUALIFIED paraphrase |
| S12 | Wired steps for A/B/C: turn off IPv6, power cycle, connect directly to modem, restart modem, different cable | fetcher summary | same as S5 | undated | US; QUALIFIED |
| S13 | D and F steps: turn off IPv6, then contact ISP/network admin and router maker (firmware update or factory reset) | fetcher summary | same as S5 | undated | US; QUALIFIED |
| S14 | Power cycle: unplug modem and router, wait 30 s, modem first then router; remove modem backup battery | fetcher summary | same as S5 | undated | US |
| S15 | IPv6 off path | System Settings > Internet > Internet Settings > select your network name > Change Settings > IPv6 Connection off | https://en-americas-support.nintendo.com/app/answers/detail/a_id/22455/p/989/c/875 | undated | US; Switch 2 and Switch |
| S16 | Other player's NAT type matters | "Both your NAT type and the NAT type any player you are attempting to connect with can affect the connection process." | same as S15 | undated | US |
| S17 | Strict NAT may block online activities | "Networks with a more strict NAT type may prevent you from performing some online activities, such as connecting with other players online." | same as S15 | undated | US |
| S18 | 22455 does not mention port forwarding, UPnP or DMZ | (absence) | same as S15 | undated | US |
| S19 | Switch 2 port forwarding range and protocol | "For the Nintendo Switch 2 console, this is port 1024 through 65535." "Set the protocol as UDP." | https://en-americas-support.nintendo.com/app/answers/detail/a_id/68445 | undated | US |
| S20 | Switch 2 static IP first | "Perform the following steps to assign a static IP address to your Nintendo Switch 2 console." | same as S19 | undated | US; example adds 20 to last octet |
| S21 | Security caveat | "it is up to each consumer to determine what security needs they have for their own networks" | same as S19 (also UK and AU pages) | undated | US |
| S22 | Router maker for specific instructions | "If you need specific instructions for your router, please contact the manufacturer of the router for further assistance." | same as S19 | undated | US |
| S23 | Original Switch port forwarding range | "For the Nintendo Switch console, this is port 1024 through 65535." "Set the protocol as UDP." | https://www.nintendo.co.uk/Support/Nintendo-Switch/How-to-Set-Up-a-Router-s-Port-Forwarding-for-a-Nintendo-Switch-Console-1498000.html | undated | UK page (US Switch 1 version not returned in search) |
| S24 | DMZ page: static IP first; generic router step | "Perform the following steps to assign a static IP address to your Nintendo Switch console:"; "Locate the DMZ or "Demilitarized Zone" setting." | https://nintendo.com/au/support/articles/how-to-place-a-nintendo-switch-console-into-a-routers-dmz | undated | Australia page; Switch 2 not mentioned |
| S25 | DMZ bypasses router firewall | "Setting up a DMZ will allow the Nintendo Switch system to communicate directly to the internet" ... "and bypass the network firewall features of your router" | https://nintendo.com/au/support/articles/troubleshooting-issues-related-to-nat | undated | Australia page |
| S26 | Nintendo pages fetched don't mention UPnP | (absence on 22455, 22541, 68445, UK 1498000, AU NAT/DMZ) | as above | | |
