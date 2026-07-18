# Marketplace-Revenue-Leakage-Gap-Analysis-using-SQL
SQL-based data analytics project that identifies revenue leakage in an online marketplace by analyzing sales, discounts, returns, logistics costs, payment fees, and product profitability to deliver actionable business insights and improve decision-making.

## 📌 Project Information

| Field | Details |
|-------|---------|
| **Project Name** | Marketplace Revenue Leakage & Gap Analysis using SQL |
| **Project Type** | SQL Data Analytics Project |
| **Industry** | Online Marketplace / E-commerce |
| **Database** | MySQL |
| **Objective** | Identify hidden revenue leakage caused by discounts, returns, logistics costs, payment gateway fees, and product profitability. |

---

# 📋 Executive Summary

The **Marketplace Revenue Leakage & Gap Analysis using SQL** project focuses on identifying hidden factors that reduce profitability in an online marketplace despite achieving strong sales performance. While revenue growth is often considered a measure of business success, organizations frequently experience declining profits due to operational inefficiencies and unnoticed financial leakages.

This project leverages **SQL** to design a structured relational database, clean and validate marketplace data, perform advanced business analysis, and identify the major contributors to revenue leakage. The analysis evaluates key profitability drivers, including product performance, discount strategies, return behavior, logistics expenses, and payment gateway fees.

Through comprehensive SQL analysis, the project transforms raw transactional data into meaningful business insights that support strategic decision-making, improve operational efficiency, and maximize profitability.

---

# 💼 Business Problem

Many online marketplaces experience consistent growth in sales while simultaneously facing declining profit margins. Although revenue appears healthy, hidden operational costs significantly reduce the actual profit generated from each order.

Major revenue leakage factors include:

- Excessive discount strategies
- High product return rates
- Expensive logistics operations
- Payment gateway processing fees
- Loss-making products
- Inefficient pricing strategies

These hidden costs create a substantial gap between gross revenue and net profitability, making it difficult for decision-makers to identify where financial losses occur.

---

## Business Impact

Revenue leakage directly affects business performance by:

- Reducing overall profitability
- Increasing operational costs
- Lowering product margins
- Decreasing return on investment (ROI)
- Weakening pricing strategies
- Increasing customer acquisition costs
- Reducing inventory efficiency
- Limiting long-term business growth

Without detailed analytical reporting, organizations struggle to identify which operational areas require optimization.

---

## Why This Analysis is Needed

This project helps businesses:

- Identify hidden revenue leakage sources
- Measure profitability at product and category levels
- Understand customer purchasing and return behavior
- Optimize discount strategies
- Reduce unnecessary logistics expenses
- Improve pricing decisions
- Increase operational efficiency
- Support data-driven business decisions

Ultimately, the analysis enables stakeholders to shift their focus from increasing sales volume to improving overall profitability.

---

# 🎯 Project Objectives

The primary objectives of this project are:

- Design a structured relational database for marketplace operations.
- Clean and validate raw transactional data to improve data quality.
- Calculate essential business KPIs using SQL.
- Measure total sales, costs, gross profit, and net profit.
- Analyze the impact of discounts on profitability.
- Evaluate customer return behavior and its financial impact.
- Identify products generating negative profit.
- Measure logistics costs across different orders.
- Analyze payment gateway fees across payment methods.
- Detect major sources of revenue leakage.
- Compare profitability across product categories.
- Identify high-performing and low-performing products.
- Generate business insights using SQL queries.
- Provide actionable recommendations for improving profitability.
- Support strategic decision-making through data-driven analysis.

---

# ❓ Business Questions

This project answers the following business questions:

1. What is the total marketplace revenue?
2. What is the overall gross profit?
3. Which product categories generate the highest revenue?
4. Which categories generate the highest profit?
5. Which products consistently generate losses?
6. How much revenue is lost due to product returns?
7. Which return reasons contribute most to financial loss?
8. How do discounts affect product profitability?
9. Which payment methods generate the highest transaction fees?
10. Which orders have unusually high logistics costs?
11. Which customers have the highest return rates?
12. Which products contribute most to overall profit?
13. What are the major contributors to revenue leakage?
14. How do operational costs impact net profitability?
15. What strategic actions can improve marketplace profitability?

