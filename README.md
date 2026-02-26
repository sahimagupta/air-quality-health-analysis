# Air Quality & Health — Global Cities Analysis

This was done as part of my STEP0020 module (Assignment 2). The idea was to look at how air pollution relates to health outcomes in 20 cities around the world, using data from 1994 to 2023.

## What's this about?

I wanted to explore whether cities with worse air quality actually have worse health. Sounds obvious, right? Turns out it's not that simple.

The dataset covers things like PM2.5, PM10, NO2 levels alongside life expectancy, child mortality, and a general health index. I also looked at GDP per capita to see if money plays a bigger role than pollution  spoiler: it does.

## What I found

- Beijing is by far the most polluted city in the dataset, averaging around 30 µg/m³ for PM2.5 (the WHO says it should be under 15)
- Global PM2.5 peaked around 2011 and has been slowly coming down
- The correlation between pollution and health is actually pretty weak on its own (r = -0.06 to -0.16)
- Once you factor in GDP, things make way more sense  R² jumps from 0.004 to 0.608
- African cities like Lagos have really poor health outcomes even though their pollution isn't that bad, which shows it's really about poverty and access to healthcare more than just air
- London has great air quality but still doesn't top the health rankings compared to Madrid or Paris

## Files

- `assignment_analysis.Rmd` all my R code and analysis
- `aqhealthcities (10).numbers` the dataset I used
- `STEP0020 Assignment 2_Sahima Gupta (5) (4).pdf` the final submitted report

## How to run it

You'll need R with these packages:

```r
install.packages(c("ggplot2", "dplyr", "tidyr", "corrplot", "gridExtra", "scales"))
```

Open the `.Rmd` file in RStudio, change the `setwd()` path to wherever you saved the data, and knit it. That's it.

## Heads up

This is a teaching dataset so the numbers are simplified. The analysis shows associations, not causation I can't say pollution *causes* lower life expectancy from this data alone. There's also some missing data (especially 2022-2023) and the exercise level variable is kind of sketchy (80% marked as "High" which doesn't seem right).

## Author

Sahima Gupta
