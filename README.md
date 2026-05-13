# Customer Shopping Behavior Analysis

## Project Overview
This project provides a comprehensive analysis of customer shopping behavior using transactional data from **3,900 purchases**. The primary objective is to uncover actionable insights into spending patterns, customer segmentation, and product preferences to drive data-informed business strategies.

## Key Insights
- **Total Revenue:** $233,081 generated from 3,900 transactions.
- **Top Category:** **Clothing** is the highest revenue-generating category (~$104K).
- **Customer Segmentation:** The majority of the customer base consists of **Loyal** customers (3,116), followed by Returning (701) and New (83).
- **Demographics:** **Young Adults** are the top revenue contributors ($62,143), closely followed by Middle-aged customers.
- **Subscription Impact:** 27% of customers are subscribers, with non-subscribers contributing the bulk of total revenue due to their larger volume.

## Tech Stack
- **Python:** Data cleaning, handling missing values, and feature engineering (Pandas).
- **SQL (PostgreSQL):** Complex business logic, revenue analysis, and customer segmentation.
- **Power BI:** Interactive data visualization and dashboard design.

## Project Workflow

### 1. Data Cleaning & Preparation (Python)
The dataset (3,900 rows, 18 columns) underwent rigorous cleaning:
- **Missing Data:** Imputed 37 missing values in the `Review Rating` column using the median rating by product category.
- **Standardization:** Renamed columns to `snake_case` and standardized categories.
- **Feature Engineering:** - Created `age_group` bins (Young Adult, Adult, Middle-aged, Senior).
  - Derived `purchase_frequency_days` for behavioral analysis.
- **Database Integration:** Exported the cleaned data to a **PostgreSQL** database using `SQLAlchemy`.

### 2. Business Logic & Analysis (SQL)
Structured queries were executed in PostgreSQL to answer key business questions:
- **Revenue Analysis:** Calculated total revenue by gender, age group, and subscription status.
- **Segmentation:** Classified customers based on previous purchase counts.
- **Product Performance:** Identified top 5 products by rating and categories with the highest discount dependency.
- **Shipping Analysis:** Compared average spend across different shipping methods (Express vs. Standard).

### 3. Interactive Dashboard (Power BI)
A professional dashboard was developed to visualize KPIs and trends:
- **KPI Cards:** Total Customers (3.9K), Avg. Purchase Amount ($59.76), and Avg. Review Rating (3.75).
- **Donut Chart:** Customer distribution by subscription status (27% Yes vs 73% No).
- **Bar Charts:** Revenue and sales volume by product category and age group.
- **Slicers:** Interactive filtering by Gender, Category, Shipping Type, and Subscription Status.

## How to Run This Project
1. **Python:** Run `customer_behavior_analysis.ipynb` to clean the raw CSV data.
2. **Database:** Execute the queries in `customer_shopping_sql.sql` in your PostgreSQL environment.
3. **Power BI:** Open the dashboard file or refer to the dashboard screenshot to view the visual analysis.

## Business Recommendations
- **Boost Subscriptions:** Introduce targeted incentives for "Returning" customers to increase the current 27% subscription rate.
- **Targeted Marketing:** Focus campaigns on the "Young Adult" segment, as they represent the highest revenue contribution.
- **Customer Loyalty:** Reward the 3,116 "Loyal" customers with exclusive early access to move them further up the value chain.
- **Product Positioning:** Highlight high-rated items like Gloves and Sandals in seasonal marketing campaigns.
