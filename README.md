<!-- Banner Image -->
<p align="center">
  <img width="846" height="470" alt="BANNER" src="https://github.com/user-attachments/assets/03ba73bb-0fa8-4313-b952-40b888e16d65" />




<h1 align="center">🧠 NEON HR ANALYTICS CASE STUDY</h1>
<h3 align="center">Employee Attrition & Workforce Insights</h3>
<h4 align="center">SQL + Power BI • 18,500 Employees • End-to-End Workforce Intelligence</h4>

<br>

An end-to-end HR Analytics solution powered by **SQL Server**, **Power BI**, and **data storytelling**, analyzing workforce patterns across **18,500 employees** to uncover attrition drivers, compensation gaps, and organizational risk.

---

# 🧩 About This Project

This project reveals why employees leave, which departments are at risk, how compensation affects attrition, and what demographic trends reveal about the workforce.

The neon-themed Power BI dashboard and SQL-based transformations deliver insights that enable HR leaders to:

- Reduce attrition  
- Improve compensation fairness  
- Strengthen leadership pipelines  
- Optimize workforce planning  

---

# 🛠️ Tech Stack

<p>
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/DAX-000000?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Data%20Analytics-4B8BBE?style=for-the-badge&logo=databricks&logoColor=white"/>
  <img src="https://img.shields.io/badge/Workforce%20Analytics-6A1B9A?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/MIT%20License-2ECC71?style=for-the-badge&logo=open-source-initiative&logoColor=white"/>
</p>

---

# 🤝 Connect With Me

<p>
  <a href="https://www.linkedin.com/in/YOUR-LINKEDIN" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="mailto:YOUR-EMAIL@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
  <a href="https://github.com/YOUR-GITHUB" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
</p>

---

# 📎 Quick Links

- 📄 **Storytelling Deck (PDF)** — [`presentation/NEON_HR_Analytics_Case_Study.pdf`](presentation/NEON_HR_Analytics_Case_Study.pdf)  
- 📊 **Power BI Dashboard (.pbix)** — [`powerbi/Neon_HR_Analytics_Dashboard.pbix`](powerbi/Neon_HR_Analytics_Dashboard.pbix)  
- 🧮 **SQL Scripts** — [`sql/`](sql/)  
- 🧠 **Insights Summary** — [`docs/insights_summary.md`](docs/insights_summary.md)  
- 🧾 **Data Dictionary** — [`data/data_dictionary.md`](data/data_dictionary.md)  
- 🔧 **Methodology** — [`docs/methodology.md`](docs/methodology.md)  
- 📐 **DAX Measures** — [`docs/DAX_measures.md`](docs/DAX_measures.md)  

---

# 🖼️ Dashboard Preview

<p align="center">
  <img width="882" height="493" alt="NEON HR CASE STUDY   DASHBOARD" src="https://github.com/user-attachments/assets/cc63ed6a-e1b8-4e22-8d85-e9ad543d03d0" />

</p>

---

# 📊 Executive Summary

- **Attrition Rate:** **20.15%**  
- **Total Exits:** **3,728 employees**  
- **Highest Attrition:** Sales, Operations, HR  
- **Highest Risk Tenure:** **0–1 years (highest)** and **1–3 years (elevated)**  
- **Salary Gap:** Up to **$27K** between operational & technical roles  
- **Bottom Salary Quartile:** **2.3× more likely** to quit  
- **Workforce Composition:** Balanced gender but leadership gap persists  

This dashboard reveals **predictable and preventable attrition patterns**, driven by compensation inequities, early-tenure disengagement, and workload imbalances.

---

# 🧩 Problem Statement

Organizations face rising turnover and wage compression in key roles. HR leaders urgently needed clarity on:

1. Where are we losing talent?  
2. Why are employees leaving?  
3. How does compensation influence attrition?  
4. Which demographics or tenure groups are at risk?  
5. What interventions would generate the highest ROI?

This project answers all five using a complete **SQL → Power BI** data pipeline.

---

# 🧱 Data Engineering (SQL)

## 📌 Scripts Included

- **01_data_cleaning.sql** — cleans raw HR data  
- **02_feature_engineering.sql** — creates tenure, age buckets, salary quartiles, etc.  
- **03_final_fact_table.sql** — builds `FactHR` (dataset used in Power BI)  

See folder: [`sql/`](sql/)  
Full documentation: [`sql/README.md`](sql/README.md)

---

# 🔍 Key Insights (from insights_summary.md)

## 🔥 Attrition
- Early-tenure employees churn fastest  
- Sales & Operations show structural instability  

## 💰 Compensation
- Pay gaps strongly correlate with attrition  
- Operational roles are under-compensated  

## 👥 Workforce Composition
- Strong gender balance  
- Leadership representation gap for women  

## 🕒 Tenure
- Retention dramatically improves after year 3  

Full insights:  
[`docs/insights_summary.md`](docs/insights_summary.md)

---

# 📐 DAX Measures (Power BI)

Includes measures for:

- Attrition Rate  
- Total Employees  
- Active Employees  
- Avg Salary  
- Gender Counts  
- Tenure metrics  

Full list:  
[`docs/DAX_measures.md`](docs/DAX_measures.md)

---

# 📁 Repository Structure
📂 NEON HR ANALYTICS CASE STUDY — Employee Attrition & Workforce Insights/
│
├── README.md
│
├── 📁 data/
│ ├── HR_Analytics_18500_Employees.csv
│ └── data_dictionary.md
│
├── 📁 sql/
│ ├── 01_data_cleaning.sql
│ ├── 02_feature_engineering.sql
│ ├── 03_final_fact_table.sql
│ └── README.md
│
├── 📁 powerbi/
│ └── Neon_HR_Analytics_Dashboard.pbix
│
├── 📁 presentation/
│ ├── NEON_HR_Analytics_Case_Study.pdf
│ └── Storytelling_Deck.pdf
│
├── 📁 images/
│ ├── banner.png
│ ├── dashboard_preview.png
│
└── 📁 docs/
├── methodology.md
├── insights_summary.md
├── DAX_measures.md


---

# 📈 Business Impact

If implemented, insights from this dashboard can deliver:

| Impact Area | Expected Outcome |
|-------------|------------------|
| Attrition Reduction | **10–20% decrease** (~$3M savings) |
| Pay Equity | **+8 point improvement** |
| Leadership Development | **40% increase** in female leadership pipeline |
| Hiring Efficiency | **12% faster time-to-fill** |

This shifts HR from reactive to **proactive workforce intelligence**.

---

# 🎤 Why This Project Matters

This case study demonstrates:

- SQL-based data engineering  
- Power BI dashboard development with DAX  
- Workforce & attrition analytics  
- Compensation equity analysis  
- Data storytelling & executive communication  
- ROI-driven recommendations  

It transforms HR analytics into **strategic workforce intelligence**.

---

# 🤝 Connect & Explore

<p>
  <a href="https://www.linkedin.com/in/YOUR-LINKEDIN" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="mailto:YOUR-EMAIL@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
  <a href="https://github.com/YOUR-GITHUB" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
</p>

---

# 🌟 Thank You for Exploring This Project  
This HR Analytics Case Study delivers actionable, visually compelling insights designed for real-world impact.


