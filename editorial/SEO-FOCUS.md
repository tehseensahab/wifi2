# SEO focus (from Search Console, updated monthly)

Month 1 baseline (3-30 Oct 2026): 16 clicks, 2,400 impressions, 0.67% CTR, avg position ~27. 96 queries at positions 1-10. Impressions doubled week over week by late Oct; 27-30 Oct fell to ~0-2/day (check indexing if not recovered). Next month's target: 40+ clicks, 5,000+ impressions.

## What works
- Guides = 12 of 16 clicks. Short "should X be on or off" and troubleshooting explainers rank first (band steering, MLO, WPS/UPnP, guest network).
- FCC / news items with a primary source rank fast (fcc-6ghz-power-rules, position ~6).
- Mobile CTR 1.4% vs desktop 0.4%. US = 11 of 16 clicks.

## What does not work yet
- Big "best X" buyer guides sit at position 27-32 (best-mesh-wifi-for-large-house 622 impressions, 0 clicks; best-wifi-router-for-large-house 212). They need backlinks and internal links, not rewrites.
- Reviews are noindex and thin; do not spend daily slots on new product reviews.
- Very long natural-language queries ("...in germany?") are AI-assistant patterns. Do not target them.

## Daily rules from this data
1. Default mix: 1 short intent-matched explainer or "on or off / vs / how to fix" guide in a topic that already earns impressions + 1 other piece (news with primary source, or a buyer guide that links into the large-house cluster). No new standalone "best X" guides while best-mesh-wifi-for-large-house and best-wifi-router-for-large-house stay below position 15.
2. Every new article links to best-mesh-wifi-for-large-house or best-wifi-router-for-large-house where relevant (push authority to the money pages).
3. Title and H1 should contain the exact query phrase (e.g. "X: On or Off?", "X vs Y").
4. Do not publish a second article on a topic that an existing page already ranks for (see cannibalization: /posts/ URLs already 301 to live URLs).

## Open quick-win queries (rewrite or add a section, one per run if time allows)
- wifi for large apartment (pos 13.6) -> guides/best-router-for-apartment, add a "large apartment" section
- best mesh wi-fi for a philly rowhome (pos 9.9, 18 impressions) -> section in best-mesh-wifi-for-large-house on narrow multi-floor rowhomes, only if sources support it
- eero mlo on or off (pos 6.6) -> done in guides/wifi-7-mlo title
- should band steering be on or off (pos 8.4-12.4) -> done in guides/what-is-band-steering title
- should i buy my own modem (pos 23.9) -> guides/buy-your-own-router-vs-isp-equipment, check heading match
- docsis 3.0 vs 3.1 (pos 40) -> guides/docsis-3-0-vs-3-1-vs-4-0-cable-modem, tighten title to "DOCSIS 3.0 vs 3.1"
- how to change wifi channel (pos 40-74), wifi dead zones (pos 49-78): add internal links from new posts

## Monthly routine
On the first of each month Tehseen sends the 28-day GSC export zip. Compare with this file, update the baseline, the works / not works lists and the quick-win queries, then commit to editorial/SEO-FOCUS.md.
