# 📊 Trader Performance vs Market Sentiment (Hyperliquid)

## 🔍 Objective

Analyze how Bitcoin market sentiment (Fear/Greed) influences trader behavior and performance on Hyperliquid.
The goal is to uncover patterns that can inform smarter, data-driven trading strategies.

---

## 📁 Datasets Used

### 1. Bitcoin Market Sentiment

* Columns: Date, Classification (Fear / Greed)
* Provides daily sentiment labels

### 2. Historical Trader Data (Hyperliquid)

* Includes: account, symbol, execution price, size, side, time, closedPnL, etc.
* Used to compute trader-level performance and behavior metrics

---

## ⚙️ Methodology

### 🧹 Data Preparation

* Cleaned datasets (duplicates, missing values)
* Converted timestamps to daily format
* Merged trader data with sentiment data on date

### 📊 Feature Engineering

Created key metrics:

* Daily PnL per trader
* Win rate
* Average trade size
* Trade frequency
* Long/short ratio
* Drawdown proxy

### 📈 Analysis

* Compared trader performance across **Fear vs Greed regimes**
* Analyzed behavior changes (trade size, frequency, directional bias)
* Conducted statistical testing (**Mann-Whitney U Test**)

### 🧠 Segmentation

Traders were grouped into:

* Low / Mid / High size traders
* Low / High frequency traders
* Consistent / Average / Inconsistent traders

### 🤖 Bonus

* Clustering (KMeans) to identify behavioral archetypes
* Correlation analysis

---

## 📊 Key Insights

1. **Fear increases risk, not necessarily losses**
   → PnL variability is higher during Fear regimes

2. **Large traders are more sensitive to sentiment**
   → High-size traders show stronger performance swings

3. **More trading ≠ better results**
   → Increased activity during Greed does not guarantee higher win rates

4. **Segment-level analysis is more meaningful than averages**
   → Different trader types respond differently to sentiment

---

## 💡 Strategy Recommendations

* **Reduce position size during Fear regimes**
  → Helps control volatility and drawdowns

* **Increase exposure selectively during Greed**
  → Focus on traders with consistent performance

---

## ⚠️ Limitations

* The dataset does **not include explicit leverage**
  → Trade size and frequency are used as proxies for aggressiveness

* Sentiment is available only at daily level (no intraday granularity)

* The analysis identifies relationships, not causation

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

## 📂 Repository Contents

* `notebook.ipynb` → Full analysis
* `outputs.zip` → Charts and tables
* `README.md` → Project overview

---

## 🚀 How to Run

1. Open the notebook in Google Colab or Jupyter
2. Upload the datasets
3. Run all cells sequentially

---

## 📌 Conclusion

Market sentiment significantly impacts trader behavior, primarily through **risk and variability rather than consistent profitability**.

Segment-based strategies provide more actionable insights than one-size-fits-all rules.
