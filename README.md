# 🏗️ ShopSmart Data Warehouse Project

## 📌 Project Overview

The **ShopSmart Data Warehouse Project** is an end-to-end SQL Server data warehousing solution designed to transform raw CRM and ERP datasets into analytics-ready business data. Following the **Medallion Architecture (Bronze → Silver → Gold)**, the project demonstrates how to build a scalable ETL pipeline that supports business intelligence and reporting.

The solution automates data ingestion, cleansing, transformation, and dimensional modeling, producing a robust **Star Schema** optimized for analytical queries and dashboard development.

---

## 🎯 Project Objectives

* Build a scalable SQL Data Warehouse from scratch.
* Automate ETL processes using SQL Server stored procedures.
* Integrate CRM and ERP datasets into a unified data model.
* Clean, validate, and standardize raw business data.
* Design a Star Schema for efficient analytical reporting.
* Generate business-ready views for downstream BI tools such as Power BI and Tableau.

---

# 🏛️ Data Warehouse Architecture

The project follows the **Medallion Architecture**, separating data into three logical layers.

## 🥉 Bronze Layer – Raw Data Ingestion

The Bronze layer acts as the landing zone for source data.

**Key Features**

* Imports CRM and ERP CSV files using **BULK INSERT**
* Preserves raw source data without transformation
* Stores data in staging tables
* Automates ingestion using the `bronze.load_bronze` stored procedure
* Synchronizes files and database using the **BCP (Bulk Copy Program)** utility

---

## 🥈 Silver Layer – Data Cleansing & Transformation

The Silver layer transforms raw data into reliable, standardized datasets.

**Transformations Performed**

* Data validation
* Duplicate removal
* Missing value handling
* Data normalization
* Standardization of formats
* Business rule implementation
* Integration of CRM and ERP datasets
* Preparation of clean datasets for analytics

The entire transformation pipeline is automated using the `silver.load_silver` stored procedure.

---

## 🥇 Gold Layer – Business Intelligence & Analytics

The Gold layer presents curated, analytics-ready data using a **Star Schema**.

### Dimension Views

* `gold.dim_customers`
* `gold.dim_products`

### Fact Views

* `gold.fact_sales`

These views consolidate data across multiple source systems, providing a clean and optimized structure for reporting, dashboards, and advanced analytics.

---

# 🔄 ETL Workflow

```text
CSV Files (CRM & ERP)
          │
          ▼
 Bronze Layer (Raw Data)
          │
          ▼
 Silver Layer (Cleaned & Standardized Data)
          │
          ▼
 Gold Layer (Star Schema)
          │
          ▼
 Business Intelligence & Reporting
```

---

# 📊 Analytical Reporting

The Gold layer includes analytical SQL views that provide actionable business insights.

### Revenue & Sales Analysis

* Revenue metrics
* Sales trends
* Product performance
* Customer purchasing behavior

### Trend Analysis

* Monthly sales trends
* Running totals
* Cumulative revenue
* Seasonality analysis

### Performance Benchmarking

* Year-over-Year (YoY) analysis
* Month-over-Month (MoM) analysis
* Growth calculations using `LAG()`
* Ranking with window functions

### Customer & Product Segmentation

* VIP customers
* Regular customers
* New customers
* High-performing products
* Low-performing products

### Consolidated Reporting

Business-ready reporting views designed for Power BI, Tableau, or other BI platforms.

---

# 🛠 Technical Implementation

### ETL Automation

* Stored Procedures
* Automated data loading
* Layer-to-layer processing

### Data Integration

* CRM Data
* ERP Data
* Multi-source integration

### SQL Features Used

* BULK INSERT
* BCP (Bulk Copy Program)
* Views
* Common Table Expressions (CTEs)
* Window Functions
* ROW_NUMBER()
* LAG()
* CASE Statements
* Joins
* Aggregate Functions
* Stored Procedures
* Schema Design
* Star Schema Modeling

---

---

# 🚀 Key Skills Demonstrated

* SQL Server
* T-SQL
* Data Warehousing
* ETL Pipeline Development
* Data Modeling
* Star Schema Design
* Data Cleansing
* Data Transformation
* Stored Procedures
* Window Functions
* Business Intelligence
* Database Design
* Data Engineering Fundamentals

---

# 🔮 Future Enhancements

* Develop interactive Power BI dashboards connected to the Gold layer.
* Optimize query performance through indexing and partitioning.
* Implement incremental data loading.
* Schedule ETL jobs using SQL Server Agent.
* Extend the warehouse with additional business domains.

---

# 👤 Author

**Mayank Goel**

Aspiring Data Analyst | SQL | Python | Power BI | Excel

If you found this project helpful, feel free to ⭐ the repository or connect with me on LinkedIn.
