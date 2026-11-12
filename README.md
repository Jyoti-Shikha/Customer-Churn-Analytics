# Customer Churn Analytics, Prediction & Retention Strategy

An end-to-end **Data Analytics, Machine Learning and Business Intelligence** project using the IBM Telco Customer Churn dataset to analyse customer behaviour, identify churn patterns, predict customer churn and develop data-driven retention strategies.

The project combines **Python-based Exploratory Data Analysis (EDA), SQL, predictive modelling and a two-page interactive Power BI dashboard** to connect customer insights with business decisions.

## Project Overview

Customer churn is a major challenge for subscription-based businesses. Understanding why customers leave and identifying customers who are likely to churn can help businesses design more effective retention strategies.

This project follows an end-to-end analytical workflow, from understanding customer behaviour and extracting business insights to developing machine learning models, classifying customers by churn risk and presenting the results through Power BI.

## Project Objectives

- Analyse customer data to identify patterns associated with churn.
- Perform data cleaning and exploratory data analysis.
- Use SQL queries to extract meaningful business insights.
- Build and evaluate machine learning models for churn prediction.
- Identify influential features associated with customer churn.
- Segment customers based on predicted churn risk.
- Develop actionable customer retention recommendations.
- Build an interactive Power BI dashboard for descriptive and predictive analytics.

## Dataset

**Source:** IBM Telco Customer Churn Dataset

- **Total Customers:** 7,043
- **Target Variable:** `Churn`
- **Features:** Customer demographics, subscribed services, contract type, tenure, payment methods and billing information.

## Tech Stack

| Category | Tools |
|---|---|
| Programming | Python |
| Data Analysis | Pandas, NumPy |
| SQL Analysis | SQLite, SQL |
| Visualization | Matplotlib, Seaborn, Power BI |
| Machine Learning | Scikit-learn |
| Development | Google Colab / Jupyter Notebook |
| Business Intelligence | Microsoft Power BI |

## Project Workflow

### 1. Data Cleaning & Preprocessing

- Inspected dataset structure, data types and missing values.
- Handled inconsistent and missing values.
- Converted `TotalCharges` to numeric format.
- Prepared the dataset for exploratory analysis and predictive modelling.

### 2. Exploratory Data Analysis (EDA)

Conducted customer-level exploratory analysis using Python and Pandas to investigate the relationships between churn and key customer attributes.

Analysed churn across:

- Contract types
- Customer tenure
- Monthly charges
- Payment methods
- Internet services
- Subscribed services

**Key analytical findings:**

- Month-to-month customers had an observed churn rate of **42.71%**, compared with **11.27%** for one-year and **2.83%** for two-year contracts.
- Customers in their first 12 months had a churn rate of **47.44%**.
- Customers using electronic checks had an observed churn rate of **45.29%**.
- Fiber-optic internet customers showed a churn rate of **41.89%**.

These findings helped identify higher-churn customer segments and informed the subsequent business analysis.

### 3. SQL-Based Business Analysis

Used SQLite to perform business-oriented analysis of customer churn.

SQL queries were developed to investigate:

- Churn distribution across contract types.
- Customer tenure and churn relationships.
- Churn rates across payment methods.
- Churn patterns by internet service type.
- Customer segmentation based on multiple attributes.

The SQL analysis complemented Python-based EDA by validating churn patterns and translating the results into business-relevant insights.

### 4. Customer Analysis & Retention Insights

Combined EDA and SQL findings to identify customer segments that may require greater attention.

The analysis highlighted the importance of:

- Early customer engagement.
- Month-to-month contract retention.
- Payment-method-based customer segmentation.
- Identifying customers with multiple churn-associated characteristics.

These insights were used to formulate practical retention recommendations.

### 5. Machine Learning & Churn Prediction

Developed and evaluated two classification models:

- Logistic Regression
- Random Forest Classifier

**Initial Model Comparison**

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 80.55% | 76.58% |
| Precision | 65.72% | 54.45% |
| Recall | 55.88% | 71.93% |
| F1-Score | 60.40% | 61.98% |
| ROC-AUC | 84.21% | 83.92% |

Models were evaluated using classification metrics, confusion matrices and ROC curves.

### 6. Feature Importance & Interpretation

Analysed model coefficients and feature importance to understand the variables associated with customer churn.

Important features identified included:

- Customer tenure
- Month-to-month contracts
- Total charges
- Monthly charges
- Two-year contracts

### 7. Threshold Optimization & Final Model Selection

Compared classification thresholds and selected the final Logistic Regression model with a prediction threshold of **0.35**.

**Final Model Performance on Held-Out Test Data**

| Metric | Result |
|---|---:|
| Accuracy | 76.44% |
| Recall | 70.59% |
| ROC-AUC | 0.8421 |

The adjusted threshold was used to improve the model's ability to identify customers likely to churn.

### 8. Customer Churn Risk Segmentation

Generated model-based churn probabilities and categorized customers into three risk groups.

| Risk Category | Customers |
|---|---:|
| Low Risk | 4,371 |
| Medium Risk | 1,633 |
| High Risk | 1,039 |
| **Total** | **7,043** |

These risk categories support the prioritization of customers for potential retention initiatives.

