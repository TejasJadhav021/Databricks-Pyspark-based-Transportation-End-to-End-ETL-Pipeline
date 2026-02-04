# 🚕 Transportation End-to-End ETL Pipeline (Databricks + PySpark)

## 📌 Project Overview
This project implements a **scalable end-to-end Transportation ETL pipeline** using **Databricks, PySpark, Delta Live Tables (DLT), Delta Lake, and Amazon S3**.  
The pipeline ingests raw transportation data, processes it through **Bronze–Silver–Gold (Medallion Architecture)** layers, and produces **analytics-ready datasets** for reporting and business insights.

---

## 🎯 Business Problem
Transportation companies generate **large volumes of data** from multiple sources such as trips, cities, and dates.  
However:
- Data is often **raw and inconsistent**
- Traditional systems **do not scale efficiently**
- Poor data quality leads to **unreliable analytics**

This project solves the problem by building a **scalable and automated ETL pipeline** that converts raw data into **clean, trusted, analytics-ready datasets**.

---

## 🏗️ Architecture (Medallion Architecture)

- **Bronze Layer**
  - Raw data ingestion from Amazon S3
  - Schema-flexible and fault-tolerant
  - Corrupt records captured without failing the pipeline

- **Silver Layer**
  - Cleaned, standardized, and validated data
  - Data quality checks using DLT expectations
  - CDC-based upserts to keep latest records

- **Gold Layer**
  - Business-friendly, analytics-ready views
  - Optimized for reporting and dashboards

---

## 🧰 Technologies Used
- Databricks
- Apache Spark (PySpark)
- Delta Live Tables (DLT)
- Delta Lake
- Amazon S3
- AWS IAM
- SQL

---

## 🔄 Data Pipeline Flow
1. Raw transportation data is ingested from **Amazon S3** into the **Bronze layer**
2. Corrupt and malformed records are captured safely
3. Data is cleaned, validated, and standardized in the **Silver layer**
4. **CDC (Change Data Capture)** is used to upsert latest records
5. **Gold views** are created for analytics and reporting

---

## 📊 Key Features
- Incremental data ingestion
- Schema evolution support
- Data quality validation using DLT expectations
- CDC-based upserts (SCD Type 1)
- Auto-optimized Delta tables
- Analytics-ready Gold views
- Scalable cloud-based design

---
## 📁 Project Structure

```text
├── bronze/
│   ├── city_bronze.py
│   ├── trips_bronze.py
│
├── silver/
│   ├── city_silver.py
│   ├── trips_silver_cdc.py
│   ├── calendar_silver.py
│
├── gold/
│   ├── fact_trips_view.sql
│
├── README.md
