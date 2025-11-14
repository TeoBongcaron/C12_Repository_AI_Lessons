
# Fairness and Explainability in Machine Learning

## Project Overview
This project demonstrates an end-to-end workflow for building, evaluating, and interpreting a machine learning model with a focus on **fairness** and **explainability**.  
We use the **UCI Adult Income dataset** to predict whether an individual earns more than \$50K annually, while analyzing fairness across **gender** groups.

---

## Dataset
- **Source**: [UCI Adult dataset](https://archive.ics.uci.edu/ml/datasets/adult)
- **Target Variable**: `class` → Binary (`<=50K`, `>50K`)
- **Sensitive Attribute**: `sex` (Male/Female)
- **Features**: Age, education, occupation, hours-per-week, marital status, etc.
- **Preprocessing**:
  - Removed missing values (`?`)
  - One-hot encoded categorical features
  - Standardized numeric features

---

## Model Training
- **Algorithm**: Logistic Regression (`scikit-learn`)
- **Pipeline**:
  - Preprocessing (scaling + one-hot encoding)
  - Logistic regression classifier
- **Train/Test Split**: 80/20 stratified
- **Evaluation Metrics**:
  - Accuracy: ~0.83
  - Confusion Matrix
  - Classification Report (precision, recall, F1-score)

---

## Fairness Analysis
Fairness metrics were computed using **Fairlearn**:

- **Metrics**:
  - Accuracy
  - Selection Rate
  - False Positive Rate (FPR)
  - True Positive Rate (TPR)
- **Sensitive Feature**: Gender (`sex`)
- **Findings**:
  - Men had higher selection rates for `>50K` predictions.
  - Disparities in FPR and TPR across gender groups.
  - Indicates potential bias requiring mitigation.

**Visualization**:  
Bar plots of fairness metrics by gender provide interpretable group comparisons.

---

## Explainability
Two complementary techniques were applied:

### SHAP (SHapley Additive Explanations)
- **Global**: Summary plots highlight most influential features (education, hours-per-week, marital status).
- **Local**: Waterfall plots explain individual predictions, showing how each feature pushes the probability toward or away from `>50K`.

### LIME (Local Interpretable Model-agnostic Explanations)
- Builds a local surrogate model around individual predictions.
- Reveals top contributing features for specific instances (e.g., education level, work hours, gender).

---

## Conclusion
This project illustrates:
- How to train and evaluate a predictive model.
- How to assess fairness across sensitive groups.
- How to apply explainability techniques for transparency.
- Why ethical AI practices are essential for responsible deployment.

Future work includes multi-attribute fairness analysis, advanced debiasing methods, and stakeholder engagement to ensure equitable AI systems.

