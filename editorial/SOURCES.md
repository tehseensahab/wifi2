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

## Fails (don't fetch)
- starlink.com/support/article/* | fails: renders empty (JavaScript) | use satellitephonestore reseller copy or Starlink PDFs on api.starlink.com | 2026-10-25
- netgear.com/<cc>/hub/* | fails: redirects to auhub.netgear.com, which asks for approval | use kb.netgear.com | 2026-10-25
- unsplash.com search pages typed from the prompt (router, internet-router) | fails: approval request times out | WebSearch for the page first | 2026-10-25
- gsc-wizard connector | fails: payment_required | not used by daily runs | 2026-10-25
- curl to wifiweekly.com live pages | blocked in run on 2026-10-25 | use the PR's Cloudflare Pages check run + one WebFetch per URL | 2026-10-25

## No official answer found
- T-Mobile / Verizon 5G Home Internet: CGNAT, public IP, IPv6 | no official page found | don't make carrier-specific CGNAT claims | 2026-10-26
- T-Mobile bridge mode and port forwarding | official answer exists: t-mobile.com/support/home-internet/connect says gateways can't do either | use that page | 2026-10-26
- Verizon IP Passthrough | official KB 301824 covers "Verizon Internet Gateway" without listing models | cite as Qualified | 2026-10-26
- eero / Google Nest Wifi Starlink setup | no official article found | describe generic Ethernet setup only | 2026-10-25
