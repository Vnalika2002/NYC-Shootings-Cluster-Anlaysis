# 🗽 NYC Shootings Clustering & Analysis using K-Means

## 📌 Overview

This project aims to uncover hidden patterns in **New York City shooting incidents** using unsupervised learning techniques — primarily **K-Means clustering**. By analyzing spatial, temporal, and demographic data, we attempt to identify incident clusters that could guide smarter crime prevention strategies, hotspot policing, and public safety policy decisions.

Through cluster analysis, we have successfully revealed latent structures in shooting patterns that are otherwise difficult to detect with traditional analytics.

---

## 🎯 Objectives

- Discover natural groupings in NYC shooting incidents using machine learning.
- Analyze the role of **location**, **time**, and **victim demographics** in shootings.
- Provide actionable insights for **crime hotspot detection** and **temporal policing**.
- Support **data-driven safety planning** and community outreach.

---

## 🗂️ Dataset Information

- **Source:** [NYC Open Data Portal – NYPD Shooting Incident Data (Historic)]  
- **Time Span:** Multiple years (historic dataset, preprocessed)
- **Records:** Tens of thousands of rows (size depends on selected timeframe)
- **Format:** CSV with spatial, temporal, and demographic data

### 🔑 Key Features

- `OCCUR_DATE`, `OCCUR_TIME`: When the incident occurred
- `BORO`, `PRECINCT`: NYC borough and precinct
- `Latitude`, `Longitude`: Spatial coordinates
- `VIC_AGE_GROUP`, `VIC_SEX`: Victim demographics
- `LOC_OF_OCCUR_DESC`: Contextual info (residential, street, etc.)

---

## 🧠 Methodology

### 1️⃣ Data Preprocessing

- Removed records with null or missing essential values (e.g., location or victim demographics)
- Extracted time-related features: **weekday**, **hour**, and **month**
- Encoded categorical data using **Label Encoding**
- Standardized numerical features using **StandardScaler**

### 2️⃣ Feature Engineering

- Selected relevant features:
  - **Spatial:** Latitude, Longitude
  - **Temporal:** Hour of day, Day of week
  - **Demographic:** Victim sex and age group
  - **Contextual:** Borough, Precinct

### 3️⃣ Clustering

- Applied **K-Means Clustering** with `k = 5` (chosen using elbow method)
- Used **Principal Component Analysis (PCA)** for 2D visualization
- Each incident was assigned to a cluster based on feature similarity

---

## 📊 Visualization & Results

### ✅ Cluster Profiles

| Cluster | Description |
|--------|-------------|
| 0 | Night-time shootings in **Manhattan and Brooklyn**, mostly **male victims** |
| 1 | Spread across boroughs, more **female victims**, peak in early evening |
| 2 | **Bronx-focused**, younger victims, often on **weekends** |
| 3 | **Morning incidents** in residential areas |
| 4 | Smaller cluster in **central NYC**, adult male victims |

### 📈 PCA Plot

- PCA revealed clear separation between clusters, validating feature usefulness and clustering accuracy.

### 🗺️ Geospatial Trends

- Hotspots emerged in **Bronx**, **Brooklyn**, and **lower Manhattan**
- Spatial clusters aligned with unique temporal/demographic traits

---

## 📌 Recommendations

- **Hotspot Policing:** Focus on high-risk clusters like 0 and 2.
- **Temporal Deployment:** Reinforce patrols during identified danger hours (e.g., Cluster 0 – night, Cluster 3 – morning).
- **Community Outreach:** Launch youth-focused interventions in Bronx and Brooklyn.
- **Data Enrichment:** Integrate socio-economic, housing, and gang activity indicators for deeper clustering.

---

## ✅ Success Criteria Evaluation

- Distinct clusters with clear separation using PCA
- Cluster-specific behavior validated by visualization and incident mapping
- High alignment with known crime trends in NYC

---

## ⚖️ Ethical Considerations

- Dataset is **anonymized** — no PII involved
- Clustering used solely for pattern recognition, not individual profiling
- Aggregated data used to avoid demographic or geographic bias
- All processing steps followed **neutral and reproducible** logic

---

## 🚧 Limitations

- Missing or incomplete records may reduce modeling accuracy
- K-Means assumes **spherical clusters** — may not capture complex geospatial boundaries
- Temporal resolution limited to hour granularity; minute-level precision could improve results
- No external data (e.g., weather, events, socio-economic status) integrated

---

## 🔮 Future Work

- Try alternative clustering techniques like **DBSCAN**, **Gaussian Mixture Models**
- Merge external data sources for multi-dimensional analysis
- Integrate real-time crime feeds for **live hotspot mapping**
- Build an **interactive dashboard** for daily use by law enforcement analysts
- Deploy a **Streamlit web app** for user interaction with filters and visualization

---

## 📁 Project Structure

