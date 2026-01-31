# US Superstore Sales Analysis & Forecasting (2019)

This project analyzes U.S. retail sales data from 2019 to uncover business insights, identify performance drivers, and build a machine learning model to forecast monthly product sales.

The primary work is contained in a structured series of Jupyter notebooks, following a full data analytics and data science workflow.

---

### 📁 Project Structure

us-superstore-analysis/
│
├── data/
│ ├── raw/
│ │ └── sales_2019.csv
│ └── processed/
│ └── cleaned_sales.csv
│ └── evaluation_results.csv
| └── feature_engineered_sales.csv
| └── model_metrics.csv
| └── model_preditions.csv
├── notebooks/
│ ├── 01_problem_definition.ipynb
│ ├── 02_data_cleaning.ipynb
│ ├── 03_eda.ipynb
│ ├── 04_feature_engineering.ipynb
│ ├── 05_modeling.ipynb
│ ├── 06_evaluation_&_diagnostics.ipynb
│ └── 07_business_report.ipynb
│
├── reports/
│ ├── draft_report.md
│ └── final_report.md
│
├── figures/
│ └── charts/
│
├── README.md
└── requirements.txt


---

### 📊 Project Overview

- **Objective:** Understand sales performance, customer behavior, and build a predictive model for monthly product demand.
- **Dataset:** U.S. retail transactional sales data (2019).
- **Tools:** Python, pandas, NumPy, matplotlib, seaborn, scikit-learn, Jupyter.

---

### Key Deliverables

| Notebook | Purpose |
|---------|---------|
| 01 | Business problem framing and analytical goals |
| 02 | Data cleaning and preprocessing |
| 03 | Exploratory data analysis (EDA) |
| 04 | Feature engineering for modeling |
| 05 | Model training (Linear Regression & Random Forest) |
| 06 | Model evaluation and diagnostics |
| 07 | Business report with insights and recommendations |

---

### 📌 Key Outcomes

- Identified strong Q4 seasonality and revenue concentration among top products.
- Built a Random Forest forecasting model that outperformed Linear Regression.
- Translated technical findings into business-ready insights and recommendations.

---

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook
Open notebooks in the notebooks/ folder in order.
---
📄 Reports

- reports/draft_report.md - Working narrative version of the analysis.

- reports/final_report.md - Polished, business-ready report extracted from notebooks.

👤 Author

Joseph M. Nwachukwu
Aspiring Data Scientist & Business Analyst
GitHub: https://github.com/jm-nwachukwu
LinkedIn: https://linkedin.com/in/jmnwachukwu
X: https://x.com/jmnwachukwu