<div align="center">

# HR Workforce Analytics BI Solution

### SQL Server • Power BI • SSIS • SSRS • DAX • Data Modelling

[![SQL Server](https://img.shields.io/badge/SQL_Server-Database_Development-blue)]()
[![Power BI](https://img.shields.io/badge/Power_BI-Business_Intelligence-yellow)]()
[![SSIS](https://img.shields.io/badge/SSIS-ETL-green)]()
[![SSRS](https://img.shields.io/badge/SSRS-Reporting-red)]()
[![Star Schema](https://img.shields.io/badge/Data_Model-Star_Schema-orange)]()
[![Status](https://img.shields.io/badge/Status-In_Progress-success)]()

**An end-to-end Business Intelligence solution for workforce analytics, employee attrition analysis, compensation reporting, and executive decision support.**

</div>

---

# Project Overview

This project demonstrates the complete Business Intelligence development lifecycle using SQL Server, Power BI, SSIS, and SSRS.

The solution transforms raw HR data into actionable business insights through data modelling, ETL processes, reporting, dashboard development, and workforce analytics.

The objective is to provide management with visibility into employee retention, workforce composition, departmental performance, and compensation trends.

---

# Business Problem

Human Resources teams require reliable reporting to understand:

* Workforce composition
* Employee turnover
* Attrition risk
* Compensation trends
* Department performance
* Workforce planning opportunities

Without effective reporting, organisations may struggle to identify retention challenges and workforce risks before they impact business performance.

---

# Solution Architecture

```text
                    ┌───────────────────┐
                    │   Raw HR Dataset  │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │   SQL Server DB   │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Data Cleaning &   │
                    │ Data Validation   │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │  Star Schema Data │
                    │      Model        │
                    └─────────┬─────────┘
                              │
          ┌───────────────────┼───────────────────┐
          ▼                   ▼                   ▼

 ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
 │    SSIS     │     │   Power BI  │     │    SSRS     │
 │ ETL Process │     │ Dashboards  │     │ Reports     │
 └─────────────┘     └─────────────┘     └─────────────┘

                              │
                              ▼

                    ┌───────────────────┐
                    │ Business Insights │
                    └───────────────────┘
```

---

# Technology Stack

| Technology | Purpose                         |
| ---------- | ------------------------------- |
| SQL Server | Database Development            |
| SSMS       | SQL Development                 |
| Power BI   | Dashboard Development           |
| DAX        | KPI Calculations                |
| SSIS       | ETL Automation                  |
| SSRS       | Paginated Reporting             |
| Draw.io    | Data Modelling                  |
| GitHub     | Documentation & Version Control |

---

# BI Development Lifecycle

## Business Requirements

Define workforce reporting requirements and KPI needs.

## Data Modelling

Design a Star Schema data warehouse.

## ETL Development

Use SQL and SSIS to transform and load data.

## Reporting

Build analytical dashboards and operational reports.

## Testing

Validate data quality and reporting accuracy.

## Deployment

Publish dashboards and reporting solutions.

---

# Star Schema Design

## Fact Table

### FactEmployeeMetrics

Measures:

* Monthly Income
* Years At Company
* Total Working Years
* Training Times Last Year
* Percent Salary Hike

---

## Dimension Tables

### DimEmployee

* Employee ID
* Age
* Gender
* Marital Status
* Business Travel

### DimDepartment

* Department

### DimJobRole

* Job Role

### DimEducation

* Education Level
* Education Field

### DimDate

* Reporting Date

---

# Dashboard Pages

## Executive Summary

### KPIs

✅ Total Employees

✅ Active Employees

✅ Attrition Count

✅ Attrition Rate

✅ Average Income

✅ Average Employee Tenure

---

## Workforce Analysis

### Insights

* Employees by Department
* Employees by Job Role
* Gender Distribution
* Education Analysis
* Workforce Demographics

---

## Attrition Analysis

### Insights

* Attrition by Department
* Attrition by Job Role
* Attrition by Overtime
* Attrition by Tenure
* Attrition by Age Group

---

## Compensation Analysis

### Insights

* Salary Distribution
* Income by Department
* Income by Job Role
* Compensation Trends

---

# ETL Development (SSIS)

This project includes an ETL workflow using SQL Server Integration Services (SSIS).

### ETL Pipeline

```text
Extract
   ↓
Transform
   ↓
Validate
   ↓
Load
   ↓
Data Warehouse
```

### ETL Tasks

* Data Extraction
* Data Cleaning
* Data Validation
* Error Handling
* Data Loading
* Process Monitoring

---

# Reporting (SSRS)

The project includes SSRS reports for operational reporting.

### Reports

* Employee Summary Report
* Department Performance Report
* Attrition Report
* Compensation Report

---

# Example DAX Measures

## Total Employees

```DAX
Total Employees =
COUNTROWS(FactEmployeeMetrics)
```

## Attrition Count

```DAX
Attrition Count =
CALCULATE(
    COUNTROWS(FactEmployeeMetrics),
    FactEmployeeMetrics[Attrition] = "Yes"
)
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

---

# Data Quality Checks

### Validation Performed

* Duplicate Employee Detection
* Missing Value Validation
* Department Validation
* Job Role Validation
* Salary Range Validation
* Data Completeness Checks

---

# Skills Demonstrated

### Business Intelligence

* BI Solution Development
* Dashboard Development
* KPI Reporting
* Executive Reporting

### SQL Development

* SQL Query Development
* Views
* Stored Procedures
* Data Validation

### Data Engineering

* ETL Development
* SSIS
* Data Transformation
* Data Integration

### Reporting

* Power BI
* SSRS
* DAX
* Analytical Reporting

### Data Modelling

* Star Schema
* Fact Tables
* Dimension Tables
* Relational Modelling

---

# Project Structure

```text
hr-workforce-analytics-bi-solution/

├── README.md
├── data/
│
├── sql/
│   ├── create_database.sql
│   ├── create_tables.sql
│   ├── data_cleaning.sql
│   ├── reporting_views.sql
│   └── data_quality_checks.sql
│
├── ssis/
│   └── hr_etl_package.dtsx
│
├── ssrs/
│   └── reports/
│
├── powerbi/
│   └── HR_Workforce_Analytics.pbix
│
├── docs/
│
├── images/
│
└── assets/
```

---

# Portfolio Relevance

This project demonstrates capabilities commonly required in:

* BI Developer
* Business Intelligence Analyst
* Reporting Analyst
* Data Analyst
* Junior Data Engineer
* SQL Developer

---

# Author

### Tshifhiwa Tshikosi

**Business Intelligence | Data Analyst | Junior Data Engineer**

Focused on building end-to-end data and BI solutions using SQL, Power BI, Databricks, Snowflake, and modern data platforms.

---



