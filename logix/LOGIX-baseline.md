# LOGIX — What we claim vs what we can prove (the yardstick for every competitor doc)

> Built from: the 11-page Logix business proposal ([text](../context/logix/business-proposal-text.md)) and the Skylabs product context ([LOGIX.md](../context/skylabs/products/LOGIX.md), info up to 8 Nov 2026).
> **No Logix codebase, demo environment or customer data was reviewed to write this.** Every capability below comes from our own deck, so each one starts as **📣 Pitched** and stays there until someone on the team confirms its real status.
> Rule: **✅ Live** = demonstrable today. **🔨 Building** = in development, not shippable. **🧭 Planned** = decided, not started. **❓** = nobody has confirmed. Don't mix them up in public. Never mark ✅ from a deck.

## In one line

**Logix (by Skylabs):** a fleet-intelligence layer for Indian fleet operators. It connects to the GPS/telematics, compliance, toll and accounting systems a fleet already uses, brings the data into one structure, flags what needs attention with AI, and answers plain-language questions (**Logix GPT**) on the web and through a mobile link. **Nothing is replaced.**

**Stage model used everywhere in this repo (from deck p4):** **Connect → Understand → Act.**

## What the deck pitches

Status column is deliberately **❓** for every row. Fill it in with the team, then add a link to the proof (demo recording, test log, screenshot of real data — kept private if client data).

### Connect — data in

| Capability | What the deck says | Deck page | Status | Proof needed |
|---|---|---|---|---|
| OEM telematics platforms | Connects to Tata Motors, Ashok Leyland, Mahindra, Eicher, Bharat Benz platforms | p3 | ❓ | Which are built / tested; how (API, file, login) |
| Third-party GPS | "Five or more GPS platforms"; "Across 5 GPS platforms" in the dashboard; "most fleet dashboards in use today" | p2, p4, p8 | ❓ | List of GPS vendors actually connected |
| Toll / compliance rails | FASTag, VAHAN, PUC, Challan | p3 | ❓ | Route used (government ULIP gateway vs paid reseller) — see [INTEGRATION-MAP.md](../integrations/INTEGRATION-MAP.md) |
| Operations / accounts | Karins, "Custom ERP", Tally, "+ more systems" | p3 | ❓ | Which exist; whether "Karins" = Karins Fleet |
| One data structure | Data "brought into one structure and compared" | p3, p4 | ❓ | Data model / how vehicles and trips are matched across vendors |

### Understand — one view, analysis

| Capability | What the deck says | Deck page | Status | Proof needed |
|---|---|---|---|---|
| Fleet overview dashboard | Total vehicles, on trip, idle > 4 h, distance today, open alerts, live map, priority alerts, 7-day utilisation | p8 | ❓ | Real screen (private OK) |
| Vehicle performance | Score on utilisation, idle time, loading/unloading, halts, trips, challans | p5, p8 | ❓ | Scoring formula |
| Trip intelligence | Planned vs actual route, distance, stops, travel time; trips by customer / vehicle / distance; planned vs actual mileage and fuel | p5, p8 | ❓ | Where "planned" comes from |
| Driver performance | Harsh driving, neutral coasting, excessive halts, long idle; utilisation and efficiency | p5, p8 | ❓ | Which sources expose these fields |
| Vehicle health and compliance | Challans, PUC, documents, service history; due-date alerts (e.g. "PUC due in 6 days") | p5, p7, p8 | ❓ | Document source and refresh |
| Fuel and expense variance | Fuel allowance vs actual; payment mismatches | p5, p8 | ❓ | Fuel source (sensor / OEM / card) and payments source |
| Insights and smart feedback | Patterns turned into plain-language summaries, alerts and reports | p5 | ❓ | Sample output |

### Act — alerts, assistant, mobile

| Capability | What the deck says | Deck page | Status | Proof needed |
|---|---|---|---|---|
| **Logix GPT** | Plain-language Q&A over all connected data; shows numbers behind answers; links to the underlying records | p6 | ❓ | How answers are grounded; error handling; permissions |
| Scheduled briefs | "Send this to the operations team on Telegram every morning" | p6 | ❓ | Demo of the Telegram flow |
| Proactive alerts | Fuel drops, delays, compliance due dates, ETA delays; daily briefs | p6, p7, p8 | ❓ | Delivery channel(s) |
| ETA deviation | "ETA delayed 2h 15m" | p7, p8 | ❓ | How ETA is computed |
| Mobile | Mobile-friendly link, opens in a browser, nothing to install | p7 | ❓ | Real phone screen |
| Role views | Owners, Operations, Fleet supervisors, Accounts | p3, p9 | ❓ | Actual role model (p9 omits Fleet supervisors) |

### Business and delivery

| Item | What we know | Status |
|---|---|---|
| Deployment | The deck says "Logix runs today at a fleet operator" (p9). Skylabs' own rule is not to say deployed or production-ready unless verified. | ❓ **Confirm wording** |
| Customers | None named in the deck (a client name stays private unless approved). | ❓ |
| Pricing | **Not in the deck.** No plan, per-vehicle price or setup fee is decided or documented here. | ❓ |
| Hosting, security, data location | Not in the deck. | ❓ |
| Languages | Not in the deck. | ❓ |

## Gaps the deck leaves open

Details and ranking in [business-proposal-analysis.md §4](../context/logix/business-proposal-analysis.md). The five that matter most: **price · how data gets in · security and permissions · AI accuracy · onboarding time.**

## Known limits (say them, don't hide them)

- All screens in the deck are **illustrative**; the deck says so on pp. 6, 7 and 8. Don't quote their numbers as results.
- The deck's AI capabilities depend on **which fields each source exposes**. A plain GPS tracker gives position and speed; neutral driving, fuel drops and gear data come from OEM telematics or sensors. Coverage will differ vendor by vendor.
- OEM and government data access has rules and costs we haven't confirmed yet — see [INTEGRATION-MAP.md](../integrations/INTEGRATION-MAP.md).

## Building / planned

❓ Not documented anywhere in this repo. Add the real list (ordered) once the team confirms it. Until then, don't describe anything as "building" or "planned" in a comparison.

## Questions for the team (answers turn this file into a real baseline)

1. For each row above, is it ✅ live, 🔨 building, 🧭 planned or ❌ not planned?
2. Which of the five OEM platforms and which of the named compliance systems are actually connected today, and how (API, file export, credentials, partner)?
3. Is p9's "runs today at a fleet operator" accurate as written? What exactly runs — which sources, how many vehicles?
4. Is "Karins" in the deck Karins Fleet (fleet.karins.in)?
5. How are VAHAN / FASTag / challan data fetched — ULIP registration, or a paid reseller?
6. What channels do alerts and briefs use — Telegram only, or also WhatsApp / SMS / push / email?
7. Is there a price range, even internal, we should benchmark against?
8. What is the first real customer segment: own-fleet owners, transporters, shippers, or all three?
