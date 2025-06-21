# 🔗 AWS S3 + IAM + AWS Glue Integration

This guide walks through the step-by-step process of setting up a pipeline to read data from Amazon S3, use AWS Glue to catalog and query the data, and manage access with IAM roles and policies.

---

## 🧰 Prerequisites

- AWS Account
- IAM Permissions to access:
  - S3
  - IAM
  - AWS Glue
- Sample CSV or JSON file to upload to S3

---

## 📁 Step 1: Create an S3 Bucket and Upload Data

1. Go to **S3 Console** → `Create bucket`.
2. Name it something like `my-data-bucket`.
3. Disable public access.
4. Click `Create`.
5. Open the bucket → `Upload` a sample data file (e.g., `sales.csv`).

---

## 👤 Step 2: Create an IAM Role for AWS Glue

1. Navigate to **IAM Console** → `Roles` → `Create role`.
2. Choose:
   - **Trusted entity**: AWS service
   - **Use case**: Glue
3. Attach the following policies:
   - `AmazonS3FullAccess`
   - `AWSGlueServiceRole`
4. Name the role: `AWSGlueServiceRole-MyProject`.

---

## 🧪 Step 3: Create a Glue Crawler

1. Go to **AWS Glue Console** → `Crawlers` → `Add crawler`.
2. Set crawler name: `my-s3-crawler`.
3. Choose **Data stores** → `S3` → Point to your bucket path.
4. Use the IAM role created earlier.
5. Output: Create or choose a Glue Database (e.g., `s3_data_db`).
6. Run the crawler to catalog the data.

---

## 🔍 Step 4: Explore Data Using Glue Data Catalog and Athena

1. After the crawler finishes, a table will appear in the Glue Data Catalog.
2. Navigate to **Amazon Athena**:
   - Set query result location in S3.
   - Run SQL queries like:
     ```sql
     SELECT * FROM s3_data_db.sales LIMIT 10;
     ```

---

## 🛡️ Step 5: Secure Your Pipeline (Optional)

- Implement IAM policies to restrict access.
- Enable logging in S3.
- Add encryption using S3 bucket policies and Glue encryption settings.

---

## ✅ Outcome

You can now:
- Automate schema detection using Glue Crawler
- Use Athena to query S3 data using SQL
- Build ETL pipelines or analytics workflows

---

## 📌 Notes

- Ensure the data in S3 is in a format Glue supports (CSV, JSON, Parquet, etc.).
- IAM roles must have trust relationship for Glue.



