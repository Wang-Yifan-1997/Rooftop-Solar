# Rooftop Solar: Project Roadmap

## Overview

This project studies China's **Whole County Photovoltaic (WCP) program** (announced September 2021, 676 counties), estimating causal effects on solar adoption, manufacturing activity, and air quality. The core identification strategy uses difference-in-differences (TWFE and SDID) and spatial regression discontinuity at treated–untreated county borders.

**Key findings (current estimates):** Solar capacity +30%, manufacturing value added +2.5%, PM₂.₅ −2%, NO₂ −2.5%.

---

## Workstream 1 — Data

**Goal:** Assemble a clean, documented county-panel dataset covering solar generation, economic outcomes, environmental outcomes, and policy variables.

- [ ] **Solar data:** Finalize pixel-level solar capacity raster pipeline (2018–2023); address sparse coverage at 1 km resolution; confirm construction of installed capacity from satellite PV area
- [ ] **Economic data:** Confirm coverage and cleaning of county-level GDP, manufacturing VA, fiscal accounts, and above-scale firm records (national sample, not just 3 provinces)
- [ ] **Environmental data:** Add ozone (O₃) as third environmental outcome; document satellite PM₂.₅ and NO₂ product names, resolution, and processing steps
- [ ] **Solar potential (selection variable):** Finalize sunlight hours data construction; document source; confirm both levels and pre-trends differ between treated and untreated counties
- [ ] **Policy dataset:** Build county-level subsidy dataset from PKULaw documents (feed-in tariff rates, provincial incentive policies, policy intensity index)
- [ ] **Census/demographic data:** Add to Section 2 as baseline characteristics; needed for balance checks and heterogeneity

---

## Workstream 2 — Empirical Analysis

**Goal:** Produce a complete set of credible causal estimates covering the main outcomes, with robustness checks and heterogeneity.

- [ ] **Main regressions:** SDID and TWFE estimates for solar, economic, and environmental outcomes; add controls to baseline SDID
- [ ] **Event studies:** Finalize event-study figures for all outcomes; add province-level raw trends alongside coefficients; add legends
- [ ] **Spatial RD:** Complete border-band DID and pixel-level spatial discontinuity; show no pre-period discontinuities
- [ ] **Heterogeneity:** Separate effects on large vs. small firms; test null effects for services and agriculture
- [ ] **Robustness:** Alternative quarterly aggregations for installation; verify sunlight as the dominant selection predictor

---

## Workstream 3 — Mechanisms

**Goal:** Explain *how* WCP caused manufacturing and environmental effects, tying reduced-form results to credible mechanisms.

- [ ] **Solar → emissions channel:** Quantify fossil fuel power plant displacement using provincial generation mix data; test whether emissions reductions are concentrated near WCP counties
- [ ] **Solar → manufacturing channel:** Establish electricity constraint story: WCP counties received grid upgrades and cheaper electricity → firm expansion
- [ ] **Subsidy mechanism:** Map provincial subsidy policies (0.1 CNY/kWh range); estimate fiscal cost of program per unit of capacity
- [ ] **Financing mechanism:** Assess whether WCP designation reduced borrowing costs for distributed solar projects
- [ ] **Carbon market interaction:** Clarify whether emissions reductions interact with China's ETS (power sector covered since 2021)

---

## Workstream 4 — Spatial Analysis

**Goal:** Document spatial extent of effects and rule out cross-county spillovers as a confound.

- [ ] **Distance-band graphs:** Plot solar installation density as function of distance from county centroid; identify spatial decay
- [ ] **Grid transmission analysis:** Map regional grid boundaries; test whether effects are contained within grid service areas
- [ ] **Spillover rings:** Add buffer-ring analysis around treated counties to assess positive or negative spillovers on neighbors

---

## Workstream 5 — Writing and Paper

**Goal:** Produce a complete draft ready for seminar circulation.

- [ ] **Section 2 (Background):** Add WCP county selection criteria and application process; add census baseline table; add grid connection institutional details
- [ ] **Section 3 (Strategy):** Sharpen parallel trends discussion; add spatial RD design description
- [ ] **Section 4.3 (Economic effects):** Strengthen mechanism narrative connecting electricity access to manufacturing — currently flagged as "not super convincing"
- [ ] **Section 5 (Model):** Make household adoption threshold and firm problem connect more tightly to reduced-form magnitudes
- [ ] **Figures/tables:** Add legends to all event-study figures; finalize formatting for all main tables
- [ ] **Citations:** Add citations for fiscal revenue sharing (Section 4.3 footnote); update literature review with top carbon market papers

---

## Immediate Priorities (Next 2 Weeks)

1. Finalize pre-policy balance tables (levels, log differences, with/without controls)
2. Complete fossil fuel generation mechanism analysis
3. Close out solar potential/selection analysis
4. Draft spatial RD section
5. Circulate updated event-study figures with legends and province-level trends
