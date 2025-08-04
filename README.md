# Cryptocurrency Forecasting

A time series modeling toolkit for cryptocurrency markets, including forecasting pipelines, volatility exploration, and walk-forward validation. Current focus: XRP.

## 📊 Project Overview

This project develops and tests a variety of models to forecast short-term cryptocurrency prices (currently focused on XRP).  
It also includes exploratory tools for understanding volatility patterns and structural behavior across time.  
All results are validated using time-aware methods to ensure realistic and reproducible conclusions.

## 📂 Dataset

This repository uses minute-level XRP market data to support time series forecasting and volatility analysis.

- `xrpdata_2025.csv` - Full 2025 XRP price series through July 18, 2025.  
  This dataset was compiled from Binance API queries and cleaned to ensure continuity and correct timestamp alignment.  
  The file maintains minute-level granularity for modeling, feature engineering, and volatility study.

## 🔍 Methods & Features

* Lagged feature engineering for causal forecasting
* Decision tree regression with cost-complexity pruning
* Block walk-forward cross-validation to preserve temporal order
* Exploratory volatility analysis using log return and raw range
* Plans to expand to linear models, ensembles, and neural networks

## 📁 Files

- `reg_tree_xrpdata.ipynb` - Baseline and pruned decision tree models with block walk-forward validation.
- `rand_forest_xrpdata.ipynb` - Random Forest model with time-aware training, contiguous hold-out testing, and walk-forward cross-validation.
- `xrp_logreturn_range_comp.ipynb` - Exploratory notebook comparing log return and raw range behavior during both a major market event and a recent trading week. Includes time-window visualizations and distributional analysis of directional movement vs. intraperiod variability.
- `xrpdata_mlp.ipynb` - Uses a simple MLP to forecast hourly XRP prices with lagged features, followed by a threshold-based trading simulation and comparison to a buy-and-hold benchmark.

## 💡 Key Results

> Initial decision tree models demonstrate consistent short-term forecast accuracy under block walk-forward validation, forming a trustworthy baseline for more advanced models.  
>  
> Random Forest models further reduce variance and maintain high forecasting accuracy across sequential blocks, highlighting the value of ensemble averaging for stable crypto time series predictions.  
>  
> Volatility analysis reveals that log return and raw range capture distinct aspects of market behavior. Log return marks directional displacement between closes, while raw range highlights turbulent candle-level motion. Used together, they provide a richer picture of short-term price dynamics.
>
> A simple MLP model trained on lagged hourly price features achieved strong predictive accuracy, but a basic threshold-based trading strategy underperformed, highlighting the gap between forecast precision and real-world trading performance.

## 🛠 Tools Used

Python · NumPy · pandas · scikit-learn · TensorFlow / Keras · Matplotlib · Jupyter Notebook · LaTeX


## 📄 Related Materials

Future work will integrate chaos theory and sentiment analysis for crypto forecasting.

## Author

*Barrett James McDonald, Ph.D. Student, University of South Florida*

---

Questions or feedback? Feel free to reach out or open an issue.
