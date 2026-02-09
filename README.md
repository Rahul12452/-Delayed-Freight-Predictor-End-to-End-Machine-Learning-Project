# 🚢 Delayed Freight Predictor – End-to-End Machine Learning Project

📦 **Predicting shipment delay days using historical freight data, feature engineering, and machine learning**
⚡ Built a complete **EDA → Modeling → Tuning → Explainability** pipeline using Python & Jupyter Notebook to deliver actionable logistics insights

---

## 🚀 Project Overview

📌 An end-to-end machine learning project using **5,000 historical freight shipment records**
📌 Covers **data cleaning, exploratory analysis, feature engineering, model training, tuning, and explainability**
📌 **Goal:** Predict shipment delay days accurately and identify key delay drivers to support proactive logistics planning

---

## 🎯 Objectives

✔ Predict freight **delay days** with high accuracy
✔ Understand the **impact of weather, congestion, distance, and cargo type**
✔ Compare multiple ML models and select the best performer
✔ Improve model performance using **hyperparameter tuning**
✔ Explain predictions using **SHAP for business interpretability**
✔ Provide **real-world logistics recommendations**

---

## 📊 Dataset Summary

* **Records:** 5,000 freight shipments
* **Features include:**

  * Origin Region, Carrier Name, Cargo Type
  * Planned ETA vs Actual Arrival
  * Weather Index
  * Port Congestion Level
  * Distance (KM)

### 🎯 Target Variables

* `Delay_Days` → Number of days shipment was delayed
* `Delayed` → Binary indicator (Delayed / On-time)

---

## 📊 Scope of Analysis

🟡 Delay distribution and extreme delay analysis
🟡 Distance vs delay relationship
🟡 Delay patterns by cargo type
🟡 Weather and port congestion impact
🟡 Correlation analysis of numerical variables
🟡 Feature engineering and interaction effects
🟡 Model comparison and explainability

---

## 🔧 Tools & Technologies

**Python**

* **Data Analysis:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:**

  * Linear Regression, Ridge Regression
  * Random Forest Regressor
  * Gradient Boosting Regressor
  * XGBoost Regressor
  * LightGBM Regressor
* **Model Evaluation:** MAE, RMSE, R² Score
* **Hyperparameter Tuning:** RandomizedSearchCV
* **Explainability:** SHAP
* **Environment:** Jupyter Notebook

---

## 📈 Key Features

📌 End-to-end Exploratory Data Analysis (EDA)
📌 Feature engineering (time-based, distance buckets, interaction features)
📌 Baseline and advanced ML model comparison
📌 Hyperparameter tuning for Random Forest, XGBoost, and Ridge Regression
📌 SHAP-based global feature importance analysis
📌 Business-focused insights and recommendations

---

## 🤖 Model Performance Summary

| Model                    | MAE       | RMSE      | R²        |
| ------------------------ | --------- | --------- | --------- |
| Linear Regression        | ~2.12     | ~2.60     | ~0.52     |
| Ridge Regression (Tuned) | ~2.12     | ~2.60     | ~0.52     |
| Random Forest (Tuned)    | ~2.19     | ~2.65     | ~0.50     |
| Gradient Boosting        | ~2.23     | ~2.73     | ~0.47     |
| LightGBM                 | ~2.19     | ~2.71     | ~0.48     |
| **XGBoost (Tuned)** ⭐    | **~2.12** | **~2.61** | **~0.52** |

👉 **Best Performing Model:** Tuned XGBoost
👉 **Average prediction error:** ~±2 days

---

## 🔍 Model Explainability (SHAP)

SHAP analysis identifies the **key contributors to shipment delays**:

🔹 Weather Index
🔹 Port Congestion Level
🔹 Hazardous Cargo Type
🔹 Distance (KM)
🔹 ETA Month and Weekday
🔹 Congestion × Weather interaction

This ensures the model is **transparent, interpretable, and business-ready**.

---

## 📉 Major Insights

🔹 Severe weather significantly increases delay risk
🔹 Port congestion is a strong predictor of late arrivals
🔹 Hazardous and fragile cargo face higher delays
🔹 Distance alone does not cause delay, but amplifies risk
🔹 Combined congestion and weather effects drive extreme delays

---

## 📌 Business Recommendations

✔ Use weather and congestion indicators for **early delay alerts**
✔ Add buffer time for hazardous and long-distance shipments
✔ Reroute shipments during high congestion + bad weather
✔ Reduce detention and penalty costs through predictive planning
✔ Integrate model into dashboards or APIs for real-time usage

---

## 🚀 Outcomes

✨ Delivered a complete **end-to-end machine learning project**
📊 Achieved reliable delay predictions with ~2-day average error
🔍 Built explainable ML using SHAP
📈 Portfolio-ready project demonstrating real-world logistics impact

---

## 🔮 Limitations & Future Enhancements

* Incorporate external data (holidays, real-time weather, carrier history)
* Apply cross-validation for more robust evaluation
* Explore ensemble stacking techniques
* Deploy using **Flask API** or **Streamlit dashboard**
* Integrate with live supply-chain systems

---

## 📌 Conclusion

The **Delayed Freight Predictor** demonstrates a complete machine learning workflow — from raw logistics data to an **interpretable, tuned, and business-impactful predictive model**.

🚚 *Designed to solve real-world supply chain delay challenges.*
