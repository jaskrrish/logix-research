# Logix — Competitor landscape (first pass, 14 Nov 2026)

> **Seed list, not research.** Every row below was found and checked on its own public site or a named third-party page on **14 Nov 2026**. Nothing here has been used, priced, or compared in depth yet. Deep write-ups come from the Argon prompts in [../research-prompts/](../research-prompts/) and land as `competitors/<name>/README.md` using [the template](../_templates/competitor-template.md).
> Tags: **vendor claim** = their own words · **third-party** = someone else's words (many are written by rival vendors — treat as claims) · ❓ = not confirmed.
> What we compare on: [the five axes](../context/logix/business-proposal-analysis.md#5-what-every-competitor-gets-compared-on) — Connect · Understand · Act · Business · Fit.

## Read this first — what the first pass changed

- **Elixia Pulse** is pitched almost word for word like Logix GPT (an AI layer over trips, invoices, GPS and rate cards, on web, phone and WhatsApp), and Elixia says it reads **80+ GPS vendors** plus Vahan, Sarathi, FASTag, Tally. Closest direct rival found.
- **Karins Fleet** is a unified FASTag + GPS + Vahan / Sarathi / e-challan dashboard — and "Karins" is also named in our deck as a system Logix connects to. Possibly both.
- **OEMs are data sources and rivals.** Tata (1M+ connected vehicles), Eicher (AI-enabled Uptime Centre, Oct 2026), BharatBenz, Mahindra and Ashok Leyland each ship their own fleet portal.
- **Global leaders ship "ask your fleet" already** (Samsara, Geotab, Motive) and expose MCP connectors, so a customer can ask Claude or ChatGPT about their own fleet data.

## Landscape

Statuses: **Not researched** · **Researching** · **Done**. Tier meanings are explained under the table.

| Name | Tier | What it is (one line) | Official site | Why it matters for Logix | Status |
|---|---|---|---|---|---|
| **Elixia** | A | AI platform for shippers, fleets and transporters (India, UAE, USA). **Track** reads GPS devices, SIM, FASTag, driver app and "existing telematics feeds"; claims **80+ GPS vendors**; **Pulse** = "the AI layer on top of your TMS". | [elixia.tech](https://www.elixia.tech/) | Same "connect everything, then ask" story as Logix. Vendor claim: 85K+ vehicles tracked, named brand customers. | Not researched |
| **Karins Fleet** | A | FASTag issuance + GPS + fuel card + Vahan / Sarathi / e-challan + Insurance on **one login**; "10 modules". | [fleet.karins.in](https://fleet.karins.in/) | Unified Indian compliance + toll view. ❓ same "Karins" as our deck p3? | Not researched |
| **Fleetx** | A | "AI-powered fleet and logistics management": GPS, trips, fuel, drivers, maintenance, EV, TMS features. Site headline: raised ₹113 Cr Series C (vendor). | [fleetx.in](https://www.fleetx.in/) | Prominent Indian fleet-software name. Rival-authored sources **disagree**: one calls it hardware-agnostic with webhook push, another says it has its own hardware ecosystem ❓ verify. | Not researched |
| **LocoNav** | A | Fleet platform with video telematics, vehicle / asset tracking, fuel, expenses. Claims 25+ industries, 50+ countries. | [loconav.com](http://loconav.com/) | Broad Indian + global player. Rival-authored sources say it can aggregate third-party trackers, and that its India business is now part of **Sensorise** — both ❓ verify (ownership change would matter). | Not researched |
| **FleetERP** | A | "Device-agnostic", **no hardware** fleet / asset software; VAHAN via "an authorised data partner"; claims a 30-day rollout. | [fleeterp.in](https://fleeterp.in/integrations/vahan) | Same "we don't replace your devices" position. Vendor claims only. | Not researched |
| **Fretron** | A | Collaborative **TMS** for manufacturers (procurement, dispatch, tracking, freight billing). "AI Supply Chain Analytics: get answers to any question using AI agents." Integrates ULIP (Sarathi, Vahan, FASTag), SAP, Oracle. | [fretron.com](https://fretron.com/) | Different buyer (shippers who hire trucks) but overlaps on "ask your data" and government rails. | Not researched |
| **Traxium** | A | Small software-first platform for Indian fleets; says it plugs into WheelsEye today, with LocoNav / Mappls / iTriangle on its roadmap; ₹2,500 / month per fleet to start (vendor). | [traxium.in](https://www.traxium.in/blog/best-fleet-management-software-india) | Closest to Logix's size and "software on top of existing trackers" model. Source is its own blog — vendor claim. | Not researched |
| **Intangles** | B | Digital-twin predictive maintenance + fuel + driver behaviour, own OBD device. | [intangles.ai](https://www.intangles.ai/) | Strong on vehicle health, which Logix pitches on p5. Own hardware. | Not researched |
| **TrackoBit** | B | White-label fleet software for GPS aggregators and resellers; AI video telematics. | [trackobit.com](https://trackobit.com/fleet-management-software) | Possible channel partner as well as competitor. | Not researched |
| **Vamosys** | B | Truck GPS + fuel-sensor monitoring, tyre management, dashcam, "FleetOS" fleet software and a driver app. Claims 10,000+ truck owners (vendor). | [vamosys.com](https://vamosys.com/) | Fuel-sensor specialist; fuel variance is one of the deck's p5 areas. | Not researched |
| **BlackBuck** | B | "India's largest digital trucking platform": FASTag, GPS, fuel cards, loads marketplace, financing. Annual report FY26: ~1 million truck operators transacting. | [blackbuck.com](https://www.blackbuck.com/) | Owns toll + fuel + GPS data for a huge base; different business model (payments-led). | Not researched |
| **WheelsEye** | B | Truck booking marketplace with GPS tracking. Site claims 20–26 lakh trucks (its pages disagree). | [wheelseye.com](https://wheelseye.com/) | GPS data source for others (Traxium plugs into it). | Not researched |
| **Tata Motors Fleet Edge** | C | OEM connected-vehicle platform. Tata's FY26 annual report: **over one million** connected vehicles. Features page offers an "API Management Solution" subscription. | [fleetedge.tatamotors.com](https://fleetedge.tatamotors.com/) | Named in our deck. Data source + rival. API route is key. | Not researched |
| **Ashok Leyland iAlert** | C | OEM telematics app / portal (Play Store: 100K+ downloads). | [Play Store listing](https://play.google.com/store/apps/details?hl=en_US&id=com.al.ialert4) | Named in our deck. API access ❓. | Not researched |
| **Mahindra iMAXX** | C | OEM telematics on BS6 trucks / buses. 2022 Mahindra blog says an "API library" is available for ERP integration. | [Mahindra blog](https://www.mahindratruckandbus.com/english/blog/all-you-need-to-know-about-mahindra-imaxx-telematics-technology.aspx) | Named in our deck. One of the few OEMs that claims an API. | Not researched |
| **Eicher (VECV): My Eicher / Eicher LIVE / Uptime NXT** | C | OEM platform; press release 13 Oct 2026: "AI enabled Uptime Centre" + GenAI "Service One"; My Eicher app connects 460,000+ vehicles (vendor). | [VECV press release](https://www.vecv.in/press-releases/eicher-trucks-buses-launches-uptime-nxt-services-powered-by-ai-enabled-uptime-centre) | Named in our deck. Shows OEMs adding AI themselves. | Not researched |
| **BharatBenz Truckonnect** | C | Daimler India OEM telematics (portal + app). Reports include a **Neutral Driving Report**. App store ratings 2.6★ (Play) / 2.0★ (App Store). | [bharatbenz.com/truckonnect](https://www.bharatbenz.com/truckonnect) | Named in our deck (as "Bharat Benz"). Already ships a feature the deck pitches. | Not researched |
| **Samsara** | D | US fleet / physical-operations platform. **Samsara Assistant**, **Agent Studio** (launched 13 Oct 2026), **Samsara MCP** (22 Sep 2026; 40+ read-only tools). | [samsara.com/…/ai-fleet-management](https://www.samsara.com/products/platform/ai-fleet-management) | Benchmark for what a mature "ask your fleet + act" looks like. | Not researched |
| **Geotab** | D | **Geotab Ace**: NL assistant inside MyGeotab; docs say it generates SQL; Gemini-based. **MCP Connector** (17 Jun 2026) for ChatGPT / Claude / Copilot. | [geotab.com/ace](https://www.geotab.com/products/ace-ai-assistant) · [developers.geotab.com](https://developers.geotab.com/ai/aiAgentAce/index.html) | Publishes a model card — best public detail on how a fleet assistant is built. | Not researched |
| **Motive** | D | **AI Answers** (27 Oct 2025): conversational analytics inside Motive Analytics. | [gomotive.com release](https://gomotive.com/motive-launches-ai-answers-the-first-conversational-ai-for-physical-operations/) | Same benchmark. | Not researched |

**Tiers.** **A** = closest: aggregates or unifies, and/or has an AI layer, for Indian fleets. **B** = Indian telematics / payments / marketplace players with their own hardware or volume. **C** = OEM platforms (our data sources and potential rivals). **D** = global leaders — benchmark for the assistant and the "act" layer.

## Integration rails — not competitors, but Logix depends on them

Detailed in [../integrations/INTEGRATION-MAP.md](../integrations/INTEGRATION-MAP.md).

| Name | What it is | Site | Why it matters |
|---|---|---|---|
| **ULIP** (Unified Logistics Interface Platform) | Government API gateway: VAHAN, SARATHI, FASTag, e-challan, e-way bill and more. Register → submit use-case → review → NDA → sandbox. | [goulip.in](https://goulip.in/) | The official route to the compliance data the deck promises. |
| **LorryCare, Masters India, PeriOne, SignCare** | Paid third-party APIs for FASTag / VAHAN / e-challan (LorryCare says its data comes from ULIP). | [lorrycare.com/api-docs](https://lorrycare.com/api-docs) · [docs.mastersindia.co](https://docs.mastersindia.co/masters-india-apis/proof-of-delivery-pod-api/fastag-api) · [perione.in](https://perione.in/services/vahan-sarathi/) · [docs.signcare.io](https://docs.signcare.io/core/api/transport/vahan-information) | Faster than ULIP onboarding, but a cost and a dependency. |
| **TallyPrime API** | Tally's XML / JSON integration with an API Explorer sandbox. | [tallysolutions.com/tallyprime-api-explorer](https://tallysolutions.com/tallyprime-api-explorer) | Route to the "Tally" in deck p3. |

## Alternatives to buying (benchmarks, no URL)

| Alternative | What to find out |
|---|---|
| Excel + a MIS / operations analyst reconciling several portals by hand | Real monthly cost of that person in Indian fleets of 20 / 100 / 500 trucks; hours spent per week. This is "the human alternative" — the benchmark Logix replaces. |
| Generic BI (Power BI, Zoho Analytics, Looker) + Copilot-style assistant | Setup effort, whether the connectors exist for Indian telematics. |
| Customer asks Claude / ChatGPT directly via a vendor's MCP (Samsara, Geotab) | Whether Indian OEM / GPS vendors will ever offer one. A cross-vendor Indian layer is the gap. |

## Discovery candidates — NOT verified

Named in the PIB press release of Oct 2022 as early **ULIP NDA signatories** (so they work with the same government data): MapMyIndia, CargoExchange, Freight Fox, Conmove, **Intugine**, Eikonatech, **Superprocure**, CargoShakti, CloudStrats, Shyplite ([PIB, 1 Oct 2022](https://www.pib.gov.in/PressReleasePage.aspx?PRID=1864095&reg=48&lang=2)). Official sites and current status ❓. **FarEye, LogiNext, Locus, Fleetio, Verizon Connect, Trimble, Webfleet** are names from general knowledge with **no check done** — they go to the discovery tier of the sweep prompt, not into the table above.
