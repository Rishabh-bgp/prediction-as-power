# Prediction as Power

Artificial intelligence, wind, and the ordering of European electricity markets.

Working paper and computational laboratory. A Germany-like hourly simulator compares legacy NWP wind forecasts with an AI forecast through merit-order prices, imbalance cash-flow, thermal commitment, and stylised cross-border flows.

## Paper

Er. Rishabh Aryan, *Prediction as Power: Artificial Intelligence, Wind, and the Ordering of European Electricity Markets.*

PDF in this repository: `Prediction_as_Power_Rishabh_Aryan.pdf`

Author: M.Tech (Artificial Intelligence and Data Science), Department of Computer Science and Engineering, Indian Institute of Information Technology, Bhagalpur.

- Email: rishabh.250201011@iiitbh.ac.in
- ORCID: https://orcid.org/0009-0004-7595-9440

## What the laboratory does

1. Maps 100 m wind through a smoothed fleet power curve.
2. Builds two years of hourly load, solar, residual load, and a convex day-ahead price.
3. Attaches persistent NWP and AI forecast errors and a D-1 / H-6 / H-1 lead-time ladder.
4. Estimates price models and a counterfactual that swaps only the wind input.
5. Scores merchant imbalance cost for a 100 MW slice and a stylised combined-cycle start rule.
6. Shocks expected home-zone wind and records export to a hydro neighbour.

Numbers in the paper are laboratory magnitudes, not official ENTSO-E statistics.

## Licence

See LICENSE.

## Files

- Prediction_as_Power_Rishabh_Aryan.pdf — 35-page manuscript.
- Prediction_as_Power_Rishabh_Aryan.docx — Word source.

If GitHub shows “Unable to render code block” on the PDF, use Download (raw). That message is a previewer fault, not a corrupt file.
