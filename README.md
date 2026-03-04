# Azure Data Factory Data Engineering Project

![Azure](https://img.shields.io/badge/Azure-DataFactory-blue)
![Azure](https://img.shields.io/badge/Azure-ADLS%20Gen2-blue)
![SQL](https://img.shields.io/badge/SQL-AzureSQL-green)
![GitHub](https://img.shields.io/badge/VersionControl-GitHub-black)

This project demonstrates an **end-to-end Azure Data Engineering pipeline** using **Azure Data Factory (ADF)** to ingest relational data from **Azure SQL Database** into **Azure Data Lake Storage Gen2 (ADLS)**.

The goal of this project is to showcase common **data ingestion and orchestration patterns used in real-world data engineering pipelines.**

---

# Project Overview

The pipelines extract data from **Azure SQL Database (AdventureWorks SalesLT tables)** and load it into **Azure Data Lake Storage Gen2** in multiple file formats.

The project demonstrates:

* Full database migration pipelines
* Incremental data ingestion
* SQL joins during ingestion
* Pipeline orchestration using ADF control flow activities
* Data storage in multiple formats

---

# Architecture

![ADF Architecture](architecture.png)

---

# Data Flow

1. Source data is stored in **Azure SQL Database (SalesLT tables)**.

2. **Azure Data Factory pipelines** orchestrate the ingestion process.

3. ADF uses **Copy Activity and SQL queries** to extract data.

4. Data is written to **Azure Data Lake Storage Gen2 Landing Zone**.

5. Data is stored in different formats:

* CSV
* JSON
* Pipe-delimited CSV

---

# Technologies Used

| Technology                   | Purpose                |
| ---------------------------- | ---------------------- |
| Azure Data Factory           | Pipeline orchestration |
| Azure SQL Database           | Source data system     |
| Azure Data Lake Storage Gen2 | Data Lake storage      |
| GitHub                       | Version control        |

---

# Pipelines Implemented

### Full_DB_Migration

Migrates multiple SQL tables into ADLS using dynamic pipelines.

### Incremental_pipeline

Implements **incremental loading** using watermark logic.

### Ingest_Product_Data

Copies **SalesLT.Product** table data into ADLS.

### Ingest_Product_Description

Loads product description data.

### Ingest_Customer_Data

Copies **SalesLT.Customer** data into ADLS.

### Ingest_Address

Loads **SalesLT.Address** table data.

### Ingest_Cust_Address_Data

Performs **Customer + Address join** and stores the result in ADLS.

---

# Control Flow Activities Used

This project demonstrates several Azure Data Factory orchestration activities:

* Lookup Activity
* ForEach Activity
* If Condition
* Execute Pipeline
* Get Metadata Activity

These activities help build **dynamic and metadata-driven pipelines**.

---

# Skills Demonstrated

* Azure Data Factory
* Data Pipeline Design
* Azure SQL Database
* Azure Data Lake Storage Gen2
* ETL / ELT pipeline development
* Incremental Data Loading
* Pipeline orchestration
* Git version control

---

# Repository Structure

```
adf-data-engineering-project
│
├── pipeline
├── dataset
├── linkedService
├── factory
├── publish_config.json
└── README.md
```

---

# Future Improvements

* Implement Bronze / Silver / Gold data lake layers
* Add transformations using Azure Databricks
* Implement CI/CD pipelines using Azure DevOps
* Add data validation and monitoring

---

# Author

**Harika Murari**

Azure Data Engineer | SQL | Power BI

GitHub
https://github.com/harikamurari2013
