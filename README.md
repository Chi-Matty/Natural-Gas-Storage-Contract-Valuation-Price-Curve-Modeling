# Natural-Gas-Storage-Contract-Valuation-Price-Curve-Modeling
Built a Python prototype to model natural gas price curves and value storage contracts, accounting for injection, withdrawal, storage costs, and seasonal trends.

## Project Summary
This project forecasts natural gas prices for any date using historical monthly data and interpolated daily values. It identifies seasonal trends, visualizes monthly patterns, and applies an ARIMA model to predict prices from September 2024 to September 2025, supporting storage contract pricing and trading desk decisions.

## Insights
January and March recorded the highest average natural gas prices, each around 11.78, suggesting possible seasonal demand spikes (winter could be raising the need for heating) while June recorded the lowest average price with 10.70 indicating a likely dip in demand

Created daily records from 2020-10-31 to 2024-09-30 and filled missing daily price data using linear interpolation which allows continuous estimates of prices across all days 

<img width="2048" height="1089" alt="image" src="https://github.com/user-attachments/assets/d0cc83e2-685b-4933-b3e7-c128e7c5418b" />

The chart shows gas price estimates using an ARIMA(2,1,2) model from 2021 to September 2025. Historical prices up to mid-2024 fluctuate between 10 and 12.5, peaking around 2023–2024. The forecast, starting October 2024 (red dashed line), remains stable around 12.5, indicating a steady trend. The model, trained on 80% of historical data and validated on 20%, achieved an RMSE of 0.9360 and MAE of 0.7826, supporting detailed planning, forecasting, and trend analysis.

Both ARIMA and SARIMA models were evaluated, but ARIMA outperformed SARIMA with significantly lower RMSE (0.9360 vs. 1.6841) and MAE (0.7826 vs. 1.4316), confirming it as the more reliable model for forecasting gas prices.

The storage contract simulation indicates a net value of $0.28, derived from a single injection of 1 MMBtu on June 1, 2024, and withdrawal of 1 MMBtu on December 1, 2024, with a maximum capacity of 10 MMBtu. The total revenue of $11.8 from withdrawal exceeds the purchase cost of $11.4, yielding a $0.4 profit, though this is offset by a $0.121 storage fee over the period. This suggests a modest profitability, sensitive to price differences and storage costs.


