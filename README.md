# PyBer-Analysis

# Overview of the Project 
The purpose of this project is to analyze all the rideshare data for PyBer (a Python based ride-sharing company) from January to early May of 2019 and create compelling visualizations telling a story about the data. Visualizations need to show the relationship between the type of city and number of drivers and riders as well as the average and total fares. The analysis produced can help PyBer improve access to ride-sharing services and determine affordability for underserved neighbourhoods.

The main visualizations will show a relationship between the Average Fare (Per City), the Total Number of Rides (Per City), and the Total Number of Drivers (Per City) for each city type (Urban, Suburban, and Rural). Another visualization is a time-series plot showing the total fare data for each city type overtime. Summary statistics and visualizations showing the distribution of data are included as well. 

# Software
Python 3.7.6; Jupyter Notebook; Matplotlib (3.5.0) library

# Data
- In the [Resources folder](https://github.com/Aigerim-Zh/PyBer-Analysis/tree/main/Resources) of this repository, you can find the original row datasets:
    - The ["city_data.csv"](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Resources/city_data.csv) contains 120 observations for "city", "driver_count", and "type" (city type) columns. The observations correspond to 120 unique city names.  
    - The ["ride_data.csv"](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Resources/ride_data.csv) contains 2375 daily observations for "city", "fare", "date", and "ride_id" corresponding to the period between 2019/01/14 and 2019/04/25. 
- Before merging, the data were checked for missing values, any potential mismatches, and if any cleaning is required. 

# Results

### Showing the Relationship for the City Type, the Average Fare, and the Total Number of Rides and Drivers. 

![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/BubbleChart_Avg%20Fare%20vs%20Tot%20Number%20of%20Rides.png)

From the bubble chart, we can see a clear trend in the datat. Urban cities have the highest number of drivers and rides and lowest fares, on average, compared to suburban and rural cities. Suburban cities have a higher number of drivers and rides and lower fares compared to rural. And, rural, have the highest fares and lowst number drivers and rides. 

## Summary Statistics for Each City Type

**Urban Cities**
![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Summary%20Statistics_Urban.png)

**Suburban Cities**
![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Summary%20Statistics_Suburban.png)

**Rural Cities**
![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Summary%20Statistics_Rural.png)


The "ride_id" does not make sense because it summarized the average of the ID number and not the count. 

## Summary Statistics of the Ride Count (Per City) for Each City Type

If we compare the average number of rides between each city type, we'll notice that the average number of rides in the rural cities is about 3.5 and 2.5 times lower than urban and suburban cities, respectively.

The median in each distribution is not that different from the mean, meaning that the distributions are normal.


The average fare price is the highest in rural cities

## Checking for outliers 

![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Box_and_whisker%20plot.png)
There is at least one outlier, closer to 40, for urban cities number of rides. 

There is one outlier in the urban ride count data. Also, the average number of rides in the rural cities is about 4- and 3.5-times lower per city than the urban and suburban cities, respectively.

## Total and Per Ride Summary Data by City Type
![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Summary%20Statistics.png)

- Customers in rural cities pay roughly $10 more, on average, than customers in urban cities.
- On the other hand, drivers in rural areas earn the highest fares, on average. The data shows roughly $40 more than in urban cities.
- There is the highest number of drivers in urban cities, 31 times the drivers in rural cities. 
- There is the highest number of rides in urban cities, 13 times the rides in rural cities; this, might also be explained by the fact that the average fare per ride is the lowest in urban areas. 

## Showing the Trend Over Time
![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Multiple%20line%20plot.png)

- The time-series plot shows that the same trend persists over time. 

# Summary
Based on the analysis above, the following conclusions and recommendations can be made:
- Rural cities are the most underrepresented:
    - They have the fewest number of PyBer drivers available, on average. 
    - At the same time, the drivers in rural cities earn the most, on average, compared to urban and suburban cities. 
    - Riders in rural cities have to pay the most, on average, than riders in urban and suburban cities. 
- Therefore, to increase PyBer's presence in rural areas, there need to be more drivers highered there and the fares need to decrease, on average. 
- However, it is important to account for other factors. Trips in rural areas might be with a longer distance, on average, and there is lower population size expected there as well. 