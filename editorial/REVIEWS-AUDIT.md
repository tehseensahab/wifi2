# Reviews audit (owner report)

Run: 2026-10-20. Scope: every page under content/reviews/. No review page was edited; this is a report only.

| Path | Claims found (exact phrases) | Risk | Suggested fix |
|---|---|---|---|
| reviews/asus-rt-be92u-review | "the fastest router we've tested this year on a real home network" (summary and body); "holding median latency under 12 ms with 15 devices online"; "Held 1.4 Gbps+ on 6 GHz at 20 feet through a wall"; "Throughput on the 6GHz band held above 1.4Gbps at 20 feet through a single drywall wall"; "something we couldn't say about the previous model"; "Band steering works without manual tweaks"; `score: 8.7` (marked "PLACEHOLDER: set from your own testing"); `testedOn: 2026-09-20`; byline "Dana Okafor" | high | Unless real test logs exist, remove score and testedOn, delete the measured-throughput, latency and "we've tested" claims, and either rebuild the page as a research-based guide (spec-sheet facts with sources) or unpublish it. If testing did happen, publish the methodology and raw results. |
| reviews/netgear-orbi-970-review | "The fastest mesh kit we've tested"; "didn't visibly slow down under a 20-device stress test"; "the first mesh kit we've tested that didn't visibly slow down under a 20-device stress test, including two simultaneous 4K uploads"; "No visible slowdown in a 20-device stress test"; `score: 8.4` (marked "PLACEHOLDER: set from your own testing"); `testedOn: 2026-09-08`; price and subscription figures ($1,199 3-pack, $99/year) with no source or check date | high | Same as above: remove score, testedOn and stress-test claims unless backed by real test data; source and date-stamp the price and subscription terms (or remove them); consider converting to a sourced guide. |

Notes
- Both pages show a score whose front-matter comment says it is a placeholder, so any rendered score is not backed by testing.
- The YAML comments ("# PLACEHOLDER ...") do not render on the page but are in the repo source.
