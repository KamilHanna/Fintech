# Fintech


## 🧠 Business Case 1 — Customer Segmentation in Retail Banking

This project applies unsupervised learning techniques to segment retail banking clients based on demographic and financial behavior data. After preprocessing, dimensionality reduction methods (UMAP, PCA, t-SNE) were used to uncover latent structure in the dataset. Clustering algorithms (DBSCAN, HDBSCAN, MiniSom) were then applied to identify distinct client groups. Cluster validity was assessed through silhouette analysis and statistical tests (MANOVA, ANOVA), confirming meaningful differences across segments. The outcome enables data-driven insights for personalized financial services and targeted marketing strategies.

## 💼 Business Case 2 — Predictive Modeling and Investment Recommendation

This project builds a comprehensive machine learning pipeline to model client investment preferences and generate personalized product recommendations. The pipeline includes preprocessing, dimensionality reduction, clustering (DBSCAN, HDBSCAN, KMeans), and classification using neural networks, XGBoost, and LightGBM. Client behavior is segmented into actionable classes, enabling tailored predictions via deep learning and hybrid recommendation systems. Multiple modeling strategies, including Two-Tower neural architectures, were explored to match financial products with client profiles based on risk, wealth, and preference.

## ⚠️ Business Case 3 — Early Warning System for Market Downturns

This project implements a market stress detection model using macro-financial time series data, including gold prices, currency indices, credit spreads, and equity benchmarks. The target variable indicates early warning periods preceding major downturns. After time-aware preprocessing and feature engineering, classification models—such as LightGBM, XGBoost, and deep neural networks—were trained to predict emerging systemic risk. SHAP analysis was used to interpret model behavior, and a scoring system was designed to support proactive risk mitigation and portfolio allocation decisions.

## 🧮 Business Case 4 — Hedge Fund Index Replication via Liquid Asset Portfolio

This project aims to replicate the performance of the HFRX hedge fund index using a dynamic long-short portfolio of liquid futures and index proxies. Through normalization, return engineering, and correlation analysis, a synthetic benchmark portfolio is constructed. Multiple linear models—including OLS, Lasso, Ridge, and Elastic Net regressions—are employed to identify optimal asset weightings. Model selection and performance evaluation are conducted using cross-validation, tracking error, and information ratios under both rolling and expanding windows, enabling robust backtested replication strategies.

## 🧠 Business Case 5 — Optimizing Marketing Nudges with Bayesian Learning

This project explores how to personalize marketing strategies by identifying the most effective nudging technique—**Framing**, **Peer Comparison**, or **Storytelling**—for different user personas. Using demographic data, users are classified and analyzed through Bayesian inference to estimate tactic effectiveness over time. Incremental learning, logistic models, decision trees, SVMs, and random forests are benchmarked, with predictions combined in an ensemble. A **Bayesian Multi-Armed Bandit** algorithm is implemented to dynamically select the highest-yielding message in real time, enabling data-driven and adaptive marketing decisions.

# 📈 Final Project — Early Market Dynamics Modeling & Hedge Fund Replication

This project aims to replicate hedge fund index returns and detect early market signals using financial time series data and advanced machine learning methods. The goal is to build a synthetic hedge fund through a combination of regression, state-space models, and reinforcement learning agents, while comparing different return preprocessing techniques for improved stability and risk-adjusted performance.

## 📊 Project Objectives

- Replicate hedge fund returns using a portfolio of liquid tradable instruments.
- Evaluate the impact of return transformations:
  - **Raw returns**
  - **Cropped returns** (negatives set to zero)
  - **Absolute returns**
- Apply regression and time-series models for forecasting and signal extraction.
- Develop reinforcement learning agents (e.g., Q-learning) for dynamic portfolio decisions.
- Analyze models through a wide range of **risk metrics**, including downside-focused ones.

## ⚙️ Techniques Used

- **Linear Models**: OLS, Ridge, Lasso, Elastic Net with walk-forward validation.
- **State-Space Models**: ARIMA, SARIMAX, and custom Kalman Filters.
- **Reinforcement Learning**: Tabular Q-learning with epsilon-greedy policies.
- **Shrinkage Estimation**: A custom Kalman Filter implementation required estimating a stable error covariance matrix. We used the **Ledoit-Wolf shrinkage estimator** based on:

> Ledoit, O., & Wolf, M. (2003).  [View the paper](Documents/honey.pdf)

> This method systematically reduces estimation error by shrinking extreme coefficients toward the center, significantly improving portfolio stability.

## 📈 Evaluation Metrics

- Total Return, CAGR, Volatility, Sharpe & Sortino Ratios
- Downside Risk: Semi-Deviation, LPM, CDaR, CVaR, Omega Ratio
- Tracking Error vs Benchmark

## 🧪 Key Results

- **Cropped returns** produced more stable portfolios with reduced downside risk.
- **Absolute returns** underperformed, except in Kalman Filter applications.
- **Reinforcement learning agents** achieved highest raw returns but with greater volatility.
- The **Ledoit-Wolf covariance shrinkage** was essential to stabilize matrix computations in the Kalman Filter, avoiding numerical instabilities.

#
