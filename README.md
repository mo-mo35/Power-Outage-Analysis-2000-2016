# Power Outage Analysis - 2000 to 2016
Project for DSC80 at University of California, San Diego

## Introduction
This dataset covers major power outages in the United States from 2000 to 2016. This analysis aims to answer the following question:

### Does the state that one resides in affect the likelihood that they will experience a major power outage?

The data gathered consists of 1534 outages reported (rows). Relevant columns and descriptions are below.

**YEAR:** Year of reported power outage
 	
**MONTH:** Month of reported power outage (set by numerical month e.g January = 1, February = 2, etc.)

**U.S._STATE:** State where reported power outage is located

**ANOMALY.LEVEL:** Oceanic El Niño/La Niña (ONI) index for cold/warm episodes by season. Estimated as running mean of 3 month ERSST.v4 SST anomalies in the Niño 3.4 region (5°N to 5°S, 120–170°W),
more found [here](https://origin.cpc.ncep.noaa.gov/products/analysis_monitoring/ensostuff/ONI_v5.php)

**CLIMATE.CATEGORY:** Represents the episode of climate by year and based on thresholds for Oceanic Niño Index (ONI) ± 0.5 °C

**CAUSE.CATEGORY:** Category of event(s) causing the power outage

**CAUSE.CATEGORY.DETAIL:** Detailed description of the category of event causing the power outage

**OUTAGE.DURATION:** Duration of power outage in minutes

**CUSTOMERS.AFFECTED:** Number of customers affected by the power outage

**OUTAGE.START:** Starting date and time of power outage

**OUTAGE.RESTORATION:** Ending date and time of power outage

**POPULATION:** Total population of state at the time of reported outage

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

Finally, I wanted to see what the main causes of power outages were, and how they changed each year.
This table describes the count of each category cause in each year for the entire dataset. This is the first 11 rows of the table.

<details> 
	<summary> Click here for the full dataset </summary>

	<pre>
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
	</pre>

</details>


## Assessment of Missingness

There were many instances of power outages having missing values in the customers affected column. This section
attempts to address these values and find whether or not there are reasons for their missingness.

| CAUSE.CATEGORY                |   False |   True |
|:------------------------------|--------:|-------:|
| equipment failure             |      30 |     30 |
| fuel supply emergency         |       7 |     44 |
| intentional attack            |     199 |    219 |
| islanding                     |      34 |     12 |
| public appeal                 |      21 |     48 |
| severe weather                |     717 |     46 |
| system operability disruption |      83 |     44 |

From the table grouping by categories of power outage causes, intentional attacks look like the leading factor for missing values in customers affected.
The values may seem like they are NMAR since companies may be less likely to publish the number affected by outages caused intentionally for safety or security reasons.
Further information would be needed on the definition of intentional attacks and whether or not "sabotage" as seen two tables ago is considered just as dangerous
for the public as "vandalism". However it is important to point out that intentional attacks are not leading in proportions of non-missing to missing values. 
In order to see if perhaps these columns are indeed Missing at Random, we'll perform 2 permutation tests.

<iframe src="assets/plot-missing1.html" width=800 height=600 frameBorder=0></iframe>

This is the histogram showing the probability of getting a total variation distance after shuffling the affected missing column. 
The red line indicates the observed total variation distance from the dataset. We can say then that the missingness of values in the customers affected column may in fact depend on the cause of the power outage.

<iframe src="assets/plot-missing2.html" width=800 height=600 frameBorder=0></iframe>

Similarly this is the histogram for the probability of getting a total variation distance after shuffling, but based on climate conditions (cold, normal, warm). The red line indicates the observed total variation distance from the dataset.
We can see in this graph, in contrast to the first, that it seems reasonable to assume that the missingness of customers affected is most likely not dependent on the climate category. 

## Hypothesis Testing

In this section we'll conduct a hypothesis test in order to answer the question in our introduction. In order to do this we'll need to define our null and alternative hypotheses.

### Null Hypothesis: The average proportion of people affected by power outages per state is due to random chance

### Alternative Hypothesis: The average proportion of people affected by power outages per state is related to location and not random chance

For the test statistic I used, I found the average proportion of the population affected in *all* states. Additionally we'll use a significance level of 0.05.

Since there were some states where they had no customers affected total but had reported outages, I conducted 2 tests. One where the missing values were replaced by 0, assuming that the cause of the outage was a specific event that didn't majorly impact the grid, and another 
where I dropped the rows of states with missing values in order to find a more accurate average. The reason why I decided to do so will become clearer later.

<iframe src="assets/plot-hypotest.html" width=800 height=600 frameBorder=0></iframe>

For the test where I filled values with 0, the p-value calculated was = 0.0737. Since this was really close to my significance level to reject the null hypothesis I decided to recalculate with only rows where true proportions existed.
After re-testing, the calculated p-value comes out to 0.2007. This is much more within the distribution of the null hypothesis. In the graph above, the red represents the average in all states not including those with 0 proportions, and the orange represents the average in all states total.

In both cases we fail to reject the null hypothesis, and can say that it is likely that living in certain states does not increase your likelihood of experiencing a power outage.

Manually looking at the data shows that states with greater surface area and less population will have lower proportions of people affected (e.g Wyoming), and vice versa (e.g District of Columbia).







