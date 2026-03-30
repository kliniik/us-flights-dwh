# US Flights Data Warehouse & Analytics Pipeline

## Project Overview
This project presents an end-to-end Data Warehouse solution built in Databricks to analyze US flight operations, delays, and punctuality. The main goal was to design a scalable data pipeline capable of processing aviation data and extracting business-friendly insights regarding network efficiency and delay patterns.

## Tech Stack & Tools
**Environment::** Databricks  
**Languages:** Python (PySpark), SQL  
**Architecture:** Medallion Architecture (Bronze, Silver, Gold)  
**Data Modeling:** Dimensional modeling with Slowly Changing Dimensions (SCD) support  

## Project Structure
The repository is organized to reflect the stages of the data pipeline:
- **0-init/:** Initialization scripts. Includes data modeling (ERD.png), database setup, and table creation.
- **1-bronze/:** Ingestion layer. Raw data extraction for airlines, airports, and flights.
- **2-silver/:** Cleansed and conformed data. Validation, deduplication, and handling of missing values.
- **3-gold/:** Business-level aggregates. Creation of fact and aggregation tables optimized for analytical queries and KPI tracking.
- **4-visualizations/:** Exploratory Data Analysis (EDA) and business insights.
- **5-tests/:** Integration testing to verify data integrity across the pipeline.

## Data Architecture (Medallion)
The pipeline strictly follows the Medallion architecture to ensure data quality and query performance:
- **Bronze Layer:** Stores raw data in its original format. Acts as a historical archive.
- **Silver Layer:** Cleansed and structured data. Here, relationships are established, and data is standardized for further processing.
- **Gold Layer:** Highly refined data aggregated for business reporting. Features a dimensional model tailored for specific KPIs (e.g., daily delay metrics).

## Key Insights & Visualizations
Note: Interactive Databricks visualizations have been exported as static images for GitHub compatibility.

**Overall Operational Status**  
Shows the proportion of delayed, cancelled, and diverted flights.

**Daily Delay Trends**  
Tracks the fluctuation of delays on a daily basis to identify operational bottlenecks.

**Root Causes of Delays**  
Breakdown of primary reasons causing disruptions in the flight network.

**Airline Performance Comparison (August)**  
Highlights the most and least punctual airlines during the analyzed period.

## Quality Assurance
To ensure the reliability of the ETL processes, the 5-tests directory contains integration tests (5_integration_test.ipynb) verifying that data flows correctly from the Bronze to the Gold layer without loss or unexpected duplication.

---
Note: The internal documentation and comments within the Jupyter notebooks are written in Polish.
