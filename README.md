# 🏥 Strategic Patient Risk Stratification & Readmission Predictive Modeling

### **Vitality Health Network (VHN) — Health Informatics Solution**

## 📌 Project Summary

Hospital readmissions within 30 days are a critical quality metric in U.S. healthcare, directly impacting patient outcomes and hospital reimbursement under the **Hospital Readmissions Reduction Program (HRRP)**.

As a **Health Informatics Consultant**, I designed and implemented a **Strategic Patient Risk Stratification System** for **Vitality Health Network (VHN)**. This project transforms raw clinical data (100K+ encounters) into actionable insights to reduce avoidable readmissions for diabetic patients.

## 🎯 Business & Clinical Objectives

* **Reduce Readmissions:** Lower 30-day readmission rates for diabetic patients.
* **Clinical Interpretability:** Convert abstract ICD-9 codes into human-readable descriptions for clinical staff.
* **Proactive Intervention:** Stratify patients by risk to optimize post-discharge care coordination.
* **Data-Driven Compliance:** Support HRRP quality benchmarks using scalable Python analytics.

---

## 🛠️ Tech Stack & Skills

* **Data Science:** Python (Pandas, NumPy)
* **Data Engineering:** High-volume cleaning, categorical normalization, null handling (`?` to `NaN`).
* **Web Scraping:** `BeautifulSoup4` & `Requests` (Automated ICD-9 description enrichment).
* **Visualization:** `Matplotlib` & `Seaborn` (Clinical trend visualization).
* **Healthcare Analytics:** ICD-9 coding, LACE-inspired risk modeling.

---

## 🧮 The Vitality Complexity Index (VCI)

The core innovation of this project is the **VCI Algorithm**, a custom risk-scoring model inspired by the LACE Index.

### **VCI Components:**

| Component | Clinical Factor |
| --- | --- |
| **L** | **Length of Stay:** Duration of the current hospital encounter. |
| **A** | **Acuity of Admission:** Type of admission (Emergency vs. Elective). |
| **C** | **Comorbidities:** Number of diagnoses and complexity of medical history. |
| **E** | **Emergency Visits:** Frequency of emergency department use in the past 6 months. |

**Risk Stratification Tiers:**

* 🟢 **Low Risk:** Standard discharge care.
* 🟡 **Medium Risk:** Scheduled follow-up & medication reconciliation.
* 🔴 **High Risk (VCI > 10):** Intensive transitional care & proactive monitoring.

---

## 🔄 End-to-End Analytical Pipeline

1. **Data Ingestion:** Merging 100,000+ hospital encounters with ID mapping tables.
2. **Clinical Sanitation:** Handling non-standard nulls, removing duplicates, and filtering out deceased patient records.
3. **EDA:** Analyzing readmission patterns based on insulin therapy vs. oral medications.
4. **ICD-9 Enrichment:** Building a **Web Scraper** to map top 20 numeric codes (e.g., 428) to labels (e.g., *Congestive Heart Failure*).
5. **Risk Scoring:** Implementing the VCI logic across the entire dataset.

---

## 📈 Key Findings

* **Insulin Impact:** Patients on insulin therapy showed significantly higher 30-day readmission risk.
* **Model Validation:** The High-Risk (VCI > 10) group accurately captured the highest density of actual readmissions.
* **Efficiency:** Automated description mapping reduced clinical interpretation time for executive reports.

---

## 📂 Repository Structure

```text
├── data/
│     ├── diabetic_data.csv                   # Diabetic Patient Data
│     ├── IDs_mapping.csv                     # IDs Data
│     └── final_processed_diabetic_data.csv   # Final Processed Data
├── notebooks/
│   └── Vitality_Health_Analysis.ipynb   # End-to-end Python pipeline
├── reports/
│   └── Strategic_Insight_Report.pdf     # 3,000-word executive report
├── Project_Charts/
│   └── *.png                            # EDA & result visualizations
└── README.md

```

## 🔄 Reproducibility

1. Download data from [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008).
2. Place `diabetic_data.csv` and `IDs_mapping.csv` in a `/data` folder.
3. Install dependencies: `pip install pandas numpy matplotlib seaborn beautifulsoup4 requests`.
4. Run the Jupyter Notebook.

---

👨‍💻 **Developed by Tharusha Sandaruwan** *Full Stack Developer & Software Engineering Student*

```