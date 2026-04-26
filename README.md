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

---

## 🤖 Models & Evaluation

Three regression models were built and compared to find the best predictor of product sales.

### Models Compared

| Model | R² (Train) | R² (Test) | MAE (Test) |
|-------|-----------|----------|------------|
| Linear Regression | 0.56 | 0.57 | ~$847 |
| Default Random Forest | 0.93 | 0.55 | ~$762 |
| **Tuned Random Forest** ✅ | **0.72** | **0.59** | **$741** |

### Preprocessing Pipeline
- Missing values handled using median imputation
- Categorical features encoded using One-Hot Encoding
- Numerical features scaled using StandardScaler
- Best hyperparameters found via GridSearchCV:
  - `max_depth = 10` | `n_estimators = 200` | `max_features = 1.0` | `min_samples_leaf = 1`

---

## 📈 Linear Regression — Top Coefficients

<img width="800" alt="Coefficients Plot" src="تنزيل (1).png"/>

### Interpretation
The coefficients plot reveals which features have the **strongest positive or negative impact** on predicted sales according to the Linear Regression model:

**Positive Impact (increases sales):**
- 🏪 **Store_Type_Supermarket Type3** (+1,611) — The single most powerful positive predictor. Supermarket Type3 stores generate significantly higher sales than any other store type
- 💰 **Max_Price** (+984) — Higher-priced items consistently drive more revenue
- 🐟 **Category_Seafood** (+300) — Seafood products outperform most other categories
- 🏬 **Store_Type_Supermarket Type1** (+236) — Also performs above average

**Negative Impact (decreases sales):**
- 🛒 **Store_Type_Grocery Store** (-1,733) — The strongest negative predictor. Grocery stores generate far lower sales than supermarkets
- 🥛 **Category_Dairy** (-123) — Dairy products tend to have lower average sales
- 🏪 **Store_Type_Supermarket Type2** (-114) — Underperforms compared to Type1 and Type3

**Key Takeaway:** Store type has the most dramatic impact on sales — far greater than product category or price alone.

---

## 🌲 Random Forest — Feature Importances

<img width="800" alt="Feature Importances" src="تنزيل (1).png"/>

### Interpretation
The feature importance plot shows which features the Random Forest model **relies on most** when making predictions:

| Rank | Feature | Importance | Insight |
|------|---------|------------|---------|
| 1 | **Max_Price** | ~0.44 | By far the most important feature — price drives nearly half of the model's predictions |
| 2 | **Store_Type_Grocery Store** | ~0.19 | Being a Grocery Store significantly impacts sales (negatively) |
| 3 | **Visibility** | ~0.10 | More shelf visibility than the linear model suggested |
| 4 | **Store_Type_Supermarket Type3** | ~0.05 | High-performing store format |
| 5 | **Weight** | ~0.05 | Product weight plays a small but measurable role |

**Key Takeaway:** Unlike the coefficients plot, the Random Forest confirms that **Max_Price alone accounts for ~44% of predictive power** — making it the single most actionable lever for retailers.

---

## 🏆 Recommended Model — Tuned Random Forest

The **Tuned Random Forest** achieved the best balance between accuracy and reliability:

- **R² = 0.59** — explains 59% of the variation in product sales
- **MAE = $741** — predictions are off by ~$741 on average
- **Well-balanced** — training (0.72) vs test (0.59) shows no severe overfitting

The Default Random Forest had a training R² of 0.93 but only 0.55 on test — a clear sign of overfitting that GridSearchCV corrected.

---

## 💡 Final Recommendations for Stakeholders

Based on both models' insights, here are the key recommendations:

1. **Prioritize pricing strategy** — Max Price is the #1 driver of sales in both models. Products with higher price points consistently outperform lower-priced alternatives.

2. **Invest in Supermarket Type3 locations** — These stores generate the highest sales by a wide margin. Expanding presence in this format would have the greatest revenue impact.

3. **Reassess Grocery Store strategy** — Grocery stores are the strongest negative predictor of sales. Consider whether the product mix or pricing needs adjustment for this channel.

4. **Improve product visibility** — The Random Forest identified Visibility as the 3rd most important feature (~10% importance). Better shelf placement could meaningfully boost sales for underperforming products.

5. **Focus on high-value categories** — Seafood and Supermarket-exclusive products consistently outperform. Expanding these categories in high-performing stores could maximize revenue.

---

## 📬 Connect

**Doha Al-Nabahin**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/doha-samir12)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat-square&logo=github)](https://github.com/dohaalnabahin)

---

*Self-directed Data Science Project | 2025 - 2026*
