# dex-analytics
A Power BI dashboard simulating Digital Employee Experience (DEX) analytics revealing how IT ticket volume alone masks hidden performance issues across departments. Built using Python, Excel &amp; Power BI.

# Digital Employee Experience (DEX) Analytics Dashboard
### A Power BI project inspired by Nexthink's approach to proactive IT intelligence

---

## Project Overview

This project simulates a real-world Digital Employee Experience (DEX) analytics use case — the kind of insight that IT leaders need to move from reactive problem solving to proactive optimisation.

Using a simulated dataset of 500 employees across 8 departments and 5 UK locations, I built a two-page interactive Power BI dashboard that surfaces hidden IT performance issues — issues that traditional IT metrics completely miss.

---

## The Key Insight — The Misleading Metric

> "Everyone was tracking IT ticket volume. But the data told a completely different story."

Finance and HR raised the fewest IT tickets — which on the surface looks like everything is fine.

But dig deeper and the data reveals:
- Highest average boot times — 45–67 seconds vs 18 seconds for Engineering
- Highest app crash rates — nearly 3x the company average
- Lowest employee satisfaction scores — 4.2 out of 10
- Most legacy OS devices — predominantly Windows 10 (Legacy)

These employees have stopped raising tickets. They have given up expecting IT to help. This silent suffering is completely invisible to IT teams who rely solely on ticket volume as a health indicator.

The recommendation: Track boot time, crash rate, and satisfaction scores alongside ticket count for true DEX visibility — exactly the proactive approach Nexthink enables.

---

Dashboard Pages

 Page 1 — DEX Overview

| Visual | Description |
|---|---|
| KPI Card — Avg Boot Time | Average device boot time across all employees |
| KPI Card — Avg Crash Rate | Average application crash rate |
| KPI Card — Total IT Tickets | Sum of IT tickets raised |
| KPI Card — Avg Satisfaction Score | Average employee satisfaction out of 10 |
| Bar Chart | Avg boot time by department — reveals HR & Finance as outliers |
| Scatter Chart | IT tickets vs satisfaction score — exposes the misleading metric |

Page 2 — Dept Intelligence

| Visual | Description |
|---|---|
| Stacked Bar Chart | OS version distribution by department — shows legacy OS concentration |
| Donut Chart | Device type breakdown across the organisation |
| Slicer | Filter by Department |
| Slicer | Filter by Location |

---

Dataset

The dataset was simulated to reflect realistic enterprise IT and employee experience patterns.

| Column | Description |
|---|---|
| Date | Date of record |
| Employee_ID | Unique employee identifier |
| Department | One of 8 departments |
| Location | One of 5 UK cities |
| Device_Type | Laptop, Desktop, or Virtual Desktop |
| OS_Version | Windows 10, Windows 11, or Windows 10 (Legacy) |
| Boot_Time_Seconds | Device boot time in seconds |
| App_Crash_Rate | Proportion of app sessions that crashed |
| IT_Ticket_Count | Number of IT tickets raised |
| Employee_Satisfaction_Score | Self-reported satisfaction score (1–10) |
| Primary_App | Most used application |
| Network_Drop_Incidents | Number of network drop events |
| Days_Since_OS_Update | Days since last OS update |

---

Tools Used

- Python — dataset generation and Excel file creation
- Power BI Desktop — dashboard design and publishing
- DAX — measures for KPI calculations
- Excel — data source

Key DAX Measures

Avg Boot Time (s) = AVERAGE(DEX_Raw_Data[Boot_Time_Seconds])

Avg Crash Rate = AVERAGE(DEX_Raw_Data[App_Crash_Rate])

Total IT Tickets = SUM(DEX_Raw_Data[IT_Ticket_Count])

Avg Satisfaction Score = AVERAGE(DEX_Raw_Data[Employee_Satisfaction_Score])

Employee Count = COUNTROWS(DEX_Raw_Data)

How to Use

1. Clone or download this repository
2. Open `DEX_Dashboard_Nexthink.pbix` in Power BI Desktop
3. If prompted, update the data source path to point to `DEX_Dataset_Nexthink.xlsx`
4. Refresh the data
5. Explore the dashboard and use the slicers to filter by Department and Location

---

## Author

Naveen Prasath
Business Analyst | Data-Driven Process Optimisation

Inspiration

This project was inspired by Nexthink's vision of AI-powered, agentic Digital Employee Experience management helping IT teams see, diagnose, and fix issues before employees even notice them.


