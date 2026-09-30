# Prediction as Power

**Artificial intelligence, wind, and the ordering of European electricity markets**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0004--7595--9440-A6CE39.svg)](https://orcid.org/0009-0004-7595-9440)
[![Open working paper](https://img.shields.io/badge/status-working%20paper-informational)](#status)

Open working paper by **Er. Rishabh Aryan**  
M.Tech (Artificial Intelligence and Data Science)  
Department of Computer Science and Engineering  
Indian Institute of Information Technology, Bhagalpur (Bihar), India

- Institutional email: [rishabh.250201011@iiitbh.ac.in](mailto:rishabh.250201011@iiitbh.ac.in)
- ORCID: [0009-0004-7595-9440](https://orcid.org/0009-0004-7595-9440)

This repository publishes the manuscript in a form GitHub can render: a Markdown-only Jupyter notebook. It also holds documentation, a citation file, and the MIT licence.

---

## Table of contents

1. [Thesis](#thesis)
2. [Abstract](#abstract)
3. [Who this is for](#who-this-is-for)
4. [Files in this repository](#files-in-this-repository)
5. [How to read the manuscript on GitHub](#how-to-read-the-manuscript-on-github)
6. [How to read the manuscript locally](#how-to-read-the-manuscript-locally)
7. [Outline of the paper](#outline-of-the-paper)
8. [Institutions the argument uses](#institutions-the-argument-uses)
9. [Core equations](#core-equations)
10. [Laboratory magnitudes (with disclaimer)](#laboratory-magnitudes-with-disclaimer)
11. [What this repository is not](#what-this-repository-is-not)
12. [Documentation map](#documentation-map)
13. [Citation](#citation)
14. [Licence and reuse](#licence-and-reuse)
15. [Contributing](#contributing)
16. [Status](#status)
17. [Contact](#contact)

---

## Thesis

Classical industrial organisation treats market power as the ability to move price by withholding quantity. In a wind-rich, coupled European electricity market a second channel exists: the ability to occupy the information set on which the market is cleared.

Wind is unobserved at the day-ahead gate. What is sold is a forecast. Single Day-Ahead Coupling (SDAC) therefore clears *expected* residual load. Single Intraday Coupling (SIDC) trades revisions to that expectation. Balancing prices whatever remains after the last gate. An agent who holds a finer description of wind than the public numerical-weather-prediction baseline can trade the revision before it becomes imbalance. That rent looks, in the accounts, like avoided imbalance. It looks, in the power system, like the right to say which machines run.

Artificial-intelligence weather models change the distribution of that description. They do not repeal physics. They change who sees a usable 100-metre wind field, at what lead time, and at what error.

---

## Abstract

European day-ahead electricity auctions clear expected residual load, not realised residual load. Wind, at near-zero short-run marginal cost, occupies the base of the merit order. A revision to the wind forecast therefore revises which conventional units are committed, which interconnectors are scheduled, and which hours clear at negative or scarcity prices.

This paper treats the difference between a public NWP baseline and a finer AI description of wind as an allocation problem rather than only a scoring problem. A two-year hourly laboratory of a Germany-like zone coupled to a hydro neighbour is used to make the claim computable. Laboratory magnitudes (price shifts, imbalance cash-flow, avoided thermal starts, cross-border shocks) are synthetic and must not be cited as official ENTSO-E or German statistics. The institutional claim does not depend on them: in this market, prediction is part of dispatch.

**Keywords.** Artificial intelligence; wind power forecasting; European electricity markets; merit-order effect; imbalance costs; day-ahead coupling; Dunkelflaute; information.

---

## Who this is for

- Readers who want the working paper without a PDF previewer.
- Students of electricity-market design who need a map of SDAC, SIDC and balancing as *forecast institutions*.
- Researchers who will replace the synthetic laboratory with Transparency Platform series (document types A.44, A.65, A.69, A.75).
- Practitioners who need the disclaimer on what the euro figures are not.

---

## Files in this repository

| Path | Role |
|---|---|
| [Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb](Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb) | **Canonical manuscript.** Markdown cells only. Title, author, abstract, Sections I–X, tables, references, appendices. Equations in LaTeX. |
| [prediction_as_power_european_electricity_markets.ipynb](prediction_as_power_european_electricity_markets.ipynb) | Companion notebook if present. Not a substitute for the manuscript file above. |
| [docs/](docs/README.md) | Institutional background, reading guide, laboratory disclaimer, citation note. |
| [CITATION.cff](CITATION.cff) | Machine-readable citation for GitHub and reference managers. |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to propose corrections. |
| [LICENSE](LICENSE) | MIT License. |

The canonical manuscript notebook contains **no executable laboratory code**. That is deliberate. GitHub failed to preview the PDF; the notebook exists so the *text of the paper* can be read in the browser.

---

## How to read the manuscript on GitHub

1. Open [Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb](Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb).
2. Wait for GitHub to render Markdown and MathJax.
3. If equations appear as raw `$...$` or an old revision appears, hard-refresh the page (Ctrl+Shift+R).
4. Use the cell headings (I. Introduction through Appendix V) as a table of contents.

GitHub’s notebook viewer typesets:

- inline mathematics: `$R_t$`
- display mathematics: `$$ ... $$`

If a file page ever shows “Unable to render code block”, that message is a viewer fault. Clone the repository and open the notebook locally.

---

## How to read the manuscript locally

```bash
git clone https://github.com/Rishabh-bgp/prediction-as-power.git
cd prediction-as-power
```

Open `Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb` in JupyterLab, Jupyter Notebook, VS Code, or any `.ipynb` viewer.

No Python packages are required to *read* the manuscript notebook. Do not expect “Run All” to estimate a market model from that file; the cells are prose.

---

## Outline of the paper

| Section | Contents |
|---|---|
| I. Introduction | Sequential markets; prediction as occupancy of an information set |
| II. Related literature | Merit-order effect; value factors; forecast trading; EPF; AI weather; information as infrastructure |
| III. Institutional architecture | SDAC, SIDC, balancing, Regulation 543/2013 |
| IV. Model | Residual load, day-ahead argument, imbalance cost, lead time, ordering |
| V. Laboratory design | Synthetic DE-like zone, power curve, two forecast regimes |
| VI. Forecast skill and market objects | Lead-time ladder, value factors, Dunkelflaute |
| VII. Counterfactuals | Price models, merchant imbalance, thermal starts, cross-border shocks |
| VIII. Who is ordered | Agents, design instruments, limits of the claim |
| IX. Limitations and a non-synthetic sequel | What to replace with ENTSO-E series |
| X. Conclusion | Institutional claim separated from laboratory euros |
| References | Verified bibliographic records |
| Appendices | Magnitudes, worked day, public baseline versus private residual, examiner checklist |

---

## Institutions the argument uses

| Institution | Gate / role | What is priced |
|---|---|---|
| SDAC | About 12:00 CET on $D{-}1$ | Expected residual load |
| SIDC | Continuous plus discrete intraday auctions | Forecast revisions |
| Balancing | After the last energy gate | Remaining system imbalance |
| Transparency Platform | Continuous publication | Public baseline (prices, load, RES forecasts, generation) |

Transparency law socialises a baseline. Private AI models capture a residual: faster inference, farm-level power curves, availability. Publishing another official *point* forecast is not the same as publishing an ensemble of residual load.

Further detail: [docs/institutional-background.md](docs/institutional-background.md).

---

## Core equations

Residual load and a compact price:

$$
R_t = D_t - W_t - S_t
$$

$$
P_t = c(R_t) + \psi\left(\frac{R_t}{K_t}\right), \qquad \frac{\partial P_t}{\partial W_t} \le 0
$$

Day-ahead argument (forecasts, not realisations):

$$
P^{DA}_t = c\big(\hat{D}_t - \hat{W}^{DA}_t - \hat{S}^{DA}_t\big) + \psi(\cdot) + \varepsilon_t
$$

Imbalance cost relative to selling realised wind at the day-ahead price:

$$
(W - \hat{W})\big(P^{\mathrm{imb}} - P^{DA}\big)
$$

These expressions are defined in Section IV of the notebook.

---

## Laboratory magnitudes (with disclaimer)

The following numbers appear in the manuscript. They come from a synthetic hourly generator. **They are not official German, ENTSO-E, or ACER statistics.**

| Object | Laboratory value |
|---|---|
| Mean price | 48.57 EUR/MWh |
| Negative-price hours | 19.5 percent of hours |
| Correlation of price with residual load | +0.893 |
| Wind value factor | 0.400 |
| Solar value factor | −0.331 |
| Day-ahead wind MAE, NWP-style | 9,078 MW (12.97 percent of 70 GW) |
| Day-ahead wind MAE, AI-style | 5,971 MW (8.53 percent of 70 GW) |
| Reduction | 34.2 percent |
| Counterfactual mean absolute price shift | 12.90 EUR/MWh |
| Ninetieth percentile of that shift | 30.89 EUR/MWh |
| Stylised imbalance-cost change on a 100 MW slice | −3.33 million EUR per year |
| Avoided false committed hours, 500 MW CCGT | 254 |

Cite the *sign and the mechanism*. Do not cite the euros as measured German market outcomes. Full wording: [docs/laboratory-disclaimer.md](docs/laboratory-disclaimer.md).

---

## What this repository is not

- It is not an official impact assessment of AIFS, GraphCast, or WeatherNext.
- It is not a live feed of ENTSO-E data.
- It is not a trading signal.
- It is not a claim of abuse of dominance under competition law.
- The manuscript notebook is not a training pipeline and does not require GPU hardware.

---

## Documentation map

| Document | Question it answers |
|---|---|
| [docs/README.md](docs/README.md) | Index of the `docs/` folder |
| [docs/reading-the-manuscript.md](docs/reading-the-manuscript.md) | How to open and navigate the notebook |
| [docs/institutional-background.md](docs/institutional-background.md) | SDAC, SIDC, balancing, document types A.44 / A.65 / A.69 / A.75 |
| [docs/laboratory-disclaimer.md](docs/laboratory-disclaimer.md) | Which sentences may be cited, and which may not |
| [docs/citation-and-reuse.md](docs/citation-and-reuse.md) | Licence scope and citation format |

---

## Citation

Plain text:

```
Aryan, R. (2026). Prediction as Power: Artificial Intelligence, Wind,
and the Ordering of European Electricity Markets. Working paper,
Department of Computer Science and Engineering, Indian Institute of
Information Technology, Bhagalpur.
https://github.com/Rishabh-bgp/prediction-as-power
ORCID: https://orcid.org/0009-0004-7595-9440
```

GitHub and many reference managers will read [CITATION.cff](CITATION.cff) automatically (“Cite this repository”).

---

## Licence and reuse

The repository is released under the [MIT License](LICENSE).

You may copy, modify, merge, publish, and distribute the files in this repository, provided the copyright notice and permission notice are included.

The licence covers the author’s text and documentation. It does not transfer rights in:

- ENTSO-E or TSO data
- vendor weather products
- third-party journal articles listed in the reference list

---

## Contributing

Corrections to citations, institutional descriptions, and typographical errors are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

Do not add confidential commercial forecasts or personal data. Do not present laboratory euros as official market statistics.

---

## Status

Working paper, 2026. The public object is the manuscript notebook. Laboratory magnitudes remain synthetic until a sequel is estimated on Transparency Platform series.

---

## Contact

Er. Rishabh Aryan  
Indian Institute of Information Technology, Bhagalpur  
[rishabh.250201011@iiitbh.ac.in](mailto:rishabh.250201011@iiitbh.ac.in)  
[ORCID 0009-0004-7595-9440](https://orcid.org/0009-0004-7595-9440)
