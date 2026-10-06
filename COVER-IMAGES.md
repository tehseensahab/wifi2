# Cover images

Every post has a `cover.jpg` in its folder. All current covers are free (non-Unsplash+) photos from Unsplash, used under the [Unsplash License](https://unsplash.com/license): free for commercial use, credit not required. We credit the photographer in each post's `imageCredit` anyway.

How covers are used:
- Hugo crops each `cover.jpg` to 1200x630 (and 600x315 for phones) as webp q80, using smart cropping. Social share images use a 1200x630 JPG.
- The original `cover.jpg` is not published; only the resized versions are.
- `imageAlt` describes what is actually in the photo. If you replace a photo, update `imageAlt` and `imageCredit` too.

**Reviews:** the two review covers are generic router photos, not the reviewed product. Replace them with your own photos of the Asus RT-BE92U and Netgear Orbi 970 when you have them.

## Current covers

| Post | Photo | Photographer |
|---|---|---|
| `content/reviews/asus-rt-be92u-review/` | [Close-up of a black Wi-Fi router with several tall antennas](https://unsplash.com/photos/43ak6tfF4Ss) | dlxmedia.hu |
| `content/reviews/netgear-orbi-970-review/` | [Ethernet cables plugged into the yellow LAN ports on the back of a router](https://unsplash.com/photos/tN344soypQM) | Stephen Phillips - Hostreviews.co.uk |
| `content/guides/best-mesh-wifi-for-large-house/` | [Bright, open living room with a sofa, shelves, and a coffee table](https://unsplash.com/photos/6qbtnk_GrfU) | Filios Sazeides |
| `content/guides/best-wifi-router-for-large-house/` | [White Wi-Fi router with two antennas against a bright background](https://unsplash.com/photos/mhA3QOXME5M) | Compare Fibre |
| `content/guides/how-to-fix-slow-wifi/` | [Phone screen showing speed test results for download, upload, and ping](https://unsplash.com/photos/gwWkv06WYFY) | Mika Baumeister |
| `content/guides/mesh-vs-router-guide/` | [Living room with a TV on a wooden shelving unit full of books and plants](https://unsplash.com/photos/XE6PBDd7_FQ) | Jonas Leupe |
| `content/guides/wifi-extender-placement-guide/` | [Plug-in Wi-Fi extender next to a small network switch with Ethernet cables](https://unsplash.com/photos/oZgzVU_B3sE) | User_Pascal |
| `content/guides/wifi-router-vs-mesh/` | [White Wi-Fi router with a blue Ethernet cable plugged into the back](https://unsplash.com/photos/hXVVNB6Qctg) | Compare Fibre |
| `content/guides/wifi-slow-but-internet-fast/` | [Person sitting on a couch at home working on a laptop](https://unsplash.com/photos/sR24zAyFgJE) | Surface |
| `content/guides/fiber-vs-cable-vs-5g-home-internet/` | [Ends of fiber-optic strands glowing blue in the dark](https://unsplash.com/photos/INNsF0Zz_kQ) | Compare Fibre |
| `content/guides/matter-thread-smart-home-explained/` | [Google smart speaker next to a smart lock and bridge on a shelf](https://unsplash.com/photos/Fh3Dtg6QX4Q) | Sebastian Scholz (Nuki) |
| `content/guides/router-hardening-checklist/` | [Network router with blue Ethernet cables plugged in and status lights on](https://unsplash.com/photos/dyUp7WPu5q4) | Albert Stoynov |
| `content/guides/fix-bufferbloat-gaming-lag/` | [Two people holding game controllers while playing a soccer game on a TV](https://unsplash.com/photos/eCktzGjC-iU) | JESHOOTS.COM |
| `content/news/fcc-6ghz-power-rules/` | [White Wi-Fi access point mounted on a metal cable tray](https://unsplash.com/photos/e8_JJxiiydc) | Valentin Lacoste |
| `content/news/test-starlink-mesh-integration-news/` | [Satellite dish mounted on the side of a building against the sky](https://unsplash.com/photos/-NWGWmcEwi4) | Rasta Gubaz |
| `content/news/fcc-router-conditional-approvals-status/` | [Shopper browsing shelves in a brightly lit electronics store](https://unsplash.com/photos/bKDOZ7neVl4) | Bhanu Singh |
| `content/news/wifi-8-routers-us-availability/` | [White Wi-Fi router with four antennas lit in blue and pink light](https://unsplash.com/photos/Wx6zqk5eUng) | Jakub Żerdzicki |
| `content/guides/2-4-ghz-vs-5-ghz-vs-6-ghz-wifi/` | [Small gray Wi-Fi 6 router with two flip-up antennas on a wooden table](https://unsplash.com/photos/mTm0YLorp1Y) | User_Pascal |
| `content/guides/wifi-6e-vs-wifi-7/` | [Small gray router with green Ethernet cables plugged in, on a yellow background](https://unsplash.com/photos/KzUCuqTTAVw) | User_Pascal |
| `content/guides/wpa2-vs-wpa3/` | [Silver combination padlock resting on a white computer keyboard](https://unsplash.com/photos/QP7RBa5r8HM) | Sasun Bughdaryan |
| `content/guides/mesh-wifi-wired-vs-wireless-backhaul/` | [Ethernet cables plugged into the ports of a network switch on a wooden desk](https://unsplash.com/photos/SwVkmowt7qA) | Jonathan |
| `content/guides/how-much-internet-speed-do-i-need/` | [Bright living room with a TV showing an underwater scene](https://unsplash.com/photos/Wx23XPAlseI) | Howard Bouchevereau |
| `content/guides/ethernet-cable-cat5e-vs-cat6-vs-cat6a/` | [Yellow Ethernet cable with an RJ45 plug on a blue background](https://unsplash.com/photos/uBcgQA7fwEA) | Markus Spiske |
| `content/guides/guest-wifi-network-smart-home-devices/` | [Round smart thermostat on a white wall showing 63 degrees](https://unsplash.com/photos/RFAHj4tI37Y) | Dan LeFebvre |
| `content/deals/eero-vs-tplink-deal/` | [Close-up of a white router's status lights](https://unsplash.com/photos/LR_wX_klOPM) | Stephen Phillips - Hostreviews.co.uk |
| `content/deals/test-tp-link-deco-mesh-deal/` | [Black Wi-Fi router next to a white TP-Link Deco mesh unit on a table](https://unsplash.com/photos/6ZXP-5-jJts) | TechieTech Tech |

## Adding a cover for a new post

1. Find a real photo (Unsplash or Pexels; no AI images or illustrations), landscape, at least 1200x630. Skip Unsplash+ (premium) photos.
2. Save it as `cover.jpg` in the post folder.
3. Set `imageAlt` to describe the photo, and `imageCredit: "Photo: Name / [Unsplash](photo page URL)"`.

Optional: a fallback share image at `static/images/og-default.jpg` (1200x630) for pages without a cover.
