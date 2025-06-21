# Telco Customer Churn Prediction - GCP Vertex AI Project

This project demonstrates an end-to-end **churn prediction pipeline** built entirely on **Google Cloud Platform (GCP)**. It uses **Dataflow, BigQuery, and Vertex AI** to train and deploy a machine learning model that predicts whether a customer is likely to churn.

# Objective

Predict customer churn using an AutoML classification model trained on Telco Customer Churn dataset.

## Tools & Technologies

- **Google Cloud Storage (GCS)** – store input CSV data
- **Apache Beam (Dataflow)** – transform and load data
- **BigQuery** – data warehouse for analytics and training
- **Vertex AI (AutoML)** – model training and deployment
- **Cloud Function (optional)** – for API endpoint

## Pipeline Flow

```text
1. Upload CSV to Cloud Storage
2. Run Dataflow job to clean & load data into BigQuery
3. Create Vertex AI Dataset from BigQuery table
4. Train AutoML Tabular Classification Model
5. Deploy Model to Endpoint (REST API)
6. Use model to predict churn for new customers
