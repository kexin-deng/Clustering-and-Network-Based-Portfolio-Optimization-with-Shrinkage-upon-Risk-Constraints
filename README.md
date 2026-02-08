# Clustering and Network-Based Portfolio Optimization with Shrinkage and CVaR

## Aim of the Project
This project develops a machine-learning–driven portfolio construction framework that enhances classical Mean–Variance Optimization (MVO) through clustering-based stock selection and advanced risk management techniques.  
We study whether combining unsupervised learning, shrinkage estimation, and tail-risk constraints can improve risk-adjusted performance relative to traditional optimization and the S&P 500 benchmark.

---

## Methodology Overview

### Stock Selection via Clustering and Network Methods
We apply multiple unsupervised learning and network-based algorithms to partition the S&P 500 equity universe, including:
- K-Means  
- Hierarchical Clustering  
- Partitioning Around Medoids (PAM)  
- Gaussian Mixture Models (GMM)  
- DBSCAN  
- Minimum Spanning Tree (MST)

Within each cluster, top assets are selected based on historical Sharpe ratios to reduce dimensionality, improve diversification, and stabilize downstream optimization.

---

### Portfolio Optimization
Selected assets are passed into three optimization frameworks:
1. **Baseline Mean–Variance Optimization (MVO)**
2. **MVO with Ledoit–Wolf Shrinkage**, improving covariance matrix stability
3. **CVaR (Expected Shortfall) Optimization**, explicitly controlling downside tail risk

All portfolios are constructed under long-only, fully invested constraints.

---

### Backtesting Framework
- Weekly return data derived from daily prices  
- Rolling 3-month (13-week) lookback window  
- Monthly rebalancing  
- Strict out-of-sample evaluation (no look-ahead bias)

Performance is evaluated using Sharpe ratio, volatility, maximum drawdown, Sortino ratio, CAGR, and Calmar ratio.

---

## Key Results
- Shrinkage significantly improves MVO robustness and out-of-sample performance  
- CVaR constraints reduce drawdowns and improve downside risk control  
- PAM and DBSCAN clustering consistently outperform other selection methods  
- Best strategies achieve Sharpe ratios above **1.6**, substantially outperforming the S&P 500 benchmark (~0.65)

---

## Data
- Equity universe: S&P 500 constituents  
- Frequency: Weekly returns  
- Period: 2020–2023  
- Source: Yahoo Finance (yfinance)

---

## References
This project builds upon classical portfolio theory (Markowitz) and recent advances in clustering, shrinkage estimation, and tail-risk optimization, including work by Rockafellar & Uryasev, Ban et al., and related academic studies.

---

## Authors
Kexin Deng · Olivia Guo · Weihang Lin  
Cornell University — ORIE
