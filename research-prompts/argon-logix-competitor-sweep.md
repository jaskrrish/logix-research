# Argon prompt — Logix competitor sweep

Paste everything under the line into Argon. Bring the output back; it gets split into `competitors/<name>/README.md` + `sources.md` (using [the template](../_templates/competitor-template.md)) and compared against [logix/LOGIX-baseline.md](../logix/LOGIX-baseline.md).

Deliberately left out of the prompt: client names, our pricing, anything about our customers, and the Logix-vs-them comparison (that stays internal). Don't add them back.

Starting list = [competitors/LANDSCAPE.md](../competitors/LANDSCAPE.md). If you add a competitor there, add it here too.

---

You are a competitive-intelligence researcher. Produce a research document a product team can act on. Be blunt and evidence-first. Today is 14 Nov 2026. Any fact older than 12 months must be rechecked for whether it is still true.

## Who we are (so you know what matters)

Logix is an AI fleet-intelligence layer for Indian fleet operators (trucking / logistics fleets of roughly 20–500 vehicles). It does **not** replace what the fleet already uses. It:
1. **Connects** to the systems a fleet already has — GPS / telematics portals (including truck-maker platforms), toll (FASTag), vehicle and driver registries (VAHAN), challans, pollution certificates (PUC), accounting (Tally), custom ERPs.
2. **Understands** — brings that data into one structure and scores vehicles, trips and drivers, and reconciles fuel and payments.
3. **Acts** — flags exceptions, sends alerts and daily briefs, and answers plain-language questions through an assistant ("which trucks idled more than 4 hours yesterday, and why?") on the web and a mobile link.

What we care about, in order:
1. **Does the product read third-party systems, or only its own hardware?** Which systems exactly (named vendors, OEM portals, government rails), and **how** — API, webhook, file export, SIM/FASTag inference, or credentials-based scraping?
2. **Is the AI assistant real, and how is it built?** What can it answer, how are answers grounded (queries over structured data, retrieval, tool calls), can it take actions (schedule reports, create alerts), which channels (web, WhatsApp, Telegram, SMS, voice)?
3. **Indian rails.** VAHAN, FASTag, e-challan, PUC, e-way bill, Tally, Sarathi: native, via a partner, or absent?
4. **What does it cost?** Per vehicle, per fleet, per integration, per user; setup fees; contract length.
5. **Is anyone actually using it?** Named Indian customers, reviews, volume — or is it a demo?

Do NOT write about us, our price, or how any competitor compares to us.

## Who to research

Official sites are listed only where already confirmed live on 14 Nov 2026. Where it says "find", locate the real official site yourself; if none exists, say so and treat status as unknown. If a name matches more than one company, say which ones you found and research the **fleet / logistics** one.

### Tier A — closest: aggregate or unify third-party systems, and/or add an AI layer, for Indian fleets (full write-up each)

| Name | Start from | Notes |
|---|---|---|
| Elixia (Elixia Tech) | https://www.elixia.tech/ · https://elixia.tech/integrations.html · https://elixia.tech/track.html | Claims **80+ GPS vendors** normalised and **Elixia Pulse** (AI layer on top of a TMS, via web / phone / WhatsApp). Verify both: which vendors, how, and what Pulse can really do. Try the sample workspace if it is free. |
| Karins Fleet | https://fleet.karins.in/ | FASTag + GPS + fuel card + Vahan / Sarathi / e-challan on one login. Find the company behind it (Karins Engineering?) and whether it exposes an API to third parties. |
| Fleetx | https://www.fleetx.in/ | Conflicting rival-authored claims: hardware-agnostic with webhook push vs own hardware ecosystem. Resolve it. Also funding (Series C headline) and AI features. |
| LocoNav | http://loconav.com/ | Does it aggregate third-party trackers? One rival blog says its India business is now part of Sensorise — verify ownership. |
| FleetERP | https://fleeterp.in/ | "Device-agnostic, no hardware." What integrations are real? VAHAN "via an authorised data partner" — which? |
| Fretron | https://fretron.com/ | TMS for manufacturers. "AI agents" over supply-chain data; ULIP integrations. Different buyer (shippers) — keep to features relevant to a fleet operator and note where the buyer differs. |
| Traxium | https://www.traxium.in/ | Small software-first player. Verify it exists as described, its integrations (WheelsEye etc.), price, customers. |

