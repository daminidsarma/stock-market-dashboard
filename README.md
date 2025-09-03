# 📈 Tech Stock Analysis Dashboard (Streamlit)

A lightweight dashboard to explore **AAPL, AMZN, GOOG, MSFT** price data:
- Closing price over time
- Moving Averages (10/20/50)
- Daily returns (%)
- Resampled average close (Monthly / Quarterly / Yearly)
- Correlation heatmap across the four stocks

> Built with **Streamlit, Plotly, pandas, NumPy, seaborn, Matplotlib**.

---

## 🚀 Features

1) **Closing Prices**  
Interactive line chart of the selected company’s closing price vs. date.

2) **Moving Averages (10/20/50)**  
Overlays 10/20/50-day rolling means on closing price.

3) **Daily Returns (%)**  
Day-over-day percentage changes in closing price.

4) **Resampling**  
Aggregate average closing prices at **Monthly / Quarterly / Yearly** frequency.

5) **Correlation Heatmap**  
Correlation matrix of closing prices for AAPL/AMZN/GOOG/MSFT.

---

## 📂 Project Structure

stock-market-dashboard/
│── Dashboard.py # Streamlit app
│── Stock_Price_Analysis.ipynb # Notebook (EDA / experiments)
│── data/ # Put your CSVs here (AAPL_data.csv, AMZN_data.csv, ...)
│── requirements.txt
│── .gitignore
│── README.md

yaml
Copy code

> If your CSVs are currently referenced by absolute Windows paths, switch to relative paths (e.g., `data/AAPL_data.csv`) in `Dashboard.py`.

---

## ⚙️ Setup & Run

```bash
git clone https://github.com/daminidsarma/stock-market-dashboard.git
cd stock-market-dashboard

# (optional) create a virtual environment
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
# source venv/bin/activate

pip install -r requirements.txt

# Place CSVs under ./data:
#   data/AAPL_data.csv
#   data/AMZN_data.csv
#   data/GOOG_data.csv
#   data/MSFT_data.csv

streamlit run Dashboard.py
