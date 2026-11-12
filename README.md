# Customer Churn Analytics, Prediction & Retention Strategy

An end-to-end data analytics and machine learning project using the **IBM Telco Customer Churn dataset** to analyse customer behaviour, identify churn patterns, predict customer churn and derive actionable business insights.

## Project Overview

Customer churn is a major challenge for subscription-based businesses. Understanding why customers leave and identifying customers who are likely to churn can help businesses develop effective retention strategies.

This project combines exploratory data analysis, SQL-based business analysis, machine learning and interactive data visualization to study customer churn, identify influential factors and prioritize customers based on their predicted churn risk.

## Project Objectives

- Analyse customer data to identify patterns and trends associated with churn.
- Perform data cleaning and exploratory data analysis.
- Use SQL queries to derive meaningful business insights.
- Build and evaluate machine learning models for churn prediction.
- Identify influential factors associated with customer churn.
- Segment customers according to their predicted churn risk.
- Develop data-driven customer retention recommendations.

## Dataset

**Source:** IBM Telco Customer Churn Dataset

- Total records: 7,043 customers
- Target variable: `Churn`
- Features include customer demographics, subscribed services, contract details, tenure, payment methods and billing information.

## Tech Stack

| Category | Tools |
|---|---|
| Programming | Python |
| Data Manipulation | Pandas, NumPy |
| Database & Queries | SQLite, SQL |
| Data Visualization | Matplotlib, Seaborn, Power BI |
| Machine Learning | Scikit-learn |
| Development Environment | Google Colab / Jupyter Notebook |

## Project Workflow

### 1. Data Cleaning & Preprocessing
- Inspected dataset structure, data types and missing values.
- Handled inconsistent and missing values.
- Converted `TotalCharges` into numeric format.
- Prepared the dataset for analysis and machine learning.

### 2. Exploratory Data Analysis (EDA)

Analysed customer churn across important attributes, including:
- Contract type
- Customer tenure
- Monthly charges
- Payment methods
- Internet and subscribed services

Used visualizations to understand churn distribution and identify patterns in customer behaviour.

### 3. SQL-Based Business Analysis

Used SQLite and SQL queries to explore customer behaviour and derive business insights, including:
- Churn across different contract types.
- Churn patterns by payment method.
- Churn across combinations of contract type and internet service.

### 4. Customer Analysis & Business Insights

Identified customer segments with higher observed churn and examined the factors associated with customer attrition to support retention planning.

### 5. Machine Learning & Churn Prediction

Developed and evaluated two classification models:

- Logistic Regression
- Random Forest Classifier

**Model Performance**

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 80.55% | 76.58% |
| Precision | 65.72% | 54.45% |
| Recall | 55.88% | 71.93% |
| F1-Score | 60.40% | 61.98% |
| ROC-AUC | 84.21% | 83.92% |

Models were evaluated using multiple classification metrics, confusion matrices and ROC curves.

### 6. Feature Importance & Interpretation

Analysed model coefficients and feature importance to understand factors associated with customer churn.

Important features identified by the Random Forest model included:
- Customer tenure
- Month-to-month contracts
- Total charges
- Monthly charges
- Two-year contracts

### 7. Threshold Optimization & Model Selection

Compared classification thresholds using a validation split and evaluated model performance to select the final model and prediction threshold.

### 8. Customer Churn Risk Segmentation

- Generated churn probabilities for customers.
- Assigned customers to Low, Medium and High churn-risk categories.
- Prepared customer-level predictions to support prioritization and targeted retention efforts.

### 9. Power BI Dashboard

Developed an interactive Power BI dashboard to present customer churn insights and support data-driven decision-making.

The dashboard complements the analytical and predictive workflow by providing a visual interface for exploring customer churn patterns.

### 10. Model Export & Output Generation

Saved the selected model and supporting metadata, including:
- Trained model
- Selected prediction threshold
- Feature information
- Model evaluation results

Exported customer churn predictions and model evaluation results as CSV files.

## Key Findings

- Month-to-month contracts are associated with higher observed churn.
- Customers with shorter tenure exhibit higher churn.
- Monthly charges and contract type are important variables in understanding churn patterns.
- Logistic Regression achieved higher accuracy and ROC-AUC.
- Random Forest achieved higher recall and F1-score in the reported evaluation.

## Business Recommendations

Based on the analysis, potential retention strategies include:

- Prioritizing high-risk customers for proactive engagement.
- Encouraging suitable long-term contract options.
- Improving early-stage customer retention.
- Evaluating pricing and service quality.
- Designing targeted retention initiatives based on customer risk.

## Repository Structure

```text
Customer-Churn-Analytics/
│
├── README.md
├── Telco-Customer-Churn.csv
├── customer_churn_analytics_refined.ipynb
└── Customer_Churn_Analytics_Retention_Dashboard.pbix
```

## How to Run the Project

1. Clone the repository:

   ```bash
   git clone https://github.com/Jyoti-Shikha/Customer-Churn-Analytics.git
   ```

2. Navigate to the project directory:

   ```bash
   cd Customer-Churn-Analytics
   ```

3. Install the required dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn joblib
   ```

4. Open the Jupyter Notebook in Google Colab or Jupyter Notebook.

5. Ensure the dataset CSV is available in the notebook's working directory.

6. Execute the notebook cells sequentially to reproduce the analysis and generate the outputs.

**Power BI Dashboard:** The `.pbix` file is included in the repository and can be opened using Power BI Desktop. The published dashboard can also be accessed through the link above.

## Future Scope

- Experiment with additional machine learning algorithms.
- Improve model performance through further hyperparameter tuning.
- Refine customer risk segmentation.
- Explore additional customer retention strategies.

---

**Project Domain:** Data Analytics | Machine Learning | Business Intelligence | Customer Retention
