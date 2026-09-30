# Prediction as Power

**Artificial intelligence, wind, and the ordering of European electricity markets**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0004--7595--9440-A6CE39.svg)](https://orcid.org/0009-0004-7595-9440)
[![Open working paper](https://img.shields.io/badge/status-working%20paper-informational)](#19-status)

An open working paper on how artificial-intelligence wind forecasts re-order coupled European electricity markets.

**Author.** Er. Rishabh Aryan  
**Programme.** M.Tech (Artificial Intelligence and Data Science)  
**Department.** Computer Science and Engineering  
**Institution.** Indian Institute of Information Technology, Bhagalpur (Bihar), India  
**Email.** [rishabh.250201011@iiitbh.ac.in](mailto:rishabh.250201011@iiitbh.ac.in)  
**ORCID.** [https://orcid.org/0009-0004-7595-9440](https://orcid.org/0009-0004-7595-9440)  
**Repository.** [https://github.com/Rishabh-bgp/prediction-as-power](https://github.com/Rishabh-bgp/prediction-as-power)

---

## 1. Start here

If you have one minute: open the manuscript notebook (text only).

[Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb](Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb)

That file *is* the public paper. It is Markdown only. GitHub renders the sections and the equations in the browser.

The **final coded version** of the laboratory is at the repository root:

- **Final coded notebook:** [prediction_as_power_european_electricity_markets.ipynb](prediction_as_power_european_electricity_markets.ipynb)

Earlier coded drafts:

- Version 1: [notebooks/v1/prediction_as_power_european_electricity_markets.ipynb](notebooks/v1/prediction_as_power_european_electricity_markets.ipynb)
- Version 2: [notebooks/v2/prediction_as_power_european_electricity_markets.ipynb](notebooks/v2/prediction_as_power_european_electricity_markets.ipynb)

This README is the handbook around those files: why the paper exists, how the markets work, what the laboratory numbers mean, and what you may cite.

If you have ten minutes: read Sections 2–6 of this README, then the Abstract and Section I in the notebook.

If you have an hour: read the notebook through Section X and [docs/laboratory-disclaimer.md](docs/laboratory-disclaimer.md).

---

## 2. Table of contents

1. [Start here](#1-start-here)
2. [Table of contents](#2-table-of-contents)
3. [The claim in plain language](#3-the-claim-in-plain-language)
4. [Why the paper was written](#4-why-the-paper-was-written)
5. [Abstract](#5-abstract)
6. [Keywords](#6-keywords)
6a. [Invitation to European universities and research scholars](#invitation-to-european-universities-and-research-scholars)
7. [Who should read this repository](#7-who-should-read-this-repository)
8. [Who should not treat it as a trading manual](#8-who-should-not-treat-it-as-a-trading-manual)
9. [Files and what each one is for](#9-files-and-what-each-one-is-for)
9a. [Notebook versions](#9a-notebook-versions)
10. [How to read the manuscript on GitHub](#10-how-to-read-the-manuscript-on-github)
11. [How to read the manuscript on your machine](#11-how-to-read-the-manuscript-on-your-machine)
12. [Suggested reading paths](#12-suggested-reading-paths)
13. [Outline of the manuscript](#13-outline-of-the-manuscript)
14. [Institutions](#14-institutions)
15. [The model, written out](#15-the-model-written-out)
16. [What the laboratory does and does not do](#16-what-the-laboratory-does-and-does-not-do)
17. [Headline laboratory magnitudes](#17-headline-laboratory-magnitudes)
18. [Sentences you may cite, and sentences you may not](#18-sentences-you-may-cite-and-sentences-you-may-not)
19. [Status](#19-status)
20. [Related literature (entry points)](#20-related-literature-entry-points)
21. [Documentation map](#21-documentation-map)
22. [Glossary](#22-glossary)
23. [Frequently asked questions](#23-frequently-asked-questions)
24. [Citation](#24-citation)
25. [Licence and reuse](#25-licence-and-reuse)
26. [Contributing](#26-contributing)
27. [Security and data](#27-security-and-data)
28. [Contact and correspondence](#28-contact-and-correspondence)

---

## 3. The claim in plain language

Electricity in coupled Europe is no longer priced mainly by the slow economics of fuel. It is priced by *expectations of weather*.

Wind farms produce when the wind blows. Their short-run marginal cost is near zero. They sit at the bottom of the merit order. When expected wind rises, expected residual load falls, and the day-ahead price usually falls with it. When expected wind collapses on a cold, dark evening, residual load rises and the price can spike.

The day-ahead auction does not see the wind that will actually blow tomorrow. It sees a forecast. Improve the forecast and you change the stack that is committed, the flows that are scheduled, and the hours that clear negative or scarce. That is not a metaphor. It is the gate timetable of SDAC, SIDC and balancing.

Artificial intelligence enters as a second description of the same atmosphere: faster, cheaper to rerun, sometimes more accurate at 100 metres than a public IFS-style control run, and privately held. The public baseline is already socialised by transparency law. The residual around that baseline is a product. This paper names that product.

---

## 4. Why the paper was written

Three facts sat next to each other and were not being read as one fact.

First, European market coupling turned a set of national auctions into a continental machine that clears expected residual load at a common gate.

Second, wind grew large enough that forecast revisions are first-order for prices and for cross-border flows. That is documented in the empirical literature on German day-ahead and intraday prices and in work on how coupled intraday markets absorb German wind updates.

Third, operational AI weather models now sit beside physics-based NWP. Industry evaluations have started to score those models not only in metres per second but in imbalance cost.

The paper is the joint reading: prediction is part of dispatch; dispatch is part of allocation; allocation is political economy as well as statistics.

---

## 5. Abstract

European day-ahead electricity auctions clear expected residual load, not realised residual load. Wind, at near-zero short-run marginal cost, occupies the base of the merit order. A revision to the wind forecast therefore revises which conventional units are committed, which interconnectors are scheduled, and which hours clear at negative or scarcity prices. Artificial-intelligence weather models now produce a private description of that wind that can differ, hour by hour, from the public numerical-weather-prediction baseline that transparency law already socialises.

This paper treats that difference as an allocation problem rather than only a scoring problem. Single Day-Ahead Coupling is a forecast-clearing auction. Single Intraday Coupling is a market in forecast revisions. Balancing settles whatever remains after the last gate. An agent who occupies a finer filtration of weather extracts a rent that appears in the accounts as avoided imbalance and appears in the power system as the right to say which machines run.

A two-year hourly laboratory of a Germany-like zone coupled to a hydro neighbour is used to make the claim computable. An AI-style wind forecast that is about one-third more accurate than a persistent NWP-style forecast at the day-ahead gate produces a mean absolute counterfactual price shift of 12.90 EUR/MWh, reduces stylised imbalance cost on a 100 MW slice by 3.33 million EUR per year, and avoids 254 false committed hours on a 500 MW combined-cycle unit. An 8 GW downward shock to expected home-zone wind raises reconstructed price by about 12 EUR/MWh and increases stylised export. These magnitudes are laboratory objects. The institutional claim does not depend on them.

---

## 6. Keywords

Artificial intelligence; wind power forecasting; European electricity markets; merit-order effect; imbalance costs; day-ahead coupling; Single Intraday Coupling; residual load; value factor; Dunkelflaute; information; Transparency Platform.

---

## Invitation to European universities and research scholars

European universities, laboratories, and research scholars are welcome to use this working paper and the accompanying notebooks in their teaching, theses, and research, provided they cite the work and retain the MIT copyright notice. Laboratory euro figures must remain labelled as synthetic. Institutional claims about SDAC, SIDC, and balancing should be checked against current ENTSO-E and NEMO Committee documentation.

Correspondence on reuse: rishabh.250201011@iiitbh.ac.in

## 7. Who should read this repository

- Graduate students in energy systems, market design, or applied machine learning who need a compact map from weather models to gates.
- Researchers preparing an ENTSO-E estimation who want the institutional claim stated before the token is issued.
- Policy readers who need the distinction between a public baseline and a private residual.
- Examiners who want the limitations listed in one place.

---

## 8. Who should not treat it as a trading manual

Do not use this repository to size a bid. The price function is stylised. The imbalance function is stressful by design. Fuel and carbon are held constant. Flow-based Core coupling is replaced by a simple NTC. There is no intra-zonal congestion, no outage calendar, and no large-agent impact on the imbalance price. A reader who trades on Table III has misread Section IX.

---

## 9. Files and what each one is for

```
prediction-as-power/
├── Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb
├── prediction_as_power_european_electricity_markets.ipynb  ← FINAL CODED VERSION
├── notebooks/
│   ├── README.md
│   ├── v1/
│   │   ├── README.md
│   │   └── prediction_as_power_european_electricity_markets.ipynb
│   └── v2/
│       ├── README.md
│       └── prediction_as_power_european_electricity_markets.ipynb
├── README.md
├── LICENSE
├── CITATION.cff
├── CONTRIBUTING.md
└── docs/
    ├── README.md
    ├── reading-the-manuscript.md
    ├── institutional-background.md
    ├── laboratory-disclaimer.md
    └── citation-and-reuse.md
```

| File | Role |
|---|---|
| `Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb` | Public manuscript. Markdown only. No laboratory code. |
| `notebooks/v1/prediction_as_power_european_electricity_markets.ipynb` | Version 1 laboratory: first executable essay. |
| `notebooks/v2/prediction_as_power_european_electricity_markets.ipynb` | Version 2 laboratory: expanded executable essay. |
| `notebooks/README.md` | Short index of the three notebooks. |
| `prediction_as_power_european_electricity_markets.ipynb` | **Final coded version** of the laboratory (executable). |
| `README.md` | This handbook. |
| `docs/` | Institutions, reading guide, disclaimer, citation. |
| `LICENSE` | MIT. |
| `CITATION.cff` | Machine-readable citation. |
| `CONTRIBUTING.md` | How to propose a correction. |

## 9a. Notebook versions

There are three public notebook objects. They are not interchangeable.

| Object | Cells (approx.) | Code? | Use it for |
|---|---|---|---|
| **Final coded version** (`prediction_as_power_european_electricity_markets.ipynb`) | Executable laboratory | Yes | **Run this** to reproduce the coded results |
| **Manuscript** (`Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb`) | Markdown only | No | Reading the paper on GitHub; equations; references |
| **Version 1** (`notebooks/v1/…`) | 31 cells (15 code, 16 Markdown) | Yes | Original laboratory draft |
| **Version 2** (`notebooks/v2/…`) | 35 cells (15 code, 20 Markdown) | Yes | Expanded laboratory draft |

**Version 1** is the first implementation: synthetic DE-like zone, fleet power curve, NWP versus AI wind errors, merit-order diagnostics, price models, imbalance cash-flow, thermal starts, cross-border shock.

**Version 2** keeps that pipeline and adds author front matter plus a fuller written argument around the same experiments.

**Final coded version** (`prediction_as_power_european_electricity_markets.ipynb`, repository root) is the laboratory you should run if you want the coded results.

**Manuscript** is the 35-page paper converted to Markdown cells so GitHub can display it. It must not be run as a model-training notebook.

**Version 1** and **Version 2** under `notebooks/` are kept as dated drafts of that laboratory.


To run version 1 or version 2 locally:

```bash
git clone https://github.com/Rishabh-bgp/prediction-as-power.git
cd prediction-as-power
pip install numpy pandas matplotlib seaborn scikit-learn
# then open notebooks/v1/... or notebooks/v2/... and Restart & Run All
```

Results from v1 and v2 are laboratory magnitudes. Read [docs/laboratory-disclaimer.md](docs/laboratory-disclaimer.md) before citing any euro figure.

## 10. How to read the manuscript on GitHub

1. Open [Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb](https://github.com/Rishabh-bgp/prediction-as-power/blob/main/Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb).
2. Wait for Markdown and MathJax. Display equations sit in `$$` fences.
3. If the page shows raw TeX or an old revision, hard-refresh (Ctrl+Shift+R) or append `?raw=0` by simply reopening the blob URL.
4. If GitHub prints “Unable to render code block”, that is the viewer, not a corrupt file. Clone and open locally.
5. Scroll by heading: Abstract, I–X, Tables, References, Appendices.

GitHub renders inline math such as `$R_t$` and display math such as

$$
R_t = D_t - W_t - S_t.
$$

---

## 11. How to read the manuscript on your machine

```bash
git clone https://github.com/Rishabh-bgp/prediction-as-power.git
cd prediction-as-power
```

Open `Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb` in JupyterLab, Jupyter Notebook, VS Code, or nbdime. No Python package is required to *read* that file. “Restart & Run All” will not estimate German prices from it.

---

## 12. Suggested reading paths

**Market-design path.** README §§3–5, 14–15 → notebook Sections I, III, IV, VIII, X.

**Empirical path.** README §§16–18 → notebook Sections V–VII and IX → `docs/laboratory-disclaimer.md`.

**Examiner path.** notebook Section IX and Appendices Q, S, T → this README §18 → `CONTRIBUTING.md`.

**Citation path.** this README §24 → `CITATION.cff` → notebook References.

---

## 13. Outline of the manuscript

| Section | What it does |
|---|---|
| Abstract | States the institutional claim and labels the laboratory |
| I. Introduction | The inversion from fuel-priced to forecast-priced hours |
| II. Related literature | Merit order, value factors, forecast trading, EPF, AI weather, information |
| III. Institutional architecture | SDAC, SIDC, balancing, Regulation (EU) No 543/2013 |
| IV. Model | Residual load, day-ahead argument, imbalance cost, lead time, ordering |
| V. Laboratory design | Synthetic DE-like zone, power curve, two forecast colours |
| VI. Forecast skill and market objects | Lead-time ladder, correlations, value factors, Dunkelflaute |
| VII. Counterfactuals | Price shift, merchant cash-flow, thermal starts, export shocks |
| VIII. Who is ordered | Agents, design instruments, what the claim is not |
| IX. Limitations | Synthetic series and the ENTSO-E sequel |
| X. Conclusion | Separate the institution from the euros |
| References | Verified records (Sensfuß; Gürtler–Paulsen; Hirth; Pinson et al.; Boehnke et al.; Lang et al.; Lam et al.; Hardy–Finney; Aliyon–Ritvanen; Uniejewski–Ziel; Weron; Hayek; Regulation 543/2013) |
| Appendices | Worked magnitudes, a day in the life of a forecast, examiner checklist, data statement |

---

## 14. Institutions

| Institution | Typical gate | Object |
|---|---|---|
| SDAC | ~12:00 CET on $D{-}1$ | Expected residual load for day $D$ |
| SIDC | After SDAC, until close to delivery | Revisions to that expectation |
| Balancing | After the last energy gate | Remaining system imbalance |
| Transparency Platform | Continuous | Public baseline |

**Document types for a non-synthetic sequel**

| Code | Content |
|---|---|
| A.44 | Day-ahead prices |
| A.65 | Load |
| A.69 | Wind and solar forecasts |
| A.75 | Actual generation per type |

More: [docs/institutional-background.md](docs/institutional-background.md).

---

## 15. The model, written out

Demand within the hour is treated as approximately inelastic. Wind and solar enter as near-zero short-run marginal cost. Residual load is

$$
R_t = D_t - W_t - S_t.
$$

A compact price is a conventional stack plus a scarcity term in tightness:

$$
P_t = c(R_t) + \psi\left(\frac{R_t}{K_t}\right), \qquad \frac{\partial P_t}{\partial W_t} \le 0.
$$

The day-ahead auction substitutes forecasts for realisations:

$$
P^{DA}_t = c\big(\hat{D}_t - \hat{W}^{DA}_t - \hat{S}^{DA}_t\big) + \psi(\cdot) + \varepsilon_t.
$$

A merchant who sold $\hat{W}$ day-ahead and is settled on $W$ at the imbalance price faces, relative to selling $W$ at $P^{DA}$,

$$
(W - \hat{W})\big(P^{\mathrm{imb}} - P^{DA}\big).
$$

Lead time is itself a product. Let $\sigma^2(\tau)$ be wind-speed error variance at lead $\tau$. The private value of a model is the path of $\sigma^2$ from $D{-}1$ through $H{-}6$ to $H{-}1$, because each SIDC gate can capitalise a revision.

---

## 16. What the laboratory does and does not do

**Does.** Builds two years of hourly load, wind, solar, residual load and a convex price. Passes NWP-style and AI-style wind-speed errors through the same fleet power curve. Attaches a lead-time ladder. Fits reduced-form price models and swaps only the wind input. Scores merchant imbalance on a 100 MW slice. Applies a binary start rule to a 500 MW combined-cycle unit. Shocks expected home-zone wind and records stylised export to a hydro neighbour.

**Does not.** Use an ENTSO-E token. Implement Core flow-based coupling. Solve a mixed-integer unit-commitment problem. Model a farm large enough to set $P^{\mathrm{imb}}$. Give solar its own AI residual. Vary fuel or carbon. Represent storage, elastic demand, or intra-zonal congestion.

The laboratory is an argument with numbers. It is not an official impact assessment of any named vendor model.

---

## 17. Headline laboratory magnitudes

Treat every cell as a laboratory object.

| Object | Value |
|---|---|
| Mean price | 48.57 EUR/MWh |
| Negative-price hours | 19.5% |
| Corr(price, residual load) | +0.893 |
| Corr(price, wind) | −0.603 |
| Wind value factor | 0.400 |
| Solar value factor | −0.331 |
| Day-ahead wind MAE, NWP-style | 9,078 MW (12.97% of 70 GW) |
| Day-ahead wind MAE, AI-style | 5,971 MW (8.53% of 70 GW) |
| MAE reduction | 34.2% |
| Counterfactual mean \|ΔP\| | 12.90 EUR/MWh |
| 90th percentile \|ΔP\| | 30.89 EUR/MWh |
| Imbalance-cost change, 100 MW slice | −3.33 million EUR / year |
| Avoided false CCGT hours (500 MW) | 254 |
| −8 GW expected-wind shock, change in mean price | about +12 EUR/MWh |

The 25–30 percent 100-metre wind MAE figure discussed in the text is attributed to an industry evaluation of WeatherNext 3 versus IFS, not to the AIFS system paper.

---

## 18. Sentences you may cite, and sentences you may not

**May be cited as institutional or theoretical claims**

- The day-ahead auction in coupled Europe clears expected residual load.
- Wind forecast revisions are traded in SIDC and settled, if they survive, in balancing.
- The slope of price with respect to expected wind is non-positive and steeper in tight hours.
- Mean absolute error in metres per second is not a sufficient economic score.
- Public transparency socialises a baseline; private models capture a residual.
- Coupling transmits the consequences of a forecast that may not have been shared.
- Thermal start costs are part of the social bill of forecast error.

**Must not be cited as official statistics**

- Day-ahead AI wind MAE is 5,971 MW.
- Mean absolute price shift is 12.90 EUR/MWh.
- A 100 MW slice saves 3.33 million EUR per year in imbalance cost.
- The wind value factor is 0.400.
- Negative-price hours are 19.5 percent of the sample.

Full list: [docs/laboratory-disclaimer.md](docs/laboratory-disclaimer.md).

---

## 19. Status

Working paper, 2026. Open manuscript. Synthetic laboratory. Institutional descriptions follow published SDAC/SIDC and Transparency rules as understood at the time of writing and should be checked against current NEMO Committee and ENTSO-E documentation before any operational use.

---

## 20. Related literature (entry points)

These are starting citations, not a complete bibliography. The notebook reference list carries volume, pages and DOI where verified.

- Sensfuß, Ragwitz and Genoese, *Energy Policy*, 2008 — merit-order effect.
- Gürtler and Paulsen, *Energy Economics*, 2018 — wind and solar *forecasts* and German prices.
- Hirth, *Energy Economics*, 2013 — value factors.
- Pinson, Chevallier and Kariniotakis, *IEEE Trans. Power Syst.*, 2007 — imbalance-aware bidding.
- Boehnke, Kolkmann, Leisen and Weber, *IET Renew. Power Gener.*, 2024 — coupled intraday absorption of German wind updates.
- Weron, *International Journal of Forecasting*, 2014 — electricity price forecasting.
- Aliyon and Ritvanen, *Energy*, 2024 — deep learning EPF in Europe.
- Uniejewski and Ziel, *Renewable Energy*, 2026 — probabilistic load and RES as EPF features.
- Lang et al., arXiv:2406.01465, 2024 — ECMWF AIFS.
- Lam et al., *Science*, 2023 — GraphCast.
- Hardy and Finney, *Meteorological Applications*, 2025 — AI weather to 100 m wind and power.
- Hayek, *American Economic Review*, 1945 — knowledge in society.
- Regulation (EU) No 543/2013 — publication of electricity market data.

---

## 21. Documentation map

| Document | Question |
|---|---|
| [docs/README.md](docs/README.md) | What else is in `docs/`? |
| [docs/reading-the-manuscript.md](docs/reading-the-manuscript.md) | How do I open the notebook? |
| [docs/institutional-background.md](docs/institutional-background.md) | What are SDAC, SIDC and A.69? |
| [docs/laboratory-disclaimer.md](docs/laboratory-disclaimer.md) | Which euros are synthetic? |
| [docs/citation-and-reuse.md](docs/citation-and-reuse.md) | How do I cite this, and what does MIT not cover? |

---

## 22. Glossary

| Term | Meaning in this paper |
|---|---|
| Residual load | Demand minus wind minus solar |
| Value factor | Generation-weighted price divided by the time-weighted average price |
| Dunkelflaute | Dark, still period: low wind, low solar, high load |
| Filtration $F_\tau$ | Information available at lead $\tau$ |
| Public baseline | TSO / ECMWF / Transparency objects everyone can see |
| Private residual | Incremental description around that baseline |
| NWP-style regime | Persistent, larger-error wind forecast in the laboratory |
| AI-style regime | Persistent, smaller-error wind forecast in the laboratory |
| False start | Thermal unit committed on a forecast residual load that does not arrive |

---

## 23. Frequently asked questions

**Why a notebook instead of a PDF?**  
GitHub’s in-browser PDF preview failed on the LibreOffice file (“Unable to render code block”). The notebook is the readable public object.

**Why is there no code in the manuscript notebook?**  
So that GitHub renders a paper rather than a laboratory. Mixing executable cells with thirty-five pages of prose made the object harder to read and easier to break. The code is in `notebooks/v1/` and `notebooks/v2/`.

**Which notebook should I run?**  
Run the **final coded version** at the root: `prediction_as_power_european_electricity_markets.ipynb`. Use `notebooks/v1/` and `notebooks/v2/` only if you need the earlier drafts. Do not run the manuscript notebook expecting model output.

**Are the 12.90 EUR/MWh and 3.33 million EUR figures real German outcomes?**  
No. They are laboratory magnitudes. See §18.

**Does the paper claim that AIFS cuts 100 m wind MAE by 25–30 percent?**  
No. That order of improvement is taken from an industry evaluation of WeatherNext 3 versus IFS. AIFS is cited as an operational data-driven system.

**Does “prediction as power” mean abuse of dominance?**  
No. The paper is explicit: it is not a competition-law allegation. It is a description of an information rent inside a forecast-clearing market.

**Can I replace the laboratory with ENTSO-E data?**  
Yes, in a sequel. You need a Transparency token and document types A.44, A.65, A.69 and A.75. This repository does not ship that token or those extracts.

**May I fork this?**  
Yes, under MIT, with the copyright notice retained.

---

## 24. Citation

```
Aryan, R. (2026). Prediction as Power: Artificial Intelligence, Wind,
and the Ordering of European Electricity Markets. Working paper,
Department of Computer Science and Engineering, Indian Institute of
Information Technology, Bhagalpur.
https://github.com/Rishabh-bgp/prediction-as-power
ORCID: https://orcid.org/0009-0004-7595-9440
```

GitHub’s “Cite this repository” button reads [CITATION.cff](CITATION.cff).

---

## 25. Licence and reuse

Released under the [MIT License](LICENSE), copyright Er. Rishabh Aryan, 2026.

You may use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the files in this repository, provided the copyright notice and permission notice appear in all copies.

MIT covers the author’s text and documentation. It does not transfer rights in ENTSO-E or TSO data, vendor weather products, or the journal articles in the reference list.

---

## 26. Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md).

Welcome: citation corrections, clearer institutional wording, typographical fixes, documentation improvements.

Not welcome: confidential forecasts, personal data, pull requests that present laboratory euros as official statistics, or conversion of the manuscript notebook into an undocumented code dump.

---

## 27. Security and data

No credentials are stored in this repository. Do not commit Transparency Platform tokens, commercial API keys, or farm-level SCADA. If you open a sequel that uses official series, keep tokens in environment variables outside git.

---

## 28. Contact and correspondence

Er. Rishabh Aryan  
Indian Institute of Information Technology, Bhagalpur  
[rishabh.250201011@iiitbh.ac.in](mailto:rishabh.250201011@iiitbh.ac.in)  
ORCID: [0009-0004-7595-9440](https://orcid.org/0009-0004-7595-9440)
