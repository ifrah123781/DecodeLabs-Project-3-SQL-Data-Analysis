# DecodeLabs-Project-3-SQL-Data-Analysis
Executed SQL analytical queries using Python and SQLite to analyze 1,200 e-commerce orders, extracting insights on product revenue, payment methods, and marketing channel performance.
SQL Data Analysis
Project Overview
This project focuses on performing SQL-based data extraction and analytical querying on an e-commerce transactions dataset using Python and SQLite. The analysis was conducted to evaluate business KPIs, product sales performance, customer payment behaviors, fulfillment funnel status, and marketing channel efficiency.
The project contains 1,200 orders and 14 original features related to customers, products, pricing, payments, order status, and sales.

Objectives
Load raw transactional data into an SQL database environment

Write and execute structured SELECT queries

Apply filtering and conditional logic using WHERE and LIMIT

Rank and organize query outputs using ORDER BY

Perform fundamental aggregations using COUNT(), SUM(), and AVG()

Segment data using GROUP BY across multiple business dimensions

Summarize key operational and commercial observations

Tools & Technologies
Python

SQLite (sqlite3)

Pandas

Google Colab / Jupyter Notebook

Excel

Dataset Information
Total Orders: 1,200

Original Features: 14

Date Range: 2023–2025

Dataset Type: E-commerce / Sales Transactions

Main Features
OrderID

Date

CustomerID

Product

Quantity

UnitPrice

ShippingAddress

PaymentMethod

OrderStatus

TrackingNumber

ItemsInCart

CouponCode

ReferralSource

TotalPrice

Analysis Performed
1. In-Memory Database Setup
The raw dataset was loaded into a Pandas DataFrame and ingested directly into an in-memory SQLite database as the orders relational table, enabling full ANSI SQL query execution without external database server configuration.

2. Overall Business KPI Summary
Aggregate functions (COUNT, SUM, AVG, ROUND) were executed to measure overall business performance.

Total Orders Processed: 1,200

Total Units Sold: 3,535

Total Cumulative Revenue: $1,264,761.96

Average Order Value (AOV): $1,053.97

3. High-Value Delivered Orders
Filtered for fulfilled customer orders using WHERE TotalPrice > 2500 AND OrderStatus = 'Delivered' and sorted descending by TotalPrice.

Successfully isolated the top 10 premium completed orders.

Order values for this cohort ranged between $2,714.20 and $3,456.40, with products including Tablets, Laptops, Printers, Chairs, and Phones.

4. Product Performance Analysis
Sales and revenue metrics were aggregated and grouped by product category using GROUP BY Product and sorted by cumulative revenue.

Chairs: 178 orders | 562 units sold | $195,620.11 total revenue | $1,098.99 avg price

Printers: 181 orders | 542 units sold | $195,612.61 total revenue | $1,080.73 avg price

Laptops: 173 orders | 535 units sold | $192,126.56 total revenue | $1,110.56 avg price

Tablets: 179 orders | 497 units sold | $186,568.95 total revenue | $1,042.28 avg price

Monitors: 163 orders | 480 units sold | $175,651.41 total revenue | $1,077.62 avg price

Desks: 170 orders | 508 units sold | $167,459.93 total revenue | $985.06 avg price

Phones: 156 orders | 411 units sold | $151,722.39 total revenue | $972.58 avg price

5. Order Fulfillment Breakdown
Aggregated order volumes and monetary amounts across all order lifecycle states using GROUP BY OrderStatus.

Cancelled: 250 orders ($276,396.21 revenue impact)

Returned: 247 orders ($243,277.70 revenue impact)

Pending: 237 orders ($256,328.15 pending revenue)

Shipped: 235 orders ($246,159.58 transit revenue)

Delivered: 231 orders ($242,600.32 fulfilled revenue)

6. Payment Channel & Spending Behavior
Audited payment methods using GROUP BY PaymentMethod to evaluate customer preference and transaction values.

Online: 258 transactions | $1,017.22 avg spend | $262,442.94 total spend

Cash: 246 transactions | $1,056.04 avg spend | $259,786.29 total spend

Credit Card: 234 transactions | $1,127.55 avg spend | $263,847.63 total spend

Debit Card: 232 transactions | $1,001.56 avg spend | $232,361.18 total spend

Gift Card: 230 transactions | $1,070.97 avg spend | $246,323.92 total spend

7. Acquisition & Marketing Channel Performance
Grouped transaction volume and revenue generation by ReferralSource.

Instagram: 259 orders | $275,285.45 generated revenue

Email: 250 orders | $261,808.55 generated revenue

Google: 241 orders | $250,441.48 generated revenue

Facebook: 228 orders | $250,410.90 generated revenue

Referral: 222 orders | $226,815.58 generated revenue

Key Observations
Total store revenue reached $1,264,761.96 across 1,200 transactions with an average order spend of $1,053.97.

Chairs and Printers were the top two revenue drivers, generating over $195.6K each.

Printers recorded the single highest order volume (181 orders), while Phones recorded the lowest volume (156 orders) and lowest revenue ($151.7K).

Credit Card transactions yielded the highest average order value ($1,127.55), while Online payment was the most frequently chosen payment method (258 orders).

Instagram proved to be the most lucrative marketing source, contributing 259 orders and generating $275,285.45 in sales.

Cancelled (250) and Returned (247) orders together accounted for 497 orders (41.42%), representing significant uncollected or reversed potential revenue ($519,673.91).

How to Run
Using Google Colab
Open DecodeLabs_Project_3.ipynb in Google Colab.

Upload Dataset for Data Analytics (2).xlsx to the environment files when prompted.

Run the notebook cells sequentially from top to bottom.

Review the SQL query formulations and tabular results returned directly via Pandas DataFrames.

Local Python Environment
Install the required libraries:

Bash
pip install pandas openpyxl
Open the .ipynb notebook using Jupyter Notebook, VS Code, or JupyterLab and execute all cells.

Skills Demonstrated
SQL Fundamentals & Relational Data Management

In-Memory Database Creation (sqlite3)

Multi-Condition Data Filtering (WHERE, AND)

Numerical Aggregation Functions (COUNT, SUM, AVG, ROUND)

Dimensional Categorization (GROUP BY)

Result Ranking & Sorting (ORDER BY DESC)

Business Data Analysis & Revenue Diagnostics

Python Integration with SQL

Project Status
Completed — DecodeLabs Virtual Internship Project 3
