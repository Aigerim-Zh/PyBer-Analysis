# PyBer-Analysis

# Overview of the Project 
The purpose of this project is to analyze all the rideshare data for PyBer (a Python-based ride-sharing company) from January to early May of 2019 and create compelling visualizations telling a story about the data. Visualizations need to show the relationship between the type of city and the number of drivers and riders as well as the average and total fares. The analysis produced can help PyBer improve access to ride-sharing services and determine affordability for underserved neighborhoods.

The main visualizations will show a relationship between the Average Fare (Per City), the Total Number of Rides (Per City), and the Total Number of Drivers (Per City) for each city type (Urban, Suburban, and Rural). Another visualization is a time-series plot showing the total fare data for each city type over time. Summary statistics and visualizations showing the distribution of data are included as well. 

# Software
Python 3.7.6; Jupyter Notebook; Matplotlib (3.5.0) library

# Data
- In the [Resources folder](https://github.com/Aigerim-Zh/PyBer-Analysis/tree/main/Resources) of this repository, you can find the original row datasets:
    - The ["city_data.csv"](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Resources/city_data.csv) contains 120 observations for "city", "driver_count", and "type" (city type) columns. The observations correspond to 120 unique city names.  
    - The ["ride_data.csv"](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Resources/ride_data.csv) contains 2375 daily observations for "city", "fare", "date", and "ride_id" corresponding to the period between 2019/01/14 and 2019/04/25. 
- Before merging, the data were checked for missing values, any potential mismatches, and if any cleaning is required. 

# Notes
There are two Jupyter Notebooks. 
- [PyBer_Challenge.ipynb]() includes the code for the data summary by city type including total rides, total drivers, total fares, average fare per ride, and average fare per driver. 
- [PyBer_Analysis1.ipynb]() contains the code for the rest of the analysis. 

# Results

### Showing the Relationship for the City Type between the Average Fare, and the Total Number of Rides and Drivers 

![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/BubbleChart_Avg%20Fare%20vs%20Tot%20Number%20of%20Rides.png)

From the chart above, we can see a clear trend in the data. Urban cities have the highest number of drivers and rides and lowest fares, on average, compared to suburban and rural cities. Suburban cities have a higher number of drivers and rides and lower fares compared to rural. And, rural, have the highest fares and lowest number of drivers and rides. 

## Summary Statistics for Each City Type

### Ride Counts 

| Metrics | Urban | Suburban | Rural| 
| --------| ------| ---------| -----| 
| count   | 66.00 | 36.00| 18.00|
| mean    | 24.62 | 17.36| 6.94|
| std     |  5.41 | 4.32| 2.50|
| min     | 12.00 | 9.00| 3.00|
| 25%     | 21.00 | 14.00| 5.25|
| 50%     | 24.00 | 17.00| 6.00|
| 75%     | 28.00 | 19.25| 8.75|
| max     | 39.000 | 27.00| 12.00|
| mode    | 22 (7 times)|  17 (7 times| 6 (5 times)|

- The average number of rides in rural cities is about 3.5 and 2.5 times lower than that in urban and suburban cities, respectively.
- The median in each distribution is not that different from the mean, i.e., the distributions are normal and no major skewness is expected. 

### Driver Counts 

| Metrics | Urban | Suburban | Rural| 
| --------| ------| ---------| -----| 
| count   | 66.00 | 36.00| 18.00|
| mean    | 36.44 | 13.61|4.33|
| std     | 19.83 | 8.02| 2.82|
| min     | 3.00  |1.00| 1.00|
| 25%     | 22.00| 6.50|1.25|
| 50%     | 37.00 | 15.00| 4.00|
| 75%     | 49.75 | 20.25| 7.00|
| max     | 73.00 | 25.00| 9.00|
| mode    |39 (86 times)|  20 (79 times| 1 (32 times)|

- The average number of drivers in rural cities is about 8.4 and 3.1 times lower than that in urban and suburban cities, respectively. 
- The median in each distribution is not that different from the mean, i.e., the distributions are normal and no major skewness is expected. 
- One interesting observation is that there are 32 rural cities where there is only one PyBer driver available. 

### Price Fare 

| The mean fare price for urban trips is $24.53.| 
| The median fare price for urban trips is $24.64.| 
| The mode fare price for urban trips is ModeResult(mode=array([22.86]), count=array([5]))|
| |
| The mean fare price for suburban trips is $30.97.| 
| The median fare price for suburban trips is $30.75.| 
| The mode fare price for suburban trips is ModeResult(mode=array([17.99]), count=array([3]))| 
| |
| The mean fare price for rural trips is $34.62.| 
| The median fare price for rural trips is $37.05.| 
| The mode fare price for rural trips is ModeResult(mode=array([37.05]), count=array([2])|

## Checking for outliers 

![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Box_and_whisker%20plot.png)
There is at least one outlier, closer to 40, for urban cities number of rides. 

There is one outlier in the urban ride count data. Also, the average number of rides in the rural cities is about 4- and 3.5-times lower per city than the urban and suburban cities, respectively.

## Total and Per Ride Summary Data by City Type
![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Summary%20Statistics.png)

- Customers in rural cities pay roughly $10 more, on average, than customers in urban cities.
- On the other hand, drivers in rural areas earn the highest fares, on average. The data shows roughly $40 more than in urban cities.
- The number of drivers in urban cities is, on average, 31 times higher than that in rural cities.
- The number of rides in urban cities is, on average, 13 times higher than that in rural cities; this might also be explained by the fact that the average fare per ride is the lowest in urban areas. 

## Showing the Trend Over Time
![](https://github.com/Aigerim-Zh/PyBer-Analysis/blob/main/Analysis/Multiple%20line%20plot.png)

- The time-series plot shows that the same trend persists over time. 

# Summary
Based on the analysis above, the following conclusions and recommendations can be made:
- Rural cities are the most underrepresented:
    - They have the fewest number of PyBer drivers available, on average. 
    - At the same time, the drivers in rural cities earn the most, on average, compared to urban and suburban cities. 
    - Riders in rural cities have to pay the most, on average, than riders in urban and suburban cities. 
- Therefore, to increase PyBer's presence in rural areas, there need to be more drivers hired there and the fares need to decrease, on average. 
- However, it is important to account for other factors. Trips in rural areas might be with a longer distance, on average, and there is a lower population size expected there as well. 