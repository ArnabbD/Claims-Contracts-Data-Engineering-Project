# End-to-End Data Engineering Pipeline using Databricks

## Overview
This project demonstrates how to build a production-style **insurance data pipeline** in **Databricks**, following the **Medallion Architecture (Bronze, Silver, Gold)**.  
It simulates real-world challenges in handling claims and contracts data, including **data quality**, **schema evolution**, **deduplication**, and **incremental ingestion**.

## Architecture
- **Bronze Layer**: Ingest raw claims and contracts data (CSV → Delta).
- **Silver Layer**: Clean, standardize, and deduplicate records using Delta Lake features (Delta MERGE).
- **Gold Layer**: Create a unified Transactions table by joining claims and contracts with business logic applied.
- **Automation**: Proposed **Autoloader** for continuous ingestion of new data batches.

## Tech Stack
- **Databricks** (Serverless + Unity Catalog)
- **Delta Lake**
- **PySpark**
- **Medallion Architecture (Bronze, Silver, Gold)**
- **Autoloader (for incremental ingestion)**

## Key Features
- Raw → Clean → Curated data transformation
- Deduplication and upserts with Delta MERGE
- Handling late-arriving and schema-evolving data
- End-to-end automated pipeline design

## How to Run
1. Upload the `sample_data/` files into Databricks Volumes.
2. Run the notebooks in sequence: Bronze → Silver → Gold.
3. Review the final Transactions table in Gold.
