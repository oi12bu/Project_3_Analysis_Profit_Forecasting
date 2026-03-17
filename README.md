# Project 3 — Timeless Transport Models Resource Analysis & Profit Forecasting

**Course:** CSB304 H10 31429 — Data Analytics in Business  
**Instructor:** Eric Lloyd  
**Authors:** Bea Sauve, Elton Nichols, Kainen Osborne  
**Date:** March 2026

---

## Overview

This project analyzes production and sales data for **Timeless Transport Models**, a B2B manufacturer and distributor of modeled vehicles. Using data collected since 2003 across three factories and two product lines each, the project delivers:

- Aggregated weekly production and cost data into monthly totals
- Exploratory data analysis (EDA) of production and sales trends
- Production forecasts for June–December 2005
- Cost and profit analysis per product line
- Projected total profit for the second half of 2005

All analyses are conducted in **R** using reproducible, documented workflows.

---

## Repository Structure

```
Project_3_Analysis_Profit_Forecasting/
├── CSV/
│   ├── weekly_factory_production.csv       # Weekly production data by factory/product line
│   └── sales_data_sample_cleaned.csv       # Customer orders and sales data (2003–2005)
├── Project_3_Technical_Report.Rmd          # Main technical report (knit to HTML)
├── Project_3_Technical_Report.html         # Rendered technical report
├── Project_3_Production.Rmd               # Supplementary production analysis notebook
├── README.md                               # Project overview (this file)
├── CONTRIBUTING.md                         # Contribution guidelines and team roles
└── AI.md                                   # AI usage transparency log
```

---

## Getting Started

### Prerequisites

Ensure you have **R** and **RStudio** installed. Then install the required packages by running the following in the RStudio Console:

```r
install.packages("readr")      # Read and import data
install.packages("tidyverse")  # Data manipulation and visualization
install.packages("lubridate")  # Date handling and weekday conversion
install.packages("forecast")   # Time series forecasting
install.packages("ggplot2")    # Data visualization
install.packages("dplyr")      # Data transformation
install.packages("car")        # Companion to Applied Regression
install.packages("MASS")       # Statistical functions
```

### Running the Analysis

1. Clone this repository:
   ```bash
   git clone <https://github.com/oi12bu/Project_3_Analysis_Profit_Forecasting>
   cd Project_3_Analysis_Profit_Forecasting
   ```

2. Open `Project_3_Technical_Report.Rmd` in RStudio.

    3. Ensure the CSV data files are located in the `CSV/` directory relative to the `.Rmd` file.

    4. Click **Knit** (or run `rmarkdown::render("Project_3_Technical_Report.Rmd")`) to generate the HTML report.

2. Open `Project_3_Technical_Report.html` in your local browser to view the pre-generated report

> **Note:** `Project_3_Production.Rmd` contains supplementary production forecasting code and can be run independently.

---

## Data Sources

| File | Description |
|------|-------------|
| `weekly_factory_production.csv` | Weekly production counts and costs by factory and product line |
| `sales_data_sample_cleaned.csv` | Customer order history including sales, territories, and order dates (2003–2005) |
| `monthly_salesXproduction.csv` | Monthly production counts and sales data grouped by month|
| `monthly_salesXproduction_by_productline.csv` | Monthly production counts and sales data grouped by month and product line |

---

## Analysis Summary

### Data Refinement
Raw data is imported, cleaned, and aggregated. Key steps include correcting data types, handling missing values, calculating production metrics, and merging production and sales datasets.

### Exploratory Data Analysis
Visual and statistical exploration of production trends, factory performance, and sales patterns across product lines and territories.

### Production Forecasting
Time series models are applied to forecast monthly production for each product line from June through December 2005. Model selection is guided by trend and seasonality decomposition.

### Cost & Profit Analysis
Average cost and revenue per product line are calculated. Total projected profit for Q4 2005 is estimated based on forecasted production volumes and historical margin data.

### Profit Forecasting
Time series models are applied to forecast monthly profits for each product line from June through December 2005. Model selection is guided by trend and seasonality decomposition.

### Project Analysis
Concluding thoughts regarding the overall analysis, and key insights of the forecasted data.

---

## Team

| Name | Role |
|------|------|
| Bea Sauve | Project Manager — documentation, production forecasting, data refinement |
| Elton Nichols | Version Control Manager — repository management, sales data refinement, EDA |
| Kainen Osborne | Analysis Auditor — profit forecasting, analysis verification |

See [CONTRIBUTING.md](CONTRIBUTING.md) for a full breakdown of individual contributions.

---

## AI Usage

This project documents all AI tool usage transparently. See [AI.md](AI.md) for a complete log of prompts, outputs, and files affected per team member.

---

## License

This project was produced for academic purposes as part of CSB304 at [North Seattle Community College]. Not intended for commercial use.