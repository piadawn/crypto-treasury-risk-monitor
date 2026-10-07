# Crypto Treasury Risk Monitor — V1
Historical portfolio risk analysis by Sofia Dawn Estrada, developed with guided AI assistance.

## Run
Open Crypto_Treasury_Risk_Monitor_V1.ipynb in Google Colab or Jupyter. Install yfinance, pandas and matplotlib, then run cells in order. Run the final export cell to generate complete CSV histories and additional charts.

## Method
Yahoo Finance daily BTC-USD and ETH-USD closing observations from January 1, 2024 to December 31, 2025. Initial hypothetical capital $10,000, split 70/30; fixed coin quantities thereafter. Daily simple returns; sample standard deviation for daily volatility; drawdown against the running portfolio peak. One-day historical VaR uses the linearly interpolated fifth percentile of 730 paired daily return scenarios replayed at final weights. ES averages the 37 scenarios at or below that percentile. Historical buy-and-hold volatility uses changing historical weights, whereas snapshot VaR/ES use the final weights.

## Findings
Final portfolio value $17,653.07; BTC share 78.56%; current drawdown 31.45%; maximum drawdown 36.20%. Historical one-day VaR 95%: 4.10% ($723.27); ES: 5.68% ($1,002.25). Example concentration and drawdown limits breached; example VaR limit not breached. Recommend reviewing concentration, loss tolerance and cash needs.

## Included outputs and verification
Executed locally in VS Code. Complete exported price, return, asset-value, weight, portfolio-history, replayed-scenario, exposure, stress and dashboard CSVs are included, alongside all four exported charts. Daily coverage, valid positive prices, and 731 observations were checked. Returns, holdings and weights were independently recalculated; final value, VaR and ES match the notebook to displayed precision. Snapshot CSVs are rounded summaries; full exports retain numerical precision. The notebook preserves the saved execution results. Original wording-practice drafts are excluded.

## Limits
Hypothetical holdings and limits, not actual company data or policy. Concentration already exceeded 60% at inception. Fixed USD valuation; no FX, trading fees, slippage, liquidity, custody, counterparty, tax, staking or cash obligation modeling. Daily close data miss intraday losses. Two years of historical returns do not guarantee future outcomes. Stress shocks have no assigned probability or time horizon. VaR and ES are descriptive snapshot estimates, not validated forecasts or maximum losses. No live monitoring, alerts or VaR backtesting yet.

## Data source
https://finance.yahoo.com/quote/BTC-USD/history/
https://finance.yahoo.com/quote/ETH-USD/history/
Data obtained through yfinance. Review source terms before publicly redistributing full market-price exports.
