# US Superstore Sales Analysis & Forecasting - Final Report

### Executive Summary

This analysis evaluates U.S. retail sales data from 2019 to uncover performance drivers, customer behavior patterns, and product-level trends, and to develop a machine learning model to forecast monthly product sales. The project integrates descriptive analytics, feature engineering, and predictive modeling to support inventory planning and revenue optimization.

Key findings reveal strong Q4 seasonality, heavy revenue concentration among a small number of high-value products, and predictable demand patterns across most product categories. A Random Forest forecasting model outperformed linear approaches, achieving lower error and higher explanatory power, though it systematically underpredicts high-volume sales.

These insights provide actionable guidance for inventory management, demand planning, and strategic growth while identifying clear opportunities for model and data improvements.

---

### Business Objectives

1. Understand overall sales performance and seasonal trends.
2. Identify top-performing products and geographic regions.
3. Quantify revenue concentration risk.
4. Build a predictive model for monthly product-level demand.
5. Translate analytical results into business-ready recommendations.

---

### Data Overview

The dataset contains transactional retail sales records for the full year of 2019, including order details, product information, pricing, timestamps, and customer locations. Data cleaning and preprocessing were performed to remove missing or malformed records and to engineer time-based and geographic features.

---

### Key Insights

#### Revenue & Volume Performance  
Total annual revenue exceeded $34.5M across over 178,000 orders and more than 209,000 units sold, indicating a high-volume retail operation.

#### Seasonal Trends  
Sales increased steadily throughout the year, peaking sharply in Q4, with December as the strongest-performing month. This confirms that holiday demand is the primary revenue driver.

#### Product Performance  
Revenue is heavily concentrated among a small number of high-value electronic products, creating both strong growth drivers and concentration risk.

#### Geographic Performance  
California dominates regional performance, with cities such as San Francisco and Los Angeles contributing a significant share of total revenue.

#### Customer Behavior  
Purchasing activity peaks during late morning and early evening hours, with stable demand across days of the week.

---

### Modeling Approach

Sales were aggregated at the product-month level, and features were engineered to capture temporal patterns, including time-based variables, lagged sales, and rolling averages. Two models were trained and evaluated:

- Linear Regression (baseline)
- Random Forest Regressor (primary model)

A time-based train-test split was used to preserve chronological order and avoid data leakage.

---

### Model Performance Summary

The Random Forest model outperformed Linear Regression across all metrics:

- Lower MAE, indicating smaller average prediction errors.
- Lower RMSE, indicating fewer extreme forecasting errors.
- Higher R², indicating stronger explanatory power.

However, diagnostic analysis revealed systematic underprediction at high sales volumes and increasing variance in predictions for top-performing products.

---

### Business Implications

1. **Inventory Risk:** Underprediction increases the risk of understocking during peak demand periods, particularly in Q4.
2. **Revenue Concentration:** Heavy reliance on a small number of products increases vulnerability to supply disruptions.
3. **Regional Strategy:** Strong performance in California highlights opportunities for geographic expansion.
4. **Demand Planning:** Predictable purchasing behavior supports optimized staffing, logistics, and promotional scheduling.

---

### Model Limitations & Next Steps

The current model is limited by its reliance on a single year of historical data, restricting its ability to capture long-term trends and rare events. The Random Forest model also exhibits systematic underprediction of high sales values, which may impact inventory planning for top-performing products.

Future improvements should focus on:

- Expanding the dataset to include multiple years of sales data.
- Incorporating external drivers such as promotions, holidays, pricing changes, and marketing campaigns.
- Implementing specialized time-series forecasting models (e.g., SARIMA, Prophet, or LSTM).
- Applying hyperparameter optimization and cross-validation to improve generalization and accuracy.

---

### Final Recommendation

The Random Forest model should be adopted as the baseline forecasting tool for monthly product-level demand, with the understanding that its predictions are conservative and less reliable for high-volume products. Decision-makers should apply safety buffers when planning inventory for peak seasons.

To unlock higher business value, the organization should prioritize expanding historical data coverage, integrating external demand drivers, and transitioning to advanced time-series models. These improvements will enhance predictive accuracy, reduce operational risk, and support more confident strategic planning.