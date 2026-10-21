# Did dockless e-bikes eat London's Santander Cycles?

## Question
After controlling for weather and calendar effects, did Santander Cycles
hires fall once dockless e-bikes became widespread (from 2022)?

## Data
- TfL daily hires, 30 Jul 2010 to [last date], [N] days (London Datastore, OGL v2)
- Daily London weather from Open-Meteo (ERA5 reanalysis)

## Method
OLS on log daily hires, 2015 onward, with temperature (and its square),
rainfall, heavy-rain flag, wind, day-of-week, month, bank holidays and
year effects. HAC (Newey-West, 14 lags) standard errors. Plus a
counterfactual trained on 2016-19 and projected onto 2022+ weather.

## Findings
1. Weather explains a large share of daily variation (R² = [x]).
2. After adjustment, hires in 2022-[year] ran [x]% [below/above] 2019
   (95% CI [lo] to [hi]).
3. The result is [stable / sensitive] to the start date: [range] across
   cut-offs of Jan 2022, Oct 2022 and Jan 2023.
4. Against the 2016-19 baseline, 2022+ is [x]% short of expectation.

## What this does and does not show
It shows a weather-adjusted shift in docked demand that coincides with
the rise of dockless e-bikes. It does not prove e-bikes caused it:
hybrid working, pricing and network changes all overlap the same window.

## Next steps
Trip-level TfL data by station; dockless operator data if it becomes
available; a difference-in-differences comparing stations near and far
from dockless parking bays.