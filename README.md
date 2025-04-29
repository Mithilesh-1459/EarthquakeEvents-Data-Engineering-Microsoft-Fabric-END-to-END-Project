# 🌎 Earthquake Events Data Engineering Project (Microsoft Fabric)


## 📖 Project Overview

This project focuses on building a **data engineering pipeline** using **Microsoft Fabric** tools to ingest, transform, and analyze **Worldwide Earthquake Events** from the **USGS API**.  
The goal is to implement a **Medallion Architecture** (Bronze, Silver, and Gold layers) using **Azure Synapse Data Engineering**, **Lakehouse**, and **Azure Data Factory**, ultimately enabling business-ready insights via **Power BI** visualizations.

---

## 🎯 Project Goals

- **Ingest** earthquake event data from the USGS API.
- **Process** and **transform** the data through structured multihop stages:
  - **Bronze**: Raw ingestion of API data (JSON format).
  - **Silver**: Cleansed and transformed data ready for analysis.
  - **Gold**: Business-ready, tabular format optimized for reporting.
- **Visualize** earthquake data using **Power BI**.
- **Operationalize** the data pipeline using **Microsoft Fabric's Data Factory**.

---
## 🏛 Architecture

![Architecture](./Architecture/Architecture%20%26%20Implementation%20.png)

---

## 🛠️ Tools and Technologies

| Tool/Service                | Purpose                                         |
|----------------------------|-------------------------------------------------|
| **Microsoft Fabric**       | Unified platform for data engineering, orchestration, and analytics |
| **Azure Synapse Data Engineering** | Build and manage the Lakehouse |
| **Azure Data Factory**     | Data pipeline orchestration and automation |
| **Azure Data Lakehouse**   | Scalable data storage (structured/unstructured) |
| **Apache Spark** (PySpark) | API data ingestion and processing |
| **Power BI**               | Data visualization and business reporting |
| **USGS API**               | Source of global earthquake data |

---

## 🏗️ Project Architecture

1. **API Data Ingestion**:  
   - PySpark scripts fetch worldwide earthquake events from the USGS API.
   
2. **Medallion Architecture** (Multihop Design Pattern):
   - **Bronze Layer**:  
     - Raw ingestion of API responses in JSON format.
   - **Silver Layer**:  
     - Data cleansing, type casting, and transformation to structured format.
   - **Gold Layer**:  
     - Business-ready tabular data, enriched and cleaned for reporting.

3. **Storage and Processing**:
   - Stored in **Azure Data Lakehouse** using **Delta Format** tables.
   - Lakehouse automatically provides **SQL Analytics Endpoints** and **Semantic Models**.

4. **Orchestration**:
   - **Azure Data Factory** pipelines schedule the ingestion and processing jobs daily.

5. **Analytics and Visualization**:
   - Power BI connects to the Lakehouse SQL Endpoint for creating dynamic earthquake reports.

---

## 📂 Project Structure

```
/earthquake-events-pipeline
 ├── /bronze
 │     └── 01 Worldwide Earthquake Events API - Bronze Layer Processing.ipynb
 ├── /silver
 │     └── 02 Worldwide Earthquake Events API - Silver Layer Processing.ipynb
 ├── /gold
 │     └── 03 Worldwide Earthquake Events API - Gold Layer Processing.ipynb
 ├── /images
 │     └── Architecture & Implementation .png
 └── README.md

```

---

## ⚡ Key Concepts Implemented

- **Medallion Architecture** (Bronze, Silver, Gold data layers)
- **Delta Tables** for versioned, transactional data in Lakehouse
- **PySpark** for large-scale data ingestion and transformation
- **Automated Data Pipelines** with Microsoft Fabric Data Factory
- **Business Intelligence** using Power BI Semantic Models

---

## 🚀 How It Works

- **Step 1**: PySpark notebooks pull earthquake data from USGS API.
- **Step 2**: Raw JSON data is stored in the **Bronze Layer**.
- **Step 3**: Transformation notebooks clean the data for the **Silver Layer**.
- **Step 4**: Business rules and structuring finalize data into the **Gold Layer**.
- **Step 5**: Power BI connects to the Lakehouse **SQL Analytics Endpoint** to visualize the global earthquake patterns.

---

## 📈 Visualization

The final Power BI report includes:
- Earthquake event heatmaps
- Event frequency trends
- Magnitude distribution charts
- Geographic drill-down reports

---

## 🧩 Prerequisites

- Basic knowledge of **SQL**, **Python**, and **Spark**.
- Familiarity with **Data Lakehouse concepts**.
- Microsoft Fabric Account (Trial or Licensed).
- Administrative permissions to enable necessary Fabric features.

---

## 🏅 Future Enhancements

- Automate deployment using GitHub Actions or Azure DevOps.
- Extend the model to support real-time streaming ingestion.
- Enrich earthquake data with geospatial data layers (e.g., tectonic plates).
- Set up advanced alerts and ML-based anomaly detection models.

