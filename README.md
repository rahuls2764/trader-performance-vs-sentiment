# 📊 Trader Performance vs Market Sentiment – Analysis Project

This project explores how **trader performance on Hyperliquid** varies based on **Bitcoin market sentiment**, using the Bitcoin Fear & Greed Index. The goal is to uncover behavioral patterns and generate insights that can inform smarter trading strategies.

---

## 📁 Datasets Used

### 1. Historical Trader Data from Hyperliquid
- Contains trade-level execution data including:
  - `Account`, `Coin`, `Execution Price`, `Size USD`, `Side` (Long/Short), `Closed PnL`, etc.
  - Timestamps of trades (in IST)

### 2. Bitcoin Fear & Greed Index
- Provides daily classification of market sentiment:
  - `Extreme Fear`, `Fear`, `Neutral`, `Greed`, `Extreme Greed`
- Used to link trader behavior with market emotion on the same dates.

---

## 🔄 Data Processing

- Converted `Timestamp IST` to standardized datetime format
- Extracted trade **dates** from timestamp for alignment with sentiment data
- Merged both datasets on the `date` column
- Cleaned and verified alignment of time ranges

---

## 📈 Analysis Performed

### ✅ 1. **PnL by Sentiment**
- Grouped trades by market sentiment
- Calculated:
  - Average **Closed PnL**
  - Total number of trades
  - Average **trade size** in USD
- Insights:
  - Highest average PnL occurred under **Extreme Greed**
  - **Fearful markets** still showed strong profit potential

### ✅ 2. **Win Rate Analysis**
- Defined profitable trades as `Closed PnL > 0`
- Calculated **percentage of winning trades** for each sentiment class
- Insights:
  - Win rate remained consistent or improved in **Extreme Fear**
  - Traders maintained discipline across emotional extremes

### ✅ 3. **Long vs Short Performance**
- Grouped trades by sentiment and `Side` (Long or Short)
- Measured average PnL for each
- Insights:
  - In **Greedy** markets, **Longs** performed stronger
  - In **Fearful** markets, **Shorts** were often more profitable

---

## 🔍 Key Findings

- Traders tended to be more profitable during **Extreme Greed**, but **opportunities still existed** in Fearful markets.
- **Win rates** stayed strong across emotions, suggesting trader confidence or algorithmic discipline.
- Strategy side (long/short) significantly affects outcome depending on sentiment — this can inform dynamic strategy tuning.

---

## 📁 Files Included

- `market_sentiment_analysis.ipynb`: Full analysis notebook with code, plots, and comments
- `README.md`: Project summary and context

---

## 📊 Tools Used

- Python with Pandas and Matplotlib
- Google Colab
- GitHub for version control and sharing



Thanks for reviewing!
