# 🍴 FoodSafeIQ - Food Establishment Inspection Analysis

## 📌 Project Overview
This project analyzes food establishment inspection data from **Chicago** and **Dallas** using a full **data pipeline and BI stack**. The goal is to improve public health visibility by identifying inspection outcomes, risk categories, violations, and facility performance trends.  

We designed and implemented an **end-to-end ETL and analytics solution** involving:
- Data extraction from raw CSVs
- Staging and transformation in SQL Server via **Talend**
- Data validation with SQL and Python profiling
- Dimensional modeling for analytical queries
- Interactive dashboards in **Tableau** and **Power BI**

---

## 🛠️ Tech Stack
- **ETL & Data Engineering**: Talend, Alteryx  
- **Databases & Modeling**: MySQL, SQL Server, ER Studio  
- **Programming & Validation**: Python (YData profiling, Jupyter notebooks)  
- **Visualization & BI**: Tableau, Power BI  

---

## 📂 Project Components
1. **Data Staging with Talend**
   - Loaded raw CSV inspection datasets into SQL Server.  
   - Applied transformations for null handling, data type corrections, and violation normalization using `tMap`, `tNormalize`, and regex extraction.  
   - Created staging tables (`stg_Dallas_Inspection`, `stg_Chicago_Inspection`).

2. **Data Profiling & Validation**
   - Used Python & Alteryx for column-level profiling (missing values, distributions, correlations).  
   - Validated inspection results, risk categories, and violation details against business rules using SQL queries.  

3. **Dimensional Model**
   - Designed a **star schema** with fact and dimension tables:
     - **Fact_Inspection**: Links inspections with facilities, dates, and violations.  
     - **Dimensions**: `Dim_Facility`, `Dim_Inspection`, `Dim_Violation`, `Dim_Location`, `Dim_Date`.  

4. **SQL Analytical Queries**
   - Top violations by frequency and outcome  
   - Inspection results by facility type, risk category, and geography  
   - Trends of inspection outcomes over time  

5. **Visualization Dashboards**
   - **Tableau** & **Power BI** dashboards highlight:
     - Pass/Fail rates by facility type  
     - Violations by category & frequency  
     - Risk category breakdown  
     - Geospatial distribution of inspections  

---

## 📊 Key Insights
- Majority of inspections result in **Pass or Pass with Warning**, but a significant portion (~19%) fail.  
- **Restaurants** dominate the inspection records, with higher violation rates compared to other facility types.  
- High-risk categories (Risk 1) account for the majority of failed inspections.  
- Most common violations include **facility cleanliness, sanitation, allergen training, and personal hygiene issues**.  

---

## 🚀 How to Use
1. **ETL Pipeline**:  
   - Open Talend job (`.job` file) and configure database connection.  
   - Run the workflow to populate SQL Server staging tables.  

2. **SQL Validation**:  
   - Execute queries in `Data_Validation-SQL Query.sql` for verification.  

3. **Exploratory Profiling**:  
   - Open `DataProfiling.ipynb` for Jupyter-based profiling reports.  

4. **Visualization**:  
   - Open Tableau workbook (`.twbr`) or Power BI file (`Food_Inspection_PowerBI.pdf`) for interactive dashboards.  

---

## 📁 Repository Structure
```
├── DataProfiling.ipynb                 # Python profiling (ydata_profiling)
├── Data_Validation-SQL Query.sql       # SQL queries for validation & insights
├── Dimensional_Model.pdf               # ER diagram and star schema
├── Stagged_Tables_Dimensions_Facts_Documentation.pdf
├── DATA VISUALIZATION-Documentation.pdf
├── Food_Inspection_PowerBI.pdf         # Power BI dashboards
├── ~Group5_Food_Inspection_TableauDashboard__18120.twbr  # Tableau workbook
├── ydata_profiling_Dcoumentation.pdf   # Profiling report
```

---

## 📌 Future Improvements
- Automate ETL pipelines with **Airflow** or Azure Data Factory.  
- Integrate real-time inspection feeds (APIs).  
- Apply **ML models** to predict inspection outcomes based on facility attributes and violation history.  

---

✨ *This project demonstrates a full data lifecycle: from raw ingestion to actionable insights for public health decision-making.*  
