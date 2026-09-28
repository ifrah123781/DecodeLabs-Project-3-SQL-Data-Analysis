# DecodeLabs-Project-3-SQL-Data-Analysis

## Project Overview

This project focuses on performing SQL-based data extraction and analytical querying on an e-commerce transactions dataset using Python and SQLite.

The analysis was conducted to evaluate business KPIs, product sales performance, customer payment behavior, order fulfillment status, and marketing channel performance.

The dataset contains 1,200 orders and 14 original features related to customers, products, pricing, payments, order status, and sales.

## Objectives

* Load transactional data into an SQL database environment
* Write and execute SQL `SELECT` queries
* Apply filtering and conditional logic using `WHERE` and `LIMIT`
* Sort query results using `ORDER BY`
* Perform aggregations using `COUNT()`, `SUM()`, and `AVG()`
* Segment data using `GROUP BY`
* Analyze business performance across different dimensions
* Summarize key commercial and operational observations

## Tools & Technologies

* Python
* SQLite (`sqlite3`)
* Pandas
* Google Colab / Jupyter Notebook
* Excel

## Dataset Information

* **Total Orders:** 1,200
* **Original Features:** 14
* **Date Range:** 2023–2025
* **Dataset Type:** E-commerce / Sales Transactions

### Main Features

* OrderID
* Date
* CustomerID
* Product
* Quantity
* UnitPrice
* ShippingAddress
* PaymentMethod
* OrderStatus
* TrackingNumber
* ItemsInCart
* CouponCode
* ReferralSource
* TotalPrice

## Analysis Performed

### 1. In-Memory Database Setup

The dataset was loaded into a Pandas DataFrame and then ingested into an in-memory SQLite database as the `orders` table.

This allowed SQL queries to be executed without requiring an external database server.

### 2. Overall Business KPI Analysis

SQL aggregate functions including `COUNT()`, `SUM()`, `AVG()`, and `ROUND()` were used to calculate overall business metrics.

* **Total Orders:** 1,200
* **Total Units Sold:** 3,535
* **Total Revenue:** $1,264,761.96
* **Average Order Value (AOV):** $1,053.97

### 3. High-Value Delivered Orders

Orders with `TotalPrice > 2500` and `OrderStatus = 'Delivered'` were filtered and sorted by order value.

The analysis identified the top 10 high-value completed orders, with order values ranging from $2,714.20 to $3,456.40.

### 4. Product Performance Analysis

Product-level sales and revenue were analyzed using `GROUP BY Product`.

| Product  | Orders | Units Sold | Total Revenue |
| -------- | -----: | ---------: | ------------: |
| Chairs   |    178 |        562 |   $195,620.11 |
| Printers |    181 |        542 |   $195,612.61 |
| Laptops  |    173 |        535 |   $192,126.56 |
| Tablets  |    179 |        497 |   $186,568.95 |
| Monitors |    163 |        480 |   $175,651.41 |
| Desks    |    170 |        508 |   $167,459.93 |
| Phones   |    156 |        411 |   $151,722.39 |

### 5. Order Fulfillment Analysis

Order volumes and revenue were grouped according to `OrderStatus`.

* **Cancelled:** 250 orders
* **Returned:** 247 orders
* **Pending:** 237 orders
* **Shipped:** 235 orders
* **Delivered:** 231 orders

Cancelled and returned orders together represented **497 orders (41.42%)**.

### 6. Payment Channel Analysis

Payment methods were analyzed using `GROUP BY PaymentMethod`.

* **Online:** 258 transactions | $1,017.22 average spend
* **Cash:** 246 transactions | $1,056.04 average spend
* **Credit Card:** 234 transactions | $1,127.55 average spend
* **Debit Card:** 232 transactions | $1,001.56 average spend
* **Gift Card:** 230 transactions | $1,070.97 average spend

### 7. Marketing Channel Analysis

Transaction volume and revenue were analyzed by `ReferralSource`.

* **Instagram:** 259 orders | $275,285.45 revenue
* **Email:** 250 orders | $261,808.55 revenue
* **Google:** 241 orders | $250,441.48 revenue
* **Facebook:** 228 orders | $250,410.90 revenue
* **Referral:** 222 orders | $226,815.58 revenue

## Key Observations

* The dataset contains **1,200 transactions** with total revenue of **$1,264,761.96**.
* **Chairs and Printers** generated approximately $195.6K each in revenue.
* **Printers** had the highest order volume with 181 orders.
* **Phones** had the lowest order volume and lowest total revenue among the analyzed products.
* **Credit Card** transactions had the highest average spend at $1,127.55.
* **Online** was the most frequently used payment method with 258 transactions.
* **Instagram** generated the highest revenue among the listed referral sources at $275,285.45.
* Cancelled and returned orders together accounted for **497 orders (41.42%)**.

## How to Run

### Using Google Colab

1. Open `DecodeLabs_Project_3.ipynb` in Google Colab.
2. Upload `Dataset for Data Analytics (2).xlsx` when prompted.
3. Run the notebook cells sequentially from top to bottom.
4. Review the SQL queries and resulting analysis tables.

### Local Python Environment

Install the required libraries:

```bash
pip install pandas openpyxl
```

The project uses Python's built-in `sqlite3` library, so no separate SQLite installation is required.

Open the `.ipynb` notebook using Jupyter Notebook, JupyterLab, or VS Code and run the cells sequentially.

## Skills Demonstrated

* SQL Fundamentals
* SQLite
* Relational Data Analysis
* Data Filtering
* `WHERE` and `AND`
* `LIMIT`
* `ORDER BY`
* `GROUP BY`
* `COUNT()`
* `SUM()`
* `AVG()`
* `ROUND()`
* Python and SQL Integration
* Business KPI Analysis
* Revenue Analysis
* Product Performance Analysis
* Payment Behavior Analysis
* Marketing Channel Analysis

## Project Status

**Completed — DecodeLabs Internship Project 3**
