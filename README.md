# Air Quality and Health Outcomes in Global Cities

An exploratory data analysis examining the relationship between air pollution (PM2.5, PM10, NO2) and health outcomes (life expectancy, child mortality, health index) across 20 major cities worldwide from 1994 to 2023.

## Overview

This project investigates whether higher air pollution levels are associated with worse health outcomes at the city level. The analysis covers cities across five regions — Asia, Europe, Africa, Americas, and Oceania — and considers how economic development (GDP per capita) mediates the pollution-health relationship.

## Key Findings

- **Asian cities** have the highest PM2.5 levels, with Beijing averaging 30 µg/m³ — double the WHO guideline
- **PM2.5 peaked globally around 2011** and has been declining since, though most cities still exceed safe levels
- **Weak direct correlations** between PM2.5 and health outcomes (r = -0.06 to -0.16), suggesting air quality alone doesn't determine health
- **GDP per capita is the dominant factor** — controlling for GDP improves model R² from 0.004 to 0.608
- **African cities** show poor health outcomes despite moderate pollution, highlighting the role of economic development
- **London** performs well on air quality (9.4 µg/m³ in 2021) but ranks below European peers on broader health measures

## Project Structure

```
├── assignment_analysis.Rmd          # Main R Markdown analysis script
├── aqhealthcities (10).numbers      # Source dataset (Apple Numbers format)
├── STEP0020 Assignment 2_Sahima Gupta (5) (4).pdf  # Final report
└── README.md
```

## Requirements

- **R** (≥ 4.0)
- R packages: `ggplot2`, `dplyr`, `tidyr`, `corrplot`, `gridExtra`, `scales`

Install dependencies:

```r
install.packages(c("ggplot2", "dplyr", "tidyr", "corrplot", "gridExtra", "scales"))
```

## Running the Analysis

1. Open `assignment_analysis.Rmd` in RStudio
2. Update the `setwd()` path in the data loading chunk to point to your local data directory
3. Ensure the dataset CSV (`aqhealthcities.csv`) is available at that path
4. Knit the document or run chunks individually

## Analysis Sections

| Section | Description |
|---------|-------------|
| **1a** | Key trends, patterns, and anomalies in PM2.5 across cities and regions |
| **1b** | Interrelationships between air quality and health outcomes (correlation + regression) |
| **1c** | Differences by city characteristics (GDP, region) |
| **1d** | London's position relative to other cities |
| **1e** | Data quality issues, limitations, and uncertainty |

## Data Quality Notes

- ~7% of health data missing (2022–2023)
- ~20% of modal split data missing
- 39 PM2.5 outliers (6.5%), primarily from Beijing's 2011–2018 pollution crisis
- Exercise level classification appears unreliable (80% marked "High")
- Dataset is simplified for educational purposes — findings should not inform real policy

## Important Caveats

This analysis identifies **associations, not causal relationships**. City-level averages mask within-city inequalities, and the simplified dataset is designed for teaching. Real public health policy would require more granular, primary data collection.

## Author

Sahima Gupta — STEP0020 Assignment 2
