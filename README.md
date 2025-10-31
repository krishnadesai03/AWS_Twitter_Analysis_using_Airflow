# 🐦 AWS Twitter Data Analytics Pipeline

This project demonstrates how to build a **scalable ETL pipeline** for extracting, transforming, and loading Twitter data into an **AWS S3 Data Lake** using **Python**, **Apache Airflow**, and multiple **AWS services**.  
It automates the process of fetching tweets via the Twitter API, transforming the data using `pandas`, and orchestrating the entire pipeline on **Airflow deployed on an EC2 instance**.

---

## 🚀 Project Overview

### **Objective**
Build an end-to-end data engineering pipeline that:
- Extracts tweets from the Twitter API using `tweepy`.
- Transforms and cleans data using Python and `pandas`.
- Automates workflow orchestration via **Apache Airflow**.
- Stores the processed data in **AWS S3**.
- Optionally performs analytics using **AWS Athena**, **QuickSight**, or **Power BI**.

---

## 🧱 Architecture

The high-level architecture of the project is as follows:

1. **Data Extraction**
   - Twitter API accessed via Python using `tweepy`.
   - API keys and tokens generated from the Twitter Developer Portal.
2. **Data Transformation**
   - Tweets are parsed and converted into structured `pandas` DataFrames.
   - Cleaned data exported as `.csv`.
3. **Workflow Orchestration**
   - Apache Airflow manages tasks using DAGs:
     - `extract_twitter_data`
     - `transform_data`
     - `load_to_s3`
4. **Data Storage**
   - Transformed data is uploaded to an **AWS S3 bucket**.
   - IAM roles and permissions allow EC2-S3 communication.
5. **Analytics (Optional)**
   - Data in S3 can be queried using **AWS Athena** or visualized in **QuickSight**.

---

## 🧩 AWS Services Used

| Service | Purpose |
|----------|----------|
| **Amazon EC2** | Hosts Apache Airflow for pipeline orchestration. |
| **Amazon S3** | Stores raw, transformed, and output data. |
| **AWS IAM** | Manages access between EC2 and S3. |
| **AWS CloudWatch** | (Optional) For monitoring Airflow logs and metrics. |
| **AWS Athena / QuickSight** | For running queries or creating visualizations. |

---

## ⚙️ Tech Stack

- **Language:** Python 3.8+
- **Packages:** `tweepy`, `pandas`, `s3fs`, `boto3`
- **Platform:** AWS EC2 (Ubuntu)
- **Workflow Tool:** Apache Airflow
- **Storage:** AWS S3
- **Version Control:** Git / GitHub

---



