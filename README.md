Power BI Project: Road Accident Analysis Dashboard 

# Road Accident Analysis Dashboard

## Project Overview

Road traffic accidents are a major public safety concern. Understanding accident patterns can help authorities identify high-risk conditions and improve road safety strategies.

This project analyzes road accident data using Power BI to identify patterns in accident severity, vehicle involvement, road infrastructure, and environmental conditions.

The final output is an interactive dashboard that enables users to explore accident trends, casualty severity, and geographic accident distribution.

---

## Business Problem

Government agencies and traffic authorities need data-driven insights to answer questions such as:

* Which vehicle types are most frequently involved in accidents?
* How do accidents vary between urban and rural areas?
* Which road types contribute to the highest number of casualties?
* Are accidents more common in daylight or darkness?
* How do accident trends compare year-over-year?

This dashboard provides insights that can help support road safety policies and infrastructure improvements.

---

## Dataset

The dataset contains information about road accidents including:

* Accident location
* Casualty severity
* Vehicle type
* Road type
* Weather conditions
* Lighting conditions
* Urban vs rural classification
* Accident dates

The data is used to analyze casualty patterns and accident trends.

---

## Tools & Technologies

| Tool              | Purpose                                 |
| ----------------- | --------------------------------------- |
| Power BI          | Dashboard development and visualization |
| Power Query       | Data cleaning and transformation        |
| DAX               | Calculations and KPI measures           |
| Map Visualization | Geographic accident distribution        |

---

## Key Dashboard Metrics

| Metric             | Value  |
| ------------------ | ------ |
| Total Casualties   | 196K   |
| Total Accidents    | 144K   |
| Fatal Casualties   | 2.9K   |
| Serious Casualties | 27K    |
| Slight Casualties  | 165.8K |

Each metric also tracks year-over-year percentage change to monitor trends.

---

## Dashboard Visualizations

### Casualties by Vehicle Type

Shows accident involvement across vehicle categories such as cars, bikes, vans, buses, and agricultural vehicles.

Insight: Cars account for the majority of accident casualties.

---

### Yearly Casualty Trend

A monthly line chart comparing current year casualties and previous year casualties. This helps identify seasonal patterns in accident frequency.

---

### Urban vs Rural Accident Distribution

Compares accident frequency between urban and rural areas. Urban areas show a higher concentration of accidents due to higher traffic density.

---

### Casualties by Road Type

Breakdown of accident distribution by road infrastructure including single carriageway, dual carriageway, roundabout, one-way street, and slip road. Single carriageways show the highest accident count.

---

### Casualties by Lighting Conditions

Examines accident distribution during daylight and darkness. Most accidents occur during daylight due to increased traffic activity.

---

### Accident Location Map

A geographic map highlights accident hotspots across the UK, helping identify high-risk regions.

---

## Key Insights

* Cars account for the largest share of accident casualties.
* Urban areas experience higher accident frequency than rural areas.
* Single carriageways contribute to the majority of accidents.
* The majority of accidents occur during daylight conditions.
* Accident hotspots are concentrated in high traffic regions.

---

## Example DAX Measures

Total Casualties

```DAX
Total Casualties = SUM('Road Accident data'[Casualties])
```

Current Year Casualties

```DAX
CY Casualties =
CALCULATE(
    [Total Casualties],
    YEAR('Calendar'[Date]) = YEAR(TODAY())
)
```

Previous Year Casualties

```DAX
PY Casualties =
CALCULATE(
    [Total Casualties],
    SAMEPERIODLASTYEAR('Calendar'[Date])
)
```

---

## Dashboard Preview

(Add a screenshot of the Power BI dashboard here)

---

## How to Use the Dashboard

1. Open the `.pbix` file in Power BI Desktop.
2. Use the Weather Conditions and Road Type filters to explore different accident scenarios.
3. Hover over visuals to see detailed metrics.
4. Use the map to analyze geographic accident distribution.

---

## Project Structure

```
Road-Accident-Analysis
│
├── data
│   └── accident_dataset.csv
│
├── dashboard
│   └── road_accident_dashboard.pbix
│
├── images
│   └── dashboard_preview.png
│
└── README.md
```

---

## Project Outcome

This project demonstrates how Power BI dashboards can transform raw accident data into meaningful insights that help identify risk patterns and support road safety improvements.
