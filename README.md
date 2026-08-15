# UK Retail Sales Performance Analysis

## Project Overview

This portfolio project analyses **2,500 retail transactions from 2025** to identify sales trends, profitability, regional performance, customer returns, and channel performance.

The project demonstrates practical skills in **Python, SQL, data cleaning, exploratory data analysis, KPI reporting, and business insight generation**.

> Note: The dataset is synthetic but designed to closely resemble a real-world UK retail transaction dataset. It contains realistic sales values, discounts, product categories, returns, customer ratings, and minor data-quality issues for cleaning practice.

## Business Questions

- Which regions generate the most revenue?
- Which product categories generate the most profit?
- How do online and store sales compare?
- What is the overall return rate?
- Which products perform best?
- How does revenue change over time?
- Are discounts helping or hurting profitability?

## Tools Used

- Python
- Pandas
- Matplotlib
- SQL
- Git / GitHub

## Dataset

The project contains two versions of the dataset:

- `retail_sales_raw.csv` — includes missing values and inconsistent region formatting.
- `retail_sales_clean.csv` — cleaned reference version.

Rows: **2,500**

Main fields include order date, region, channel, category, product, quantity, unit price, discount, revenue, cost, profit, return status, and customer rating.

## Key Findings

- Total revenue: **£320,707**
- Total profit: **£116,331**
- Overall profit margin: **36.3%**
- Highest-revenue region: **Midlands**
- Highest-profit category: **Electronics**
- Overall return rate: **9.2%**

## Analysis Workflow

1. Loaded and inspected the raw dataset.
2. Standardised inconsistent region names.
3. Filled missing customer ratings using the median.
4. Checked and removed duplicates.
5. Calculated revenue, profit, profit margin, and return KPIs.
6. Analysed performance by region, category, channel, and product.
7. Created visualisations for monthly revenue, regional revenue, and category profit.
8. Wrote reusable SQL queries to reproduce key business metrics.

## Repository Structure

```text
retail-sales-analysis/
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
│   └── profit_by_category.png
│
├── requirements.txt
└── README.md
```

## How to Run

Clone the repository and install the required packages:

```bash
pip install -r requirements.txt
python python/retail_sales_analysis.py
```

## Skills Demonstrated

**Data Cleaning:** missing values, inconsistent text formatting, duplicate checks  
**Python:** pandas, grouping, aggregation, KPI calculation  
**SQL:** GROUP BY, CASE WHEN, aggregate functions, sorting, filtering  
**Visualisation:** business-focused charts using Matplotlib  
**Business Analysis:** translating transaction data into actionable insights

## Business Recommendations

Based on the analysis, management should prioritise high-performing regions and profitable categories while reviewing categories with elevated return rates. Online and store performance should be compared alongside average order value rather than revenue alone. Discount levels should also be monitored to make sure promotions increase volume without reducing margins excessively.

## Author

**Tasnem Islam Prome**

Aspiring Data Analyst | Applied Computing Student

Skills: Python | SQL | Excel | Power BI | Data Analysis
