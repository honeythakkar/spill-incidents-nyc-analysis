# Spill Incidents in New York, USA

![Python](https://img.shields.io/badge/Python-3.11-blue) ![DBSCAN](https://img.shields.io/badge/Model-DBSCAN-orange) ![Clustering](https://img.shields.io/badge/Model-Hierarchical_Clustering-red) ![License](https://img.shields.io/badge/License-MIT-green)

## Overview

A data mining project analyzing **552,290 real spill incident records** from the New York State Department of Environmental Conservation (DEC) using unsupervised machine learning — identifying geographic hotspots and high-risk incident types to support resource allocation and environmental protection.

**Key Results:**
- 🗺️ Identified high-frequency geographic spill hotspots across NY State using DBSCAN
- ⚠️ Equipment failure (37%) was the leading cause of all spill incidents
- 🛢️ Petroleum accounted for 84.67% of all material incidents
- 📊 Categorized incidents into high, mid, and low risk levels using Hierarchical Clustering

---

## Project Structure

```
spill-incidents-nyc-analysis/
│
├── README.md
└── (analysis notebooks coming soon)
```

---

## Dataset

**Source:** [NYSDEC Spill Incident Dataset](https://catalog.data.gov/dataset/spill-incidents) (Government open data)

| Attribute | Value |
|-----------|-------|
| Total Records | 552,290 rows |
| Features | 20 columns |
| Target Variable | None (Unsupervised Learning) |
| Date Range | 1978 – present |

**Key columns:** Spill Number, County, DEC Region, Spill Date, Contributing Factor, Material Family, Quantity, Recovered, Source

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Primary analysis language |
| pandas | Data cleaning & preprocessing |
| seaborn / matplotlib | Data visualization |
| scikit-learn | DBSCAN & Agglomerative Clustering |
| statsmodels | STL decomposition |

---

## Methodology

### 1. Data Cleaning & Preprocessing
- Handled missing values in ZIP Code, Waterbody, Quantity, and Units columns
- Standardized date formats for Spill Date, Received Date, and Close Date
- Encoded categorical columns (Contributing Factor, Source, Material Family)

### 2. Feature Engineering
- **Spill Duration:** Time difference between Spill Date and Close Date
- **Recovery Efficiency:** Ratio of Recovered quantity to total Quantity spilled
- Key finding: Spill Duration and Recovery Efficiency are negatively correlated

### 3. Exploratory Data Analysis
- Most common spill localities via horizontal bar charts
- Material family distribution (Petroleum vs Hazardous Materials)
- Source vs Contributing Factor heatmaps
- Time-series analysis of spill frequency over decades
- STL decomposition for seasonal and trend patterns
- Monthly spill incident visualization by affected area

### 4. DBSCAN Clustering (Geographic)
- Applied DBSCAN to identify high-frequency geographic spill hotspots
- Helps DEC prioritize where to focus preventive efforts and allocate resources

### 5. Agglomerative (Hierarchical) Clustering (Incident Type)
- Categorized spill incidents into high, mid, and low risk levels
- Helps DEC understand what types of incidents need special attention and protocol adjustments

---

## Key Findings

| Finding | Detail |
|---------|--------|
| Top Contributing Factor | Equipment Failure (37.38%) |
| Top Material Family | Petroleum (84.67%) |
| Top Spill Source | Commercial/Industrial (28.42%) |
| Highest Spill County | Westchester (9.99%) |
| Top Material | #2 Fuel Oil (25.25% of incidents) |

---

## Business Impact

The clustering insights help the NY State DEC:
- **Where** to focus preventive efforts — via DBSCAN geographic hotspot detection
- **What** incident types need special attention — via Hierarchical risk categorization
- **How** to allocate resources efficiently to reduce environmental damage

---

## Course Information

- **Course:** INSY: Principles of Business Data Mining
- **Institution:** University of Texas at Arlington
- **Date:** 2024–2025
- **Team:** Group project (4 members)

---

## Author

**Honey Bhatt**
MS Business Analytics | UT Arlington '25
[LinkedIn](https://www.linkedin.com/in/honeythakkar)
