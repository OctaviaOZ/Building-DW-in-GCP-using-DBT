# Data Engineering Project

## Overview
This project focuses on designing a data warehouse and implementing an ETL/ELT pipeline to process e-commerce data efficiently. The solution is built on Google BigQuery and follows best practices for data modeling, quality assurance, and security.

## Key Components
### 1. Schema Design
A well-structured schema was designed to store and process e-commerce data, enabling efficient analytics. Key considerations included:
- Normalized schema with tables for orders, customers, addresses, shipments, and billing.
- Optimized for common queries such as revenue tracking, customer activity analysis, and shipping performance monitoring.
- Ensuring data correctness and handling anomalies.
- Example SQL queries for analytics.

### 2. Data Pipeline & Quality Assurance
A data pipeline was implemented to extract, transform, and load (ETL) data into BigQuery. Key elements include:
- Extraction from the ERP system via API (push and pull methods).
- Loading into BigQuery with appropriate transformations.
- Ensuring data accuracy using validation checks and anomaly detection.
- Security measures to protect sensitive data.

### 3. ELT Implementation with dbt
As the data warehouse grew, an ELT approach using dbt (Data Build Tool) was adopted to enhance scalability and maintainability. Key enhancements:
- A **Raw Data Project** storing unprocessed data.
- A **Production Project** containing transformed data for analytics and visualization.
- A **Sandbox Project** for testing and experimentation.
- dbt models to transform raw data into structured datasets.

### 4. Security & Access Control
IAM roles were assigned to enforce access control:
- Engineers have full access to raw data.
- Analysts and visualization tools can access only production data.
- Developers can use the sandbox environment without impacting production.

## Conclusion
This project provides a scalable and secure data architecture for e-commerce analytics, leveraging BigQuery and dbt to optimize data transformation and access management.

## Extract from IPython Notebook to HTML
```bash
```python -m jupyter nbconvert dw_in_gcp_dbt.ipynb --to html 