### Tier B — Indian telematics / payments / marketplace players (short write-up: sections 1, 3, 4, 5 only)

| Name | Start from |
|---|---|
| Intangles | https://www.intangles.ai/ |
| TrackoBit | https://trackobit.com/fleet-management-software |
| Vamosys | https://vamosys.com/ |
| BlackBuck | https://www.blackbuck.com/ (FY26 annual report is public) |
| WheelsEye | https://wheelseye.com/ |

### Tier C — truck-maker (OEM) fleet platforms (short write-up + a mandatory "data access" paragraph)

For each: what does the customer portal show; **is there an API or data-export route for a third party, who can use it, what does it cost, and what proof is there that anyone uses it?**

| Name | Start from |
|---|---|
| Tata Motors Fleet Edge | https://fleetedge.tatamotors.com/ · https://fleetedge.tatamotors.com/features (mentions an "API Management Solution") |
| Ashok Leyland iAlert | find official page; Play Store: com.al.ialert4 |
| Mahindra iMAXX | https://www.mahindratruckandbus.com/english/blog/all-you-need-to-know-about-mahindra-imaxx-telematics-technology.aspx (2022 blog mentions an "API library" — still true?) |
| Eicher (VECV): My Eicher / Eicher LIVE / Uptime NXT | https://www.vecv.in/press-releases/eicher-trucks-buses-launches-uptime-nxt-services-powered-by-ai-enabled-uptime-centre |
| BharatBenz Truckonnect (Daimler India) | https://www.bharatbenz.com/truckonnect |

### Tier D — global leaders, as a benchmark for the assistant and the "act" layer (short write-up)

| Name | Start from | Focus |
|---|---|---|
| Samsara | https://www.samsara.com/products/platform/ai-fleet-management | Assistant, Agent Studio (13 Oct 2026), MCP (22 Sep 2026). Pricing for AI features. Does it work for Indian fleets / Indian rails at all? |
| Geotab | https://www.geotab.com/products/ace-ai-assistant · https://developers.geotab.com/ai/aiAgentAce/index.html | Ace, model card, MCP connector (17 Jun 2026). Summarise exactly how the assistant is built and constrained. India presence? |
| Motive | https://gomotive.com/motive-launches-ai-answers-the-first-conversational-ai-for-physical-operations/ | AI Answers. India presence? |

### Tier E — the human alternative (benchmark, not a product)

Get a real cost and effort benchmark for **how Indian fleets manage today without a unifying layer**:
- Monthly cost (₹) of an operations / MIS executive or analyst who compares several portals and Excel sheets for a 20-, 100- and 500-vehicle fleet. Use at least 8 real sources (salary sites, job postings, trade interviews). Give ranges and how many sources each range rests on.
- Hours per week spent reconciling fuel, toll, challans and trip data, from any credible source (case studies, trade press, operator interviews). If none, say none.
- Typical per-vehicle monthly cost of GPS / telematics subscriptions in India, with the number of sources behind the range. Do not average a handful of vendor listings and call it "the market rate".

### Tier F — discovery

Find up to **10 other** players I have not listed — prioritise Indian fleet / TMS / telematics aggregators and anyone offering an AI assistant over fleet data in India. Candidates to check (names only, **unverified**): FarEye, LogiNext, Locus, Intugine, Superprocure, MapMyIndia (Mappls), Fleetio, Verizon Connect, Trimble, Webfleet. One row each: name · URL · what it does · how serious it looks (real customers vs demo) · one source. No full write-up.

## What to find for each full write-up (Tier A) — use this exact structure, in this order

