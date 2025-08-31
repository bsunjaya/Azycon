# Azycon

# Allianz Datathon 2025 – Ski Resort Visitation Forecasting
This repository contains the workflow and models developed for the **Allianz Datathon 2025**, focusing on **ski resort visitation prediction** based on weather, snow reliability index (SRI), and other factors.  

The project is organized into **three main phases**:
1. **Exploratory Data Analysis (EDA) & Visualization**
2. **Model Development for Weather & SRI Forecasting**
3. **Visitor Forecasting with Prophet**
4. **Stack model**
---

## 📂 Repository Structure

## Notebook Overview
### **1. Exploratory Data Analysis (EDA)**
- **`001A_EDA.ipynb`**  
  Initial exploratory data analysis (EDA) on meteorology, visitation, and SRI datasets.  
  Focuses on data cleaning, understanding key distributions, and identifying trends.

- **`001B_GraphForPopularWeek.ipynb`**  
  Graphical analysis of **popular ski weeks** across resorts.  
  Helps identify high-demand periods and seasonal visitation patterns.

---

### **2. Forecasting Weather & Snow Reliability Index (SRI)**
- **`002A_weather_ES_RF.ipynb`**  
  Models SRI forecasting using:  
  - **Exponential Smoothing (ES)**  
  - **Random Forest (RF)**  

  After evaluation, **Random Forest (RF)** was chosen as the preferred model.

- **`002B_weather_RF_mulvar.ipynb`**  
  Multi-variable Random Forest model to forecast:  
  - **TempMin**  
  - **TempMax**  
  - **Rainfall**  

  These forecasts are used as inputs for downstream visitor prediction.

---

### **3. Visitor Forecasting**
- **`003_prophet_model_visitor.ipynb`**  
  Facebook Prophet model to predict **visitor counts** based on historical visitation data, seasonal patterns, and outputs from the weather & SRI models.

- **`visitor_2025.ipynb`**  
  Visitor prediction workflow for the year 2025.  
  Uses Prophet forecasts combined with meteorology and SRI data.

---

## 📊 Data Sources
- **`2025 Allianz Datathon Dataset.xlsx`** – Primary dataset for the competition.  
- **`Meteorology.xlsx`** – Historical weather data.  
- **`Visitation.xlsx`** – Historical visitation data.  
- **`data_input_SRI.csv`** – Preprocessed input data for SRI modeling.  
- **`visit_data.csv`** – Visitor records for Prophet modeling.

---

## 📈 Outputs
- **`SRI_forecast_2026_ES.csv`** – SRI forecasts using Exponential Smoothing.  
- **`SRI_forecast_2026_RF.csv`** – Final SRI forecasts using Random Forest (selected model).  
- **`rf_forecasts_mulvar.csv`** – Random Forest multi-variable forecasts (TempMin, TempMax, Rainfall).  
- **`outputs/`** – Folder containing plots, graphs, and model results.

---

## 🚀 Workflow Summary
1. Perform **EDA** (trend analysis, popular weeks, correlations).  
2. Forecast **SRI** using ES and RF → select **RF** as the best performer.  
3. Build a **multi-variate RF model** to forecast weather variables.  
4. Use **Prophet** to predict **visitor counts** for 2025+ leveraging weather & SRI predictions.  

---

## 📌 Next Steps
- Improve RF hyperparameter tuning for weather forecasts.  
- Incorporate external tourism/holiday data into visitor prediction.  
- Evaluate ensemble models combining Prophet + ML-based regressors.  

---

## 👥 Contributors
- **Bryan Alfason Sunjaya, Richardo Husni, Hanyi Zhu, Cong Li**  
- Team Azycon for Allianz Datathon 2025  