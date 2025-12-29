# Digital Asset Integration in Global Financial Cyycles  
### A Regime-Switching Perspective (2017–2025)

---

## Overview
This project analyzes how **cryptocurrencies (Bitcoin and Ethereum)** integrate with **traditional financial markets** across different market conditions. Using **regime-switching techniques**, the study identifies hidden market states—**Bull, Stable, and Bear**—and evaluates how correlations, risk, and portfolio performance change across these regimes.

The motivation is to test whether cryptocurrencies truly provide **portfolio diversification**, especially during periods of market stress, and to examine how their role evolved after **institutional adoption post-2020**.

---

## Technical Track
- **Programming Language:** Python  
- **Data Processing:** pandas, numpy  
- **Machine Learning:**  
  - Hidden Markov Models (Gaussian HMM – `hmmlearn`)  
  - K-Means Clustering (`scikit-learn`)  
- **Econometrics:** Granger Causality (`statsmodels`)  
- **Portfolio Optimization:** Mean-Variance Optimization (`scipy`)  
- **Visualization:** matplotlib, seaborn  
- **Data Frequency:** Daily time-series (2017–2025)

---

## Success Metrics
The success of the project is evaluated using:

- **Clear regime separation** (Bull / Stable / Bear)
- **Statistical stability** of regime transition probabilities
- **Regime-specific correlation shifts** between crypto and equities
- **Portfolio performance improvement**, measured via:
  - Sharpe Ratio
  - Maximum Drawdown
- **Economic interpretability** of regimes using macro indicators (VIX, yields)

---

## Methodology
1. **Data Collection & Cleaning**
   - Historical price data for BTC, ETH, S&P 500, NASDAQ, Gold, Oil, VIX, and US 10-Year Yield
   - Alignment of dates and handling missing values

2. **Feature Engineering**
   - Daily log returns
   - Rolling volatility measures
   - Standardization for clustering and regime detection

3. **Regime Detection**
   - Gaussian Hidden Markov Model with three latent states
   - K-Means clustering as a robustness check

4. **Regime-Wise Analysis**
   - Correlation matrices by regime
   - Macro-economic behavior across regimes
   - Lead-lag relationships using Granger causality

5. **Portfolio Construction**
   - Regime-specific optimal asset allocation
   - Comparison of static vs. regime-aware portfolios

---

## Key Features
- Identifies **structural break in crypto behavior post-2020**
- Shows **correlation spikes during Bear markets**, reducing diversification benefits
- Demonstrates **regime-aware portfolios outperform static allocations**
- Combines **machine learning + financial economics**
- Includes **clear visualizations** for regimes, correlations, and portfolio weights

---

## Files in Repository



