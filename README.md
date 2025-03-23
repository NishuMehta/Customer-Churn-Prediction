# Customer Churn Prediction

## Project Overview
This project aims to predict customer churn for a subscription-based service. By analyzing historical customer data, the goal is to identify key factors contributing to customer retention and churn. The final model highlights significant features that influence customer behavior and provides actionable insights for improving retention strategies.

## Dataset
**Dataset:** Churn_Modelling.csv  
**Key Features:**
- **CreditScore** - Customer's credit score
- **Age** - Customer's age
- **Tenure** - Duration of customer subscription
- **Balance** - Account balance
- **NumOfProducts** - Number of products subscribed
- **IsActiveMember** - Customer's active status
- **EstimatedSalary** - Customer's salary details

**Target Variable:** `Exited` (1 = Customer churned, 0 = Customer retained)

## Objective
The goal is to:
- Build a machine learning model that predicts customer churn.
- Identify the most influential factors contributing to churn.

## Steps to Run the Project
1. **Install Required Libraries:**
   ```bash
   pip install pandas scikit-learn xgboost seaborn matplotlib
   ```
2. **Download the Dataset:**
   Place the dataset file (`Churn_Modelling.csv`) in the project folder.

3. **Run the Jupyter Notebook (`.ipynb`) or Python Script:**
   ```bash
   jupyter notebook
   ```
   Open the notebook and run the cells step by step.

4. **Key Steps in Code Implementation:**
   - Data Cleaning & Preprocessing (Encoding, Scaling, Missing Value Handling)
   - Exploratory Data Analysis (EDA)
   - Model Building (Logistic Regression, Random Forest, XGBoost, SVM)
   - Manual Hyperparameter Tuning for Random Forest and XGBoost
   - Feature Importance Visualization
   - Key Insights from Visualizations

5. **Results:**
   
    | Model              | Accuracy  | ROC-AUC Score |  
    |--------------------|-----------|---------------|  
    | Logistic Regression| 0.8115    | 0.5809        |  
    | Random Forest      | **0.8675**| 0.7205        |<br>
    | XGBoost            | 0.863     | **0.7235**    |<br>
    | SVM                | 0.8535    | 0.6637        |<br>

The **Random Forest** model showed the best balance between accuracy and ROC-AUC score, making it the preferred model for this project.

## Insights from Feature Importance
- **Age** was the most significant factor in predicting churn. Older customers had a higher likelihood of leaving the service.
- **Number of Products** strongly influenced churn; customers with fewer products had a higher risk of leaving.
- **Balance** and **Estimated Salary** also played notable roles in customer behavior.

## Visualizations
- Distribution of churn across different age groups.
- Relationship between balance and customer churn.
- Churn trends based on the number of subscribed products.

## Repository Structure
```
|-- data
|   |-- Churn_Modelling.csv
|-- notebooks
|   |-- Customer_Churn_Prediction.ipynb
|-- README.md
|-- requirements.txt
``
