 `reports/draft_report.md` — Working Narrative (Technical but readable)

# US Superstore Sales Analysis & Forecasting — Draft Report

## 1. Introduction

This project analyzes U.S. retail sales data from 2019 to uncover performance drivers, customer behavior patterns, and product-level trends, and to develop a machine learning model capable of forecasting monthly product sales. The goal is to support data-driven decision-making in inventory planning, demand forecasting, and revenue optimization.

---

## 2. Business Objectives

- Understand overall sales performance and seasonal trends.
- Identify top-performing products and locations.
- Quantify revenue concentration and operational risk.
- Build and evaluate a predictive model for monthly product sales.
- Translate analytical results into actionable business recommendations.

---

## 3. Data Overview

The dataset contains transactional retail sales records for 2019, including order details, product information, pricing, timestamps, and customer locations. Data cleaning steps included removing missing values, correcting malformed timestamps, and engineering features such as total sales, city, state, and time-based variables.

---

## 4. Exploratory Data Analysis (EDA)

Key findings from exploratory analysis include:

- Total revenue reached approximately $34.5M across over 178,000 orders and more than 209,000 units sold.
- Sales increased steadily throughout the year, peaking sharply in Q4, with December being the highest-performing month.
- A small number of high-value electronic products accounted for a disproportionate share of total revenue.
- California emerged as the top-performing state, with cities such as San Francisco and Los Angeles leading in revenue.
- Customer purchasing activity peaked during late morning and early evening hours, with relatively stable demand across days of the week.

---

## 5. Feature Engineering

To support modeling, sales were aggregated at the product-month level. Additional features included:

- Time-based features: month number, quarter.
- Lag features: previous 1–2 months’ sales.
- Rolling statistics: 3-month rolling averages.

These features were designed to capture temporal patterns and improve predictive performance.

---

## 6. Modeling Approach

Two models were trained and evaluated:

- Linear Regression as a baseline model.
- Random Forest Regressor as a nonlinear ensemble model capable of capturing complex relationships.

A time-based train-test split was used to preserve chronological order and avoid data leakage.

---

## 7. Model Evaluation

The Random Forest model outperformed Linear Regression across all evaluation metrics:

- Lower MAE and RMSE, indicating smaller average and extreme prediction errors.
- Higher R², indicating stronger explanatory power.

However, diagnostic analysis revealed systematic underprediction, particularly for high-volume products, and increasing variance at higher sales values.

---

## 8. Business Implications

- Inventory Risk: Systematic underprediction increases the risk of understocking during peak periods.
- Revenue Concentration: Heavy reliance on a small number of products increases vulnerability to supply disruptions.
- Regional Strategy: Strong performance in California highlights opportunities for geographic expansion.
- Demand Planning: Predictable purchasing behavior can inform staffing, logistics, and promotional timing.

---

## 9. Model Limitations & Next Steps

The current model is trained on a single year of historical data, limiting its ability to capture long-term trends and unusual events. The Random Forest model also demonstrates systematic bias toward underpredicting high sales values, which could negatively impact inventory planning for peak-demand products.

Future improvements include:

- Expanding the dataset to include multiple years of historical sales.
- Incorporating external variables such as promotions, holidays, pricing changes, and marketing campaigns.
- Implementing specialized time-series models (e.g., SARIMA, Prophet, or LSTM).
- Performing hyperparameter optimization and cross-validation to improve generalization.

---

## 10. Conclusion

This project demonstrates the full data analytics and data science lifecycle, from business problem framing and data cleaning to modeling, evaluation, and business reporting. The Random Forest model provides a strong foundation for demand forecasting, and the insights generated offer actionable guidance for inventory management, revenue optimization, and strategic growth.
