# 🛒 Prediction of Product Sales

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green?style=flat-square&logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-teal?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)

> Analyzing food item sales across retail stores to identify the key factors that drive product sales.

---

## 📌 Project Overview

Retail businesses generate massive amounts of sales data, but understanding **what drives product performance** remains a challenge. This project dives into a food retail dataset to uncover patterns, clean messy data, and visualize the factors that influence sales — helping retailers make smarter, data-driven decisions.

---

## 🎯 Objectives

- ✅ Explore and understand the structure of the dataset
- ✅ Clean and prepare the data for analysis
- ✅ Handle missing values and inconsistent categories
- ✅ Create visualizations to uncover patterns
- ✅ Identify relationships between product/outlet characteristics and sales

---

## 🛠️ Tools & Libraries

```python
Language    : Python 3.10
Libraries   : Pandas, Matplotlib, Seaborn
Environment : Google Colab
```

---

## 📊 Exploratory Data Analysis

### 1️⃣ Distribution of Numerical Features

<img width="1241" alt="Histograms" src="https://github.com/user-attachments/assets/9b07ee12-6881-42da-bd77-b29311ac9eec"/>

**Key Findings:**
- 📈 **Sales** are **right-skewed** — most products have lower sales, while a few achieve very high sales
- 👁️ **Visibility** is concentrated near zero — many items have low in-store visibility
- ⚖️ **Weight** follows a roughly normal distribution across products

---

### 2️⃣ Correlation Heatmap

<img width="515" alt="Heatmap" src="https://github.com/user-attachments/assets/d9ad4110-b1ad-4b97-97a1-f66fc708fd7d"/>

**Key Findings:**

| Relationship | Correlation | Insight |
|---|---|---|
| Max Price ↔ Sales | **+0.57** (Strong) | Higher-priced products tend to generate higher sales |
| Weight ↔ Sales | ~0 (Weak) | Weight has minimal impact on sales |
| Visibility ↔ Sales | ~0 (Weak) | Visibility alone is not a strong sales predictor |

---

## 💡 Key Takeaways

- **Price is the strongest predictor** of sales in this dataset
- **Visibility and Weight** show weak correlations with sales — suggesting other factors matter more
- Sales distribution is skewed, which is important to consider when building predictive models

---

## 📬 Connect

**Doha Al-Nabahin**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/doha-samir12)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat-square&logo=github)](https://github.com/dohaalnabahin)

---

*Prediction of Product Sales Data Science Project | 2025 - 2026*
