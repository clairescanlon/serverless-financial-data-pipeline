# Serverless Financial Data Pipeline
Production-grade ETL pipeline for processing financial transactions in real-time. 

> [!NOTE]
> This project is currently under active development. Check back regularly for updates.

## Overview
ETL (Extract, Transform, Load) pipeline for processing financial transactions in real-time. The pipeline handles millions of transactions daily using AWS serverless services. The pipeline processes millions of transactions daily with minimal operational overhead.

## Architecture
```
┌─────────────────────────────┐
│ S3 Bucket │
│ (Financial Data Source) │
└──────────────┬──────────────┘
│
▼
┌──────────────────────────────────┐
│ AWS Lambda Function │
│ - Parse transactions │
│ - Validate schema │
│ - Enrich with metadata │
└──────────────┬───────────────────┘
│
▼
┌──────────────────────────────────┐
│ Amazon SQS Queue + DLQ │
│ - Message buffering │
│ - Error handling │
│ - Automatic retries │
└──────────────┬───────────────────┘
│
▼
┌──────────────────────────────────┐
│ Amazon Aurora PostgreSQL │
│ - Normalized schema │
│ - Optimized indexes │
│ - High availability │
└──────────────┬───────────────────┘
│
▼
┌──────────────────────────────────┐
│ CloudWatch Monitoring │
│ - Real-time dashboards │
│ - Cost tracking │
│ - Performance metrics │
└──────────────────────────────────┘
```

**Data Flow:**
1. Raw transaction files land in S3
2. Lambda function processes each transaction (sub-second latency)
3. Valid transactions go to SQS for database loading
4. Failed transactions go to Dead Letter Queue (DLQ) for review
5. Aurora database stores normalized data
6. CloudWatch tracks pipeline health and costs


## Key Features
* **Real-time processing**: Handles incoming transactions with sub-second latency
* **Automatic error handling**: Failed transactions move to DLQ for manual review, then retry
* **Data validation**: Schema validation at every stage prevents bad data from reaching the database
* **Cost optimization**: Serverless architecture reduces operational costs by 60-70% vs. traditional servers
* **Monitoring built-in**: CloudWatch dashboards show pipeline health, throughput, and costs in real-time
* **Production-ready**: Includes logging, error handling, and graceful failure modes

## Tech Stack
* Amazon S3
* AWS Lambda
* Amazon Aurora PostgreSQL
* QlikSense
* AWS CloudWatch
* AWS CloudTrail
* AWS Secrets Manager
* IAM
* Amazon SNS
* AWS Config
* AWS KMS 




## Core Tables
### Accounts Table
* Customer accounts

### Transactions Table
* Cash flows, trades, payments

### Positions Table
* Current holdings or exposures



## Project Structure </br>
### sql/ folder 
* All database‑related scripts.

### src/ folder 
* Actual code for the pipeline.

### docs/ folder 
* Project documentation for humans.

### architecture/ folder 
* High-level visuals and diagrams.

### tests/ folder 
* Scripts for testing and validation of logic.

### config/ folder
* Settings for different environments.

### template.yaml file 
* AWS “blueprint” describing infrastructure as code.

### README.md file 
* High-level overview for this project.

### .gitignore file 
* Prevents committing secrets and sensitive data.

> [!NOTE]
> This is currently under construction. Check back again soon.



## Data Handling & Confidentiality </br>
All data, schemas, and code logic in this repository are completely synthetic and redesigned.
* ✓ No real client, customer, or proprietary information included
* ✓ No personally identifiable information (PII)
* ✓ No real company or client names
* ✓ Database schemas completely redesigned and generic
* ✓ Business logic rewritten for educational purposes
* ✓ All data transformers use synthetic financial data patterns
 </br>

 ### Important Note on Code Reusability
This project demonstrates serverless data engineering patterns and AWS best practices. The implementation is intentionally generic and would not be useful for replicating the original system. Key differences:
* Database schema has been redesigned from scratch with generic table structures
* Transformation logic has been rewritten to showcase architectural patterns
* Validation rules are generic data quality checks, not business-specific
* Error handling follows standard AWS patterns, not original workflows
* Data models are completely different from original implementations

This project was originally developed for confidential client work. It has been redesigned and published as a public portfolio project to demonstrate expertise in AWS serverless architecture, ETL pipeline design, and data engineering patterns without disclosing any confidential client information.

## License & Usage

This project is **proprietary software** provided for portfolio demonstration purposes only.

**Permitted Uses:**
- View and study this code for personal learning
- Review during job interviews or technical evaluations
- Discuss in technical interviews with potential employers
- Fork and modify for personal, non-commercial projects

**NOT Permitted:**
- Commercial use of any kind
- Incorporation into products or services
- Redistribution or sharing with others
- Use by previous employers or their affiliates

See the `LICENSE` and `NOTICE.md` files for complete terms and restrictions.

> [!NOTE]
> This project is currently under active development. Check back regularly for updates.




