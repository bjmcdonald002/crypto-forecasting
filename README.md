# Cryptocurrency Forecasting

Comprehensive time series forecasting pipelines for cryptocurrency markets, using interpretable models, ensembles, and deep learning with robust walk-forward validation.

## 📊 Project Overview

This project develops and tests a variety of models — from regression trees to neural networks — to forecast short-term cryptocurrency prices (currently focused on XRP). Rigorous time-aware validation ensures results are realistic and reproducible.

## 📂 Dataset

Includes processed XRP market data at various granularities for experimentation and model benchmarking.

🔗 [Raw minute-level XRP data on Kaggle](https://www.kaggle.com/datasets/imranbukhari/comprehensive-xrpusd-1m-data)

- `xrpdata_sample.csv` — 10,000-observation sample for quick experiments


## 🔍 Methods & Features

* Lagged feature engineering for causal forecasting
* Decision tree regression with cost-complexity pruning
* Block walk-forward cross-validation to preserve temporal order
* Plans to expand to linear models, ensembles, and neural networks

## 📁 Files

* `reg_tree_xrpdata.ipynb` — Baseline and pruned tree models with block walk-forward validation

## 💡 Key Result

> Initial decision tree models demonstrate consistent short-term forecast accuracy under robust block walk-forward validation — forming a trustworthy baseline for more advanced models.

## 🛠 Tools Used

Python (NumPy, pandas, scikit-learn) · Matplotlib · Seaborn

## 📄 Related Materials

Future work will integrate chaos theory and sentiment analysis for crypto forecasting.

## Author

*Barrett James McDonald — Ph.D. Student, University of South Florida*

---

Questions or feedback? Feel free to reach out or open an issue.
