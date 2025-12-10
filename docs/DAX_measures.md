# 📐 DAX Measures
This page lists all DAX measures used in the **Neon HR Analytics Case Study**, grouped by analytics category.  
The structure and formatting match the SQL Scripts documentation for a consistent professional presentation.

---

# 1️⃣ Headcount Metrics

### 🔹 Total Employees
```DAX
Total Employees :=
COUNTROWS(FactHR)
```

### 🔹 Active Employees
```DAX
Active Employees :=
CALCULATE(
    [Total Employees],
    FactHR[IsActiveEmployee] = 1
)
```

### 🔹 Terminated Employees
```DAX
Terminated Employees :=
CALCULATE(
    [Total Employees],
    FactHR[IsActiveEmployee] = 0
)
```

---

# 2️⃣ Attrition Metrics

### 🔹 Attrition Count
```DAX
Attrition Count :=
CALCULATE(
    COUNTROWS(FactHR),
    FactHR[ExitFlag] = 1
)
```

### 🔹 Attrition Rate
```DAX
Attrition Rate :=
DIVIDE(
    [Attrition Count],
    [Total Employees]
)
```

### 🔹 Attrition by Department
```DAX
Attrition by Department :=
CALCULATE(
    [Attrition Count],
    ALLEXCEPT(FactHR, FactHR[Department])
)
```

### 🔹 Attrition by Tenure Group
```DAX
Attrition by Tenure Group :=
CALCULATE(
    [Attrition Count],
    ALLEXCEPT(FactHR, FactHR[TenureGroup])
)
```

---

# 3️⃣ Compensation Measures

### 🔹 Average Salary
```DAX
Average Salary :=
AVERAGE(FactHR[Salary])
```

### 🔹 Average Salary by Department
```DAX
Average Salary by Department :=
CALCULATE(
    [Average Salary],
    ALLEXCEPT(FactHR, FactHR[Department])
)
```

### 🔹 Employees by Salary Quartile
```DAX
Employees by Salary Quartile :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[SalaryQuartile])
)
```

---

# 4️⃣ Tenure Insights

### 🔹 Average Tenure
```DAX
Average Tenure :=
AVERAGE(FactHR[TenureYears])
```

### 🔹 Employees by Tenure Group
```DAX
Employees by Tenure Group :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[TenureGroup])
)
```

### 🔹 Exit Count by Tenure Group
```DAX
Exit Count by Tenure Group :=
CALCULATE(
    [Attrition Count],
    ALLEXCEPT(FactHR, FactHR[TenureGroup])
)
```

---

# 5️⃣ Workforce Composition

### 🔹 Employees by Gender
```DAX
Employees by Gender :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[Gender])
)
```

### 🔹 Employees by Age Group
```DAX
Employees by Age Group :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[AgeGroup])
)
```

### 🔹 Employees by Education Level
```DAX
Employees by Education Level :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[EducationLevel])
)
```

---

# 6️⃣ Department Performance

### 🔹 Headcount by Department
```DAX
Headcount by Department :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[Department])
)
```

### 🔹 Attrition Rate by Department
```DAX
Attrition Rate by Department :=
DIVIDE(
    [Attrition by Department],
    [Headcount by Department]
)
```

---

# 7️⃣ KPI Formatting

### 🔹 Attrition Rate (%)
```DAX
Attrition Rate % :=
FORMAT([Attrition Rate], "0.00%")
```

### 🔹 Formatted Headcount
```DAX
Headcount :=
FORMAT([Total Employees], "#,0")
```

---

# 8️⃣ Slicer / Filter Helpers

### 🔹 Is Active Filter
```DAX
Is Active Filter :=
IF(FactHR[IsActiveEmployee] = 1, "Active", "Terminated")
```

### 🔹 Attrition Type Filter
```DAX
Attrition Type Filter :=
FactHR[AttritionType]
```

---

# 📚 Summary of What These Measures Support
- Headcount reporting  
- Attrition analysis  
- Compensation insights  
- Tenure risk analytics  
- Workforce diversity  
- Department performance  

These measures collectively power the **Neon HR Analytics Dashboard**.

---

# 📬 Need Help?
For questions or collaboration:  
**aarondatascientist@gmail.com**
