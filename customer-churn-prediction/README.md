# Customer Churn Prediction

End-to-end machine learning project that predicts customer churn using the IBM Telco Customer Churn sample dataset.

## Business Problem

Customer churn directly affects recurring revenue. The goal of this project is to identify customers at higher risk of leaving so retention teams can prioritize outreach.

## Project Workflow

1. Load and inspect the dataset
2. Clean missing and invalid values
3. Explore churn patterns
4. Prepare categorical and numerical features
5. Train baseline Logistic Regression and Random Forest models
6. Evaluate with accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrices
7. Inspect important churn drivers
8. Save the best model for reuse

## Repository Structure

```text
customer-churn-prediction/
├── README.md
├── requirements.txt
├── .gitignore
├── customer_churn.ipynb
├── data/
│   └── Telco-Customer-Churn.csv
├── images/
└── models/
```

## Dataset

Source: IBM Telco Customer Churn sample data.

Target:
- `Churn = Yes` means the customer left.
- `Churn = No` means the customer remained.

Examples of predictors include tenure, contract type, payment method, internet service, monthly charges, and total charges.

## Models

- Logistic Regression
- Random Forest

The notebook uses a preprocessing pipeline with:
- median imputation for numeric columns
- standard scaling for numeric columns
- most-frequent imputation for categorical columns
- one-hot encoding for categorical columns

## Evaluation

The project compares models using:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

For churn prediction, recall and ROC-AUC matter because missing a likely churner can be more costly than contacting some customers who would have stayed.

## How to Run

```bash
git clone <your-repository-url>
cd customer-churn-prediction
pip install -r requirements.txt
jupyter notebook customer_churn.ipynb
```

## Portfolio Talking Points

Be ready to explain:
- why `customerID` is excluded
- why `TotalCharges` must be converted to numeric
- why stratified train/test splitting is useful
- why accuracy alone is not enough
- the tradeoff between precision and recall
- how the model could support a retention campaign

## Next Improvements

- tune model hyperparameters
- optimize the probability threshold for retention cost/benefit
- add SHAP explanations
- deploy the model with FastAPI
- containerize with Docker
- add monitoring for data and prediction drift
