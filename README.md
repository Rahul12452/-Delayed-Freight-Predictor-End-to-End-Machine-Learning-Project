# 🚚 Delayed Freight Predictor – End-to-End Delay Prediction

An end-to-end **machine learning project** that predicts freight shipment delay days using historical logistics data.  
This project demonstrates the full data science lifecycle — from raw data cleaning and EDA to model training, hyperparameter tuning, and explainability — with a strong focus on **real-world supply chain impact**.

---

## 📌 Project Objective

Freight delays lead to high operational costs such as detention, demurrage, penalties, and customer dissatisfaction.  
The objective of this project is to:

- Predict **shipment delay days** in advance
- Identify **key drivers of freight delays**
- Enable **proactive logistics planning and decision-making**

---

## 📊 Dataset Overview

- **Total Records:** 5,000 shipments  
- **Initial Features:** 9  
- **Target Variable:** `Delay_Days`

### Key Columns
| Feature | Description |
|-------|------------|
| Shipment_ID | Unique shipment identifier |
| Origin_Region | Origin country/region |
| Carrier_Name | Logistics carrier |
| Cargo_Type | Cargo category |
| Planned_ETA | Expected arrival date |
| Actual_Arrival | Actual arrival date |
| Weather_Index | Weather severity indicator |
| Port_Congestion_Level | Port congestion score (0–1) |
| Distance_KM | Shipment distance |

---

## 🧹 Data Cleaning & Preparation

- Handled missing values:
  - Carrier name → `Unknown`
  - Port congestion → Median imputation
- Standardized country names (DE → Germany, CN → China, etc.)
- Converted date columns to `datetime`
- Created target variables:
  - `Delay_Days`
  - `Delayed` (binary indicator)

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights:
- Most shipments are delayed **0–6 days** (average ≈ 4 days)
- **Distance shows weak correlation** with delays
- **Perishable cargo** has the highest delay variability
- Weather and port congestion influence delays but in **non-linear ways**

Visual analyses include:
- Delay distribution
- Delay vs distance
- Delay by cargo type
- Weather & congestion impact
- Correlation heatmap

---

## ⚙️ Feature Engineering

Engineered features to improve model performance:

- **Time-based features:** `ETA_Month`, `ETA_Weekday`, `Weekend`
- **Operational indicators:**
  - `Distance_per_Day` (speed proxy)
  - `Congestion_Weather` (interaction feature)
  - `Severe_Weather` flag
- Distance categorization: Short / Medium / Long

---

## 🧠 Models Implemented

Baseline and advanced regression models:

- Linear Regression
- Ridge Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor
- LightGBM Regressor

### Evaluation Metrics
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## 📈 Model Performance (Before Tuning)

| Model | MAE | RMSE | R² |
|------|----|----|----|
| Linear Regression | 2.12 | 2.60 | 0.519 |
| Ridge Regression | 2.12 | 2.60 | 0.519 |
| Random Forest | 2.16 | 2.68 | 0.490 |
| Gradient Boosting | 2.23 | 2.73 | 0.470 |
| XGBoost | 2.20 | 2.70 | 0.481 |
| LightGBM | 2.19 | 2.71 | 0.477 |

---

## 🔧 Hyperparameter Tuning

Applied **RandomizedSearchCV** to:
- Random Forest
- XGBoost
- Ridge Regression

### Final Tuned Model Comparison

| Model | MAE | RMSE | R² | Rank |
|------|----|----|----|----|
| **Tuned Ridge Regression** | **2.118** | **2.598** | **0.519** | 🥇 |
| Tuned XGBoost | 2.124 | 2.607 | 0.516 | 🥈 |
| Tuned Random Forest | 2.184 | 2.653 | 0.499 | 🥉 |

✅ **Ridge Regression emerged as the best model**, offering strong accuracy, interpretability, and stability.

---

## 🔍 Model Explainability (SHAP)

Used **SHAP** to interpret predictions for:
- Tuned XGBoost
- Tuned Ridge Regression

### Key Delay Drivers
- Distance_per_Day (speed proxy)
- Distance_KM
- Weather_Index
- Port_Congestion_Level
- ETA timing features
- Cargo type indicators

This ensures transparency and trust for business adoption.

---

## 💼 Business Impact

With an average prediction error of **~2.1 days**, the model supports:

- Early delay alerts
- Proactive rerouting & buffer planning
- Improved customer communication

### Potential Outcomes
- ⏱ 15–30% reduction in average delay days
- 💰 Savings of ₹50,000–₹2,00,000 per delayed high-value shipment
- 📈 Higher on-time delivery rate & customer satisfaction
- 🏆 Competitive advantage through predictive logistics

---

## ⚠️ Limitations

- Limited feature set (no holidays, strikes, real-time carrier data)
- Single train-test split
- Historical data only

---

## 🚀 Future Enhancements

- Integrate live APIs (weather, port congestion, carrier performance)
- Implement full cross-validation & ensemble stacking
- Deploy via Flask API or Streamlit dashboard
- Add model monitoring & concept drift detection

---

## 🧠 Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost, LightGBM
- SHAP

---

## 🏁 Final Note

This project demonstrates **end-to-end machine learning applied to a real logistics problem** — transforming raw shipment data into interpretable insights and measurable business value.

