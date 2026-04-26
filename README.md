# 🛒 Prediction of Product Sales

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green?style=flat-square&logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3-orange?style=flat-square&logo=scikit-learn)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-teal?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

> Analyzing food item sales across retail stores to identify the key factors that drive product sales — and building predictive models to forecast future performance.

---

## 📌 Project Overview

Retail businesses generate massive amounts of sales data, but understanding **what drives product performance** remains a challenge. This project analyzes a food retail dataset containing **8,523 records** across multiple store types and locations — uncovering patterns, cleaning messy data, and building regression models to predict product sales.

**Business Question:**
> Which product and outlet characteristics have the greatest impact on sales — and can we reliably predict future sales?

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| Records | 8,523 products |
| Features | 11 (product & outlet characteristics) |
| Target | `Item_Outlet_Sales` — product sales in dollars |
| Key Features | Max Price, Item Type, Store Type, Store Location |

---

## 🔍 Key Insights from the Data

### 1️⃣ Sales Distribution is Right-Skewed

<img width="1241" alt="Histograms" src="https://github.com/user-attachments/assets/9b07ee12-6881-42da-bd77-b29311ac9eec"/>

Most products generate relatively low sales, while a small number of high-performing products achieve significantly higher revenue. This skewed distribution suggests that a small subset of products drives a disproportionate share of total sales — a critical insight for inventory and marketing decisions.

Additionally, many items have **near-zero visibility** in stores, raising the question: does low shelf visibility hurt sales?

---

### 2️⃣ Price is the Strongest Driver of Sales

<img width="515" alt="Heatmap" src="https://github.com/user-attachments/assets/d9ad4110-b1ad-4b97-97a1-f66fc708fd7d"/>

| Relationship | Correlation | Insight |
|---|---|---|
| Max Price ↔ Sales | **+0.57** (Strong) | Higher-priced products generate more revenue |
| Weight ↔ Sales | ~0 (Weak) | Product weight has minimal impact on sales |
| Visibility ↔ Sales | ~0 (Weak) | Shelf visibility alone is not a strong predictor |

**Pricing strategy** plays a far more significant role than product size or shelf placement in driving sales.

---

## 🤖 Models & Evaluation

Three regression models were built and compared to find the best predictor of product sales.

### Models Compared

| Model | R² (Train) | R² (Test) | MAE (Test) |
|-------|-----------|----------|------------|
| Linear Regression | 0.56 | 0.57 | ~847 |
| Default Random Forest | 0.93 | 0.55 | ~762 |
| **Tuned Random Forest** ✅ | **0.72** | **0.59** | **$741** |

### Preprocessing Pipeline
- Missing values handled using median imputation
- Categorical features encoded using One-Hot Encoding
- Numerical features scaled using StandardScaler
- Best hyperparameters found via GridSearchCV:
  - `max_depth = 10`
  - `n_estimators = 200`
  - `max_features = 1.0`
  - `min_samples_leaf = 1`

---

## 🏆 Recommended Model — Tuned Random Forest

The **Tuned Random Forest** achieved the best balance between accuracy and reliability:

- **R² = 0.59** — explains 59% of the variation in product sales
- **MAE = $741** — predictions are off by ~$741 on average
- **Well-balanced** — training score (0.72) vs test score (0.59) shows minimal overfitting

The Default Random Forest had a training R² of 0.93 but only 0.55 on test data — a clear sign of overfitting. Tuning with GridSearchCV corrected this and improved generalization.

---

## 💡 Recommendations for Stakeholders

- **Invest in pricing strategy** — Max Price has the strongest measurable impact on sales
- **Investigate low-visibility products** — improving shelf placement could unlock untapped revenue
- **Prioritize high-performing outlet types** — certain store formats consistently generate higher sales
- **Focus on high-margin product categories** — not all product types perform equally across store locations

---

## 📬 Connect

**Doha Al-Nabahin**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/doha-samir12)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat-square&logo=github)](https://github.com/dohaalnabahin)

---

*Self-directed Data Science Project | 2025 - 2026*
