# HR Attrition Analysis Dashboard (Power BI) 📊

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Dataset](https://img.shields.io/badge/Dataset-IBM%20HR%20Analytics%20(Kaggle)-blue)

An interactive **Power BI dashboard** built using the **IBM HR Analytics Employee Attrition & Performance dataset (Kaggle)** to analyze employee attrition patterns, identify key drivers of attrition, and support HR stakeholders with actionable insights for retention planning.

---

## 📌 Project Overview

Employee attrition can significantly impact productivity and increase hiring/training costs. This dashboard provides a comprehensive view of attrition trends across departments, job roles, demographics, and employee satisfaction indicators.

The dashboard is designed for **HR teams and business leaders** to make data-driven retention decisions.

---

## 📊 Dataset

This project uses the **IBM HR Analytics Employee Attrition & Performance dataset**, fetched from **Kaggle**.

- Source: IBM HR Analytics Dataset  
- Platform: Kaggle  
- Target Variable: `Attrition` (Yes/No)  
- Key Fields: Age, Gender, Department, Job Role, Years at Company, OverTime, Monthly Income, Job Satisfaction, Performance Rating, etc.

> ⚠️ Note: Dataset is publicly available and used strictly for educational/project purposes.

---

## 🎯 Objectives

- Analyze employee attrition distribution and trends  
- Identify key drivers contributing to attrition  
- Segment attrition by job role, department, tenure, income, satisfaction, and overtime  
- Enable HR stakeholders to explore insights interactively  

---

## 🧩 Dashboard Features

### ✅ Key KPIs
- Total Employees  
- Attrition Count  
- Attrition Rate (%)  
- Average Monthly Income  
- Average Years at Company  
- Average Job Satisfaction  

### 📌 Interactive Visual Insights
- Attrition by Department  
- Attrition by Job Role  
- Attrition by Age Group  
- Attrition by Gender & Marital Status  
- Attrition vs OverTime  
- Attrition vs Job Satisfaction  
- Attrition vs Monthly Income Bands  
- Attrition by Years at Company (Tenure)  

### 🎛 Filters / Slicers
- Department  
- Job Role  
- Gender  
- Age Group  
- OverTime  
- Marital Status  

---

## ⚙️ Power BI Implementation

### 1) Data Preparation
- Imported dataset into Power BI  
- Cleaned and transformed data using **Power Query**
- Handled missing values and column formatting  
- Created calculated columns (Age groups, Income bands, Tenure buckets)

### 2) Data Modeling
- Built relationships (if using multiple tables)
- Created measures using **DAX**

---

## 🧮 Key DAX Measures (Examples)

```DAX
Attrition Count =
CALCULATE(COUNTROWS('HR_Data'), 'HR_Data'[Attrition] = "Yes")
Total Employees = 
COUNTROWS('HR_Data')
Attrition Rate % = 
DIVIDE([Attrition Count], [Total Employees], 0)
Avg Monthly Income = 
AVERAGE('HR_Data'[MonthlyIncome])
```

###📂 Repository Structure
```
hr-attrition-powerbi-dashboard/
│
├── data/
│   ├── raw/                         # Original dataset (IBM HR Analytics)
│   └── processed/                   # Cleaned / transformed dataset (optional)
│
├── dashboard/
│   └── HR_Attrition_Dashboard.pbix   # Power BI report file
│
├── images/
│   ├── dashboard_overview.png        # Screenshot of dashboard
│   └── insights.png                  # Key visuals screenshot (optional)
│
├── README.md
└── LICENSE
```
### 🚀 How to Use
1) Download the Power BI File
Download HR_Attrition_Dashboard.pbix from the dashboard/ folder

2) Open in Power BI Desktop
Install Power BI Desktop
Open the .pbix file

3) Refresh Data (Optional)
Go to Home → Refresh

If needed, update the dataset path in Power Query

### 📌 Business Impact

This dashboard helps HR teams to:

- Identify high-attrition departments and job roles
- Understand how factors like overtime, satisfaction, and income influence attrition
- Support proactive retention strategies
- Improve workforce planning and reduce turnover costs

### 🔮 Future Improvements

- Add drill-through pages for employee-level analysis
- Integrate forecasting / trend analysis for attrition
- Publish to Power BI Service with scheduled refresh
- Add RLS (Row-Level Security) for role-based access
- Integrate predictive attrition risk score output from ML model

### 👤 Author
Saravanan Srinivasan

Email: meet.saravanan10@gmail.com
