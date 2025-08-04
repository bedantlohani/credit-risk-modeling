# Credit Risk Modeling on Freddie Mac Loan-Level Data


A comprehensive credit risk pipeline built end-to-end on Freddie Mac single-family loan-level data, from ingestion through model validation and stress testing under Basel III/CCAR guidelines.

---

## 🚀 Project Overview

- **Objective:** Build and validate probability-of-default (PD), loss-given-default (LGD), and exposure-at-default (EAD) models; quantify portfolio tail risk (CVaR); and perform macro stress testing.
- **Data:** Freddie Mac Single-Family dataset (origination & performance files, 2000–2024).
- **Key Steps:**
  1. **Dynamic ETL Pipeline**  
     - Download, unzip, and load origination & performance CSVs  
     - Clean, normalize, and merge on loan identifiers  
  2. **Feature Engineering**  
     - Compute Debt-to-Income (DTI) ratios  
     - Bucketize and Weight-of-Evidence (WoE) encode categorical predictors  
  3. **Model Training & Tuning**  
     - PD: Logistic Regression & Random Forest  
     - LGD/EAD: Random Forest & XGBoost  
     - Hyperparameter search via cross-validation  
  4. **Portfolio Risk & Stress Testing**  
     - Calculate Conditional Value-at-Risk (CVaR) at multiple confidence levels  
     - Execute EBA-style macro stress scenarios (house-price shocks, unemployment spikes)  
  5. **Validation & Metrics**  
     - Discrimination: AUC, Kolmogorov–Smirnov (KS)  
     - Calibration: Hosmer–Lemeshow  
     - Benchmark against regulatory thresholds  

---

