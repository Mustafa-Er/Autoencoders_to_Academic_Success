# 🎓 Student Academic Risk Prediction

## 📘 Project Overview

The goal of this project is to **predict the academic risk of students** in higher education using machine learning.  
This is a **multi-class classification** problem where the target label can be:

- `Dropout`
- `Enrolled`
- `Graduate`

The data originates from a project aimed at reducing academic failure and dropout rates through early-stage risk detection and intervention.

---

## 📊 Dataset Description

- **Instances**: Each row represents a student.
- **Features**: Demographic, academic, socio-economic, and institutional characteristics known at enrollment.
- **Target Variable**: A 3-class categorical variable representing the academic outcome.
- ✅ No missing values — all features are clean and well-documented.

---

## 🔍 Exploratory Data Analysis (EDA)

### 🧩 Categorical Feature Insights

- **Marital Status**: Singles mostly graduated; married/divorced students had higher dropout rates.
- **Application Order**: First-choice applicants mostly graduated.
- **Attendance Time**: Evening students are more likely to drop out.
- **Displaced Students**: Displaced students mostly graduated.
- **Debtor Status**: Debtors showed significantly higher dropout risk.
- **Tuition Payment**: Unpaid tuition correlated with dropout.
- **Gender**: Female students had higher graduation rates.
- **Scholarship Holders**: Significantly better academic performance.

### 📈 Numerical Feature Insights

- **Curricular Units (1st/2nd Semester)**:
  - Dropout students clustered near `0` on grades/approvals.
  - Graduated students clustered near `13`.

---

## 📌 Feature Engineering

### ✅ Removed Highly Correlated Features:

| Removed Feature                        | Reason         |
|----------------------------------------|----------------|
| Curricular units 1st sem (grade)       | High correlation |
| Curricular units 1st sem (credited)    | High correlation |
| Curricular units 1st sem (enrolled)    | High correlation |
| Curricular units 1st sem (evaluations) | High correlation |
| Curricular units 2nd sem (approved)    | High correlation |

---

## 🧬 Dimensionality Reduction with Autoencoder

- Applied on **continuous features** only.
- Features were **scaled** before input to the autoencoder.
- Reduced **13 dimensions to 4**.
- Structure and variance were preserved, as validated by reconstruction error plots.

![Autoencoder Reconstruction](https://github.com/user-attachments/assets/6f46e807-8463-4bda-819d-e3881f681f55)

---

## 🧠 Models Used

| **Model**                    | **Training Time** | **Validation Accuracy** |
|------------------------------|-------------------|--------------------------|
| XGBoost Classifier           | ~608 seconds      | **78.84%**               |
| Feed Forward Neural Network  | ~448 seconds      | **79.29%**               |

---

## 💡 Conclusion

Both **XGBoost** and the **Feed Forward Neural Network** achieved high validation accuracy, confirming the strength of the features and preprocessing.  
Insights from EDA, such as academic performance and socio-economic indicators, were strongly aligned with model predictions, showing their importance in predicting student academic outcomes.

---

Let me know if you'd like to add model training code, a confusion matrix, or performance plots!

