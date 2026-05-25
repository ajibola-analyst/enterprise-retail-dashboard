# Enterprise Commercial Analytics & Operations Engine

## Executive Summary
This repository contains an end-to-end data analytics solution developed to track commercial performance, optimize logistics, and segment customer profitability for a global retail entity. Built entirely within Excel, this project demonstrates advanced data modeling, complex Pivot Table architectures, and the translation of raw transactional logs into a clean, spacious, "app-like" executive dashboard.

The objective of this analysis was to move beyond basic reporting and uncover strategic insights regarding revenue drivers, operational friction in shipping, and customer retention metrics. 

## Technical Stack
* **Data Processing & ETL:** Excel (Power Query/Advanced Formulas for data cleaning and feature engineering)
* **Data Modeling:** Flat-file dimensional modeling, Primary Key generation, Time Intelligence
* **Visualization & UI/UX:** Advanced Pivot Tables, Pivot Charts, Custom KPI Dashboards with modern, low-clutter, spacious aesthetics.

## Data Architecture & ETL Process
The raw dataset consisted of transactional logs containing thousands of records. To prepare this data for a scalable analytical dashboard, a rigorous data cleaning and feature engineering pipeline was executed:

1. **Schema Standardization:** Removed structural inconsistencies, cleaned delimiters, and standardized headers for seamless pivot integration.
2. **Feature Engineering (Time Intelligence):** Engineered `Year` and `Year Fixed` columns from raw timestamps to enable YOY (Year-Over-Year) aggregations.
3. **Operational Metrics (Logistics):** Calculated `Days to Ship` by extracting the delta between `Ship_Date` and `Order_Date` to evaluate supply chain efficiency.
4. **Customer Identity Resolution:** Generated `Unique Customer Name`, `UniqueCustomerKey`, and `Rank` arrays to handle duplicate identities and enable precise distinct-count customer analytics.

## Strategic Business Questions Addressed
The analytics engine answers core commercial questions across three domains:

### 1. Revenue & Profitability Drivers
* **Geographic Performance:** Identified the Top 10 countries by gross sales volume and assessed the impact of discount strategies on these regions.
* **Product Margin Analysis:** Isolated the Top 5 most profitable products, and evaluated top performers across a combined matrix of Sales, Profit, and Quantity.
* **Loss-Leader Identification:** Highlighted the 7 lowest-performing categories by profit to inform potential discontinuation or repricing strategies.
* **Urban Market Analysis:** Mapped the highest-performing cities by category and total sales.

### 2. Customer Segmentation
* **Demographic Density:** Analyzed customer distribution to determine which states hold the highest market penetration.
* **Value Tiering:** Segmented the customer base into top-performing and low-performing cohorts to identify key accounts and inform re-engagement strategies.

### 3. Operational & Supply Chain Friction
* **Fulfillment Efficiency:** Developed a Bubble Chart visualization plotting the engineered `Days to Ship` metric against `Ship Mode` to identify logistics bottlenecks.
* **Turnover Velocity:** Evaluated which shipment modes generate the highest turnover volume.
* **Volume vs. Revenue Correlation:** Assessed the statistical significance and relationship between purchase quantities and total gross sales.

## 📂 Repository Structure
* 📂 **`data/`**
  * `raw_sales_data.csv` *(The original, uncleaned transactional log)*
  * `processed_sales_data.xlsx` *(The final ETL-processed dataset with engineered features)*
* 📂 **`dashboards/`** * `executive_summary_view.jpg` *(High-level commercial KPIs)*
  * `operational_insights_view.jpg` *(Logistics and supply chain metrics)*
  * `performance_drilldown.jpg` *(Granular product and regional performance)*