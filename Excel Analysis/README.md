# 📊 Excel Analysis — IBM HR Employee Attrition

## Overview

Microsoft Excel was used as the first stage of the IBM HR Employee Attrition Analytics project.

The objective of the Excel analysis was to inspect, clean, transform, and explore the HR dataset before loading it into PostgreSQL and Power BI.

This stage established the foundation for the subsequent SQL analysis and Power BI dashboard.

---

## 🎯 Business Objective

The HR Director wants to understand the factors associated with employee attrition and identify areas where HR can focus retention efforts.

The Excel analysis focused on identifying patterns in:

* Employee attrition
* Department
* Job role
* Age
* Salary
* Overtime
* Job satisfaction
* Work-life balance
* Career progression
* Employee tenure

---

## 🛠️ Tools Used

* Microsoft Excel
* Excel Tables
* PivotTables
* PivotCharts
* Excel formulas
* Data validation
* Conditional formatting

---

## 📂 Dataset

**Dataset:** IBM HR Analytics Employee Attrition & Performance

**Records:** 1,470 employees

The dataset contains employee information across demographic, job, compensation, satisfaction, and employment dimensions.

---

## 🔄 Excel Workflow

```text
Raw Dataset
     ↓
Data Inspection
     ↓
Data Cleaning
     ↓
Data Transformation
     ↓
Helper Columns
     ↓
PivotTable Analysis
     ↓
Exploratory Data Analysis
     ↓
Export Clean Dataset
```

---

## 🧹 Data Cleaning

The following checks were performed:

* Reviewed column names
* Checked for missing values
* Checked for duplicate records
* Verified data types
* Confirmed categorical values
* Reviewed numerical fields
* Confirmed `EmployeeNumber` uniqueness
* Verified `Attrition` values
* Checked salary and age fields
* Reviewed potential outliers

---

## 🔧 Data Transformation

Additional analytical fields were created to support HR analysis.

### Age Group

Employees were grouped into age categories to analyze attrition across different workforce generations.

Example:

* Under 25
* 25–34
* 35–44
* 45–54
* 55+

---

### Salary Band

Monthly income was categorized into salary groups.

Example:

* Low
* Medium
* High

The salary band was created to make compensation analysis easier to interpret.

---

### Tenure Band

Employees were grouped according to years at the company.

| Years at Company | Tenure Band |
| ---------------- | ----------- |
| 0–2              | New         |
| 3–5              | Growing     |
| 6–10             | Experienced |
| 10+              | Veteran     |

---

### Salary Hike Band

`PercentSalaryHike` was grouped into broader categories to simplify visualization.

Example:

* 11–15%
* 16–20%
* 21–25%

---

## 📌 Exploratory Analysis

PivotTables were used to investigate:

* Overall attrition
* Attrition by department
* Attrition by job role
* Attrition by gender
* Attrition by age group
* Attrition by marital status
* Attrition by overtime
* Attrition by salary band
* Attrition by work-life balance
* Attrition by job satisfaction
* Attrition by tenure

---

## 📊 Key Excel Outputs

The Excel analysis produced:

* Cleaned HR dataset
* Helper columns
* Attrition PivotTables
* Compensation analysis
* Employee experience analysis
* Tenure analysis
* Preliminary risk analysis

---

## 💡 Business Questions Explored

The Excel analysis provided an initial view of the following stakeholder questions:

1. What is the overall attrition rate?
2. Which departments lose the most employees?
3. Which job roles have the highest attrition?
4. Does overtime increase attrition?
5. Does salary affect employee retention?
6. Which age group resigns the most?
7. Does work-life balance influence attrition?

The results from Excel were later validated and expanded through PostgreSQL and Power BI.

---

## 📁 Excel Deliverable

The main workbook is:

`IBM_HR_Excel_Analysis.xlsx`

The workbook contains the cleaned dataset, helper columns, PivotTables, and exploratory analysis.

---

## 🔗 Next Stage

After completing the Excel analysis, the cleaned dataset was loaded into PostgreSQL for structured SQL analysis.

**Next:** `03_SQL_Analysis`
