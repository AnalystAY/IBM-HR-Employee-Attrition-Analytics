# 🗄️ SQL Analysis — IBM HR Employee Attrition

## Overview

PostgreSQL was used to perform structured data analysis on the IBM HR Employee Attrition dataset.

The SQL stage transformed the cleaned Excel dataset into a relational database environment and provided a structured approach to answering the HR Director's business questions.

---

## 🎯 Business Objective

The goal of the SQL analysis was to identify patterns and relationships associated with employee attrition and provide evidence for HR retention strategies.

The analysis focused on:

* Attrition rate
* Department-level attrition
* Job role attrition
* Overtime
* Compensation
* Age
* Work-life balance
* Employee experience
* Career progression

---

## 🛠️ Tools Used

* PostgreSQL
* pgAdmin 4
* SQL

---

## 📂 Dataset

**Dataset:** IBM HR Analytics Employee Attrition & Performance

**Records:** 1,470 employees

---

## 🔄 SQL Workflow

```text
Cleaned Excel Dataset
        ↓
CSV Export
        ↓
PostgreSQL Database
        ↓
Table Creation
        ↓
Data Import
        ↓
Data Quality Checks
        ↓
SQL Business Queries
        ↓
Insights
```

---

## 🗃️ Database Table

The primary table is:

`employee_attrition`

The table contains employee demographic, employment, compensation, satisfaction, and performance information.

Key fields include:

* EmployeeNumber
* Age
* Attrition
* Department
* JobRole
* MonthlyIncome
* OverTime
* JobSatisfaction
* EnvironmentSatisfaction
* WorkLifeBalance
* YearsAtCompany
* YearsSinceLastPromotion
* StockOptionLevel
* PercentSalaryHike

---

## 🧪 Data Quality Checks

SQL queries were used to validate:

* Total row count
* Duplicate EmployeeNumber values
* NULL values
* Distinct categorical values
* Attrition values
* Department values
* Job role values
* Salary ranges
* Age ranges

Example:

```sql
SELECT COUNT(*)
FROM employee_attrition;
```

---

## 📊 Business Questions

SQL queries were developed to answer:

### 1. Overall Attrition Rate

Determine the percentage of employees who left the organization.

### 2. Department Attrition

Identify departments with the highest employee attrition.

### 3. Job Role Attrition

Identify job roles experiencing the highest turnover.

### 4. Overtime and Attrition

Compare attrition between employees who work overtime and those who do not.

### 5. Salary and Retention

Analyze whether lower-income employee groups experience higher attrition.

### 6. Age and Attrition

Identify age groups with the highest attrition.

### 7. Work-Life Balance

Analyze the relationship between work-life balance ratings and employee attrition.

### 8. Employee Experience

Analyze job satisfaction and environment satisfaction in relation to attrition.

### 9. Career Progression

Investigate whether employees with longer periods since their last promotion experience higher attrition.

---

## 🔍 SQL Techniques Demonstrated

The project demonstrates:

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `COUNT()`
* `AVG()`
* `SUM()`
* `CASE`
* `COUNT(CASE WHEN...)`
* `NULLIF()`
* `ROUND()`
* Subqueries
* Aggregation
* Conditional analysis

---

## 📌 Example SQL Analysis

### Attrition by Department

```sql
SELECT
    "Department",
    COUNT(*) AS total_employees,
    COUNT(CASE WHEN "Attrition" = 'Yes' THEN 1 END) AS attrition_count,
    ROUND(
        COUNT(CASE WHEN "Attrition" = 'Yes' THEN 1 END) * 100.0
        / COUNT(*),
        2
    ) AS attrition_rate
FROM employee_attrition
GROUP BY "Department"
ORDER BY attrition_rate DESC;
```

---

## 💡 Business Value

The SQL analysis provides a structured foundation for:

* Identifying high-attrition departments
* Identifying high-risk job roles
* Understanding compensation patterns
* Evaluating overtime-related turnover
* Supporting HR retention decisions

The SQL results were subsequently used to validate the Power BI dashboard analysis.

---

## 📁 SQL Deliverables

### `01_create_table.sql`

Creates the `employee_attrition` table.

### `02_data_quality_checks.sql`

Contains data validation and quality assurance queries.

### `03_hr_business_questions.sql`

Contains SQL queries answering the HR Director's stakeholder questions.

---

## 🔗 Next Stage

The validated dataset and SQL findings were used to develop the interactive Power BI dashboard.

**Next:** `04_PowerBI`