---

# 🗄️ Database Schema

## Database Design

The project is built using a **normalized relational database schema** that models the core business processes of an online marketplace. The database is designed to ensure data integrity, minimize redundancy, and support efficient analytical querying.

The schema establishes relationships between customers, products, categories, orders, payments, returns, and logistics, enabling comprehensive profitability and revenue leakage analysis.

---

## Main Tables

| Table | Description |
|---------|------------|
| Customers | Stores customer information and purchase activity. |
| Products | Contains product details including pricing and category assignments. |
| Orders | Stores transactional order information. |
| Returns | Records returned products and return reasons. |
| Payments fees | Stores payment methods and associated gateway fees. |
| Logistics | Tracks shipping and logistics costs for each order. 
| Discounts | Stores discount information applied to orders or products. |

---

## Relationship Overview

- One customer can place multiple orders.
- Each order can contain one or more products.
- Every product belongs to a category.
- Orders may generate returns.
- Each order has an associated payment record.
- Logistics costs are tracked for every completed order.
- Each order may have an associated discount record.
- The **Discounts** table stores discount type, discount amount, and promotional details applied to orders.
- Each discount is linked to an order using **Order_ID**, enabling analysis of discount impact on revenue and profitability.

This relational structure enables multi-table SQL joins, KPI calculations, and profitability analysis across different business dimensions.

---

# 🔄 Project Workflow

```text
Business Understanding
        │
        ▼
Requirement Analysis
        │
        ▼
Dataset Collection
        │
        ▼
Database Design
        │
        ▼
Data Cleaning & Validation
        │
        ▼
Data Loading into SQL
        │
        ▼
Exploratory Data Analysis (EDA)
        │
        ▼
SQL Query Development
        │
        ▼
Revenue Leakage Analysis
        │
        ▼
Business Insights Generation
        │
        ▼
Strategic Recommendations
        │
        ▼
Project Documentation
```
---

# 🧹 Data Cleaning Process

Ensuring high-quality data was a critical step before performing any business analysis. The raw marketplace dataset contained inconsistencies, missing values, duplicate records, and invalid entries that could negatively impact analytical accuracy. A systematic data cleaning process was performed using SQL to prepare a reliable, analysis-ready dataset.

## Data Cleaning Activities

- Removed duplicate records to maintain unique transactions.
- Identified and handled missing (`NULL`) values using appropriate filtering and validation techniques.
- Standardized date formats to ensure consistency across all tables.
- Corrected inconsistent text values by standardizing capitalization and formatting.
- Validated numeric fields such as price, quantity, discounts, logistics costs, and payment fees.
- Removed invalid records containing negative or zero values where not applicable.
- Enforced **Primary Key** and **Foreign Key** constraints to maintain referential integrity.
- Verified relationships between Orders, Customers, Products, Payments, Discounts, Returns, and Logistics tables.
- Performed cross-table validation to ensure logical consistency (e.g., returns only exist for completed orders).
- Identified and treated outliers affecting profitability analysis.
- Created calculated columns required for KPI calculations and business reporting.
- Prepared a clean and structured dataset optimized for SQL querying and reporting.

---

# 💻 SQL Work

SQL served as the primary tool for database design, data preparation, and business analysis throughout this project.

## Database Creation

- Created a relational database for marketplace operations.
- Designed normalized tables representing core business entities.
- Established relationships between transactional and master data.

## Data Definition Language (DDL)

Implemented DDL statements to:

- Create database
- Create tables
- Define data types
- Configure Primary Keys
- Configure Foreign Keys
- Apply NOT NULL constraints

## Data Manipulation Language (DML)

Used DML operations to:

- Insert records
- Update existing records
- Delete invalid records
- Modify transactional data

## SQL Joins

Performed multiple joins to combine business information across tables.

- INNER JOIN / JOIN
- LEFT JOIN

These joins enabled comprehensive profitability analysis across customers, products, orders, payments, discounts, logistics, and returns.

## Aggregate Functions

Calculated business KPIs using:

- SUM()
- AVG()
- COUNT()
- MAX()
- MIN()

