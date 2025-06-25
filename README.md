# Autoencoders_to_Academic_Success

🎓 Student Academic Risk Prediction
📘 Project Overview
The goal of this project is to predict the academic risk of students in higher education by using machine learning models. This is a multi-class classification problem where the target label can be:

Dropout

Enrolled

Graduate

The data originates from a project aimed at reducing academic failure and dropout rates in higher education through early-stage risk detection.


📊 Dataset Description
Instances: Each row represents a student.

Features: Include demographic, academic, socio-economic, and institutional characteristics known at the time of enrollment.

Target Variable: A 3-class categorical variable indicating the academic outcome.

The dataset contains no missing values and all features are well-documented.



🔍 Exploratory Data Analysis (EDA)
Key insights gathered from count plots and feature distributions:



Categorical Feature Observations:
Marital Status: Singles mostly graduated; married and divorced students had a higher dropout rate.

Application Order: First-choice applicants mostly graduated.

Daytime/Evening Attendance: Evening students are more likely to drop out.

Displaced Students: Non-displaced students dropped more; displaced students mostly graduated.

Debtor Status: Debtors had a much higher dropout rate.

Tuition Fee Up-to-date: Students with unpaid fees were more likely to drop out.

Gender: Female students had higher graduation rates.

Scholarship Holder: Scholarship students showed significantly better academic outcomes.



Numerical Feature Observations:
Features with strong class separation:

Curricular units 1st/2nd sem (grade/approved/evaluations):

Dropout students are clustered around 0.

Graduated students are clustered around 13 on grades and approved units.




📌 Feature Engineering
✅ Removed Features (due to high correlation):

Curricular units 1st sem (grade)

Curricular units 1st sem (credited)

Curricular units 1st sem (enrolled)

Curricular units 1st sem (evaluations)

Curricular units 2nd sem (approved)




🧬 Dimensionality Reduction with Autoencoder
Applied Autoencoder only on continuous features (excluding categorical features).

Scaled features before reduction.

Reduced dimensions from 13 to 4.

Successfully preserved structural integrity (as shown in reconstruction plot).

![image](https://github.com/user-attachments/assets/6f46e807-8463-4bda-819d-e3881f681f55)




🧠 Models Used
🔷 1. XGBoost Classifier
⏱ Training Time: ~608 seconds

✅ Validation Accuracy: 78.84%

🔶 2. Feed Forward Neural Network (FFNN)
⏱ Training Time: ~448 seconds

✅ Validation Accuracy: 79.29%




💡 Conclusion
Both XGBoost and Feed Forward Neural Network models achieved high accuracy. The insights from EDA strongly align with the model behavior, showing the importance of academic performance and socio-economic factors in predicting student outcomes.
