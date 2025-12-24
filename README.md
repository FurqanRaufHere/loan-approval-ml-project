# Loan Approval Prediction & Credit Risk Analysis

## Business Problem Summary
Financial institutions process a high volume of personal loan applications monthly, each carrying a different level of credit risk. Approving high-risk applicants leads to defaults and financial losses, while rejecting low-risk applicants reduces revenue and customer trust.

**The goal of this project is to:**
* **Predict** loan approval decisions using historical applicant data.
* **Identify** key factors influencing credit risk.
* **Build** an explainable machine learning solution suitable for real-world banking environments.

This project simulates a real-world credit underwriting workflow, focusing on both predictive performance and decision transparency.

---

## Dataset Overview
The dataset contains ~20,000 historical loan application records with 36 features.

### Target Variable
* **`LoanApproved`**
  * **1** → Loan Approved
  * **0** → Loan Declined

### Feature Categories
* **Demographics:** Age, marital status, dependents.
* **Financials:** Income, employment details, debt-to-income ratios.
* **Credit Behavior:** Past defaults, credit scores, bankruptcy history.
* **Loan Characteristics:** Amount, duration, and purpose

---

## Approach & Methodology
The project follows a structured, bank-style machine learning pipeline:

### 1. Data Understanding & Cleaning
* Validated data types and distributions.
* Engineered time-based features and removed redundant/leaky variables.
* Ensured features remained realistic from a credit risk perspective.

### 2. Exploratory Data Analysis (EDA)
* Analyzed approval rates across employment, education, and home ownership.
* Assessed the impact of credit scores and debt-to-income ratios.
* Identified high-risk applicant segments using combined risk indicators.

### 3. Modeling & Evaluation
Three classification models were trained and evaluated:
* **K-Nearest Neighbors (KNN)**
* **Decision Tree**
* **Random Forest**

**Evaluation Strategy:** Stratified train/test splits, Cross-validation, ROC-AUC, and Precision-Recall analysis.

### 4. Model Interpretability
* Feature importance ranking to identify top risk drivers.
* Partial dependence plots for key numeric features.
* Plain-English interpretation of model behavior for stakeholders.

---

## Key Insights
* **Credit Score** is the strongest driver of loan approval decisions.
* **High Debt-to-Income (DTI)** ratios significantly decrease approval probability.
* **Stability Matters:** Stable employment and home ownership correlate positively with approval rates.
* **Risk History:** Previous defaults or bankruptcies clearly identify high-risk segments.

---

## Final Model Performance
**Selected Model:** Random Forest

**Reasoning:**
* Achieved the highest **ROC-AUC** across cross-validation and test data.
* Successfully captured non-linear relationships and feature interactions.
* Provided a strong balance between predictive power and explainability.

---

## Business Impact
* **Reduced Defaults:** Improved identification of high-risk applicants.
* **Efficiency:** Automated preliminary screening to speed up the manual underwriting process.
* **Transparency:** Clear feature importance ensures the model aligns with regulatory and ethical banking standards.

---

## How to Run the Project
1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd loan-approval-ml-project