<!-- Banner Image -->
<p align="center">
  <img width="846" height="470" alt="BANNER" src="https://github.com/user-attachments/assets/03ba73bb-0fa8-4313-b952-40b888e16d65" />











<br>

<h1 align="center">🧠 NEON HR ANALYTICS CASE STUDY</h1>
<h3 align="center">Employee Attrition & Workforce Insights</h3>
<h4 align="center">SQL • Power BI • 18,500 Employees • Workforce Intelligence</h4>



<br>


An end-to-end HR Analytics solution powered by **SQL Server**, **Power BI**, and **data storytelling**, analyzing workforce patterns across **18,500 employees** to uncover attrition drivers, compensation gaps, and organizational risk.

  
<br>

---
https://github.com/user-attachments/assets/f1909c2f-8c93-455e-84a8-31c17d892bf7

### 🔍 Interactive Case Study Walkthrough (Silent Demo)

This silent walkthrough demonstrates how the Power BI dashboard supports exploratory workforce analysis:

- Click-based cross-filtering across departments, tenure groups, education, and gender  
- Responsive KPIs that update dynamically with each selection  
- Hover tooltips providing detailed metric context  
- Designed for fast investigation of attrition drivers and workforce risk segments  

The dashboard enables HR leaders to move from high-level trends to root-cause insights in seconds.

---

# ✨ About This Project

This project reveals why employees leave, which departments are at risk, how compensation affects attrition, and what demographic trends reveal about the workforce.

The neon-themed Power BI dashboard and SQL-based transformations deliver insights that enable HR leaders to:

- Reduce attrition  
- Improve compensation fairness  
- Strengthen leadership pipelines  
- Optimize workforce planning  

---



# 🛠️ Tech Stack

<p>
<a href="https://learn.microsoft.com/sql" target="_blank"><img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white"/></a><a href="https://learn.microsoft.com/power-bi" target="_blank"><img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/></a><a href="https://dax.guide" target="_blank"><img src="https://img.shields.io/badge/DAX-000000?style=for-the-badge"/></a><a href="https://www.ibm.com/topics/data-analytics" target="_blank"><img src="https://img.shields.io/badge/Data%20Analytics-4B8BBE?style=for-the-badge&logo=databricks&logoColor=white"/></a><a href="https://www.shrm.org/resourcesandtools/hr-topics/organizational-and-employee-development/pages/workforce-analytics.aspx" target="_blank"><img src="https://img.shields.io/badge/Workforce%20Analytics-6A1B9A?style=for-the-badge"/></a><a href="https://opensource.org/licenses/MIT" target="_blank"><img src="https://img.shields.io/badge/MIT%20License-2ECC71?style=for-the-badge&logo=open-source-initiative&logoColor=white"/></a>
</p>



---



# 🤝 Connect With Me

<p>
<a href="https://www.linkedin.com/in/aaron-goldmans/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a><a href="mailto:aarondatascientist@gmail.com" target="_blank"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a><a href="https://github.com/Aarongoldmananalyst" target="_blank"><img src="https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white"/></a>
</p>



---


# 📎 Quick Links

<p>
<a href="presentation/NEON_HR_Analytics_Case_Study.pdf" target="NEON_HR_Analytics_Case_Study.pdf.">📄 Storytelling Deck (PDF)</a><br>
<a href="powerbi/Neon_HR_Analytics_Dashboard.pbix" target="_blank">📊 Power BI Dashboard (.pbix)</a><br>
<a href="sql/" target="_blank">🧮 SQL Scripts</a><br>
<a href="docs/insights_summary.md" target="_blank">🧠 Insights Summary</a><br>
<a href="data/data_dictionary.md" target="_blank">🧾 Data Dictionary</a><br>
<a href="docs/methodology.md" target="_blank">🔧 Methodology</a><br>
<a href="docs/DAX_measures.md" target="_blank">📐 DAX Measures</a>
</p>

---




# 🖼️ Dashboard Preview

<p align="center">
  <img width="881" height="493" alt="DASHBOARD" src="https://github.com/user-attachments/assets/087190d0-11c0-40e9-ac89-78c98fb2be08" />

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

This dashboard exposes **predictable and preventable** attrition patterns driven by compensation inequities, workload imbalances, and early-tenure disengagement.

---

# 🧩 Problem Statement

Organizations face rising turnover and wage compression. HR leaders needed answers to:

1. Where are we losing talent?  
2. Why are employees leaving?  
3. How does compensation influence attrition?  
4. Which demographics or tenure groups are most at risk?  
5. What interventions produce the highest ROI?

This project answers these questions using a **SQL → Power BI** analytics pipeline.

---

# 🧱 Data Engineering (SQL)

### 📌 **Scripts Included**

- **01_data_cleaning.sql** — cleans raw HR data  
- **02_feature_engineering.sql** — creates tenure, age buckets, salary quartiles, etc.  
- **03_final_fact_table.sql** — builds `FactHR` (dataset used in Power BI)  

📁 Folder: [`sql/`](sql/)  
📘 Documentation: [`sql/README.md`](sql/README.md)

---

# 🔍 Key Insights (from `insights_summary.md`)

### 🔥 **Attrition**
- Early-tenure employees churn fastest  
- Sales & Operations show structural risk  

### 💰 **Compensation**
- Pay gaps strongly correlate with attrition  
- Operational roles experience wage compression  

### 👥 **Workforce Composition**
- Strong gender balance overall  
- Leadership representation gap for women persists  

### 🕒 **Tenure**
- Retention improves dramatically after year 3  

📘 Full insights: [`docs/insights_summary.md`](docs/insights_summary.md)

---

# 📐 DAX Measures (Power BI)

Includes DAX for:

- Attrition Rate  
- Total Employees  
- Active Employees  
- Avg Salary  
- Gender Metrics  
- Tenure Calculations  

📘 Full list: [`docs/DAX_measures.md`](docs/DAX_measures.md)

---

# 📁 Repository Structure

📁 data/
📁 sql/
📁 powerbi/
📁 presentation/
📁 images/
📁 docs/
README.md
LICENSE


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

# 🎯 Why This Project Matters

This case study demonstrates the ability to:

- Engineer data using SQL  
- Build professional dashboards in Power BI with DAX  
- Analyze workforce & compensation patterns  
- Tell compelling business stories  
- Communicate insights to leadership  
- Deliver ROI-driven recommendations  

It transforms HR analytics into **strategic decision-making tools**.

---

# 🤝 Connect & Explore

<p>
<a href="https://www.linkedin.com/in/aaron-goldmans/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a><a href="mailto:aarondatascientist@gmail.com" target="_blank"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a><a href="https://github.com/Aarongoldmananalyst" target="_blank"><img src="https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white"/></a>
</p>

---

# 🌟 Thank You for Exploring This Project  
This HR Analytics Case Study delivers actionable, visually compelling insights designed for real-world impact.



