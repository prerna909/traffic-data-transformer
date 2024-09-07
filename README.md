# Traffic Data Insights - Data Engineering Project

This project focuses on creating a data pipeline for traffic data using Azure and Databricks, transforming raw data into insightful visualizations in Power BI.

## Project Overview

The objective of this project is to process and analyze traffic data by ingesting, transforming, and loading data through different layers (bronze, silver, gold) in an Azure Databricks environment. The final data is then visualized using Power BI to generate meaningful insights.

## Tools and Technologies Used

- **Python**
- **SQL**
- **PySpark**
- **Azure Databricks**
- **Power BI**

## Key Steps

1. **Create Development Workspace and Catalog in Azure**
   - Set up the development environment in Azure.
   - Created a development catalog to organize and manage data assets.

2. **Set Up Azure Databricks Containers**
   - Created containers for data processing:
     - **Landing**
     - **Medallion**
     - **Checkpoints**
   - Within the Landing container:
     - Created folders: `raw_roads` and `raw_traffic` for initial data ingestion.

3. **Access Management and Storage Configuration**
   - Created an access connector for Azure.
   - Configured external locations for:
     - **Bronze**
     - **Silver**
     - **Gold**
     - **Checkpoints**
     - **Landing**
   - Configured storage credentials to securely manage data.

4. **Schema and Table Creation**
   - Inside the Dev Catalog:
     - Created schemas for the **Bronze**, **Silver**, and **Gold** layers.
   - Created tables `raw_traffic` and `raw_roads` within the Bronze schema.

5. **Data Ingestion and Processing**
   - Ingested raw traffic and roads data into the Bronze layer.
   - Performed data cleaning:
     - Removed duplicate rows.
     - Removed null values.
   - Added new columns:
     - Count of Electric Vehicles (EV).
     - Count of all motor vehicles.
   - Merged and transformed the data for the Silver layer.

6. **Transformation and Aggregation in Silver Layer**
   - Generated vehicle intensity data and added it to a new column.
   - Created a `load_time` column to track data loading times.
   - Transformed data for the Gold layer.

7. **Data Visualization in Power BI**
   - Leveraged the Gold layer data to create insightful visualizations in Power BI, providing meaningful traffic data insights.

## Project Insights

The project showcases how to effectively manage and process large datasets in a cloud environment, transforming raw data into actionable insights. The use of Azure Databricks for data engineering tasks ensures scalability and efficiency, while Power BI provides a powerful platform for data visualization.

This end-to-end pipeline enables real-time insights into traffic patterns, helping in decision-making processes for traffic management and urban planning.