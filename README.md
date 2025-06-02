# AWS S3 + Lambda CSV Aggregator
A serverless AWS project that reads a CSV file uploaded to S3, parses and aggregates salary data by country, and writes the results back to the same bucket. Built using **AWS Lambda**, **Amazon S3**, and **Python (boto3)**.

---

## 📌 Use Case

Every time a `.csv` file is uploaded to a specified S3 bucket, a Lambda function is triggered to:
- Read the file content
- Parse employee records (ID, name, salary, country)
- Calculate total salary spend for India and the USA
- Write the result back to the same S3 bucket as an output file

---

## 🧱 Tech Stack

- **AWS Lambda**
- **Amazon S3**
- **IAM (Identity and Access Management)**
- **Python**
- **Boto3**

---

## 🔁 Architecture

+------------+ +----------+ +-------------+ +----------------+
| Upload CSV | ---> | S3 | ---> | Lambda | ---> | S3 (Result)|
+------------+ +----------+ +-------------+ +----------------+
