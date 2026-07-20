# NPS Driver Analysis using Random Forest and SHAP  
Author: **Petar**

## 📘 Overview
This project identifies the **biggest drivers of Net Promoter Score (NPS)** using
modern machine-learning classification methods and explainability techniques.

Instead of predicting the exact NPS score, the project treats the task as a
**classification problem**, grouping customers into:
- **Detractors (0–6)**
- **Passives (7–8)**
- **Promoters (9–10)**

To understand *why* the model makes certain predictions,
**SHAP (SHapley Additive exPlanations)** is used to measure feature importance
and reveal the most influential NPS drivers.

---

## 🎯 Project Goals
- Convert NPS numerical scores into meaningful customer classes  
- Train classification model:
  - **Random Forest Classifier**
- Use **SHAP** to explain predictions and identify the biggest NPS drivers  
- Provide clear insights for decision-makers

---

## 🧠 Methodology

### 1. Data Preparation
- Data cleaning & preprocessing  
- Handling missing values  
- One-hot encoding of categorical variables  
- Train/test split  
- Creation of NPS categories: Detractor / Passive / Promoter  

### 2. Models Used
The project includes tree-based ensemble model:

#### 🌲 **Random Forest Classifier**
- Robust to noise  
- Handles nonlinear relationships  
- Captures complex interactions  
- Works well with SHAP (TreeExplainer)

### 3. Explainability with SHAP
SHAP is applied to each model to reveal:

- **Global feature importance** (which factors matter overall)
- **Local explanations** (why a specific prediction happened)
- **Direction of influence**  
  (which features push customers toward promoter or detractor classes)

This helps discover **true NPS drivers**, such as:
- Support rating  
- Product satisfaction  
- Delivery issues  
- Pricing perception  
- Demographics / segmentation  
(and more depending on dataset)

---

## 📊 Outputs & Results

The notebook generates:
- Classification metrics (accuracy, F1-score, confusion matrix)
- SHAP summary plots for:
  - Random Forest  
- Comparison of feature importance across models  
- Driver insights, such as:
  - "Feature A strongly increases promoter probability"
  - "Feature B drives detractor outcomes"
  - "Feature C has minimal influence"

This allows you to see **which factors consistently emerge as the biggest drivers**.

