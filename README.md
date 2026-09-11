# 🏥 Executive Hospital Operations & Patient Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-CC292B?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data_Analytics-0078D4?style=for-the-badge&logo=azure&logoColor=white)

## 📌 Executive Overview
This end-to-end business intelligence project addresses key operational bottlenecks in hospital clinical management, emergency room (ER) patient throughput, and resource allocation. By leveraging **SQL** for data transformation and **Power BI** for interactive data modeling and visualization, this executive dashboard equips healthcare administrators with real-time operational metrics to reduce patient wait times, optimize bed occupancy, and enhance care quality.

---

## 🎥 Video Demonstration & Walkthrough

https://github.com/user-attachments/assets/Hospital_Operations_Executive_Dashboard_PowerBI.mp4

> *Note: Watch the 1-minute video walk-through above for a detailed breakdown of operational KPIs, interactive filtering, and patient admission trends.*

---

## 💡 Key Business Insights & Impact
* **Emergency Department (ER) Throughput:** Identified peak bottleneck windows during admission cycles, enabling dynamic staff allocation.
* **Length of Stay (LOS) & Capacity Management:** Modeled patient turnover to improve bed turnover rates and minimize admission delay backlogs.
* **Financial & Cost Metrics:** Tracked operational cost per patient department to highlight resource allocation inefficiencies.

---
# 🏥 Executive Hospital Operations & Patient Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-CC292B?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data_Analytics-0078D4?style=for-the-badge&logo=azure&logoColor=white)

## 📌 Executive Overview
This end-to-end business intelligence project addresses key operational bottlenecks in hospital clinical management, emergency room (ER) patient throughput, and resource allocation. By leveraging **SQL** for data transformation and **Power BI** for interactive data modeling and visualization, this executive dashboard equips healthcare administrators with real-time operational metrics to reduce patient wait times, optimize bed occupancy, and enhance care quality.

---

## 🎥 Video Demonstration & Walkthrough

https://github.com/user-attachments/assets/Hospital_Operations_Executive_Dashboard_PowerBI.mp4

> *Note: Watch the 1-minute video walk-through above for a detailed breakdown of operational KPIs, interactive filtering, and patient admission trends.*

---

## 💡 Key Business Insights & Impact
* **Emergency Department (ER) Throughput:** Identified peak bottleneck windows during admission cycles, enabling dynamic staff allocation.
* **Length of Stay (LOS) & Capacity Management:** Modeled patient turnover to improve bed turnover rates and minimize admission delay backlogs.
* **Financial & Cost Metrics:** Tracked operational cost per patient department to highlight resource allocation inefficiencies.

---

## 🛠️ Data Pipeline & Architecture

### 1. Data Cleaning & SQL Querying
Raw patient records, admission logs, and clinical operational data were extracted and transformed using SQL. 

```sql
-- Sample SQL Query: Aggregating Departmental Patient Volume & Average Wait Times
SELECT 
    Department_Name,
    COUNT(Patient_ID) AS Total_Patients,
    AVG(Wait_Time_Minutes) AS Avg_Wait_Time,
    ROUND(AVG(Length_Of_Stay_Days), 2) AS Avg_LOS
FROM Hospital_Admissions
WHERE Admission_Date >= DATEADD(month, -12, GETDATE())
GROUP BY Department_Name
ORDER BY Avg_Wait_Time DESC;

## 🛠️ Data Pipeline & Architecture

### 1. Data Cleaning & SQL Querying
Raw patient records, admission logs, and clinical operational data were extracted and transformed using SQL. 

```sql
-- Sample SQL Query: Aggregating Departmental Patient Volume & Average Wait Times
SELECT 
    Department_Name,
    COUNT(Patient_ID) AS Total_Patients,
    AVG(Wait_Time_Minutes) AS Avg_Wait_Time,
    ROUND(AVG(Length_Of_Stay_Days), 2) AS Avg_LOS
FROM Hospital_Admissions
WHERE Admission_Date >= DATEADD(month, -12, GETDATE())
GROUP BY Department_Name
ORDER BY Avg_Wait_Time DESC;
