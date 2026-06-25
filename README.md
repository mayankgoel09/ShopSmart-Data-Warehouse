# ShopSmart Data Warehouse Project

## Project Overview
This project is an end-to-end automated Data Warehouse solution, engineered from the ground up to manage the full lifecycle of business data. It implements a robust, multi-layer architecture—**Bronze (Raw)**, **Silver (Cleaned/Standardized)**, and **Gold (Reporting Ready)**—to transform raw source files into high-value business intelligence.

## Architecture & Layers
* **Bronze Layer (Ingestion)**: The entry point where raw CRM and ERP data is ingested from external CSV sources into the database.
* **Silver Layer (Transformation)**: The processing zone where data is cleaned, validated, normalized, and deduplicated for consistency.
* **Gold Layer (Modeling)**: The presentation layer where data is structured into a Star Schema (Facts and Dimensions), providing an optimized environment for reporting and analytics.

## Technical Implementation
* **Pipeline Automation**: Developed custom ETL stored procedures (`bronze.load_bronze`, `silver.load_silver`) to automate the transition of data through the layers.
* **Bi-directional Synchronization**: Integrated `bcp` (Bulk Copy Program) logic to ensure real-time synchronization between the database and the filesystem.
* **Advanced Analytics**: Engineered a suite of analytical SQL views covering:
    * **Magnitude Analysis**: Quantifying data distribution and revenue metrics.
    * **Trend & Cumulative Analysis**: Tracking growth, seasonality, and running totals.
    * **Performance Benchmarking**: Year-over-Year (YoY) and Month-over-Month (MoM) analysis using `LAG()` and window functions.
    * **Segmentation**: Advanced customer and product tiering (e.g., VIP/Regular/New customers, High/Low-performer products).
    * **Consolidated Reporting**: High-level reporting views for actionable business insights.

## Project Workflow
1.  **System Setup**: Database initialization and schema creation.
2.  **Raw Data Loading**: Execute `EXEC bronze.load_bronze` for automated ingestion and file syncing.
3.  **Data Processing**: Run `EXEC silver.load_silver` to transform raw inputs into clean, reliable data.
4.  **Reporting & Insights**: Query the `gold` schema views for real-time business analytics and report generation.

## Key Technologies
* **SQL Server**: Relational database engine for storage and ETL logic.
* **T-SQL**: Advanced window functions, CTEs, and stored procedures for complex data modeling.
* **File System Automation**: `BULK INSERT` and `bcp` utility integration for seamless file-to-database workflows.
