# Fact-check: 5G Home Internet vs. Cable (2026-11-18)

Independent fact-check by a separate agent that did not write the draft; 4 sources re-fetched (T-Mobile metrics, T-Mobile Test Drive, Verizon broadband services, Xfinity outage page). Result before fixes: 21 verified / 16 qualified / 4 not verified.

Not verified, fixed: "port forwarding" as a cable advantage in description (removed; cable needs checking too); "no-contract switchers" (replaced by 15-day Test Drive); "cable capacity is shared with your neighborhood" (cut); "add your own router behind the gateway" (now framed as pointer to internal guide).
Qualified, rewritten: prioritization wording now per carrier (T-Mobile heavy-data-user priority; Verizon "certain plans"); upload range "10 to 56 Mbps on most plans, up to 75 on Verizon's top plan"; Comcast footnote applies to speed and latency (tests to the cable modem gateway); "several times faster" -> "roughly 1.5 to 4 times"; "effective" -> "as of May 8, 2024"; Internet Essentials described as low-income, not mid-split; Verizon up-to-100 Mbps tier added to table.
Calculations: peak vs off-peak download gaps 0.3%, 1.4%, 5.6%, 5.1% ("within about 6 percent"); 114/55=2.1, 209/55=3.8, 114/75=1.5, 209/75=2.8 ("roughly 1.5 to 4 times").
Fast-changing facts rechecked 2026-11-18: T-Mobile Test Drive terms (credit needs timely gateway return; $370 non-return fee). No prices used.

## Research log (verbatim quotes)
## Article A: 5G Home Internet vs. Cable (content/guides/5g-home-internet-vs-cable/index.md)

S1 https://www.t-mobile.com/home-internet/policies/internet-service/network-speed-performance-metrics.html (no page date; © 2026; US)
- All-In/Amplified (5G): Download "Typically between 133 – 415 Mbps"; upload "Typically between 12 – 55 Mbps"; latency "Typically between 16 – 28 ms."
- Rely (5G): "Typically between 87 – 318 Mbps"; upload "Typically between 14 – 56 Mbps"; latency "Typically between 18 – 36 ms."
- Lite (5G): "Typically between 52 – 241 Mbps"; upload "Typically between 11 – 30 Mbps"; latency "Typically between 18 – 36 ms."
- "Based on internal analysis and projections from third-party, crowd-sourced data." "These ranges are projections based on roughly the 25th and 75th percentiles of network tests."

S2 https://www.t-mobile.com/home-internet/policies/internet-service/network-management-practices.html (dates: "As of May 8, 2024" for threshold)
- "In general, T-Mobile Internet customers receive the same network prioritization as Mobile Wireless Heavy Data Users."
- "T-Mobile Internet customers using more than 1.2TB of data in a billing cycle are also considered Heavy Data Users." ... "Internet Heavy Data Users who will be prioritized last on the network."
- "For plans where Internet equipment is intended to be stationary and is only available in limited areas (for example, Home Internet and Home Internet Plus), these customers should be less likely to notice congestion in general."
- No mention of public IP/port forwarding/CGNAT; no Home Internet video resolution limit stated.

S3 https://www.t-mobile.com/support/home-internet/15-day-test-drive
- "Worry-free 15-day test drive." Eligibility "Any customer who activates T-Mobile Home Internet or Small Business Internet on a qualifying plan." "Limited to one per account."
- Cancel: "A one-time bill credit"; return equipment within 45 days of cancellation or "non-return fee of up to $370."
- "If you keep T-Mobile Internet after the 15-day Test Drive, your service continues on your selected plan."

S4 https://www.verizon.com/support/broadband-services/ ("Last update: October 29, 2025")
- Table (25th–75th percentile): 5G Home up to 100 Mbps (mid-band) 25-85 / 5-10 / 50-70 ms; 5G Home up to 300 (high-band/mmWave) 85-300 / 10-20 / 35-55; 5G Home Plus up to 150 50-100/10-15/40-60; 5G Home Plus up to 500 200-500 / 20-35 / 35-55; 5G Home Ultimate up to 300 85-250/10-20/35-55; 5G Home Ultimate up to 1 Gig 300-1000 / 25-75 / 35-55.
- "On certain plans, we may prioritize your 5G and 4G LTE data behind other traffic." "If the cell site you are connected to begins experiencing high demand" speeds may be slower.
- "After 150 GB of data, speeds lowered up to 10 Mbps download and 3 Mbps upload." (Home Internet Lite)
- "at 1080p to devices with larger screens and on the 5G Home, 5G Home Plus, LTE Home, LTE Home Plus," "All Access Home Internet, Verizon Home Internet Lite and Wi-Fi Backup plans," "and at 4K on the 5G Home Ultimate plans, unless a different video resolution is disclosed"
- "5G Home Internet plans vary depending on address/location, equipment, network connection". No mention of public IP/port forwarding/CGNAT.

S5 https://www.xfinity.com/policies/internet-broadband-disclosures (no date)
- "Comcast currently does not maintain a separate system to assist with managing times of congestion."
- "Under these plans, usage that exceeds a monthly usage threshold is subject to an additional charge." (unlimited data available for monthly fee)
- "Comcast blocks a limited number of ports that are commonly used to send spam."

S6 https://www.xfinity.com/networkmanagement ("Published: December 18, 2024"; "the tiers listed in the table below are limited to those currently available for purchase as of April 9, 2024"; peak "Monday through Friday from 7:00pm to 11:00pm local time")
- Columns: Technology | Download tier | DL median peak | DL median off-peak | Upload tier | UL median peak | UL median off-peak | Latency median peak | Latency off-peak | Notation
- "Internet Essentials - HFC/DOCSIS 75 86 87 10 11 11 21 20 1"
- "HFC/DOCSIS Mid-Split 300 351 352 100 114 114 16 15 1"
- "HFC/DOCSIS Mid-Split 1,000 1,142 1,158 100 114 114 16 16 1"
- "HFC/DOCSIS Mid-Split 1,200 1,302 1,379 200 208 209 15 15 1"
- "HFC/DOCSIS Mid-Split 2,000 2,088 2,201 200 206.37 206 14 14 1"
- Footnote (1) "Based on tests to the cable modem gateway."

