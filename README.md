# Data_Modeling
This repository documents my learning journey and hands-on practice with core data engineering and analytics concepts. It covers data modeling fundamentals, OLTP vs OLAP systems, fact and dimension schema design, the Medallion Architecture, and Slowly Changing Dimensions (SCD Type-1 &amp; Type-2).

Here is a clean, professional, GitHub-ready **README description** for your learning summary on
**Data Modeling, OLTP/OLAP, Fact–Dimension Modeling, Medallion Architecture, and SCD Type-1 & Type-2.**

You can directly paste this into your repo.

---

# 📘 Data Modeling & ETL Concepts — Learning Summary

This repository documents my learning journey and hands-on practice with core data engineering and analytics concepts.
It covers data modeling fundamentals, OLTP vs OLAP systems, fact and dimension schema design, the Medallion Architecture, and Slowly Changing Dimensions (SCD Type-1 & Type-2).

---

## 🚀 What I Learned

### 1. Data Modeling

Data modeling is the process of designing the logical structure of data for efficient storage, retrieval, and analytics.
I learned how to:

Identify business entities and relationships
Apply normalization/denormalization based on use case
Build scalable schemas for reporting and analytics
Model data for both transactional and analytical workloads


### 2. OLTP vs OLAP

**OLTP (Online Transaction Processing)**

Used for day-to-day transactional systems
High volume reads/writes (INSERT/UPDATE/DELETE)
Optimized for speed and concurrency
Examples: Banking systems, e-commerce checkout, CRMs

**OLAP (Online Analytical Processing)**

Used for reporting and analytics
Large volume reads and aggregations
Optimized for queries, joins, aggregations
Supports dashboards and BI tools

I learned the differences, use cases, and how modeling changes based on the environment.


### 3. Fact & Dimension Tables (Star Schema)

**Dimension Tables**
* Contain descriptive, textual attributes (Who, What, Where, When)
* Examples: Product, Customer, Date, Region

**Fact Tables**
* Contain numeric, measurable business metrics
* Examples: Sales facts, Order facts, Inventory facts
* Include foreign keys to relevant dimensions

I learned how Fact and Dimension tables form a **Star Schema**, enabling fast analytical queries.


###  4. Medallion Architecture (Bronze → Silver → Gold)

A modern data lake/lakehouse pattern used in Databricks and cloud platforms.

| Layer      | Purpose                                                              |
| ---------- | -------------------------------------------------------------------- |
| **Bronze** | Raw, uncleaned data directly ingested from source systems            |
| **Silver** | Cleaned, standardized, deduplicated data with business logic applied |
| **Gold**   | Aggregated, analytics-ready data used for dashboards and reporting   |

I practiced creating tables across these layers and applying transformations in each stage.


### 5. SCD Type-1 & SCD Type-2 (Slowly Changing Dimensions)

**SCD Type-1**

* Overwrites old data with new data
* No history preserved
* Used when historical changes are not important

**SCD Type-2**

Maintains full history of changes
Adds new records with `StartDate`, `EndDate`, `InUse` flags
Previous record is marked inactive
Useful for tracking attribute changes over time (e.g., product category updates, customer address history)

I implemented SCD Type-2 using SQL `MERGE` statements and tested update scenarios.

