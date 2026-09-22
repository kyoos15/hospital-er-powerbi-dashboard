# 🏥 Hospital Emergency Room Analytics Dashboard

An interactive **Power BI dashboard** developed to analyze Emergency Room (ER) operations using patient-level data. The project transforms raw hospital data into actionable insights on patient volume, waiting time, satisfaction, admissions, referrals, demographics, and staffing requirements.

---

## 📌 Project Overview

Emergency departments need to balance fluctuating patient demand with limited staff and resources. This project uses **Power BI and DAX** to analyze ER performance over a **19-month period (April 2023 – October 2024)**.

The dashboard contains **9,216 unique patient records** and provides interactive views of operational KPIs, patient demographics, referral patterns, admission trends, and peak demand periods.

A **What-If staffing simulator** was also developed using DAX parameters to evaluate how changes in staffing levels could affect patient waiting time and estimated delay costs.

---

## 🎯 Objectives

The main objectives of this project were to:

- Analyze Emergency Room patient volumes and operational trends.
- Monitor average patient waiting time.
- Analyze patient satisfaction.
- Understand admission and discharge patterns.
- Identify the most common departmental referrals.
- Identify peak days and hours of ER activity.
- Analyze patient demographics.
- Build a What-If staffing simulator.
- Provide data-driven recommendations for ER resource allocation.

---

## 🛠️ Tools & Technologies

| Tool / Technology | Usage |
|---|---|
| **Power BI** | Dashboard development and visualization |
| **DAX** | KPI calculations, measures and time intelligence |
| **Power BI Data Modeling** | Data relationships and analytical model |
| **Star Schema** | Structured analytical data model |
| **What-If Parameters** | Staffing scenario simulation |
| **Time Intelligence** | Month-over-month performance analysis |

---

# 📊 Dashboard Structure

The dashboard consists of four major sections:

### 1. Monthly View

Provides a month-wise analysis of Emergency Room performance.

Key metrics include:

- Number of patients
- Average waiting time
- Patient satisfaction score
- Number of patients referred
- Monthly KPI trends
- Previous-month comparisons
- Staffing scenario analysis

Interactive filters allow users to explore performance across different time periods and patient characteristics.

---

### 2. Consolidated View

Provides a high-level overview of overall Emergency Room operations.

The page includes:

- Total patient count
- Average waiting time
- Patient satisfaction
- Referral volume
- Admission status
- Patient demographics
- Referral department distribution
- Patient volume by day and hour
- Patients meeting the 30-minute waiting-time target

This view is designed to provide a quick overview of the hospital's ER performance.

---

### 3. Patient Details

Provides a detailed patient-level view of the dataset.

Users can filter and inspect individual patient records based on available attributes and analyze patient characteristics alongside their ER visit information.

---

### 4. Key Takeaways

A dedicated insights page summarizes the major findings from the analysis and translates the dashboard results into operational recommendations.

---

# 📈 Key Performance Indicators

The dashboard tracks several important ER KPIs:

### Patient Volume

**9,216 unique patients** were recorded during the analyzed 19-month period.

### Average Waiting Time

The overall average patient waiting time was approximately:

**35.3 minutes**

### Patient Satisfaction

The average patient satisfaction score was:

**4.99 / 10**

### Admissions

The dataset recorded:

- **4,612 patients admitted**
- **4,604 patients treated and released**

This represents an almost even split between admissions and patients released after treatment.

### Referral Volume

A substantial portion of patients did not require departmental referral, while General Practice and Orthopedics accounted for the largest referral volumes among referred patients.

---

# 🔍 Key Insights

## 1. Patient Wait Time & Satisfaction

The average ER waiting time was approximately **35.3 minutes**.

The average patient satisfaction score was **4.99/10**, indicating an opportunity to investigate the relationship between waiting time and patient experience.

The dashboard also tracks the proportion of patients seen within the **30-minute target**.

Approximately **34% of visits were outside the 30-minute target**, highlighting specific periods where patient flow may require further investigation.

---

## 2. Departmental Referrals

A large number of patients did not require a departmental referral:

**5,400 patients**

Among referred patients, the largest referral categories were:

| Referral Department | Patients |
|---|---:|
| General Practice | 1,840 |
| Orthopedics | 995 |
| Physiotherapy | 276 |
| Cardiology | 248 |

General Practice and Orthopedics therefore represent major referral pathways within the analyzed ER data.

---

## 3. Peak Patient Periods

The analysis identified several high-volume days.

### Busiest Days

| Day | Patients |
|---|---:|
| Saturday | 1,377 |
| Monday | 1,322 |
| Tuesday | 1,318 |

The dashboard also identifies **11 AM, 1 PM, 7 PM, and 11 PM** as notable high-volume hours.

These patterns can be used to investigate whether staffing levels are aligned with patient demand.

---

## 4. Patient Demographics

The dashboard analyzes patient distribution across age groups.

The largest age group was:

**30–39 years → 1,200 patients**

followed by:

**20–29 years → 1,188 patients**

The analysis also includes other age groups to provide a broader view of the ER patient population.

---

## 5. Race Distribution

The dashboard provides a breakdown of patient records by race.

The largest recorded groups were:

| Race | Patients |
|---|---:|
| White | 2,571 |
| African American | 1,951 |
| Multiracial | 1,557 |
| Asian | 1,060 |

Additionally, **1,030 patients declined to identify their race**.

These demographic breakdowns are included for descriptive analysis of the dataset.

---

## 6. Admission Patterns

The dashboard shows an almost even split between patients who were admitted and those who were treated and released.

- **4,612 admitted**
- **4,604 treated and released**

This provides an overview of the proportion of ER visits resulting in hospital admission versus release after treatment.

---

# ⚙️ DAX & Data Modeling

## Star Schema

The project uses a structured data model based on a **star-schema approach**, allowing the dashboard to efficiently analyze patient records across different dimensions.

The model supports:

- Date-based analysis
- Patient-level analysis
- KPI calculations
- Filtering and slicing
- Monthly trend analysis
- Staffing simulations

---

# 🧮 DAX Measures

Several DAX measures were developed to calculate operational KPIs dynamically.

Examples include calculations for:

- Total patients
- Average wait time
- Patient satisfaction
- Referral counts
- Admission counts
- Delay-related costs
- Previous-month KPIs
- Staffing impact

---

## 📅 Time Intelligence

DAX time-intelligence functions were used to analyze changes in operational KPIs over time.

Key functions include:

```DAX
CALCULATE()
DATEADD()
