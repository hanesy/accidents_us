# Accidents in the United States
__Team AAA: Dagney Cooke, Diana Silva, Heain Yee__  
Project 1 (January 2020); UC Berkeley Data and Analytics Bootcamp  

## Introduction
The project group sought to review data regarding the car accidents in the United States. We reviewed data on reported car accidents across the United States between 2016 and 2019. We sought to answer the following questions:

1. Have car accidents increased over time?
2. Where do the highest number of accidents occur, and where do the most severe accidents occur?
3. When do the highest number of accidents occur?
4. Under what weather conditions do accidents occur?
5. Is there any correlation between different traffic infrastructure and frequency of accidents? Between street direction and accidents?

This file contains the executive level summary. Detailed findings, methodology, and limitations are available within the final presentation at this [link](https://docs.google.com/presentation/d/1Qo-e_8BA8SlvF52k39OP4iQ8TkSZ4GOLJ6O3hjBERls/edit?usp=sharing).

## Findings

### 1. Have car accidents increased over time?
*(Slide 5)*

There was a 120% increase in the number of reported car accidents from 2016 to 2018.

We recognized that the increase in accidents data could be driven by the following factors:
1. Increase in population/drivers
2. Increase in rate of accidents reported
3. Increase in the actual occurence of accidents

For the scope of our project, we wanted to make sure to normalize for population in answering our geographic questions. 
_(Data about the rate of accidents reported or the actual occurence of accidents was unavailable at the time of the project.)_

### 2. Where do the highest number of accidents occur, and where do the most severe accidents occur?
*(Slides 6 through 8 (and appendix slide 19); focused on 2017)*

We found that the highest number of accidents occured where there were the most number of drivers (California, Texas, Florida). However, when we adjusted for population, South Carolina had the highest rate of accidents, followed by California and North Carolina.

Approximately half of Wyoming and Arkasas's accidents were likely to be reported as severe (i.e., to cause long delay). Despite having had the most number of accidents, accidents in California, Texas, and Florida were less likely to be reported as severe.

### 3. When do the highest number of accidents occur?
*(Slide 9 (and appendix slide 21, 22); focused on 2017)*

We found that a higher number of accidents occured during commute times (i.e., 7 am to 9 am and 4 pm to 6 pm).

We found that a number of accidents occured between August and December.

### 4. Under what weather conditions do accidents occur?
*(Slide 10; 2016 to 2018)*

Looking purely at the number of accidents per weather condition, we can see that 51% of the total accidents between 2016 and 2018 occurred when it was a Cloudy weather and 38% when it was Clear. The third biggest Weather condition with most accidents is Rain with only 7%.

Even though the accidents occur mostly when supposedly there are the best weather conditions (visibility, road conditions), we would have liked to normalize this data per average number of days in a year of the different weather conditions. However, we were unable to normalize the accident data with weather data that was available to us during the course of this project. 

We believe that we could have better insights on correlations between the number of accidents and the road conditions if had the information of the road conditions at the time of the accident.

### 5. Is there any correlation between different traffic infrastructure and frequency of accidents? Between street direction and accidents?
*(Slide 11-13; 2016 to 2018)*

While we found that fewer accidents occur near traffic infrastructure than not, there were a lot of questions that arose about what exactly this data meant.  The data set creator does not describe what “near” means, is this a distance or just a general observation by the reporting officer?  Can an accident be near multiple types of infrastructure (it could be near an amenity and a crossing and a traffic signal).  This data is not necessarily either/or, but it presented as such in the data set.  While the indication is that the highest number of accidents occur at traffic infrastructure where cars meet going in different directions, it’s hard to tell what data we’re missing.

In examining different street types, we were able to parse out whether a street was “local” or a highway/freeway/type, but there are many things to consider about those classifications.  Is a highway always more than two lanes?  Can’t local streets or roads be multi-laned as well?  Is it better to classify based on speed limits of the road, or the speed the cars were going?  While we can make general assumptions about more accidents occurring on what we have categorized as “multi-lane/high speed” vs “local roads”, this question requires a deeper dive into a whole other slew of variables to really figure out how exactly to classify these different types of streets.

We also looked at whether there were more accidents on roads that went N/S, or roads that go W/E.  The data shows that more accidents occur on N/S roads than W/E roads, for roads that have a cardinal direction designation.  It would be interesting to look into how many N/S roads there are vs W/E, or determine which bucket the roads without a direction designation fall into.  There’s also the question that roads do not always maintain a perfect N/S orientation, and thus accidents could occur on a N/S while the car is actually moving E/W.  Another question to take into account would be direction and sunrise/sunset times - are E/W roads more dangerous during sunrise and sunset when drivers could be blinded?  Can this be merged with the data on accident frequency based on time of day?

## Sources 
### Accident Data
[link to kaggle](https://www.kaggle.com/sobhanmoosavi/us-accidents)

* Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, and Rajiv Ramnath. “A Countrywide Traffic Accident Dataset.”, 2019.
* Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, Radu Teodorescu, and Rajiv Ramnath. "Accident Risk Prediction based on Heterogeneous Sparse Data: New Dataset and Insights." In proceedings of the 27th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems, ACM, 2019. 
### Other Relevant Data
* ACS: Population data by [state](https://www.census.gov/content/census/en/data/tables/time-series/demo/popest/2010s-state-total.html#par_textimage_1574439295), [county](https://www.census.gov/content/census/en/data/tables/time-series/demo/popest/2010s-counties-total.html#par_textimage_242301767), [city](https://www.census.gov/content/census/en/data/tables/time-series/demo/popest/2010s-total-cities-and-towns.html) 
* Department of Transportation: ["Highway Statistic 2017 - Licensed Drivers by State"](https://www.fhwa.dot.gov/policyinformation/statistics/2017/)
* National Center for Environmental Information: [Climate Data Online for Denver, San Francisco and Rhode Island](https://www.ncdc.noaa.gov/cdo-web/)
