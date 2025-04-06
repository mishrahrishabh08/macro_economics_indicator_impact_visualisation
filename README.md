# Macro-Economic Indicator Impact Simulator

## 📌 Objective
The objective of this project is to **understand and demonstrate data collection, preprocessing, and visualization** to analyze the impact of **macro-economic indicators** (GDP, Unemployment Rate, Inflation) on the **S&P 500 index** over time. The project utilizes data from trusted sources such as the **FRED API** and **Yahoo Finance**, aiming to uncover trends, correlations, and anomalies between economic health and market behavior.

---

## 📊 Project Description
This project leverages Python for data collection, preprocessing, and visualization of the following economic indicators:

- **S&P 500 (Close Price)** – Financial market performance (via `yfinance`)
- **Unemployment Rate** – Indicator of labor market strength (via FRED)
- **GDP (Gross Domestic Product)** – Broadest measure of economic output (via FRED)
- **Inflation (CPI)** – Measures changes in price levels (via FRED)

All these indicators are **standardized using `StandardScaler`** to enable visual and analytical comparisons, despite their differing units and magnitudes.

---

## 📂 Folder Setup & Virtual Environment
To ensure reproducibility and manage dependencies, a **Python virtual environment** is recommended.

### ✅ Steps to Create a Virtual Environment:
```bash
python3 -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
```

---

## 🔌 APIs Used
### 1. **FRED API (Federal Reserve Economic Data)**
- Provides U.S. economic data such as GDP, Unemployment, and Inflation.
- Requires an API key (free registration at [https://fred.stlouisfed.org/]).

### 2. **yfinance**
- Pulls historical stock market data.
- Used to extract daily S&P 500 index values.

---

## ⚙️ Preprocessing Notes
- All CSV files were programmatically merged using a script that relies on a common `date` column.
- `sp500.csv` file had inconsistent column naming, which was manually corrected to ensure smooth merging.
- Columns were standardized to lowercase and stripped of leading/trailing spaces for consistency.

---

## 📉 Key Visualization: Trends from 2006 to 2024
![output](https://github.com/user-attachments/assets/febbdcb6-435c-44b6-a3c5-d18069e11095)

The line graph plots the standardized values of:
- **S&P 500 Close (Blue)**
- **Unemployment Rate (Red)**
- **GDP (Orange)**
- **Inflation (Green)**

### 📈 Observed Trends & Reasoning
| Period        | Event / Observation                              | Reason                                                                 |
|---------------|---------------------------------------------------|------------------------------------------------------------------------|
| 2008–2009     | S&P 500 drop, Unemployment spikes, GDP falls     | Global Financial Crisis: Bank failures, housing crash, credit freeze. |
| 2010–2019     | Market recovery, low unemployment                | Low interest rates, steady economic growth, tech boom.                |
| 2020          | Sharp S&P crash and recovery, unemployment spike | COVID-19 pandemic: Lockdowns, Fed stimulus, tech sector resilience.   |
| 2021–2022     | Inflation surge, GDP fluctuation, market wobble  | Post-COVID recovery, stimulus overheating, supply chain disruptions.  |
| 2023–2024     | Stabilization across all indicators               | Fed rate hikes, inflation control, economic soft landing.             |

> 🔍 The graph highlights how **macro factors influence the market**, with the S&P 500 often acting as a **leading indicator** of broader economic shifts.

---

## ✅ Summary
- Data was merged, cleaned, and transformed for accurate visualization.
- `StandardScaler` was used to scale features and ensure fair comparison.
- The main visual captures **18 years** of economic history in a single, intuitive plot.

---

## 🛠️ Technologies Used
- `pandas`, `matplotlib`, `yfinance`, `fredapi`, `scikit-learn`
- Python 3.10+

---

## 📬 Future Work
- Integrate forecasting models (VAR, LSTM).
- Build an interactive web dashboard for simulation.
- Extend to global economic indicators.

