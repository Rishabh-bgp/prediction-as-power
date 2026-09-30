# Institutional background

This note is a reader’s map, not a substitute for ENTSO-E or NEMO Committee rules.

## Sequential markets

- **SDAC** (Single Day-Ahead Coupling) closes near 12:00 CET on day D−1. Wind is unobserved. Accepted bids are forecasts of residual load.
- **SIDC** (Single Intraday Coupling) is the market in which those forecasts are revised as new weather information arrives.
- **Balancing** settles the residual after the last gate. Imbalance prices typically depend on the sign and size of the system imbalance.

## Transparency baseline

Commission Regulation (EU) No 543/2013 and the ENTSO-E Transparency Platform socialise a public baseline. Common document types used in a non-synthetic sequel include:

- A.44 day-ahead prices
- A.65 load
- A.69 wind and solar forecasts
- A.75 actual generation per type

Private models capture the residual around that baseline: faster inference, farm power curves, availability.

## Claim in one sentence

In this market the day-ahead auction clears a *description* of weather. Improving that description changes which machines run.
