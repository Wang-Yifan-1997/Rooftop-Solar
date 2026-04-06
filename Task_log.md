# Rooftop Solar: Detailed Progress Tracker

*Last updated: 2026-04-06*

---

## 1. Data Assembly

### Done
- **Household solar generation data:** ~30,000 stations, 20M+ daily observations, 3 provinces (Hebei, Henan, Shandong), 2021–2023 — in hand
- **County-level economic statistics:** GDP, manufacturing VA, fiscal accounts assembled
- **Satellite environmental data:** PM₂.₅, NO₂, O₃ at 1 km grid assembled and aggregated to county-year
- **Distributed solar capacity figures:** National PV construction data (2021–2025) and Power Industry Statistics (2018–2023) by province compiled; provincial stacked charts and share maps (2018, 2021, 2023) produced; focus-province charts for Hebei, Henan, Shandong done
- **Grid infrastructure briefing:** Comprehensive brief on PV transmission pathways, grid injection modes, net load impacts, regional grid structure, and cross-region transmission completed (Chinese)
- **Carbon market review:** China ETS structure, quota allocation, compliance cycle, price levels (~82.8 CNY/ton), sector coverage (power 2021 → steel/cement/aluminum 2024), comparison with EU ETS — completed

### Remaining
- [ ] **National solar data expansion:** Currently only 3 provinces; county-level economic analysis needs full national sample — expansion not yet done
- [ ] **Pixel-level solar capacity raster (2018–2023):** Pipeline incomplete; 95% of 1 km grid cells empty — needs resolution strategy (aggregation to coarser grid, or threshold-based presence indicator)
- [ ] **Sunlight hours data:** Source and construction not yet finalized; need to confirm: (a) which product, (b) whether pre-treatment levels *and* trends differ between WCP and non-WCP counties
- [ ] **County-level subsidy policy dataset:** Need to scrape PKULaw documents for feed-in tariff rates and provincial incentive policies; compute implied subsidy cost per installed kW; not started
- [ ] **Firm-level emissions data:** Compliance reports through carbon registry identified but access not secured; Shanghai Environment and Energy Exchange trading data requires data-sharing agreement — in progress
- [ ] **Census/demographic data:** Identified as needed for Section 2 baseline table; not yet assembled
- [ ] **Electricity consumption data by county:** Availability varies by grid company and provincial bureau; collection in progress, not complete
- [ ] **Carbon market firm-level data:** Trading data from Shanghai exchange requires agreements; emissions registry data access ongoing

---

## 2. Policy Analysis

### Done
- **WCP program overview:** Design, voluntary application, 676 counties announced Sept 2021, household compensation mechanisms (on-grid, feed-in tariffs) documented
- **Grid-PV institutional brief:** How distributed solar connects to grid, three injection modes, grid constraints, regional grid service boundaries — completed
- **Provincial support policy summary:** Policies for Shandong, Shaanxi, Zhejiang, Hainan, Henan, Guangdong, Hubei, Jiangsu documented (subsidies 15–30%, grid green channels, financing support)
- **WCP mechanism breakdown:** Three channels documented — (1) government coordinates scale economies at county level, (2) prioritized grid upgrades in pilot areas, (3) reduced financing costs for projects

### Remaining
- [ ] **WCP county selection criteria:** ~600 counties selected; need to document formal selection criteria (solar radiation thresholds, grid access requirements, building stock conditions) and application process — partially done, not complete
- [ ] **National policy document collection:** Full set of national-level notices (pilot list, feed-in tariff revisions, grid connection rules) not yet systematically collected
- [ ] **Local implementation variation:** Provincial and county-level rollout timing variation not yet coded into a usable dataset — in progress
- [ ] **Policy intensity index:** Quantitative measure of policy strength by county (subsidy rate × eligible capacity) not yet constructed

---

## 3. Empirical Analysis

### Done
- **Baseline SDID estimates:** Main results for solar (+34% capacity), manufacturing (+2.5% VA), PM₂.₅ (−2%), NO₂ (−2.5%) — in slides
- **Event studies:** Produced for main outcomes; shown in slides
- **Selection analysis (preliminary):** Solar potential (minimum and summer sunlight) predicts WCP selection; economic pre-trends do not — preliminary evidence

