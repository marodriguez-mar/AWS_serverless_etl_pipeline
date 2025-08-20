# Serverless ETL Pipeline on AWS (S3, Lambda, Glue, Athena)

# 📖 Project Overview
This project demonstrates how to build a **serverless ETL (Extract, Transform, Load) pipeline** on AWS.  
The pipeline processes **incoming JSON order data**, transforms it into a query-friendly format, and makes it available for analysis using **Amazon Athena**.  

This use case mirrors common real-world scenarios in **data analytics and data engineering**, where raw data needs to be cleaned, structured, and analyzed at scale.  

---

## 🏗️ Architecture

```mermaid
flowchart LR
    A[📂 S3 Incoming Orders Folder] -->|Trigger| B[🟦 AWS Lambda]
    B --> C[📂 S3 Staging Folder]
    C --> D[🗂️ AWS Glue Crawler & Database]
    D --> E[🔍 Athena ]
