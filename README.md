# Customer Churn Analytics, Prediction & Retention Strategy

An end-to-end data analytics and machine learning project using the **IBM Telco Customer Churn dataset** to analyse customer behaviour, identify churn patterns, predict customer churn and derive actionable business insights.

## Project Overview

Customer churn is an important challenge for subscription-based businesses. Understanding why customers leave and identifying customers who are likely to churn can help businesses develop effective retention strategies.

This project combines exploratory data analysis, SQL-based business analysis and machine learning to study customer churn, identify influential factors and segment customers according to their predicted churn risk.

## Dataset

**Source:** IBM Telco Customer Churn Dataset

- Total records: 7,043 customers
- Target variable: `Churn`
- Features include customer demographics, subscribed services, contract details, tenure, payment methods and billing information.

## Tech Stack

- **Programming:** Python
- **Data Manipulation:** Pandas, NumPy
- **Database:** SQLite, SQL
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Environment:** Google Colab / Jupyter Notebook

## Project Workflow

### 1. Data Loading & Preprocessing
- Loaded and inspected the customer churn dataset.
- Examined data types, summary statistics and missing values.
- Converted `TotalCharges` into numeric format.
- Created a binary churn target variable (`Churn_Flag`).

### 2. Exploratory Data Analysis (EDA)
Analysed customer churn across important attributes, including:
- Contract type
- Customer tenure
- Monthly charges
- Customer and service segments

Used data visualizations to understand churn distribution and identify patterns in customer behaviour.

### 3. SQL-Based Business Analysis
Used SQLite to perform structured queries and analyse:
- Churn across different contract types.
- Churn patterns by payment method.
- Churn across combinations of contract type and internet service.

### 4. Customer Prioritization & Business Insights
Identified customer segments with higher observed churn and summarized findings to support retention planning.

### 5. Business Recommendations
Developed recommendations based on the analysis, focusing on:
- Improving early customer retention.
- Targeting high-churn contract segments.
- Evaluating pricing and service quality.
- Implementing data-driven retention experiments.

### 6. Predictive Modelling

Developed two machine learning classification models:

- Logistic Regression
- Random Forest Classifier

The dataset was split into training and testing sets, with preprocessing pipelines for numerical and categorical features.

**Model evaluation metrics:**

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 80.55% | 76.58% |
| Precision | 65.72% | 54.45% |
| Recall | 55.88% | 71.93% |
| F1-Score | 60.40% | 61.98% |
| ROC-AUC | 84.21% | 83.92% |

Models were evaluated using classification metrics, confusion matrices and ROC curves.

### 7. Feature Interpretation
- Extracted Logistic Regression coefficients to understand feature associations with churn.
- Analysed Random Forest feature importance.
- Identified influential factors such as tenure, contract type, total charges and monthly charges.

### 8. Threshold Optimization & Model Selection
Compared classification thresholds using a validation split and evaluated model performance to select the final model.

### 9. Customer Churn Risk Segmentation
- Generated churn probabilities for customers.
- Assigned customers to Low, Medium and High churn-risk categories.
- Prepared customer-level predictions for prioritization and retention analysis.

### 10. Model Export & Output Generation
Saved the selected model and supporting metadata, including:
- Trained model
- Selected prediction threshold
- Feature information
- Model evaluation results

Exported customer churn predictions and final model evaluation results as CSV files.

## Key Findings

- Month-to-month contracts are associated with higher observed churn.
- Customers with shorter tenure exhibit higher churn.
- Monthly charges and contract type are important variables in understanding churn patterns.
- Logistic Regression achieved higher accuracy and ROC-AUC, while Random Forest achieved higher recall and F1-score in the reported evaluation.

## Repository Structure

```text
Customer-Churn-Analytics/
│
├── customer_churn_analytics_refined.ipynb
└── README.md
```

The notebook contains the complete workflow, including analysis, SQL queries, model development, evaluation, risk segmentation and output generation.

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR-USERNAME/customer-churn-analytics.git
   ```

2. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn joblib
   ```

3. Open the notebook in Google Colab or Jupyter Notebook.

4. Upload the IBM Telco Customer Churn CSV dataset when prompted by the notebook.

5. Execute the cells sequentially to reproduce the analysis and generate the outputs.

## Future Scope

- Further experimentation with classification algorithms.
- Improvement of model performance through hyperparameter tuning.
- Refinement of customer risk segmentation and retention strategies.

---

**Project Domain:** Data Analytics | Machine Learning | Customer Retention