### Remaining
- [ ] **Pre-policy balance tables:** Comparison of treatment vs. control (levels, log differences, with/without controls) — assigned to RA, not yet complete
- [ ] **Solar potential replication:** Reproduce balance tables conditioning on solar potential — assigned, not yet complete
- [ ] **Controls in SDID:** Currently no controls in baseline SDID (slow with controls); need strategy (subsample, covariates as outcomes, or accept no-controls baseline)
- [ ] **Alternative quarterly aggregations:** Robustness of installation outcomes to different aggregations — not started
- [ ] **Firm heterogeneity:** Large vs. small firms; services and agriculture null tests — not started
- [ ] **O₃ results:** Currently only in slides; need to add to main text environmental table
- [ ] **Province-level raw trends:** Add level trends alongside event-study coefficients — not started
- [ ] **Sunlight claim confirmation:** Need evidence that sunlight "varies less across locations" (for conclusion in paper); need both levels and pre-trends documented

---

## 4. Mechanisms

### Done
- **Mechanism framing:** Three candidate channels identified — (1) fossil fuel power plant displacement, (2) household fuel replacement, (3) confounding policies co-launched with WCP
- **Grid transmission framework:** Regional grid boundaries, power flow patterns (sender/receiver provinces), directional corridor effects documented
- **Subsidy mechanism:** Provincial subsidy rates documented; mechanism via increased investment return articulated
- **Infrastructure mechanism:** Government grid upgrade prioritization in WCP areas documented; National Public Resource Trading Platform data identified (~78,000 grid projects, ~61,000 solar projects)
- **PM₂.₅ diffusion literature:** Papers reviewed showing diffusion ranges of 100–250 km for power plant emissions

### Remaining
- [ ] **Fossil fuel power station analysis:** Obtain province-level electricity generation by fuel type (2018–2024); test whether WCP counties show reduction in fossil generation post-2021; quantify displacement — assigned, not yet done
- [ ] **Power generation/trading tables:** Cross-province electricity generation and trading flows — assigned to RA, not complete
- [ ] **Grid upgrade data analysis:** Use National Public Resource Trading Platform data to show WCP counties received more grid investment — data identified but analysis not done
- [ ] **Financing cost mechanism:** Need data on lending rates or bond issuances for distributed solar projects in WCP vs. non-WCP counties — not started
- [ ] **Carbon market interaction:** Clarify whether power plant emissions reductions generate carbon credits; how ETS compliance interacts with WCP-driven displacement — carbon market review done, but causal linkage to WCP not yet analyzed

---

## 5. Spatial Analysis

### Done
- **Grid structure documentation:** Regional grid boundaries and cross-region transmission patterns (10%+ of electricity crosses regions) documented

### Remaining
- [ ] **Spatial RD — border-band DID:** Estimate effects restricted to counties within X km of treated–untreated borders — in progress, not complete
- [ ] **Spatial RD — pixel-level:** Signed distance to borders at pixel resolution; requires complete raster pipeline (blocked by item 1 above)
- [ ] **No pre-period discontinuity test:** Needed to validate spatial RD design — not done
- [ ] **Distance-band solar installation graphs:** Plot installation as function of distance from county center — assigned in meeting notes, not done
- [ ] **Spillover buffer rings:** Estimate effects on neighboring counties at various distances — not started

---

## 6. Writing

### Done
- **Paper structure:** Sections 1–6 outlined with key claims and findings
- **Data table:** Sources, coverage, frequency documented

### Remaining
- [ ] **Section 2:** Add WCP county selection criteria; add census baseline table; expand grid connection discussion
- [ ] **Section 3:** Sharpen parallel trends and spatial RD descriptions
- [ ] **Section 4.3 (economic effects):** Mechanism narrative flagged as "not super convincing" — needs reworking once fossil fuel and electricity access analysis is done
- [ ] **Section 5 (model):** Connect household threshold and firm problem to reduced-form magnitudes more explicitly
- [ ] **Figures:** Add legends to all event-study figures; finalize all main table formatting
- [ ] **Citations:** Fiscal revenue sharing footnote; carbon market literature (top NBER/CEPR papers + Chinese journals)
- [ ] **Introduction:** Full draft not yet written; related literature section needs expansion

---

## Summary Table

| Workstream | Status |
|---|---|
| Solar/economic/environmental data (3 provinces) | Done |
| Distributed solar capacity figures | Done |
| Grid + carbon market institutional background | Done |
| Provincial policy mapping | Done |
| Baseline SDID estimates | Done |
| National data expansion | In progress |
| Pixel raster pipeline | In progress |
| Policy document collection & intensity index | In progress |
| Firm-level emissions data access | In progress |
| Pre-policy balance tables | In progress (RA) |
| Solar potential selection analysis | In progress (RA) |
| Fossil fuel displacement analysis | In progress (RA) |
| Spatial RD (border-band) | In progress |
| County subsidy dataset | Not started |
| Firm heterogeneity / sector null tests | Not started |
| Spillover buffer rings | Not started |
| Full paper draft | Not started |
