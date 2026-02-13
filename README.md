# Strategic Patient Risk Stratification & Readmission Predictive Modeling

**Vitality Health Network (VHN)**  
*Python for Data Science, Healthcare Analytics & AI*

---

## 📌 Project Summary

Hospital readmissions within 30 days are a critical quality metric in U.S. healthcare, directly impacting patient outcomes and hospital reimbursement under the **Hospital Readmissions Reduction Program (HRRP)**.

This project focuses on **diabetic patient readmissions** at **Vitality Health Network (VHN)**.  
As a **Health Informatics Consultant**, I designed and implemented a **Strategic Patient Risk Stratification System** that:

- Identifies high-risk diabetic patients at discharge  
- Improves clinical interpretability of complex medical codes  
- Provides actionable insights for care coordination teams  
- Supports data-driven reduction of avoidable readmissions  

The solution integrates large-scale clinical data processing, automated ICD-9 enrichment, exploratory analysis, and a custom risk-scoring algorithm inspired by the **LACE Index**.

---

## 🎯 Business & Clinical Objectives

- Reduce 30-day readmission rates for diabetic patients  
- Support compliance with HRRP quality benchmarks  
- Enable proactive intervention for high-risk patients  
- Improve executive and clinical interpretability of EHR data  
- Demonstrate scalable healthcare analytics using Python  

---

## 🛠️ Tech Stack & Core Skills

### Programming & Data Science
- **Python 3.x**
- **Pandas** — data wrangling, aggregation, feature engineering  
- **NumPy** — numerical operations and vectorized computation  

### Data Engineering
- High-volume data cleaning (100K+ encounters)
- Type conversion and categorical normalization
- Null handling and data integrity validation

### Web Scraping & Data Enrichment
- **Requests**
- **BeautifulSoup4**
- Automated ICD-9 code description extraction

### Data Visualization
- **Matplotlib**
- **Seaborn**
- Exploratory Data Analysis (EDA) and clinical trend visualization

### Healthcare Analytics
- ICD-9 diagnosis codes
- Readmission outcome analysis
- Custom risk index design (VCI)

---

## 📂 Repository Structure

```text
├── notebooks/
│   └── Vitality_Health_Analysis.ipynb   # End-to-end Python pipeline
│
├── reports/
│   └── Strategic_Insight_Report.pdf     # 3,000-word executive report
│
├── charts/
│   └── *.png                            # Exported EDA & results visualizations
│
└── data/
    └── (Ignored via .gitignore)
        ├── diabetic_data.csv
        └── IDs_mapping.csv
```
Note: Raw clinical datasets are excluded to protect patient privacy.

---

## Dataset Description

**Source:**
UCI Machine Learning Repository — Diabetes 130-US Hospitals (1999–2008)

**Scope:**
* 100,000+ hospital encounters
* 130 U.S. hospitals
* Diabetic patients only
* Includes demographics, diagnoses, procedures, medications, length of stay, and readmission outcomes

**Target Variable:**
30-day readmission status (<30, >30, NO)

---

##🔁 End-to-End Analytical Pipeline

1. Data Ingestion
* Loaded raw CSV files using Pandas
* Merged diagnosis and ID mapping tables
* Verified schema consistency and record counts

2. Clinical Data Sanitation
Key preprocessing steps included:
* Replaced non-standard nulls **?** with NaN
* Dropped encounters involving deceased patients
* Removed duplicate patient encounters
* Standardized categorical variables
* Reduced noise in high-cardinality ICD-9 features
**Outcome:**
  A clean, analysis-ready clinical dataset suitable for risk modeling.

3. Exploratory Data Analysis (EDA)
Performed extensive EDA to uncover readmission patterns:
* Readmission rates by:
    * Admission type
    * Length of stay
    * Medication category
    * Number of diagnoses
* Insulin vs. oral antidiabetic therapy comparison
* Distribution analysis of emergency visits and comorbidities
Visualizations were exported for clinical and executive reporting.

4. Automated ICD-9 Code Enrichment
To improve interpretability:
* Identified Top 20 most frequent ICD-9 diagnosis codes
* Built a web scraper to fetch long clinical descriptions
* Mapped numeric codes (e.g., 428) to human-readable labels (e.g., Congestive Heart Failure)
This step significantly enhanced stakeholder comprehension of clinical risk drivers.

---

## 🧮 Vitality Complexity Index (VCI)
**Overview**
The **Vitality Complexity Index (VCI)** is a custom patient risk-scoring algorithm inspired by the LACE Index, designed to stratify diabetic patients by readmission risk at discharge.

**VCI Components**

Each component contributes weighted points to a composite risk score.

**Risk Stratification**
Patients were grouped into:
* Low Risk
* Medium Risk
* High Risk (VCI > 10)
This stratification enables targeted post-discharge interventions.

---

## 📈 Key Findings & Insights
**Medication Type & Readmission Risk**
Patients receiving insulin therapy showed significantly higher 30-day readmission rates compared to those on oral antidiabetic medications.

**Model Validation**
* The High Risk (VCI > 10) group demonstrated the highest observed readmission frequency.
* Clear monotonic increase in readmission risk across VCI tiers validated the index design.

**Clinical Implications** 
* High-risk patients may benefit from:
    * Post-discharge follow-ups
    * Medication reconciliation
    * Transitional care programs
---

## 🏥 Business & Clinical Impact

* Supports proactive care coordination
* Enhances discharge planning decisions
* Improves HRRP compliance readiness
* Demonstrates scalable analytics for population health management

----

## 🔐 Data Privacy & Ethics
* No protected health information (PHI) is stored in this repository
* Public dataset usage complies with UCI data sharing guidelines
* Project intended strictly for educational and analytical demonstration

---

## 🔄 Reproducibility Instructions

1. Download the dataset from:
[UCI Machine Learning Repository.](https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008)

2. Create a data/ folder in the project root
3. Add:
   * diabetic_data.csv
   * IDs_mapping.csv
4. Run `Vitality_Health_Analysis.ipynb`





