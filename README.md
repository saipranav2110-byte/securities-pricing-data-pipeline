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

