# Logix business proposal — what the deck claims, what it leaves out, what to compare on

> Written 14 Nov 2026 from the 11-page deck ([full text](business-proposal-text.md)) plus the outside checks listed in [../../competitors/LANDSCAPE.md](../../competitors/LANDSCAPE.md).
> ✅ checked against a public source · ❓ not confirmed · The deck is **our** copy — nothing in it counts as proof.
> Purpose: turn the deck into (1) a claim list the baseline can be audited against, (2) the axes every competitor gets compared on, (3) the questions a buyer will ask that the deck doesn't answer.

---

## 1. What the deck is

| | |
|---|---|
| Audience | An Indian fleet operator's owner / operations / accounts team. Not an investor deck. |
| Length and shape | 11 pages: problem → where Logix fits → solution → AI → Logix GPT → mobile → platform preview → impact → team → contact. |
| One-line pitch | A layer that sits **on top of** the systems a fleet already uses, reads them together, and tells people what needs attention. "Nothing is replaced." |
| The three verbs | **Connect → Understand → Act** (p4). Our template for competitor features uses the same three stages so the comparison lines up with how we sell. |
| Hero feature | **Logix GPT** (p6–7): ask a question in plain language, get a number-backed answer, schedule it to Telegram. |
| Proof offered | One line on p9: "Logix runs today at a fleet operator." No customer, number or screenshot of real data. All screens are marked illustrative. |
| What it does not contain | Price, integration method, security, onboarding time, accuracy, number of customers. See §4. |

---

## 2. Claim inventory

Every claim a buyer could test. **Status stays ❓ until the team confirms it** — the deck's own wording is not evidence. Fill the last column as proof arrives.

