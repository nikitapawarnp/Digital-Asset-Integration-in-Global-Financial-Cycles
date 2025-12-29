# Digital Asset Integration in Global Financial Cycles  
## A Regime-Switching Perspective (2017–2025)

---

## Overview

Financial markets evolve through distinct phases—**Bull**, **Bear**, and **Stable**—and asset behavior varies significantly across these regimes. Over the last decade, cryptocurrencies such as **Bitcoin (BTC)** and **Ethereum (ETH)** have transitioned from niche speculative instruments to assets increasingly integrated with traditional financial markets.

This project applies **machine learning–based regime detection** to analyze how cryptocurrencies interact with **equities (S&P 500, NASDAQ)** and **safe-haven assets (Gold)** across market cycles. Using **Hidden Markov Models (HMM)** and **K-Means clustering**, the study evaluates regime-wise **returns, volatility, correlations, lead–lag relationships, and optimal portfolio allocations** from 2017 to 2025.

A key finding is a **structural break after 2020**, where cryptocurrencies shift from weakly correlated assets to **high-beta risk-on instruments**, particularly during market stress.This transformation has significant implications for portfolio diversification and risk management strategies.

---

## Technical Track

**Models & Techniques**
- Machine Learning: Hidden Markov Models (HMM), K-Means Clustering
- Statistical Analysis: DCC-GARCH models, Granger causality tests, cross-correlation functions
- Data Processing: Time series analysis, rolling volatility calculations, feature engineering
- Granger causality and lead–lag analysis (5, 10, 20-day horizons)  
- Mean–variance portfolio optimization with regime-specific risk-free rates
- Optimization: Portfolio optimization using Sharpe ratio maximization
- Validation: AIC/BIC model selection, silhouette analysis, train/test splits 

**Assets & Data**
- Cryptocurrencies: Bitcoin (BTC), Ethereum (ETH)  
- Traditional Assets: S&P 500, NASDAQ Composite, Gold, Crude Oil  
- Macroeconomic Indicators: VIX, US 10-Year Treasury Yield  
- Daily data (2017–2025) sourced from Investing.com  

**Tools**
- Python, Pandas, NumPy  
- scikit-learn, HMM-learn  
- statsmodels  
- matplotlib, seaborn  

---

## Success Metrics

**Model Performance**

- Regime Detection Accuracy: Successfully identified 3 distinct market regimes with clear VIX differentiation (Bull: 12.1, Stable: 16.4, Bear: 26.8)
- Regime Distribution: Stable (52%), Bear (31%), Bull (17%) over 2,207 trading days

**Portfolio Performance**

- Sharpe Ratio Improvement: +53% (0.78 → 1.19) for regime-aware vs static allocation
- Risk Reduction: Maximum drawdown cut in half (-56% → -27%)
- Optimal Crypto Allocation: 3-12% across regimes (significantly lower than commonly assumed)

**Key Findings**

- Correlation Shift: BTC-S&P 500 correlation increased 5x in bear markets (0.07 → 0.38)
- Structural Break: Post-2020 crypto-equity integration intensified (bear correlation >0.51 in 2022-2025)
- Gold as Hedge: Only consistent safe-haven asset with 88% allocation in bear regimes  

---

## Methodology

1. **Data Preparation**
   - Align daily prices across assets  
   - Convert prices to log returns  
   - Compute 20-day rolling volatility  
   - Standardize features using z-scores  

2. **Regime Detection**
   - Train HMM models with 2–4 states  
   - Select optimal 3-state model via BIC and interpretability  
   - Label regimes as Bull, Stable, and Bear  

3. **Validation & Robustness**
   - K-Means clustering comparison  
   - Sub-period analysis (2017–2019, 2020–2021, 2022–2025)  
   - Out-of-sample testing  

4. **Regime-Wise Analysis**
   - Returns, volatility, Sharpe ratios  
   - Correlation matrices and beta estimates  
   - Maximum drawdowns  

5. **Lead–Lag & Causality**
   - Cross-correlation analysis  
   - Granger causality tests across multiple horizons  

6. **Portfolio Optimization**
   - Maximum Sharpe portfolios per regime  
   - Regime-specific US Treasury yields as risk-free rates  
   - Comparison of static vs regime-aware strategies  

---

## Key Features

- Regime-aware analysis instead of static correlations  
- Evidence that crypto diversification fails during crises  
- Identification of Bitcoin as a leading indicator for equity markets  
- Gold remains the only consistent defensive asset across regimes  
- Quantifies the breakdown of the “digital gold” narrative post-2020  
- Actionable insights for dynamic asset allocation and risk management  

---

## 📁 Files in Repository

| File Name | Description |
|----------|-------------|
| `Fin_Tech_Project_Group_8.ipynb` | End-to-end Python notebook implementing data ingestion, feature engineering, regime detection (HMM & K-Means), correlation analysis, lead–lag tests, and regime-aware portfolio optimization |
| `Group_8_Presentation.pptx` | Final project presentation summarizing motivation, methodology, key findings, visualizations, and investment implications |

## 🚀 Future Scope

- **On-Chain & Alternative Data Integration**  
  Extend the framework by incorporating on-chain metrics (active addresses, transaction volume, realized volatility) and alternative data sources such as Google Trends and sentiment indicators to improve early detection of regime transitions.

- **High-Frequency & Intraday Regime Analysis**  
  Apply the regime-switching methodology to high-frequency data to study intraday spillovers, microstructure effects, and faster lead–lag relationships between crypto and equity markets.

- **Global & Emerging Market Expansion**  
  Expand the asset universe to include international equity indices, emerging markets, currencies, and regional crypto adoption patterns to assess cross-country differences in market integration and systemic risk.

- **Advanced Regime Models**  
  Explore more flexible models such as Bayesian HMMs, time-varying transition probability models, and deep learning approaches (LSTM-HMM hybrids) to capture nonlinear regime dynamics more accurately.

- **Transaction Costs & Real-World Constraints**  
  Incorporate transaction costs, taxes, liquidity constraints, and rebalancing frictions to evaluate the practical feasibility of regime-aware investment strategies.

- **Real-Time Dashboards & Decision Tools**  
  Develop real-time dashboards that display regime probabilities, macro signals (VIX, yields), and allocation recommendations for investors, risk managers, and policymakers.

- **Automated Regime-Aware Investment Strategies**  
  Translate the regime-based insights into deployable trading or asset-allocation systems that dynamically adjust exposure to crypto, equities, and defensive assets based on detected market conditions.

- **Regulatory & Policy Implications**  
  Study how changes in crypto regulation, ETF approvals, or institutional participation affect regime behavior and crypto–traditional market integration over time.



