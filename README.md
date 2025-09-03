# Natural-Gas-Storage-Contract-Valuation-Price-Curve-Modeling
Built a Python prototype to model natural gas price curves and value storage contracts, accounting for injection, withdrawal, storage costs, and seasonal trends.

## Project Summary
This project forecasts natural gas prices for any date using historical monthly data and interpolated daily values. It identifies seasonal trends, visualizes monthly patterns, and applies an ARIMA model to predict prices from September 2024 to September 2025, supporting storage contract pricing and trading desk decisions.

## Insights
January and March recorded the highest average natural gas prices, each around 11.78, suggesting possible seasonal demand spikes (winter could be raising the need for heating) while June recorded the lowest average price with 10.70 indicating a likely dip in demand

Created daily records from 2020-10-31 to 2024-09-30 and filled missing daily price data using linear interpolation which allows continuous estimates of prices across all days 

Utilized an ARIMA(2,1,2) model to forecast daily gas prices, training on 80% of historical data and validating on the remaining 20%. The model achieved an RMSE of 0.9360 and MAE of 0.7826, indicating reasonable accuracy. The forecast extends from late September 2024 to September 30, 2025, supporting detailed planning, forecasting and trend analysis.

Both ARIMA and SARIMA models were evaluated, but ARIMA outperformed SARIMA with significantly lower RMSE (0.9360 vs. 1.6841) and MAE (0.7826 vs. 1.4316), confirming it as the more reliable model for forecasting gas prices.