| # | Claim (page) | Type | Why it needs proof | Proof we have |
|---|---|---|---|---|
| C1 | "Connects to **most fleet dashboards in use today**" (p4) | Broad vendor claim | The only integrations *named* are 5 OEM platforms + Karins, FASTag, PUC, VAHAN, Challan, Tally, "custom ERP" (p3). "Most" is a much bigger promise than 12 named systems. | ❓ none |
| C2 | Names Tata Motors, Ashok Leyland, Mahindra, Eicher, Bharat Benz as connected GPS/telematics platforms (p3) | Logos shown as "your systems" | Logo ≠ working integration. OEM portals differ in whether they expose data at all (see [../../integrations/INTEGRATION-MAP.md](../../integrations/INTEGRATION-MAP.md)). | ❓ which are built / tested |
| C3 | Connects to FASTag, PUC, VAHAN, Challan, Tally (p3) | Vendor claim | VAHAN, FASTag and e-challan are reachable through the government's ULIP gateway or paid third-party API resellers; each has access rules and cost. PUC has no separate source we could find. | ❓ route not confirmed |
| C4 | "Logix runs today at a fleet operator, bringing GPS, compliance and toll data into one view" (p9) | Deployment claim | Skylabs' own rule: do not say deployed / production-ready unless verified ([../skylabs/products/LOGIX.md](../skylabs/products/LOGIX.md)). | ❓ **confirm wording matches reality before the deck circulates** |
| C5 | "Across 5 GPS platforms" / "Connected to 8 sources" (p6, p8) | Illustrative | Marked illustrative, but a buyer will read it as a real capability. | ❓ |
| C6 | AI "finds anomalies a person would take hours to spot" (p5) | Capability claim | No accuracy, false-alarm rate or example from real data. | ❓ |
| C7 | Detects "harsh driving, **neutral coasting**, excessive halts, long idle" (p5) | Capability claim | These need richer data than a GPS ping. GPS-only trackers can't see neutral coasting; OEM telematics can. So the feature only works for sources that expose those fields. Also see §3: OEM portals already ship some of this. | ❓ |
| C8 | "Fuel allowance against actual use, and **payment mismatches**" (p5, p8) | Capability claim | Needs fuel data (sensor / OEM CAN / fuel card) **and** a payments source. Which payments source? Not stated. | ❓ |
| C9 | Logix GPT answers "from **all** connected data", shows "the numbers behind them" (p6) | Capability claim | How are answers grounded (query over a normalised store, or a model reading raw text)? Competitors publish this — e.g. Geotab says Ace turns questions into SQL ([developers.geotab.com](https://developers.geotab.com/ai/aiAgentAce/index.html), accessed 14 Nov 2026). | ❓ |
| C10 | Logix GPT can schedule a daily report to **Telegram** (p6) | Feature | Real, specific, and different from competitors that lead with WhatsApp. Needs a demo. | ❓ |
| C11 | "Mobile-friendly link … nothing to install" (p7) | Feature | A web app, not a native app — fine, but no push alerts unless built. Alerts "as they happen" (p7) needs a channel (Telegram? SMS? WhatsApp?). | ❓ channel |
| C12 | Role views for Owners, Operations, **Fleet supervisors**, Accounts (p3) | Feature | p9 lists only Owners, Operations, Accounts. Fleet supervisors drop out. | ❓ pick one list |
| C13 | "Nothing to replace. Nothing to retrain." (p4) | Positioning | Strong claim; the whole thesis. True only if data comes in without touching the customer's workflows. | ❓ |

**Internal consistency (✅ checked):** the illustrative numbers agree across pages — 84 on trip + 19 idle + 27 alerts + 18.4K km (p7) = p8's tiles; 84 of 128 = 66%; the 19 idle trucks split 11 + 5 + 3 = 19 (p6). The deck is tidy; the gaps are in what's behind the screens, not in the screens.

---

## 3. What the outside check changed (14 Nov 2026)

Four findings from the first landscape pass. All sources are in [LANDSCAPE.md](../../competitors/LANDSCAPE.md) and [INTEGRATION-MAP.md](../../integrations/INTEGRATION-MAP.md); none are researched in depth yet.

1. **"Ask your fleet" is no longer rare.** Samsara (Assistant, Agent Studio launched 13 Oct 2026, MCP), Geotab (Ace; MCP connector 17 Jun 2026) and Motive (AI Answers, Oct 2025) all ship natural-language fleet Q&A. In India, **Elixia Pulse** is pitched almost exactly like Logix GPT: "the AI layer on top of your TMS", connected to trips, invoices, GPS and rate cards, reachable on web, phone and WhatsApp. Fretron's TMS also advertises "AI agents" over supply-chain data. Logix GPT as a *feature* is not the differentiator; **cross-vendor reach for Indian fleets** has to be.
2. **Multi-vendor aggregation already has Indian players.** Elixia claims "80+ GPS and telematics vendors" normalised into one feed plus Vahan, Sarathi, FASTag, SAP, Tally. FleetERP sells "device-agnostic, no hardware". Karins Fleet bundles FASTag + GPS + Vahan + Sarathi + e-challan on one dashboard. All vendor claims — to verify — but "nobody connects them" is not safe to say.
3. **OEMs are the data sources *and* the incumbents.** Tata Motors says Fleet Edge passed 1 million connected vehicles (FY26 annual report); Eicher launched an "AI enabled Uptime Centre" and a GenAI "Service One" on 13 Oct 2026; BharatBenz's Truckonnect already lists a "Neutral Driving Report". So some of p5's AI "gaps" are partly closed inside each OEM portal. The honest pitch is the **cross-system** view (a mixed fleet), not any single detection.
4. **Karins appears in our own deck.** p3 lists "Karins" among the systems Logix connects to, but Karins Fleet is itself a unified toll/GPS/compliance dashboard. It may be a data source, a competitor, or both. ❓ Confirm the deck's "Karins" is Karins Fleet.

---

## 4. What a buyer will ask that the deck doesn't answer

Rank by how likely it stops a deal. These become the "Still open" list for the baseline and the research prompts.

| Priority | Question | Where we'd look |
|---|---|---|
| 1 | **How much?** Per vehicle, per fleet, per integration, one-time setup? | Competitor pricing pages; Indian per-vehicle benchmarks (one third-party guide quotes ₹350–800 / vehicle / month for tracking alone — competitor-authored ❓) |
| 2 | **How does data actually get in?** API, webhook, file export, or scraping a login? Who holds the credentials? | Per-vendor docs; [INTEGRATION-MAP.md](../../integrations/INTEGRATION-MAP.md) |
| 3 | **Security and permissions.** Where is data stored? Who can see what? Samsara and Geotab both lead with "respects existing permissions". | Competitor security pages |
| 4 | **How accurate is the AI?** False alarms, wrong answers, "show your working". | Competitor model cards (Geotab publishes one) |
| 5 | **Onboarding time.** How long from signature to first useful screen? | Fretron says 6–8 weeks to first plant (vendor claim); FleetERP says a 30-day rollout (vendor claim) |
| 6 | **Government-data access.** Is VAHAN/FASTag/e-challan data pulled through ULIP (registration, use-case review, NDA) or a reseller? | [INTEGRATION-MAP.md](../../integrations/INTEGRATION-MAP.md) |
| 7 | **Which customers?** Even one reference. (Client name stays confidential unless approved.) | Team |
| 8 | **Languages.** Drivers and supervisors may not read English. Elixia's driver app is multilingual (vendor claim). | Competitor feature pages |

---

## 5. What every competitor gets compared on

Derived from the deck's own promises. These are the rows of the template ([../../_templates/competitor-template.md](../../_templates/competitor-template.md)) and the questions in the research prompts.

| Stage | Axis |
|---|---|
| **Connect** | Which systems does it read — own hardware only, or third-party GPS / OEM portals too? How many vendors, and how (API / webhook / file)? Indian rails: VAHAN, FASTag, e-challan, PUC, Tally, e-way bill? |
| **Understand** | One normalised data model, or separate screens? Vehicle score, trip planned-vs-actual, driver behaviour, fuel variance, compliance calendar — what's shipped vs claimed? |
| **Act** | Natural-language assistant (what can it answer, how is it grounded, can it *do* things)? Alert channels (WhatsApp / Telegram / SMS / push / email)? Scheduled briefs? Role views? |
| **Business** | Price per vehicle / seat / integration; contract length; onboarding time; named Indian customers; funding and traction; languages. |
| **Fit** | Buyer size (5 trucks vs 500), buyer type (fleet owner vs shipper vs transporter), India-readiness. |
