# Cryptocurrency Forecasting

A time series modeling toolkit for cryptocurrency markets, including forecasting pipelines, volatility exploration, and walk-forward validation. Current focus: XRP.

## 📊 Project Overview

This project develops and tests a variety of models to forecast short-term cryptocurrency prices (currently focused on XRP).  
It also includes exploratory tools for understanding volatility patterns and structural behavior across time.  
All results are validated using time-aware methods to ensure realistic and reproducible conclusions.

## 📂 Dataset

This repository uses minute-level XRP market data to support time series forecasting and volatility analysis.

- `xrpdata_2025.csv` - Full 2025 XRP price series through July 25, 2025.  
  This dataset was compiled from Binance API queries and cleaned to ensure continuity and correct timestamp alignment.  
  The file maintains minute-level granularity for modeling, feature engineering, and volatility study.

## 🔍 Methods & Features

• Time-aware walk-forward cross-validation  
• Lagged and rolling feature engineering for causal forecasting  
• Decision tree and ensemble methods with cost-complexity pruning  
• Exploratory volatility metrics (log returns, raw ranges, and mixed signals)
• Planned extensions: linear baselines, neural networks, and chaos-based forecasting

## 📁 Files

- `reg_tree_xrpdata.ipynb` - Baseline and pruned decision tree models with block walk-forward validation.
- `rand_forest_xrpdata.ipynb` - Random Forest model with time-aware training, contiguous hold-out testing, and walk-forward cross-validation.
- `xrp_logreturn_range_comp.ipynb` - Exploratory notebook comparing log return and raw range behavior during both a major market event and a recent trading week. Includes time-window visualizations and distributional analysis of directional movement vs. intraperiod variability.
- `xrpdata_mlp.ipynb` - Uses a simple MLP to forecast hourly XRP prices with lagged features, followed by a threshold-based trading simulation and comparison to a buy-and-hold benchmark.
- `LSTM_xrpdata.ipynb` - LSTM model trained on hourly XRP data using lagged and rolling features. Includes sequentialized input generation, walk-forward validation, and a comparison of model-guided trading results against a buy-and-hold benchmark.

## 💡 Key Results

> Initial decision tree models demonstrate consistent short-term forecast accuracy under block walk-forward validation, forming a trustworthy baseline for more advanced models.  
>  
> Random Forest models further reduce variance and maintain high forecasting accuracy across sequential blocks, highlighting the value of ensemble averaging for stable crypto time series predictions.  
>  
> Volatility analysis reveals that log return and raw range capture distinct aspects of market behavior. Log return marks directional displacement between closes, while raw range highlights turbulent candle-level motion. Used together, they provide a richer picture of short-term price dynamics.
>
> A simple MLP model trained on lagged hourly price features achieved strong predictive accuracy, but a basic threshold-based trading strategy underperformed, highlighting the gap between forecast precision and real-world trading performance.
>
> A recurrent neural network (LSTM) trained on lagged hourly XRP features achieved strong prediction accuracy, effectively capturing local trend dynamics. While its predictions were smoother than actual market movements, a simple model-guided trading simulation outperformed a passive buy-and-hold benchmark, indicating that the model identified meaningful short-term directional signals.

## 🛠 Tools Used

Python · NumPy · pandas · scikit-learn · TensorFlow / Keras · Matplotlib · Jupyter Notebook · LaTeX

## 🔮 Future Work

Future development will incorporate chaos theory and sentiment analysis to improve crypto forecasting.

## Author

*Barrett James McDonald, Ph.D. Student, University of South Florida*

---

Questions or feedback? Feel free to reach out or open an issue.
