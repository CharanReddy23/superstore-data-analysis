# 📊 Superstore Sales & Profit Analysis

> Multi-tool data analysis project uncovering revenue trends, regional performance gaps, and profit drivers across a retail superstore dataset — using Python, Excel, and Power BI.

![Python](https://img.shields.io/badge/Python-Pandas%20%7C%20Matplotlib-blue?style=flat-square&logo=python)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?style=flat-square&logo=powerbi)
![Excel](https://img.shields.io/badge/Excel-Pivot%20Tables-green?style=flat-square&logo=microsoftexcel)

---

## 📌 Project Overview

Retail businesses generate large volumes of transactional data, but raw data alone doesn't drive decisions. This project performs end-to-end analysis of a Superstore sales dataset — cleaning, exploring, and visualizing the data to answer real business questions about profitability, regional performance, and customer segments.

**Dataset:** 9,994 retail orders across 4 regions, 3 product categories, and 17 sub-categories.

---

## ❓ Business Questions Answered

1. **Which month generates the highest profit?** → Drives inventory and campaign planning
2. **Which product sub-categories are most and least profitable?** → Informs discontinuation or promotion decisions
3. **How does performance vary by region?** → Identifies where to focus sales resources
4. **What is the impact of discounts on profit?** → Reveals over-discounting patterns
5. **Who are the top customers by revenue?** → Supports account prioritization

---

## 🔍 Key Insights

| Finding | Insight |
|---|---|
| **November & December** are peak profit months | Seasonal demand — stock up early |
| **Copiers & Phones** are top sub-categories by sales | High-volume, high-margin items worth promoting |
| **Tables & Bookcases** show negative profit margins | Heavy discounting eroding profitability |
| **West region** leads in total sales | East has strong volume but lower margins |
| **Average discount in Furniture** is 2x that of Technology | Discount strategy needs review |

---

## 🛠️ Tools & Methodology

### 1. 🐍 Python (Pandas + Matplotlib) — `Superstore_Data_Analysis.ipynb`

**Data Cleaning:**
- Removed null values and duplicate records
- Converted `Order Date` to datetime format
- Engineered `Month` and `Year` columns for time-series analysis

**Analysis performed:**
```python
# Monthly profit trend
df.groupby('Month')['Profit'].sum().plot(kind='line')

# Top 5 sub-categories by sales
df.groupby('Sub-Category')['Sales'].sum().nlargest(5)

# Regional profit & sales summary
df.groupby('Region')[['Sales', 'Profit']].sum()

# Discount impact by category
df.groupby('Category')['Discount'].mean()
```

### 2. 📊 Power BI Dashboard

Interactive dashboard with:
- **KPI Cards:** Total Sales, Total Profit, Order Count, Avg Discount
- **Bar Chart:** Sales by Region and Profit by Sub-Category
- **Donut Chart:** Orders by Ship Mode
- **Customer Table:** Top 5 customers by revenue
- **Slicers:** Filter by Region, Category, and Customer Segment

![Dashboard Preview](Superstore%20Dashboard.PNG)

### 3. 📋 Excel Analysis

- Pivot tables summarizing Profit by Month, Sales by Region, Top Sub-Categories
- Conditional formatting to highlight high/low performers
- Month extraction using `TEXT(OrderDate, "MMM")` formula

---

## 📁 Repository Structure

```
├── Superstore_Data_Analysis.ipynb   # Python EDA notebook (Pandas + Matplotlib)
├── Superstore Dashboard.PNG         # Power BI dashboard screenshot
└── README.md
```

---

## 🚀 How to Run

**Python Notebook:**
```bash
# Install dependencies
pip install pandas matplotlib jupyter

# Launch notebook
jupyter notebook Superstore_Data_Analysis.ipynb
```

**Dataset:** Uses the publicly available [Superstore dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) from Kaggle.

---

## 💡 What I Learned

- Full EDA workflow: cleaning → analysis → visualization → insight
- Using Pandas `groupby`, `pivot_table`, and `datetime` operations for business analysis
- Building multi-page Power BI dashboards with cross-filtering slicers
- Translating data findings into actionable business language

---

## 👤 Author

**Kudumula Sri Charan Reddy**
[LinkedIn](https://linkedin.com/in/charan-reddyr) • [GitHub](https://github.com/CharanReddy23) • sricharanreddykudumula@gmail.com
