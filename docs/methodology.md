# 🔧 Methodology
This methodology explains the full analytical workflow used to build the **Neon HR Analytics Case Study**, from raw data ingestion to final visualization in Power BI.  
The process ensures data quality, transparency, and reproducible insights across all HR metrics.

---

# 🛰️ 1. Project Overview

The project analyzes workforce patterns across **18,500 employees** to uncover:

- Drivers of attrition  
- Compensation disparities  
- Workforce demographics  
- Tenure risk patterns  
- Departmental performance differences  

The analysis combines **SQL Server**, **Power BI**, and **DAX** to create a professional HR analytics solution.

---

# 🧱 2. Data Ingestion

Raw employee data was provided as CSV / HRIS extracts and imported into SQL Server.

### **Raw Input Tables Included**
- Employee master data  
- Job and department data  
- Salary and compensation  
- Termination records  
- Demographic attributes  

These raw inputs contained inconsistencies, missing fields, and mixed formats — requiring cleaning and transformation.

---

# 🧼 3. Data Cleaning (SQL)

Executed in `01_data_cleaning.sql`.

### **Key Cleaning Steps**
- Standardized date formats (HireDate, TerminationDate)  
- Removed duplicates and bad records  
- Normalized categorical fields (Gender, Education, Dept names)  
- Imputed missing demographic values where necessary  
- Ensured numeric fields were properly typed  

**Output Table:**  
`stg_HRData`

This table acts as the foundation for all downstream calculations.

---

# 🧮 4. Feature Engineering (SQL)

Executed in `02_feature_engineering.sql`.

### **Engineered Fields Created**
- **TenureYears** → Time employed in years  
- **TenureGroup** → Risk buckets based on tenure  
- **AgeGroup** → Demographic slicing  
- **SalaryQuartile** → Income segmentation  
- **ExitFlag** → Signals if the employee left  
- **IsActiveEmployee** → Binary indicator  
- **AttritionType** → Voluntary, involuntary, retirement  

These engineered fields unlock deeper storytelling in Power BI.

**Output Table:**  
`stg_HRFeatures`

---

# 🧩 5. Data Modeling (SQL → Power BI)

Executed in `03_final_fact_table.sql`.

A single, denormalized table was created for Power BI:

### **FactHR**
Contains all features needed for:

- Attrition analysis  
- Salary analysis  
- Tenure insights  
- Department performance  
- Demographic distribution  

### ⭐ Why use a single fact table?
- Faster Power BI refresh  
- Simpler DAX logic  
- Cleaner relationships  
- Less chance of model errors  

Star-schema modeling principles were applied where relevant.

---

# 📐 6. DAX Measures

Power BI uses custom DAX to compute:

- **Attrition Rate**  
- **Total Employees**  
- **Active Employees**  
- **Avg Salary**  
- **Employee Count by Department**  
- **Exits by TenureGroup**  
- **Salary Quartile Metrics**  
- **Diversity Indicators**  

Full DAX definitions:  
`docs/DAX_measures.md`

DAX transforms SQL outputs into dynamic, interactive metrics.

---

# 🎨 7. Dashboard Design (Power BI)

The visualization layer uses a **neon analytic theme** inspired by modern enterprise dashboards.

### **Key Design Principles**
- High contrast colors for readability  
- Minimal clutter  
- KPI-driven layout  
- Drill-down navigation  
- Intuitive filters & slicers  
- Persona-specific storytelling (HR Directors, People Partners, Execs)  

### **Pages Included**
- Overview  
- Attrition & Exits  
- Compensation Analysis  
- Workforce Composition  
- Tenure & Risk  
- Department Analysis  

---

# 🎯 8. Insights Extraction

Insights were derived by analyzing patterns across:

- Departments with highest turnover  
- Salary quartile risk  
- Tenure distribution  
- Gender & age representation  
- Education-level stability  
- Early-tenure risk behavior  

Detailed narrative:  
`docs/insights_summary.md`

---

# 📝 9. Reporting & Storytelling

The project includes a **12-slide storytelling deck** explaining:

- Business problem  
- Analytical approach  
- Dashboard walkthrough  
- Key insights  
- Recommendations  
- Business impact  

Deck File:  
`presentation/NEON_HR_Analytics_Case_Study.pdf`

---

# 🚀 10. Final Deliverables

- SQL transformation scripts  
- Power BI dashboard (.pbix)  
- Storytelling Deck (PDF)  
- GitHub README case study  
- Insights, data dictionary, methodology pages  
- DAX measure library  

These deliverables together form a complete, recruiter-ready analytics portfolio project.

---

# 📬 Contact

For questions or collaboration:  
**aarondatascientist@gmail.com**