## Grouping & Filtering

Applied:

- GROUP BY
- HAVING
- ORDER BY

to summarize business performance across different dimensions.

## Common Table Expressions (CTEs)

Used CTEs to improve readability and simplify complex analytical queries.

Applications included:

- Revenue calculations
- Profitability analysis
- Revenue leakage identification
- Ranking products
  
## Window Functions

Implemented window functions such as:

- ROW_NUMBER()
- RANK()
- DENSE_RANK()
- SUM() OVER()
- AVG() OVER()

to perform advanced ranking and comparative analysis.

## Constraints

Implemented:

- PRIMARY KEY
- FOREIGN KEY
  
to maintain data quality and consistency.

---

# 📊 Exploratory Data Analysis (EDA)

The Exploratory Data Analysis phase focused on understanding marketplace performance, identifying hidden revenue leakage, and evaluating profitability across multiple business dimensions.

## Revenue Analysis

- Calculated total sales revenue.
- Compared revenue against gross and net profit.
- Identified the gap between sales and actual profitability.

## Category Performance

- Analyzed revenue by product category.
- Compared category-wise profit margins.
- Identified high-performing and low-performing categories.

## Product Profitability Analysis

- Ranked products based on profit contribution.
- Identified loss-making products.
- Evaluated product-level profitability trends.

## Discount Analysis

- Measured total discount amount.
- Evaluated frequency of discounts.
- Compared discounted and non-discounted order profitability.

## Return Analysis

- Calculated revenue lost due to product returns.
- Identified the most common return reasons.
- Measured profit impact caused by returned orders.

## Logistics Cost Analysis

- Measured logistics cost per order.
- Identified orders with unusually high delivery expenses.
- Evaluated logistics cost as a percentage of order value.

## Payment Fee Analysis

- Compared payment gateway fees across payment methods.
- Identified payment methods contributing to higher transaction costs.

## Revenue Leakage Analysis

Combined all major cost components including:

- Discounts
- Returns
- Logistics Costs
- Payment Fees

to determine the overall impact on marketplace profitability.

---

# 🔍 Key Insights

The SQL analysis uncovered several critical findings that explain the gap between marketplace revenue and actual profitability.

1. Although the marketplace generated strong sales revenue, net profit was significantly reduced due to multiple hidden cost factors.

2. Discounts were one of the largest contributors to revenue leakage, reducing overall profit margins despite increasing sales volume.

3. Product returns resulted in substantial revenue reversal and had a major negative impact on profitability.

4. Products returned due to **Wrong Item** contributed the highest financial loss, indicating operational fulfillment issues.

5. A small number of products consistently generated negative profit despite maintaining regular sales volume.

6. Electronics emerged as the highest revenue-generating category while maintaining strong profitability.

7. Beauty products generated comparatively lower revenue and lower profit than other categories.

8. Frequent promotional discounts increased order volume but significantly reduced profit per transaction.

9. Customer payment preferences were concentrated around a few payment methods, creating uneven transaction costs.

10. Certain payment methods incurred considerably higher payment gateway fees, increasing operational expenses.

11. Several orders experienced logistics costs exceeding 20% of order value, reducing profitability.

12. A smaller group of orders incurred logistics costs greater than 50% of the order value, indicating highly inefficient deliveries.

13. Revenue leakage was caused by the combined effect of discounts, returns, logistics costs, and payment gateway fees rather than a single operational issue.

14. Product profitability varied significantly across categories, indicating opportunities for pricing optimization.

15. A limited number of high-performing products generated a large share of total profit.

16. Multiple low-performing products silently reduced overall marketplace profitability.

17. Stable product categories consistently maintained healthier profit margins than categories with high pricing fluctuations.

18. Accurate and well-structured data significantly improved the reliability of business analysis.

19. SQL enabled efficient identification of operational bottlenecks that are difficult to detect through manual reporting.

20. Business profitability depends not only on increasing sales but also on controlling operational costs and minimizing revenue leakage.

---

# 🚀 Strategic Recommendations

## 🔴 High Priority

