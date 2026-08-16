# Customer Churn Prediction

An end-to-end machine learning project for predicting customer churn using Python and scikit-learn.

## Project Overview

Customer churn is an important business problem because retaining existing customers is often more cost-effective than acquiring new ones.

This project builds a machine learning pipeline to identify customers who are at higher risk of leaving based on demographic, account, and service-related information.

## Dataset

The project uses the Telco Customer Churn dataset.

The dataset contains customer information including:

- Tenure
- Contract type
- Internet service
- Payment method
- Monthly charges
- Total charges
- Customer demographics
- Churn status

**Target variable:** `Churn`

## Project Workflow

1. Data loading and inspection
2. Data cleaning
3. Exploratory Data Analysis (EDA)
4. Feature preprocessing
5. Train/test split
6. Logistic Regression
7. Random Forest
8. Model evaluation
9. Feature importance analysis
10. Churn prediction

## Machine Learning Models

### Logistic Regression

Used as an interpretable classification baseline.

### Random Forest

Used to capture more complex nonlinear relationships between customer characteristics and churn.

## Model Evaluation

Models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- ROC Curve

For churn prediction, accuracy alone is not sufficient. Recall is particularly important because failing to identify customers who are likely to churn can result in lost revenue.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- scikit-learn
- Jupyter Notebook

## Repository Structure

```text
customer-churn-prediction/
│
├── Telco-Customer-Churn.csv
├── customer_churn.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## How to Run

Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
customer_churn.ipynb
```

and run the notebook cells sequentially.

## Business Application

A churn prediction model can help businesses identify high-risk customers before they leave.

Predicted churn probabilities can be used to prioritize retention campaigns, targeted offers, customer support outreach, and account reviews.

## Future Improvements

- Hyperparameter tuning
- Cross-validation
- SHAP model explanations
- Churn probability threshold optimization
- FastAPI model deployment
- Docker containerization
- Cloud deployment
- Model monitoring
