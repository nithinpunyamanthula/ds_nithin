# ds_nithin
📊 Bitcoin Sentiment vs Trader Performance — Machine Learning Analysis

A full end-to-end data science project exploring how Bitcoin market sentiment influences trading performance on the Hyperliquid platform.

🚀 Project Overview

This project analyzes two datasets:

Bitcoin Market Sentiment (Fear–Greed Index)

Columns: Date, Classification

Hyperliquid Historical Trade Data

Columns: Account, Symbol, Execution Price, Size Tokens,
Size USD, Side, Timestamp, Start Position, Event,
ClosedPnL, Fee, Trade ID, etc.

🎯 Objective

To uncover how market sentiment affects trader behavior and profitability, identify hidden patterns, and build a machine-learning model to predict trade success.

This project delivers:

A complete data cleaning workflow

Feature engineering

Exploratory data analysis

Machine learning modeling using CatBoost

Optuna hyperparameter tuning

Final performance evaluation (92% accuracy)

Actionable trading insights & recommendations

📁 Dataset Links

Trader Data:
https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view

Bitcoin Fear–Greed Index:
https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view

🛠️ Tech Stack

Python

Pandas, NumPy

Matplotlib, Seaborn

CatBoost

Optuna (hyperparameter tuning)

Scikit-learn

Jupyter Notebook

🔄 Project Workflow
1. Data Cleaning

Standardized column names

Converted timestamps

Removed duplicates

Handled missing values

Extracted date/time features

Merged sentiment data with trade data

2. Feature Engineering

Created new predictive features:

value = ExecutionPrice × SizeTokens

volatility (rolling std)

exposure = SizeUSD

hour, day_of_week

Encoded sentiment as 0 = Fear, 1 = Greed

3. Exploratory Data Analysis (EDA)

Identified several patterns:

Win rates are higher during Greed periods

Traders take larger positions during Fear

Best performance occurs between 08:00–11:00 IST

High volatility reduces profitability

4. Machine Learning

Models tested:

Logistic Regression

Random Forest

Gradient Boosting

CatBoost (best)

5. Optuna Hyperparameter Tuning

Best parameters discovered:

iterations: 1800
depth: 11
learning_rate: 0.1807
l2_leaf_reg: 6.00
random_strength: 0.6658
bagging_temperature: 0.5401
subsample: 0.8538
rsm: 0.9426

6. Final Model Performance

The tuned CatBoost model achieves:

Metric	Score
Accuracy	92.1%
Precision (Class 0)	0.93
Precision (Class 1)	0.91
Recall (Class 0)	0.94
Recall (Class 1)	0.90
📌 Key Insights

Trades during Greed sentiment yield the highest profitability.

Traders oversize during Fear, increasing risk.

Morning trades (8–11 AM IST) show higher success rates.

Volatility and fees strongly affect profitability.

The ML model can reliably predict trade outcomes based on engineered features.

🧠 Recommendations

Avoid oversized trades during Fear periods

Increase activity during Greed sentiment

Focus on trades between 08:00–11:00 IST

Use volatility filters to reduce losses

Deploy the 92% CatBoost model into a real-time alert system

ds_nithin/
├── notebook_1.ipynb
├── csv_files/
│   └── *.csv                    (your datasets + processed CSVs)
├── outputs/
│   └── *.png / *.jpg            (charts, plots)
├── ds_report.pdf                (summary PDF)
└── README.md                   


🏁 Conclusion

This project demonstrates a complete, real-world data science workflow for trading analytics.
With 92% prediction accuracy and explainable insights, it supports smarter decision-making in volatile crypto markets.
