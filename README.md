# 🏦 Loan Approval Prediction

A machine learning project that predicts whether a loan application will be approved based on applicant financial and demographic features.

## 📋 Overview

This project performs end-to-end exploratory data analysis (EDA), data preprocessing, feature engineering, and classification modelling on a synthetic loan application dataset of 1,000 records. The goal is to build an interpretable model that can assist financial institutions in automating the initial screening of loan applications.

## 📊 Dataset

| Property | Value |
|---|---|
| File | `loan_approval_data.csv` |
| Records | 1,000 |
| Features | 19 |
| Target | `Loan_Approved` (Yes / No) |

### Feature Description

| Feature | Type | Description |
|---|---|---|
| `Applicant_ID` | Numeric | Unique identifier |
| `Applicant_Income` | Numeric | Monthly income of applicant |
| `Coapplicant_Income` | Numeric | Monthly income of co-applicant |
| `Employment_Status` | Categorical | Salaried / Self-employed / Contract / Unemployed |
| `Age` | Numeric | Age of applicant |
| `Marital_Status` | Categorical | Married / Single |
| `Dependents` | Numeric | Number of dependents |
| `Credit_Score` | Numeric | Credit bureau score |
| `Existing_Loans` | Numeric | Number of existing active loans |
| `DTI_Ratio` | Numeric | Debt-to-Income ratio |
| `Savings` | Numeric | Applicant's total savings |
| `Collateral_Value` | Numeric | Value of collateral offered |
| `Loan_Amount` | Numeric | Requested loan amount |
| `Loan_Term` | Numeric | Loan duration in months |
| `Loan_Purpose` | Categorical | Personal / Car / Home / Business |
| `Property_Area` | Categorical | Urban / Semiurban / Rural |
| `Education_Level` | Categorical | Graduate / Not Graduate |
| `Gender` | Categorical | Male / Female |
| `Employer_Category` | Categorical | Private / Government / MNC / Unemployed |

## 🔬 Methodology

```
Raw Data → EDA → Missing Value Handling → Encoding → Scaling → Modelling → Evaluation
```

### Steps
1. **Exploratory Data Analysis** — Distribution plots, correlation heatmaps, class balance checks
2. **Data Cleaning** — Mode/median imputation for missing values in categorical and numerical columns
3. **Encoding** — Label encoding for binary targets; one-hot / ordinal encoding for features
4. **Feature Engineering** — Polynomial features (`DTI_Ratio²`, `Credit_Score²`) to capture non-linear relationships
5. **Modelling** — Logistic Regression and Gaussian Naïve Bayes classifiers
6. **Evaluation** — Accuracy, Precision, Recall, Confusion Matrix

## 📈 Results

| Model | Accuracy | Precision | Recall |
|---|---|---|---|
| Logistic Regression | **87%** | 0.787 | 0.787 |
| Gaussian Naïve Bayes | 85.5% | 0.808 | 0.689 |

## 🗂️ Project Structure

```
loan-approval-prediction/
│
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
│
├── loan_approval_prediction.ipynb
│
├── data/
│   └── loan_approval_data.csv
```

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook / JupyterLab

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/CreditSystem.git
cd CreditSystem

# 2. Create and activate a virtual environment (recommended)
python -m venv venv
source venv/bin/activate        # Linux / macOS
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the notebook
jupyter notebook loan_approval_prediction.ipynb
```

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-4c72b0)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the [MIT License](LICENSE).
