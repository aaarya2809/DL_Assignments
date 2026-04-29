# 🧠 Explainable AI in Machine Learning (Titanic Dataset)

## 🚀 Open in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1hdwUX5ih7JST-QjkCEAFa6Al3SyKVB0E?usp=sharing)

👉 You can directly run the notebook using the Colab link above.

---

## 📌 Project Overview

This project implements **Explainable AI (XAI)** techniques on a Machine Learning model to understand how predictions are made.

A **Random Forest Classifier** is trained on the Titanic dataset, and XAI methods such as **SHAP** and **LIME** are used to interpret both global and local model behavior.

---

## 🎯 Objectives

* Understand model transparency
* Apply Explainable AI techniques
* Visualize feature importance
* Detect bias in ML models

---

## 📊 Dataset

* **Name:** Titanic Dataset
* **Source:** https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

### Features:

* Pclass, Sex, Age, SibSp, Parch, Fare, Embarked

### Target:

* Survived (0 = No, 1 = Yes)

---

## ⚙️ Technologies Used

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* SHAP
* LIME

---

## 🔄 Workflow

### 1️⃣ Data Preprocessing

* Handling missing values
* Encoding categorical variables
* Train-test split

### 2️⃣ Model Implementation

* Random Forest Classifier
* Model training and prediction

### 3️⃣ Evaluation

* Accuracy
* Precision
* Recall
* F1-score

---

## 🔍 Explainable AI Techniques

### 🌍 Global Explanation

* Feature Importance
* SHAP Summary Plot
* Permutation Importance

### 🎯 Local Explanation

* LIME Explanation
* SHAP Force Plot

---

## 📊 Visualizations

* Confusion Matrix
* Feature Importance Plot
* SHAP Summary Plot
* SHAP Dependence Plot
* LIME Output
* Correlation Heatmap
* Survival Analysis (Gender, Class, Age)

---

## 📈 Key Insights

* Gender is the most important feature
* Female passengers had higher survival rates
* Higher fare and first-class passengers had better survival chances

---

## ⚠️ Bias Analysis

* Gender bias (female favored)
* Socio-economic bias (higher fare advantage)
* Class bias (first class advantage)

---

## ✅ Results

* Accuracy: ~80–85%
* Model performs well on classification task
* XAI techniques provide clear interpretability

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn scikit-learn shap lime
```

Run the notebook using the Colab link above.

---

## 📁 Project Structure

```
DL_Assignments/
   └── XAI/
        ├── README.md
        ├── XAI.ipynb
```

---

## 👨‍💻 Author

**Aarya Malghe**

---

## 📢 Conclusion

This project demonstrates how Explainable AI improves transparency, interpretability, and trust in Machine Learning models by making predictions understandable.
