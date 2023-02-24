# Power Outage Analysis - 2000 to 2016
Project for DSC80 at University of California, San Diego

## Introduction
This dataset covers major power outages in the United States from 2000 to 2016. This analysis aims to answer the following question:

### Does the state that one resides in affect the likelihood that they will experience a major power outage?

The data gathered consists of 1534 outages reported (rows). Relevant columns and descriptions are below.

YEAR: Year of reported power outage
 	
MONTH: Month of reported power outage (set by numerical month e.g January = 1, February = 2, etc.)

U.S._STATE: State where reported power outage is located

ANOMALY.LEVEL: Oceanic El Niño/La Niña (ONI) index for cold/warm episodes by season. Estimated as running mean of 3 month ERSST.v4 SST anomalies in the Niño 3.4 region (5°N to 5°S, 120–170°W)
	more found [here](https://origin.cpc.ncep.noaa.gov/products/analysis_monitoring/ensostuff/ONI_v5.php)

CLIMATE.CATEGORY: Represents the episode of climate by year and based on thresholds for Oceanic Niño Index (ONI) ± 0.5 °C

CAUSE.CATEGORY: Category of event(s) causing the power outage

CAUSE.CATEGORY.DETAIL: Detailed description of the category of event causing the power outage

OUTAGE.DURATION: Duration of power outage in minutes

CUSTOMERS.AFFECTED: Number of customers affected by the power outage

OUTAGE.START: Starting date and time of power outage

OUTAGE.RESTORATION: Ending date and time of power outage

POPULATION: Total population of state at the time of reported outage

## Exploratory Analysis

test plot <iframe src="assets/plot1.html" width=800 height=600 frameBorder=0></iframe>

