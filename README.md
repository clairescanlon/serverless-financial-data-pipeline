# Serverless Financial Data Pipeline
This project aims to create a fully serverless ETL pipeline on AWS for financial data management. It addresses current challenges in data quality and compliance while preparing for future scalability. The pipeline automates data ingestion, processing, and visualization.

**View the full project case study on my portfolio:** 
[How I Increased Data Management Efficiency by 50% with an AWS ETL Pipeline](https://claire-scanlon.com/aws-data-pipeline/)

## Data & Security
The data included in this repository is purely synthetic and for demonstration purposes only. It does not contain any real client, proprietary, or personally identifiable information (PII). 

## Languages Used
* Python
* SQL

## AWS Services
* Amazon S3: Landing zone for CSV uploads. Separate buckets for different data, versioning and SSE-KMS encryption
* Amazon Aurora Serverless (PostgreSQL): Relational data storage with RDS Data API for batch upserts and schema enforcement
* AWS Lambda: Lambda function for automated CSV parsing, data cleaning, transformation, batch loading, archiving and error handling
* AWS IAM: Execution roles with least-privilege policies 
* Amazon CloudWatch: Logs, metrics and custom dashboards for monitoring pipeline execution and performance
* AWS CloudTrail: Audit trail of API calls and data events for SOX/GDPR compliance
* AWS KMS: Customer managed key for environment variable decryption and S3/Aurora encryption
* AWS Secrets Manager: Secure storage and rotation of database credentials accessed by Lambda
* Amazon SQS: Dead-Letter Queue for failed event capture and retry
* AWS Config: Continuous configuration monitoring to ensure compliance drift detection
* Qlik Sense: Interactive analytics and visualization layer enabling users to explore, filter and generate real-time financial reports securely

## Features
* Data Pipelines
* ETL (Extract, Transform, Load)
* Scalable Data Architecture
* Financial Data Compliance
* Data Modeling
* Database Normalization
* Error Handling and Monitoring
* Automated Data Ingestion and Processing
* Metadata Management
* Relational Database
*  _Coming Soon_

## Code Samples
> [!NOTE]
> This is currently under construction. Check back again soon.
> If you need additional information, send me an email. 
* AWS Lambda Function - _Coming Soon_
* Data Validation and Transformation  - _Coming Soon_
* S3 File Upload Handling  - _Coming Soon_
* Database Code - _Coming Soon_
* Qlik Sense Script to Load Data  - _Coming Soon_

> [!CAUTION]
> © 2025 Claire Scanlon. All rights reserved.
Unauthorized copying, distribution, or derivative use prohibited.
