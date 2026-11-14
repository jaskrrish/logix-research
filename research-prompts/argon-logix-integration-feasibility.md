# Argon prompt — can Logix really connect to these systems?

How to use: copy everything under the line. To research a subset, delete the rows you don't need from the table in "What to research". Bring the output back; it updates [integrations/INTEGRATION-MAP.md](../integrations/INTEGRATION-MAP.md). Re-run after any change to the systems named in the pitch deck.

Left out on purpose: client names, our pricing, our customers.

---

You are a technical-feasibility researcher for an Indian B2B software product. Be blunt and evidence-first. Today is 14 Nov 2026. Anything older than 12 months must be rechecked for whether it is still true.

## Context

We are building a fleet-intelligence layer for Indian fleet operators. It reads data that a fleet already holds in **other** companies' systems — truck-maker telematics portals, GPS vendors, toll, vehicle and driver registries, challans, accounting — and joins it in one place. The central promise is "nothing is replaced; we connect to what you already use". Before we commit to that promise in front of customers we need to know, system by system, **whether a legitimate, stable, affordable route to the data exists**.

"Legitimate" means: an official API or export, a documented partner programme, or customer-granted access that the vendor's terms allow. A route that works only by scraping a customer's login or using an undocumented endpoint is **not** a finding — report it as a risk, not a route.

## What to research

For every row, answer the **per-system questions** below.

| # | System | Start from |
|---|---|---|
| 1 | Tata Motors Fleet Edge (connected-vehicle platform) | https://fleetedge.tatamotors.com/features — mentions an "API Management Solution" |
| 2 | Ashok Leyland iAlert | find official page; Play Store `com.al.ialert4` |
| 3 | Mahindra iMAXX telematics | https://www.mahindratruckandbus.com/english/blog/all-you-need-to-know-about-mahindra-imaxx-telematics-technology.aspx — 2022 blog mentions an "API library" |
| 4 | Eicher / VECV — My Eicher, Eicher LIVE | https://www.eichertrucksandbuses.com/our-story/technology/hundered-percent-connected |
| 5 | BharatBenz Truckonnect (Daimler India) | https://www.bharatbenz.com/truckonnect |
| 6 | VAHAN (vehicle registry, MoRTH / Parivahan) | https://goulip.in/ (confirmed live) · https://parivahan.gov.in (not yet checked) |
| 7 | SARATHI (driving licences) | https://goulip.in/ |
| 8 | FASTag (NETC / NPCI / IHMCL) | https://goulip.in/ · https://www.ihmcl.co.in |
| 9 | e-Challan (Parivahan) | https://goulip.in/ (confirmed live) · find the official e-challan portal (not yet checked) |
| 10 | PUC (pollution under control certificate) | Find the official source. Is there an API, or is it only a field inside VAHAN data? |
| 11 | e-way bill | https://goulip.in/ · official e-way bill portal |
| 12 | TallyPrime (and older Tally ERP 9) | https://tallysolutions.com/tallyprime-api-explorer |
| 13 | Karins Fleet | https://fleet.karins.in/ — a unified FASTag / GPS / compliance platform; does it offer partner or API access? |
| 14 | Popular third-party GPS platforms used by Indian fleets (find the 8 most-used: e.g. LocoNav, Fleetx, Vamosys, Trakzee, iTriangle, Mappls, WheelsEye, TrackoBit, Elixia — confirm which are real and current) | their developer / API pages |
| 15 | Resellers of government data: LorryCare, Masters India, PeriOne, SignCare | https://lorrycare.com/api-docs · https://docs.mastersindia.co · https://perione.in/services/vahan-sarathi/ · https://docs.signcare.io |

## Per-system questions (answer every one; write "not found" rather than guessing)

