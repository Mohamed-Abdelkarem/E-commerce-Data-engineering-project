# E-Commerce Data Warehouse Project

This project focuses on building a comprehensive e-commerce data warehouse, demonstrating practical data engineering principles in data modeling, ETL, and database optimization. Raw transactional data has been transformed into a well-structured, efficient model designed for advanced analytical queries and insights across the data.

Using dimensional modeling and multiple fact tables, I’ve created a system that captures order, item, payment, and feedback details with flexibility for detailed analysis. This project highlights essential skills in data engineering, from managing complex joins, redundancy, and granularity to ensuring data integrity, query performance, and data consistency across a scalable schema.


## Dimensional Modeling: Strategic Importance
Dimensional modeling is a cornerstone of effective data warehousing. Structuring data into fact tables for transactional metrics and dimension tables for contextual attributes. This architecture streamlines data retrieval, supports sophisticated analytics, and optimizes performance for high-demand reporting environments.


## Dimensional Modeling: Implementation in This Project
In this project, I adopted a robust dimensional modeling approach, establishing fact tables (e.g., Fact_Order, Fact_Feedback) to encapsulate core transactional data, alongside dimension tables (e.g., Date, Seller, Product) that offer contextual depth for comprehensive analysis across time, location, and product categories.

This approach enables faster queries, scalable analysis, and user-friendly reporting, making the data warehouse efficient for uncovering insights and supporting business intelligence.

[Click to view the Evolution of the Dimensional Model Design](Dimensional Model Design Overview/README.md)

<img src="https://github.com/Mohamed-Abdelkarem/e-commerce-data-engineering-project-/blob/main/dimensional%20model.png" alt="dimensional model" width="400" height="450">

## Skills and Technologies:
•  **Microsoft SQL Server:** Used for database creation and management, SQL Server allows for efficient querying and data manipulation, supporting complex operations needed in data warehousing.

•  **ETL (Extract, Transform, Load):** Implemented ETL processes to clean, transform, and load data from CSV files into the warehouse, handling data anomalies, duplicates, and inconsistencies.

•  **Dimensional Modeling:** A database design technique optimized for data warehouses, allowing for efficient querying and reporting by organizing data into fact and dimension tables.

•  **SQL (Structured Query Language):** The primary language for interacting with the database, used to create, query, and manage tables and relationships within the data warehouse.

•  **Fact and Dimension Tables:** Core components of the data warehouse schema, where fact tables store measurable data, and dimension tables contain descriptive attributes, enabling organized data storage and efficient analytics.

•  **Data Cleaning:** Involved identifying and removing duplicates, resolving inconsistencies, and handling null values to ensure data quality and integrity.

•  **Surrogate Keys:** Used to uniquely identify rows in dimension tables, separate from natural keys, and allow for tracking changes over time, especially when dealing with historical data.

•  **Database Optimization:** Applied normalization and indexing techniques to improve query efficiency and storage management within the warehouse.

•  **Documentation:** Created detailed self-documentation on data models, transformations, and problem-solving approaches to make the project accessible and replicable for future users or reviewers.
