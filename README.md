# 📊 UK Retail Sales Performance Analysis

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![SQL](https://img.shields.io/badge/SQL-Analytics-336791)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Status](https://img.shields.io/badge/Project-Complete-success)

> **End-to-end retail analytics project analysing 2,500 UK retail transactions using Python, SQL, Pandas and Matplotlib to uncover sales, profitability, regional and customer behaviour insights.**

---

## 🎬 Project Preview

<p align="center">
  <img src="images/retail_sales_dashboard.gif" alt="Animated preview of UK Retail Sales Analysis" width="900"/>
</p>

---

## 📌 Overview

This project demonstrates an end-to-end **data analytics workflow**, transforming raw retail transaction data into actionable business insights.

The analysis explores:

* 💰 Revenue and profitability
* 🌍 Regional sales performance
* 🛍️ Product and category performance
* 🌐 Online vs in-store sales
* ↩️ Customer return behaviour
* ⭐ Customer ratings
* 📅 Monthly sales trends
* 🏷️ Discount impact

The workflow follows a practical analyst process:

**Raw Data → Data Cleaning → Validation → Exploratory Analysis → KPI Calculation → SQL Analysis → Visualisation → Business Recommendations**

> **Dataset Disclaimer:** This project uses a **synthetic dataset** created to resemble realistic UK retail transactions. Minor data-quality issues were intentionally included to demonstrate data-cleaning techniques. It does not represent a real company or real customers.

---

## 🎯 Business Questions

The analysis was designed to answer eight key questions:

1. Which regions generate the highest revenue?
2. Which product categories generate the most profit?
3. How do online and physical store sales compare?
4. What is the overall customer return rate?
5. Which products generate the most revenue?
6. How does revenue change throughout the year?
7. Which categories receive the strongest customer ratings?
8. How do discounts relate to profitability?

---

## 🛠️ Tech Stack

| Technology       | Application                               |
| ---------------- | ----------------------------------------- |
| **Python**       | Data analysis and automation              |
| **Pandas**       | Cleaning, transformation and aggregation  |
| **SQL**          | Business queries and KPI analysis         |
| **Matplotlib**   | Data visualisation                        |
| **Git & GitHub** | Version control and project documentation |

---

## 📂 Dataset

The dataset contains **2,500 transactions from 2025** across multiple UK regions, product categories and sales channels.

| Dataset Metric     |     Value |
| ------------------ | --------: |
| Transactions       | **2,500** |
| Period             |  **2025** |
| Regions            |     **5** |
| Product Categories |     **4** |
| Sales Channels     |     **2** |

### Key Variables

`order_id` · `order_date` · `region` · `sales_channel` · `category` · `product` · `quantity` · `unit_price_gbp` · `discount_pct` · `revenue_gbp` · `cost_gbp` · `profit_gbp` · `payment_method` · `returned` · `customer_rating`

### Files

**Raw data:** `data/retail_sales_raw.csv`

Contains intentionally introduced issues including missing customer ratings and inconsistent region formatting.

**Clean data:** `data/retail_sales_clean.csv`

Contains the cleaned reference dataset.

**Data dictionary:** `data/data_dictionary.csv`

Provides descriptions of the dataset fields.

---

# 📈 Key Results

| KPI                        |          Result |
| -------------------------- | --------------: |
| 💰 **Total Revenue**       |    **£320,707** |
| 💵 **Total Profit**        |    **£116,331** |
| 📊 **Profit Margin**       |       **36.3%** |
| 🏆 **Top Revenue Region**  |    **Midlands** |
| 🥇 **Top Profit Category** | **Electronics** |
| ↩️ **Return Rate**         |        **9.2%** |

### 💡 Key Insight

**Electronics generated the highest category profit, while the Midlands produced the highest regional revenue.**

The overall return rate was **9.2%**. Although this is below 10%, analysing returns at product and category level remains important because products with strong sales but high return rates may contribute less value than headline revenue suggests.

---

# 📊 Visual Analysis

<details>
<summary><strong>📅 Monthly Revenue Trend</strong></summary>

<br>

<p align="center">
  <img src="images/monthly_revenue.png" alt="Monthly Revenue Trend" width="800"/>
</p>

The monthly analysis highlights changes in revenue throughout 2025 and allows stronger and weaker trading periods to be identified.

</details>

<details>
<summary><strong>🌍 Revenue by Region</strong></summary>

<br>

<p align="center">
  <img src="images/revenue_by_region.png" alt="Revenue by UK Region" width="800"/>
</p>

Regional analysis identifies the geographic areas contributing most strongly to overall sales performance.

</details>

<details>
<summary><strong>💷 Profit by Product Category</strong></summary>

<br>

<p align="center">
  <img src="images/profit_by_category.png" alt="Profit by Product Category" width="800"/>
</p>

Category-level profitability provides a clearer view of commercial performance than revenue alone.

</details>

---

# 🔄 Analytics Workflow

```mermaid
flowchart LR
    A["📁 Raw Data"] --> B["🧹 Cleaning"]
    B --> C["✅ Validation"]
    C --> D["🔎 EDA"]
    D --> E["📊 KPI Analysis"]
    E --> F["🗄️ SQL"]
    F --> G["📈 Visualisation"]
    G --> H["💡 Business Insights"]
```

## 1️⃣ Data Cleaning

The raw dataset was inspected for:

* missing values
* duplicate transactions
* inconsistent categorical values
* incorrect data types
* unexpected numerical values

Cleaning included standardising region names, handling missing customer ratings and validating transaction-level data.

## 2️⃣ Exploratory Data Analysis

The cleaned dataset was explored to understand:

* transaction distributions
* regional performance
* category performance
* channel behaviour
* return patterns
* customer ratings

## 3️⃣ KPI Analysis

Core business metrics were calculated, including:

* total revenue
* total profit
* profit margin
* return rate
* regional revenue
* category profitability
* channel performance

## 4️⃣ Visualisation

Business-focused visualisations were created to communicate findings clearly to both technical and non-technical stakeholders.

---

# 🗄️ SQL Analysis

Reusable SQL queries are included for common business-analysis tasks.

### Example: Revenue by Region

```sql
SELECT
    region,
    ROUND(SUM(revenue_gbp), 2) AS revenue
FROM retail_sales
GROUP BY region
ORDER BY revenue DESC;
```

The complete SQL analysis covers:

* total revenue and profit
* profit margin
* regional revenue
* category profitability
* online vs store performance
* category return rates
* top-performing products
* customer ratings

📄 **Full query file:** `sql/analysis_queries.sql`

---

# 💡 Business Recommendations

### 1. Focus on Strong Regional Markets

The **Midlands** generated the highest revenue. Management could investigate the drivers behind this performance and determine whether successful regional strategies can be replicated elsewhere.

### 2. Protect Electronics Profitability

**Electronics** generated the highest category profit. Inventory availability, pricing and promotional activity should therefore be monitored carefully to protect this contribution.

### 3. Investigate Returns at Product Level

The overall return rate is **9.2%**, but aggregate figures can hide poorly performing products. Product-level return analysis could identify potential quality, fulfilment or customer-expectation issues.

### 4. Evaluate Channels Beyond Revenue

Online and physical stores should be compared using multiple measures, including:

* revenue
* average order value
* profit
* return rate

This provides a more complete picture of channel performance.

### 5. Monitor Discount Profitability

Promotions should be evaluated against both **sales volume and profit margin** to determine whether discounts are generating profitable growth.

---

# 📁 Repository Structure

```text
uk-retail-sales-analysis/
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

# 🚀 Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/uk-retail-sales-analysis.git
cd uk-retail-sales-analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the analysis

```bash
python python/retail_sales_analysis.py
```

The script performs the analysis and generates the project visualisations inside the `images` directory.

---

# 🧠 Skills Demonstrated

| Area                  | Skills                                                        |
| --------------------- | ------------------------------------------------------------- |
| **Data Cleaning**     | Missing values, standardisation, duplicate checks, validation |
| **Python**            | Pandas, grouping, aggregation, KPI calculations               |
| **SQL**               | GROUP BY, CASE WHEN, aggregates, filtering, sorting           |
| **Visualisation**     | Trend, regional and profitability analysis                    |
| **Business Analysis** | KPI interpretation and actionable recommendations             |
| **GitHub**            | Repository organisation and technical documentation           |

---

# 🔮 Future Development

Possible extensions include:

* 📊 Interactive Power BI dashboard
* 📈 Tableau dashboard
* 👥 Customer segmentation
* 🔮 Sales forecasting
* ↩️ Return-risk modelling
* 🤖 Automated monthly reporting
* 🗄️ Advanced SQL window functions

---

# 👩‍💻 Author

## Tasnem Islam Prome

**Aspiring Data Analyst | Applied Computing Student**

`Python` · `SQL` · `Excel` · `Power BI` · `Data Analysis`

This project was developed as part of my data analytics portfolio to demonstrate practical skills in **data cleaning, exploratory analysis, SQL, Python, visualisation and business decision support**.

---

<p align="center">
  <strong>⭐ Thank you for viewing this project!</strong>
</p>
