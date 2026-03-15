# 🛒 Superstore Sales — Exploratory Data Analysis (EDA)

A comprehensive exploratory data analysis of the **Sample Superstore** dataset, uncovering key business insights around sales, profitability, discounting strategies, and regional performance.

---

## 📋 Project Overview

This project performs end-to-end EDA on a retail superstore's transactional data. The goal is to identify what's driving profit and loss across categories, regions, and customer segments — and surface actionable business recommendations.

---

## 📁 Dataset

- **File:** `SampleSuperstore.csv`
- **Records:** ~9,994 orders (after duplicate removal)
- **Features:** Ship Mode, Segment, Region, Category, Sub-Category, Sales, Quantity, Discount, Profit, and more

---

## 🔍 Analysis Workflow

1. **Data Loading & Inspection** — `df.info()`, `df.describe()`, `df.shape`
2. **Data Cleaning** — Null value check (none found), duplicate removal, column type fixes
3. **Outlier Analysis** — IQR-based detection across Sales, Quantity, Discount, Profit *(outliers retained as genuine business events)*
4. **Univariate Analysis** — Distributions of Sales, Profit, Quantity, Discount, Ship Mode, Segment, Region
5. **Bivariate Analysis** — Sales vs. Profit, Discount vs. Profit (by Category), Category/Sub-Category profitability
6. **Correlation Analysis** — Pearson and Spearman heatmaps
7. **Pair Plot** — Multi-variable relationship exploration across Categories

---

## 💡 Key Business Insights

| # | Insight |
|---|---------|
| 1 | Dataset is structurally clean — no missing values, duplicates removed |
| 2 | Overall profit margin ~12.5%, but ~18.7% of orders result in losses |
| 3 | Outliers retained — they represent real events (e.g., large tech orders, discounted furniture losses) |
| 4 | Sales are heavily right-skewed — most transactions are small-value |
| 5 | Profit is bimodal — many small gains but a significant cluster of losses |
| 6 | **Technology** is the most profitable category; **Furniture** is near break-even (2.4% margin) |
| 7 | **Tables** and **Bookcases** are consistent net-loss sub-categories |
| 8 | Discounts above **20%** consistently erode profit; above **40%** almost guarantee losses |
| 9 | **West** and **East** regions lead in both sales and profit; **Central** underperforms |
| 10 | Consumer segment drives the highest transaction volume and total profit |

---

## 📊 Visualizations

- Histograms & KDE plots (Sales, Profit, Quantity)
- Box plots for outlier detection
- Bar charts (Category/Region/Sub-Category profitability)
- Scatter plots (Sales vs. Profit by Segment & Category)
- Relational plots (Discount vs. Profit per Category)
- Correlation heatmaps (Pearson & Spearman)
- Pair plot (Sales, Quantity, Discount, Profit — colored by Category)
- Pie/Donut charts (Profit vs. Loss frequency, Ship Mode distribution)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Base plotting |
| Seaborn | Statistical visualization |
| Google Colab | Notebook environment |

---

## 🚀 How to Run

1. Clone this repository
   ```bash
   git clone https://github.com/your-username/superstore-eda.git
   cd superstore-eda
   ```

2. Open `DS1.ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook

3. When prompted, upload `SampleSuperstore.csv`

4. Run all cells sequentially (`Runtime → Run all`)

---

## 📌 Recommendations

- **Revise discounting policy** — Cap discounts at 20% for Furniture and Office Supplies
- **Investigate Tables & Bookcases** — Re-evaluate pricing or consider discontinuing
- **Focus on Central region** — Diagnose why sales don't convert to profit
- **Double down on Technology** — Highest margin category with consistent growth potential

---

## 📄 License

This project is for educational purposes. Dataset sourced from the publicly available Tableau Sample Superstore data.
