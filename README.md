# Cultural Spillover: Nana → Vivienne Westwood (Google Trends)

This project tests whether renewed interest in the manga/anime **Nana** predicts increased consumer interest in **Vivienne Westwood**, using Google Trends as a proxy for attention.

## Research question
Do increases in *Nana* search interest lead (with a lag) to increases in *Vivienne Westwood* search interest?

## Data
- Source: Google Trends (normalized index 0–100; not raw counts)
- Market: US (from the exported file)
- Frequency: monthly
- Period: 2004–2026 (approx.)
- Series: Nana, Vivienne Westwood, Chanel (control)

## Approach
1. Exploratory time-series plots  
2. Lead–lag analysis ($$Nana_{t-1}$$ vs $$VW_t$$)  
3. Regression with controls and trend, using HAC robust standard errors:

$$
VW_t = \alpha + \beta_1 Nana_{t-1} + \beta_2 Chanel_t + \beta_3 Trend_t + \varepsilon_t
$$

## Key result (summary)
Lagged Nana interest is strongly positively associated with Vivienne Westwood interest, even after controlling for general luxury attention and a time trend.

## Limitations
- Google Trends values are normalized; comparisons are relative
- Observational design; results are consistent with spillover but not definitive causality
- Residual autocorrelation may remain (HAC used; robustness checks recommended)

## Files
- `nana-and-vivienne-westwood.ipynb` — Main analysis notebook  
- `time_series_US_*.csv` — Google Trends raw data
