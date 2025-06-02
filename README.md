# AWS S3 + Lambda CSV Aggregator
A serverless AWS project that reads a CSV file uploaded to S3, parses and aggregates salary data by country, and writes the results back to the same bucket. Built using **AWS Lambda**, **Amazon S3**, and **Python (boto3)**.

---

## Use Case

Every time a `.csv` file is uploaded to a specified S3 bucket, a Lambda function is triggered to:
- Read the file content
- Parse employee records (ID, name, salary, country)
- Calculate total salary spend for India and the USA
- Write the result back to the same S3 bucket as an output file

---

## Tech Stack

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

## How to Deploy

- **Create an S3 bucket**

- **Upload your Lambda code**

- **Go to AWS Lambda Console**

- **Create a new function (Python runtime)**

- **Paste lambda_function.py or upload a .zip**

- **Set up S3 trigger**

- **Go to the Lambda function > Triggers > Add S3 trigger**

- **Choose the ObjectCreated event for your bucket**

- **Attach proper IAM Role**

- **Use the policy above to allow access to s3:GetObject, s3:PutObject, and s3:ListBucket**

- **Test by uploading a CSV**

- **View the logs or the result file in S3**