1. **Official route.** Is there an official API, data export or partner programme? Link to the primary source (developer docs, regulator page, press release). Quote sparingly.
2. **Who can use it.** Only the vehicle owner? Any registered company? Needs the owner's consent — how is it captured? Is a partner agreement, NDA, or government approval required?
3. **Access process and timeline.** Steps, documents, fees, how long it takes, and who has actually completed it (name public examples).
4. **Cost.** Per call, per vehicle per month, per plan, setup fee, minimums. INR plus approximate conversion date if foreign. If hidden, say so and look for tenders, partner listings or reviews.
5. **Data you get.** Fields (e.g. position, speed, ignition, fuel level, odometer, DTCs, gear / neutral flags, document validity dates, toll plaza, amounts). Be exact about **which fields are missing** compared with what the vendor's own app shows.
6. **Freshness and history.** Refresh rate, delay, how many days of history can be queried (e.g. FASTag crossings are reported as "last 72 hours" by resellers — confirm against official docs).
7. **Limits.** Rate limits, bulk limits, daily caps, vehicle caps.
8. **Terms.** Can a third party combine this data with other sources, store it, show it to its customers, and use it to train or ground an AI model? Retention limits? Resale restrictions? Quote the relevant clause with a link.
9. **Authentication and operations.** OAuth, API key, IP allow-list, signed NDAs on paper? Sandbox available? Support SLA?
10. **Proof of real use.** Named products or companies that already integrate it (partner pages, case studies, app stores). A logo wall is not proof — say whether there is documentation, a SDK, or a customer quote.
11. **Risk.** Single points of failure, regulatory change, deprecation notices, outage history, anything that suggests the route could vanish.

## Government data — extra questions

- Compare what the official ULIP portal (goulip.in) says with what resellers say. Where they differ, report both and say which you trust and why.
- Can a private SaaS company obtain VAHAN / SARATHI / FASTag / e-challan access **for its own customers' vehicles** under ULIP? What use-case wording is accepted, and what has been rejected, if anything is public?
- What does registering directly (ULIP) cost in time, paperwork and obligations versus buying the same data from a reseller per call? Give a worked example for a 100-vehicle fleet checking VAHAN weekly, FASTag daily, challans daily, using published reseller prices.
- Is there a legitimate source for **toll amounts paid** (billing, not just crossings) — issuing bank portals, fleet fuel / toll cards? How does a fleet get it today?
- Is there a legitimate source for **payments** that Logix could use to flag "payment mismatches" (fuel cards, FASTag wallets, bank feeds, Tally vouchers)? Which is the most common in Indian fleets?

## Data protection — flag, don't give legal advice

India's Digital Personal Data Protection Act, 2023 (and any rules notified under it) may apply to driver identity, driving-behaviour scores and location. Summarise, with links to primary sources: what status the Act and its rules have today, what duties a software provider that processes driver data for a fleet operator would have, and any rules specific to location or vehicle data in transport. Mark everything you are unsure of with ❓. This is background for a lawyer, not advice.

## Rules for the writing

- Every claim gets a source link and an access date. Tag each: **official** (government, regulator, the vendor's own docs), **vendor claim** (marketing or blog), **third-party**, or **observed** (you used a sandbox or free tier without paying and without using someone else's data).
- Mark anything you could not confirm with ❓. Mark confirmed items ✅. Never fill a gap with a guess.
- Do not pay for anything, do not use fake identities, do not access anyone's login, do not call unofficial or leaked endpoints.
- Blunt and simple. "Needs the owner's written consent and a signed API agreement" — not "enterprise-grade integration capabilities".
- Each fact appears once.

## Output

One Markdown document.

1. **Feasibility table first** — one row per system: system · official route? (yes / partner / no / unclear) · who can use it · cost · fields we'd get · history window · biggest blocker · confidence (high / medium / low).
2. **Then one section per system**, answering the 11 questions, ending with a **Sources** list (URL · date accessed · tag · the fact it supports).
3. **Then** the government-data section (with the worked cost example), then the data-protection section.
4. **Finally** a ranked list: which five integrations to build first (easiest legitimate route and highest customer value), which three are riskiest, and a "Still open" list ranked by how much it would change the plan.

If length forces a cut, finish rows 1–13 first, then 15, then 14, and say at the top exactly what is missing.
