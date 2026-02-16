# 🌲🔥 Day 24 – Forest Fire Prediction

## 📌 Project Overview
Forest fires pose a significant threat to ecosystems, wildlife, and human life.  
This project aims to **predict the occurrence of forest fires** using environmental, meteorological, and fuel moisture indicators through machine learning.

The focus is on building a **classification model** that can assist in early warning systems and forest management decisions.

---

## 📊 Dataset Description
The dataset contains environmental and fire-related attributes, including:

- **Weather features:** Temperature, relative humidity, wind speed, rainfall
- **Fire indices:** FFMC, DMC, DC, ISI
- **Spatial features:** X and Y coordinates
- **Temporal features:** Month and day
- **Target:** Burned area (converted into binary fire occurrence)

Target variable:
- `fire = 0` → No fire
- `fire = 1` → Fire occurred

---

## 🎯 Objectives
- Analyze environmental conditions leading to forest fires
- Perform detailed exploratory data analysis (EDA)
- Build a machine learning model to predict fire occurrence
- Identify the most important factors contributing to fires

---

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## 🔍 Exploratory Data Analysis (EDA)

Key analyses performed:
- Fire vs No-Fire distribution
- Temperature, humidity, wind, and rainfall vs fire occurrence
- Monthly fire probability analysis
- Spatial distribution of fires
- Correlation heatmap of numeric features

### 🔑 Key EDA Insights
- Fires are more frequent during dry months (especially August)
- Higher temperature and lower humidity significantly increase fire risk
- Rainfall is mostly zero, offering limited short-term suppression
- Certain spatial regions show higher fire concentration

---

## 🤖 Model Building

### Approach
- Converted burned area into a binary classification problem
- Train-test split with stratification
- Random Forest Classifier used as the primary model

### Evaluation Metrics
- Accuracy
- Precision, Recall, F1-score
- ROC-AUC score

### Model Performance
- **Accuracy:** ~62%
- **ROC-AUC:** ~0.71

This performance is reasonable given the complexity and variability of environmental data.

---

## 🌟 Feature Importance

Top contributing features:
1. Temperature
2. Relative Humidity
3. Drought Code (DC)
4. Duff Moisture Code (DMC)
5. Initial Spread Index (ISI)
6. Wind Speed

These results align well with real-world fire behavior and environmental science.

---

## 📌 Key Conclusions
- Temperature and humidity are the strongest predictors of forest fires
- Fire indices provide more predictive power than raw weather variables alone
- Spatial and seasonal patterns play an important role
- Forest fire prediction is a recall-sensitive and challenging task

---

## 🚀 Future Improvements
- Handle class imbalance using SMOTE
- Hyperparameter tuning for better recall
- Try Gradient Boosting / XGBoost
- Deploy the model as a web app for real-time prediction

---
