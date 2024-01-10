Azure Data Engineering Project: Healthcare Revenue Cycle Management (RCM)

This project focuses on building a robust data pipeline for a healthcare revenue cycle management system using the Azure Data Engineering stack. RCM involves managing financial aspects from patient appointment scheduling to provider payments, emphasizing key objectives such as minimizing accounts receivable (AR) collection periods and improving cash flow.

Key Features and Solution Architecture

Data Sources:

EMR data from Azure SQL DB (Patients, Providers, Departments, Encounters, Transactions).
Claims data from flat files in Azure Data Lake.
NPI and ICD codes from public APIs.
Architecture:

Medallion approach with Bronze (parquet, raw), Silver (cleaned, enriched, CDM, SCD2), and Gold (aggregated, fact, and dimension tables) layers.
Azure Data Factory for data ingestion, Azure Databricks for transformation, and Azure Data Lake Storage for managing data layers.
Pipeline Design:

Config-driven pipelines for scalable and reusable data processing.
Incremental and full data loading with audit mechanisms.
Key Vault for secure credential management.
Enhancements:

Parallel pipeline execution, naming conventions, and retries for robustness.
Transition to Unity Catalog for centralized metadata management.
