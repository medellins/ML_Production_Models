# Machine Learning Ecosystem Applied to the Banking & Financial Sector 🏦📉

This repository contains an advanced suite of analytical frameworks developed under banking industry standards using **LightGBM**, **XGBoost**, **SHAP**, and **Optuna**. The ecosystem addresses two of the most critical business and financial pain points in financial institutions: credit default risk evaluation (*Credit Scoring*) and customer attrition control (*Customer Churn*).

---

## 📁 Corporate Directory Architecture (MLOps)

The environment implements structured binary persistence and statistical matrix isolation. The production ecosystem synchronizes automatically under the following tree structure:

```text
02_Sector_Bancario_Financiero/
├── datos_credit_scoring_bancario.csv   # Dataset for Module 1 (Credit Risk)
├── datos_churn_bancario.csv            # Dataset for Module 2 (Customer Churn)
├── modelo_scoring_bancario.pkl         # Serialized binary & metadata for Module 1 (LightGBM)
└── modelo_churn_bancario.pkl           # Serialized binary & metadata for Module 2 (XGBoost + Optuna)
```

---

## 🏗️ Methodological Breakdown of Banking Solutions

### 💳 1. Explainable and Regulated Credit Scoring (LightGBM + SHAP)
*   **Business Case:** Analytical classification of loan default risk for consumer and corporate lending portfolios, strictly complying with international regulatory frameworks (such as Basel III) that mandate algorithmic transparency.
*   **Methodology:** Gradient boosting classifier powered by **LightGBM**. The model's "black box" is audited end-to-end using Shapley Additive Explanations (**SHAP**), allowing a linear breakdown of how critical features like annual income, age, and debt-to-income ratio shift individual risk assessments.

### 🏃 2. Customer Churn Prediction via Bayesian Optimization (XGBoost + Optuna)
*   **Business Case:** Proactively identifying anomalous transactional patterns or drops in user activity that signal imminent account closures, enabling automated deployment of hyper-targeted retention marketing campaigns.
*   **Methodology:** Tree-boosting classifier powered by **XGBoost** hyper-optimized through **Optuna** (Bayesian Optimization). The framework runs intelligent searches across complex hyperparameter spaces (`learning_rate`, `max_depth`, `subsample`, `colsample_bytree`), minimizing cross-entropy loss (`logloss`) in a fraction of the time required by traditional grid search approaches.

---

## 📊 Operational Dashboards and Advanced Interaction (Plotly)

Statistical validation tools are developed with **Plotly (Dynamic HTML)** following a strict **four-decimal-place (`.4f`)** precision requirement for both dashboard layouts and hover tooltips:

1.  **Relative Feature Importance Plots:** Horizontal bar charts with explicit percentage mapping formatted directly outside each visual axis.
2.  **Operational Confusion Matrices:** Interactive heatmaps designed to audit critical False Negatives and False Positives, balancing capital credit losses against marketing retention costs.
3.  **Receiver Operating Characteristic Curves (ROC Curve):** Continuous mathematical tracing of sensitivity versus specificity, allowing risk officers to evaluate the optimal probability threshold by hovering over the curve.

---
**Engineered under strict software architecture and data science standards applied to large-scale financial services.** 🚀
