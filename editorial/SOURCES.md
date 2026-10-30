# Source playbook

Read before research; update at the end of every daily run. One line per source: domain or page | works / fails (how) | workaround | date checked. Keep under ~80 lines.

## Works (fetch via WebSearch result, no approval)
- rfc-editor.org (RFC .txt/.html) | works | none needed | 2026-10-25
- blog.apnic.net | works | none | 2026-10-25
- tailscale.com/docs (.md pages) | works | none | 2026-10-25
- kb.netgear.com | works; shows "Last Updated" date | none | 2026-10-25
- asus.com/us/support/FAQ/<id> (and /support/FAQ/<id>, /ca-en techspec) | works; shows "Last Update"; US techspec rarely returned | cite Canadian spec page, note it | 2026-10-30
- vigi.com/<cc>/support/faq and omadanetworks.com/<cc>/support/faq (TP-Link KB mirrors) | works; shows "Last updated" | use when tp-link.com FAQ doesn't come back in search | 2026-10-25
- api.starlink.com/public-files/*.pdf (Starlink setup guides) | works | none | 2026-10-25
- dishytech.com | works; third-party Starlink reporting | cite as Qualified | 2026-10-25
- telecompetitor.com | works; reports Ookla figures | none | 2026-10-25
- support.google.com/wifi and /googlenest, eero.com/support/articles/* (incl. MAC randomization, bridge mode, product comparison), eero.com/shop (US prices), learn.microsoft.com, pulse.internetsociety.org, xfinity.com/support | works | none | 2026-10-24
- images.unsplash.com (curl download) | works | append ?fm=jpg&q=85&w=2400&fit=max | 2026-10-25
- unsplash.com/s/photos/<term>, /collections/<id>, /photos/<slug> | work ONLY when the URL came back in a WebSearch; photo pages return images.unsplash.com src | search "unsplash <term> photos" first | 2026-10-25
- t-mobile.com/support/home-internet/* and t-mobile.com/home-internet/policies/* | works; no last-updated date shown | none | 2026-10-26
- verizon.com/support/knowledge-base-* and verizon.com/support/broadband-services | works; KB pages don't list covered models | cite model scope as Qualified | 2026-10-26
- support.google.com/googlehome (port forwarding, DHCP reservation) | works | none | 2026-10-26
- tp-link.com/ca/home-networking/deco/* | works for specs and working modes | note it's the Canada page | 2026-10-26
- xfinity.com/support/internet/list-of-approved-cable-modems and /support/articles/upgraded-areas-leased-equipment-required-for-upload-speeds | works; modified dates in metadata; no model lists | use My Device Info wording, don't claim model certification | 2026-10-27
- surfboard.com/products/cable-modems/<model>/ (US pages) | works; specs, warranty, ISP qualification text | none | 2026-10-27
- prnewswire.com news releases | works; launch MSRP and dates | MSRP is not a current price | 2026-10-27
- support.apple.com/<cc>/102509 (private Wi-Fi addresses) and support.apple.com/guide/platform-support/* | works; shows Published Date | none | 2026-10-28
- source.android.com/docs/core/connect/* | works; shows last-updated date | none | 2026-10-28
- support.microsoft.com/windows/<guid> | works | none | 2026-10-28
- support.linksys.com/kb/article/<id> | works; some articles render in Dutch (e.g. 1524) | prefer articles that come back in English | 2026-10-28
- tp-link.com/en/products/details/<model>.html and tp-link.com/us/support/faq/<id> | works; global page doesn't state US hardware version | note it | 2026-10-28
- netgear.com/home/wifi/routers/<model>/ (US) | works; price only in metadata; shows stock status | don't cite metadata price | 2026-10-28

- learn.microsoft.com/<locale>/troubleshoot/windows-server/networking/change-ip-address-network-adapter | works; English body on ar-sa locale; old Control Panel steps | cite as Qualified | 2026-10-29
- doctorengenius.engeniustech.com/en/articles/* | works; dated vendor FAQ | cite as Qualified | 2026-10-29
- netgear.com/home/wifi/routers/rs100 (no trailing slash) | works; US RS100 page only came back with this exact search phrasing; no per-band rates | search "netgear.com home wifi routers rs100 Nighthawk WiFi 7 Router RS100 3.6Gbps" | 2026-10-29
- businesswire.com/news/home/* | works; text has no date (date only in URL) | note date as inferred | 2026-10-29
- notebookcheck.net | works; launch prices with dates | MSRP is not a current price | 2026-10-29
- bhphotovideo.com RS100 page | works; price + stock | none | 2026-10-29
- adorama.com product pages | works; price, stock, per-band specs | retailer specs = Qualified | 2026-10-29
- pcrichard.com product pages | works; price but "enter email to reveal" and no stock | note it | 2026-10-29
- unsplash.com/s/photos/wifi-router, /s/photos/router, /id/s/foto/router | works from WebSearch; nearly all router photos already used | search non-router subjects (printer, desk, cables) | 2026-10-29
- rfc-editor.org/rfc/rfc1122.html | works; long page, use offset=100000 for sec 3.3 | none | 2026-10-30
- eero.com/blog/articles/* and support.eero.com/hc/articles/115002904283 (eero Plus price) and prod.eero.com/eero-plus | works | none | 2026-10-30
- eero.com/support/articles/what-are-the-advanced-networking-settings | works only when it came back in search (support.eero.com/hc 302s to it) | search the eero.com title | 2026-10-30
- omadanetworks.com/en/support/faq/3007 (HomeShield prices, US) and /faq/2996 (HomeShield features) | works; dated | none | 2026-10-30
- asus.com/uk/Content/AiProtection | works; "subscription-free" claim; no US equivalent found | cite as Qualified (UK) | 2026-10-30
- support.google.com/googlenest/answer/7571856 (custom LAN IP) | works | none | 2026-10-30
- support.ksu.edu (Windows ipconfig) | works; university IT | cite as Qualified | 2026-10-30
- adorama.com/asrtbe58u.html | works; price + stock | none | 2026-10-30

## Fails (don't fetch)
- starlink.com/support/article/* | fails: renders empty (JavaScript) | use reseller copies (support.satellitephonestore.com, cite Qualified) or Starlink PDFs on api.starlink.com | 2026-10-25
- netgear.com/<cc>/hub/* | fails: redirects to auhub.netgear.com, which asks for approval | use kb.netgear.com | 2026-10-25
- unsplash.com search pages typed from the prompt (router, internet-router) | fails: approval request times out | WebSearch for the page first | 2026-10-25
- gsc-wizard connector | fails: payment_required | not used by daily runs | 2026-10-25
- curl to wifiweekly.com live pages | blocked in run on 2026-10-25 | use the PR's Cloudflare Pages check run + one WebFetch per URL | 2026-10-25
- bestbuy.com product pages | renders without visible price (metadata only) | leave prices out | 2026-10-27
- community.surfboard.com threads | fail: 302 redirect to surfboard.com | don't rely on forum claims | 2026-10-27
- URLs carried over from IDEAS.md without a fresh search result (support.google.com/googlehome/answer/6274660, kb.netgear.com/25722) | fail: PROVENANCE_REQUIRED approval timeout | always re-search so the URL comes back in today's results | 2026-10-28
- rtings.com router reviews | renders metadata only (no results) | don't rely on RTINGS for measurements | 2026-10-28
- wi-fi.org/system/files/*.pdf | fails: redirects to login | use FCC or internal band guide | 2026-10-28

- bhphotovideo.com RS200 pages (1861250-REG) | fail: client_error | use another retailer or leave price out | 2026-10-29
- electronicexpress.com product pages | render without price or stock | leave price out | 2026-10-29
- community.netgear.com/kb/nighthawk-firmware-releases/* | fail: client_error | use kb.netgear.com firmware pages | 2026-10-29
- learn.microsoft.com/en-us/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting (also via support.microsoft.com/kb/164015 redirect) | fails: PROVENANCE_REQUIRED approval timeout | use RFC 1122/4632 | 2026-10-30
- technet.microsoft.com ipconfig pages | redirect to learn.microsoft.com previous-versions (not fetched) | use support.ksu.edu | 2026-10-30
- unsplash.com/photos/a-young-boy-...-9LqVKYoG75w | Unsplash+ (premium) | check license before download | 2026-10-30

## No official answer found
- T-Mobile / Verizon 5G Home Internet: CGNAT, public IP, IPv6 | no official page found | don't make carrier-specific CGNAT claims | 2026-10-26
- T-Mobile bridge mode and port forwarding | official answer exists: t-mobile.com/support/home-internet/connect says gateways can't do either | use that page | 2026-10-26
- Verizon IP Passthrough | official KB 301824 covers "Verizon Internet Gateway" without listing models | cite as Qualified | 2026-10-26
- eero / Google Nest Wifi Starlink setup | no official article found | describe generic Ethernet setup only | 2026-10-25
- Xfinity: which retail modems are certified for upgraded (mid-split) upload by address | only via My Device Info (sign-in/address) | tell readers to check My Device Info | 2026-10-27
- NETGEAR RS-series MLO support | not stated on US product pages or RS100 firmware note | describe as "not mentioned" | 2026-10-29
- Cox residential certified modems list | page exists (cox.com/residential/support/cox-certified-cable-modems.html per cox.com/llms.txt) but never returned in WebSearch | retry search with new phrasing; otherwise skip Cox | 2026-10-28
- Spectrum approved/compliant modem list | spectrum.net page never returned in WebSearch (only Hitron/third-party) | Spectrum modem topic dropped | 2026-10-30
- AT&T Fiber own router / IP Passthrough | no att.com support page returned (forums only) | topic dropped | 2026-10-30
- NETGEAR Smart Parental Controls US price | KB says price shown in app only | don't quote a price | 2026-10-30
