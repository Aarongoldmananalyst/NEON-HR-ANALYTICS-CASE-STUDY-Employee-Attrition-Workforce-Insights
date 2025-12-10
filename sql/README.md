# 🧮 SQL Scripts Documentation
This folder contains all SQL transformation steps used to clean, normalize, engineer, and prepare the final HR dataset for Power BI.  
The SQL workflow follows a clean and reusable data-engineering pattern:

**Raw Data → Cleaning → Feature Engineering → Final Fact Table → Power BI Model**

---

# 📁 SQL Files Overview

## 1️⃣ **01_data_cleaning.sql**
Cleans and standardizes the raw HR data.

### **Key Tasks Performed**
- Removes duplicates  
- Handles missing or null values  
- Standardizes date formats (HireDate, TerminationDate)  
- Fixes inconsistent categorical labels  
- Ensures numeric fields are properly typed  
- Creates cleaned staging tables for further processing  

**Output:**  
`stg_HRData` — a clean and reliable version of the core HR dataset.

---

## 2️⃣ **02_feature_engineering.sql**
Creates all calculated fields needed for analysis, including tenure metrics and demographic groups.

### **Fields Generated**
- **Tenure** (in years)  
- **TenureGroup**  
  - 0–1 yrs (High Risk)  
  - 1–3 yrs (Elevated Risk)  
  - 3–6 yrs (Stable)  
  - 6+ yrs (Low Risk)

- **AgeGroup**  
  - 18–24  
  - 25–34  
  - 35–44  
  - 45–54  
  - 55+  

- **SalaryQuartile** (Q1, Q2, Q3, Q4)  
- **IsActiveEmployee** flag  
- **ExitFlag** for attrition analysis  
- **AttritionType**  

**Output:**  
`stg_HRFeatures` — enriched dataset ready for star schema modeling.

---

## 3️⃣ **03_final_fact_table.sql**
Builds the final dataset **FactHR**, used directly by Power BI.

### **Actions Performed**
- Joins all staging tables  
- Combines employee, salary, demographic, and tenure fields  
- Removes unneeded raw HR columns  
- Produces a clean, analytics-ready record per employee  

### **Final Columns in `FactHR`**
- EmployeeID  
- Gender  
- Age & AgeGroup  
- Department  
- JobRole  
- Salary  
- SalaryQuartile  
- TenureYears  
- TenureGroup  
- EducationLevel  
- HireDate  
- TerminationDate  
- IsActiveEmployee  
- ExitFlag  
- AttritionType  

**Output:**  
`FactHR` — master analytics table consumed by Power BI dashboards.

---

# 🔄 End-to-End SQL Data Flow

Raw HR Data
↓
01_data_cleaning.sql
↓
Cleaned Table (stg_HRData)
↓
02_feature_engineering.sql
↓
Feature Table (stg_HRFeatures)
↓
03_final_fact_table.sql
↓
FactHR (used in Power BI)


---

# 🧠 Why SQL Matters in This Project

Using SQL enables:

### ✔ Clean and consistent HR data  
HR data is messy — SQL creates a standardized dataset for analysis.

### ✔ Feature engineering for workforce intelligence  
Tenure, salary quartiles, and age groups are core predictors of attrition.

### ✔ Reproducible, auditable pipelines  
All transformations are version-controlled and transparent.

### ✔ High-performance Power BI modeling  
Power BI runs fastest when fed a **single clean fact table**.

---

# 📌 How to Use These Scripts

1. Load your raw HR dataset into SQL Server  
2. Run `01_data_cleaning.sql`  
3. Run `02_feature_engineering.sql`  
4. Run `03_final_fact_table.sql`  
5. Connect Power BI to the `FactHR` table  
6. Build or refresh the dashboard  

---

# 📬 Need Help?

Open an issue in the repo or contact:  
**aarondatascientist@gmail.com**



