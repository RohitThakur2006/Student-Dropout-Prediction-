# Predicting Student Attrition Using Behavioural Analytics
**A Comparative Study of Machine Learning Algorithms**

### 👥 Authors
* [cite_start]**Aman** - Lovely Professional University [cite: 2, 3]
* [cite_start]**Rohan Dhiman** - Lovely Professional University [cite: 2, 3]
* [cite_start]**Rohit Thakur** - Lovely Professional University [cite: 2, 3]

---

## 📌 Overview
Student retention is a critical performance indicator for higher education institutions. [cite_start]Traditional predictive models rely on static demographic data, which fails to capture a student's dynamic academic trajectory[cite: 6, 7].

This project presents a machine learning-based decision support system that predicts dropout risk. [cite_start]By utilizing a dataset of **4,424 undergraduates** and implementing novel **Behavioral Feature Engineering** (such as "Academic Efficiency" and "Struggle Ratios"), we transformed complex educational data into a linearly separable problem[cite: 9, 12].

## 🎯 Key Objectives
1.  [cite_start]**Prediction:** Classify students into **Dropout** or **Graduate** categories[cite: 20].
2.  [cite_start]**Innovation:** Engineer **Behavioral Ratios** (e.g., Effort vs. Result) that outperform raw data[cite: 21].
3.  [cite_start]**Optimization:** Prioritize **Recall** to minimize False Negatives (missed at-risk students)[cite: 22].

---

## ⚙️ Methodology & Feature Engineering
We moved beyond raw numbers (like "exams passed") to understand the *context* of student behavior. The key engineered features included:

* [cite_start]**Academic Efficiency (Approval Rate):** $\frac{Units Approved}{Units Enrolled}$ — Measures success rate rather than volume[cite: 47, 49].
* [cite_start]**Struggle Ratio:** $\frac{Evaluations Taken}{Units Approved}$ — Identifies students putting in high effort but achieving low results (burnout indicator)[cite: 51, 52].
* [cite_start]**Financial Pressure Index:** Combines scholarship status and tuition payment lags[cite: 55].
* [cite_start]**Grade Trend:** Captures the momentum between Semester 1 and Semester 2 grades[cite: 58].

---

## 📊 Model Performance
We compared three algorithms: **Logistic Regression**, **Decision Tree (CART)**, and **Random Forest**.

| Algorithm | Accuracy | Recall (Dropout) | AUC Score |
| :--- | :--- | :--- | :--- |
| **Logistic Regression** | **91.46%** | **0.89** | **0.96** |
| Random Forest | 90.63% | 0.86 | 0.95 |
| Decision Tree | 87.74% | 0.85 | 0.87 |

[cite_start]*Table Data Source: [cite: 76]*

[cite_start]**Key Finding:** Logistic Regression achieved the highest accuracy (91.46%) and Recall (0.89), proving that robust feature engineering can allow simpler models to outperform complex ensemble methods[cite: 11, 12].

---

## 🚀 Future Scope
* [cite_start]**Deployment:** Building a dashboard using **Streamlit** for University Administrators[cite: 104].
* [cite_start]**Intervention:** Integration with university systems to automate support emails for students with high "Struggle Ratios"[cite: 105].

## 📚 Data Source
[cite_start]The dataset was sourced from the **Polytechnic Institute of Portalegre**[cite: 33].
* *Reference:* V. Realinho, J. Machado, L. Baptista, and M. V. Martins, "Predict Students' Dropout and Academic Success," Data, vol. 6, no. 11, p. [cite_start]146, 2021[cite: 110].

---
*Project conducted at Lovely Professional University, Phagwara, Punjab.*
