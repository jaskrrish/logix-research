# Integration map — can Logix really connect to what the deck names?

> First pass, 14 Nov 2026. The deck's whole promise is "connects to the systems you already use" (p3, p4). This file lists each named system, the route we found to its data, and what's still unknown. Nothing here was tested by us — we read public pages.
> Tags: **vendor claim** · **official** (government or regulator) · **third-party** · ❓ = not confirmed. Fill the last column as the team confirms what's built.
> To research any row in depth, run [argon-logix-integration-feasibility.md](../research-prompts/argon-logix-integration-feasibility.md).

## Systems named in the deck (p3)

### GPS and telematics platforms

| System | Route to data we found | Evidence | Open questions | Built? |
|---|---|---|---|---|
| **Tata Motors — Fleet Edge** | Features page: "Subscribe to **API Management Solution** to receive data about your vehicle in real time." | vendor claim — [fleetedge.tatamotors.com/features](https://fleetedge.tatamotors.com/features) (accessed 14 Nov 2026) | Price; who can subscribe (owner, or a third party with the owner's consent); fields; rate limits | ❓ |
| **Ashok Leyland — iAlert** | Customer app / portal. No API found in the search. | vendor claim — [Play Store](https://play.google.com/store/apps/details?hl=en_US&id=com.al.ialert4) | API exists? Or only login-based access? | ❓ |
| **Mahindra — iMAXX** | 2022 Mahindra blog: "**API library** available for easy integration with the legacy / ERP systems at the client's end." Position sent every 10 s (vendor claim). | vendor claim — [Mahindra Truck & Bus blog, 25 Nov 2022](https://www.mahindratruckandbus.com/english/blog/all-you-need-to-know-about-mahindra-imaxx-telematics-technology.aspx) | Still true in 2026? Docs, cost, access | ❓ |
| **Eicher (VECV) — My Eicher / Eicher LIVE** | Customer app + portal. No API found in the search. | vendor claim — [VECV, Oct 2026](https://www.vecv.in/press-releases/eicher-trucks-buses-launches-uptime-nxt-services-powered-by-ai-enabled-uptime-centre) | API exists? | ❓ |
| **BharatBenz — Truckonnect** | Customer portal + app (location, fuel, AdBlue, DTCs, reports). No API found. | vendor claim — [bharatbenz.com/truckonnect](https://www.bharatbenz.com/truckonnect) | API exists? | ❓ |
| **Third-party GPS vendors** (deck: "five or more GPS platforms") | Elixia says it normalises **80+** GPS / sensor / dashcam vendors; Traxium says it plugs into WheelsEye; Fleetx is described as taking "webhook push from many trackers" by a rival guide. | vendor claim · third-party (rival-authored) — see [LANDSCAPE.md](../competitors/LANDSCAPE.md) | Which vendors our first customers actually use; whether they publish APIs | ❓ |

**Pattern:** only two OEMs (Tata, Mahindra) advertise an integration route in the public pages we found. For Ashok Leyland, Eicher and BharatBenz the public material shows apps and portals only. If those APIs don't exist, the options are customer-granted credentials with unofficial access (legal and stability risk ❓) or data exports. The deck says "connects to each platform" — this is the biggest feasibility question in the file.

### Compliance, toll, operations and accounts

| System | Route to data we found | Evidence | Open questions | Built? |
|---|---|---|---|---|
| **VAHAN** (vehicle registry) | **Official:** ULIP gateway (MoRTH VAHAN is one of the integrated systems). **Paid resellers:** LorryCare (2 credits / call), Masters India, PeriOne, SignCare. Fields incl. insurance, fitness, pollution certificate, permit, tax, RC status. | official — [goulip.in](https://goulip.in/) · third-party — [LorryCare](https://lorrycare.com/api-docs), [SignCare](https://docs.signcare.io/core/api/transport/vahan-information) (accessed 14 Nov 2026) | ULIP approval timeline; reseller cost per vehicle per month; are customer-owned vehicles or only any vehicle queryable? | ❓ |
| **FASTag** (toll) | **Official:** ULIP lists IHMCL FASTag and toll-plaza tariffs. **Resellers:** same four. Crossings only for the **last 72 hours**; each crossing = plaza, time, direction. | official — [goulip.in](https://goulip.in/) · third-party — [Masters India](https://docs.mastersindia.co/masters-india-apis/proof-of-delivery-pod-api/fastag-api), [SignCare](https://docs.signcare.io/core/api/transport/fastag-information) | 72-hour window means Logix must **store** history itself to show toll over time; toll *billing* (what the fleet paid) is a different source — issuing bank / fuel-card portals ❓ | ❓ |
| **Challan** (e-challan) | **Official:** ULIP lists E-Challan. **Resellers:** same four (pending and disposed challans). | official — [goulip.in](https://goulip.in/) · third-party — [Masters India](https://docs.mastersindia.co/masters-india-apis/proof-of-delivery-pod-api/vehicle-e-challan) | Refresh frequency; legal limits on re-use | ❓ |
| **PUC** (pollution certificate) | No separate source found. The certificate number and validity appear as a **field inside VAHAN RC data** per reseller docs; Karins says its Vahan module alerts on expiring fitness / PUC. | third-party — [LorryCare](https://lorrycare.com/api-docs) · vendor claim — [fleet.karins.in](https://fleet.karins.in/) | Is the VAHAN field complete and current? Is there an official PUC database API? | ❓ |
| **Tally** (accounts) | TallyPrime has XML and JSON integration with a free **API Explorer**; Educational Mode needs no licence. | vendor — [tallysolutions.com/tallyprime-api-explorer](https://tallysolutions.com/tallyprime-api-explorer) | How Logix would reach a Tally that sits on the customer's own machine (connector, export or hosted) ❓; TallyPrime vs older Tally ERP 9 customers ❓ | ❓ |
| **Karins** | Karins Fleet is a unified FASTag / GPS / fuel card / compliance platform. Whether it has an API for third parties is ❓. Also a **competitor** — see [LANDSCAPE.md](../competitors/LANDSCAPE.md). | vendor claim — [fleet.karins.in](https://fleet.karins.in/) | Same "Karins"? Partner or rival? | ❓ |
| **Custom ERP** | Per customer. Fretron and Elixia list SAP / Oracle connectors; a custom one means a custom integration each time. | vendor claim | Which customer ERPs; effort per integration | ❓ |
| **e-way bill** (not in the deck) | Available via ULIP and the same resellers. Not mentioned in deck, but fleets live by it. | official — [goulip.in](https://goulip.in/) | Add to the pitch? | — |

## ULIP in one box (the official route for VAHAN, FASTag, e-challan, Sarathi)

| | |
|---|---|
| What | A government API gateway run by NICDC Logistics Data Services Ltd. under the National Logistics Policy; launched 17 Sep 2022. Homepage: 14 ministries, 50 systems, 141 APIs. |
| Who can join | Any registered company. PIB, Mar 2023: 400+ companies registered in 6 months; TCIL, Jun 2026: 1,600+ registered. |
| Process | Register at goulip.in → submit a use-case → review → sign an NDA → sandbox → production. A third-party how-to says use-case review takes 3–5 working days and the NDA is on ₹100 stamp paper, signed and posted ❓ (not from the official site — verify). |
| Data protection | Homepage states ULIP "neither receives nor shares unmasked personally identifiable information". |
| Why it matters | If Logix registers its own ULIP access it avoids per-call reseller fees, but takes on the NDA, use-case limits and data-retention rules. If it uses a reseller, it's faster to start but costs per lookup and adds a dependency. A decision for the team. ❓ |
| Sources | [goulip.in](https://goulip.in/) (accessed 14 Nov 2026) · [PIB 24 Mar 2023](https://www.pib.gov.in/PressReleasePage.aspx?PRID=1910298&lang=2&reg=48) · [TCIL, Jun 2026](https://tcil.com/wp-content/uploads/2026/07/ULIP-Building-Indias-Digital-Backbone-for-Integrated-Logistics_1.pdf) · [NirmanKit how-to (third-party)](https://www.nirmankit.in/learn/ulip-api-integration-how-to) |

## What this changes for the pitch

1. "Connects to **most** fleet dashboards" (p4) is not supported by anything public we found. Safer: name the integrations that are really built, and say how new ones get added.
2. The compliance and toll promises are the **most feasible** (official gateway + resellers). OEM portals are the **least certain**.
3. Toll history needs Logix's own storage: FASTag lookups only cover 72 hours.
4. "Payment mismatches" (p5, p8) has no source named anywhere. Fuel card? FASTag issuer? Tally vouchers? ❓
