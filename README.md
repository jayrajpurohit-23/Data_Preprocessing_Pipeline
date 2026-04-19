# 🧠 HR Attrition Prediction System

A machine learning pipeline to predict employee attrition (whether an employee is likely to leave the company) using structured HR data.

---

## 📌 Overview

This project builds an end-to-end ML pipeline that:

* Cleans and preprocesses HR data
* Performs feature engineering
* Trains a classification model
* Evaluates performance
* Predicts employee attrition

The goal is to help HR teams **identify high-risk employees early** and take preventive actions.

---

## ⚙️ Tech Stack

* Python 🐍
* Pandas & NumPy
* Scikit-learn

---

## 📂 Project Structure

```
├── hr_data.csv              # Input dataset
├── main.py                 # ML pipeline script
├── attrition_model.pkl     # Saved model (after training)
├── hr_data_export.csv      # Processed dataset (optional)
└── README.md               # Project documentation
```

---

## 🔄 Workflow

### 1. Data Loading

* Reads dataset using Pandas

### 2. Data Cleaning

* Standardizes column names
* Handles string formatting
* Converts date columns

### 3. Feature Engineering

Creates new meaningful features:

* `experience_years` → tenure in company
* `age` → employee age
* `productivity` → engagement × satisfaction
* `attendance_risk` → absences + late days
* `high_performer` → binary performance flag
* `log_salary` → normalized salary
* `project_load` → workload category

---

### 4. Handling Missing Values

* Numeric → filled with median
* Categorical → filled with "unknown"

---

### 5. Encoding

* Converts categorical variables into numerical using one-hot encoding

---

### 6. Feature Selection

* Removes highly correlated features (>0.95)

---

### 7. Model Training

* Algorithm: Random Forest Classifier
* Parameters:

  * `n_estimators=200`
  * `max_depth=8`

---

### 8. Evaluation

* Accuracy Score
* Classification Report (Precision, Recall, F1-score)

---

## 🎯 Target Variable

* `termd`

  * `1` → Employee left
  * `0` → Employee stayed

---

## 🚀 How to Run

### 1. Install dependencies

```
pip install pandas numpy scikit-learn joblib
```

### 2. Run the script

```
python main.py
```

---

## 📊 Sample Output

```
Accuracy: 0.87

Classification Report:
              precision    recall  f1-score   support
           0       0.89      0.92      0.90       200
           1       0.82      0.76      0.79       100
```

---

## 📈 Future Improvements

* Add ROC-AUC and confusion matrix
* Handle class imbalance
* Use advanced models (XGBoost, LightGBM)
* Build a Streamlit dashboard
* Deploy as an API or SaaS product

---

## 💡 Use Cases

* HR analytics
* Employee retention strategy
* Workforce planning
* Predictive decision-making

---

## ⚠️ Disclaimer

* This model is for educational/demo purposes
* Real-world deployment requires:

  * Data validation
  * Bias handling
  * Compliance with HR policies

---

## 👨‍💻 Author

**JRP Soft Tech**
AI | SaaS | Drone Tech | Automation

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

---