The segmentation was generated across the full customer dataset, whereas the final model performance metrics were evaluated on held-out test data.

### 9. Interactive Power BI Dashboard

Developed a **two-page Power BI dashboard** combining descriptive customer analytics with machine learning predictions.

#### Page 1 — Customer Churn & Retention Overview

Designed to provide a business-level understanding of customer churn.

**Key Performance Indicators:**

- Total Customers: **7,043**
- Churned Customers: **1,869**
- Churn Rate: **26.54%**
- Retention Rate: **73.46%**

**Dashboard Features:**

- Contract-wise churn analysis
- Internet-service-wise churn comparison
- Payment-method-wise churn patterns
- Tenure-based customer segmentation
- Interactive slicers for contract type, internet service and payment method

#### Page 2 — Predictive Churn & Risk Analysis

Developed to visualize machine learning predictions and model performance.

**Dashboard Features:**

- Customer distribution by churn risk
- Predicted churn probability distribution
- Model Recall KPI: **70.59%**
- Model ROC-AUC KPI: **0.8421**
- Customer counts across Low, Medium and High risk categories

The dashboard integrates analytical findings and model outputs into a visual interface for exploring customer behaviour and churn risk.

**Dashboard Files:**

- `Customer_Churn_Analytics_Retention_Dashboard.pbix` — Interactive Power BI report
- `Customer_Churn_Analytics_Report.pdf` — Two-page dashboard preview

The interactive `.pbix` report can be explored using Microsoft Power BI Desktop.

### 10. Model Export & Output Generation

Saved model artifacts and supporting information, including:

- Trained model
- Selected classification threshold
- Feature information
- Model evaluation results
- Customer-level churn predictions

Exported predictions and evaluation results as CSV files for integration with Power BI.

## Key Findings

- Month-to-month customers showed substantially higher churn than customers on longer contracts.
- Customers with shorter tenure were more likely to churn.
- Electronic check users showed comparatively higher observed churn.
- Fiber-optic internet customers exhibited relatively high churn.
- Logistic Regression achieved higher accuracy and ROC-AUC in the initial model comparison.
- Random Forest achieved higher recall and F1-score in the initial comparison.
- Threshold adjustment improved the selected Logistic Regression model's recall.
- Risk-based customer segmentation provides a way to prioritize customer engagement efforts.

## Business Recommendations

Based on the analysis, potential retention strategies include:

1. **Prioritize high-risk customers:** Focus proactive retention efforts on customers with higher predicted churn probabilities.

2. **Improve early-stage retention:** Strengthen onboarding and engagement for customers in their first year.

3. **Encourage longer-term contracts:** Explore suitable incentives for customers considering longer commitments.

4. **Investigate payment-related churn:** Examine the experiences of customers using payment methods associated with higher observed churn.

5. **Review service and pricing concerns:** Further investigate the higher churn observed among certain internet-service segments.

6. **Use predictive insights for targeting:** Combine customer segmentation with predicted churn probabilities to plan and evaluate retention campaigns.

These are proposed strategies derived from observed patterns, rather than experimentally validated interventions.

## Project Contributors & Responsibilities

This project was completed collaboratively, with responsibilities distributed across data analytics, predictive modelling and business intelligence.

### Lohitaksha Guha — Data Analytics, SQL & Power BI

- Performed exploratory data analysis using Python and Pandas.
- Analysed churn patterns across customer demographics, contracts, tenure, payments and subscribed services.
- Developed SQL queries using SQLite for customer segmentation and business analysis.
- Interpreted analytical findings and developed customer retention recommendations.
- Designed and developed the complete **two-page interactive Power BI dashboard**.
- Integrated machine learning prediction outputs and evaluation metrics into Power BI.
- Developed visualizations of customer churn, retention KPIs, risk distribution and prediction probabilities.

### Jyoti Shikha — Machine Learning & Predictive Modelling

- Developed the machine learning pipeline using Scikit-learn.
- Implemented Logistic Regression and Random Forest classifiers.
- Performed model evaluation and comparison.
- Analysed feature importance and model interpretation.
- Conducted threshold optimization and final model selection.
- Generated customer-level churn predictions, risk classifications and model evaluation outputs.

Together, these contributions form an end-to-end analytical workflow connecting business analysis, predictive modelling and dashboard reporting.

## Repository Structure

```text
Customer-Churn-Analytics/
│
├── README.md
├── Telco-Customer-Churn.csv
├── customer_churn_analytics_refined.ipynb
├── Customer_Churn_Analytics_Retention_Dashboard.pbix
└── Customer_Churn_Analytics_Report.pdf
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

6. Execute the notebook cells sequentially to reproduce the analysis and generate the required outputs.

7. Open the `.pbix` file using Microsoft Power BI Desktop to explore the interactive dashboard.

**Note:** The PDF provides a static preview of the dashboard, while the `.pbix` file contains the interactive report.

## Future Scope

- Experiment with additional machine learning algorithms.
- Improve model performance through further hyperparameter tuning.
- Refine customer risk segmentation.
- Evaluate retention strategies through controlled experiments.
- Explore automated reporting and model monitoring.

---

**Project Domain:** Data Analytics | Machine Learning | Business Intelligence | Customer Retention
