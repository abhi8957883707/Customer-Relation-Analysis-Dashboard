# Customer-Relation-Analysis-Dashboard


End-to-end analysis of 3,900 retail transactions — from raw data cleaning to a business-ready Power BI dashboard — built with Python, PostgreSQL, and Power BI.



📌 Project Overview

This project analyzes customer relation using transactional data from 3,900 purchases across four product categories. The goal was to uncover actionable insights into spending patterns, customer segments, product performance, and subscription behavior to support data-driven business decisions.

Business questions explored:


Who are our customers, and how do behaviors differ by age, gender, and shipping preference?
Which products/categories drive the most revenue, and which rely heavily on discounts?
Does the subscription program actually retain higher-value customers?



🧰 Tech Stack

StageToolsData cleaning & feature engineeringPython (pandas)Business analysis PostgreSQL (SQL)Visualization / dashboardPower BI


📁 Dataset


Rows: 3,900 transactions
Columns: 18
Fields: Customer demographics (age, gender, location, subscription status), purchase details (item, category, amount, season, size, color), shopping behavior (discounts, promo codes, purchase frequency, review rating, shipping type)
Data quality: 37 missing values in review_rating, imputed using the median rating within each product category



🔧 Methodology


Data cleaning — handled missing values, standardized column names to snake_case
Feature engineering — created age_group (binned) and purchase_frequency_days
Data consistency check — identified discount_applied and promo_code_used as redundant signals; dropped the duplicate
Database integration — loaded the cleaned dataset into PostgreSQL for structured SQL analysis
SQL analysis — answered 10 business questions (revenue by gender, discount-dependent products, top-rated items, subscriber vs. non-subscriber spend, customer segmentation, repeat buyer behavior, and more)
Dashboard build — designed an interactive Power BI dashboard with slicers for subscription status, gender, category, and shipping type



📊 Key Insights


Subscription status isn't a spend driver. Subscribers spend slightly less per customer on average ($59.49) than non-subscribers ($59.87) — the subscription program's value case needs to rest on retention/frequency, not average order size.
Gender is the strongest revenue signal in the data. Male customers generated ~2x the revenue of female customers ($157.9K vs. $75.2K).
Category demand is concentrated but not monopolized. Clothing leads overall, with Blouses, Pants, and Shirts as top sellers — each item pulling 160–171 orders, showing balanced demand across top products.
Some products are discount-dependent. Hats, Sneakers, and Coats show 47–50% of purchases involving a discount — a margin-risk flag worth investigating.
Customer segmentation needs recalibration. 80% of customers (3,116/3,900) fall into the "Loyal" tier under current thresholds — too broad to be actionable for targeting.


