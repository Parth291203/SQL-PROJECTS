# RetailMart Analytics 📊

RetailMart Analytics is an end-to-end, production-style analytics project that
simulates how enterprise retail organizations build SQL-driven analytics
pipelines and executive dashboards. The project focuses on data quality,
KPI computation, alerting, refresh workflows, and dashboard-ready outputs.

---

## 🚀 Project Objective

The primary goals of this project are to:
- Build a scalable analytics layer using SQL
- Track critical retail KPIs for business stakeholders
- Enforce data quality before analytics computation
- Generate dashboard-ready datasets
- Demonstrate real-world analytics engineering practices

---
**** Steps for run this Projects******


Step 1: Analytics Setup

psql -d retailmart -U postgres -f 01_setup/01_create_analytics_schema.sql
psql -d retailmart -U postgres -f 01_setup/02_create_metadata_tables.sql
psql -d retailmart -U postgres -f 01_setup/03_create_indexes.sql

Step 2: Data Quality Checks

psql -d retailmart -U postgres -f 02_data_quality/data_quality_checks.sql

Step 3: KPI Computation

psql -d retailmart -U postgres -f 03_kpi_queries/01_sales_analytics.sql

psql -d retailmart -U postgres -f 03_kpi_queries/02_customer_analytics.sql

psql -d retailmart -U postgres -f 03_kpi_queries/03_product_analytics.sql

psql -d retailmart -U postgres -f 03_kpi_queries/04_store_analytics.sql

psql -d retailmart -U postgres -f 03_kpi_queries/05_operations_analytics.sql

psql -d retailmart -U postgres -f 03_kpi_queries/06_marketing_analytics.sql

Step 4: Alerts & Monitoring

psql -d retailmart -U postgres -f 04_alerts/business_alerts.sql

Step 5: Refresh Analytics

psql -d retailmart -U postgres -f 05_refresh/refresh_all_analytics.sql

Step 6: Export Dashboard Data (JSON

chmod +x 05_refresh/export_all_json.sh
./05_refresh/export_all_json.sh

🔄 Execution Flow

Setup → Data Quality → KPI Computation → Alerts → Refresh → Dashboard Export


*Dashboard Overview

1.Executive-level KPI cards

2.Revenue trends (last 12 months)

3.Department-wise analytics views

4.Interactive and business-friendly UI

## 🧱 Project Structure


```text
RetailMart_Analytics/
│
├── 01_setup/
│   ├── 01_create_analytics_schema.sql
│   ├── 02_create_metadata_tables.sql
│   └── 03_create_indexes.sql
│
├── 02_data_quality/
│   └── data_quality_checks.sql
│
├── 03_kpi_queries/
│   ├── 01_sales_analytics.sql
│   ├── 02_customer_analytics.sql
│   ├── 03_product_analytics.sql
│   ├── 04_store_analytics.sql
│   ├── 05_operations_analytics.sql
│   └── 06_marketing_analytics.sql
│
├── 04_alerts/
│   └── business_alerts.sql
│
├── 05_refresh/
│   ├── refresh_all_analytics.sql
│   └── export_all_json.sh
│
├── 06_dashboard/
│   ├── index.html
│   ├── styles.css
│   └── charts.js
│
└── 07_documentation/
    └── business_logic.md


