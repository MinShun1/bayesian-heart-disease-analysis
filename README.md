# bayesian-predictive-modeling-heart-disease

This project applies **Bayesian logistic regression** to the Heart Disease UCI dataset.

The project compares two models:
- **Baseline model** with uninformative priors.
- **Hypertuned model** with informative priors (based on [Ahamad et al., 2023](https://www.mdpi.com/2227-9717/11/3/3734)).

## Repository Structure
- `1_Data/` → dataset used in this project (already preprocessed & scaled).
- `2_Analysis/` → RMarkdown source files and knitted reports (including exploratory analysis, model diagnostics, and plots).
- `3_Results/` → comparison summary between baseline and hypertuned models (numerical tables & final conclusions).
