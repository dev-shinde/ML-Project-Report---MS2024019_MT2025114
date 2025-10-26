# 🧠 Obesity Classification using Machine Learning

This repository contains all project files, datasets, and experiment records for the **Machine Learning project on Obesity Classification**.  
The project focuses on analyzing demographic and lifestyle factors to classify individuals into different obesity categories using advanced machine learning models.  
The work emphasizes **iterative experimentation**, **hyperparameter fine-tuning**, and **systematic model improvement** through structured experimentation with XGBoost and related algorithms.

---

## 📂 Repository Structure

📦 **Project Directory Overview**  
│  
├── 📄 **Datasets**  
│ ├── `train.csv` — Processed training dataset containing all features and target labels  
│ └── `test.csv` — Evaluation dataset used for generating predictions  
│  
├── 📓 **Experiment Notebooks**  
│ ├── Multiple Jupyter notebooks, each representing a separate experimental phase  
│ ├── These notebooks include model preprocessing, training, and parameter tuning logic  
│ └── Example: iterative fine-tuning runs stored as `final<num>.ipynb` (e.g., final8, final10, etc.)  
│  
├── 📁 **Experiment Folders**  
│ ├── Each folder (e.g., `Final 8`, `Final 9`, etc.) corresponds to one experimental iteration  
│ ├── Contains generated result files (Excel/CSV) for top-performing models in that phase  
│ ├── Includes:  
│ │ - Top parameter configurations discovered during tuning  
│ │ - Model output files (`model_score_xxxx.csv`) for predictions  
│ └── These files document experiment outcomes, allowing comparison of results across iterations  
│  
├── 🧾 **Parameter Records**  
│ ├── `All Record for params Note.txt` — Contains parameter configurations and validation scores  
│ └── Used to trace hyperparameter evolution across different experimental phases  
│  
├── 🧩 **Model Generator Script**  
│ └── `Model Generator.ipynb` — Automates model training for top parameter sets and generates multiple prediction files for evaluation  
│  
├── 📄 **README File**  
│ └── Provides structured documentation of the workflow, directory organization, and methodology  
│  
└── 📁 **Fine-Tuning Phases**  
  Each subdirectory under this section stores results from a specific iteration in the hyperparameter optimization process, enabling clear reproducibility of experiments  

---

## ⚙️ Workflow Overview

The project follows a **structured, experiment-driven workflow**:

1. **Data Preprocessing**  
   - Categorical features encoded via One-Hot Encoding  
   - Numerical features standardized using `StandardScaler`  
   - Ensured alignment between training and test feature spaces  

2. **Baseline Model Development**  
   - Established initial benchmarks using Logistic Regression, Decision Tree, and Random Forest  
   - Selected **XGBoost** as the primary model due to superior generalization and performance  

3. **Iterative Experimentation**  
   - Each notebook (`final<num>.ipynb`) represents an independent experimental iteration  
   - Experiments explored parameter ranges for learning rate, max depth, regularization, and sampling ratios  
   - Validation accuracy and parameter configurations recorded after each run  

4. **Result Recording and Analysis**  
   - For each tuning iteration, the top-performing parameter sets and corresponding output predictions were stored as `.csv` or `.xlsx` files in their respective experiment folders  
   - These outputs were used for comparative performance tracking and ensemble validation  

5. **Refinement and Fine-Tuning**  
   - Subsequent iterations narrowed parameter ranges around previously optimal values  
   - Gradual improvements achieved through controlled experimentation and ensemble averaging  
   - Each phase captured incremental learning in the parameter optimization process  

6. **Final Model Selection**  
   - The best-performing configuration was identified through analysis of top experiment results  
   - The final model achieved the highest validation accuracy across all iterations, and its predictions were used for submission and evaluation  

---

## 📊 Outcome and Insights

- Achieved high multi-class classification accuracy through methodical fine-tuning of XGBoost  
- The structured experimentation allowed tracing how parameter refinement influenced accuracy improvements  
- Each experiment folder serves as a transparent record of the model evolution process, ensuring reproducibility and traceability  
- The approach prioritized interpretability and robustness, not just high accuracy  
