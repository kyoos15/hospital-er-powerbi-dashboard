# 🏥 Hospital Emergency Room Dashboard — Power BI

An interactive **Power BI dashboard for analyzing hospital Emergency Room (ER) operations**, built to understand patient volume, waiting times, admissions, referrals, satisfaction, demographics, and peak operational periods.

The dashboard uses a combination of **Power BI data modeling, DAX measures, interactive slicers, KPI cards, drill-down analysis, and a What-If parameter** to transform raw hospital ER data into actionable operational insights.

---

## 📊 Project Overview

Emergency departments need to balance patient volume, waiting times, staffing, referrals, and patient satisfaction.

This project analyzes **9,216 unique ER patients** across a **19-month period from April 2023 to October 2024**.

The dashboard provides both high-level management insights and detailed patient-level analysis.

### Key questions addressed

* How many patients visited the Emergency Room?
* What is the average patient waiting time?
* How does patient satisfaction vary?
* How many patients were admitted versus released?
* Which departments receive the most referrals?
* When are the ER's busiest days and hours?
* What are the major patient demographic patterns?
* What proportion of patients are seen within 30 minutes?
* How can staffing changes affect operational metrics?
* Which areas may require operational attention?

---

# 🎯 Objectives

The main objectives of this project were to:

1. Analyze Emergency Room patient volume and operational performance.
2. Monitor average patient waiting time.
3. Track patient admission and referral patterns.
4. Analyze patient satisfaction.
5. Identify peak days and hours for ER visits.
6. Understand demographic distributions.
7. Provide patient-level drill-down capabilities.
8. Build an interactive dashboard for hospital management.
9. Use DAX to create meaningful KPIs and calculated metrics.
10. Implement a **What-If parameter** to analyze the effect of staff increases on selected operational metrics.

---

# 🗂️ Dashboard Structure

The Power BI report is divided into **four main pages**:

| Page                 | Purpose                                      |
| -------------------- | -------------------------------------------- |
| 📅 Monthly View      | Analyze ER performance across months         |
| 📊 Consolidated View | Overall operational overview                 |
| 👤 Patient Details   | Explore individual patient-level information |
| 💡 Key Takeaways     | Summarized findings and recommendations      |

---

# 📅 1. Monthly View

The **Monthly View** focuses on understanding how ER performance changes over time.

### Main KPIs

* **Number of Patients**
* **Average Wait Time**
* **Patient Satisfaction Score**
* **Number of Patients Referred**

### Interactive controls

The page includes slicers for:

* Year
* Month
* **Staff Increase % — What-If Parameter**

### Visual analysis

The page contains several visualizations for:

* Patient volume trends
* Waiting-time trends
* Satisfaction trends
* Referral patterns
* Admission status
* Patient demographics
* Department referrals
* Patients seen within 30 minutes
* Gender distribution
* Patient volume by day
* Patient volume by hour

This allows users to move from a monthly overview into specific operational patterns.

---

# 📊 2. Consolidated View

The **Consolidated View** provides an overall summary of ER activity.

Instead of focusing primarily on month-to-month analysis, this page provides a broader view of the hospital's emergency department performance.

### Key KPIs

* Total Number of Patients
* Average Wait Time
* Patient Satisfaction Score
* Number of Patients Referred

### Analysis included

* Admission status
* Patient referrals
* Patient wait-time performance
* Department referral distribution
* Gender distribution
* Patient volume by day
* Patient volume by hour
* Patients seen within 30 minutes

A date slicer allows the user to dynamically filter the dashboard.

---

# 👤 3. Patient Details

The **Patient Details** page provides a more granular view of individual patients.

Users can filter the data using the available date controls and inspect patient-level information.

### Patient-level attributes include

* Patient ID
* Patient Name
* Age
* Age Group
* Gender
* Race
* Admission Date
* Wait Time
* Admission Status
* Department Referral
* Satisfaction Score
* Wait-Time Status

This page is useful when moving from **high-level KPI analysis to individual patient records**.

---

# 💡 4. Key Takeaways

The Key Takeaways page summarizes the major findings from the analysis.

## Dataset Overview

* **9,216 unique patients**
* Analysis period: **April 2023 – October 2024**
* Total period: **19 months**

---

## ⏱️ Patient Wait Time & Satisfaction

The dashboard reports an average patient wait time of approximately:

### **35.3 minutes**

The average patient satisfaction score is approximately:

### **4.99 / 10**

The dashboard uses these KPIs to highlight the relationship between ER waiting time and the overall patient experience.

---

## 🏥 Departmental Referrals

A substantial portion of patients did not require departmental referral.

