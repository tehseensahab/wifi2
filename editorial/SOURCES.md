# Source playbook

Read before research; update at the end of every daily run. One line per source: domain or page | works / fails (how) | workaround | date checked. Keep under ~80 lines.

## Works (fetch via WebSearch result, no approval)
- rfc-editor.org (RFCs), blog.apnic.net, tailscale.com/docs (.md pages) | works | none | 2026-10-25
- kb.netgear.com/<id> (24053 Block Sites, 000062159, 000064414/000064415/000064272 6 GHz, 9665 reset, 000061793 power cycle, 000038536 modem reset) | works; Last Updated shown (most 07/07/2025) | none | 2026-11-04
- asus.com/us/support/FAQ/<id> (incl. 1000925 reset, 1044308 AiMesh brands, 1015009 AP mode, 1037946) and /ca-en techspec | works; shows Last Update; US techspec rarely returned | cite Canadian spec page, note it | 2026-11-05
- api.starlink.com/public-files/*.pdf (Starlink setup guides) | works | none | 2026-10-25
- t-mobile.com/support/home-internet/* and t-mobile.com/home-internet/policies/* | works; no last-updated date shown | none | 2026-10-26
- verizon.com/support/knowledge-base-* and verizon.com/support/broadband-services | works; KB pages don't list covered models | cite model scope as Qualified | 2026-10-26
- support.google.com/googlehome (port forwarding, DHCP reservation) and /googlenest/answer/7571856 (custom LAN IP) | works | none | 2026-10-30
- xfinity.com/support/internet/list-of-approved-cable-modems and /support/articles/upgraded-areas-leased-equipment-required-for-upload-speeds | works; modified dates in metadata; no model lists | use My Device Info wording, don't claim model certification | 2026-10-27
- surfboard.com/products/cable-modems/<model>/ (US pages) | works; specs, warranty, ISP qualification text | none | 2026-10-27
- source.android.com/docs/core/connect/* | works; shows last-updated date | none | 2026-10-28
- support.linksys.com/kb/article/<id> | works; some articles render in Dutch (e.g. 1524) | prefer articles that come back in English | 2026-10-28
- netgear.com/home/wifi/routers/<model>/ (US) | works; price only in metadata; shows stock status | don't cite metadata price | 2026-10-28
- businesswire.com (no date in text; date only in URL), notebookcheck.net, prnewswire.com (launch prices), adorama.com (price, stock, per-band specs) | works | MSRP is not a current price; retailer specs = Qualified | 2026-10-29
- asus.com/uk/Content/AiProtection | works; "subscription-free" claim; no US equivalent found | cite as Qualified (UK) | 2026-10-30
- wi-fi.org/news-events/newsroom/* | works; dated press releases | none | 2026-10-31
- fcc.gov/document/* (6 GHz order: title only) + techblog.comsoc.org (dated IEEE ComSoc reporting, secondary) | works | pair them for dates | 2026-10-31
- arubanetworking.hpe.com/techdocs/* (Wi-Fi 7 features) | works; undated | none | 2026-10-31
- support.mozilla.org/en-US/kb/configuring-networks-disable-dns-over-https/revision/* | works | none | 2026-11-01
- press.aboutamazon.com/devices/2025/9/* (eero Signal launch), 3gpp.org/news-events/partner-news/redcap-gsa-article01 (RedCap rates) | works | launch prices are not current prices | 2026-11-01
- static.gl-inet.com datasheet PDFs and store-us.gl-inet.com product pages | works; US price shown, no stock status | none | 2026-11-02
- help.ui.com/hc/en-us/articles/360052548713 (UniFi WAN failover) and store.ui.com/us/en/products/* | works; store shows price, surcharge and stock | none | 2026-11-02
- memoryexpress.com product pages | works; retailer specs | cite as Qualified | 2026-11-02
- bhphotovideo.com RT-BE58U (1859883-REG) | works; band list, stock, no price | leave price out | 2026-11-02
- dlink.com/en/support/faq/aquilaproai/* (Wi-Fi 7 6 GHz FAQ) | works; undated; fetch summary paraphrased a quote (exact: "the SSID security must use WPA3 through all bands") | ask WebFetch for exact sentence | 2026-11-03
- community.tp-link.com/us/smart-home/kb/detail/412544 (official KB on community site) | works; dated 2023 | none | 2026-11-03
- APC/CyberPower UPS: mouser.com/datasheet/*, images.salsify.com APC brochure, cdn.blueally.com/apcguard/datasheets/*, cyberpowersystems.com/product/ups/* (MSRP only), apcguard.com/<model>.asp (shows discontinued), bhphotovideo.com BE600M1 (price+stock) | works | none | 2026-11-03
- xfinity.com/support/articles/power-outages-and-digital-voice-service, govinfo.gov/link/fr/80/62485 (FCC 2015 backup power order; 115k chars, use offset) | works; dated | none | 2026-11-03
- images.unsplash.com (curl, append ?fm=jpg&q=85&w=2400&fit=max); unsplash.com/s/photos/<term>, /trends/<term> and /photos/<slug> work ONLY when returned by WebSearch; most router/cable/AP shots already used, many Unsplash+, some 'photos' are 3D renders (e.g. Wi-Fi 7 USB adapter Dk6ukIRBrWE) | check COVER-IMAGES.md; try PC, concept (puzzle), or non-router subjects | 2026-11-05
- eero.com/support/articles/* (Wi-Fi 6E, WPA3, MAC randomization, bridge mode, eero Plus, Signal, Hotspot Backup, block sites, advanced settings), eero.com/eero-plus, eero.com/shop (US prices, no page dates), eero.com/legal/network-management-statement; support.google.com/wifi, /googlenest, /googlehome | works | links inside eero.com/support/sections/* must be re-searched; support.eero.com/hc 302s to eero.com | 2026-11-03
- support.apple.com/102285 (Wi-Fi 6E list, 2026-10-27), /102766 (router settings, 2026-07-14), /102509 (private address), support.apple.com/guide/platform-support/* and /guide/deployment/* | works; Published Date shown | none | 2026-11-03
- support.microsoft.com/windows/<guid>, /topic/26177a28-38ed-1a8e-7eca-66f24dc63f09 (netsh, Network band); learn.microsoft.com (most pages) | works | see Fails for subnetting page | 2026-11-02
- tp-link.com/us|ca|uk|en (product pages, /support/faq/<id> incl. 2643, 3092; /us/blog/<id>/; Canada Deco pages), vigi.com/<cc>/support/faq, omadanetworks.com/<cc>/support/faq (incl. 3007/2996 HomeShield), asus.com/us/support/FAQ/1037946 | works; dated; global pages don't state US hardware version | note region | 2026-11-02
- tp-link.com/us/deco-mesh-wifi/product-family/deco-be25-outdoor/ and /deco-x50-outdoor/, tp-link.com/us/support/faq/3611/ (X50-Outdoor FAQ), /faq/497/ (factory reset, Apr 17 2026) | works; no US price on product pages | leave Deco prices out unless a US retailer page comes back | 2026-11-04
- store.ui.com/us/en/products/u7-outdoor | works; price + surcharge, no specs/stock | pair with ui.com/wifi/outdoor (spec columns unlabeled: cite Qualified) and help.ui.com/hc/en-us/articles/360012622613 (adoption) | 2026-11-04
- github.com/gohugoio/hugo/releases (curl hugo_extended_0.167.0_linux-amd64.tar.gz) | works; hugo not preinstalled in sandbox | install at start of run | 2026-11-04

- support.microsoft.com/windows/faster-and-more-secure-wi-fi-in-windows-26177a28-38ed-1a8e-7eca-66f24dc63f09 | works; Wi-Fi 7 from Win 11 24H2, netsh 802.11be check, MLO check; updated 2026-10-08 in metadata; does NOT state Wi-Fi 7 unavailable on Win 10 (fetch summary claimed it) | quote only the 24H2 sentence | 2026-11-05
- netgear.com/home/wifi/adapters/a9000/ (US price, no stock) + downloads.netgear.com/files/GDC/A9000/A9000_TS.pdf | works | product page and data sheet differ on 320 MHz; cite each | 2026-11-05
- tp-link.com/us/products/details/archer-tbe6500u.html, tp-link.com/us/home-networking/pci-adapter/ (US lineup, no prices), vigi.com/us/home-networking/pci-adapter/archer-tbe550e/ (TP-Link US page on vigi domain) | works; no prices | leave TP-Link adapter prices out | 2026-11-05
- tp-link.com/us/faq-2248.html (mix Deco models, updated 2026-11-03), tp-link.com/support/faq/3529 (EasyMesh, 2022), omadanetworks.com/us/support/faq/3611 | works | none | 2026-11-05
- eero.com/support/articles/can-i-use-an-eero-beacon-or-eero-6-extender-with-a-non-eero-router, /does-eero-replace-my-current-router, eero-outdoor-7(-frequently-asked-questions), /is-eero-waterproof-or-water-resistant, /215473703-How-do-I-reboot-or-reset-my-eero, eero.com/shop/eero-outdoor-7 | works; undated; shop and spec page disagree on Outdoor 7 adapter wattage | don't cite adapter wattage | 2026-11-05
- support.google.com/googlenest/answer/12353201 (Nest Wifi Pro mesh compatibility), wi-fi.org/node/35426 (EasyMesh 2018 release) | works | none | 2026-11-05

## Fails (don't fetch)
- starlink.com/support/article/* | fails: renders empty (JavaScript) | use reseller copies (support.satellitephonestore.com, cite Qualified) or Starlink PDFs on api.starlink.com | 2026-10-25
- netgear.com/<cc>/hub/* | fails: redirects to auhub.netgear.com, which asks for approval | use kb.netgear.com, or www.netgear.com/hub/network/* (no country code), which works | 2026-10-31
- gsc-wizard connector | fails: payment_required | not used by daily runs | 2026-10-25
- curl to wifiweekly.com live pages | blocked in run on 2026-10-25 | use the PR's Cloudflare Pages check run + one WebFetch per URL | 2026-10-25
- bestbuy.com product pages | renders without visible price (metadata only) | leave prices out | 2026-10-27
- URLs carried over from IDEAS.md without a fresh search result (support.google.com/googlehome/answer/6274660, kb.netgear.com/25722) | fail: PROVENANCE_REQUIRED approval timeout | always re-search so the URL comes back in today's results | 2026-10-28
- rtings.com router reviews | renders metadata only (no results) | don't rely on RTINGS for measurements | 2026-10-28
- wi-fi.org/system/files/*.pdf | fails: redirects to login | use FCC or internal band guide | 2026-10-28
- bhphotovideo.com RS200 pages (1861250-REG) | fail: client_error | use another retailer or leave price out | 2026-10-29
- community.netgear.com/kb/nighthawk-firmware-releases/* | fail: client_error | use kb.netgear.com firmware pages | 2026-10-29
- blog.eero.com/* | 302 redirect to eero.com/blog/articles/* | search the eero.com/blog/articles title | 2026-10-31
- techspecs.ui.com/* | fails: robots_disallowed | use store.ui.com product page + help.ui.com + a retailer listing | 2026-11-02
- store.google.com/product/pixel_*_specs | fails: returns current Pixel lineup, not the requested model | use carrier/maker spec PDFs or skip Pixel claims | 2026-11-02
- bhphotovideo.com CyberPower CP1500PFCLCD (1512415-REG) | fails: client_error | use MSRP from cyberpowersystems.com, labeled | 2026-11-03
- apc.com/us/en/product/BGE90M/* | fails: 302 to se.com all-products (discontinued) | use apcguard.com page | 2026-11-03
- omadanetworks.com/<cc>/support/faq/2303 | works but is about Wi-Fi 6 detection on old Intel cards, not 6 GHz | don't cite for 6 GHz | 2026-11-03

## No official answer found
- NETGEAR Orbi with other brands | only community.netgear.com threads returned | omit Orbi cross-brand claims | 2026-11-05
- Micro Center ASUS PCE-BE92BT | price renders garbled ("$6999"), in-store only | don't cite | 2026-11-05
- TP-Link Deco outdoor US prices | no US retailer page returned (only intl. retailers, slickdeals, camelcamelcamel) | leave out | 2026-11-04
- techspecs.ui.com U7 Outdoor | returned in search but robots_disallowed (see Fails) | use ui.com/wifi/outdoor, Qualified | 2026-11-04
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
- CyberPower DC-output (FTTx) mini UPS models | family page lists no models/specs | skip DC UPS picks | 2026-11-03
- Router/modem typical power draw | no maker figure fetched; APC brochure uses 10 W example | cite APC example only | 2026-11-03
