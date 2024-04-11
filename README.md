# Tableau with an Air Traffic Dataset

**Table of Contents:**
- [Introduction, Project Overview](#introduction-project-overview)
- [Questions to Explore](#questions-to-explore)
- [Data](#data)
- [Notebooks](#notebooks)
- [Configuration](#configuration)




## Introduction, Project Overview

This project is to showcase my fluency with Tablau.

#### Goal:

The goal of this project is to:
1. Answer the questions provided using Tableau.


## Questions to Explore

#### **Question 1:**
*Create visualizations to address the questions and add descriptive titles, subtitles, captions, and/or annotations for highlighting your insights.*

- **1.1** How do the three carriers compare in terms of total number of flights between 2018 and 2019?
- **1.2** How do the monthly number of flights vary over time for each of the three carriers?
- **1.3** What are the top 10 most highly utilized origin airports for the three carriers and how are the number of flights from these airports distributed between these carriers? Build a stacked bar chart to answer this question and describe the key patterns, similarities, and differences in how each carrier's flights are distributed at each of the 10 airports.

#### **Question 2:**
*We will investigate on-time performance next in terms of departure delays and cancellations.*

- **2.1** Create a calculated field that identifies on-time vs delayed departures: consider negative or missing delay times as on-time. Then, create a visualization that contrasts the number of on-time vs delayed flights broken down by month for the year 2019. Which month has the highest/lowest total number of delayed flights?
- **2.2** Create a highlight table (crosstab) that shows the average departure delay for each state broken down by year and fiscal quarter. Use the calculated field from the previous question to include only those flights that are delayed. What states have the highest departure delay for flights and when? Describe your insights and do some research why these delays could have occurred. Indicate which 3 states have the highest average delays in Q1 of 2019.
- **2.3** Next, generate a map of the US states which shows the average departure delay by state. Using this map and the tabulation from Q2.2, comment on notable trends or patterns observed in departure delays versus state.
- **2.4** How do the reasons reported for flight cancellation vary by month? Visualize the total number of cancelled flights for each month in both years broken down by the reason for cancellation. What trends do you notice about the flights cancelled?

#### **Question 3:**
*Next, we will analyze the fleet and distance traveled by each airline which can provide an indication of their revenue.*

- **3.1** How are flight times and distances related to one another? Create a scatter plot of average flight time vs average distance traveled on the airport level. What is the approximate range of flight times in which most flights in this dataset tend to lie? Include a trend line and comment on what this represents. Are there any outliers?
- **3.2** How do the three carriers compare year-over-year in terms of total distance flown and total number of planes in service? Use the "Year over year growth" quick table calculation to visualize the percent change in total distance flown and total unique tail numbers in 2019 vs 2018. Describe the differences between the three carriers.
- **3.3** Create a calculated field to show the average distance traveled per plane using the SUM() and COUNTD() functions. How do carriers compare in this respect? Visualize the average broken down by airline. Now, imagine we want to start thinking about carrier profits, even though we have no data on costs or revenue. Which airline do you believe is the most efficient in terms of costs per mile flown and why?

#### **Question 4:**
*Finally, the fund managers would like an interactive dashboard to explore the data further about departure delays and cancellations state-by-state. Your goal is to use Q2.3, Q2.4 and to create one extra visual of your choice for the dashboard (you can, for example, look into the cancellation rates). Make sure you enable some interactive capabilities to filter the data in order to dig into the details.*


## Data: 

The data has been sourced from the open data portal at the [Bureau of Transportation Statistics](https://www.transtats.bts.gov/DatabaseInfo.asp?QO_VQ=EFD&DB_URL=).  It is available for download in SQL format [here](https://drive.google.com/file/d/1eAg_CWEChp9W1o4ebgp29oKrZyDArW7Y/view?usp=sharing).


### Data Dictionaries:

#### Airports table:

| COLUMN      | TYPE   | DESCRIPTION                     |
|-------------|--------|---------------------------------|
| AirportID   | int    | unique airport code (Primary Key) |
| AirportName | string | Full name of airport            |
| City        | string | Airport city                    |
| Country     | string | Airport country                 |
| State       | string | Airport state                   |
| Latitude    | float  | Latitude of airport             |
| Longitude   | float  | Longitude of airport            |


#### Flights table:


| COLUMN                           | TYPE   | DESCRIPTION                                                       |
|----------------------------------|--------|-------------------------------------------------------------------|
| FlightID                         | int    | Unique ID number for each flight (Primary Key)                    |
| FlightDate                       | date   | Date of flight departure                                          |
| ReportingAirline                 | string | DOT Unique Carrier Code                                           |
| TailNumber                       | string | FAA Tail number identifying flight                                |
| FlightNumberReportingAirline     | string | Public flight number                                              |
| OriginAirportID                  | int    | Origin / departure airport code                                   |
| DestAirportID                    | int    | Destination / arrival airport code                                |
| CRSDepTime                       | string | Scheduled local departure time                                    |
| DepTime                          | string | Actual local departure time                                       |
| DepDelay                         | int    | Difference in minutes between scheduled and actual departure time |
| TaxiOut                          | int    | Taxi out time, in minutes                                         |
| WheelsOff                        | string | Wheels off in local time                                          |
| WheelsOn                         | string | Wheels on in local time                                           |
| TaxiIn                           | int    | Taxi in time, in minutes                                          |
| CRSArrTime                       | string | Scheduled arrival time                                            |
| ArrTime                          | string | Actual arrival time                                               |
| ArrDelay                         | int    | Difference in minutes between scheduled and actual arrival        |
| Cancelled                        | int    | Cancelled indicator                                               |
| Diverted                         | int    | Diverted indicator                                                |
| AirTime                          | int    | Flight time (total time in the air) in minutes                    |
| Distance                         | float  | Distance between airports in miles                                |
| AirlineName                      | string | DOT full airline name                                             |
| CancellationReason               | string | Reason for cancellation                                           |



## Notebooks

This project is contained in a single .twb file. 



## Configuration

This work was performed on Tableau Professional Edition, 2023.3.4 (20233.24.0314.1442).


If you have any questions about this project, I would love to speak with you!  Please don't hesitate to reach out:
Phone: +1 778 995 7801
Email: [Drewe.MacIver@gmail.com](mailto:drewe.maciver@gmail.com)
LinkedIn: [Drewe MacIver on LinkedIn](https://www.linkedin.com/in/drewe-maciver/)
Portfolio: [DreweItWithData.com](https://www.dreweitwithdata.com)
