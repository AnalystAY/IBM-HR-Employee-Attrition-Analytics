# IBM HR Employee Attrition Analytics

### End-to-End HR Analytics Project | Excel | PostgreSQL | Power BI | DAX

![HR Analytics](https://img.shields.io/badge/Project-HR%20Analytics-blue)
![Excel](https://img.shields.io/badge/Tool-Excel-green)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-blue)
![Power BI](https://img.shields.io/badge/Visualization-Power%20BI-yellow)
![DAX](https://img.shields.io/badge/Language-DAX-orange)

---

## 📊 Project Snapshot

| Metric                  | Details                            |
| ----------------------- | ---------------------------------- |
| 👥 Employees Analyzed   | 1,470                              |
| 🎯 Business Focus       | Employee Attrition & Retention     |
| 🛠️ Tools               | Excel, PostgreSQL, Power BI, DAX   |
| 📄 Dashboard Pages      | 5                                  |
| ❓ HR Business Questions | 9                                  |
| 🔎 Analysis Type        | Descriptive & Diagnostic Analytics |
| ⚠️ Risk Analysis        | Rule-Based Risk Segmentation       |

---

## 📌 Executive Summary

Employee turnover is a significant challenge for organizations because high attrition can increase recruitment costs, reduce productivity, disrupt team performance, and create additional pressure on remaining employees.

This project analyzes the **IBM HR Analytics Employee Attrition & Performance** dataset to investigate the factors associated with employee attrition and identify workforce segments that may require targeted retention strategies.

The project follows an end-to-end analytics workflow:

**Excel → PostgreSQL → SQL Analysis → Power BI → DAX → HR Recommendations**

The analysis focuses on employee demographics, departments, job roles, compensation, overtime, employee experience, career progression, and other workforce characteristics associated with attrition.

The final deliverable is a five-page interactive Power BI dashboard designed to help HR leadership understand:

> **What is happening, where it is happening, what factors may be contributing to attrition, and where HR should focus retention efforts.**

---

# 🎯 Business Problem

The HR Director has observed increasing employee turnover and wants to understand:

> **Why are employees leaving, which workforce groups are most affected, and what actions can HR take to improve employee retention?**

The analysis was designed to provide evidence-based insights that can support HR workforce planning and retention discussions.

---

# ❓ Stakeholder Questions

The project addresses the following business questions:

1. What is the overall employee attrition rate?
2. Which departments lose the most employees?
3. Which job roles have the highest attrition?
4. Does overtime increase employee attrition?
5. Does salary affect employee retention?
6. Which age group experiences the highest attrition?
7. Does work-life balance influence attrition?
8. Which employees or employee groups meet the highest-risk criteria?
9. What recommendations can HR consider to reduce employee attrition?

---

# 🛠️ Tools & Technologies

## Microsoft Excel

Used for:

* Initial data inspection
* Data cleaning
* Data validation
* Helper columns
* Age grouping
* Salary band creation
* Tenure band creation
* Pivot table analysis
* Exploratory data analysis

## PostgreSQL

Used for:

* Relational data storage
* Table creation
* Data validation
* SQL-based exploratory analysis
* Business question analysis
* Aggregation and segmentation

## Power BI

Used for:

* Data modeling
* Interactive dashboard development
* KPI visualization
* Slicers and filtering
* Business storytelling
* Executive reporting

## DAX

Used for:

* KPI measures
* Attrition calculations
* Attrition rate
* Average salary
* Average age
* Average tenure
* Employee experience metrics
* Rule-based risk scoring

## GitHub

Used for:

* Project documentation
* SQL scripts
* DAX code
* Data analysis workflow
* Portfolio presentation
* Version control

---

# 📂 Dataset

### Dataset Name

**IBM HR Analytics Employee Attrition & Performance**

### Source

Kaggle

### Dataset Size

**1,470 employee records**

The dataset contains information across multiple workforce dimensions, including:

* Demographics
* Department
* Job role
* Education
* Business travel
* Compensation
* Overtime
* Job satisfaction
* Environment satisfaction
* Work-life balance
* Performance rating
* Career progression
* Tenure

---

# 🔄 Project Workflow

```text
                    RAW HR DATASET
                         │
                         ▼
                 EXCEL DATA CLEANING
                         │
                         ▼
              EXPLORATORY DATA ANALYSIS
                         │
                         ▼
                POSTGRESQL DATA LOAD
                         │
                         ▼
                 SQL BUSINESS ANALYSIS
                         │
                         ▼
                 POWER BI DATA MODEL
                         │
                         ▼
                DAX MEASURES & ANALYSIS
                         │
                         ▼
              INTERACTIVE HR DASHBOARD
                         │
                         ▼
               INSIGHTS & RECOMMENDATIONS
```

---

# 📊 Power BI Dashboard

The final Power BI report contains five analytical pages designed around the HR Director's decision-making journey.

---

## 01 — Executive Overview

### Business Question

> **What is happening with employee attrition?**

The Executive Overview provides a high-level view of workforce health and attrition patterns.

### Key KPIs

* Total Employees
* Attrition Count
* Attrition Rate
* Active Employees
* Average Salary
* Average Age
* Average Tenure
* Average Job Satisfaction

### Key Visuals

* Attrition by Department
* Attrition by Job Role
* Attrition by Age Group
* Attrition by Gender
* Attrition by Marital Status

### Interactive Filters

* Department
* Job Role
* Gender
* Age Group
* Salary Band
* Overtime
* Marital Status

---

## 02 — Department Analysis

### Business Question

> **Where is employee attrition concentrated?**

This page examines attrition across organizational structures.

### Key Analysis

* Attrition by Department
* Attrition by Job Role
* Attrition by Education Field
* Attrition by Business Travel
* Department-level comparisons

### Purpose

Identify departments and job roles that may require deeper investigation or targeted retention initiatives.

---

## 03 — Employee Experience

### Business Question

> **How does employee experience relate to attrition?**

This page analyzes employee satisfaction and workplace experience.

### Key Analysis

* Job Satisfaction
* Environment Satisfaction
* Work-Life Balance
* Relationship Satisfaction
* Performance Rating

### Purpose

Explore whether employee experience factors are associated with higher or lower attrition.

---

## 04 — Compensation Analysis

### Business Question

> **Does compensation influence employee retention?**

This page investigates compensation-related factors.

### Key Analysis

* Attrition by Salary Band
* Average Salary by Department
* Stock Options vs Attrition
* Salary Hike vs Attrition
* Monthly Income Distribution

### Purpose

Identify whether compensation and financial incentives may be associated with employee retention.

---

## 05 — Risk Analysis

### Business Question

> **Which employees or workforce segments meet the defined high-risk criteria?**

This page combines selected attrition-related factors into a rule-based risk segmentation framework.

### Key Analysis

* Overtime vs Attrition
* Attrition by Tenure Band
* Years Since Last Promotion
* Risk Factor Analysis
* Risk Level Distribution
* High-Risk Employee Table

### Purpose

Help HR identify workforce segments that may benefit from targeted retention interventions.

---

# 📐 Key DAX Measures

## Total Employees

```DAX
Total Employees =
COUNT(FactEmployee[EmployeeNumber])
```

## Attrition Count

```DAX
Attrition Count =
CALCULATE(
    COUNT(FactEmployee[EmployeeNumber]),
    FactEmployee[Attrition] = "Yes"
)
```

## Active Employees

```DAX
Active Employees =
[Total Employees] - [Attrition Count]
```

## Attrition Rate

```DAX
Attrition Rate =
DIVIDE(
    [Attrition Count],
    [Total Employees],
    0
)
```

## Average Salary

```DAX
Average Salary =
AVERAGE(FactEmployee[MonthlyIncome])
```

## Average Age

```DAX
Average Age =
AVERAGE(FactEmployee[Age])
```

## Average Tenure

```DAX
Average Tenure =
AVERAGE(FactEmployee[YearsAtCompany])
```

## Average Job Satisfaction

```DAX
Average Job Satisfaction =
AVERAGE(FactEmployee[JobSatisfaction])
```

---

# ⚠️ Risk Scoring Framework

A rule-based risk score was developed to segment employees based on selected attrition-related characteristics.

| Risk Factor                | Condition |  Points |
| -------------------------- | --------- | ------: |
| Overtime                   | Yes       |      30 |
| Job Satisfaction           | ≤ 2       |      25 |
| Work-Life Balance          | ≤ 2       |      20 |
| Monthly Income             | < 5,000   |      15 |
| Years Since Last Promotion | ≥ 5       |      10 |
| **Maximum Score**          |           | **100** |

### Risk Classification

| Risk Score | Risk Level  |
| ---------- | ----------- |
| 0–39       | Low Risk    |
| 40–69      | Medium Risk |
| 70–100     | High Risk   |

### DAX Implementation

```DAX
Risk Score =
IF(FactEmployee[OverTime] = "Yes", 30, 0)
+
IF(FactEmployee[JobSatisfaction] <= 2, 25, 0)
+
IF(FactEmployee[WorkLifeBalance] <= 2, 20, 0)
+
IF(FactEmployee[MonthlyIncome] < 5000, 15, 0)
+
IF(FactEmployee[YearsSinceLastPromotion] >= 5, 10, 0)
```

### Risk Level

```DAX
Risk Level =
SWITCH(
    TRUE(),
    FactEmployee[Risk Score] >= 70, "High Risk",
    FactEmployee[Risk Score] >= 40, "Medium Risk",
    "Low Risk"
)
```

> **Important:** The risk score is a rule-based analytical segmentation framework created for this portfolio project. It is not a predictive machine-learning model and should not be interpreted as a probability that an individual employee will leave.

---
# 🔎 Key Findings

### Finding 1 — Overall Attrition

The overall employee attrition rate was **16.12%**, with **237 employees leaving out of 1,470 employees** in the dataset.

This indicates that approximately **1 in 6 employees** in the analyzed workforce had left the organization, highlighting the importance of understanding the factors associated with employee turnover and developing targeted retention strategies.

---

### Finding 2 — Department Attrition

The **Sales department** recorded the highest attrition rate at approximately **20.63%**, with **92 employees leaving out of 446 employees**.

This suggests that HR should investigate department-specific factors such as workload, overtime, compensation, management practices, job satisfaction, and career progression within Sales.

The **Human Resources department** followed with an attrition rate of approximately **19.05%**, while **Research & Development** recorded a lower attrition rate of approximately **13.84%**.

---

### Finding 3 — Job Role Attrition

The **Sales Representative** role recorded the highest attrition rate at approximately **39.76%**, with **33 employees leaving out of 83 employees**.

This is substantially higher than the overall organizational attrition rate of 16.12% and indicates that Sales Representatives represent a particularly vulnerable workforce segment.

HR should investigate factors such as workload, overtime, compensation, career progression, job satisfaction, and the employee experience associated with this role.

---

### Finding 4 — Overtime

Employees working overtime demonstrated an attrition rate of approximately **30.53%**, compared with **10.44%** among employees who did not work overtime.

This represents a difference of approximately **20 percentage points** and indicates a strong association between overtime and employee attrition in this dataset.

The finding suggests that workload, employee burnout, and work-life balance may be important areas for HR retention planning.

---

### Finding 5 — Compensation

Employees in the **Low Salary Band** experienced the highest attrition rate at approximately **21.76%**, compared with **11.14%** for the Medium Salary Band and **8.90%** for the High Salary Band.

This pattern suggests that lower-paid employees may experience greater turnover and that compensation competitiveness and internal pay equity should be considered when developing retention strategies.

However, salary should be evaluated alongside other factors such as overtime, job satisfaction, career progression, and job role rather than being considered the sole cause of attrition.

---

### Finding 6 — Age Group

The **18–25 age group** recorded the highest attrition rate at approximately **35.77%**, with **44 employees leaving out of 123 employees**.

This was followed by the **26–35 age group**, which recorded an attrition rate of approximately **19.14%**.

The relatively high attrition among younger employees may indicate an opportunity for targeted engagement, career development, mentorship, compensation, and early-career retention strategies.

---

### Finding 7 — Employee Experience

Employees reporting the lowest **Job Satisfaction** score of 1 recorded an attrition rate of approximately **22.84%**, compared with **11.33%** among employees with the highest Job Satisfaction score of 4.

Similarly, employees with the lowest **Work-Life Balance** score of 1 recorded an attrition rate of approximately **31.25%**.

These findings suggest that employee experience, particularly job satisfaction and work-life balance, should be considered alongside compensation and workload when developing employee retention initiatives.

---

### Finding 8 — Risk Segmentation

Employees classified as **High Risk** based on the project's rule-based risk framework demonstrated an observed attrition rate of approximately **36.96%**, with **17 of 46 high-risk employees leaving**.

This compares with an attrition rate of approximately **22.87%** among Medium Risk employees and **7.14%** among Low Risk employees.

The results show a clear relationship between the project's risk classification and observed historical attrition, with the High Risk group experiencing more than five times the attrition rate of the Low Risk group.

This provides initial evidence that the risk framework is useful for identifying employee groups with elevated historical attrition. However, the risk score should be treated as an analytical segmentation tool rather than a predictive model or probability of individual employee departure.



---

# 💡 HR Recommendations

Recommendations should be aligned with the final analysis results.

### 1. Review Overtime and Workload

Where overtime is strongly associated with attrition, HR should review workload distribution, staffing levels, and employee burnout risks.

### 2. Strengthen Career Progression

Employees experiencing long periods without promotion may benefit from clearer career pathways, development programs, and internal mobility opportunities.

### 3. Review Compensation

Employee groups experiencing high attrition alongside lower compensation should be evaluated against internal pay structures and external market benchmarks.

### 4. Improve Employee Experience

Where satisfaction and work-life balance are associated with higher attrition, HR should consider targeted engagement initiatives and manager-led interventions.

### 5. Target High-Risk Workforce Segments

HR should prioritize retention programs toward employee segments that demonstrate multiple risk factors rather than applying broad interventions across the entire workforce.

### 6. Establish Continuous Attrition Monitoring

Organizations should monitor attrition metrics regularly and create recurring HR dashboards to identify emerging turnover patterns.

---

# 📈 Recommended HR Actions

| Priority | Action                               | Target                             |
| -------- | ------------------------------------ | ---------------------------------- |
| High     | Review overtime and workload         | High-overtime employee groups      |
| High     | Investigate high-attrition job roles | Department and role leaders        |
| Medium   | Review compensation                  | Low-income/high-attrition groups   |
| Medium   | Strengthen career progression        | Employees with long promotion gaps |
| Medium   | Improve work-life balance            | Low work-life balance groups       |
| Ongoing  | Monitor attrition KPIs               | HR Leadership                      |

---

# 🗂️ Project Structure

```text
IBM-HR-Employee-Attrition-Analytics/
│
├── README.md
│
├── 01_Data/
│   ├── raw/
│   │   └── HR_Employee_Attrition.csv
│   │
│   └── cleaned/
│       └── IBM_HR_Employee_Attrition_Cleaned.xlsx
│
├── 02_Excel_Analysis/
│   ├── IBM_HR_Excel_Analysis.xlsx
│   ├── Excel_Dashboard.png
│   └── README.md
│
├── 03_SQL_Analysis/
│   ├── 01_create_table.sql
│   ├── 02_data_quality_checks.sql
│   ├── 03_hr_business_questions.sql
│   └── README.md
│
├── 04_PowerBI/
│   ├── IBM_HR_Attrition_Dashboard.pbix
│   │
│   ├── Dashboard_Screenshots/
│   │   ├── 01_Executive_Overview.png
│   │   ├── 02_Department_Analysis.png
│   │   ├── 03_Employee_Experience.png
│   │   ├── 04_Compensation_Analysis.png
│   │   └── 05_Risk_Analysis.png
│   │
│   └── README.md
│
├── 05_DAX/
│   ├── measures.dax
│   ├── calculated_columns.dax
│   └── README.md
│
├── 06_Insights/
│   ├── HR_Executive_Summary.pdf
│   ├── Key_Findings.md
│   └── HR_Recommendations.md
│
└── 07_Documentation/
    ├── Data_Dictionary.xlsx
    ├── Data_Model.png
    └── Project_Methodology.md
```

---

# 🚀 Future Improvements

Potential extensions to this project include:

* Build a predictive employee attrition model using Python
* Use machine learning to estimate attrition probability
* Compare rule-based risk scores with model predictions
* Develop employee-level attrition probability scores
* Add time-based HR attrition monitoring
* Integrate real-world HRIS data
* Build automated Power BI data refresh pipelines
* Develop a workforce retention ROI analysis

---

# 📌 Project Limitations

This analysis is based on a static historical dataset and therefore has several limitations:

* The dataset does not represent a live organizational workforce.
* Observed relationships do not necessarily imply causation.
* The rule-based risk score is a portfolio analytical framework and is not a validated predictive model.
* The analysis does not include qualitative employee feedback.
* External labor market conditions and organizational policies are not included.

Therefore, findings should be interpreted as **analytical insights and potential areas for HR investigation**, rather than definitive explanations for why individual employees leave.

---

# 👤 About This Project

This project demonstrates an end-to-end approach to solving a real-world HR analytics problem using data preparation, SQL, business analysis, Power BI, and DAX.

The focus is not only on creating visualizations but on translating workforce data into insights that can support **employee retention, workforce planning, and HR decision-making**.

---

## ⭐ If You Found This Project Useful

Feel free to explore the repository and connect with me on GitHub.

**Skills Demonstrated:**

`Data Cleaning` · `Excel` · `SQL` · `PostgreSQL` · `Power BI` · `DAX` · `Data Modeling` · `HR Analytics` · `Business Intelligence` · `Data Storytelling`
