# 🎧 Spotify Data Pipeline using AWS

This project is an end-to-end serverless **ETL (Extract, Transform, Load)** pipeline that collects music data from the **Spotify API**, processes it using **AWS Lambda**, stores it in **Amazon S3**, and performs analytics using **AWS Glue** and **Amazon Athena**.

---

### Components Used

- **Spotify API** – Source of music-related data
- **Python** – Used for data extraction and transformation logic
- **Amazon CloudWatch** – Triggers the pipeline daily
- **AWS Lambda** – Handles data extraction and transformation
- **Amazon S3** – Stores raw and transformed data
- **S3 Triggers** – Invokes transformation on new data
- **AWS Glue** – Crawls transformed data and creates schema
- **Amazon Athena** – Performs SQL-based analysis on structured data

---

## ⚙️ Workflow Steps

1. **Extract**  
   - A Python-based Lambda function is triggered daily by CloudWatch to extract data from Spotify API and store it as raw JSON in S3.

2. **Transform**  
   - On object upload, another Lambda function is triggered to transform the raw data and save the cleaned version in a separate S3 bucket or folder.

3. **Load**  
   - AWS Glue Crawler infers schema from the transformed data and updates the Glue Data Catalog.
   - Amazon Athena is used to query and analyze the structured data.

---

## 🧪 Technologies Used

- AWS Lambda  
- Amazon S3  
- Amazon CloudWatch  
- AWS Glue  
- Amazon Athena  
- Python  
- Spotify Web API

---

## 🚀 How to Run

1. Clone the repository and configure AWS credentials.
2. Deploy the Lambda functions using AWS Console or SAM CLI.
3. Set up the CloudWatch trigger for daily execution.
4. Configure S3 triggers and Glue Crawlers.
5. Use Athena to run queries on your data.

---

## 📈 Use Cases

- Music trend analysis
- Artist and track popularity reports
- Integration into data dashboards

---

