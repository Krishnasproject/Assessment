# **Trader Behavior \& Market Sentiment Analysis**

\## 📌 Project Overview

This project analyzes the relationship between \*\*Bitcoin Market Sentiment\*\* (Fear \& Greed Index) and \*\*Trader Behavior\*\* (Profitability, Volume, and Risk). The objective is to uncover hidden patterns in how traders react to emotional market signals and to identify potential contrarian trading strategies.



\## 📂 Repository Structure

The submission follows the required directory structure:



```text

ds\_<candidate\_name>/

├── notebook\_1.ipynb          # Main analysis notebook (Google Colab)

├── ds\_report.pdf             # Final summary report with insights \& visualizations

├── README.md                 # Project documentation (this file)

├── csv\_files/

│   ├── historical\_data.csv   # Raw high-frequency trader data

│   ├── fear\_greed\_index.csv  # Raw sentiment data

│   └── merged\_daily\_data.csv # Processed dataset (daily aggregation)

└── outputs/

&nbsp;   ├── pnl\_by\_sentiment.png        # Chart: Profitability analysis

&nbsp;   ├── volume\_by\_sentiment.png     # Chart: Volume analysis

&nbsp;   ├── risk\_by\_sentiment.png       # Chart: Position size (risk) analysis

&nbsp;   ├── buy\_sell\_trend.png          # Chart: Buy vs. Sell pressure

&nbsp;   └── market\_trend\_analysis.png   # Chart: Price vs. Sentiment trend



###### **3 Setup \& Usage**

* Environment: The analysis was performed using Google Colab.
* Dependencies: Python 3.x, Pandas, Matplotlib, Seaborn.
* How to Run: Open notebook\_1.ipynb.
* Upload the datasets from the csv\_files/ directory to the runtime.
* Run all cells sequentially to reproduce the data cleaning, aggregation, and visualizations.



###### **4 Methodology**

###### Data Preprocessing:



1. Historical Data: Converted Unix timestamps (ms) to UTC dates. Verified data integrity.
2. Sentiment Data: Standardized mixed date formats to align with trading data.
3. Aggregation:
4. High-frequency trading data was aggregated to daily intervals.
5. Key metrics calculated: Total PnL, Total Volume, Trade Count, and Average Position Size.
6. Merging: Performed an inner join on the date column to align trader actions with market sentiment.



##### **5 Data Limitations**

* Missing Leverage Data: The provided historical\_data.csv did not contain the expected 'leverage' column. 'Size USD' (Position Size) was used as a proxy for risk-taking behavior.
* Limited Data Overlap: The intersection between the Trader Data and Sentiment Data resulted in only 6 overlapping days. Insights regarding "Fear" vs. "Greed" are based on specific high-volatility events within this window rather than long-term statistical trends.



##### **6Key Insights**

* "Panic = Profit": The highest trading volume and realized PnL occurred during the "Fear" sentiment, suggesting a capitulation event where sophisticated traders absorbed sell pressure.
* Contrarian Signal: Traders remained net buyers during "Fear" periods, contradicting the assumption of panic selling.

notebook url  :"https://colab.research.google.com/drive/1dCEwDM6c2_jb_hssR8w0ay9WlCCvKpQP?usp=sharing"





**Author: Krishnanand Jha Date:20 November 2025**

