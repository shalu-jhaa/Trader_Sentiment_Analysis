# Trader_Sentiment_Analysis
# Trader Sentiment Analysis 

## Overview
This repository contains the analysis of **Bitcoin market sentiment** and **historical trader performance** from Hyperliquid.  
The objective of this assignment is to explore the relationship between trader performance (PnL) and market sentiment (Fear/Greed Index), uncover patterns, and provide actionable insights.

---

## Datasets
1. **Bitcoin Market Sentiment Dataset**  
   - Columns: `Date`, `Classification` (Fear/Greed), `Value/Index`  
   - Source: [Fear Greed Index](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing)

2. **Historical Trader Data**  
   - Columns include: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `closedPnL`, `leverage`, etc.  
   - Source: [Hyperliquid Historical Data](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)

---

## Analysis Steps
1. **Data Preparation**  
   - Load datasets and detect roles (sentiment vs trader) automatically.  
   - Parse timestamps and normalize dates for merging.  
   - Shift sentiment data to align with trader data if needed.  

2. **Merging Data**  
   - Merge trader dataset with sentiment dataset on `date`.  
   - Select sentiment columns for analysis (`Classification` label and numeric index).  

3. **Feature Engineering**  
   - Identify key numeric features such as `closedPnL` and `trade size`.  
   - Aggregate daily statistics: average PnL, average sentiment, trade counts per account/day.  

4. **Exploratory Data Analysis (EDA)**  
   - Boxplots of PnL by sentiment label  
   - Daily time series plots of average PnL vs sentiment index  
   - Correlation and Granger causality tests (limited by dataset size/variability)

---

## Key Insights
- Trader performance (PnL) tends to be higher on **“Greed”** days and lower on **“Fear”** days.  
- Boxplots show variability in PnL for different sentiment classifications.  
- Limited dataset size prevents strong statistical conclusions from lagged correlation or Granger causality tests.  
- Recommendations:
  - Collect more historical data for statistically meaningful analysis.  
  - Explore additional trader features (leverage, size, account type) for deeper insights.  
  - Use this foundation for predictive modeling or smarter trading strategies.

---

## Files
- `Trader_Sentiment_Analysis.ipynb` – Jupyter notebook containing full analysis, plots, and insights  
- `outputs/` – Folder containing merged datasets, summary tables, and generated plots

---

## Conclusion
This assignment demonstrates the relationship between market sentiment and trader performance, providing a basis for **smarter trading strategies** in the crypto market.  

---
