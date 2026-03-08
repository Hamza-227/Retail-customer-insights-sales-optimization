# 📊 Retail Customer Behavior & Sales Analytics

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/MySQL-Analysis-orange?logo=mysql&logoColor=white)
![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-green?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 🧩 Problem Statement

A retail company needed to understand **why customers buy, when they buy, and who buys most** — to improve sales strategy, reduce churn, and grow subscriptions.

> *"How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?"*

---

## 💡 Key Findings

| Insight | Finding |
|---|---|
| 💰 Gender Revenue Gap | Male customers generated **2x more revenue** ($157,890 vs $75,191) |
| 🏆 Top Rated Products | Gloves (3.86), Sandals (3.84), Boots (3.82) |
| 📦 Shipping & Spend | Express shipping users spend **~$2 more** on average |
| 🔁 Customer Loyalty | **80% of customers** are Loyal (3,116 out of 3,900) |
| 🏷️ Discount Dependency | Hat & Sneakers have ~50% discount rate — margin risk |
| 👶 Top Age Group | Young Adults contribute the highest revenue ($62,143) |
| 📋 Subscription Gap | Only **27% are subscribers** despite similar avg spend |
| 🛒 High-Value Discounters | 839 customers used discounts but still spent above average |

---

## 🗂️ Project Structure

```
📁 retail-customer-behavior-analysis/
│
├── 📓 Data_Cleaning_Python.ipynb     # Data cleaning, EDA, feature engineering
├── 🗄️ Sql_Analysis.sql               # 10 business queries in MySQL
├── 📊 DashBoard_Using_PowerBi.pbix   # Interactive Power BI dashboard
├── 📄 Project_Report.pdf             # Full written report
├── 📑 Slides.pptx                    # Stakeholder presentation
├── 📋 Business_Problem_Document.pdf  # Original problem statement
└── 📂 customer_shopping_behavior.csv # Raw dataset (3,900 rows)
```

---

## 🔧 Tools & Technologies

| Layer | Tool |
|---|---|
| Data Cleaning & EDA | Python, Pandas, NumPy, Matplotlib, Seaborn |
| Database | MySQL / PostgreSQL |
| Visualization | Power BI |
| Reporting | PDF Report + PowerPoint |

---

## 📁 Dataset Overview

- **Rows:** 3,900 purchases
- **Columns:** 18 features
- **Missing Values:** 37 in `review_rating` → imputed using category median

| Feature Type | Columns |
|---|---|
| Demographics | Age, Gender, Location, Subscription Status |
| Purchase Info | Item, Category, Amount (USD), Season, Size, Color |
| Behavior | Discount Applied, Previous Purchases, Frequency, Review Rating, Shipping Type |

---

## 🐍 Python — Data Preparation

Performed in `Data_Cleaning_Python.ipynb`:

- **Missing Data:** Imputed `review_rating` using median per product category
- **Column Standardization:** Renamed all columns to `snake_case`
- **Feature Engineering:**
  - `age_group` — binned ages into Young Adult / Adult / Middle-aged / Senior
  - `purchase_frequency_days` — derived from purchase history
- **Redundancy Check:** Validated `discount_applied` vs `promo_code_used` → dropped redundant column
- **DB Integration:** Loaded cleaned DataFrame into PostgreSQL for SQL analysis

---

## 🗄️ SQL — Business Analysis (10 Queries)

Performed in `Sql_Analysis.sql` using MySQL:

1. **Revenue by Gender** — Male: $157,890 | Female: $75,191
2. **High-Spending Discount Users** — 839 customers spent above average despite using discounts
3. **Top 5 Products by Rating** — Gloves, Sandals, Boots, Hat, Skirt
4. **Shipping Type Comparison** — Express ($60.48) vs Standard ($58.46)
5. **Subscribers vs Non-Subscribers** — 1,053 vs 2,847 customers; similar avg spend
6. **Discount-Dependent Products** — Hat (50%), Sneakers (49.66%), Coat (49.07%)
7. **Customer Segmentation** — Loyal: 3,116 | Returning: 701 | New: 83
8. **Top 3 Products per Category** — Using `ROW_NUMBER()` window function
9. **Repeat Buyers & Subscriptions** — 2,518 repeat buyers are NOT subscribed (opportunity!)
10. **Revenue by Age Group** — Young Adult leads at $62,143

---

## 📊 Power BI Dashboard

Interactive dashboard built in `DashBoard_Using_PowerBi.pbix`:

**KPI Cards:** Total Customers (3.9K) · Avg Purchase ($59.76) · Avg Rating (3.75)

**Visuals:**
- % Customers by Subscription Status (donut chart)
- Revenue & Sales by Category (bar charts)
- Revenue & Sales by Age Group (horizontal bars)
- Filters: Gender · Category · Subscription Status · Shipping Type

---

## 📌 Business Recommendations

**1. Fix the Subscription Gap**
Only 27% of customers subscribe despite spending the same as non-subscribers. Offer exclusive early access or free shipping to drive conversions.

**2. Launch a Loyalty Program**
80% of customers are already "Loyal" — capitalize on this with a points/rewards system to increase basket size.

**3. Review Discount Strategy**
Hat and Sneakers have ~50% discount rates. Audit whether these discounts are driving incremental sales or just eroding margins.

**4. Target Young Adults**
They are the highest revenue group. Build seasonal campaigns (they respond to trends) specifically for this segment.

**5. Convert Repeat Buyers to Subscribers**
2,518 repeat buyers are not subscribed. A targeted re-engagement campaign here has direct revenue upside.

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/retail-customer-behavior-analysis.git

# 2. Install Python dependencies
pip install pandas numpy matplotlib seaborn sqlalchemy psycopg2

# 3. Run the notebook
jupyter notebook Data_Cleaning_Python.ipynb

# 4. Import SQL file into MySQL
mysql -u root -p < Sql_Analysis.sql

# 5. Open Power BI dashboard
# Open DashBoard_Using_PowerBi.pbix in Power BI Desktop
```

---

## 👤 Author

**[Your Name]**
Data Analyst | Python · SQL · Power BI
[LinkedIn](https://linkedin.com/in/yourprofile) · [GitHub](https://github.com/yourusername) · [Email](mailto:your@email.com)
