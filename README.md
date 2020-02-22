# BME450-Project2-Meteorology
Matthew Munson   
2/21/19   
Profesor Shima Abadi   

# Preface:

A recent class discussion highlighted the importance of pointing out when the data you've processed does not appear to be accurate. Regardless of fault, whether it be the source or the method of processing, we decided as a class that it's up to the data scientist to identify when something is wrong. I would like to point out that the data I have processed in this assignment does not appear to be entirely accurate, and I believe that further analysis and refinement is required before this data is used for any purpose. The most significant source of error is that the time values between the two locations don't match up perfectly, and the correlation and lag data is inaccurate as a result. Smaller sources of error include inaccurate wind speed readings within the data and small gaps in time due to bad timestamps being removed.


# Introduction:

This project tasked students with determining the correlation between wind speed and rain at two different weather stations off the Pacific Coast. We used the Ocean Observatories Initiative web resources to obtain a year worth of data for wind speed and rain rate. The selected locations were the Oregon Shelf Surface Mooring and the Oregon Offshore Surface Mooring Site. The Shelf mooring is located on the Pacific Continental Shelf at 80 meters depth with numerous instruments positioned at the seafloor and surface. The Oregon Offshore Surface Mooring is situated in deeper waters at a depth of 550 meters[2].

This project was completed in three portions. Wind speed and rain rate were first plotted over a year's worth of time for each location. Color coding was used to show the four combinations of no wind or rain, windy and rainy, windy but no rain, and rain but no wind. The second portion used correlation equations to find the relationship between each site. This was performed to see if the movement of a weather pattern from one location to another could be identified in the data. Finally, the monthly averaged wind speed and rain rate for each location was analyzed with the maximums and minimums identified.

# My Approach:

To complete this assignment I used a similar approach to project I in importing my data from the OOI website. This time because the amount of data was so large, I made a URL-generator to fetch one month of data at a time. This data was extracted from multiple files and fed into large lists of wind speed, rain rate, and time values.

The data was then fed through a validation cell which ensured that the time values were in order and that invalid wind speeds were set to zero. The time values are also converted from the OOI timestamp format to standard, then to Pacific time. 

With the data correctly formatted, the wind speed and rain rate graphs can be generated. These utilize four conditionals to determine if the it's not windy or rainy, windy and rainy, windy but not rainy, or rainy but not windy. Depending on the result the data point is plotted in a different color. Strips of color are overlayed in the background displaying the weather conditions at the given point in time.

The data from both locations is combined in the correlation function. This determines whether there are any similar patterns between the two locations in wind speed or rain rate. This would indicate a weather pattern moving from one location to another. The time lag, or the amount of time between the two locations having similar values, is measured and recorded.

Finally, average graphs are created with rain rate and wind speed averaged over an entire month. This is achieved by tracking the indicies where a month begins and summing only those numbers. These are plotted with two scales, one for wind speed and the other for rain rate.

# Results/Plots:

#### Figure 1: Plot of Wind Speed vs. Time: Oregon Shelf Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/Data/Shelf/2017ShelfWindSpeed.png "Shelf Wind Speed") 

#### Figure 2: Plot of Wind Speed vs. Time: Oregon Offshore Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/Data/Offshore/2017OffshoreWind.png "Offshore Wind Speed")  


#### Figure 3: Plot of Rain Rate vs. Time: Oregon Shelf Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/Data/Shelf/2017ShelfRain.png "Shelf Rain Rate")  

#### Figure 4: Plot of Rain Rate vs. Time: Oregon Offshore Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/Data/Offshore/2017OffshoreRain.png "Offshore Rain Rate")  

#### Figure 5: Wind Speed Correlation:

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/Fixed/Data/Correlation/WindSpeedCorrelation.png "Wind Speed Correlation")  

#### Figure 6: Rain Rate Correlation:

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/Fixed/Data/Correlation/RainRateCorrelation.png "Rain Rate Correlation")  

#### Figure 7: Monthly Wind Speed and Rain Rate Averages: Oregon Shelf Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/Data/Shelf/2017ShelfAverage.png "Shelf Average") 

#### Figure 8: Monthly Wind Speed and Rain Rate Averages: Oregon Offshore Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/Data/Offshore/2017OffshoreAverage.png "Offshore Average") 

# Analysis - Assignment Questions:

### 1.	What is the highest correlation and at what time lag for…

  a.	Wind Speed?  
  
  Max Correlation: 1.00
  Time Lag: 0
  
  b.	Rain Rate? 

  Max Correlation: 0.218
  Time Lag: 47 seconds


### 2.	What patterns do you see in the monthly averages?

The monthly average plots show a pattern of decreased precipitation in the Summer and an increase during the Winter months. This is consistent with Northwest weather, especially considering the dry Summer of 2017 which had record breaking wildfires. Average wind speed is also highest during the winter and lowest in the month of September for both locations. There is a steep increase in average wind speed between September and October, consistent with the Autumn storms that begin early in the season. The decrease in wind speeds and precipitation from Winter into Spring is more gradual than the increase from Summer into Fall.


### 3.	Which month had the highest rain rate? Which month had the lowest rain rate?

The month of February had the greatest rain rate for both locations, averaging 7 mm per hour at the Oregon Shelf and nearly 8.5 mm per hour at the offshore mooring. This reflects the rainy Northwest winters we’re familiar with. The month of July had the lowest rain rate, averaging just over 5 mm per hour at both locations. This reflects the weather in July of 2017, which was a particularly dry month.


### 4.	Which month had the highest wind speed? Which month had the lowest wind speed?

Compared to precipitation, wind speed varied considerably between the Oregon Shelf and Oregon Offshore moorings in the year of 2017. At the Shelf Surface Mooring, the month with the greatest wind speed was March, averaging just over 7 meters per second. While the offshore mooring had similar numbers for the month of march, it averaged 8.5 meters per second in the month of November, nearly 2 meters per second faster than what was recorded at the shelf. This is likely a result of error in the shelf data, which may have had a greater percentage of inaccurate readings or a smaller amount of data points to average.


#  Conclusions

This project introduced concepts related to handling, filtering, and processing large amounts of data. It was also my first time finding the correlation between two data sources, which I now understand is a fundemental aspect of data science. It's clear that parts of my data are not entirely accurate in part due to the data source and my code as well. I feel that it's important to acknowledge these shortcomings, especially if this data were to be used for any purpose other than grading. If I had more time to improve this assignment I would find a way to ensure that the recording times were exactly the same, and that all gaps or abnormalities in the time data were accounted for. 


# References:

[1]	Currents.soest.hawaii.edu. (2020). SEM_EDOF. [online] Available at: https://currents.soest.hawaii.edu/ocn_data_analysis/_static/SEM_EDOF.html [Accessed 21 Feb. 2020].

[2]	Ocean Observatories Initiative. (2020). METBKA. [online] Available at: https://oceanobservatories.org/instrument-series/metbka/ [Accessed 21 Feb. 2020].






