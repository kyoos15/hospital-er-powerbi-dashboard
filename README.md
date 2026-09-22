#  Hospital Emergency Room Dashboard

An end-to-end Power BI project analyzing emergency room operations, covering 9,216 unique patient records from April 2023 to October 2024. The dashboard uncovers patterns in patient wait times, admissions, demographics, and department referrals — turning raw ER data into actionable insights for hospital resource planning.

![Dashboard Preview](screenshots/monthly-view.png)

---

##  Project Overview

- **Dataset size:** 9,216 unique patients
- **Time period:** April 2023 – October 2024 (19 months)
- **Tools used:** Power BI Desktop, DAX, Power Query
- **Type:** Multi-page interactive dashboard with What-If simulation

---

##  Objective

Emergency rooms often struggle with staffing allocation and patient flow. This project analyzes historical ER data to identify:
- When the ER is busiest (day/hour patterns)
- How long patients typically wait, and whether that's within target
- Which departments receive the most referrals
- Patient demographic and admission trends
- The potential impact of increased staffing on wait times (via simulation)

---

##  Dashboard Pages

| Page | Description |
|---|---|
| **Monthly View** | KPI overview (patients, wait time, satisfaction, referrals), admission status, peak day/hour breakdown, demographics |
| **Consolidated View** | Full-period trends across all months |
| **Patient Details** | Row-level patient data with filtering |
| **Key Takeaways** | Summary of insights and recommendations |

---

## 🧮 Key DAX Measures

```dax
Admission Status = 
IF('Hospital ER_Data'[Patient Admission Flag] = TRUE, "Admitted", "Not Admitted")

Age Group =
SWITCH(
    TRUE(),
    'Hospital ER_Data'[Patient Age] >= 100, "100+",
    'Hospital ER_Data'[Patient Age] >= 90, "90-99",
    'Hospital ER_Data'[Patient Age] >= 10, "10-19",
    "0-9"
)

Waittime Status = 
IF('Hospital ER_Data'[Patient Waittime] <= 30, "Within Target", "Target Missed")

No of Patient Referred = 
CALCULATE(
    COUNTROWS('Hospital ER_Data'), 
    'Hospital ER_Data'[Department Referral] <> "None"
)
```

---

## 🔬 Interactive Feature: Staffing Simulation

A custom **What-If Parameter** lets users simulate the effect of increasing ER staffing during peak hours on average patient wait time — turning the dashboard from purely descriptive into a lightweight prescriptive tool.

```dax
Adjusted Wait Time = 
[Average Waittime] * (1 - ('Staff Increase %'[Staff Increase % Value] / 100) * 0.6)
```

---

##  Key Insights

- Average patient wait time: **~35.3 minutes**
- Busiest day: **Monday** (1,377 patients); busiest hours: **11 AM, 7 PM, 1 PM, 11 PM**
- **5,400 patients** required no referral; among those referred, **General Practice (1,840)** and **Orthopedics (995)** were most common
- Nearly even admission split: **~50% admitted**, rest treated and released
- Largest patient age group: **30–39 years** (1,200 patients)

## 🔎 Key Insights & Recommendations

**What the data shows:**
- The ER handled 9,216 patient visits over 19 months (Apr 2023–Oct 2024), averaging a 35.3-minute wait time.
- ~34% of visits exceeded the 30-minute wait target, indicating a meaningful portion of patients experience delays.
- Monday was the consistently busiest day for patient arrivals.
- General Practice (1,840 cases) and Orthopedics (995 cases) were the top referral departments by far.
- Admissions were nearly a coin flip (~50%), and the 30–39 age group made up the largest patient segment.

**What this means for the hospital:**
1. **Staffing could be shifted toward peak days/hours** instead of spread evenly, directly targeting the periods driving the longest waits.
2. **The ~34% of delayed visits warrant a root-cause look** — segmenting delays by department or hour would help pinpoint where bottlenecks actually occur.
3. **General Practice and Orthopedics referral pathways are high-volume enough to justify a dedicated fast-track process**, potentially reducing overall ER congestion.

This turns the dashboard from a descriptive report into a decision-support tool — surfacing not just *what* happened in the ER, but *where hospital leadership could act* to improve patient flow.

---

##  Screenshots

| Monthly View | Consolidated View |
|---|---|
| ![Monthly View](screenshots/monthly-view.png) | ![Consolidated View](screenshots/consolidated-view.png) |

| Patient Details | Key Takeaways |
|---|---|
| ![Patient Details](screenshots/patient-details.png) | ![Key Takeaways](screenshots/key-takeaways.png) |

---

##  Future Improvements

- Add time-intelligence measures (rolling averages, YoY comparison)
- Extend staffing simulation to model cost vs. wait-time tradeoffs
- Add drill-through pages for individual department deep-dives

---

