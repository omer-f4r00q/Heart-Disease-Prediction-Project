# 🫀 Heart Disease Prediction: End-to-End Data Science & Analytics Project

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn%20%7C%20XGBoost-orange)
![Data Science](https://img.shields.io/badge/Data%20Science-Pandas%20%7C%20Seaborn-green)

## 📌 Project Overview
Cardiovascular diseases (CVDs) are the leading cause of death globally. Early detection and management are critical for patients with high cardiovascular risk. 

This project involves the complete end-to-end development of a machine learning pipeline to predict the presence of heart disease in patients. By analyzing clinical metrics (such as blood pressure, cholesterol, and stress test results), this project provides actionable, data-driven recommendations to hospital administrators to improve triage and prevent life-threatening misdiagnoses.

## 🎯 Core Objectives Completed
1. **Exploratory Data Analysis (EDA):** Uncovered the medical narrative within the data, identifying strong predictive correlations between maximum heart rate, asymptomatic chest pain, and heart disease.
2. **Data Preprocessing & Engineering:** Handled categorical data via One-Hot Encoding, addressed severe feature scale disparities using `StandardScaler`, and prevented data leakage through rigorous train-test splitting protocols.
3. **Predictive Modeling:** Trained and evaluated multiple classification algorithms (Logistic Regression, Random Forest, SVM, XGBoost).
4. **Clinical Optimization:** Shifted evaluation priority from baseline Accuracy to minimizing **False Negatives (Type II Errors)** to ensure critically ill patients are not misdiagnosed as healthy.

## 🏆 Final Model Performance
The **Tuned Random Forest Classifier** (`GridSearchCV` optimized) was selected as the production model.
* **Accuracy:** 86.1%
* **False Negatives:** Reduced to 1 (maximizing Recall for the positive class).
* **Rationale:** It structurally mitigated overfitting (`min_samples_split=10`) while providing the best balance of overall accuracy and critical patient safety.

## 🏥 Actionable Hospital Recommendations
Based on the AI's Feature Importance extraction, the following clinical protocols are recommended:
1. **Mandate Thallium Stress Tests:** The model identified the results of the Thallium stress test (`thal`) as the single most powerful predictor of heart disease. Prioritize funding for this specific test.
2. **Re-evaluate "Asymptomatic" Chest Pain:** Patients presenting with Type 4 (asymptomatic) chest pain showed a drastically higher rate of diagnosed heart disease. Doctors must be trained to recognize "silent" heart disease.
3. **Deploy AI as an Early Triage Tool:** Integrate this Tuned Random Forest model into the hospital's Electronic Health Records (EHR) to automatically flag high-risk patient files prior to discharge.

## 🛠️ Repository Structure
```text
├── data/                                 # Contains the raw dataset files (ignored in git)
├── notebooks/
│   └── 01_heart_disease_eda_and_modeling.ipynb  # Main project notebook (EDA to Modeling)
├── .gitignore                            # Hidden files and virtual environments to ignore
├── requirements.txt                      # Dependencies for perfect reproducibility
└── README.md                             # Project documentation
```

## 🚀 How to Run the Project Locally
To reproduce this project on your local machine, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/omer-f4r00q/Heart-Disease-Prediction.git
   cd Heart-Disease-Prediction
   ```
2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/Scripts/activate  # On Windows Git Bash
   ```
3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
4. **Launch Jupyter Lab:**
   ```bash
   jupyter lab
   ```