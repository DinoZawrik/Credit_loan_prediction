# Credit Default Prediction: A Machine Learning Approach

## Project Overview
This project focuses on developing a machine learning model to predict credit defaults. The primary objective is to maximize **recall**, reducing false negatives (predicting loan repayment when a default occurs) to minimize financial losses. The workflow includes data analysis, preprocessing, model training, evaluation, and hyperparameter tuning, showcasing the full lifecycle of a machine learning pipeline.

## Features
- **Exploratory Data Analysis (EDA):** Insights into feature relationships and their impact on credit default.
- **Data Preprocessing:** Includes handling missing values, label encoding, and scaling.
- **Class Imbalance Handling:** Utilizes SMOTE for balanced training data.
- **Machine Learning Models:** Logistic Regression with hyperparameter tuning.
- **Model Evaluation:** Performance metrics like recall, ROC-AUC, and confusion matrices.
- **Interpretability:** SHAP values for feature importance analysis.

---

## Installation
### Prerequisites
Ensure you have Python installed. Install the required libraries:
```bash
pip install numpy pandas seaborn matplotlib scikit-learn imbalanced-learn xgboost shap tqdm
```

### Dataset
The project uses the LendingClub loan dataset from Kaggle. Download it from [this link](https://www.kaggle.com/itssuru/loan-data) and save it in the `source/` directory as `loan_data.csv`.

---

## Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/credit-default-prediction.git
   cd credit-default-prediction
   ```
2. Run the Python script:
   ```bash
   python main.py
   ```

---

## Data Dictionary
| Variable          | Description                                                                                                           |
|-------------------|-----------------------------------------------------------------------------------------------------------------------|
| `credit_policy`   | 1 if the applicant meets credit underwriting criteria; 0 otherwise.                                                  |
| `purpose`         | Purpose of the loan (e.g., debt consolidation, credit card).                                                         |
| `int_rate`        | Interest rate (higher rates indicate riskier borrowers).                                                             |
| `installment`     | Monthly payment amount.                                                                                              |
| `log_annual_inc`  | Natural log of the self-reported annual income.                                                                      |
| `dti`             | Debt-to-income ratio.                                                                                               |
| `fico`            | FICO credit score.                                                                                                  |
| `days_with_cr_line` | Number of days the borrower has had a credit line.                                                                 |
| `revol_bal`       | Revolving balance (outstanding credit card balance).                                                                 |
| `revol_util`      | Revolving line utilization rate (credit used relative to total credit available).                                    |
| `inq_last_6mths`  | Number of inquiries in the past 6 months.                                                                            |
| `delinq_2yrs`     | Number of delinquencies (30+ days past due) in the last 2 years.                                                     |
| `pub_rec`         | Number of derogatory public records.                                                                                 |
| `not_fully_paid`  | Target variable: 1 if the loan is not fully paid (default), 0 otherwise.                                             |

---

## Key Results
- **Logistic Regression Model:**
    - **Recall:** Achieves high recall for detecting defaults.
    - **ROC-AUC:** High discrimination power between default and non-default cases.
- **SHAP Analysis:** Identified key features influencing default predictions, such as interest rate, FICO score, and debt-to-income ratio.

### Visualizations
1. **Correlation Matrix:** Heatmap to identify feature relationships.
2. **Confusion Matrix:** Displaying the model's performance.
3. **ROC Curve:** Visualizing model discrimination power.
4. **SHAP Summary Plot:** Feature importance for model interpretability.

---

## Contribution
Contributions are welcome! Follow these steps:
1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your message"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

---


## Acknowledgements
- Dataset sourced from Kaggle: [LendingClub Loan Data](https://www.kaggle.com/itssuru/loan-data).
- Libraries: NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn, Imbalanced-learn, SHAP, TQDM.

---

