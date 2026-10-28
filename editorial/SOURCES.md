# Source playbook

Read before research; update at the end of every daily run. One line per source: domain or page | works / fails (how) | workaround | date checked. Keep under ~80 lines.

## Works (fetch via WebSearch result, no approval)
- rfc-editor.org (RFC .txt/.html) | works | none needed | 2026-10-25
- blog.apnic.net | works | none | 2026-10-25
- tailscale.com/docs (.md pages) | works | none | 2026-10-25
- kb.netgear.com | works; shows "Last Updated" date | none | 2026-10-25
- asus.com/us/support/FAQ | works; shows "Last Update" date | none | 2026-10-25
- vigi.com/<cc>/support/faq and omadanetworks.com/<cc>/support/faq (TP-Link KB mirrors) | works; shows "Last updated" | use when tp-link.com FAQ doesn't come back in search | 2026-10-25
- api.starlink.com/public-files/*.pdf (Starlink setup guides) | works | none | 2026-10-25
- support.satellitephonestore.com (reseller copies of Starlink help text) | works | cite as Qualified (reseller copy) | 2026-10-25
- dishytech.com | works; third-party Starlink reporting | cite as Qualified | 2026-10-25
- telecompetitor.com | works; reports Ookla figures | none | 2026-10-25
- support.google.com/wifi, eero.com/support (also eero.com/support/articles/*), learn.microsoft.com, pulse.internetsociety.org, xfinity.com/support | works | none | 2026-10-24
- images.unsplash.com (curl download) | works | append ?fm=jpg&q=85&w=2400&fit=max | 2026-10-25
- unsplash.com/s/photos/<term> or /es/s/fotos/<term> | works ONLY when the URL came back in a WebSearch | search "unsplash <term> photos" first | 2026-10-25
- t-mobile.com/support/home-internet/* and t-mobile.com/home-internet/policies/* | works; no last-updated date shown | none | 2026-10-26
- verizon.com/support/knowledge-base-* and verizon.com/support/broadband-services | works; KB pages don't list covered models | cite model scope as Qualified | 2026-10-26
- support.google.com/googlehome (port forwarding, DHCP reservation) | works | none | 2026-10-26
- eero.com/shop/eero-7?pack=pt | works; shows US prices | none | 2026-10-26
- tp-link.com/ca/home-networking/deco/* | works for specs and working modes | note it's the Canada page | 2026-10-26
- asus.com/support/FAQ/<id> (no country prefix) | works; shows "Last Update" | none | 2026-10-26
- unsplash.com/photos/<slug> photo pages from WebSearch | works; returns images.unsplash.com src | none | 2026-10-26
- xfinity.com/support/internet/list-of-approved-cable-modems and /support/articles/upgraded-areas-leased-equipment-required-for-upload-speeds | works; modified dates in metadata; no model lists | use My Device Info wording, don't claim model certification | 2026-10-27
- surfboard.com/products/cable-modems/<model>/ (US pages) | works; specs, warranty, ISP qualification text | none | 2026-10-27
- cox.com print_media Motorola data sheets (PDF) | works | cite as "Motorola data sheet (Cox-hosted)" | 2026-10-27
- netgear.com/home/wifi/modems/<model>/ | works; no price shown; CM2050V page contradicts itself on ISPs | quote both statements | 2026-10-27
- prnewswire.com news releases | works; launch MSRP and dates | MSRP is not a current price | 2026-10-27
- support.apple.com/102078 (Thread) | works; list titled "Thread-enabled Apple devices", not "border routers" | describe Apple devices as Thread-enabled home hubs | 2026-10-27
- support.google.com/googlenest/answer/9249088 and support.google.com/android/answer/16335330 | works | none | 2026-10-27
- developer.amazon.com/docs/alexaplus/smarthome/thread-support | works; Echo/eero border-router list with Thread versions | none | 2026-10-27
- threadgroup.org/newsroom/newsletters/* and developer.espressif.com/blog | works | Espressif = Qualified (chipmaker) | 2026-10-27
- unsplash.com/trends/<term> and /pt-br/s/fotografias/<term> | works when from WebSearch; few modem photos not already used | try localized search pages | 2026-10-27
- support.apple.com/<cc>/102509 (private Wi-Fi addresses) and support.apple.com/guide/platform-support/* | works; shows Published Date | none | 2026-10-28
- source.android.com/docs/core/connect/* | works; shows last-updated date | none | 2026-10-28
- support.microsoft.com/windows/<guid> | works | none | 2026-10-28
- eero.com/support/articles/* (MAC randomization, product comparison) | works; no dates | none | 2026-10-28
- asus.com/us/support/FAQ/<id> and asus.com/ca-en/.../techspec | works; US techspec didn't come back in search | cite Canadian spec page, note it | 2026-10-28
- support.linksys.com/kb/article/<id> | works; some articles render in Dutch (e.g. 1524) | prefer articles that come back in English | 2026-10-28
- tp-link.com/en/products/details/<model>.html and tp-link.com/us/support/faq/<id> | works; global page doesn't state US hardware version | note it | 2026-10-28
- netgear.com/home/wifi/routers/<model>/ (US) | works; price only in metadata; shows stock status | don't cite metadata price | 2026-10-28
- cox.com/llms.txt | works; lists Cox URLs | but linked pages need their own search result | 2026-10-28

## Fails (don't fetch)
- starlink.com/support/article/* | fails: renders empty (JavaScript) | use satellitephonestore reseller copy or Starlink PDFs on api.starlink.com | 2026-10-25
- netgear.com/<cc>/hub/* | fails: redirects to auhub.netgear.com, which asks for approval | use kb.netgear.com | 2026-10-25
- unsplash.com search pages typed from the prompt (router, internet-router) | fails: approval request times out | WebSearch for the page first | 2026-10-25
- gsc-wizard connector | fails: payment_required | not used by daily runs | 2026-10-25
- curl to wifiweekly.com live pages | blocked in run on 2026-10-25 | use the PR's Cloudflare Pages check run + one WebFetch per URL | 2026-10-25
- bestbuy.com product pages | renders without visible price (metadata only) | leave prices out | 2026-10-27
- community.surfboard.com threads | fail: 302 redirect to surfboard.com | don't rely on forum claims | 2026-10-27
- URLs carried over from IDEAS.md without a fresh search result (support.google.com/googlehome/answer/6274660, kb.netgear.com/25722) | fail: PROVENANCE_REQUIRED approval timeout | always re-search so the URL comes back in today's results | 2026-10-28
- cox.com/modems | renders metadata only | Cox residential certified-modem page doesn't surface in search; Cox modem topic dropped | 2026-10-28
- community.verizon.com/kb/* | fails: 302 to verizon.com/support (community sunset) | no Verizon primary for Fios own-router found | 2026-10-28
- rtings.com router reviews | renders metadata only (no results) | don't rely on RTINGS for measurements | 2026-10-28
- wi-fi.org/system/files/*.pdf | fails: redirects to login | use FCC or internal band guide | 2026-10-28

## No official answer found
- T-Mobile / Verizon 5G Home Internet: CGNAT, public IP, IPv6 | no official page found | don't make carrier-specific CGNAT claims | 2026-10-26
- T-Mobile bridge mode and port forwarding | official answer exists: t-mobile.com/support/home-internet/connect says gateways can't do either | use that page | 2026-10-26
- Verizon IP Passthrough | official KB 301824 covers "Verizon Internet Gateway" without listing models | cite as Qualified | 2026-10-26
- eero / Google Nest Wifi Starlink setup | no official article found | describe generic Ethernet setup only | 2026-10-25
- Xfinity: which retail modems are certified for upgraded (mid-split) upload by address | only via My Device Info (sign-in/address) | tell readers to check My Device Info | 2026-10-27
- Cox residential certified modems list | page exists (cox.com/residential/support/cox-certified-cable-modems.html per cox.com/llms.txt) but never returned in WebSearch | retry search with new phrasing; otherwise skip Cox | 2026-10-28
- Verizon Fios using your own router | no fetchable Verizon page found | skip | 2026-10-28
