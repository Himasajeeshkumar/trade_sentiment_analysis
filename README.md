# Trader Performance vs Market Sentiment Analysis

## 📌 Project Overview

This project analyzes how Bitcoin market sentiment (Fear/Greed index) influences trader behavior and performance on Hyperliquid.

The objective is to identify behavioral patterns across sentiment regimes and derive actionable trading strategies based on data-driven insights.

---

## 📂 Dataset Description

Two datasets were used:

1. **Bitcoin Market Sentiment Dataset**
   - Daily sentiment classification (Fear, Greed, Neutral, Extreme variants)
   - Sentiment index value

2. **Hyperliquid Trader Dataset**
   - Trader-level execution data
   - Includes: Account, Execution Price, Trade Size, Side (BUY/SELL), Closed PnL, Position Size, Timestamp, etc.

> Note: The datasets were provided as part of the internship assignment and are not included in this repository.

---

## ⚙️ Methodology

The analysis was conducted in three structured stages:

### 1️⃣ Data Preparation
- Standardized column names
- Converted timestamps to daily format
- Aligned trader data with sentiment data at daily granularity
- Checked for missing values and duplicates
- Converted financial columns to numeric format

### 2️⃣ Feature Engineering
Created key trading metrics:
- Daily PnL per trader
- Win rate (% profitable trades)
- Average trade size
- Trade frequency per day
- Long/Short ratio
- Risk proxy using position exposure

Built trader segments:
- High vs Low activity traders
- Consistent vs Inconsistent traders (based on win rate)

### 3️⃣ Comparative Analysis
- Compared performance across Fear, Greed, and Neutral regimes
- Analyzed behavior changes by sentiment
- Evaluated performance differences across trader segments
- Generated supporting visualizations

---

## 🔍 Key Insights

1. **Higher Average Profitability During Fear**  
   Average PnL per trade is higher during Fear periods compared to Greed, despite similar win rates.  
   This suggests stronger volatility-driven profit opportunities during Fear regimes.

2. **Win Rate Stability Across Regimes**  
   Win rates remain relatively consistent between Fear and Greed periods, indicating that sentiment affects trade magnitude more than trade success probability.

3. **Behavioral Shifts Across Sentiment Conditions**  
   Trade frequency and positioning behavior vary depending on sentiment regime, with traders showing a mild sell bias overall.

4. **Segment-Based Performance Differences**  
   High-activity and consistent traders respond differently to sentiment changes, highlighting the importance of adaptive risk management.

---

## 🚀 Strategy Recommendations

1. **Increase Controlled Exposure During Fear**  
   Traders may benefit from slightly increasing exposure during Fear periods while maintaining strict risk controls.

2. **Reduce Overtrading During Greed**  
   As average profitability per trade declines during Greed, traders should focus on selective high-quality trades instead of increasing volume.

3. **Apply Segment-Specific Risk Rules**  
   High-activity traders should implement trade caps during volatile periods, and inconsistent traders should reduce position size during high-risk regimes.

---

## 🛠️ Setup Instructions

### Requirements

- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- jupyter

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter

▶️ How to Run the Project

Clone the repository:

git clone <your-repository-link>
cd Trader-Performance-Analysis


Download the provided datasets:

sentiment.csv

trader_data.csv

Place both files in the same directory as analysis.ipynb.

Launch Jupyter Notebook:

jupyter notebook


Open analysis.ipynb and run all cells sequentially.

📁 Repository Structure
Trader-Performance-Analysis/
│
├── trade_sentiment_analysis.ipynb
└── README.md
