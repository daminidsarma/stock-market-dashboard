# 📈 Stock Market Time Series Analysis Dashboard

Interactive dashboard for **exploring, analyzing, and visualizing stock time series**.  
Built with **Streamlit + Plotly + yfinance**, with technical indicators, resampling, and basic portfolio backtesting.

---

## 🚀 Features
- 🔎 **Ticker search & multi-select** (e.g., TCS.NS, AAPL, BTC-USD)
- ⏱️ **Date range & interval** controls (1d/1wk/1mo, intraday where supported)
- 📊 **Interactive charts**: candlesticks, OHLC, volume, line
- 🧠 **Indicators**: SMA/EMA, RSI, MACD, Bollinger Bands (via `pandas_ta`)
- 🧮 **Returns & risk**: cumulative/rolling returns, drawdown, Sharpe (basic)
- 🧾 **Download**: export filtered data to CSV; save charts as HTML/PNG
- ⚡ Caching for faster reloads; graceful fallback if API rate-limits

---

## 🧱 Project Structure
stock-market-dashboard/
│── app.py # Streamlit app
│── requirements.txt # Dependencies
│── .env.example # Sample secrets file
│── modules/
│ ├── data.py # yfinance fetch, caching, resampling
│ ├── indicators.py # pandas_ta wrappers
│ └── metrics.py # returns, drawdown, Sharpe, etc.
│── assets/ # screenshots, logos
│── data/ # optional local CSV cache (gitignored)
│── README.md

yaml
Copy code

---

## ⚙️ Setup

```bash
git clone https://github.com/daminidsarma/stock-market-dashboard.git
cd stock-market-dashboard

python -m venv venv
# Windows
venv\Scripts\activate
# Mac/Linux
# source venv/bin/activate

pip install -r requirements.txt
Optional: create .env (copy from .env.example) if you later add paid data sources (Alpha Vantage, Finnhub, etc.).

Run:

bash
Copy code
streamlit run app.py
🛠️ Tech Stack
Streamlit, Plotly

pandas, numpy, pandas_ta

yfinance, python-dotenv

🌟 Roadmap
Forecasting (Prophet / statsmodels)

Event overlays (earnings/dividends)

Portfolio allocation what-ifs (equal-weight vs. CAPM)

