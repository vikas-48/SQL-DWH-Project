# SQL-DWH-Project
# Data Warehouse and Analytics Project

This repository contains an **end-to-end Data Warehouse and Analytics implementation** built using **SQL Server**.  
The project focuses on designing a clean data architecture, implementing ETL pipelines, and enabling analytical reporting on consolidated business data.

The primary goal of this project was to **apply real-world data engineering concepts** such as data modeling, data quality handling, and SQL-based analytics in a structured and reproducible way.

---

## 🏗️ Architecture Overview

The data warehouse is implemented using a **Medallion Architecture** approach with three logical layers: **Bronze**, **Silver**, and **Gold**.

![Data Architecture](docs/data_architecture.png)

### Bronze Layer
- Raw data ingestion layer
- Source data is loaded directly from CSV files into SQL Server tables
- No transformations are applied at this stage to preserve original data

### Silver Layer
- Data cleansing and standardization layer
- Handles null values, formatting inconsistencies, and normalization
- Prepares data for analytical modeling

### Gold Layer
- Business-ready analytical layer
- Data is modeled using a **star schema**
- Fact and dimension tables are optimized for reporting and analytical queries

---

## 📦 Data Sources

- ERP and CRM datasets provided as CSV files
- Data represents sales-related information used for analytical reporting
- Only the most recent dataset is considered (no historization or SCD handling)

---

## 🔄 ETL Implementation

- Data is extracted from CSV files and loaded into staging (Bronze) tables
- Transformation logic is applied using SQL to clean and normalize data in the Silver layer
- Final analytical tables are populated in the Gold layer
- ETL logic is implemented using **SQL scripts** executed via SQL Server Management Studio

---

## 🧩 Data Modeling

- Designed **fact and dimension tables** to support analytical queries
- Applied star schema principles to improve query performance and readability
- Ensured clear relationships between dimensions and fact tables

---

## 📊 Analytics & Reporting

- Developed SQL queries to analyze:
  - Customer behavior
  - Product performance
  - Sales trends
- Queries are written with a focus on clarity and reusability
- Output metrics are intended to support high-level business decision-making

---

## 🛠️ Tech Stack & Tools

- **Database**: SQL Server Express  
- **Query & Management**: SQL Server Management Studio (SSMS)  
- **Version Control**: Git & GitHub  
- **Design & Diagrams**: Draw.io  

---

## 📁 Repository Structure

```text
├── datasets/          # Source CSV files
├── docs/              # Architecture diagrams and documentation
├── sql/
│   ├── bronze/        # Raw data ingestion scripts
│   ├── silver/        # Data cleansing and transformation scripts
│   └── gold/          # Analytical model scripts
└── README.md
