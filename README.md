# Attrition Analysis Dashboard

This repository contains the Power BI dashboard for Attrition Analysis, including data visualizations that provide insights into employee attrition based on factors such as age, salary, job role, education, and more.

## Project Overview

The Attrition Analysis dashboard includes the following key metrics:
- **Total Employees**: 1,470
- **Total Attrition Count**: 237
- **Average Age**: 36.92 years
- **Average Salary**: 6.5k
- **Average Tenure**: 7.01 years

## Visualizations

The following visualizations have been created in the Power BI dashboard:

### 1. Donut Chart: Attrition Count by Education Field
A donut chart that visualizes the attrition count based on the employee's field of education.

- **Education Fields**:
  - Life Sciences
  - Medical
  - Marketing
  - Technical Degree
  - Human Resources
  - Other

### 2. Bar Chart: Attrition Count by Age Group
A bar chart representing the count of attrition segmented by different age groups.

- **Age Groups**:
  - 18-25
  - 25-34
  - 35-44
  - 45-54
  - 55+

### 3. Bar Chart: Attrition by Job Role
A horizontal bar chart showing the count of attrition across different job roles, such as:
  - Sales Executive
  - Research Scientist
  - Laboratory Technician
  - Manufacturing Director
  - Healthcare Representative

### 4. Matrix Table: Attrition by Years at Company
A matrix table that displays attrition based on job role and the job satisfaction the employees have.

### 5. Area Chart: Attrition Count by Years at Company
An area chart that visualizes attrition count against years spent in the company. A sharp drop in attrition is visible after 1-2 years.

### 6. Bar Chart: Attrition Count by Salary Range
A bar chart breaking down attrition count by salary ranges:
  - Upto 5k
  - 5k-10k
  - 10k-15k
  - 15k+

## DAX Formulas

The following DAX formulas have been used to calculate custom fields:

### Salary Slab Calculation

This formula is used to categorize employees into salary slabs based on their salary.

```dax
SalarySlab = 
SWITCH(
    TRUE(),
    [Salary] <= 5000, "Upto 5k",
    [Salary] > 5000 && [Salary] <= 10000, "5k-10k",
    [Salary] > 10000 && [Salary] <= 15000, "10k-15k",
    [Salary] > 15000, "15k+"
)
