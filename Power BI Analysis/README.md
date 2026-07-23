# 📈 Power BI Dashboard — IBM HR Employee Attrition

## Overview

Power BI was used to transform the results of the Excel and PostgreSQL analysis into an interactive HR analytics dashboard.

The dashboard is designed for the HR Director and provides an end-to-end view of employee attrition, employee experience, compensation, and workforce risk.

---

## 🎯 Business Objective

The dashboard helps HR leadership understand:

> **What is happening with employee attrition, where it is concentrated, what factors are associated with turnover, and which workforce segments may require targeted retention attention?**

---

## 🛠️ Tools Used

* Microsoft Power BI
* Power Query
* DAX
* Data Modeling
* Interactive Visualizations
* Slicers
* Drill-through
* Report Navigation

---

## 🔄 Power BI Workflow

```text
Excel / PostgreSQL
       ↓
Power Query
       ↓
Data Transformation
       ↓
Data Model
       ↓
DAX Measures
       ↓
Calculated Columns
       ↓
Interactive Visualizations
       ↓
HR Dashboard
```

---

# ⭐ Dashboard Structure

The report contains five analytical pages.

---

## Page 1 — Executive Overview

### Business Question

> What is happening with employee attrition?

### KPIs

* Total Employees
* Attrition Count
* Attrition Rate
* Active Employees
* Average Salary
* Average Age
* Average Tenure
* Average Job Satisfaction

### Visuals

* Attrition by Department
* Attrition by Gender
* Attrition by Age Group
* Attrition by Marital Status

### Purpose

Provide HR leadership with a high-level overview of workforce attrition.

---

## Page 2 — Department Analysis

### Business Question

> Where is employee attrition concentrated?

### Visuals

* Attrition by Job Role
* Attrition by Education Field
* Attrition by Business Travel
* Department-level analysis

### Purpose

Identify departments and job roles that may require deeper investigation.

---

## Page 3 — Employee Experience

### Business Question

> How does employee experience relate to attrition?

### Visuals

* Job Satisfaction vs Attrition
* Environment Satisfaction vs Attrition
* Work-Life Balance vs Attrition
* Relationship Satisfaction vs Attrition
* Performance Rating vs Attrition

### Purpose

Understand how workplace experience and satisfaction relate to employee retention.

---

## Page 4 — Compensation Analysis

### Business Question

> Does compensation influence employee retention?

### Visuals

* Attrition by Salary Band
* Average Salary by Department
* Stock Option Level vs Attrition
* Salary Hike vs Attrition
* Monthly Income Distribution
* Compensation Summary Matrix

### Purpose

Investigate whether compensation and financial incentives are associated with employee turnover.

---

## Page 5 — Risk Analysis

### Business Question

> Which employees or workforce segments meet the defined high-risk criteria?

### Visuals

* Overtime vs Attrition
* Attrition by Tenure Band
* Years Since Last Promotion vs Attrition
* Risk Factor Analysis
* Risk Level Distribution
* High-Risk Employee Table

### Purpose

Identify employees or employee segments that meet multiple predefined attrition-related risk criteria.

---

# 🎛️ Interactive Features

The dashboard includes interactive slicers for:

* Department
* Job Role
* Gender
* Age Group
* Salary Band
* Tenure Band
* Overtime
* Marital Status

These allow HR users to explore attrition patterns across different workforce segments.

---

# 📐 Core DAX Measures

The dashboard includes DAX measures for:

* Total Employees
* Attrition Count
* Active Employees
* Attrition Rate
* Average Salary
* Average Age
* Average Tenure
* Average Job Satisfaction
* Average Salary Hike
* Average Stock Option

---

# ⚠️ Risk Analysis

A rule-based risk scoring framework was developed using selected factors:

| Risk Factor                | Condition | Points |
| -------------------------- | --------- | -----: |
| Overtime                   | Yes       |     30 |
| Job Satisfaction           | ≤ 2       |     25 |
| Work-Life Balance          | ≤ 2       |     20 |
| Monthly Income             | < 5,000   |     15 |
| Years Since Last Promotion | ≥ 5       |     10 |

### Risk Levels

* Low Risk: 0–39
* Medium Risk: 40–69
* High Risk: 70–100

The risk score is intended to support workforce segmentation and exploratory analysis.

It is not a predictive model and should not be interpreted as a probability of individual employee attrition.

---

# 📊 Dashboard Design Principles

The dashboard was designed using the following principles:

### Executive Focus

KPIs and high-level visuals provide immediate visibility into workforce attrition.

### Interactive Exploration

Slicers allow HR stakeholders to investigate specific workforce segments.

### Consistent Storytelling

The five pages follow a logical analytical journey:

```text
What is happening?
        ↓
Where is it happening?
        ↓
How does employee experience relate?
        ↓
Does compensation relate?
        ↓
Which groups meet high-risk criteria?
```

### Action-Oriented Analysis

The dashboard focuses on insights that can support:

* Retention planning
* Workforce planning
* Employee engagement
* Compensation review
* Career development
* Work-life balance initiatives

---

# 💡 Business Impact

The Power BI dashboard provides HR leadership with a centralized analytical view of employee attrition.

It enables stakeholders to:

* Monitor attrition KPIs
* Identify high-attrition departments
* Investigate high-risk job roles
* Explore employee experience factors
* Examine compensation patterns
* Segment employees using a rule-based risk framework
* Develop targeted retention strategies

---

# 📁 Power BI Deliverables

### `IBM_HR_Attrition_Dashboard.pbix`

The complete interactive Power BI report.

### `Dashboard_Screenshots/`

Contains screenshots of the five dashboard pages for portfolio presentation.

```text
Dashboard_Screenshots/
│
├── 01_Executive_Overview.png
├── 02_Department_Analysis.png
├── 03_Employee_Experience.png
├── 04_Compensation_Analysis.png
└── 05_Risk_Analysis.png
```

---

# 🔗 Project Navigation

| Project Stage      | Repository Folder   |
| ------------------ | ------------------- |
| Data Preparation   | `01_Data`           |
| Excel Analysis     | `02_Excel_Analysis` |
| SQL Analysis       | `03_SQL_Analysis`   |
| Power BI Dashboard | `04_PowerBI`        |
| DAX                | `05_DAX`            |
| Insights           | `06_Insights`       |

---

# 🚀 Future Improvements

Future versions of this project could include:

* Predictive attrition modeling using Python
* Machine learning-based attrition probability
* Employee-level prediction scores
* Model validation and performance metrics
* Automated Power BI refresh
* Real-time HR data integration
* Retention ROI analysis

---

## 👤 Portfolio Project

This project demonstrates an end-to-end HR analytics workflow combining:

`Excel` · `SQL` · `PostgreSQL` · `Power BI` · `DAX` · `Data Modeling` · `Business Intelligence` · `Data Storytelling`

The goal is to demonstrate how employee data can be transformed into actionable insights that support HR decision-making and employee retention strategies.
