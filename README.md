# Securities Pricing Data Pipeline

An end-to-end Securities Pricing Data Pipeline built using Docker, Apache Airflow, Snowflake, Python, SQL, and AWS.

## 📌 Project Overview

This project focuses on building an automated End-of-Day (EOD) pricing analytics pipeline for securities data.

The pipeline demonstrates how data can be ingested, transformed, validated, stored, and prepared for analytics using modern data engineering tools.

## 🏗️ Technologies Used

- **Apache Airflow** – Workflow orchestration
- **Snowflake** – Cloud data warehouse and data modeling
- **Docker** – Containerization and environment setup
- **Python** – Data processing and automation
- **SQL** – Data transformation and analysis
- **AWS** – Cloud-based data workflows

## 🔄 Data Pipeline

The overall workflow follows:

**Data Ingestion → Data Transformation → Data Validation → Data Storage → Analytics**

The pipeline includes automated EOD pricing workflows and processes securities pricing data for analytical use.

## 🗂️ Data Warehouse Structure

The Snowflake data warehouse is organized into different layers, including:

- **RAW** – Raw ingested pricing data
- **CORE** – Cleaned and processed data
- **DM_DIM** – Dimension tables such as security and date
- **DM_FACT** – Fact tables containing daily pricing information
- **SA** – Business-ready analytical views

## ⚙️ Key Components

### Apache Airflow

Used to orchestrate and automate the data pipeline workflows.

### Snowflake

Used for data storage, transformation, data modeling, and analytical queries.

### Docker

Used to create a consistent development environment and run the Airflow components.

### Python & SQL

Used for data processing, transformations, validation, and analytical queries.

## 📊 EOD Pricing Analytics

The pipeline processes daily security pricing information such as:

- Security ID
- Symbol
- Trade Date
- Open Price
- High Price
- Low Price
- Close Price
- Trading Volume

The processed data is made available through analytical views for downstream consumption.

## 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

- Building an end-to-end data pipeline
- Workflow orchestration using Apache Airflow
- Data warehousing using Snowflake
- SQL-based data transformation
- Docker-based development environments
- Data modeling using fact and dimension tables
- Automated EOD data processing
- Building business-ready analytical views

## 👨‍💻 Author

**Ankolla Sai Pranav**

Aspiring Data Engineer


securities-pricing-data-pipeline/
│
├── README.md
│
├── 1_historical_load/
│   ├── extract_historical_data.py
│   ├── init_snowflake_objects.sql
│   ├── load_transform_historical_data.sql
│   └── polygon_eod_grouped_20251017_20251024.csv
│
├── 2_daily_load/
│   ├── dags/
│   │   ├── get_securities_data.py
│   │   ├── lib/
│   │   │   ├── eod_data_downloader.py
│   │   │   └── slack_utils.py
│   │   ├── sql/
│   │   │   ├── 1. copy_to_raw.sql
│   │   │   ├── 2. check_loaded.sql
│   │   │   ├── 3. premerge_metrics.sql
│   │   │   ├── 4. merge_core.sql
│   │   │   ├── 5. merge_dim_security.sql
│   │   │   ├── 6. dm_dim_date.sql
│   │   │   ├── 7. merge_fact_daily_price.sql
│   │   │   └── 8. postmerge_metrics.sql
│   │   ├── test_aws_conn.py
│   │   ├── test_slack_conn.py
│   │   └── test_snowflake_conn.py
│   ├── load_daily_eod_prices.sql
│   └── requirements.txt
│
├── 3_reject_table_scenario/
│   ├── 3. premerge_metrics.sql
│   ├── 4. merge_core.sql
│   ├── eod_data_downloader.py
│   ├── get_securities_data.py
│   └── reject_table_creation.sql
│
├── 4_dashboarding/
│   ├── securities_market_insights.pbix
│   ├── securities_pricing_views_meta_data.csv
│   ├── security_attributes.csv
│   └── sec_pricing_views.sql
│
└── resources/
    ├── problem_statement.pdf
    ├── project_architecture.png
    ├── RBF_EOD_Pricing_Analytics_SOW.pdf
    ├── securities_market_report1.jpg
    └── securities_market_report2.jpg

