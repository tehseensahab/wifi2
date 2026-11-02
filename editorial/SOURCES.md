# Source playbook

Read before research; update at the end of every daily run. One line per source: domain or page | works / fails (how) | workaround | date checked. Keep under ~80 lines.

## Works (fetch via WebSearch result, no approval)
- rfc-editor.org (RFCs), blog.apnic.net, tailscale.com/docs (.md pages) | works | none | 2026-10-25
- kb.netgear.com (incl. 24053 Block Sites, 000062159, 000064414 Windows 6 GHz) | works; shows "Last Updated" date | none | 2026-11-02
- asus.com/us/support/FAQ/<id> (and /support/FAQ/<id>, /ca-en techspec) | works; shows "Last Update"; US techspec rarely returned | cite Canadian spec page, note it | 2026-10-30
- vigi.com/<cc>/support/faq and omadanetworks.com/<cc>/support/faq (TP-Link KB mirrors) | works; shows "Last updated" | use when tp-link.com FAQ doesn't come back in search | 2026-10-25
- api.starlink.com/public-files/*.pdf (Starlink setup guides) | works | none | 2026-10-25
- dishytech.com (third-party Starlink, cite Qualified), telecompetitor.com (Ookla figures) | works | none | 2026-10-25
- support.google.com/wifi and /googlenest, eero.com/support/articles/* (incl. MAC randomization, bridge mode, product comparison), eero.com/shop (US prices), learn.microsoft.com, pulse.internetsociety.org, xfinity.com/support | works | none | 2026-10-24
- images.unsplash.com (curl download) | works | append ?fm=jpg&q=85&w=2400&fit=max | 2026-10-25
- unsplash.com/s/photos/<term>, /collections/<id>, /photos/<slug> | work ONLY when the URL came back in a WebSearch; photo pages return images.unsplash.com src | search "unsplash <term> photos" first | 2026-10-25
- t-mobile.com/support/home-internet/* and t-mobile.com/home-internet/policies/* | works; no last-updated date shown | none | 2026-10-26
- verizon.com/support/knowledge-base-* and verizon.com/support/broadband-services | works; KB pages don't list covered models | cite model scope as Qualified | 2026-10-26
- support.google.com/googlehome (port forwarding, DHCP reservation) and /googlenest/answer/7571856 (custom LAN IP) | works | none | 2026-10-30
- tp-link.com/ca/home-networking/deco/* | works for specs and working modes | note it's the Canada page | 2026-10-26
- xfinity.com/support/internet/list-of-approved-cable-modems and /support/articles/upgraded-areas-leased-equipment-required-for-upload-speeds | works; modified dates in metadata; no model lists | use My Device Info wording, don't claim model certification | 2026-10-27
- surfboard.com/products/cable-modems/<model>/ (US pages) | works; specs, warranty, ISP qualification text | none | 2026-10-27
- support.apple.com/<cc>/102509 (private Wi-Fi addresses) and support.apple.com/guide/platform-support/* | works; shows Published Date | none | 2026-10-28
- source.android.com/docs/core/connect/* | works; shows last-updated date | none | 2026-10-28
- support.microsoft.com/windows/<guid> | works | none | 2026-10-28
- support.linksys.com/kb/article/<id> | works; some articles render in Dutch (e.g. 1524) | prefer articles that come back in English | 2026-10-28
- tp-link.com/en/products/details/<model>.html and tp-link.com/us/support/faq/<id> | works; global page doesn't state US hardware version | note it | 2026-10-28
- netgear.com/home/wifi/routers/<model>/ (US) | works; price only in metadata; shows stock status | don't cite metadata price | 2026-10-28
- businesswire.com (no date in text; date only in URL), notebookcheck.net, prnewswire.com (launch prices), adorama.com (price, stock, per-band specs) | works | MSRP is not a current price; retailer specs = Qualified | 2026-10-29
- unsplash.com/s/photos/wifi-router, /s/photos/router, /id/s/foto/router | works from WebSearch; nearly all router photos already used | search non-router subjects (printer, desk, cables) | 2026-10-29
- eero.com/support/articles/what-are-the-advanced-networking-settings | works only when it came back in search (support.eero.com/hc 302s to it) | search the eero.com title | 2026-10-30
- omadanetworks.com/en/support/faq/3007 (HomeShield prices, US) and /faq/2996 (HomeShield features) | works; dated | none | 2026-10-30
- asus.com/uk/Content/AiProtection | works; "subscription-free" claim; no US equivalent found | cite as Qualified (UK) | 2026-10-30
- wi-fi.org/news-events/newsroom/* | works; dated press releases | none | 2026-10-31
- fcc.gov/document/* (6 GHz order: title only) + techblog.comsoc.org (dated IEEE ComSoc reporting, secondary) | works | pair them for dates | 2026-10-31
- arubanetworking.hpe.com/techdocs/* (Wi-Fi 7 features) | works; undated | none | 2026-10-31
- tp-link.com/us/blog/<id>/ and netgear.com/hub/network/* | works; dated | none | 2026-10-31
- eero.com/eero-plus, eero.com/support/articles/* (eero-7, what-is-eero-plus, eero-signal, Guardian VPN, 1Password), eero.com/shop/eero-signal/buy | works; US prices on shop/plus pages; no page dates | links listed inside eero.com/support/sections/* must be re-searched before fetching | 2026-10-31
- unsplash.com/s/photos/online-privacy, /wifi-network, /signal, /website-security | works from WebSearch; /signal has cell towers, /website-security has padlock-on-keyboard shots | none | 2026-11-01
- eero.com/support/articles/what-is-block-and-allow-sites, /what-is-eero-hotspot-backup, /how-do-i-troubleshoot-eero-signal; eero.com/shop/eero-signal (plan prices only, no device prices on 2026-11-01); eero.com/legal/network-management-statement (Signal speed/data labels; body text has typos, use Broadband Facts labels) | works | none | 2026-11-01
- asus.com/us/support/FAQ/1037946 (URL Filter) and vigi.com/baltic/support/faq/1124 (TP-Link Archer parental controls), tp-link.com/us/support/faq/2643 (Deco troubleshooting) | works; dated | tp-link.com/support/faq/1008 is modem routers only | 2026-11-01
- support.mozilla.org/en-US/kb/configuring-networks-disable-dns-over-https/revision/* | works | none | 2026-11-01
- press.aboutamazon.com/devices/2025/9/* (eero Signal launch), 3gpp.org/news-events/partner-news/redcap-gsa-article01 (RedCap rates) | works | launch prices are not current prices | 2026-11-01
- static.gl-inet.com datasheet PDFs and store-us.gl-inet.com product pages | works; US price shown, no stock status | none | 2026-11-02
- help.ui.com/hc/en-us/articles/360052548713 (UniFi WAN failover) and store.ui.com/us/en/products/* | works; store shows price, surcharge and stock | none | 2026-11-02
- memoryexpress.com product pages | works; retailer specs | cite as Qualified | 2026-11-02
- support.apple.com/102285 (Wi-Fi 6E device list, published 2026-10-27), intel.com/content/www/us/en/support/articles/000059385 and /000087538, tp-link.com/uk/support/faq/3092, wi-fi.org/node/37285 | works; dated | none | 2026-11-02
- support.microsoft.com/topic/26177a28-38ed-1a8e-7eca-66f24dc63f09 (netsh check, Network band path) | works | none | 2026-11-02
- bhphotovideo.com RT-BE58U (1859883-REG) | works; band list, stock, no price | leave price out | 2026-11-02
- unsplash.com/s/photos/internet-cable, /internet-cables, /disconnect | works from WebSearch; most cable/router shots already used; many Unsplash+ results | check COVER-IMAGES.md before downloading | 2026-11-02

## Fails (don't fetch)
- starlink.com/support/article/* | fails: renders empty (JavaScript) | use reseller copies (support.satellitephonestore.com, cite Qualified) or Starlink PDFs on api.starlink.com | 2026-10-25
- netgear.com/<cc>/hub/* | fails: redirects to auhub.netgear.com, which asks for approval | use kb.netgear.com, or www.netgear.com/hub/network/* (no country code), which works | 2026-10-31
- unsplash.com search pages typed from the prompt (router, internet-router) | fails: approval request times out | WebSearch for the page first | 2026-10-25
- gsc-wizard connector | fails: payment_required | not used by daily runs | 2026-10-25
- curl to wifiweekly.com live pages | blocked in run on 2026-10-25 | use the PR's Cloudflare Pages check run + one WebFetch per URL | 2026-10-25
- bestbuy.com product pages | renders without visible price (metadata only) | leave prices out | 2026-10-27
- community.surfboard.com threads | fail: 302 redirect to surfboard.com | don't rely on forum claims | 2026-10-27
- URLs carried over from IDEAS.md without a fresh search result (support.google.com/googlehome/answer/6274660, kb.netgear.com/25722) | fail: PROVENANCE_REQUIRED approval timeout | always re-search so the URL comes back in today's results | 2026-10-28
- rtings.com router reviews | renders metadata only (no results) | don't rely on RTINGS for measurements | 2026-10-28
- wi-fi.org/system/files/*.pdf | fails: redirects to login | use FCC or internal band guide | 2026-10-28
- bhphotovideo.com RS200 pages (1861250-REG) | fail: client_error | use another retailer or leave price out | 2026-10-29
- community.netgear.com/kb/nighthawk-firmware-releases/* | fail: client_error | use kb.netgear.com firmware pages | 2026-10-29
- learn.microsoft.com/en-us/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting (also via support.microsoft.com/kb/164015 redirect) | fails: PROVENANCE_REQUIRED approval timeout | use RFC 1122/4632 | 2026-10-30
- blog.eero.com/* | 302 redirect to eero.com/blog/articles/* | search the eero.com/blog/articles title | 2026-10-31
- eero.com/shop/eero-signal/buy | fails 2026-11-01: PROVENANCE_REQUIRED approval timeout (worked 2026-10-31) | use eero.com/shop/eero-signal for plan prices; leave device prices out | 2026-11-01
- unsplash.com/photos/...-8_u0uDD8qEM (Wi-Fi 7 USB adapter) | looks like a 3D render, not a photo | don't use | 2026-10-31
- techspecs.ui.com/* | fails: robots_disallowed | use store.ui.com product page + help.ui.com + a retailer listing | 2026-11-02
- store.google.com/product/pixel_*_specs | fails: returns current Pixel lineup, not the requested model | use carrier/maker spec PDFs or skip Pixel claims | 2026-11-02

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
- eero Signal device prices at a retailer | Amazon listing never returned in search | leave prices out | 2026-11-01
- Android: how to check 6 GHz support in Settings | no official Google/Samsung page returned | tell readers to check the model spec sheet | 2026-11-02
