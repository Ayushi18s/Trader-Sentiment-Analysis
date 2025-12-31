# Trader-Sentiment-Analysis

## Overview
This project analyzes the relationship between **Bitcoin market sentiment (Fear vs Greed)** and **trader performance** using historical trade data from Hyperliquid and the Bitcoin Fear & Greed Index.

The objective is to understand how market sentiment influences trader profitability, win rate, and trading behavior, and to extract insights that can help improve trading strategies.

---

## Datasets

### Bitcoin Market Sentiment Dataset
- Source: Bitcoin Fear & Greed Index
- Columns:
  - `date`
  - `classification` (Fear / Greed)

### Historical Trader Data (Hyperliquid)
- Columns include:
  - `Account`
  - `Timestamp IST`
  - `Closed PnL`
  - `Size USD`
  - `Execution Price`
  - `Fee`
  - `Side`, `Direction`, and other trade attributes

---

## Objectives
- Merge trader activity data with daily market sentiment
- Compare trader performance under Fear vs Greed conditions
- Analyze:
  - Average profit and loss
  - Win rate
  - Trade frequency
- Identify consistently profitable traders
- Visualize performance patterns across market sentiment

---

## Methodology

1. **Data Cleaning**
   - Parsed `Timestamp IST` in `DD-MM-YYYY HH:MM` format
   - Normalized dates to `YYYY-MM-DD`
   - Converted numeric columns and handled missing values

2. **Data Integration**
   - Merged trader and sentiment datasets using normalized dates

3. **Feature Engineering**
   - Created a Win/Loss indicator based on `Closed PnL`

4. **Exploratory Data Analysis**
   - Average PnL by market sentiment
   - Win rate comparison
   - Trade count analysis

5. **Visualization**
   - Bar charts for average PnL and win rate
   - Boxplot for PnL distribution
   - Trader-level performance insights

---

## Key Insights
- Trader performance differs noticeably between Fear and Greed phases
- Market sentiment influences risk-taking and trading frequency
- Greed periods generally show higher activity, while Fear periods show increased volatility
- A small group of traders remains profitable across different market conditions

---

## Technologies Used
- Python
- Pandas
- Matplotlib
- Seaborn

---

## How to Run

1. Clone the repository:
```bash
git clone <repository-url>
cd trader-sentiment-analysis
