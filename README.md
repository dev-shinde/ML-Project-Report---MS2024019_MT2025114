# 🧠 Obesity Classification using Machine Learning

This repository contains the complete implementation, analysis, and experimentation workflow for the **Obesity Classification Machine Learning Project**.  
The project explores how demographic, behavioral, and lifestyle attributes contribute to predicting different obesity levels using multiple machine learning models, with **XGBoost** emerging as the most robust and optimized model.

This work was conducted as part of the **Machine Learning (AIM 511)** course at the **International Institute of Information Technology, Bangalore (IIITB)**.

---

## 📘 Project Overview

The project aims to build a multi-class classification model to categorize individuals into seven obesity levels based on lifestyle and physical activity factors.  
It combines **Exploratory Data Analysis (EDA)**, **Feature Engineering**, and **Iterative Hyperparameter Tuning** to achieve high model accuracy while maintaining interpretability and practical relevance.

Key objectives:
- Analyze relationships between lifestyle factors and obesity levels  
- Compare multiple ML models for classification performance  
- Optimize XGBoost through systematic hyperparameter fine-tuning  
- Generate interpretable insights from the dataset for real-world applicability  

---

## 📂 Repository Structure

📦 **Project Directory Overview**  
│  
├── 📁 **EDA/**  
│ &nbsp;&nbsp;&nbsp;&nbsp;Contains all exploratory data analysis notebooks and visualizations.  
│ &nbsp;&nbsp;&nbsp;&nbsp;Focuses on understanding feature distributions, correlations, and behavioral trends.  
│  
├── 📁 **Tested-Models/**  
│ &nbsp;&nbsp;&nbsp;&nbsp;Includes all Jupyter notebooks for baseline and comparative models.  
│ &nbsp;&nbsp;&nbsp;&nbsp;Models include Logistic Regression, Random Forest, Decision Tree, SVM, AdaBoost, and XGBoost.  
│ &nbsp;&nbsp;&nbsp;&nbsp;Each notebook records model accuracy, performance metrics, and confusion matrices.  
│  
├── 📁 **Hyperparameter-Finetuning/**  
│ &nbsp;&nbsp;&nbsp;&nbsp;Contains iterative fine-tuning experiments for XGBoost.  
│ &nbsp;&nbsp;&nbsp;&nbsp;Each subfolder (e.g., “Final 8”, “Final 10”, etc.) represents a distinct experiment phase.  
│ &nbsp;&nbsp;&nbsp;&nbsp;Includes:  
│ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• CSV/Excel result files of top-performing parameter sets  
│ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Model outputs (`model_score_xxxx.csv`) for submission and evaluation  
│ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• Parameter notes documenting cross-validation scores and observations  
│  
│ &nbsp;&nbsp;&nbsp;&nbsp;Also includes:  
│ &nbsp;&nbsp;&nbsp;&nbsp;`Model Generator.ipynb` — Automates model retraining for top parameter sets.  
│ &nbsp;&nbsp;&nbsp;&nbsp;`All Record for params Note.txt` — Records the evolution of hyperparameters across runs.  
│  
├── 📄 **README.md**  
│ &nbsp;&nbsp;&nbsp;&nbsp;Project documentation (this file). Provides structure, workflow explanation, and summary.  
│  
└── 📊 **Project Files Summary**  
  • All datasets (`train.csv`, `test.csv`) are preprocessed and consistent across experiments.  
  • All experiment folders are self-contained, ensuring reproducibility.  

---

## ⚙️ Workflow Overview

### 1. Data Preprocessing and Exploration
- Verified data completeness — no missing values were found.  
- Identified numerical, categorical (binary and multi-class) features.  
- Applied **Standard Scaling** to normalize numerical variables.  
- Used **One-Hot Encoding** for categorical variables to preserve interpretability.  
- Labeled target variable (`WeightCategory`) using label encoding.  

### 2. Exploratory Data Analysis (EDA)
- Conducted extensive visualization-based analysis on:
  - Gender-wise obesity trends  
  - Impact of physical activity and dietary patterns  
  - Distribution of BMI, height, and weight across categories  
  - Lifestyle behaviors (e.g., water intake, technology use, alcohol consumption)
- EDA highlighted meaningful real-world relationships between behavior and obesity—extending beyond prediction to actionable insight.

### 3. Model Development and Baseline Testing
- Trained multiple classification algorithms to establish performance baselines:
  - Logistic Regression  
  - Decision Tree  
  - Random Forest  
  - Support Vector Classifier  
  - AdaBoost  
  - XGBoost  
- Tree-based models demonstrated the strongest predictive performance, with XGBoost achieving ~89% baseline accuracy.

### 4. Iterative Hyperparameter Fine-Tuning
- Performed systematic parameter searches using:
  - **GridSearchCV** for exhaustive combinations  
  - **RandomizedSearchCV** for stochastic exploration  
- Evaluated tuning parameters such as:
  - `learning_rate`, `max_depth`, `min_child_weight`  
  - `subsample`, `colsample_bytree`, `gamma`  
  - `reg_alpha`, `reg_lambda`, `n_estimators`
- Each iteration refined the search space based on prior best-performing configurations.
- Achieved **final cross-validation accuracy: 91.4%**, marking convergence after several controlled iterations.

### 5. Result Tracking and Model Evaluation
- Each fine-tuning round generated:
  - Multiple prediction files (`submission_top5_model<num>.csv`)  
  - Corresponding logs and validation results  
- Experiment folders contain all artifacts for transparent performance comparison.
- Final evaluation conducted on test predictions and validation metrics confirmed strong generalization.

---

## 📊 Results and Insights

- Final XGBoost model achieved **~91.4% accuracy** with robust generalization.  
- Key predictors included physical activity (FAF), frequency of vegetable consumption (FCVC), and family history.  
- EDA findings demonstrated that behavioral and lifestyle factors have strong, interpretable effects on obesity categories.  
- The project highlights the importance of iterative experimentation for model refinement and real-world interpretability.

---

## 🧩 Summary

This repository encapsulates the entire lifecycle of an applied machine learning project — from exploratory data understanding to advanced model fine-tuning.  
The structured directory, detailed experiment tracking, and reproducible methodology make it a comprehensive reference for academic and applied machine learning workflows.
