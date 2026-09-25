# 🏥 Patient Readmission Risk Analysis

![SQL](https://img.shields.io/badge/SQL-SQLite-4479A1?logo=sqlite&logoColor=white)
![Python](https://img.shields.io/badge/Python-Pandas-3776AB?logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> Identifying which patient groups drive hospital readmissions, and what interventions would reduce them most.

---

## 📌 Overview

This project analyzes **101,766 patient encounters** from a diabetes-focused hospital dataset to answer a real operational question hospitals face:

> **"Which patient groups are driving the hospital's high readmission rate, and what three interventions would reduce it most?"**

The analysis segments patients into **Low / Medium / High risk tiers** using a composite score, then breaks down readmission drivers by diagnosis, age, insurance type, and discharge disposition.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| 🐍 **Python (Pandas)** | Data cleaning, diagnosis grouping, risk scoring |
| 🗄️ **SQL (SQLite)** | Segment-level aggregation and root-cause queries |
| 📊 **Power BI** | Interactive dashboard and visualization |

---

## 📂 Repository Structure

```
📁 patient-readmission-analysis/
├── README.md                        # This file
├── Executive_Summary.md             # One-page business summary
├── data_cleaning.py                 # Python/Pandas cleaning & risk scoring script
├── sql_queries.sql                  # All analysis queries, documented
├── diabetic_data_clean.csv          # Cleaned dataset (ready for SQL/BI import)
├── healthcare_readmission.db        # SQLite database (pre-loaded)
├── HealthCare.pbix                  # Power BI dashboard file
└── dashboard_screenshot.png         # Dashboard preview image
```

---

## 🎯 Key Findings

| Metric | Value |
|---|---|
| 📊 Overall 30-day readmission rate | **11.16%** |
| 🔴 High-risk segment readmission rate | **16.68%** |
| 🟢 Low-risk segment readmission rate | 7.56% |
| ⚠️ High-risk + Diabetes diagnosis | **22.13%** |
| ⚠️ High-risk + age 20–30 | **31.57%** (highest in dataset) |
| 🏥 Transferred to rehab/other facility | 20.9%–31.3% (vs ~9% discharged home) |
| 💳 Insurance type impact | Minimal — ruled out as a driver |

**Root cause:** Readmission risk is driven by **prior utilization, diagnosis type, and discharge pathway — not insurance coverage.**

---

## 📈 Dashboard Preview

![Dashboard Demo](dashboard_demo.gif)

*Live demo showing Risk Segment, Diagnosis Category, and cross-filtering in action.*

![Dashboard Screenshot](dashboard_screenshot.png)

*Static view. Built in Power BI — download `HealthCare.pbix` to explore interactively.*

---

## ✅ Recommendations

1. **🩺 Targeted post-discharge care for high-risk Diabetes patients** — proactive follow-up calls and medication reconciliation within 7 days of discharge.
2. **🔄 Strengthen discharge-transfer protocols** — structured handoff documentation and a 48-hour post-transfer check-in for patients moving to rehab/other facilities.
3. **🧑‍⚕️ Dedicated support pathway for high-risk patients aged 20–40** — case management and social worker outreach alongside clinical care.

📄 Full write-up: [Executive_Summary.md](Executive_Summary.md)

---

## 🔍 Methodology

1. **Data Cleaning (Python/Pandas)** — handled missing values, grouped 700+ ICD-9 diagnosis codes into 9 clinical categories, mapped discharge disposition codes to readable labels
2. **Risk Scoring** — composite score from prior inpatient visits + length of stay + medication count → Low/Medium/High segments
3. **SQL Analysis** — aggregated readmission rates across risk segment, diagnosis, age, insurance, and discharge type ([full queries here](sql_queries.sql))
4. **Dashboard Build** — interactive Power BI report with cross-filtering slicers and KPI callouts

---

## 📊 Dataset Source

[Diabetes 130-US Hospitals Dataset](https://www.kaggle.com/datasets/brandao/diabetes) — 101,766 patient encounters, Kaggle.

---

## 📬 Contact

**Mohammed Fahad Chouhan**
📧 fahadchouhan111@gmail.com
