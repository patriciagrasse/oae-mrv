# OAE Credit Decomposition Dashboard

Interactive supplementary figure for:

> **Non-Point Source Pollution Regulation as a Monitoring, Reporting, and Verification Framework for Ocean Alkalinity Enhancement: Theory and Application**
> *Submitted to Environmental Research Letters*

---

## What this is

This dashboard is a single-page interactive figure accompanying the paper. It shows how gross modelled carbon removal x̂ is decomposed into verified carbon credits under two approaches:

- **Current Isometric approach** — both environmental stochasticity (σₑ) and measurement/model uncertainty (σₘ) are deducted from x̂ as per-tonne haircuts before any credits are issued.
- **NPSP option (c)** — based on Segerson (1988) non-point source pollution incentive theory. σₑ is still deducted from the marginal credit rate, because it is genuinely irreducible and the operator must bear it. σₘ is managed instead through a threshold gate x̄: the operator receives no marginal credits if x̂ does not clearly exceed x̄, but once that bar is cleared, σₘ no longer reduces the per-tonne credit rate. A lump-sum k compensates fixed entry costs independently of removal volume.

The key result: for a project where measurement and model uncertainty account for β = 10% of gross removal, NPSP option (c) recovers β·x̂ additional credits per deployment without reducing environmental integrity.

---

## Case study

**Planetary Technologies — Tufts Cove, Halifax Harbour, Nova Scotia**

In June 2025, Isometric issued 625 verified CDR credits from this project — the world's first independently certified ocean alkalinity enhancement (OAE) credits. The three-step MRV protocol employed (outfall monitoring → dissolution verification → coupled ROMS/ECCO ocean model) maps structurally onto the Segerson NPSP framework evaluated here.

Baseline parameter values in the figure (α = 8%, β = 10%, LCA = 4%) are illustrative and consistent with the Tufts Cove uncertainty budget reported in Isometric (2025b).

---

## How to use the figure

Three sliders control the decomposition:

| Slider | Symbol | What it represents |
|--------|--------|--------------------|
| Environmental stochasticity | α (σₑ) | Irreducible year-to-year variation in air-sea CO₂ uptake driven by wind speed, mixed-layer depth, sea surface temperature, and biological feedbacks |
| Measurement & model uncertainty | β (σₘ) | Reducible uncertainty from feedstock characterisation, dosing instrumentation, and ocean model parameterisation (ROMS/ECCO calibration) |
| LCA emissions | — | Life-cycle CO₂ emissions from feedstock production, transport, and site operations, subtracted from gross removal |

The dashed threshold line x̄ moves as α and LCA change. Under NPSP option (c), this line is the gateway: projects that clear it receive full marginal credits net of σₑ; projects that do not receive only the lump-sum k.

---

## Equations

**Isometric current approach (eq. 10)**

```
C_Isometric = (1 − α − β) · x̂ − LCA
```

**NPSP option (c) (eq. 11)**

```
C_NPSP = (1 − α) · x̂ · 1[x̂ > x̄] + k − LCA
```

**Credit gain from switching to option (c)**

```
Gain = β · x̂
```

---

## Files

| File | Description |
|------|-------------|
| `index.html` | Self-contained interactive dashboard — no build step, no dependencies beyond Google Fonts |
| `README.md` | This file |
| `figure2_npsp_oae.png` | Static black-and-white version of Figure 2 (NPSP causal chain mapped to Tufts Cove MRV protocol), 300 dpi, for inclusion in the manuscript |

---

## Hosting

The dashboard is designed for GitHub Pages. To deploy:

1. Push `index.html` and `README.md` to the root of a public GitHub repository.
2. Go to **Settings → Pages → Source** and select `main` branch, `/ (root)`.
3. The page will be live at `https://yourusername.github.io/repository-name/` within ~60 seconds.

No build tools, compilers, or server configuration required.

---

## Key references

- Segerson K 1988 Uncertainty and incentives for nonpoint pollution control. *Journal of Environmental Economics and Management* **15** 87–98
- Ho D T, Bopp L, Palter J B et al 2023 Monitoring, reporting, and verification for ocean alkalinity enhancement. *State Planet* 2-oae2023-12. https://doi.org/10.5194/sp-2-oae2023-12-2023
- Halloran P R et al 2025 Seawater carbonate chemistry based CDR: towards commonly agreed principles for MRV. *Frontiers in Climate* **7** 1487138. https://doi.org/10.3389/fclim.2025.1487138
- Fennel K, Long M C et al 2023 Modelling considerations for OAE research. *State Planet* 2-oae2023-9. https://doi.org/10.5194/sp-2-oae2023-9-2023
- Isometric 2025b How the world's first OAE credits were quantified. https://webflow.isometric.com/writing-articles/quantifying-the-worlds-first-oae-credits
- Wang H et al 2025 Regional ocean modelling of OAE in Halifax Harbour. *Earth's Future*. https://doi.org/10.1029/2024EF005463

---

## Licence

Code: MIT. Paper content and figure captions: © the authors. All rights reserved pending journal publication.
