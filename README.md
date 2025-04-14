# 🌍 Sierra Leone Maternal & Child Health Analysis

An applied analytics project aimed at identifying gaps in maternal and child health services in Sierra Leone using data from the District Health Information System (DHIS2). We combined statistical forecasting, geospatial mapping, and deep learning to analyze coverage, trends, and facility performance across districts.

## 📌 Project Scope

This project explores various public health metrics in Sierra Leone—one of the most affected countries by maternal and child mortality. Using DHIS2 data from 2022–2023, we focused on:

- ANC IPT coverage (malaria preventive treatment during pregnancy)
- Severe and moderate malnutrition rates
- Measles vaccination coverage
- Births attended by skilled personnel

---

## 📊 Key Results

### ✅ Forecasting & Trend Insights
- **ANC IPT 1 vs IPT 2**: Trendlines show no convergence between coverage of first and second doses across the country. **ARIMA models** suggest the gap is widening.
- **SES Forecast** (Western Area): α = 0.1 gave more accurate predictions than α = 0.8, forecasting IPT 2 coverage at **131.2** with **MAE: 56.2**.
  
### 🧠 Deep Learning
- Used **Inception ResNet V2** to analyze monthly **choropleth maps** and predict malnutrition severity in Bo District.
- Achieved **75% accuracy**, **100% recall**, and an **F1 score of 85.7%** for the ‘3–6’ malnutrition category using image-based classification.

### 💉 Measles Coverage
- National level: **<60% target missed** in nearly all months.
- **Urban areas (25.5%) outperformed rural areas (18.9%)**, highlighting a critical accessibility gap.
- Facility-level drilldowns show **CHCs and hospitals outperform MCHPs**, which are often underrepresented in data.

---

## 🧪 Methodology

1. **Data Source**: DHIS2 – national health system for Sierra Leone  
2. **Tools**: R (ggplot2, timeSeries), Python (TensorFlow, OpenCV), GIS layers (Google Maps, Bing Roads)  
3. **Statistical Methods**:  
   - Time Series (ARIMA, SES)  
   - Logistic Regression & Error Metrics (RMSE, MAE)  
   - Non-parametric correlation (Spearman, Kendall)  
4. **Deep Learning**:  
   - Transfer learning with Inception ResNet V2  
   - Data augmentation, categorical encoding, early stopping  
   - Accuracy and F1-score evaluation  
5. **Data Validation Rules**:
   - ANC IPT2 should never exceed IPT1
   - Measles coverage <1yr must stay under 100%
   - Severe malnutrition must not exceed moderate malnutrition

---

## 📍 Geographic Insights

- **Western Area** (urban, capital region) achieved the best results in most categories
- **Port Loko** had the lowest rate of births attended by skilled personnel, despite proximity to the capital
- **Chiefdoms like Lokomasama, Dibia, Bumpeh**—all within 75mi of the capital—showed elevated malnutrition rates

---

## 📈 Visualization Highlights

- **Time-series trend graphs** for ANC IPT and Measles
- **Choropleth maps** showing district and chiefdom disparities
- **Bar charts** for dropout vs coverage rates by district

---

## 📉 Data Quality & Limitations

- Missing data from key facility types (e.g., MCHPs) may have skewed regional comparisons
- Inconsistent reporting (e.g., IPT2 > IPT1) suggests data entry or system limitations
- Some predictions are subject to limited training data in deep learning module

---

## 👥 Team Members

- Kruthika Gaddam  
- Bekezela Kusina  
- Megha Moncy  
- Sahiti Somalraju  
- Shikhar Shukla

---

## 📄 References

Anchang-Kimbi, J.K., et al. (2014). Antenatal care and IPTp attendance. *Malaria Journal*.  
Babughirana, G., et al. (2018). Assessment of CHWs readiness in Bo District. *American Journal of Computer Science and IT*.

