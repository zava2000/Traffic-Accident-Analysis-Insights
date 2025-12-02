# 🚦 Traffic-Accident-Analysis-Insights  
### A Data-Driven Approach to Public Safety & Risk Management

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Library](https://img.shields.io/badge/Library-Pandas-150458)
![Status](https://img.shields.io/badge/Status-Completed-green)

---

## 📌 What This Project Demonstrates  
This project showcases advanced skills in:

- **Exploratory Data Analysis (EDA)** on large datasets  
- **Feature engineering & pattern discovery**  
- **Correlation and risk-factor quantification**  
- **Predictive modeling for classification (Logistic Regression)**  
- **Data storytelling & actionable insights for real-world decision-making**

Perfect for Data Analyst, Data Scientist and Risk Analytics roles.

---

## 📋 Executive Summary  
The objective of this project is to **analyze historical traffic accident data** to determine how environmental, temporal, behavioral, and infrastructural factors influence crash occurrence and injury severity.

Insights were translated into **practical recommendations for transportation safety officials**, enabling data-driven policies to reduce injuries and fatalities.

A **baseline predictive model** was developed to quantify the strength of identified risk factors and validate their statistical significance.

---

## 🧠 Key Insights & Safety Implications  

![Top Factors](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Top%2020%20Factors.png)

### **Actionable Takeaways**
1. **The "Ideal Conditions" Paradox**  
   Over **79%** of accidents occur under clear weather and dry road conditions. Human behavior—not external conditions—is the dominant risk factor.

2. **Intersections Are the Core Danger Zone**  
   **95.2%** of accidents occur at intersections. The infrastructure is stable; the issue is decision-making complexity.

3. **Vulnerable Road Users Drive Severity**  
   Pedestrian (+0.33) and cyclist (+0.19) involvement are the strongest predictors of critical injury.

4. **Temporal Predictability**  
   Accident risk peaks during **15:00–18:00** and on **Fridays**, consistent with fatigue + traffic density dynamics.

---

## 📄 Dataset Overview  
- **Size:** 209 306 rows × 24 columns  
- **Source:** Kaggle — Traffic Accidents dataset  
- **Target Variable:** injury/accident severity (or damage level)  
- **Data Types:** temporal, environmental, infrastructure, crash mechanics, human/behavioral factors  

---

## 📊 Exploratory Data Analysis (EDA)

## 🕓 Temporal Patterns — When Do Crashes Happen?  
![Temporal Features](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Image%201.png)

## 🏗️ Infrastructure & Location  
![Infrastructure](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Image%203.png)

## 🌤️ Environmental Conditions  
![Environmental Conditions](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Image%202.png)

## 🔧 Crash Mechanics  
![Crash Mechanics](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Image%204.png)

---

## 📈 Predictive Model Performance  
A **Logistic Regression** model was built using `class_weight='balanced'` to address class imbalance.

| Metric | Score | Interpretation |
| --- | --- | --- |
| **Recall (Severe)** | **0.96** | Captures 96% of severe/fatal injury cases. |
| **ROC-AUC** | **0.86** | Strong discrimination between high-risk and low-risk scenarios. |
| **Precision** | **0.08** | High false-alarm rate, acceptable for safety-first applications. |

---

## 🧰 Technologies Used  
- **Python**  
- **Pandas, NumPy**  
- **Matplotlib, Seaborn**  
- **Scikit-learn** (Logistic Regression, Random Forest)  
- **Jupyter Notebook**