- Reduce excessive discount campaigns by implementing data-driven promotional strategies.
- Investigate and resolve the primary causes of product returns, especially fulfillment-related issues.
- Review pricing strategies for products consistently generating negative profit.
- Optimize logistics operations for low-value orders with disproportionately high delivery costs.
- Monitor high-risk products contributing significantly to revenue leakage.
- Implement continuous revenue leakage monitoring dashboards.

---

## 🟠 Medium Priority

- Encourage customers to use lower-cost payment methods where feasible.
- Optimize product pricing based on category-level profitability.
- Improve inventory planning for high-performing products.
- Review supplier costs for products with shrinking profit margins.
- Introduce automated profitability reporting using SQL views and scheduled reports.

---

## 🟢 Low Priority

- Expand profitability analysis to customer segmentation.
- Develop predictive models for return risk.
- Integrate real-time business dashboards.
- Perform seasonal profitability analysis.
- Benchmark profitability against historical performance.

---

# 📈 Business Impact

Implementing the recommendations from this analysis can significantly improve business performance across multiple operational areas.

| Business Area | Expected Impact |
|---------------|-----------------|
| **Revenue** | Reduce hidden revenue leakage and improve revenue realization. |
| **Profitability** | Increase net profit through better cost control and optimized pricing strategies. |
| **Customer Satisfaction** | Reduce return rates by improving product quality and order accuracy. |
| **Operational Efficiency** | Lower logistics expenses and improve delivery performance. |
| **Decision Making** | Enable data-driven strategic planning using SQL-generated insights. |
| **Cost Optimization** | Identify unnecessary operational expenses and eliminate inefficiencies. |

---

# 🎯 Project Outcomes

The project successfully achieved the following outcomes:

- Designed a normalized SQL database for marketplace operations.
- Built relationships across multiple business entities.
- Cleaned and validated raw marketplace data.
- Performed advanced SQL analysis using joins, CTEs, views, and window functions.
- Calculated business KPIs for revenue and profitability.
- Identified key sources of revenue leakage.
- Evaluated profitability across products and categories.
- Generated actionable business recommendations.
- Demonstrated SQL proficiency through real-world business analysis.
- Delivered a complete end-to-end data analytics case study suitable for portfolio presentation.

---

# 💼 Skills Demonstrated

## Technical Skills

- SQL Database Design
- Relational Database Modeling
- Data Cleaning
- Data Validation
- Data Transformation
- Complex SQL Query Writing
- Joins
- Subqueries
- Common Table Expressions (CTEs)
- Window Functions
- Views
- Aggregate Functions
- KPI Development
- Performance Optimization

---

## Business Skills

- Revenue Leakage Analysis
- Profitability Analysis
- Cost Optimization
- Business Process Analysis
- Operational Performance Evaluation
- Decision Support
- Strategic Recommendation Development
- Business Reporting

---

## Analytical Skills

- Exploratory Data Analysis
- Root Cause Analysis
- Trend Analysis
- Comparative Analysis
- Revenue Analysis
- Profit Analysis
- Customer Behavior Analysis
- Product Performance Analysis
  
---

# ⚠️ Challenges Faced

Throughout the project, several realistic challenges were encountered and addressed.

- Handling incomplete and inconsistent marketplace data.
- Maintaining referential integrity across multiple relational tables.
- Managing complex SQL joins involving several business entities.
- Identifying hidden revenue leakage from multiple cost components.
- Optimizing analytical SQL queries for better readability and performance.
- Balancing business requirements with database normalization principles.
- Ensuring accurate KPI calculations across interconnected datasets.
- Converting technical SQL outputs into meaningful business insights.

---

# 🔮 Future Improvements

This project can be further enhanced through the following improvements:

- Develop an interactive Power BI dashboard for real-time monitoring.
- Integrate Python for advanced statistical analysis and predictive modeling.
- Build machine learning models to predict customer return behavior.
- Automate SQL reporting using scheduled jobs.
- Incorporate customer segmentation analysis.
- Perform cohort and retention analysis.
- Add time-series forecasting for sales and profitability.
- Expand the dataset with real-world marketplace transactions.
- Integrate cloud-based SQL databases such as Azure SQL or PostgreSQL.
- Implement automated anomaly detection for revenue leakage monitoring.

---
