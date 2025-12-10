# 🧾 Data Dictionary
This data dictionary defines all fields used in the HR Analytics data model.  
It includes raw HRIS fields, engineered features, and final metrics used in the Power BI dashboard.

The dataset consists of **18,500 employees** across all departments, roles, and demographic groups.

---

# 📁 1. Employee Demographics

| Field Name | Type | Description |
|-----------|------|-------------|
| **EmployeeID** | Integer | Unique identifier for each employee. |
| **Gender** | Text | Employee gender (Male, Female). |
| **Age** | Integer | Employee age at snapshot date. |
| **AgeGroup** | Text | Categorized age bucket (18–24, 25–34, 35–44, 45–54, 55+). |
| **MaritalStatus** | Text | Single, Married, Divorced, etc. |
| **EducationLevel** | Text | Highest educational attainment (High School, Bachelors, Masters, etc.). |

---

# 🏢 2. Job & Role Attributes

| Field Name | Type | Description |
|-----------|------|-------------|
| **Department** | Text | Department the employee belongs to (Sales, Operations, HR, etc.). |
| **JobRole** | Text | Specific job function or title. |
| **EmploymentStatus** | Text | Active or Terminated. |
| **HireDate** | Date | Employee’s official start date. |
| **TerminationDate** | Date | Employee’s exit date (if applicable). |
| **IsActiveEmployee** | Boolean | 1 = Active, 0 = Terminated. |

---

# 💰 3. Compensation Fields

| Field Name | Type | Description |
|-----------|------|-------------|
| **Salary** | Decimal | Annual salary of the employee. |
| **SalaryQuartile** | Text | Salary bucket (Q1 = lowest, Q4 = highest). |
| **MonthlyIncome** | Decimal | Monthly compensation derived from salary. |
| **PercentSalaryHike** | Decimal | YOY salary increase percentage (if applicable). |

---

# 🕒 4. Tenure & Experience Fields

| Field Name | Type | Description |
|-----------|------|-------------|
| **TenureYears** | Decimal | Total years employed measured from HireDate (calculated in SQL). |
| **TenureGroup** | Text | Categorized tenure bucket: <br> - **0–1 yrs (High Risk)** <br> - **1–3 yrs (Elevated Risk)** <br> - **3–6 yrs (Stable)** <br> - **6+ yrs (Low Risk)** |
| **YearsAtCompany** | Integer | Years of service based on HRIS data. |

---

# 🔥 5. Attrition Fields

| Field Name | Type | Description |
|-----------|------|-------------|
| **ExitFlag** | Boolean | 1 = Employee left the organization, 0 = Still active. |
| **AttritionType** | Text | Voluntary, Involuntary, Retirement, or N/A. |
| **ReasonForLeaving** | Text | If provided in HRIS (optional field). |

---

# 📊 6. Performance & HR Engagement Fields (if applicable)

| Field Name | Type | Description |
|-----------|------|-------------|
| **PerformanceScore** | Integer | HR performance evaluation rating. |
| **TrainingHours** | Integer | Hours of training completed. |
| **JobSatisfaction** | Integer | 1–4 rating based on employee survey. |

*(These fields appear only if included in extended datasets.)*

---

# 🧱 7. SQL Engineered Fields

These fields were created inside SQL during the feature engineering process.

| Field Name | Type | Description |
|-----------|------|-------------|
| **AgeGroup** | Text | Bucketed age category derived from Age. |
| **TenureYears** | Decimal | Calculated as DATEDIFF(year, HireDate, UTCDate). |
| **TenureGroup** | Text | Categorized tenure bucket based on TenureYears. |
| **SalaryQuartile** | Text | Quartile assignment using NTILE(4) or equivalently ranked salary distribution. |
| **IsActiveEmployee** | Boolean | Derived field to simplify filtering. |
| **ExitFlag** | Boolean | Derived from EmploymentStatus or TerminationDate. |

---

# 📐 8. Power BI Measures (DAX)

These measures power the KPIs in the dashboard.

| Measure | Description |
|--------|-------------|
| **Attrition Rate** | # of Exits / Average Headcount |
| **Total Employees** | COUNT(EmployeeID) |
| **Active Employees** | COUNT rows where IsActiveEmployee = 1 |
| **Avg Salary** | AVERAGE(Salary) |
| **Employees by Department** | COUNT(EmployeeID) grouped by Department |
| **Attrition by Tenure Group** | Exits grouped by TenureGroup |
| **Salary by Quartile** | Averages per SalaryQuartile |

Full DAX list is available in:  
`docs/DAX_measures.md`

---

# 🧭 9. Final Data Model Table: FactHR

This is the master table used by Power BI.

**FactHR Contains:**
- EmployeeID  
- Gender, Age, AgeGroup  
- Department, JobRole  
- Salary, SalaryQuartile  
- TenureYears, TenureGroup  
- Education, MaritalStatus  
- HireDate, TerminationDate  
- ExitFlag  
- IsActiveEmployee  

**Purpose:**  
Supports all attrition, compensation, diversity, and tenure analysis in the dashboard.

---

# 🎯 Purpose of This Data Dictionary

This document ensures:

- Transparency of all fields used  
- Easier model maintenance  
- Reproducible analytics pipelines  
- Recruiters & hiring managers understand your data modeling skills  
- Alignment between SQL, Power BI, and business logic  

---

# 📬 Contact

For questions or collaboration:  
**aarondatascientist@gmail.com**

