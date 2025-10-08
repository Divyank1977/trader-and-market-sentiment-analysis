# Trader and MArket Sentiment Analysis — Data Science Assignment

This project explores the relationship between **trader behavior** and **market sentiment** (Fear vs Greed) using real historical trading data and Bitcoin market sentiment indices.  
It is part of the **Web3 Trading Team Data Science Assessment**.

---

##  Project Structure
ds_Divyank/
├── notebook_1.ipynb # Main analysis and modeling notebook (Google Colab)
├── csv_files/ # Cleaned and intermediate datasets
│ ├── trader_data_cleaned.csv
│ ├── sentiment_data_cleaned.cs│
├── outputs/ # All generated charts, plots, and visual summaries
├── ds_report.pdf # Final summarized insights and explanations
└── README.md # Project overview, setup, and references


---

##  Objective

To analyze how **trading performance metrics** — such as **profitability, leverage, exposure** — align or diverge from the **overall market sentiment** (Fear vs Greed).  
The goal is to identify hidden behavioral signals that can guide **data-driven trading strategies**.

---

##  Datasets

1. **Bitcoin Market Sentiment Dataset**  
   - Columns: `Date`, `Classification` (Fear / Greed)

2. **Hyperliquid Trader Data**  
   - Columns: `account`, `symbol`, `execution_price`, `size`, `side`, `time`, `start_position`, `event`, `closedPnL`, `leverage`, etc.

**Dataset Links:**  
- [Historical Trader Data](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)  
- [Fear & Greed Index](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing)

---

##  Methodology

1. **Data Preprocessing**  
   - Converted UNIX timestamps to readable formats  
   - Cleaned inconsistent entries and merged both datasets by `date`  
   - Created derived columns:  `signed_pnl`, `notional`, `exposure`,  and `effective_leverage`

2. **Exploratory Data Analysis (EDA)**  
   - Distribution plots for PnL, leverage, and position sizes  
   - Boxplots of PnL segmented by sentiment (`Fear`, `Greed`, `Neutral`)  
   - Daily average PnL trends and sentiment flips analysis

3. **Feature Engineering & Modeling**  
   - Encoded categorical variables ( `classification`) using dummies  
   - Applied OLS regression to evaluate relationships between `signed_pnl` and explanatory variables (`leverage`, `notional`)  
   - Performed t-tests to compare mean profitability across sentiment categories

4. **Insights Generation**  
   - Quantified trader risk–return behavior under different market sentiments  
   - Detected structural shifts when sentiment flipped (Fear → Greed or vice versa)  
   - Identified behavioral biases in position sizing and leverage usage

---

## Key Visuals (in `/outputs`)

| Plot | Description |
|------|--------------|
| `pnl_by_sentiment.png` | PnL distribution by sentiment |
| `leverage_distribution.png` | Leverage levels under Fear vs Greed |
| `regression_summary.png` | Regression coefficients and significance |

---

##  Tools & Technologies

- **Languages:** Python (Pandas, NumPy, Scikit-learn)  
- **Visualization:** Matplotlib, Seaborn  
- **Analysis:** Statsmodels (OLS, t-tests)  
- **Data Handling:** SQL, Google Colab, CSV  
- **Version Control:** Git, GitHub  
- **Cloud:** Google Drive for dataset access  

---

##  How to Run

1. Open the [Google Colab Notebook](https://colab.research.google.com/)  
2. Run cells sequentially to reproduce analysis and visual outputs  
3. Final insights and explanations are summarized in `ds_report.pdf`

---

##  Author

**Divyank Goyal**  
B.Tech CSE — Guru Jambeshwar University, Hisar (2021–2025)  
📧 [divyank1977@gmail.com](mailto:divyank1977@gmail.com)  
🔗 [Portfolio](https://divyank.lovable.app) • [LinkedIn](https://linkedin.com/in/divyankgoyal) • [GitHub](https://github.com/Divyank1977)

---

##  Submission Compliance

✅ Directory follows standardized format  
✅ Google Colab notebooks shared with view access  
✅ Visuals and report included  
✅ Code and structure mirror GitHub repository standards  

---



