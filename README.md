# 🕵️ EDA Patrol: Crime Analysis Across Indian Districts

Welcome to the **EDA Patrol** project — a comprehensive data exploration and modeling pipeline built to analyze crime patterns across Indian districts using real IPC crime data. This project spans data cleaning, exploratory analysis, clustering, risk indexing, geospatial mapping, and Power BI dashboards.

---

## 📁 Dataset

- **Source**: `Districtwise_Crime_of_India_2001_to_2014.csv`
- **Granularity**: District-level records from all Indian states and union territories (2001–2014).
- **Features**: 
  - Crime categories (Murder, Rape, Theft, etc.)
  - Total IPC Crimes
  - State/UT, District, Year columns

---

## 🔍 EDA Highlights

1. **Total IPC Crimes**:  
   > 🔢 Over **58 million crimes** recorded across all districts.

2. **Top States by Crime Volume**:
   - Madhya Pradesh
   - Maharashtra
   - Tamil Nadu
   - Andhra Pradesh

3. **Top Districts by IPC Crimes**:
   - Concentrated in Madhya Pradesh and Maharashtra

4. **Urban vs Rural Analysis**:
   - Urban-like districts (top 25%) show higher averages across all major crime types.
   - Theft is the most distinguishing crime in urban districts.

5. **Correlation Heatmap**:
   - High positive correlation between **murder** and **dowry deaths** (0.91).
   - Rape and murder are also strongly correlated (0.79).

---

## 📈 Visualizations

All graphs were generated using **Matplotlib** and **Seaborn**:

- 🔹 Distribution Plots: Show right-skewed nature of total crimes
- 🔹 Clustered Scatterplots: Murder vs Rape with KMeans (4 clusters)
- 🔹 Monthly Simulated Trend: Shows peak in March and July (for visual use only)
- 🔹 State-wise Choropleth: Built using **GeoPandas** and shapefiles
- 🔹 Bar Charts: Top districts and states by crime category

---

## 🧠 Advanced Analysis

### ✅ Crime Clustering
- KMeans on standardized features (Murder, Rape, Theft, Riots, etc.)
- Created 4 clusters:
  - **Low crime zones** (rural-like)
  - **Moderate crime** (urban average)
  - **High sexual violence**
  - **High murder and theft concentration**

### ✅ Predictive Modeling
- **Linear Regression** to forecast total IPC crimes:
  - R² = ~0.93
  - RMSE ≈ realistic for total volume prediction

- **Random Forest Classifier** to label high-crime districts (binary):
  - Train Accuracy: ~100%
  - Test Accuracy: ~96%

### ✅ Crime Risk Index
- Created using normalized sum of selected crime types
- Top districts identified as high risk

### ✅ Crime Against Women
- 22.4% of crimes are against women
- **Uttar Pradesh** reported the highest **dowry deaths**

---

## 📊 Power BI Dashboard

An interactive Power BI report includes:

- Filters for **Year**, **State/UT**, and **District**
- Dynamic crime summary tables
- Bar charts by crime type and district
- Filled maps using **District-level totals**
- Color-coded visualizations for crime severity

> File: `Challenge5_2013.pbix`

---

## 🗺️ Geospatial Mapping

- Uses `Admin2.shp` shapefile of India
- Maps total IPC crimes across states
- Crime hotspots clearly visible in:
  - Madhya Pradesh
  - Maharashtra
  - Uttar Pradesh

---

## 📦 Dependencies

Install all dependencies with:

```bash
pip install pandas geopandas matplotlib seaborn scikit-learn statsmodels
