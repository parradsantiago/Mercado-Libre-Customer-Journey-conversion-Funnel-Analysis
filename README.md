# 🛒 Mercado Libre: Customer Journey & conversion Funnel Analysis

## 📋 Project Overview
This project provides a comprehensive analysis of the customer conversion funnel for Mercado Libre, utilizing user behavior micro-data from January to August 2025. The objective is to identify friction points and drop-off rates across the user journey—from the initial visit to the final purchase—segmented by country to uncover regional performance variations.

## 🚀 SQL Methodology & Architecture
The analysis was built using a robust SQL structure with **CTEs (Common Table Expressions)** to ensure modularity, readability, and high performance:

1.  **Stage Segmentation:** Granular definition of each funnel step: `first_visit` → `select_item` → `add_to_cart` → `begin_checkout` → `shipping_info` → `payment_info` → `purchase`.
2.  **Behavioral Logic:** Implemented `LEFT JOIN` operations anchored on the `first_visit` event to strictly track the progression of unique users through the ecosystem.
3.  **Conversion Rate Modeling:** Advanced calculation of conversion rates per stage using `NULLIF` logic to prevent division-by-zero errors and ensure data integrity.

## 📊 Key Analytical Insights
* **Cross-Border Performance:** Hierarchical ranking of markets based on final conversion efficiency (`conversion_purchase`).
* **Friction Point Identification:** Pinpointing critical gaps between high-intent actions (e.g., `add_to_cart`) and the start of the checkout process.
* **Checkout Optimization:** Analysis of user drop-off during the shipping and payment information entry phases to suggest UX improvements.

## 🧠 Technical Justification: SQL for Product Analytics
This specific SQL architecture was chosen for:
* **Scalability:** The code is easily adaptable to new event types or different time-frames.
* **Geographical Granularity:** Grouping by `country` provides actionable insights for regional business strategies and localized marketing efforts.
* **Data Transparency:** The use of sequential CTEs allows for easy debugging and clear visualization of the data transformation layers.

## 🛠️ Tech Stack
* **Language:** SQL (Google BigQuery / PostgreSQL)
* **Techniques:** CTEs, Multi-layer Aggregations, Behavioral Joins, Conversion Rate Optimization (CRO) logic.

## 📁 Repository Structure
* `funnel_analysis.sql`: Source code for the conversion and journey query.
* `Funnel_analysis_executive_Summary.xlsx`: Executive Summary
* `README.md`: Project documentation and methodology.