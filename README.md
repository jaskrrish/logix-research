# LOGIX — Competitor & Market Research

One repository for all the research behind **Logix** (Skylabs' fleet-intelligence layer for Indian fleet operators): competitor analysis, pitch-deck analysis, the Logix baseline, and the Skylabs context. Blunt, plain-English, evidence-first — same method as the Sculpt competitor repo.

> **Visibility:** this repo was **public** when checked on 14 Nov 2026. Nothing confidential belongs in it — see [rules](#rules-for-these-docs). If it should be team-only, change it in GitHub → Settings → Danger Zone.

## Read in this order

1. [logix/LOGIX-baseline.md](logix/LOGIX-baseline.md) — what Logix **claims** vs what it can **prove**. Every comparison uses this. Statuses start as ❓ until the team confirms them.
2. [context/logix/business-proposal-analysis.md](context/logix/business-proposal-analysis.md) — what the pitch deck claims, what it leaves out, and what every competitor is compared on. Full deck text: [business-proposal-text.md](context/logix/business-proposal-text.md).
3. [competitors/LANDSCAPE.md](competitors/LANDSCAPE.md) — the verified seed list of competitors (first pass, 14 Nov 2026).
4. [integrations/INTEGRATION-MAP.md](integrations/INTEGRATION-MAP.md) — can Logix really connect to the systems the deck names?
5. [context/skylabs/](context/skylabs/) — who Skylabs is and the voice and boundary rules.

## Competitors

None researched in depth yet — each row becomes `competitors/<name>/README.md` once the research prompt has run. Full table with sources: [LANDSCAPE.md](competitors/LANDSCAPE.md).

| Tier | Who | Why they matter | Status |
|---|---|---|---|
| A — closest | [Elixia](https://www.elixia.tech/) (80+ GPS vendors + "Pulse" AI layer) · [Karins Fleet](https://fleet.karins.in/) · [Fleetx](https://www.fleetx.in/) · [LocoNav](http://loconav.com/) · [FleetERP](https://fleeterp.in/) · [Fretron](https://fretron.com/) · [Traxium](https://www.traxium.in/) | Aggregate or unify systems, and/or add an AI layer, for Indian fleets | Not researched |
| B — Indian telematics / payments | Intangles · TrackoBit · Vamosys · BlackBuck · WheelsEye | Own hardware or large volume | Not researched |
| C — truck-maker platforms | Tata Fleet Edge · Ashok Leyland iAlert · Mahindra iMAXX · Eicher · BharatBenz Truckonnect | Our data sources **and** rivals | Not researched |
| D — global benchmark | Samsara · Geotab · Motive | What a mature "ask your fleet" looks like | Not researched |
| Rails (not competitors) | ULIP · LorryCare / Masters India / PeriOne / SignCare · TallyPrime API | Official and paid routes to compliance data | Mapped, not tested |

## Folder map

```
README.md                      ← you are here
CLAUDE.md                      ← how an agent works in this repo
logix/LOGIX-baseline.md        ← our yardstick (claims vs proof)
competitors/
    LANDSCAPE.md               ← verified seed list
    <name>/                    ← created per competitor from the template (none yet)
        README.md              ← the blunt breakdown
        sources.md             ← every URL + key quotes
        evidence/              ← raw captured copy
integrations/INTEGRATION-MAP.md ← each system named in the deck: route to its data
research-prompts/              ← prompts to paste into Argon
    argon-logix-competitor-sweep.md
    argon-logix-single-competitor.md
    argon-logix-integration-feasibility.md
build-prompts/                 ← ready-to-run agent prompts for features we take from competitors (none yet)
context/
    logix/                     ← deck text + analysis
    skylabs/                   ← public-safe excerpt of the Skylabs context
_templates/competitor-template.md
.claude/skills/ · .agents/skills/ · skills-lock.json   ← agent skills (see below)
codebase/                      ← optional: a clone of the Logix code for feature checks (gitignored)
```

## How a research cycle works

1. **Baseline first.** Make sure [LOGIX-baseline.md](logix/LOGIX-baseline.md) reflects reality. Anything unconfirmed stays ❓.
2. **Pick a prompt** in [research-prompts/](research-prompts/): the sweep for breadth, the single-competitor prompt for depth, the integration prompt for "can we connect to X".
3. **Run it in Argon**, bring the output back.
4. **File it.** Competitor output → `competitors/<name>/README.md` + `sources.md` using [the template](_templates/competitor-template.md); integration output → update [INTEGRATION-MAP.md](integrations/INTEGRATION-MAP.md). Keep the raw captured pages under `evidence/`.
5. **Compare** against the baseline in section 6 of each competitor doc. Mark ✅ for Logix only where the baseline says live.
6. **Update the status** in [LANDSCAPE.md](competitors/LANDSCAPE.md) and the table above. Turn the gaps into the next prompt.

## Skills

`find-skills` helps an agent **discover and install** other agent skills (`npx skills find …`). It does not research competitors itself — the research engine here is [research-prompts/](research-prompts/). `frontend-design` is for building shareable pages (one-pagers, comparison sheets) later. Both are pinned in `skills-lock.json`.

## Rules for these docs

- Say what goes in and what comes out. "Reads 80 GPS vendors via API" — not "empowers seamless fleet intelligence".
- If we couldn't confirm it, mark ❓. Don't guess quietly.
- Tag every claim: **observed** (we saw or used it) · **vendor claim** (their own words) · **third-party** (and say **rival-authored** when a competitor wrote it). Never present a vendor claim as fact.
- Our side: **live** vs **building** vs **planned**, never blurred. A deck is not proof.
- Each fact appears once; other sections point to it. Put the access date on every source.
- **Confidential, never in this repo:** client names or logos, contract values, our pricing, customer data, screenshots of real fleet data, delivery timelines, staffing. Those stay in the private Skylabs pack.
- Don't publish these research docs outside the team without approval.
