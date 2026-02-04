# Databricks-Pyspark-based-Transportation-End-to-End-ETL-Pipleline-
This project implements an end-to-end transportation data ETL pipeline on Databricks using PySpark and Spark’s Declarative Pipeline framework (Delta Live Tables – DLT).
The pipeline ingests raw transportation data such as trip details, city metadata, vehicle information, timestamps, and fares from Amazon S3, processes it through Bronze, Silver, and Gold layers, and stores optimized, analytics-ready data in Delta Lake.

Delta Live Tables enables a declarative, reliable, and scalable ETL design, where data quality rules, transformations, dependencies, and incremental processing are managed automatically. The architecture follows modern lakehouse principles, supporting both batch and streaming ingestion with built-in data validation and observability.
