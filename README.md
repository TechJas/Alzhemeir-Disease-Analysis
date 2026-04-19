

# 🧠 Alzheimer’s Disease Diagnosis Detection using Machine Learning

## 📌 Overview

This project focuses on building a **machine learning-based diagnosis detection system** for Alzheimer’s Disease using clinical, cognitive, and functional assessment data.

The objective is to accurately identify whether a patient is diagnosed with Alzheimer’s Disease (binary classification: 0 = No, 1 = Yes) while prioritizing **minimization of false negatives**, which is critical in healthcare applications.

---

## 🎯 Problem Statement

Early and accurate detection of Alzheimer’s Disease is essential for timely intervention. Traditional analysis often fails to capture complex relationships between cognitive decline and behavioral symptoms.

This project aims to:

* Analyze key factors influencing Alzheimer’s diagnosis
* Identify strong predictive features
* Build and evaluate robust ML models for classification

---

## 📊 Dataset Description

The dataset consists of **2,149 patient records** with features including:

### 🧍 Demographics

* Age, Gender, Ethnicity, EducationLevel

### 🧬 Lifestyle Factors

* BMI, Smoking, AlcoholConsumption, PhysicalActivity
* DietQuality, SleepQuality

### 🏥 Medical History

* Hypertension, Diabetes, CardiovascularDisease
* Depression, HeadInjury, FamilyHistoryAlzheimers

### 🧠 Cognitive & Functional Assessments

* MMSE (Cognitive score)
* ADL (Activities of Daily Living)
* MemoryComplaints, Forgetfulness
* Confusion, Disorientation
* DifficultyCompletingTasks

### 🎯 Target Variable

* Diagnosis (0 = No Alzheimer’s, 1 = Alzheimer’s)

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights derived:

* **Strong Predictors**

  * MemoryComplaints → Significant increase in diagnosis probability
  * ADL → Lower activity strongly correlates with disease
  * MMSE → Lower cognitive scores indicate higher risk

* **Weak / Inconsistent Predictors**

  * Blood Pressure (Systolic/Diastolic)
  * Cardiovascular indicators
  * Diet & Sleep Quality

* **Key Finding**

  > Cognitive and functional decline features dominate prediction over lifestyle factors.

---

## 🧠 Feature Engineering

* Created derived features:

  * Pulse Pressure (Systolic - Diastolic)
  * Cardiovascular Risk Score (combined indicators)
* Applied quantile-based binning (`qcut`) for non-linear analysis
* Identified threshold-based behavior in ADL and cognitive features

---

## 🤖 Machine Learning Models

The following models were implemented:

| Model               | Purpose                          |
| ------------------- | -------------------------------- |
| Logistic Regression | Baseline & interpretability      |
| Decision Tree       | Rule-based understanding         |
| Random Forest ⭐     | Primary model (best performance) |

---

## ⚙️ Model Training Pipeline

* Feature selection based on EDA
* Train-test split (80/20)
* Standard scaling (for linear models)
* Class imbalance handled using `class_weight='balanced'`

---

## 📈 Evaluation Metrics

Given the healthcare context, emphasis was placed on:

* **Recall (Sensitivity)** → Minimize False Negatives
* Precision
* F1 Score
* Accuracy
* Confusion Matrix

---

## 🔍 Confusion Matrix Interpretation

| Metric           | Meaning                                         |
| ---------------- | ----------------------------------------------- |
| True Positive    | Correctly detected Alzheimer’s cases            |
| True Negative    | Correctly identified healthy patients           |
| False Positive   | Incorrect diagnosis (acceptable to some extent) |
| ❗ False Negative | Missed Alzheimer’s case (critical error)        |

> The model is optimized to **reduce false negatives**, ensuring that actual patients are not overlooked.

---

## 🚀 Model Optimization

* Applied **threshold tuning** to improve recall:

  * Lower threshold → Higher sensitivity
* Random Forest selected due to:

  * Non-linear learning capability
  * Feature interaction handling
  * Robust performance on tabular data

---

## 📊 Feature Importance (Key Findings)

Top contributing features:

1. MemoryComplaints
2. ADL
3. MMSE
4. DifficultyCompletingTasks

---

## ⚠️ Key Observations

* Lifestyle factors alone are insufficient predictors
* Cognitive decline signals are dominant
* Dataset is **synthetic**, so real-world generalization may vary

---

## 🏥 Real-World Implications

This system can be used as:

* Clinical decision-support tool
* Early-stage screening assistant
* Risk prioritization system for healthcare providers

---

## 🧪 Future Improvements

* Implement Gradient Boosting (XGBoost / LightGBM)
* Perform hyperparameter tuning
* Build a real-time prediction interface (Streamlit)
* Integrate real-world datasets for validation

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn

---

## 📌 Conclusion

This project demonstrates that:

> Alzheimer’s diagnosis is more strongly associated with cognitive and functional impairments than lifestyle or cardiovascular factors.

The developed model effectively captures these relationships and provides a reliable framework for diagnosis detection.

---

## 👤 Author

**Jasmin Banu M.**
B.Tech AI & Data Science

---

## ⭐ If you found this project useful, consider giving it a star!


---

