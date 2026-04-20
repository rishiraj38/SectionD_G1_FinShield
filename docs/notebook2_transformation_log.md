#  Notebook 02 – Data Transformation & Feature Engineering Log

## Input Dataset
- Source: loan_stage1_cleaned.csv

---

##  Step 1: Categorical Value Transformation
Converted encoded categorical values into meaningful real-world labels for better interpretability:

- loan_limit:
  - cf → conforming loan
  - ncf → non-conforming loan
  
- gender:
  - sex not available → NA
 
- approv_in_adv:
  - nopre → no pre-approval
  - pre → pre-approved

- loan_type:
  - type1 → home loan
  - type2 → personal loan
  - type3 → commercial loan

- loan_purpose:
  - p1 → home purchase
  - p2 → home improvement
  - p3 → debt consolidation
  - p4 → business purpose

- credit_worthiness:
  - l1 → high creditworthy
  - l2 → medium creditworthy

- open_credit:
  - nopc → no open credit
  - opc → open credit line

- business_or_commercial:
  - b/c → business use
  - nob/c → personal use

- neg_ammortization:
  - not_neg → no
  - neg_amm → yes

- interest_only:
  - not_int → no
  - int_only → yes

- lump_sum_payment:
  - not_lpsm → no
  - lpsm → yes

- occupancy_type:
  - pr → primary residence
  - sr → secondary residence
  - ir → investment residence

- credit_type:
  - cib → cibil
  - exp → experian
  - crif → crif
  - equi → equifax


---

##  Step 2: Feature Engineering
Feature Engineering Summary

We have performed the following feature engineering steps:

*   **`ltv_risk_bucket`**: Created a categorical variable based on `ltv` (loan-to-value) to classify loans into 'Low', 'Moderate', 'High', and 'Very High' risk buckets.
*   **`credit_score_bucket`**: Created a categorical variable based on `credit_score` to classify applicants into 'Poor', 'Fair', 'Good', 'Very Good', and 'Excellent' credit score buckets.
*   **Column Renaming**: Renamed the column `dtir1` to `debt_to_income_ratio` for better clarity and understanding.
*   **Column Removal**: Removed the redundant columns `security_type` and `secured_by` as they were not adding significant value to the dataset.

---

## Step 3: Final Validation
- Verified:
  - Data types
  - Missing values
  - Dataset shape
- Ensured dataset is clean, consistent, and analysis-ready

---

##  Output
- Final dataset saved as:
  - `loan_final_cleaned.csv`

---

##  Summary
This notebook focused on:
- Converting encoded categorical values into meaningful business-friendly labels
- Selective outlier handling on critical numerical features
- Creating new financial ratio features for deeper insights

The dataset is now fully prepared for data visualization and analysis.
