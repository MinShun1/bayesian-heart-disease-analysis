# Bayesian Predictive Modeling for Heart Disease

This project applies **Bayesian Logistic Regression** to the **Heart Disease UCI dataset** to perform **model comparison**, **predictive analysis**, and **prescriptive decision-making**.

## Overview
Heart disease remains one of the leading causes of death globally. Early identification of individuals at risk can significantly improve prevention and treatment outcomes. This project leverages the Bayesian framework to model uncertainty, quantify parameter credibility, and guide clinical decisions through probabilistic reasoning.

## Objectives
1. **Model Comparison:**  
   Compare a baseline model with uninformative priors to a hypertuned model with informative priors (based on [Ahamad et al., 2023]).
2. **Predictive Analysis:**  
   Assess predictive accuracy on unseen data using posterior predictive checks, classification metrics (accuracy, AUC, sensitivity, specificity), and calibration.
3. **Prescriptive Analysis:**  
   Develop cost-sensitive decision rules to minimize expected misclassification cost, assuming that **missing a sick patient (false negative)** is **ten times more costly** than **treating a healthy patient unnecessarily (false positive)**.

## Repository Structure
- `1_Data/` → Dataset used in this project (already preprocessed and scaled).  
- `2_Analysis/` → RMarkdown source files and knitted reports, including:
  - Exploratory data analysis and feature inspection.  
  - Model building and diagnostics for both baseline and hypertuned models.  
  - **Predictive and prescriptive analysis for the best-performing (hypertuned) model**, incorporating decision thresholds and cost-based evaluation.  
- `3_Reports/` → Final comparison summary between baseline and hypertuned models (numerical tables and conclusions), compiled into a **comprehensive PDF report**.

## Key Insights
- The **hypertuned Bayesian model** with informative priors outperformed the baseline in both calibration and predictive performance.  
- Incorporating asymmetric misclassification costs improved model sensitivity for high-risk patients.  
- Posterior distributions provide interpretable evidence of variable importance (e.g., age, cholesterol, and sex) in predicting heart disease.

## Tools & Environment
- **Language:** R  
- **Libraries:** `rjags`
- **Computation:** 2 chains × 5000 iterations (burn-in = 1000, thin = 5)

## Reference
Ahamad, M. N., et al. (2023). *Bayesian Predictive Modelling of Heart Disease Using Logistic Regression.* Processes, 11(3), 3734.
