# Power Outage Analysis - 2000 to 2016
Project for DSC80 at University of California, San Diego

## Introduction
This dataset covers major power outages in the United States from 2000 to 2016. This analysis aims to answer the following question:

### Does the state that one resides in affect the likelihood that they will experience a major power outage?

The data gathered consists of 1534 outages reported (rows). Relevant columns and descriptions are below.

YEAR: Year of reported power outage
 	
MONTH: Month of reported power outage (set by numerical month e.g January = 1, February = 2, etc.)

U.S._STATE: State where reported power outage is located

ANOMALY.LEVEL: Oceanic El Niño/La Niña (ONI) index for cold/warm episodes by season. Estimated as running mean of 3 month ERSST.v4 SST anomalies in the Niño 3.4 region (5°N to 5°S, 120–170°W),
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

<iframe src="assets/plot2.html" width=800 height=600 frameBorder=0></iframe>

First I wanted to explore how the nature of power outages have changed over time, 
this plot shows the total duration of power outages per year of our dataset. 
It appears that in general power outages have become more severe in duration as years increase with extreme spikes and dips 
in duration presumably due to large-scale events.

<iframe src="assets/plot1.html" width=800 height=600 frameBorder=0></iframe>

This is also reflected by the frequency of outages per year generally on the rise with the same large spike in 2011.
Some outside investigation shows that 2011 was a year of extreme weather events including but not limited to: 
[winter blizzards, wildfires, tornadoes, and Hurricane Irene.](https://emergency.cdc.gov/recentincidents/recentincidents_2011.asp)

<iframe src="assets/scatter1.html" width=800 height=600 frameBorder=0></iframe>

Additionally some more exploration into the dataset shows that cold to normal weather (anomaly levels <= 1) generally produces longer durations 
in power outages than hotter weather.

|                                                                        |   Count |
|:-----------------------------------------------------------------------|--------:|
| (2000.0, 'equipment failure', 'failure')                               |       1 |
| (2000.0, 'equipment failure', 'line fault')                            |       1 |
| (2000.0, 'equipment failure', 'relaying malfunction')                  |       2 |
| (2000.0, 'equipment failure', 'transformer outage')                    |       1 |
| (2000.0, 'intentional attack', 'vandalism')                            |       2 |
| (2000.0, 'severe weather', 'heavy wind')                               |       1 |
| (2000.0, 'severe weather', 'thunderstorm')                             |       2 |
| (2000.0, 'severe weather', 'tornadoes')                                |       1 |
| (2000.0, 'severe weather', 'wildfire')                                 |       2 |
| (2000.0, 'severe weather', 'winter storm')                             |       2 |
| (2000.0, 'system operability disruption', 'transmission interruption') |       2 |
| (2001.0, 'equipment failure', 'feeder shutdown')                       |       1 |
 Finally, I wanted to see what the main causes of power outages were, and how they changed each year.
This table describes the count of each category cause in each year for the entire dataset. This is the first 12 rows of the table.
<details>
    <summary> Click here for the full dataset </summary>
|                                                                        |   Count |
|:-----------------------------------------------------------------------|--------:|
| (2000.0, 'equipment failure', 'failure')                               |       1 |
| (2000.0, 'equipment failure', 'line fault')                            |       1 |
| (2000.0, 'equipment failure', 'relaying malfunction')                  |       2 |
| (2000.0, 'equipment failure', 'transformer outage')                    |       1 |
| (2000.0, 'intentional attack', 'vandalism')                            |       2 |
| (2000.0, 'severe weather', 'heavy wind')                               |       1 |
| (2000.0, 'severe weather', 'thunderstorm')                             |       2 |
| (2000.0, 'severe weather', 'tornadoes')                                |       1 |
| (2000.0, 'severe weather', 'wildfire')                                 |       2 |
| (2000.0, 'severe weather', 'winter storm')                             |       2 |
| (2000.0, 'system operability disruption', 'transmission interruption') |       2 |
| (2001.0, 'equipment failure', 'feeder shutdown')                       |       1 |
| (2001.0, 'severe weather', 'flooding')                                 |       1 |
| (2002.0, 'intentional attack', 'vandalism')                            |       1 |
| (2002.0, 'severe weather', 'hurricanes')                               |       1 |
| (2002.0, 'severe weather', 'winter storm')                             |      11 |
| (2003.0, 'equipment failure', 'breaker trip')                          |       2 |
| (2003.0, 'equipment failure', 'cables')                                |       1 |
| (2003.0, 'equipment failure', 'generator trip')                        |       1 |
| (2003.0, 'equipment failure', 'relaying malfunction')                  |       1 |
| (2003.0, 'equipment failure', 'transmission interruption')             |       1 |
| (2003.0, 'intentional attack', 'vandalism')                            |       2 |
| (2003.0, 'severe weather', 'earthquake')                               |       1 |
| (2003.0, 'severe weather', 'flooding')                                 |       1 |
| (2003.0, 'severe weather', 'heavy wind')                               |       8 |
| (2003.0, 'severe weather', 'hurricanes')                               |       5 |
| (2003.0, 'severe weather', 'storm')                                    |       3 |
| (2003.0, 'severe weather', 'thunderstorm')                             |       7 |
| (2003.0, 'severe weather', 'wildfire')                                 |       2 |
| (2003.0, 'severe weather', 'winter storm')                             |       3 |
| (2003.0, 'system operability disruption', 'transmission interruption') |       1 |
| (2004.0, 'equipment failure', 'generator trip')                        |       2 |
| (2004.0, 'equipment failure', 'line fault')                            |       1 |
| (2004.0, 'equipment failure', 'substation')                            |       1 |
| (2004.0, 'equipment failure', 'switching')                             |       1 |
| (2004.0, 'severe weather', 'heatwave')                                 |       1 |
| (2004.0, 'severe weather', 'heavy wind')                               |       8 |
| (2004.0, 'severe weather', 'hurricanes')                               |      16 |
| (2004.0, 'severe weather', 'storm')                                    |       1 |
| (2004.0, 'severe weather', 'thunderstorm')                             |      16 |
| (2004.0, 'severe weather', 'tornadoes')                                |       1 |
| (2004.0, 'severe weather', 'wildfire')                                 |       4 |
| (2004.0, 'severe weather', 'wind/rain')                                |       1 |
| (2004.0, 'severe weather', 'winter storm')                             |       7 |
| (2004.0, 'system operability disruption', 'transmission interruption') |       1 |
| (2005.0, 'equipment failure', 'plant trip')                            |       1 |
| (2005.0, 'equipment failure', 'transmission interruption')             |       1 |
| (2005.0, 'fuel supply emergency', 'Coal')                              |       1 |
| (2005.0, 'severe weather', 'heavy wind')                               |       1 |
| (2005.0, 'severe weather', 'hurricanes')                               |      11 |
| (2005.0, 'severe weather', 'storm')                                    |       2 |
| (2005.0, 'severe weather', 'thunderstorm')                             |      18 |
| (2005.0, 'severe weather', 'tornadoes')                                |       1 |
| (2005.0, 'severe weather', 'wildfire')                                 |       1 |
| (2005.0, 'severe weather', 'winter storm')                             |       8 |
| (2005.0, 'system operability disruption', 'transmission interruption') |       1 |
| (2006.0, 'equipment failure', 'generator trip')                        |       1 |
| (2006.0, 'fuel supply emergency', 'Coal')                              |       1 |
| (2006.0, 'severe weather', 'earthquake')                               |       2 |
| (2006.0, 'severe weather', 'heatwave')                                 |       4 |
| (2006.0, 'severe weather', 'heavy wind')                               |      12 |
| (2006.0, 'severe weather', 'hurricanes')                               |       3 |
| (2006.0, 'severe weather', 'storm')                                    |       1 |
| (2006.0, 'severe weather', 'thunderstorm')                             |      11 |
| (2006.0, 'severe weather', 'tornadoes')                                |       1 |
| (2006.0, 'severe weather', 'wildfire')                                 |       2 |
| (2006.0, 'severe weather', 'winter storm')                             |      10 |
| (2006.0, 'system operability disruption', 'shed load')                 |       1 |
| (2007.0, 'equipment failure', 'generator trip')                        |       5 |
| (2007.0, 'equipment failure', 'transmission trip')                     |       1 |
| (2007.0, 'severe weather', 'heatwave')                                 |       3 |
| (2007.0, 'severe weather', 'heavy wind')                               |       3 |
| (2007.0, 'severe weather', 'hurricanes')                               |       1 |
| (2007.0, 'severe weather', 'storm')                                    |       9 |
| (2007.0, 'severe weather', 'thunderstorm')                             |       9 |
| (2007.0, 'severe weather', 'wildfire')                                 |       5 |
| (2007.0, 'severe weather', 'winter storm')                             |       9 |
| (2008.0, 'equipment failure', 'breaker trip')                          |       1 |
| (2008.0, 'equipment failure', 'generator trip')                        |       2 |
| (2008.0, 'equipment failure', 'transmission trip')                     |       2 |
| (2008.0, 'severe weather', 'flooding')                                 |       1 |
| (2008.0, 'severe weather', 'heatwave')                                 |       1 |
| (2008.0, 'severe weather', 'heavy wind')                               |      12 |
| (2008.0, 'severe weather', 'hurricanes')                               |      15 |
| (2008.0, 'severe weather', 'lightning')                                |       1 |
| (2008.0, 'severe weather', 'storm')                                    |       9 |
| (2008.0, 'severe weather', 'thunderstorm')                             |      16 |
| (2008.0, 'severe weather', 'thunderstorm; islanding')                  |       1 |
| (2008.0, 'severe weather', 'wildfire')                                 |       5 |
| (2008.0, 'severe weather', 'winter storm')                             |       7 |
| (2008.0, 'system operability disruption', 'transmission interruption') |       1 |
| (2008.0, 'system operability disruption', 'uncontrolled loss')         |       1 |
| (2009.0, 'equipment failure', 'computer hardware')                     |       1 |
| (2009.0, 'equipment failure', 'generator trip')                        |       1 |
| (2009.0, 'equipment failure', 'substation')                            |       1 |
| (2009.0, 'equipment failure', 'switching')                             |       1 |
| (2009.0, 'equipment failure', 'transformer outage')                    |       1 |
| (2009.0, 'equipment failure', 'transmission')                          |       1 |
| (2009.0, 'equipment failure', 'transmission trip')                     |       3 |
| (2009.0, 'severe weather', 'heavy wind')                               |       6 |
| (2009.0, 'severe weather', 'storm')                                    |       6 |
| (2009.0, 'severe weather', 'thunderstorm')                             |      11 |
| (2009.0, 'severe weather', 'wind/rain')                                |       4 |
| (2009.0, 'severe weather', 'winter storm')                             |      14 |
| (2009.0, 'system operability disruption', 'HVSubstation interruption') |       1 |
| (2009.0, 'system operability disruption', 'transmission interruption') |       1 |
| (2010.0, 'equipment failure', 'breaker trip')                          |       1 |
| (2010.0, 'equipment failure', 'generator trip')                        |       1 |
| (2010.0, 'equipment failure', 'transformer outage')                    |       1 |
| (2010.0, 'equipment failure', 'transmission')                          |       2 |
| (2010.0, 'fuel supply emergency', 'Hydro')                             |       1 |
| (2010.0, 'severe weather', 'flooding')                                 |       1 |
| (2010.0, 'severe weather', 'heavy wind')                               |       4 |
| (2010.0, 'severe weather', 'hurricanes')                               |       1 |
| (2010.0, 'severe weather', 'storm')                                    |       4 |
| (2010.0, 'severe weather', 'thunderstorm')                             |      16 |
| (2010.0, 'severe weather', 'tornadoes')                                |       1 |
| (2010.0, 'severe weather', 'wildfire')                                 |       2 |
| (2010.0, 'severe weather', 'wind/rain')                                |       6 |
| (2010.0, 'severe weather', 'winter storm')                             |      13 |
| (2010.0, 'system operability disruption', 'transmission interruption') |       2 |
| (2011.0, 'equipment failure', 'generator trip')                        |       1 |
| (2011.0, 'fuel supply emergency', ' Natural Gas')                      |       1 |
| (2011.0, 'fuel supply emergency', 'Coal')                              |       5 |
| (2011.0, 'intentional attack', 'vandalism')                            |     121 |
| (2011.0, 'severe weather', 'earthquake')                               |       1 |
| (2011.0, 'severe weather', 'storm')                                    |       5 |
| (2011.0, 'severe weather', 'thunderstorm')                             |       7 |
| (2011.0, 'severe weather', 'winter')                                   |       1 |
| (2011.0, 'severe weather', 'winter storm')                             |       9 |
| (2011.0, 'system operability disruption', 'distribution interruption') |       1 |
| (2011.0, 'system operability disruption', 'majorsystem interruption')  |       1 |
| (2011.0, 'system operability disruption', 'transmission interruption') |       2 |
| (2012.0, 'fuel supply emergency', 'Coal')                              |       1 |
| (2012.0, 'fuel supply emergency', 'Hydro')                             |       3 |
| (2012.0, 'intentional attack', 'vandalism')                            |      79 |
| (2012.0, 'severe weather', 'heavy wind')                               |       1 |
| (2012.0, 'severe weather', 'hurricanes')                               |      21 |
| (2012.0, 'severe weather', 'storm')                                    |       1 |
| (2012.0, 'severe weather', 'thunderstorm')                             |      34 |
| (2012.0, 'severe weather', 'wind storm')                               |       1 |
| (2012.0, 'severe weather', 'wind/rain')                                |       1 |
| (2012.0, 'severe weather', 'winter storm')                             |       4 |
| (2012.0, 'system operability disruption', 'transmission interruption') |       2 |
| (2013.0, 'equipment failure', 'generator trip')                        |       2 |
| (2013.0, 'fuel supply emergency', ' Coal')                             |       2 |
| (2013.0, 'fuel supply emergency', ' Natural Gas')                      |       2 |
| (2013.0, 'fuel supply emergency', 'Hydro')                             |       1 |
| (2013.0, 'fuel supply emergency', 'Petroleum')                         |       1 |
| (2013.0, 'intentional attack', 'sabotage')                             |       4 |
| (2013.0, 'intentional attack', 'suspicious activity')                  |       1 |
| (2013.0, 'intentional attack', 'vandalism')                            |      55 |
| (2013.0, 'severe weather', 'fog')                                      |       1 |
| (2013.0, 'severe weather', 'hailstorm')                                |       3 |
| (2013.0, 'severe weather', 'heatwave')                                 |       1 |
| (2013.0, 'severe weather', 'heavy wind')                               |       2 |
| (2013.0, 'severe weather', 'lightning')                                |       2 |
| (2013.0, 'severe weather', 'snow/ice ')                                |       6 |
| (2013.0, 'severe weather', 'snow/ice storm')                           |       1 |
| (2013.0, 'severe weather', 'thunderstorm')                             |      20 |
| (2013.0, 'severe weather', 'tornadoes')                                |       3 |
| (2013.0, 'severe weather', 'uncontrolled loss')                        |       1 |
| (2013.0, 'severe weather', 'wind storm')                               |       3 |
| (2013.0, 'severe weather', 'winter storm')                             |       4 |
| (2013.0, 'system operability disruption', '100 MW loadshed')           |       1 |
| (2013.0, 'system operability disruption', 'distribution interruption') |       1 |
| (2013.0, 'system operability disruption', 'transmission interruption') |       1 |
| (2013.0, 'system operability disruption', 'uncontrolled loss')         |       1 |
| (2014.0, 'fuel supply emergency', ' Coal')                             |       8 |
| (2014.0, 'fuel supply emergency', ' Hydro')                            |       1 |
| (2014.0, 'fuel supply emergency', ' Natural Gas')                      |       4 |
| (2014.0, 'intentional attack', 'sabotage')                             |       1 |
| (2014.0, 'intentional attack', 'vandalism')                            |      33 |
| (2014.0, 'severe weather', 'heavy wind')                               |       3 |
| (2014.0, 'severe weather', 'snow/ice ')                                |       7 |
| (2014.0, 'severe weather', 'thunderstorm')                             |      10 |
| (2014.0, 'severe weather', 'wildfire')                                 |       3 |
| (2014.0, 'severe weather', 'wind')                                     |       1 |
| (2014.0, 'severe weather', 'wind storm')                               |       2 |
| (2014.0, 'severe weather', 'winter')                                   |      18 |
| (2015.0, 'intentional attack', 'sabotage')                             |      11 |
| (2015.0, 'intentional attack', 'suspicious activity')                  |       2 |
| (2015.0, 'intentional attack', 'vandalism')                            |      28 |
| (2015.0, 'severe weather', 'public appeal')                            |       1 |
| (2015.0, 'severe weather', 'thunderstorm')                             |       1 |
| (2015.0, 'severe weather', 'uncontrolled loss')                        |       1 |
| (2015.0, 'severe weather', 'wind')                                     |       2 |
| (2015.0, 'severe weather', 'winter')                                   |       4 |
| (2015.0, 'system operability disruption', 'uncontrolled loss')         |       6 |
| (2016.0, 'intentional attack', 'sabotage')                             |      16 |
| (2016.0, 'intentional attack', 'vandalism')                            |      14 |
| (2016.0, 'system operability disruption', 'public appeal')             |       1 |
| (2016.0, 'system operability disruption', 'transmission interruption') |       3 |
| (2016.0, 'system operability disruption', 'uncontrolled loss')         |       4 |
| (2016.0, 'system operability disruption', 'voltage reduction')         |       1 |
</details>


## Assessment of Missingness