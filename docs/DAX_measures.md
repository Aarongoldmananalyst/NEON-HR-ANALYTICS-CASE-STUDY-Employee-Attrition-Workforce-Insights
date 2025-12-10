# 📐 DAX Measures
This document provides all DAX measures used in the **Neon HR Analytics Case Study**.  
Measures are organized by analytical category to enhance clarity, transparency, and reusability across the Power BI model.

These metrics translate raw SQL outputs into dynamic KPIs that power the dashboard.

---

# 🧮 1. Headcount Metrics

### **Total Employees**
```DAX
Total Employees :=
COUNTROWS(FactHR)
Active Employees
DAX
Copy code
Active Employees :=
CALCULATE(
    [Total Employees],
    FactHR[IsActiveEmployee] = 1
)
Terminated Employees
DAX
Copy code
Terminated Employees :=
CALCULATE(
    [Total Employees],
    FactHR[IsActiveEmployee] = 0
)
🔥 2. Attrition Metrics
Attrition Count
DAX
Copy code
Attrition Count :=
CALCULATE(
    COUNTROWS(FactHR),
    FactHR[ExitFlag] = 1
)
Attrition Rate
DAX
Copy code
Attrition Rate :=
DIVIDE(
    [Attrition Count],
    [Total Employees]
)
Attrition by Department
DAX
Copy code
Attrition by Department :=
CALCULATE(
    [Attrition Count],
    ALLEXCEPT(FactHR, FactHR[Department])
)
Attrition by Tenure Group
DAX
Copy code
Attrition by Tenure Group :=
CALCULATE(
    [Attrition Count],
    ALLEXCEPT(FactHR, FactHR[TenureGroup])
)
💰 3. Compensation Measures
Average Salary
DAX
Copy code
Average Salary :=
AVERAGE(FactHR[Salary])
Average Salary by Department
DAX
Copy code
Average Salary by Department :=
CALCULATE(
    [Average Salary],
    ALLEXCEPT(FactHR, FactHR[Department])
)
Employees by Salary Quartile
DAX
Copy code
Employees by Salary Quartile :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[SalaryQuartile])
)
🧭 4. Tenure Insights
Average Tenure
DAX
Copy code
Average Tenure :=
AVERAGE(FactHR[TenureYears])
Employees by Tenure Group
DAX
Copy code
Employees by Tenure Group :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[TenureGroup])
)
Exit Count by Tenure Group
DAX
Copy code
Exit Count by Tenure Group :=
CALCULATE(
    [Attrition Count],
    ALLEXCEPT(FactHR, FactHR[TenureGroup])
)
👥 5. Workforce Composition Measures
Employees by Gender
DAX
Copy code
Employees by Gender :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[Gender])
)
Employees by Age Group
DAX
Copy code
Employees by Age Group :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[AgeGroup])
)
Employees by Education Level
DAX
Copy code
Employees by Education Level :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[EducationLevel])
)
🏢 6. Department Measures
Headcount by Department
DAX
Copy code
Headcount by Department :=
CALCULATE(
    [Total Employees],
    ALLEXCEPT(FactHR, FactHR[Department])
)
Attrition Rate by Department
DAX
Copy code
Attrition Rate by Department :=
DIVIDE(
    [Attrition by Department],
    [Headcount by Department]
)
🎯 7. KPI Formatting
Attrition Rate (%)
DAX
Copy code
Attrition Rate % :=
FORMAT([Attrition Rate], "0.00%")
Formatted Headcount
DAX
Copy code
Headcount :=
FORMAT([Total Employees], "#,0")
📊 8. Visual Slicer / Filter Helpers
Is Active Filter
DAX
Copy code
Is Active Filter :=
IF(FactHR[IsActiveEmployee] = 1, "Active", "Terminated")
Attrition Type Filter
DAX
Copy code
Attrition Type Filter :=
FactHR[AttritionType]
📚 Summary of DAX Coverage
Category	Key Measures Included
Headcount	Total, Active, Terminated
Attrition	Count, Rate, Dept/Tenure analysis
Compensation	Average Pay, Salary Quartiles
Tenure	Avg Tenure, Tenure Risk Analysis
Workforce	Gender, AgeGroup, Education
Department	Headcount + Attrition Relationships

These measures form the analytical backbone of the Neon HR Analytics dashboard.

🧠 Why These Measures Matter
Enable interactive, filter-responsive visualizations

Translate SQL fields into executive-level KPIs

Power the attrition, tenure, and compensation insights

Follow BI best practices for performance and clarity

Strengthen your portfolio by demonstrating DAX proficiency

📬 Contact
For questions or collaboration:
aarondatascientist@gmail.com
