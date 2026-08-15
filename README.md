# 📊 UK Retail Sales Performance Analysis

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![SQL](https://img.shields.io/badge/SQL-Analytics-336791)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Status](https://img.shields.io/badge/Project-Complete-success)

A portfolio-ready retail analytics project using **Python, SQL, Pandas, and Matplotlib** to explore revenue, profitability, customer returns, regional performance, product performance, and sales channels across **2,500 UK retail transactions from 2025**.

---

## 🎬 Project Preview

<p align="center">
  <img src="images/retail_sales_dashboard.gif" alt="Retail Sales Analysis Preview" width="900"/>
</p>

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Questions](#-business-questions)
- [Tools & Technologies](#-tools--technologies)
- [Dataset](#-dataset)
- [Key Findings](#-key-findings)
- [Visual Analysis](#-visual-analysis)
- [Analysis Workflow](#-analysis-workflow)
- [SQL Analysis](#-sql-analysis)
- [Repository Structure](#-repository-structure)
- [How to Run](#-how-to-run)
- [Skills Demonstrated](#-skills-demonstrated)
- [Business Recommendations](#-business-recommendations)
- [Author](#-author)

---

## 🔎 Project Overview

The objective of this project is to analyse retail sales data and convert raw transaction-level information into practical business insights.

The analysis focuses on:

- revenue performance
- profitability
- product category performance
- regional sales performance
- online vs store sales
- customer return behaviour
- customer ratings
- monthly sales trends
- discount impact

The project follows a typical junior data analyst workflow: **data cleaning → exploration → KPI calculation → SQL analysis → visualisation → business recommendations**.

> **Dataset note:** This is a synthetic dataset designed to resemble a realistic UK retail transaction dataset. It includes intentionally introduced data-quality issues such as missing values and inconsistent text formatting.

---

## ❓ Business Questions

This project answers the following questions:

1. Which regions generate the highest revenue?
2. Which product categories generate the most profit?
3. How do online and physical store sales compare?
4. What is the overall customer return rate?
5. Which products generate the most revenue?
6. How does revenue change throughout the year?
7. Which categories receive the strongest customer ratings?
8. Are discounts affecting profitability?

---

## 🛠 Tools & Technologies

| Tool | Purpose |
|---|---|
| **Python** | Data analysis and automation |
| **Pandas** | Data cleaning, transformation and aggregation |
| **Matplotlib** | Data visualisation |
| **SQL** | Business querying and KPI analysis |
| **Git / GitHub** | Version control and portfolio presentation |

---

## 📂 Dataset

The project contains two versions of the data:

### Raw Dataset

`data/retail_sales_raw.csv`

Contains realistic data-quality issues including:

- missing customer ratings
- inconsistent region formatting
- values requiring standardisation

### Clean Dataset

`data/retail_sales_clean.csv`

Contains the cleaned reference version used for analysis.

### Dataset Summary

| Metric | Value |
|---|---:|
| Transactions | **2,500** |
| Year | **2025** |
| Regions | **5** |
| Product Categories | **4** |
| Sales Channels | **2** |

Main fields include:

`order_id`, `order_date`, `region`, `sales_channel`, `category`, `product`, `quantity`, `unit_price_gbp`, `discount_pct`, `revenue_gbp`, `cost_gbp`, `profit_gbp`, `payment_method`, `returned`, and `customer_rating`.

A complete field description is available in:

`data/data_dictionary.csv`

---

## 📈 Key Findings

| KPI | Result |
|---|---:|
| 💰 Total Revenue | **£320,707** |
| 💵 Total Profit | **£116,331** |
| 📊 Profit Margin | **36.3%** |
| 🏆 Highest-Revenue Region | **Midlands** |
| 🥇 Highest-Profit Category | **Electronics** |
| ↩️ Overall Return Rate | **9.2%** |

### Main Business Insight

The analysis shows that **Electronics is the strongest category by profit**, while the **Midlands generates the highest overall revenue**.

The overall return rate remains below 10%, but return behaviour should still be reviewed by product category because high-return products can reduce profitability even when sales are strong.

---

## 📊 Visual Analysis

<details>
<summary><strong>📅 Monthly Revenue Trend</strong></summary>

<br>

![Monthly Revenue](images/monthly_revenue.png)

This visual shows how revenue changes across the 12 months of 2025 and helps identify stronger and weaker sales periods.

</details>

<details>
<summary><strong>🌍 Revenue by Region</strong></summary>

<br>

![Revenue by Region](images/revenue_by_region.png)

Regional analysis helps identify which UK areas contribute most strongly to total sales.

</details>

<details>
<summary><strong>💷 Profit by Product Category</strong></summary>

<br>

![Profit by Category](images/profit_by_category.png)

This comparison highlights which categories contribute the most to overall profitability.

</details>

---

## 🔄 Analysis Workflow

```mermaid
flowchart LR
    A[Raw Retail Data] --> B[Data Cleaning]
    B --> C[Data Validation]
    C --> D[Exploratory Analysis]
    D --> E[KPI Calculation]
    E --> F[SQL Analysis]
    F --> G[Visualisation]
    G --> H[Business Insights]
```

### 1. Data Loading

The raw CSV file was loaded into Pandas and inspected for:

- missing values
- duplicate records
- inconsistent text values
- incorrect data types

### 2. Data Cleaning

The cleaning process included:

- standardising region names
- filling missing customer ratings using the median
- checking for duplicate transactions
- validating numeric fields

### 3. KPI Analysis

Key performance indicators included:

- total revenue
- total profit
- profit margin
- return rate
- average order performance

### 4. Segmentation

Performance was analysed by:

- region
- product category
- product
- sales channel
- customer return behaviour

### 5. Visualisation

Charts were created to communicate trends clearly to non-technical stakeholders.

---

## 🗄 SQL Analysis

The repository includes reusable SQL queries covering:

- total revenue and profit
- profit margin
- revenue by region
- profit by category
- online vs store performance
- return rate by category
- top-performing products
- average customer rating

Example:

```sql
SELECT
    region,
    ROUND(SUM(revenue_gbp), 2) AS revenue
FROM retail_sales
GROUP BY region
ORDER BY revenue DESC;
```

Full SQL file:

`sql/analysis_queries.sql`

---

## 📁 Repository Structure

```text
retail_sales_analysis_portfolio/
│
├── data/
│   ├── retail_sales_raw.csv
│   ├── retail_sales_clean.csv
│   └── data_dictionary.csv
│
├── python/
│   └── retail_sales_analysis.py
│
├── sql/
│   └── analysis_queries.sql
│
├── images/
│   ├── monthly_revenue.png
│   ├── revenue_by_region.png
│   ├── profit_by_category.png
│   └── retail_sales_dashboard.gif
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/uk-retail-sales-analysis.git
cd uk-retail-sales-analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Python analysis

```bash
python python/retail_sales_analysis.py
```

The analysis will calculate the key KPIs and generate the visualisations inside the `images` folder.

---

## 🧠 Skills Demonstrated

**Data Cleaning**
- missing-value treatment
- data standardisation
- duplicate checks
- data validation

**Python**
- Pandas
- grouping
- aggregation
- KPI calculation
- automated analysis

**SQL**
- `GROUP BY`
- `CASE WHEN`
- aggregate functions
- sorting
- filtering
- business KPI queries

**Data Visualisation**
- trend analysis
- regional comparison
- category profitability
- business-focused chart design

**Business Analysis**
- interpreting KPIs
- identifying performance patterns
- translating data into recommendations

---

## 💡 Business Recommendations

Based on the analysis:

1. **Prioritise high-performing regions** such as the Midlands when planning campaigns or inventory allocation.
2. **Protect Electronics profitability** by monitoring discount levels and product return rates.
3. **Review high-return products** to identify possible quality, fulfilment, or customer expectation issues.
4. **Compare online and store performance using both revenue and average order value**, rather than judging channels only by total sales.
5. **Monitor discount effectiveness** to ensure promotional activity generates profitable growth instead of simply increasing sales volume.

---

## 🔮 Possible Future Improvements

Future versions of this project could include:

- an interactive Power BI dashboard
- Tableau visualisations
- customer segmentation
- sales forecasting
- product-level return prediction
- automated monthly reporting
- advanced SQL window functions

---

## 👩‍💻 Author

### Tasnem Islam Prome

**Aspiring Data Analyst | Applied Computing Student**

**Core Skills:** Python · SQL · Excel · Power BI · Data Analysis

This project was created as part of my data analytics portfolio to demonstrate practical skills in data cleaning, business analysis, SQL querying, Python, and data visualisation.

---

⭐ **If you found this project useful, feel free to star the repository.**
