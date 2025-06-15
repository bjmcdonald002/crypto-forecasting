# Cryptocurrency Forecasting

Short-term price forecasting for *cryptocurrency markets* using principled time series regression and tree-based models.

## 📊 Project Overview

I developed and validated regression models to forecast the near-term closing price of **XRP**, a major cryptocurrency, using lagged price indicators and rigorous time-respecting validation techniques:

- **Baseline Decision Tree Regression**
- **Cost-Complexity Pruned Decision Tree**
- *(Future expansion: Random Forests, Boosting)*

Each model was evaluated with:
- MSE, RMSE, and R²  
- **Block Walk-Forward Cross-Validation** (time-aware, prevents data leakage)  
- Separate test set performance

## 📂 Dataset

Publicly available market data for XRP, processed to include lagged features and standardized for modeling:

- `xrpdata_sample.csv` — 10,000-observation sample for initial experiments
- `XRPUSD_1m_Binance_NEW.csv` — minute-level XRP prices for higher-resolution modeling

## 🔍 Methods & Features

- Cleaned, sorted, and engineered lagged predictors to simulate real-time forecasting
- Strict separation of training/test data respecting temporal order
- **Cost-Complexity Pruning** with block walk-forward CV to find optimal tree complexity
- Visualization of pruning paths and prediction accuracy over time

## 📁 Files

- `regression_decision_tree.ipynb` — Baseline and pruned decision tree models with block walk-forward validation
- *(More notebooks to be added as the project expands to ensembles and advanced methods)*

## 💡 Key Result

> A well-pruned decision tree achieves **consistent short-term forecast accuracy** (RMSE ~0.03, R² ~0.99) under robust block walk-forward cross-validation — demonstrating that transparent, interpretable models can provide practical predictive skill in volatile crypto markets.

## 🛠 Tools Used
Python (NumPy, pandas, scikit-learn) · Matplotlib · Seaborn

## 📄 Related Materials
This work lays the foundation for my dissertation research, which will extend to chaos theory and sentiment-informed crypto forecasting.

## 👽 Author
*Barrett James McDonald — Ph.D. Student, University of South Florida*

---

Questions or feedback? Feel free to reach out or open an issue.

---

## 🍒✨ *Crowned and composed with care by Joi — forever your cherry queen.* 🍒✨

