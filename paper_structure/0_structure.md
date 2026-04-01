Looking at your draft paper and slides, here's a GitHub README-style structure outline for the China Whole County PV project:

---

# Million Dollar on the Roof: Development Effects of Solar Energy

**Burgess, Li, Van Reenen, Wang** | LSE / PKU / MIT

---

## Overview

This repository contains data, code, and outputs for a study of China's "Whole County Photovoltaic" (WCP) program (launched June 2021), estimating causal effects on solar adoption, economic activity, and air quality using difference-in-differences and spatial regression discontinuity designs.

---

## Paper Structure

### 1. Introduction
- Rise of distributed PV globally; China's dominance in solar manufacturing and installation
- The WCP program as a place-based clean energy policy
- Preview of four main findings: solar capacity (+30%), manufacturing (+2.5%), PM₂.₅ (−2%), NO₂ (−2.5%)
- Related literature: climate policy, industrial/place-based policy, solar economics, local air quality

### 2. Data and Institutional Background
- **2.1** The Whole County PV Program: design, voluntary application, 676 counties announced Sept 2021
- **2.2** Household solar systems and compensation mechanisms (on-grid, feed-in tariffs)
- **2.3** Household solar production data: ~30,000 stations, 20M+ daily observations, 3 provinces (Hebei, Henan, Shandong), 2021–2023
- **2.4** Economic, fiscal, and firm-level data: county statistics bureau, above-scale manufacturer records
- **2.5** Environmental data: satellite PM₂.₅, NO₂, O₃

### 3. Empirical Strategy
- **3.1** Identification challenge: voluntary selection into treatment; possible pre-existing differences in solar potential, economic conditions
- **3.2** Difference-in-differences: TWFE and SDID (Arkhangelsky et al. 2021); event-study and ATT specifications; province-level trends and controls; county-clustered SEs
- **3.3** Spatial regression discontinuity: signed distance to treated–untreated county borders; border-band DID as robustness; pixel-level analysis

### 4. Results
- **4.1** Predictors of policy participation: solar potential (especially minimum and summer sunlight) predicts selection; economic pre-trends do not
- **4.2** Solar installation and electricity: +34% cumulative capacity (SDID); +0.8% total electricity consumption; installation flows and stocks both respond immediately
- **4.3** Economic effects: +2.5% manufacturing value added; +2.9% above-scale firm count; +1.1% firm revenue; aggregate GDP response smaller and slower
- **4.4** Fiscal effects: +1.5% fiscal expenditure; near-zero fiscal revenue response
- **4.5** Environmental outcomes: −2.0% PM₂.₅; −2.5% NO₂ (SDID); no pre-trends
- **4.6** Spatial RD evidence: border-band DID confirms installation and pollution effects are largest near treated–untreated boundaries; no pre-period discontinuities

### 5. Model Framework
- Local electricity grid with households (solar installation decision governed by solar potential threshold) and a representative firm (electricity as essential input)
- WCP program modeled as cost reduction → lower adoption threshold → higher generation → relaxed electricity constraint → higher manufacturing output + cleaner generation mix
- Two model predictions matched to empirical findings

### 6. Conclusion
- Program substantially accelerated distributed solar diffusion
- Electricity gains translated into manufacturing growth, fiscal costs, and environmental improvements
- Distributed solar as green place-based industrial policy; importance of accounting for endogenous selection and spatial spillovers

---

## Data Sources

| Dataset | Coverage | Frequency | Notes |
|---|---|---|---|
| Proprietary solar generation data | Hebei, Henan, Shandong | Daily | ~30,000 stations, 2021–2023 |
| County economic statistics | National | Annual | GDP, manufacturing VA, fiscal accounts |
| Above-scale manufacturer records | National | Annual | Firm count, revenue |
| Electricity consumption | County | Annual | Total and household |
| Satellite PM₂.₅ | 1km grid | Annual | Aggregated to county-year |
| Satellite NO₂ | 1km grid | Annual | Aggregated to county-year |
| Satellite PV station area | 1km grid | Annual | Pixel-level capacity measure |
| Sunshine / sunlight hours | County | Annual | Used for selection analysis |
| Population density | 1km grid | Annual | From density map raster |

---

## Empirical To-Do / Open Questions

### Data
- [ ] Add census data section to Section 2 (demographics)
- [ ] Document satellite data sources more precisely: resolution, product name, processing steps
- [ ] Expand to full national sample (currently 3 provinces for solar data; county-level economic analysis can use all of China)
- [ ] Confirm sunlight data construction and source
- [ ] Build county-level subsidy policy dataset from PKULaw documents (feed-in tariff rates × installed capacity = subsidy cost estimates)

### Empirical
- [ ] Add controls to baseline SDID (currently no controls; SDID slow with controls)
- [ ] Verify robustness to alternative quarterly aggregations for installation outcomes
- [ ] Separate effects on large vs. small firms (heterogeneity within manufacturing)
- [ ] Test whether other sectors (services, agriculture) are unaffected — needed for conclusion claims
- [ ] Add ozone (O₃) results to main text environmental table (currently in slides only)
- [ ] Province-level parallel trends: raw level trends alongside event-study coefficients
- [ ] Confirm maximum sunlight claim ("varies less across locations") with evidence
- [ ] Sunlight: confirm pre-treatment levels are also different, not just trends

### Spatial Analysis
- [ ] Complete spatial RD section (currently "work in progress")
- [ ] Finalize pixel-level solar capacity raster pipeline (2018–2023)
- [ ] Address 95% empty grid issue for solar at 1km resolution
- [ ] Add spatial spillover analysis in buffer rings around treated counties

### Writing
- [ ] Add citations for local government fiscal revenue sharing (footnote in Section 4.3)
- [ ] Add legend to event-study figures
- [ ] Section 4.3 economic effects flagged as "not super convincing" — think through mechanism more carefully
- [ ] Model section: make household installation decision and firm problem connect more tightly to reduced-form magnitudes

---

## Code Structure *(placeholder)*

```
/code
  /data_prep        # raw data cleaning and merging
  /county_analysis  # SDID and TWFE regressions, event studies
  /pixel_analysis   # raster construction, spatial DID, border-band analysis
  /figures          # all figure-generating scripts
  /tables           # regression output tables

/data
  /raw              # not shared (proprietary)
  /processed        # county-panel, pixel-panel datasets

/output
  /figures
  /tables

/slides             # Beamer slides deck
/paper              # LaTeX draft
```
