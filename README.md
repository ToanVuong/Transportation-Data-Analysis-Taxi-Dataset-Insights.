# NYC-Taxi-Data-Analytics-using-Microsoft-Fabric-Lakehouse
# 📊 Data Engineering Application for Data Processing

## 📌 1. Introduction

This project is a final assignment for the **Data Engineering (CO5173)** course, focusing on applying **Microsoft Fabric Lakehouse** to build an end-to-end data pipeline for managing, processing, and analyzing large-scale data.

The project consists of two main parts:

* Overview and experimentation with Microsoft Fabric Lakehouse
* 🚕 Building a data pipeline for NYC Taxi data management and analysis

---

## 👥 2. Team Information

* **Supervisor:** Assoc. Prof. Dr. Vo Thi Ngoc Chau

### Team Members

* Mai Quang Vinh – 2570375
* Vuong Minh Toan – 2491057
* Do Hoang Linh – 2211844
* Dam Quang Phuc – 2570483

---

## 🎯 3. Project Objectives

* Study the architecture of **Microsoft Fabric Lakehouse**
* Compare with **Azure Synapse Analytics** and **Databricks**
* Experiment with key components (Lakehouse, Notebook, Dataflow, Power BI)
* 🚕 Apply to a real-world dataset: NYC Taxi
* Build a pipeline using **Medallion Architecture (Bronze – Silver – Gold)**
* Generate insights and business recommendations

---

## 🧠 4. Overview of Microsoft Fabric Lakehouse

### 4.1 What is Fabric Lakehouse?

* Combines **Data Lake + Data Warehouse**
* Supports BI, AI/ML on a unified platform
* ⚡ Follows the **OneLake – One Copy** principle to reduce duplication

### 4.2 Core Concepts

* **Data Warehouse**: structured data, optimized for BI and reporting
* **Data Lake**: raw data, suitable for Big Data & ML
* **Lakehouse**: hybrid model combining both advantages

### 4.3 Architecture

* 🗄️ OneLake as centralized storage
* Supports 200+ connectors
* Enables **zero-copy (shortcuts)** from AWS S3, ADLS
* Uses open formats: **Parquet, Delta Lake**
* Accessible via Spark, SQL Analytics, Power BI

---

## 🏗️ 5. Medallion Architecture

* 🥉 **Bronze**: raw data, ensures traceability
* 🥈 **Silver**: cleaned and standardized data
* 🥇 **Gold**: optimized for BI and analytics

---

## ⚖️ 6. Platform Comparison

* **Microsoft Fabric**: simple, all-in-one, Microsoft ecosystem
* **Databricks**: strong for Big Data & AI/ML
* **Azure Synapse**: suitable for traditional data warehousing

---

## ⚙️ 7. Experiments on Microsoft Fabric

### 7.1 Basic Workflow

1. Create workspace
2. Create Lakehouse
3. Load data
4. Create tables
5. Use Notebook (Spark SQL)
6. Build Semantic Model
7. 📊 Visualize with Power BI

### 7.2 Cloud Integration

* Use Dataflow Gen2 for ingestion
* 🌐 Connect to cloud databases
* 🔄 Sync data via FastAPI

### Results

* Fabric supports a full end-to-end pipeline
* Data can be successfully synchronized and updated

---

## 🚕 8. Main Use Case: NYC Taxi Data

### Dataset

* **NYC TLC Trip Record Data**
* 📦 Large-scale dataset (billions of records)
* Includes Yellow & Green taxis
* Stored in **Parquet** format

### Key Features

* Timestamps: pickup, dropoff
* Distance, fare, tip
* Passenger count, payment type

### Engineered Features

* ⏱️ Trip duration
* 🚗 Speed
* 📅 Day / Hour
* 🎯 Rush hour / Holiday

---

## 🚀 9. Why Microsoft Fabric

* End-to-end architecture: ingestion → storage → processing → serving
* 🧩 Unified tooling (Spark, SQL, Power BI)
* ⚡ Zero-copy analytics
* ☁️ SaaS → fast deployment, low maintenance

---

## 🔄 10. NYC Taxi Pipeline

### 🥉 Bronze

* Data ingestion
* Remove null records

### 🥈 Silver

* Data cleaning & transformation
* Time feature engineering
* Join with location data

### 🥇 Gold

* Build BI-ready tables
* Filter year 2025
* Optimize queries

### 📊 Power BI

* Build Semantic Model
* Create dashboards

---

## 🔐 11. Governance & Security

* Workspace role management
* 🔒 RLS, CLS
* Secure data sharing via views
* Data lineage & monitoring

---

## ⚙️ 12. Automation & Optimization

* Build ETL pipelines
* ⏰ Schedule triggers
* Incremental processing
* Optimize with **OPTIMIZE, Z-Order, partitioning**
* Monitor performance and cost

---

## 📊 13. Key Insights

* ~6 million trips analyzed
* 🚗 Average speed: ~13 MPH
* 🏙️ ~80% trips in Manhattan
* 👤 ~78% single-passenger trips
* 📅 Peak days: Wednesday & Thursday
* 🕕 Peak hours: 18:00–19:00
* 🌙 Lowest demand: 03:00–05:00
* ✈️ EWR trips: high cost (~$90), ~40 minutes

---

## ⚠️ 14. Anomaly Analysis

### Invalid Anomalies

* <1% of data
* Unrealistic distances with low fares
* ❌ Likely due to GPS or mapping errors → should be removed

### Business-valid Anomalies

* ✈️ Airport trips (EWR)
* High cost due to surcharge & tolls
* ✅ Valid → should be analyzed separately

---

## 💡 15. Recommendations

### 🚕 Fleet Allocation

* Increase supply in Manhattan (17:00–19:00)

### 💰 Pricing Strategy

* Apply flat-rate pricing for airport trips

### 🤝 Ride Pooling

* High potential due to single-passenger dominance

### ⚙️ Operations Optimization

* Use 03:00–05:00 for maintenance

---

## 🧪 16. Fabric Trial Evaluation

### ✅ Advantages

* All-in-one platform
* No infrastructure setup required
* ⏳ Free for 60 days
* Reduced data duplication

### ⚠️ Limitations

* Limited resources
* Possible performance throttling
* Not suitable for production

---

## 🛠️ 17. Technologies Used

* Microsoft Fabric
* Lakehouse / OneLake
* Spark, SQL
* Power BI
* FastAPI
* Delta Lake, Parquet

---

## 🏁 18. Conclusion

The project successfully built a complete data pipeline on **Microsoft Fabric**, from ingestion to visualization.

Results demonstrate that Fabric is a strong platform for modern data workloads, especially with its integration with Power BI and the **Lakehouse + Medallion architecture**.

---

## 🚀 19. Future Work

* Extend to multi-year datasets
* 🤖 Apply ML/forecasting models
* Improve monitoring & alerting
* Integrate external data (weather, events)
* Compare cost & performance across platforms