1. **At a glance** — what it is (input → output, one sentence); which third-party systems it reads; one line each on strong / weak.
2. **Who they are** — table: company (legal name, country, founded, team size) · founders (name + prior companies) · funding · named Indian customers (only if sourced) · reach (app downloads, vehicles tracked, headcount) · tech (any AI vendors / models visible) · independent opinion (reviews, trade press — say if none).
3. **Plans and pricing** — table: plan · price · allowance (vehicles, users, integrations) · what the plan adds. Original currency + approximate INR with the conversion date. Free tier or trial? Setup fee? Contract length? Hardware cost shown separately.
4. **Every feature**, grouped by stage — **Connect** (data in: devices, vendors, government rails, accounting, ERP), **Understand** (normalised data, scoring, trips, fuel, compliance, reports), **Act** (assistant, alerts, briefs, workflows, channels), **Business** (roles, languages, onboarding, support). Columns: feature · what it does · output · plan. Include limits (refresh rate, history window, vehicle caps).
5. **The questions that matter** — short, evidence-backed answers:
   - Third-party systems: which exactly, how, and is there evidence (docs, partner pages, demo footage, customer quotes) or is it a logo wall?
   - The assistant: what it can answer, how it is grounded, whether it can act, channels, any published accuracy or limits.
   - Indian rails: VAHAN / FASTag / e-challan / PUC / e-way bill / Tally — native, partner or absent?
   - India presence: INR price, Indian customers, languages, local support.
   - Real traction vs vanity claims.
   - Anything in the Terms of Service or privacy policy that reveals real limits, data use or underlying vendors.
6. **Social log** — table of public posts / videos that reveal product, price, tier or customers: date · platform · what it shows · link. Only entries that add a fact.
7. **Still open** — everything you could not confirm, ranked by how much it would change a buying decision.

Skip any "us vs them" section.

## Where to look (go deep, not just the homepage)

- Official site: pricing page, product and integration pages, help centre / docs / API reference, changelog, blog, case studies, security page, terms and privacy policy.
- Single-page apps leak copy and tier names in their JavaScript — read it if the visible site is thin.
- App stores (Play, App Store): version history, ratings, review text — reviews often reveal real data problems.
- Social: LinkedIn / YouTube / Instagram / X. Captions and videos often show prices and customers the website hides.
- Independent: Crunchbase, LinkedIn (team size, funding), Tracxn, MCA company records, trade press (Logistics Insider, Transport & Logistics, Autocar Professional, ET Auto, YourStory, Inc42), Reddit, G2 / Capterra / Software Suggest, YouTube demos.
- Job postings (they reveal the real stack and what is being built).
- Government pages for the Indian rails (goulip.in, parivahan.gov.in, nhai / IHMCL) — for context only; the integration questions have their own prompt.
- If a free tier or free trial exists and you can use it without paying and without personal data of third parties, do so and record what you saw. Do not pay for anything, do not use fake identities, do not access anything behind someone else's login, and do not call unofficial or leaked APIs.

## Rules for the writing

- Blunt and simple. "Reads 80 GPS vendors via API" — not "empowers seamless fleet intelligence". No marketing language, no stories, no filler.
- Say what goes in and what comes out. Exact vendors, exact prices, exact limits.
- Every claim gets a source link. Tag each as **observed** (you saw or used it), **vendor claim** (their own words) or **third-party**. Many "best X" guides are written by competing vendors — tag those third-party **(rival-authored)** and treat them as claims. Never present a vendor claim as fact.
- Mark anything you could not confirm with ❓ — never fill a gap with a guess. Mark confirmed items ✅.
- Each fact appears **once**. If it fits two sections, put it in one and refer to it from the other.
- Quote sparingly: short phrases only, in quotation marks, with the source link. Paraphrase everything else.
- Watch for same-name companies and products; state which one you are describing.
- Put the access date on every source.

## Output

One document in Markdown.

1. **Landscape table first** — one row per player across all tiers: name · tier · reads third-party systems (yes / own hardware only / unclear) · AI assistant (yes / no / unclear) · Indian rails (native / partner / none) · starting price · traction (strong / some / none found) · status (live / unclear / dead).
2. **Then one section per competitor**, in the structure above, each ending with a **Sources** list (URL · date accessed · observed / vendor claim / third-party · the key fact it supports).
3. **Then** the Tier E benchmark and the Tier F discovery table.
4. **Finally** a consolidated "Still open" list, ranked by how much it would change a buying decision.

If length forces a cut, finish Tier A completely first, then Tier C, D, B, E, F, and say at the top exactly what is missing.
