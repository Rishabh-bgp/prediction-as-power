# Prediction as Power

**Artificial intelligence, wind, and the ordering of European electricity markets**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0004--7595--9440-A6CE39.svg)](https://orcid.org/0009-0004-7595-9440)

Open working paper by **Er. Rishabh Aryan**, M.Tech (Artificial Intelligence and Data Science), Department of Computer Science and Engineering, Indian Institute of Information Technology, Bhagalpur.

- Manuscript notebook (text only): [Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb](Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb)
- Documentation: [docs/README.md](docs/README.md)
- Licence: [MIT](LICENSE)

## Abstract

European day-ahead electricity auctions clear expected residual load, not realised residual load. Wind sits at the base of the merit order. A revision to the wind forecast therefore revises which conventional units are committed, which interconnectors are scheduled, and which hours clear at negative or scarcity prices. This paper treats the difference between a public numerical-weather-prediction baseline and a finer artificial-intelligence description of wind as an allocation problem. Single Day-Ahead Coupling is a forecast-clearing auction. Single Intraday Coupling is a market in forecast revisions. Balancing settles whatever remains after the last gate.

## Why this repository is open

The notebook is the manuscript. It is published here so the argument, the laboratory disclaimers, and the reference list can be read without a paywall and without depending on GitHub’s PDF previewer.

## Repository layout

```
prediction-as-power/
├── Prediction_as_Power_Rishabh_Aryan_Manuscript.ipynb
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

The manuscript notebook contains **Markdown cells only**. It is not the computational laboratory.

## How to read

1. Open the notebook on GitHub and allow equations to typeset.
2. Or clone the repository and open the `.ipynb` in any notebook viewer.
3. Read [docs/laboratory-disclaimer.md](docs/laboratory-disclaimer.md) before citing any euro figure.

```bash
git clone https://github.com/Rishabh-bgp/prediction-as-power.git
cd prediction-as-power
```

No Python packages are required to read the manuscript.

## Principal institutional objects

| Object | Role |
|---|---|
| SDAC | Day-ahead coupled auction; clears expected residual load |
| SIDC | Intraday coupled market; trades forecast revisions |
| Balancing | Settles the residual after the last gate |
| Regulation (EU) No 543/2013 | Public data baseline (Transparency Platform) |

## Citation

```
Aryan, R. (2026). Prediction as Power: Artificial Intelligence, Wind,
and the Ordering of European Electricity Markets. Working paper,
IIIT Bhagalpur. https://github.com/Rishabh-bgp/prediction-as-power
```

See `CITATION.cff` and [docs/citation-and-reuse.md](docs/citation-and-reuse.md).

## Contact

- Email: rishabh.250201011@iiitbh.ac.in
- ORCID: https://orcid.org/0009-0004-7595-9440

## Status

Working paper. Laboratory magnitudes are synthetic. Institutional claims about sequential European markets do not depend on the generator.