### Referral distribution highlighted in the dashboard

* **No referral:** 5,400 patients
* **General Practice:** 1,840 patients
* **Orthopedics:** 995 patients
* **Physiotherapy:** 276 patients
* **Cardiology:** 248 patients

General Practice and Orthopedics account for a substantial share of the referred patients.

---

# 📈 Peak ER Periods

The dashboard identifies significant variation in patient volume by day and hour.

### Busiest days

* **Saturday:** 1,377 patients
* **Monday:** 1,322 patients
* **Tuesday:** 1,318 patients

### Busiest hours

The dashboard highlights:

* 11 AM
* 1 PM
* 7 PM
* 11 PM

These patterns can be used to investigate whether staffing levels are aligned with periods of higher patient demand.

---

# 👥 Patient Demographics

## Age Distribution

The dashboard identifies the following major age groups:

* **30–39 years:** approximately 1,200 patients
* **20–29 years:** approximately 1,188 patients
* 40–50 years also represents a significant patient group

---

## Gender Distribution

The dashboard provides a breakdown of patient volume by gender, allowing demographic differences in ER utilization to be explored.

---

## Race Distribution

The dashboard reports:

| Race                 | Patients |
| -------------------- | -------: |
| White                |    2,571 |
| African American     |    1,951 |
| Multiracial          |    1,557 |
| Asian                |    1,060 |
| Declined to identify |    1,030 |

These figures are presented descriptively to understand the composition of the dataset.

---

# 🏥 Admission Patterns

The dashboard compares patients who were admitted with those who were treated and released.

### Reported figures

* **Admitted:** 4,612 patients
* **Treated & Released:** 4,604 patients

This provides a near-even split between the two outcomes in the analyzed dataset.

---

# ⏰ 30-Minute Wait-Time Analysis

One of the dashboard's operational KPIs evaluates whether patients were seen within a **30-minute target**.

The dashboard indicates that approximately **34% of visits did not meet the 30-minute target**.

This metric provides a simple operational indicator for identifying potential waiting-time bottlenecks.

---

# 🎛️ What-If Analysis

A **What-If parameter** was implemented to analyze the potential effect of changing staffing levels.

### Parameter

**Staff Increase %**

Users can interact with the staff-increase slicer and examine how changing the assumed staffing level affects the relevant dashboard metrics.

This introduces a basic scenario-analysis component to the dashboard.

### Why use a What-If parameter?

Instead of looking only at historical performance, users can ask:

> "What happens to the operational metrics if staffing is increased?"

This makes the dashboard more useful for **planning and scenario analysis**, rather than only historical reporting.

---

# 📐 Data Model

The report uses a structured Power BI data model involving:

### Main data table

**Hospital ER_Data**

This contains the primary patient and operational information.

### Supporting date table

**Date Table**

The report uses a dedicated date table for time-based analysis and filtering.

The model supports analysis across:

* Year
* Month
* Date
* Day
* Patient admission date
* Time-based trends

A separate table is also used for the **Staff Increase % What-If parameter**.

---

# 🧮 DAX & Calculated Metrics

DAX was used to create and/or expose several analytical metrics used throughout the dashboard.

Important measures/metrics include:

* `No of Patients`
* `No of Patients1`
* `Avg Wait Time`
* `Avg Wait Time Numeric`
* `Previous Month Wait Time`
* `Adjustedd Wait Time`
* `Adjusted Cost of Delays`
* `1 No of Patient Referred`
* `Satisfaction Score`
* `Waittime Status`
* `Waittime Interval`
* `1 Admission Status`
* `Age Group`

These calculations allow raw patient-level records to be converted into meaningful operational KPIs.

---

# 📊 Key KPIs

The main dashboard KPIs include:

| KPI                          | Purpose                                              |
| ---------------------------- | ---------------------------------------------------- |
| 👥 Number of Patients        | Measures overall ER patient volume                   |
| ⏱️ Average Wait Time         | Measures patient waiting performance                 |
| ⭐ Patient Satisfaction Score | Tracks patient experience                            |
| 🔄 Patients Referred         | Measures departmental referral volume                |
| 🏥 Admission Status          | Compares admitted vs released patients               |
| ⏰ 30-Minute Performance      | Measures performance against the waiting-time target |
| 💰 Adjusted Cost of Delays   | Provides an operational cost perspective             |
| 📈 Previous Month Wait Time  | Enables time-based comparison                        |
| 👨‍⚕️ Staff Increase %       | Enables staffing scenario analysis                   |

---

# 📊 Visualizations Used

The dashboard combines multiple Power BI visual types, including:

