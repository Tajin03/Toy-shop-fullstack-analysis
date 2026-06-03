# Full-Stack Retail Intelligence & Data Pipeline (Toy Shop)

An end-to-end data analytics and business intelligence platform built to monitor transaction velocity, analyze geographic revenue distributions, and track real-time margin variances for a multi-category toy retailer.

## 📊 Project Highlights & Features
* **Total Transaction Volume Analytics:** A waterfall breakdown tracking cumulative sales volumes across multiple product categories (Action Figures, Art & Crafts, Construction, etc.).
* **Sales Velocity & Profitability Tracking:** Real-time variance tracking against dynamic targets with automated threshold calculations.
* **Geographic Revenue Distribution:** Geospatial visualization mapping market performance and regional order densities.
* **Advanced Time-Series Modeling:** Dynamic date and category filters allowing granular deep-dives by Day, Week, or Month.

## 🛠️ Tech Stack & Architecture
* **Frontend/BI Layer:** Metabase UI / Embedded Interactive Dashboards
* **Database & Transformation Layer:** SQL (Advanced Joins, Window Functions, and Subqueries for time-series aggregation)
* **Backend Pipeline:** Python (For data ingestion, cleaning, and metric calculation)
* **Environment:** Localhost development server

## 🔍 Sample Complex SQL Query
*Tip: Paste one of your best queries here to prove your SQL skills!*
```sql
-- Example: Calculating weekly rolling profit margins against targeted estimates
SELECT 
    week_start,
    SUM(profit) AS weekly_profit,
    3000 AS weekly_target,
    (SUM(profit) - 3000) AS variance
FROM retail_sales
GROUP BY week_start
ORDER BY week_start DESC;
