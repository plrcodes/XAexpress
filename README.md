# XA Express (v2.1)

**Deemed-to-Satisfy Compliance Calculator for SANS 10400-XA:2026 (3rd Edition)**

XA Express is a lightweight, zero-installation, single-file web application for South African architectural professionals, energy consultants, and building control officers to verify and document **full Deemed-to-Satisfy (Clause 4.2) compliance with SANS 10400-XA:2026 (Edition 3)**.

---

## Full SANS 10400-XA:2026 (3rd Edition) Compliance Coverage

Every calculation, lookup table, and qualitative confirmation in XA Express v2.1 is aligned with **SANS 10400-XA:2026 (3rd Edition)** across all mandatory Deemed-to-Satisfy clauses (`4.2 a` through `4.2 h`):

### 1. Project Setup, Energy Zones & Annex C Cities (`Clauses 4.2, 5.1, 5.7 & Table C.1`)
- **Full South African Cities Database (390 Locations):** Includes all 389 towns from **Annex C (Table C.1)** plus Sutherland, with automatic **Energy Zone (`1–7`, `5H`)**, **Site Latitude**, and **Southern Cape Condensation Problem Area (SCCP)** lookup. Repeated town names are differentiated by province (`Heidelberg (GP/WC)`, `Middelburg (EC/MP)`), printed Table C.1 coordinate/spelling typos are corrected, and a **Custom / Manual Entry** option is included alongside a direct link to the CSIR Energy Demand Map.
- **Occupancy Classification (`Reg XA1 & Clause 4.2`):** Supports all 19 regulated occupancy classes and automatically flags all 12 exempt classes (`A5`, `B1–B3`, `D1–D4`, `J1–J4`).
- **Primary Building Orientation (`Clause 5.1 & Figure 2`) & General Building Sealing (`Clause 5.7`):** Built directly into the Project tab with Zone `5H` natural ventilation guidance and Zone `1–7` solar sector advisories.

### 2. Building Envelope (`Clauses 5.4, 5.5, 5.6 & Tables 6–9`)
- **External Walls (`Clause 5.5`, Tables 6 & 7):**
  - Interactive multi-layer assembly builder with to-scale cross-section visualizer and **Table 8** insulation material presets.
  - Automatic classification into **Heavyweight (`≥ 270 kg/m²`, Table 6)** and **Lightweight (`< 270 kg/m²`, Table 7)** walls, supporting both **Total R-value** and **Thermal Capacity–Resistance (`CR = C × R`, `80 h` / `100 h`)** compliance pathways, plus a CR-aware automatic thickness solver.
  - Dedicated **Category 1 Single-Leaf Masonry (`Clauses 3.2 & 5.5.2`, `≥ 140 mm`)** compliance mode for eligible buildings `≤ 80 m²`.
- **Roofs & Ceilings (`Clause 5.6`, Tables 8 & 9):**
  - Dual-direction Winter (Upward) and Summer (Downward) R-value verification with SANS 6946 air films (`Rse = 0.04`, `Rsi Up = 0.10`, `Rsi Down = 0.17`).
  - Full **Table 9** reflective foil support across **Flat / Skillion (`≤ 10°`)**, **Pitched Naturally Ventilated**, **Pitched Non-Ventilated**, and **Cathedral (`22° / 30° / 45°`)** roof spaces (both `0.9` standard/dusty and `0.2` sealed emissivities), with automatic **Table 9 Note 1** duplicate air-gap warnings and manual fixed R-value overrides.
  - Dedicated **Thatched Roof Assembly (`Clause 5.6.6`)** verification (`210 mm` / `175 mm` in Zone `5H` for fine grass/reed; `300 mm` for water reed) with automatic exemption of inapplicable ceiling/attic clauses.
- **Floors (`Clause 5.4`):**
  - Evaluates **insulation-only R-value** per Clause 5.4 across Slab-on-Ground and Suspended Floors, including combined **Underfloor Heating** + **Suspended Floor** targets (`1.50 m²·K/W` in Zones 1, 2, 6, 7; `1.00 m²·K/W` elsewhere) and downward heat-flow air films for heated slabs.

