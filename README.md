# Predicting Student Attrition Using Behavioural Analytics
**A Comparative Study of Machine Learning Algorithms**

### 👥 Authors
* **Aman**
* **Rohan Dhiman**
* **Rohit Thakur**
* *Institution:* Lovely Professional University, Phagwara, Punjab

---

## 📌 Project Overview
Student retention is a critical performance indicator for higher education institutions. Traditional predictive models often rely heavily on static demographic data (e.g., background, income), which fails to capture the dynamic academic trajectory of a student.

This project presents a machine learning-based decision support system aimed at predicting student dropout risk. By utilizing a dataset of **4,424 undergraduates** and implementing novel **Behavioral Feature Engineering** (specifically focusing on "Academic Efficiency" and "Struggle Ratios"), we successfully transformed complex educational data into a linearly separable problem.

### 🎯 Key Objectives
1.  **Prediction:** Classify students into **Dropout** or **Graduate** categories.
2.  **Innovation:** Engineer **Behavioral Ratios** that outperform raw data by providing context to student efforts.
3.  **Optimization:** Prioritize **Recall** to minimize False Negatives (identifying at-risk students before they leave).

---

## ⚙️ Feature Engineering Strategy
We hypothesized that raw numbers (e.g., "Passed 3 exams") are misleading without context. We derived four novel features to capture student behavior:

### 1. Academic Efficiency (Approval Rate)
Instead of counting passed exams, we calculate the rate of success.
$$Approval Rate = \frac{Curricular Units Approved}{Curricular Units Enrolled}$$
*Rationale:* A student passing 2/2 courses (100%) is essentially safer than one passing 4/8 courses (50%).

### 2. The Struggle Ratio
$$Struggle Ratio = \frac{Evaluations Taken}{Units Approved}$$
*Rationale:* Identifies students who attend many exams (high effort) but fail to pass (low result). A high ratio is a primary indicator of academic burnout.

### 3. Financial Pressure Index
$$Risk = Debtor + (1 - Tuition Paid)$$
*Rationale:* Combines debt status and tuition payment lags into a single distress signal.

### 4. Grade Trend (Momentum)
$$Trend = Sem2 Grade - Sem1 Grade$$
*Rationale:* Captures whether a student is adapting to university life (positive trend) or disengaging (negative trend).

---

## 📊 Experimental Results
We compared three supervised learning algorithms. Contrary to the initial hypothesis that complex ensemble methods would dominate, the robust feature engineering allowed the simpler Logistic Regression model to perform best.

| Algorithm | Accuracy | Recall (Dropout) | Precision | AUC Score |
| :--- | :--- | :--- | :--- | :--- |
| **Logistic Regression** | **91.46%** | **0.89** | **0.92** | **0.96** |
| Random Forest | 90.63% | 0.86 | 0.93 | 0.95 |
| Decision Tree | 87.74% | 0.85 | 0.89 | 0.87 |

### Key Findings
* **Logistic Regression** achieved the highest accuracy (**91.46%**) and best Recall (**0.89**).
* **Feature Importance:** The top predictors were the engineered **Sem2 Approval Rate** and **Struggle Ratio**, proving that behavioral ratios are more predictive than static demographics.
* **Generalization:** The model showed negligible overfitting (0.17% gap between Training and Testing accuracy).

---

## 🛠️ Technologies Used
* **Language:** Python
* **Libraries:** Scikit-learn, Pandas, NumPy, Matplotlib/Seaborn
* **Environment:** Jupyter Notebook

---

## 🚀 Future Scope
* **Dashboard Deployment:** Develop a web-based dashboard using **Streamlit** for University Administrators to visualize risk in real-time.
* **Automated Intervention:** Integration with university email systems to automatically send support resources to students flagged with a "High Struggle Ratio."

---

## 📚 Acknowledgments & References
**Guidance:**
Special thanks to **Geetika Sethi** for guiding the statistical validation phase, specifically regarding the prioritization of Recall over Accuracy.

**Data Source:**
* V. Realinho, J. Machado, L. Baptista, and M. V. Martins, "Predict Students' Dropout and Academic Success," *Data*, vol. 6, no. 11, p. 146, 2021.
* Dataset provided by the **Polytechnic Institute of Portalegre**.
