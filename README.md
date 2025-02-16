# 📊 Forecasting Energy Availability from Renewable Sources

## 📌 Project Overview
This project aims to predict surplus energy availability from **renewable sources (solar & wind)** to optimize energy distribution and notify local residents in advance. Using time series forecasting techniques and deep learning models, we analyze energy trends and develop an AI-driven **Multi-Output LSTM model** for accurate predictions.

## ⚡ Business Context
**Company:** Energy Provider  
**Service:** Renewable Energy Surplus Alerts  
**Target Audience:** Local residents near solar and wind farms  
**Objective:**  
✅ Predict energy surplus **24 hours in advance**  
✅ Provide **free energy during surplus periods**  
✅ Notify clients in advance for opt-in participation  

---

## 📂 Project Structure
- **`data_exploration.ipynb`** → Data preprocessing & exploratory data analysis (EDA)  
- **`modeling.ipynb`** → Machine learning model training & evaluation  
- **`README.md`** → Project documentation  

---

## 🔍 Data Exploration & Preprocessing
### 🗂 Dataset Information
- **Location:** Brighton (Primary), Colchester (For validation)
- **Time Range:** Historical energy data from 2000 to recent years
- **Features:**
  - **Solar Energy (Wh) & Wind Speed (m/s)** → Key predictors
  - **Temporal Variables** → Hourly, daily, seasonal trends
  - **Weather Features** → Air temperature, humidity, etc.
  
### 🛠 Data Cleaning & Handling Missing Values
✔️ Filled missing values using previous year's data (seasonal assumption)  
✔️ Standardized & normalized data for model input  
✔️ Identified temporal patterns using **Autocorrelation (ACF) & Partial Autocorrelation (PACF)**  

### 📊 Key Insights from EDA
- Solar energy exhibits **daily fluctuations** with peak production at midday.
- Wind speed is **more variable**, showing **seasonal trends**.
- ACF & PACF indicate **strong periodicity**, validating time-series modeling.

---

## 🤖 Modeling Approach
### 📌 Selected Model: **Multi-Output LSTM (MO-LSTM)**
- **Why?** Unlike traditional LSTMs, MO-LSTM predicts multiple outputs (**solar & wind energy**) simultaneously.
- **Training:**
  - Input: Historical energy & weather data
  - Output: Forecasted **solar & wind energy** for the next 24 hours
- **Evaluation:** Mean Absolute Error (MAE) & Visualization of predictions

### 🚀 Results
📉 **Low MAE**, indicating strong generalization performance.  
⚡ **Successful prediction of energy surplus periods**, making real-time notifications feasible.  

---

## 📌 Key Findings & Recommendations
✅ **Accurate Forecasting:** Reliable energy surplus predictions enable efficient energy distribution.  
✅ **Cost-Effective Solution:** Free energy distribution during surplus enhances customer satisfaction.  
✅ **Scalability:** The model can be extended to multiple cities using cloud-based deployment.  

---

## 🔗 Future Enhancements
🚀 Improve real-time data ingestion from IoT sensors.  
🌍 Expand the model to integrate **real-time weather forecasting**.  
☁️ Deploy model on **Azure/AWS for live inference**.  
