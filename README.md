# Netflix-DE-Project-Azure

This repository demonstrates an end-to-end modern data engineering architecture
built on Azure using **Databricks Delta Live Tables (DLT)** and **ADLS Gen2**.

---

## 🏗 Architecture Overview

<img width="1536" height="1024" alt="Flow" src="https://github.com/user-attachments/assets/9fa38cb8-5cc3-4242-bb5f-8dd1d27eea5c" />



The pipeline follows the **Medallion Architecture** pattern:

- **Bronze Layer** – Raw incremental data ingestion
- **Silver Layer** – Cleaned and transformed data
- **Gold Layer** – Business-ready star schema for analytics

Delta Live Tables (DLT) is used to manage transformations, dependencies,
data quality, and orchestration.

---

## 🔁 Data Flow

1. **Source Systems**
   - Files / Databases
   - Code versioned in GitHub

2. **Ingestion**
   - Azure Data Factory loads incremental data
   - Data is stored in ADLS Gen2 (Bronze layer)

3. **Transformation (DLT)**
   - Bronze → Silver: cleansing, deduplication
   - Silver → Gold: business logic & star schema
   - All layers stored as Delta tables

4. **Consumption**
   - Azure Synapse for warehouse querying
   - Power BI for reporting & dashboards

---

## 🧱 Technology Stack

- **Azure Databricks**
- **Delta Live Tables**
- **Azure Data Lake Gen2**
- **Azure Data Factory**
- **Azure Synapse Analytics**
- **Power BI**
- **GitHub** (CI/CD & version control)

---

## 🔐 Security & Governance

- Azure Entra ID authentication
- Unity Catalog for data governance
- Role-based access control (RBAC)
- Managed identities for storage access

---

## 📌 Key Benefits

- Declarative pipelines with DLT
- Built-in data quality checks
- Scalable & reliable transformations
- Clear separation of raw, refined & serving data
- Production-ready enterprise architecture

---

## 🚀 Notes

> Delta Live Tables requires a **paid Azure Databricks workspace**.
In trial environments, the same logic can be implemented using standard
Delta tables and scheduled jobs.

---

## 👨‍💻 Author
Built for learning, interviews, and real-world Azure Data Engineering use cases.