### 3. Fenestration, Shading & Roof Lights (`Clauses 5.2, 5.3 & Tables 3–5`)
- **Vertical Fenestration (`Clause 5.3 & Table 4`):** Independent per-storey assessment (`Clause 5.3.5 Note 2`) with area-weighted `U_avg` and separate N-sector **Shaded** vs **Unshaded** `SHGC_avg` averages (`Clause 5.3.4 d`), plus S/SE/SW SHGC exemption.
- **Shading Verification (`Clause 5.2, Table 3 & Figure 4`):** Latitude-band projection check (`P ≥ H × multiplier`), `Clause 5.2.1a` lateral extension confirmation, `Clause 5.2.1b` external shutter/screen mode, and conservative unshaded assessment whenever `P`/`H` dimensions are unverified.
- **Skylights & Roof Lights (`Clause 5.3.9 & Table 5`):** Assessed per room/space served across all Table 5 area-ratio tiers (`≤ 1.5%` through `> 10%`).
- **SCCP Condensation Enforcement (`Clause 5.3.7`):** Explicit glazing construction selector (`Single Clear`, `Single Low-E`, `Double Glazed`, `Other`) that automatically flags prohibited single Low-E glazing on both vertical fenestration and roof lights in SCCP areas.

### 4. Building Services (`Clauses 6.1, 6.2, 6.3 & Tables 10, 11, B.3`)
- **Lighting Power Density (`Clause 6.2 & Table 10`):** Space-by-space fixture schedules plus an automatic prefilled **External & Perimeter Lighting** zone (`Clause 6.2.1 Note` & `Clause 3.13` — `0 m²` outside-envelope area aggregated against internal nett floor area), **Clause 6.2.2** mixed LED/CFL + Other watt separation for `H3/H4`, and **Clause 6.2.3** occupancy/daylight sensor confirmation for non-`H3/H4` occupancies.
- **Hot Water Supply (`Clause 6.1, Reg XA2 & Table B.3`):** Automatic occupancy-synced daily demand rates (`L/person/day` at `60 °C`), 50% non-resistance heating yield verification, exposed hot water pipe insulation schedule (`SANS 10252-1`), and heat pump standards confirmations (`SANS 1687 / 1352`).
- **Mechanical Air-Conditioning / HVAC (`Clause 6.3 & Table 11`):** Minimum `COP_C` and `COP_H` verification across all Table 11 equipment classes and capacity tiers, cooling-only toggle, `≥ 10 kW` resistance-heating limit check (`Table 11 Note a`), capacity-range warnings, and natural-ventilation exemption.

### 5. Integrated Statutory Confirmations & Submission-Ready PDF Reports
- **Live Tab Status Indicators:** Every tab displays an at-a-glance status dot (**Green** compliant & confirmed, **Amber** calculation passes / awaiting confirmation, **Red** non-compliant, **Slate** exempt).
- **Per-Tab Clause Confirmations:** Context-aware statutory sign-offs (air leakage `SANS 613`, whole-unit `ANSI/NFRC 100 & 200` ratings, plastering, thermal breaks, attic sealing, moisture retention, sensors, and rating standards) sit directly on the relevant tab with automatic `N/A` detection and one-click typical defaults.
- **Single-Tab & Full Compliance Reports:** Export individual schedules or a complete submission-ready **SANS 10400-XA:2026 Deemed-to-Satisfy Compliance Report** featuring a **Master Compliance Matrix** cover page, referenced drawings, office logo, registered professional details, SACAP registration block, and municipal stamp area.

---

## Getting Started

1. Download **`xa_express_v2_1.html`** and open it directly in any modern web browser (Chrome, Edge, Firefox, or Safari).
2. No installation, server, or external tooling is required—all project inputs and office branding are saved automatically in your browser's local storage.

---

## Training & CPD Course

Want to master the technical rules, edge cases, and submission requirements behind the 3rd edition standard?

**[Enrol in the Mastering SANS 10400-XA (3rd Edition) Course on CPD Central →](https://www.cpdcentral.co.za/courses/mastering-sans-10400-XA)**

---

## Copyright & Author

© 2026 Peter le Roux. All rights reserved.  
Website: **[peterleroux.co.za](https://peterleroux.co.za)**
