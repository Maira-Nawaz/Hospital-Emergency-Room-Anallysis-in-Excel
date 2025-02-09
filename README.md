# **Hospital Emergency Room Dashboard - End-to-End Project**  

## **Project Overview**  
This project involves designing an **interactive Hospital Emergency Room Analysis Dashboard in Excel**, leveraging **data visualization techniques** to help stakeholders make data-driven decisions. The dashboard provides real-time insights into patient admission trends, wait times, department referrals, and patient satisfaction scores, ultimately enhancing hospital efficiency.  

## **Problem Statement**  
Hospital emergency rooms (ERs) face numerous challenges, including long wait times, overcrowding, inefficient patient management, and resource allocation issues. Healthcare professionals need a data-driven approach to monitor key performance indicators (KPIs) such as:  

- **Admission Rates** – How many patients are admitted vs. not admitted?  
- **Waiting Times** – Are patients attended to in a timely manner?  
- **Age & Gender Analysis** – What are the demographic patterns of ER visits?  
- **Department Referrals** – Which specialties receive the highest patient volume?  

To solve these challenges, this project aims to build a **comprehensive ER analytics dashboard**, allowing hospital administrators to track trends, improve decision-making, and optimize operations.  

## **Project Objectives**  
- Visualize hospital emergency room data to track key performance metrics.  
- Identify inefficiencies in patient wait times and admission processes.  
- Analyze patient demographics (age, gender, and referrals) to improve service quality.  
- Optimize resource allocation by identifying high-demand hospital departments.  
- Enhance decision-making through interactive reports and real-time insights.  

## **Key Performance Indicators (KPIs) Tracked**  
The dashboard includes the following key KPIs:  

### **1. Total Number of Patients**  
- Displays the total number of patients handled in a selected month.  
- Example: 4,338 patients in a given month.  

### **2. Average Wait Time (Minutes)**  
- Measures the efficiency of patient service.  
- Current Value: 35.03 minutes average wait time.  

### **3. Patient Satisfaction Score**  
- Evaluates overall patient experience and service quality.  
- Current Value: 5.03 (on a scale of 10).  

### **4. Admission Status (Admitted vs. Not Admitted)**  
- Admitted: 2,157 patients (50%)  
- Not Admitted: 2,181 patients (50%)  
- Helps monitor hospital capacity and bed availability.  

### **5. Timeliness of Patient Attendance**  
- On Time: 2,516 patients (57%)  
- Delayed: 1,822 patients (42%)  
- Used to assess hospital response time efficiency.  

### **6. Patient Demographics (Age & Gender Analysis)**  
- Age Groups Tracked: 0-9, 10-19, 20-29, 30-39, 40-49, 50-59, 60-69, 70-79.  
- Gender Breakdown: Male (49%) | Female (51%).  
- Helps identify which age groups visit the ER most frequently.  

### **7. Department Referrals**  
- Tracks which hospital departments receive the most patient referrals.  
- Top Referred Departments:  
  - General Practice – 874 patients  
  - Orthopedics – 463 patients  
  - Physiotherapy – 134 patients  
  - Cardiology – 125 patients  

## **Data Processing & Formulas Used**  

### **Calendar Table Formula (For Date Selection)**  
```excel
= List.Dates(#date(2023,01,01),731,#duration(1,0,0,0))
```
- Generates a date range for analysis, enabling yearly comparisons (2023 & 2024).  

### **Age Group Classification (DAX Formula)**  
```excel
=IF([Patient Age]>=70,"70-79",
IF([Patient Age]>=60,"60-69",
IF([Patient Age]>=45,"45-59",
IF([Patient Age]>=30,"30-44",
IF([Patient Age]>=15,"15-29",
IF([Patient Age]>=5,"05-14","0-4"))))))
```
- Categorizes patients into age groups for better visualization.  

### **Timeliness Calculation (DAX Formula)**  
```excel
= IF ([Patient Waittime ]<30, "Within Time" , "Delayed" )
```
- Determines whether a patient was attended to on time or faced a delay.  

## **Features of the Dashboard**  
- Dynamic Year Selection (2023 / 2024) – Compare trends across years.  
- Monthly Data Navigation – Users can view reports for each month.  
- Interactive Charts & Visualizations – For quick data insights.  
- Excel-Based Implementation – Easily accessible for non-technical users.  

## **Tools & Technologies Used**  
- Microsoft Excel – Data entry, formulas, pivot tables, and charts.  
- Power Query – Data transformation & cleansing.  
- DAX (Data Analysis Expressions) – Custom calculations for KPIs.  

## **Impact & Benefits**  
- Optimized hospital resource management by tracking patient flow.  
- Reduced wait times by identifying bottlenecks.  
- Improved patient experience through data-driven decisions.  
- Better staffing strategies based on peak admission hours.  
- Enhanced hospital efficiency by monitoring department workloads.  

## **How to Use This Dashboard?**  
1. Select Year (2023 / 2024) to analyze trends.  
2. Navigate monthly reports using the side panel.  
3. Check KPIs like Wait Time, Satisfaction Score, and Admissions.  
4. Analyze patient demographics using Age & Gender Charts.  
5. Review Department Referrals to optimize resource allocation.  
