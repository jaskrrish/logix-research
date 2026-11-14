# Argon prompt — one Logix competitor at a time

How to use: copy everything under the line, replace `[COMPETITOR NAME]` with the name (e.g. `Elixia`, `Karins Fleet`, `Tata Motors Fleet Edge`). `[KNOWN LINKS]` is optional — paste URLs from [LANDSCAPE.md](../competitors/LANDSCAPE.md), or delete that line. Run it once per competitor, bring the output back, and it becomes `competitors/<name>/README.md` + `sources.md` ([template](../_templates/competitor-template.md)).

Left out on purpose: client names, our pricing, and the Logix-vs-them comparison (done internally afterwards).

Name clashes to watch when you fill it in: "Karins" = Karins Fleet (fleet.karins.in), not other Karins companies. "Elixia" = Elixia Tech (elixia.tech, fleet and logistics), not the many other products with similar names. "Fleetx" — confirm the official domain (fleetx.in) before reading anything else.

---

You are a competitive-intelligence researcher. Research **one company only: [COMPETITOR NAME]**. Produce a single document a product team can act on. Be blunt and evidence-first. Today is 14 Nov 2026 — anything older than 12 months must be rechecked for whether it is still true.

[KNOWN LINKS: paste URLs here, or delete this line]

## Scope

- Research only [COMPETITOR NAME]. Do not write about other companies, and do not compare it to anyone. If [COMPETITOR NAME] names its own rivals, note who they are in one line and move on.
- It is a fleet-management / telematics / logistics-software player (or a truck-maker platform, or a global fleet-intelligence leader). If the name matches more than one company or product, say which ones you found and research the **fleet / logistics** one. State clearly which one you are describing.
- Find the official website first. If there is no official site, app or recent activity, say so and treat its status as unknown — do not pad the document with guesses.

## Why we are asking (so you know what matters)

We are building an AI fleet-intelligence layer for Indian fleet operators. It does not replace what a fleet already uses: it connects GPS / telematics portals (including truck-maker platforms), FASTag, VAHAN, challans, PUC and Tally, brings the data into one structure, flags exceptions, and answers plain-language questions through an assistant on web and mobile.

What we care about, in order:
1. Does [COMPETITOR NAME] read **third-party** systems, or only its own hardware? Which systems exactly, and **how** (API, webhook, file, SIM / FASTag inference, credentials-based scraping)?
2. Is its AI assistant real? What can it answer, how are answers grounded, can it take actions, which channels?
3. Indian rails — VAHAN, FASTag, e-challan, PUC, e-way bill, Tally: native, via a partner, or absent?
4. What does it cost? (per vehicle, per fleet, per integration, per user; setup; contract)
5. Is anyone really using it? (named Indian customers, reviews, volume) — or is it a demo?

## Structure of the document (use exactly this, in this order)

### 1. At a glance
- **What it is:** input → output, one sentence.
- **Third-party systems it reads:** named, with the method.
- **Strong / weak:** one line each.

### 2. Who they are
Table: company (legal name, country, founded, team size) · founders (name + prior companies) · funding · who uses it (named customers only if sourced) · reach (app downloads, vehicles tracked, headcount) · tech (AI vendors / models visible) · independent opinion (reviews, trade press — say if none).

### 3. Plans and pricing
Table: plan · price · allowance (vehicles, users, integrations) · what the plan adds. Give the original currency plus approximate INR with the conversion date. Free tier / trial, setup fee, hardware cost, contract length, what's billed on top. If there is no public price, say so — look for prices in social posts, reviews, listings, partner pages, tenders and press before giving up.

### 4. Every feature
Tables grouped by stage — **Connect** (devices, vendors, government rails, accounting, ERP), **Understand** (normalised data, scoring, trips, fuel, compliance, reports), **Act** (assistant, alerts, briefs, workflows, channels), **Business** (roles, languages, onboarding, support). Columns: feature · what it does · output · plan. Include limits (refresh rate, history window, vehicle caps).

### 5. The questions that matter
Short, evidence-backed answers:
- Third-party systems: which exactly, how, and what is the proof (docs, partner pages, demo footage, customer quotes) versus a logo wall?
- The assistant: what it answers, how it is grounded, whether it can act, channels, published accuracy or limits.
- Indian rails: native, partner or absent?
- India presence: INR price, Indian customers, languages, support.
- Real traction vs vanity claims.
- Anything in the Terms of Service or privacy policy that reveals real limits, data use or underlying vendors.

### 6. Social log
Table of their public posts / videos that reveal product, price, tier or customers: date · platform · what it shows · link. Only entries that add a fact — skip generic marketing.

### 7. Still open
Everything you could not confirm, ranked by how much it would change a buying decision.

### 8. Sources
List: URL · date accessed · **observed** / **vendor claim** / **third-party** · the key fact it supports.

Do not write a "Logix vs them" section. We do that internally.

## Where to look (go deep, not just the homepage)

- Official site: pricing, product and integration pages, help centre / docs / API reference, changelog, blog, case studies, security page, terms of service and privacy policy.
- If the site is a single-page app and looks thin, read its JavaScript bundles — they often hold copy, tier names and limits.
- App stores: version history, ratings, review text.
- Social: LinkedIn / YouTube / Instagram / X. Cover the whole posting history, not just recent posts.
- Independent: Crunchbase, Tracxn, LinkedIn (team size, funding), MCA records, trade press, G2 / Capterra / Software Suggest, Reddit, YouTube demos.
- Job postings (they reveal the real stack and priorities).
- Patents and trademarks, if any.
- If a free tier or free trial exists and you can use it without paying and without third parties' personal data, do so and record what you actually saw. Do not pay for anything, do not use fake identities, do not access anything behind someone else's login, do not call unofficial or leaked APIs.

## Rules for the writing

- Blunt and simple. "Reads 80 GPS vendors via API" — not "empowers seamless fleet intelligence". No marketing language, no stories, no filler.
- Say what goes in and what comes out. Exact vendors, exact prices, exact limits.
- Every claim gets a source link. Tag each as **observed**, **vendor claim** or **third-party**. Many "best X" guides are written by competing vendors — tag those **third-party (rival-authored)** and treat them as claims. Never present a vendor claim as fact.
- Mark anything you could not confirm with ❓ — never fill a gap with a guess. Mark confirmed items ✅.
- Each fact appears **once**. If it fits two sections, put it in one and refer to it from the other.
- Quote sparingly: short phrases only, in quotation marks, with the source link. Paraphrase everything else.
- Put the access date on every source.

## Output

One Markdown document, sections 1–8 in order, with a one-line "last updated 14 Nov 2026 · verified against: <list what you actually checked>" under the title. If you cannot finish a section, say exactly what is missing at the top instead of padding it.
