# Azure Data Factory Data Engineering Project

![Azure](https://img.shields.io/badge/Azure-DataFactory-blue)
![Azure](https://img.shields.io/badge/Azure-ADLS%20Gen2-blue)
![SQL](https://img.shields.io/badge/SQL-AzureSQL-green)
![GitHub](https://img.shields.io/badge/VersionControl-GitHub-black)

This project demonstrates an **end-to-end Azure Data Engineering pipeline** built using **Azure Data Factory** to ingest relational data from **Azure SQL Database** into **Azure Data Lake Storage Gen2**.

The project implements common enterprise **data ingestion and orchestration patterns** used in modern data platforms.

---

# Project Architecture

<img width="2685" height="549" alt="mermaid-diagram" src="https://github.com/user-attachments/assets/397d6fde-d683-4d34-b282-043a30b31727" />


---

# Data Flow

1. Source data resides in **Azure SQL Database (AdventureWorks SalesLT tables)**

2. **Azure Data Factory pipelines** orchestrate the ingestion process using:

* Copy Activity
* Lookup Activity
* ForEach Activity
* If Condition
* Execute Pipeline

3. Data is ingested into **Azure Data Lake Storage Gen2 landing zone**

4. Data is stored in multiple formats:

* CSV
* JSON
* Pipe-delimited CSV

---

# Technologies Used

| Technology                   | Purpose                |
| ---------------------------- | ---------------------- |
| Azure Data Factory           | Pipeline orchestration |
| Azure SQL Database           | Source system          |
| Azure Data Lake Storage Gen2 | Data Lake storage      |
| GitHub                       | Version control        |

---

# Pipelines Implemented

### Full_DB_Migration

Migrates multiple SQL tables into ADLS using dynamic pipelines.

### Incremental_pipeline

Implements **incremental loading** using watermark logic.

### Ingest_Product_Data

Copies **SalesLT.Product** table data to ADLS.

### Ingest_Product_Description

Loads product description data.

### Ingest_Customer_Data

Copies **SalesLT.Customer** data to ADLS.

### Ingest_Address

Loads **SalesLT.Address** table data.

### Ingest_Cust_Address_Data

Performs **Customer + Address join** and stores output in ADLS.

---

# Control Flow Activities Demonstrated

* Lookup Activity
* ForEach Activity
* If Condition
* Execute Pipeline
* Get Metadata Activity

These activities allow building **dynamic and metadata-driven pipelines**.

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

# Key Data Engineering Concepts Demonstrated

* ETL / ELT pipeline design
* Data ingestion into Data Lake
* SQL joins during ingestion
* Incremental loading patterns
* Pipeline orchestration
* Git version control for ADF

---

# Author

**Harika Murari**

Azure Data Engineer | SQL | Power BI

GitHub
https://github.com/harikamurari2013