* KPI Cards
* Area Charts
* Column Charts
* Clustered Column Charts
* Clustered Bar Charts
* Donut Charts
* Tables / Matrix Visuals
* Slicers
* Page Navigation
* Images
* What-If Parameter Controls

This combination allows both **summary-level monitoring** and **detailed exploration**.

---

# 🔍 Interactive Features

The dashboard was designed to be interactive rather than static.

### Users can:

* Filter by date
* Filter by year
* Filter by month
* Explore individual patients
* Analyze admission patterns
* Examine departmental referrals
* Compare patient demographics
* Investigate peak days and hours
* Analyze wait-time performance
* Adjust staffing assumptions using the What-If parameter
* Navigate between dashboard pages

---

# 💼 Business Insights

The analysis provides several operational insights.

### 1. Waiting time is an important operational KPI

An average waiting time of approximately **35.3 minutes** provides a baseline for evaluating ER patient flow.

---

### 2. Patient satisfaction provides another performance dimension

The approximately **4.99/10 average satisfaction score** can be monitored alongside waiting-time metrics to understand the patient experience.

---

### 3. Patient demand varies significantly by time

Saturday, Monday, and Tuesday show relatively high patient volumes, while several specific hours also experience higher demand.

This can help hospital administrators investigate whether staffing schedules align with patient arrival patterns.

---

### 4. Referrals are concentrated in specific departments

General Practice and Orthopedics represent major referral destinations.

This may help identify departments that interact frequently with ER operations.

---

### 5. Admission and release outcomes are relatively balanced

The dataset contains approximately equal numbers of admitted and treated-and-released patients.

This provides useful context when analyzing ER workload and downstream hospital capacity.

---

### 6. A meaningful share of visits exceeds the 30-minute target

The dashboard indicates that around **34% of visits did not meet the 30-minute target**, making waiting-time analysis an important operational area.

---

# 💡 Recommendations Derived from the Analysis

The dashboard highlights several areas that could be investigated further:

### 1. Align staffing with peak periods

Patient volumes vary across days and hours. Staffing schedules can therefore be analyzed against these demand patterns.

---

### 2. Investigate delayed visits

Cases exceeding the 30-minute target can be further segmented by:

* Day
* Hour
* Department
* Admission status
* Patient characteristics

This can help identify where delays are concentrated.

---

### 3. Analyze high-volume referral pathways

Since General Practice and Orthopedics account for substantial referral activity, these pathways can be examined for potential process bottlenecks.

---

### 4. Use What-If analysis for staffing scenarios

The Staff Increase % parameter provides a framework for testing different staffing assumptions before making operational decisions.

---

# 🛠️ Tools & Technologies

### Power BI

* Power BI Desktop
* Power Query
* DAX
* Data Modeling
* Interactive Visualizations
* What-If Parameters
* Slicers
* KPI Cards
* Drill-down / filtering
* Dashboard navigation

### Data Analysis Concepts

* Exploratory Data Analysis
* Time-Series Analysis
* KPI Development
* Patient Segmentation
* Operational Performance Analysis
* Scenario Analysis
* Demographic Analysis

---



# 📸 Dashboard Pages

## Monthly View

Add a screenshot of your Monthly View here:

```markdown
Screenshot 2026-09-22 181227.png
```

---

## Consolidated View

```markdown
Screenshot 2026-09-23 001720.png
```

---

## Patient Details

```markdown
Screenshot 2026-09-23 001730.png
```

---

## Key Takeaways

```markdown
Screenshot 2026-09-23 001737.png
```

---

# 📌 Project Highlights

* Analyzed **9,216 unique ER patients**
* Covered **19 months of hospital ER activity**
* Built **4 interactive Power BI dashboard pages**
* Created operational KPIs using **DAX**
* Analyzed **wait times, admissions, referrals, satisfaction, and patient demographics**
* Identified peak patient-demand periods
* Evaluated performance against a **30-minute waiting-time target**
* Implemented a **Staff Increase % What-If parameter**
* Added patient-level analysis for detailed exploration
* Built an interactive dashboard suitable for operational decision support

---

# 🔮 Future Improvements

The dashboard could be extended by adding:

* Real-time ER monitoring
* Predictive patient-volume forecasting
* Wait-time prediction using Machine Learning
* Department-level performance benchmarking
* Staff utilization metrics
* Bed occupancy analysis
* Doctor/nurse workload analysis
* Automated alerts for excessive waiting times
* Predictive admission modeling
* Cost-benefit analysis of staffing changes
* More detailed What-If scenarios
* Integration with live hospital databases

---
