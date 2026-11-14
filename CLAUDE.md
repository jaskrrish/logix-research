# Working in this repo (agents)

This is a **research** repo for Logix (Skylabs). The output is Markdown that a product team acts on. Start at [README.md](README.md).

## Read first
1. [logix/LOGIX-baseline.md](logix/LOGIX-baseline.md) — the yardstick. Statuses are ❓ until the team confirms them.
2. [context/skylabs/CONTENT_GUIDELINES.md](context/skylabs/CONTENT_GUIDELINES.md) — voice and factual standards.
3. [context/skylabs/products/LOGIX.md](context/skylabs/products/LOGIX.md) — what may and may not be claimed.

## Rules that decide most calls
- **Public repo.** Never add client names, contract values, our pricing, customer data, real fleet screenshots, delivery timelines or staffing. If a source file contains them, summarise without them or leave it out.
- **Evidence tags on every claim:** observed · vendor claim · third-party (rival-authored where true). Never present a vendor claim as fact. Mark unknowns ❓, confirmed ✅. Put an access date on every source.
- **Never mark Logix ✅ from the pitch deck.** The deck is our own marketing copy. Only the team can confirm a capability is live.
- **Don't guess to fill a gap.** A named competitor you haven't checked goes in "discovery — unverified", not in a table of facts.
- **Don't pay, don't use fake identities, don't touch anyone's login or unofficial APIs** while researching.
- Each fact appears once; link to it from elsewhere.

## How to add a competitor
Use [_templates/competitor-template.md](_templates/competitor-template.md) → `competitors/<name>/README.md` + `sources.md` (+ `evidence/`). Run the matching prompt from [research-prompts/](research-prompts/) first. Update the status in [competitors/LANDSCAPE.md](competitors/LANDSCAPE.md) and the table in [README.md](README.md).

## Stage model
Everything is compared on **Connect → Understand → Act** (+ Business, Fit) — the same three verbs the Logix deck sells. See [context/logix/business-proposal-analysis.md](context/logix/business-proposal-analysis.md#5-what-every-competitor-gets-compared-on).
