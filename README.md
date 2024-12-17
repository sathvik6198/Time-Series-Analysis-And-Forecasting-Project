# Time Series Analysis and Forecasting Project  
**MA 641: Time Series Analysis**  
**Author**: Sathvik Vadlapatla  
**Year**: 2024  

---

## 📋 **Project Overview**  
This project involves time series analysis and forecasting of **seasonal** and **non-seasonal** data using ARIMA and SARIMA models.  

### **Datasets**:  
1. **Seasonal Data**:  
   - **Dataset**: Monthly electric car sales in the USA.  
   - **Source**: Flourish Visualizations (via Kaggle).  
   - **Objective**: Analyze and forecast monthly sales to identify trends and seasonality.  

2. **Non-Seasonal Data**:  
   - **Dataset**: Yahoo Finance daily stock closing prices over 5 years.  
   - **Source**: Yahoo Finance (via Kaggle).  
   - **Objective**: Analyze and forecast stock prices while accounting for trends and volatility.  

---

## ⚙️ **Tools and Libraries Used**  
- **Programming Language**: R  
- **Key Libraries**:  
   - `forecast` for ARIMA modeling  
   - `tseries` for stationarity tests  
   - `ggplot2` for visualizations  
   - `tidyverse` for data wrangling  

---

## 🛠️ **Methodology**  

### 1. **Data Preprocessing**  
- For **seasonal data**: Missing values were imputed using forward-filling.  
- For **non-seasonal data**: Data was clean with no missing values or outliers.  

### 2. **Stationarity Check**  
- Conducted **Augmented Dickey-Fuller (ADF) Test** to determine stationarity.  
   - If non-stationary, differencing was applied to stabilize the mean.  

### 3. **Model Selection**  
- **Seasonal Data**: Selected an **ARIMA(2,2,2)** model based on AIC minimization and residual diagnostics.  
- **Non-Seasonal Data**: Chose **ARIMA(5,1,2)** with drift using `auto.arima()`.  

### 4. **Forecasting**  
- Forecasted:  
   - **Next 12 months** for electric car sales.  
   - **Next 30 days** for stock prices.  
- Visualized predictions with **confidence intervals** (80% and 95%).  

---

## 📈 **Results**  

### 1. **Seasonal Data: Electric Car Sales**  
- **Model**: ARIMA(2,2,2)  
- **Metrics**:  
   - AIC: 1453.38  
   - RMSE: 26,061.1  
- **Forecast**: Predicted steady growth in electric car sales with seasonal peaks.  

### 2. **Non-Seasonal Data: Yahoo Stock Prices**  
- **Model**: ARIMA(5,1,2) with drift  
- **Metrics**:  
   - AIC: 17,173.57  
   - RMSE: 26.67  
   - MAPE: 0.529%  
- **Forecast**: Stock prices show a slight upward trend with low volatility over the next 30 days.  

---

## 🗂️ **Project Files**  
| File Name                   | Description                                   |  
|-----------------------------|-----------------------------------------------|  
| `MA_641_Project_Report.pdf` | Final project report summarizing the analysis |  
| `electric_car_sales.R`      | R script for seasonal data analysis           |  
| `yahoo_stock_prices.R`      | R script for non-seasonal data analysis       |  
| `Electric_Car_Sales.csv`    | Dataset for electric car sales                |  
| `Yahoo_Stock_Prices.csv`    | Dataset for Yahoo stock prices                |  

---

## 📊 **Visualizations**  
1. **Electric Car Sales**:  
   - Trend, seasonality, and residual decomposition plots.  
   - Forecast plot with confidence intervals.  

2. **Yahoo Stock Prices**:  
   - Time series plot for closing prices.  
   - Forecast plot showing predicted values and uncertainty range.  

---

## 🔍 **Conclusions**  
- **Seasonal Data**: The analysis predicts consistent growth in electric car sales, reflecting increasing adoption.  
- **Non-Seasonal Data**: The forecast suggests stable stock prices with minor upward movement.  

---

## 📚 **References**  
- Box, Jenkins, and Reinsel: *Time Series Analysis: Forecasting and Control*.  
- Data Sources:  
   - [Flourish Visualization (Kaggle)](https://kaggle.com)  
   - [Yahoo Finance](https://finance.yahoo.com)  

---
