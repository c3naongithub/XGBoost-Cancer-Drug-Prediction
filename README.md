# XGBoost-Cancer-Drug-Prediction
Machine Learning project predicting cancer drug sensitivity using XGBoost on the GDSC dataset, exploring hyperparameter tuning and model performance.
# DrugResponsePrediction

## Overview
This project explores **predicting drug sensitivity in cancer cell lines** using **XGBoost**, trained on a curated subset of the **GDSC (Genomics of Drug Sensitivity in Cancer) dataset from Kaggle**.  

The goal was to predict drug response using biologically significant features and evaluate multiple XGBoost configurations to determine the most effective model.

---

## Dataset Features & Biological Interpretation

The model was trained on the following columns:

| Feature | Biological Interpretation |
|---------|---------------------------|
| **MAX_CONC** | Maximum drug concentration is the strongest predictor. Higher concentrations directly impact drug sensitivity. |
| **MIN_CONC** | Minimum concentration also significant but has a negative relationship. Lower concentrations may indicate different response mechanisms. |
| **DRUG_ID** | Specific drug properties strongly influence sensitivity. Different drugs have varying potency and mechanisms. |
| **PATHWAY_NAME** | Biological pathways affect drug response. Certain pathways make cells more/less sensitive. |
| **PUTATIVE_TARGET** | Drug targets influence effectiveness. Presence/absence of target determines response. |
| **CELL_LINE_NAME** | Cell line characteristics matter. Genetic background affects drug sensitivity. |
| **DRUG_NAME** | Least important (often correlated with DRUG_ID). Name itself doesn't add predictive power beyond ID. |

---

## Modeling Approach

- **Algorithm:** XGBoost (Gradient Boosting)  
- **Configurations Tested:** Shallow, Medium, Deep, Conservative, Aggressive, Baseline, Tuned  
- **Performance Metrics:** R², MSE, MAE  

**Best Model:** `XGB_Tuned`  
- **R² = 0.7376**  
- **MSE = 0.1373**  
- **MAE = 0.1033**  

---

## Key Insights

- **MAX_CONC** is the strongest predictor of drug response.  
- Biological context (pathway, target, cell line) significantly influences drug sensitivity.  
- Hyperparameter tuning improves model performance.  
- Some features (like **DRUG_NAME**) are redundant when correlated with stronger predictors (**DRUG_ID**).  

---

## Tech Stack

`Python | XGBoost | Pandas | NumPy | Scikit-Learn | Matplotlib | Kaggle Dataset`

---


