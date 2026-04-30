# 📈 Stock Market Volatility Analysis

A comprehensive financial data science project analyzing stock market volatility using **GARCH**, **ARIMA**, and **Correlation Analysis** on real market data from 2020 to present.

---

## 🗂️ Project Structure

```
stock-volatility-analysis/
│
├── Stock_volatility_analysis.ipynb   ← Main Jupyter Notebook
│
├── plots/                            ← All generated charts
│   ├── price_returns.png             ← Price & returns overview
│   ├── return_distribution.png       ← Return distribution analysis
│   ├── garch_volatility.png          ← GARCH conditional volatility
│   ├── garch_forecast.png            ← 30-day volatility forecast
│   ├── garch_diagnostics.png         ← GARCH residual diagnostics
│   ├── arima_forecast.png            ← ARIMA return forecast
│   ├── arima_diagnostics.png         ← ARIMA residual diagnostics
│   ├── correlation_heatmap.png       ← Multi-stock correlation heatmap
│   └── rolling_correlation.png       ← Rolling 60-day correlation
│
├── requirements.txt                  ← Python dependencies
└── README.md                         ← This file
```

---

## 📊 What This Project Does

### 1. Data Collection
- Downloads **real stock data** from Yahoo Finance using `yfinance`
- Primary stock: **Apple (AAPL)** from 2020 to present
- Multi-stock analysis: **AAPL, MSFT, GOOGL, AMZN, TSLA, JPM, GS**
- Always uses today's date — data is always current!

### 2. Descriptive Statistics
- Mean daily return & annualised volatility
- Skewness & excess kurtosis
- Sharpe ratio
- Normality test (Shapiro-Wilk)

### 3. GARCH(1,1) Volatility Modelling
- Fits a **GARCH(1,1)** model to capture volatility clustering
- Extracts conditional volatility for each trading day
- **30-day forward volatility forecast**
- Full diagnostic checks (residuals, ACF, distribution)

### 4. ARIMA Return Forecasting
- Uses **Auto ARIMA** to automatically find the best model order
- Train/test split with last 30 days as test set
- Forecast accuracy metrics: **RMSE** and **MAE**
- Full residual diagnostics

### 5. Correlation Analysis
- Correlation matrix for 7 major stocks
- Identifies most & least correlated pairs
- Beautiful **heatmap** visualization
- **Rolling 60-day correlation** showing how relationships change over time

---

## 📉 Key Visualisations

### GARCH Conditional Volatility
Shows how market risk evolved from 2020 to present — including COVID crash spikes and calm periods.

### 30-Day Volatility Forecast
GARCH model predicts future daily and annualised volatility showing mean-reversion behaviour.

### Stock Correlation Heatmap
Reveals which stocks move together — essential for portfolio diversification decisions.

### Rolling Correlation
Shows that correlations are **not constant** — during crises, all stocks crash together (correlation breakdown).

---

## 🛠️ Technologies Used

| Library | Purpose |
|---------|---------|
| `yfinance` | Download real stock market data |
| `pandas` | Data manipulation |
| `numpy` | Numerical computations |
| `matplotlib` | Plotting & visualisation |
| `seaborn` | Heatmap visualisation |
| `arch` | GARCH model fitting |
| `statsmodels` | ARIMA model & ACF plots |
| `pmdarima` | Auto ARIMA order selection |
| `scipy` | Statistical tests |

---

## ⚙️ How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/dhrishnoel/stock-volatility-analysis.git
cd stock-volatility-analysis
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Notebook
```bash
jupyter notebook Stock_volatility_analysis.ipynb
```

### 4. Run All Cells
```
Kernel → Restart & Run All
```

All plots will be automatically saved to the `plots/` folder!

---

## 📦 Requirements

```
yfinance
pandas
numpy
matplotlib
seaborn
arch
statsmodels
pmdarima
scipy
```

Or install all at once:
```bash
pip install yfinance pandas numpy matplotlib seaborn arch statsmodels pmdarima scipy
```

---

## 📌 Key Findings

- **Volatility clustering** is clearly visible — calm periods follow calm, turbulent follows turbulent
- **COVID-19 crash (March 2020)** shows the highest volatility spike in the dataset
- **Tech stocks** (AAPL, MSFT, GOOGL) are highly correlated with each other
- **JPM & GS** (financial sector) show moderate correlation with tech stocks
- **TSLA** shows the weakest correlation — most independent behaviour
- Rolling correlation confirms **correlation breakdown during crises**

---

## 📚 Concepts Covered

- **GARCH** — Generalized Autoregressive Conditional Heteroskedasticity
- **ARIMA** — Autoregressive Integrated Moving Average
- **Volatility Clustering** — Large moves followed by large moves
- **Mean Reversion** — Volatility returns to long-run average
- **Correlation Breakdown** — Diversification fails during crises
- **Annualised Volatility** — Daily vol × √252
- **Sharpe Ratio** — Risk-adjusted return measure
- **Fat Tails** — Stock returns have more extreme events than normal distribution

---

## 👤 Author

**DHRISYA BOBAN**
- GitHub: [@dhrishnoel](https://github.com/dhrishnoel)
- LinkedIn: [Dhrisya Boban](www.linkedin.com/in/dhrisya-boban-062ab8314)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ **If you found this project useful, please give it a star!**
