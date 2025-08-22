# 🏥 HealthData IQ – Hospital Insights & Patient Analytics

**Analyze hospital performance and patient feedback across the United States using CMS data. Gain actionable insights into hospital quality, patient experience, emergency services, and ownership types.**

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/) [![Pandas](https://img.shields.io/badge/Pandas-1.5-green)](https://pandas.pydata.org/) [![Plotly](https://img.shields.io/badge/Plotly-5-orange)](https://plotly.com/) [![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

---

## 🔗 Dataset
**Source:** [Kaggle – Hospital General Information](https://www.kaggle.com/datasets/CMS/hospital-general-information)  

**Key Columns:**  
- Hospital Name  
- Type & Ownership  
- Ratings & Patient Survey Results  
- Emergency Services  
- Mortality, Readmission, Safety Metrics  
- Location (State, ZIP, County)

**Primary Focus:**  
- Hospital types & ownership  
- Overall ratings & patient experience  
- Emergency service availability  
- Quality metrics & performance comparison

---

## 🧹 Data Cleaning

- Removed rows with missing `County Name`  
- Dropped `Meets criteria for meaningful use of EHRs` and footnote columns (high missing values)  
- Converted categorical comparison columns (e.g., "Above the national average") to **ordinal numeric scores**  
- Standardized `Hospital overall rating` to numeric  
- Fixed inconsistent values and missing data  

---

## 🔍 Exploratory Data Analysis (EDA)

### Hospital Type & Ownership
- Most hospitals are **Acute Care Hospitals** (skewed distribution)  
- Common ownership: **Voluntary non-profit – Private** & **Proprietary**

### Ratings by Ownership
- Median hospital rating ~3 across most ownership types  
- `Physician-owned` hospitals show slightly higher median  
- Missing ratings (`Not Available`) affect comparison reliability  

### Emergency Services
- High availability in states with the most hospitals (e.g., **TX, CA**)  
- Majority of hospitals offer **emergency services**

### Patient Experience
- Most hospitals rated **"Same as the national average"**

### Correlation Analysis
- Weak correlation between `Hospital overall rating`, `ZIP Code`, and `Phone Number`  
- Heatmap of ratings vs quality metrics shows independent indicators  

### Mortality Comparison
- Most hospitals: `"Same as the national average"`  
- Significant counts for `"Below"` and `"Above"` average  

### Chi-Square Test: Hospital Type vs Patient Experience
- **Chi-Square Statistic:** 1831.28  
- **P-Value:** 0.0000  
- **Conclusion:** Significant association between hospital type and patient experience ratings  

---

## 📊 Visualizations

- **Histogram:** Rating distributions  
- **Bar Chart:** Ratings by ownership  
- **Pie Chart:** Emergency service availability  
- **Correlation Heatmap:** Ratings vs quality metrics  
- **Boxplot:** Ratings by ownership type  

### Interactive Dashboard (Plotly)
- Filters for **State** & **Ownership**  
- Dynamic charts & interactive visuals  
- Combined subplot layout for overview  

**Dashboard Features:**  
- Hospital Type Count  
- Ownership Distribution  
- Ratings by Ownership  
- Emergency Services Availability (Top 10 States)  
- Patient Experience Comparison  

---

## 💡 Key Insights

- **Acute Care & Non-Profit hospitals dominate** the dataset  
- Most hospitals have **average ratings ~3**  
- **Emergency services** widely available in high-count states  
- Weak correlations among quality metrics → **distinct performance indicators**  
- **Patient experience varies significantly** by hospital type  

---

## ⚠️ Limitations

- High missing data in quality metrics and ratings  
- Incomplete data reduces robustness of statistical analysis  

---

## ✅ Recommendations

- Encourage **full reporting** of quality metrics & overall ratings  
- Use quality metrics as **complementary performance indicators**  
- Improve **data completeness** in future datasets  

---

## 🛠️ Tools & Libraries
- **Data Handling:** Pandas, NumPy  
- **Visualization:** Matplotlib, Seaborn, Plotly  
- **Statistical Analysis:** SciPy (Chi-Square, Correlation)  

---


