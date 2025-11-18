# Obesity Classification Using Lifestyle and Physical-Condition Data

## Overview
This repository contains the full workflow for a data science project aimed at predicting **obesity levels** using lifestyle, demographic, and physical-condition features.

The project follows an academic research structure and includes:

- Data preprocessing  
- Exploratory Data Analysis (EDA)  
- Machine-learning modeling  
- Statistical evaluation  
- Feature-importance analysis  
- Comparison with medical BMI standards  
- Two written reports summarising key findings  

The goal is to understand which behavioural and physical factors most strongly influence obesity and to evaluate how well different models can classify multiple obesity categories.

---

## Research Motivation
Obesity is a rising global health concern, strongly linked to chronic diseases and long-term health risks.  
Machine learning provides a scalable way to identify patterns in lifestyle behaviour and physical characteristics that contribute to obesity.

This project explores:

- Predictive performance of different classification models  
- Key drivers of obesity  
- Whether model complexity provides meaningful performance improvements  
- How model results align with **WHO BMI thresholds**

---

## Why These Models?

### **Logistic Regression — Baseline**
Chosen for:

- High interpretability  
- Low computational cost  
- Transparent feature effects  
- Common use in epidemiology and health research  

It provides a stable baseline for comparison with more complex models.

### **Gradient Boosting — Benchmark**
Chosen for:

- Ability to capture non-linear feature relationships  
- Strong performance on structured tabular data  
- Prior success in obesity prediction studies  
- Robust behaviour across mixed feature types  

---

## Evaluation Strategy
To assess model performance rigorously, the project uses several academic evaluation methods:

### **Accuracy**
Measures overall correctness of predictions.

### **Macro F1-Score**
Treats all obesity classes equally—important for a multi-class dataset.

### **95% Confidence Intervals**
Used to examine reliability and stability of evaluation metrics.

### **5×2 Cross-Validation Paired t-Test**
Tests whether two models differ **significantly**.  
Our result (**p = 0.24**) shows **no significant difference** between Logistic Regression and Gradient Boosting.

### **Confusion Matrix**
Highlights class-specific errors.  
Normal Weight and Overweight I show expected overlap, as individuals in these categories often share similar lifestyle patterns.

### **Feature Importance**
Evaluated through:

- Permutation Importance  
- Logistic Regression coefficients (after PCA, interpreted with caution)  

This helps explain **why** the model makes certain predictions.

### **BMI-Based Validation**
A separate BMI-only classifier achieved **95% accuracy**, confirming:

- Alignment with **WHO medical standards**  
- External validity of the ML models  
- Strong influence of physical measures such as weight and height  

---

## Repository Structure

**Dataset from https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition**

### `stage_1_prep.ipynb`
- Initial data cleaning and preparation  
- Encoding of categorical features  
- Scaling and anomaly checks  
- BMI computation using WHO thresholds  

### `DSI_AT_STAGE1_EDA.ipynb`
- Exploratory analysis of dataset structure  
- Patterns in diet, activity, and physical measurements  
- Correlation analysis and initial insights  

### `dsi_at_stage_2c_Modeling.ipynb`
- Preprocessing pipeline (scaling, PCA)  
- Model training and hyperparameter tuning  
- Cross-validation and statistical evaluation  
- Confusion matrix & ROC curves  
- Feature-importance analysis  
- BMI validation experiment  

### Stage 1 Report
Summarises EDA results and key observations.

### Stage 2 Report
Presents modeling workflow, evaluation, interpretation, and conclusions.

---

## Key Findings
- Both models achieved **~97% accuracy**, with *no significant difference* in performance.  
- Weight, height, gender, diet habits, and activity level were the strongest predictors.  
- BMI-only classification reached **95% accuracy**, consistent with WHO obesity ranges.  
- Obesity risk is strongly associated with both **physical measurements** and **daily lifestyle behaviours**.  
- **Logistic Regression** is recommended due to its interpretability and efficiency.

---

## How to Use This Repository

### 1. Environment
Run notebooks using **Jupyter Notebook** or **Google Colab**.

### 2. Execution Workflow
1. Run `stage_1_prep.ipynb`  
2. Run `DSI_AT_STAGE1_EDA.ipynb`  
3. Run `dsi_at_stage_2c_Modeling.ipynb`  
4. Review the reports for complete interpretation  

---

