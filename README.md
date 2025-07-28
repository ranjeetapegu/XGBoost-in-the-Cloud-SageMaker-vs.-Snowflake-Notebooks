
# XGBoost in the Cloud: SageMaker vs. Snowflake Notebooks

This project compares Amazon SageMaker Notebooks and Snowflake Notebooks for building and running a machine learning pipeline using the XGBoost algorithm.

The goal is to help data scientists understand the trade-offs between the two platforms in terms of setup, performance, cost, and developer experience — all using the same binary classification use case.

---

## Use Case: Churn Prediction
Customer loss can significantly impact a business’s bottom line. By detecting at-risk customers early, companies can proactively engage them with retention strategies. In this workshop, we'll explore how to use Snowflake’s machine learning (ML) capabilities to automate the identification of dissatisfied customers—commonly referred to as churn prediction

---

## Platforms Compared

### ✅ Amazon SageMaker Notebook
https://sagemaker-examples.readthedocs.io/en/latest/introduction_to_applying_machine_learning/xgboost_customer_churn/xgboost_customer_churn_outputs.html#Data

- Runs on managed EC2 infrastructure
- Uses S3 for data input/output
- Supports distributed training with `sagemaker.estimator.Estimator`
- Ideal for custom training jobs and real-time inference endpoints

### ✅ Snowflake Notebook
- Fully browser-based (no setup required)
- Uses in-database compute with Snowpark ML
- Training and inference happen inside Snowflake (no data movement)
- Easy integration with Snowflake ML Registry & Cortex LLMs

---

## 📦 Workflow Overview

| Step               | SageMaker                         | Snowflake                            |
|--------------------|-----------------------------------|--------------------------------------|
| Data Source        | S3                                | Snowflake Table                      |
| Preprocessing      | pandas                            | Snowpark DataFrame                   |
| Training           | XGBoost via Estimator             | XGBoost via Snowpark ML              |
| Inference          | Batch Transform / Endpoint        | `predict()` on DataFrame             |
| Model Registry     | Optional                          | Built-in                             |
| Deployment         | Real-time or batch endpoints      | Batch processing

---






