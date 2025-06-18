# 🚴‍♂️ Azure Modern Data Warehouse Project – Bike Share Analytics

This project demonstrates a **complete modern data warehouse pipeline** built with **Azure cloud services**. It covers data ingestion, transformation, and loading into a **star schema** using Azure Synapse Analytics, with operational data sourced from PostgreSQL.

---

## 📈 Business Case

A **bike share company** aims to analyze rider behavior, trip patterns, and payment records to improve **operational efficiency and customer experience**. This project ingests their transactional data and organizes it into a **star schema** to support **reporting, dashboards, and business intelligence**.

---

## 🏗️ Architecture Overview

```mermaid
graph TD;
    A["PostgreSQL Database"] -->|Python Ingestion Script| B["Azure PostgreSQL"]
    B -->|Synapse Ingest Wizard| C["Azure Data Lake"]
    C --> D["Serverless SQL Pool (External Tables)"]
    D --> E["Transformations via T-SQL"]
    E --> F["Dedicated SQL Pool (Star Schema)"]
    F --> G["BI / Analytics Tools"]
