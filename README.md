# National Park Service — Mortality Analytics Dashboard

![Dashboard Overview](images/Causes_of_Death.png)

## Overview

This Power BI dashboard analyzes visitor fatality data across US National Parks
from 2007 through February 2026, covering 4,931 deaths across 206 parks.

The analysis surfaces mortality patterns by demographics, cause of death, activity
type, time trends, and geographic concentration. The Power BI dashboard provides a comprehensive picture
of where, when, and how fatal incidents occur within the National Park system.

## Questions Explored

- Which parks have the highest fatality rates, and what causes drive them?
- How do age, sex, and activity type correlate with cause of death?
- What seasonal and day-of-week patterns emerge in park fatalities?
- How has annual mortality trended over nearly two decades, and what explains
  the peak in 2018?
- Which activities carry the highest risk, and how do they rank by intent
  (unintentional vs. intentional vs. undetermined)?

## Dashboard Pages

### Demographics
Breaks down fatalities by sex (80.4% male), age group, and the intersection of
both. Includes an age-group-to-top-cause table revealing that drowning dominates
younger age groups while motor vehicle crashes are the leading cause for visitors
45 and older.

### Trends
Shows annual fatalities over time, cumulative deaths, average deaths by month
(peak: July at 709), deaths by day of week (Saturday highest at 897), and
quarterly breakdowns grouped by intent.

### Causes of Death
Ranks causes of death (drowning: 877, motor vehicle crash: 843, undetermined: 834),
maps activities to risk tiers, and identifies the top 8 parks by cause-group
death volume. Lake Mead National Recreation Area leads with 380 total deaths.

## Data Model

Built on NPS incident/mortality records spanning CY2007–Feb 2026. Key dimensions:

- **Date** — year, month, quarter, day of week
- **Location** — park name, region
- **Decedent** — age range, sex
- **Incident** — cause of death, cause group, activity, activity category, intent

## Data Scope and Validation Considerations
The National Park Service (NPS) mortality dataset contains records from calendar year CY2007 through the present; however, the official NPS mortality dashboard only reports validated data from CY2014–2019. According to the NPS, records from CY2007–2013 and CY2020–present have not completed the agency's formal validation process, which includes quality checks and coordination with individual park units prior to official publication.

For this analysis, the complete mortality dataset (CY2007–February 2026) was utilized to provide a more comprehensive view of long-term trends and patterns across the National Park System. While this approach incorporates records that have not yet undergone NPS validation, it allows for a broader examination of mortality incidents over time. To support both perspectives, the Power BI dashboard was designed with interactive filters that enable users to isolate specific years or focus exclusively on the validated 2014–2019 period if desired.

The inclusion of unvalidated records raises important questions regarding data collection and quality assurance. Specifically, how are mortality incidents reported, who is responsible for recording them, and what procedures are used to verify their accuracy and completeness? These questions are particularly relevant because variations in reporting practices, delayed updates, or incomplete records may influence analytical findings. It introduces a degree of uncertainty that should be considered when interpreting results. The dataset remains a valuable source for identifying broad trends, seasonal patterns, geographic concentrations, and activity-related mortality risks. Findings should be viewed as exploratory for years outside the validated 2014–2019 period, while conclusions drawn from the validated years can be considered more reliable.

Check out the official NPS Power BI Dashboard [here](https://www.nps.gov/aboutus/mortality-data.htm).

## Tools Used

- **Power BI Desktop** — data model, DAX measures, report design
- **DAX** — custom measures for fatality counts, rankings, rolling totals,
  and risk tier classification

## How to Use This File

1. Download `report/NPS_Mortality_Analytics.pbix`
2. Open in Power BI Desktop (free download from Microsoft)
3. Use the Year, Region, and Park slicers to filter the full dataset
4. Navigate between the Demographics, Trends, and Causes of Death report pages

## Dashboard Preview

### Demographics
![Demographics](images/Demographics.png)

### Temporal Trends
![Trends](images/Trends.png)

### Causes of Death
![Causes of Death](images/Causes_of_Death.png)

## What Are the Key Terms Used on This Dashboard?
- Mortality – another word for death
- Intent – Identifies whether a death was caused by an act carried out on purpose (by oneself or by another person), an unintended and unplanned act, or a - natural/medical event.
- Intentional – death resulting from purposeful harmful actions upon oneself (suicide) or others (homicide) or due to legal intervention.
- Medical – death resulting from natural or medical related causes (e.g., seizure, heart attack), when sedentary or during physical activity, and are not due to intentional or unintentional causes.
- Unintentional – death that occur without the intention of hurting oneself or others which result in damage to the body from acute exposure to kinetic, thermal, electrical, or chemical energy or from the absence of such essentials as heat or oxygen (e.g., drownings, motor vehicle crash, fall, poisoning, hypothermia, thermal burns).
- Undetermined – deaths where the intent could not be determined due to one of the following reasons:
  - Official intent classified as “Undetermined”
  - Insufficient information in the incident report to determined intent
  - Record is restricted in the source system of record
  - Data captured by an outside agency (e.g., local law enforcement agency)

Access the data dictionary `data/NPS-Mortality-Data-CY2007-to-CY2026-Released.xlsx - Mortality Data CY2007-Feb 2026.csv` to find definitions for additional terms used in the dashboard.

## About

Built to explore public safety patterns in the US National Park system using
official NPS mortality data.

[LinkedIn](#) | [Portfolio](#)
