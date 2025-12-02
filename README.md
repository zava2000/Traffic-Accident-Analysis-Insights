# 🚦 Traffic-Accident-Analysis-Insights

### A Data-Driven Approach to Public Safety & Risk Management

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Library](https://img.shields.io/badge/Library-Pandas-150458)
![Status](https://img.shields.io/badge/Status-Completed-green)

---

## 📋 Executive Summary
The primary objective of this project is **to analyze historical traffic accident data** to identify the primary conditions, temporal factors, and causal elements contributing to crash occurrence and injury severity.

The ultimate goal is to generate **actionable insights for transportation safety officials**, enabling evidence-based decision-making to mitigate future traffic risks and fatalities.

While the core focus is diagnostic analysis, a **baseline predictive model** was utilized as a statistical tool to quantify the relative weight of identified risk factors and validate the significance of the findings.

---

## 💡 Key Intelligence Insights
Based on the analysis, we identified the specific factors that influence the risk of severe injury. The analysis highlights which variables have the strongest correlation with accident severity:

![Top Factors](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Top%2020%20Factors.png)

**Actionable Takeaways:**
1.  **The "Ideal Conditions" Paradox:** Over **79% of accidents occur in clear weather** and on dry roads. External factors like rain, snow, or road defects are negligible contributors. The primary risk factor is **human behavior** (inattention, aggression) operating under a false sense of security provided by good conditions.
2.  **Intersections are the Critical Conflict Point:** A staggering **95.2% of crashes are intersection-related**, primarily occurring on straight, level roads controlled by traffic signals. The infrastructure itself is stable, but the complex decision-making required at crossings is where drivers consistently fail.
3.  **Vulnerable Users Drive Severity:** While the vast majority of accidents (74%) result in no injuries (property damage only), the **severity skyrockets** when pedestrians (+0.33 correlation) or cyclists (+0.19 correlation) are involved. These are the single strongest predictors of critical outcomes.
4.  **Temporal Predictability:** Risk is highly predictable, peaking during the **evening rush hour (15:00–18:00)** and on **Fridays**. This correlates strongly with commuter fatigue and traffic density rather than random chance.

---

## 📊 Project Methodology

### 1. Exploratory Data Analysis (EDA)
We utilized **Seaborn** and **Matplotlib** to uncover patterns across multiple dimensions.

#### A. Temporal Analysis: When do crashes happen?
Analysis reveals a distinct peak during the evening rush hour (3 PM - 6 PM) and on Fridays, suggesting commuter fatigue is a major factor.
![Temporal Features](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Image%201.png)

#### B. Infrastructure & Location
The data confirms that road geometry is rarely the issue (most roads are straight and level). The danger lies in **Traffic Control Devices** (signals/stop signs) where conflict points exist.
![Infrastructure](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Image%203.png)

#### C. Environmental Conditions
Most accidents occur under "ideal" conditions (Clear weather, Dry roads, Daylight), indicating that drivers may lower their guard when the environment seems safe.
![Environmental Conditions](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Image%202.png)

#### D. Crash Mechanics
"Turning" and "Angle" collisions are the most common types, reinforcing the finding that intersections are the primary hazard zones.
![Crash Mechanics](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Image%204.png)

### 2. Feature Engineering & Selection
To handle the high dimensionality of the data, we performed One-Hot Encoding and filtered features based on their correlation with the target variable.

**Top 20 Features by Correlation:**
![Feature Selection](https://github.com/zava2000/Traffic-Accident-Analysis-Insights/blob/main/Images/Top%2020%20Factors.png)
*We removed post-crash variables (like 'Ambulance Required') to prevent Data Leakage.*

---

## 📈 Model Performance
We deployed a **Logistic Regression** model with `class_weight='balanced'` to handle the severe class imbalance. The strategy was to prioritize **Recall** (Sensitivity) to create a "Safety Net" model.

| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **Recall (Severe)** | **0.96** | The model correctly identifies **96%** of all severe/fatal injuries. |
| **ROC-AUC** | **0.86** | Strong ability to distinguish between high-risk and low-risk scenarios. |
| **Precision** | **0.08** | Low precision indicates a high false-alarm rate, accepted as a necessary trade-off for safety. |

---

## 🛠️ Technologies Used
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (LogisticRegression, RandomForestClassifier)
* **Environment:** Jupyter Notebook

-----

*This project was developed for educational and portfolio purposes to demonstrate end-to-end data analysis and modeling workflows in the context of Public Safety.*
