# Cryptocurrency Forecasting

Comprehensive time series forecasting pipelines for cryptocurrency markets, using interpretable models, ensembles, and deep learning with robust walk-forward validation.

## 📊 Project Overview

This project develops and tests a variety of models — from regression trees to neural networks — to forecast short-term cryptocurrency prices (currently focused on XRP). Rigorous time-aware validation ensures results are realistic and reproducible.

## 📂 Dataset

This repository uses **minute-level XRP market data** to support time series forecasting experiments.

🔗 [Raw historical XRP data on Kaggle](https://www.kaggle.com/datasets/imranbukhari/comprehensive-xrpusd-1m-data)

- `xrpdata_2025.csv` — Full 2025 XRP price series.  
   - January 1, 2025 to mid-February 2025 sourced from the Kaggle dataset.
   - February 2025 to June 13, 2025 retrieved programmatically and appended to create a continuous 2025 dataset.
   - This file preserves minute-level granularity and chronological order, ensuring clean training and testing for forecasting models.

## 🔍 Methods & Features

* Lagged feature engineering for causal forecasting
* Decision tree regression with cost-complexity pruning
* Block walk-forward cross-validation to preserve temporal order
* Plans to expand to linear models, ensembles, and neural networks
## 📁 Files

- `reg_tree_xrpdata.ipynb` — Baseline and pruned decision tree models with block walk-forward validation.
- `rand_forest_xrpdata.ipynb` — Random Forest model with time-aware training, contiguous hold-out testing, and block walk-forward cross-validation.

## 💡 Key Results

> Initial decision tree models demonstrate consistent short-term forecast accuracy under robust block walk-forward validation — forming a trustworthy baseline for more advanced models.  
> Random Forest models further reduce variance and maintain high forecasting accuracy across sequential blocks, showcasing the value of ensemble averaging for stable crypto time series predictions.

## 🛠 Tools Used

Python (NumPy, pandas, scikit-learn) · Matplotlib · Seaborn

## 📄 Related Materials

Future work will integrate chaos theory and sentiment analysis for crypto forecasting.

## Author

*Barrett James McDonald — Ph.D. Student, University of South Florida*

---

Questions or feedback? Feel free to reach out or open an issue.
