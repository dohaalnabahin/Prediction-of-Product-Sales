# 🛒 Prediction of Product Sales

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green?style=flat-square&logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-teal?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

> Analyzing food item sales across retail stores to identify the key factors that drive product sales — and building a predictive model to forecast future performance.

---

## 📌 Project Overview

Retail businesses generate massive amounts of sales data, but understanding **what drives product performance** remains a challenge. This project dives into a food retail dataset to uncover patterns, clean messy data, and visualize the factors that influence sales — helping retailers make smarter, data-driven decisions.

**Business Question:**
> Which product and outlet characteristics have the greatest impact on sales?

---

## 🔍 Key Insights from the Data

### 1️⃣ Sales Distribution is Right-Skewed

<img width="1241" alt="Histograms" src="https://github.com/user-attachments/assets/9b07ee12-6881-42da-bd77-b29311ac9eec"/>

Most products generate relatively low sales, while a small number of high-performing products achieve significantly higher revenue. This skewed distribution suggests that a small subset of products drives a disproportionate share of total sales — a critical insight for inventory and marketing decisions.

Additionally, many items have near-zero visibility in stores, which raises the question: **does low visibility hurt sales?**

---

### 2️⃣ Price is the Strongest Driver of Sales

<img width="515" alt="Heatmap" src="https://github.com/user-attachments/assets/d9ad4110-b1ad-4b97-97a1-f66fc708fd7d"/>

The correlation heatmap reveals a strong positive relationship between **Max Price and Sales (r = 0.57)** — meaning higher-priced products tend to generate more revenue. In contrast, **Weight and Visibility** show near-zero correlation with sales, suggesting that pricing strategy plays a far more significant role than product size or shelf placement alone.

---

## 🤖 Model & Evaluation

### Model Used
A **Linear Regression** model was built to predict item sales based on product and outlet features.

### Preprocessing
- Missing values handled using median imputation for numerical features
- Categorical features encoded using One-Hot Encoding
- Features scaled using StandardScaler

### Model Performance

| Metric | Training Set | Test Set |
|--------|-------------|----------|
| R² Score | 0.56 | 0.57 |
| MAE | ~847 | ~804 |
| RMSE | ~1,082 | ~1,057 |

### Key Finding
The model explains approximately **57% of the variance in sales**, with **Max Price** emerging as the most influential predictor. While the model provides a solid baseline, future iterations could explore tree-based models to capture non-linear relationships in the data.

---

## 💡 Recommendations

- **Focus on pricing strategy** — it has the strongest measurable impact on sales
- **Investigate low-visibility products** — improving shelf placement could unlock untapped revenue
- **Prioritize high-performing outlet types** — certain store formats consistently outperform others

---

## 📬 Connect

**Doha Al-Nabahin**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/doha-samir12)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat-square&logo=github)](https://github.com/dohaalnabahin)

---

*Prediction of Product Sales | 2025 - 2026*
