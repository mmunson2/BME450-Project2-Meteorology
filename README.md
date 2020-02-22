# BME450-Project2-Meteorology
## Matthew Munson
## 2/21/19


# Introduction:

This project tasked students with determining the correlation between wind speed and rain at two different weather stations off the Pacific Coast. We used the Ocean Observatories Initiative web resources to obtain a year worth of data for wind speed and rain rate. The selected locations were the Oregon Shelf Surface Mooring and the Oregon Offshore Surface Mooring Site. The Shelf mooring is located on the Pacific Continental Shelf at 80 meters depth with numerous instruments positioned at the seafloor and surface. The Oregon Offshore Surface Mooring is situated in deeper waters at a depth of 550 meters[2].

This project was completed in three portions. Wind speed and rain rate were first plotted over a year's worth of time for each location. Color coding was used to show the four combinations of no wind or rain, windy and rainy, windy but no rain, and rain but no wind. The second portion used correlation equations to find the relationship between each site. This was performed to see if the movement of a weather pattern from one location to another could be identified in the data. Finally, the monthly averaged wind speed and rain rate for each location was analyzed with the maximums and minimums identified.

# My Approach:

To complete this assignment I used a similar approach to project I in importing my data from the OOI website. This time because the amount of data was so large, I made a URL-generator to fetch one month of data at a time. This data was extracted from multiple files and fed into large lists of wind speed, rain rate, and time values.

The data was then fed through a validation cell which ensured that the time values were in order and that invalid wind speeds were set to zero. The time values are also converted from the OOI timestamp format to standard, then to Pacific time. 

With the data correctly formatted, the wind speed and rain rate graphs can be generated. These utilize four conditionals to determine if the it's not windy or rainy, windy and rainy, windy but not rainy, or rainy but not windy. Depending on the result the data point is plotted in a different color. Strips of color are overlayed in the background displaying the weather conditions at the given point in time.

The data from both locations is combined in the correlation function. This 



# Results/Plots:

Figure 1: Plot of Wind Speed vs. Time: Oregon Shelf Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/data/Shelf/2017ShelfWindSpeed.png "Shelf Wind Speed") 

Figure 2: Plot of Wind Speed vs. Time: Oregon Offshore Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/data/Offshore/2017OffshoreWind.png "Offshore Wind Speed")  


Figure 3: Plot of Rain Rate vs. Time: Oregon Shelf Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/data/Shelf/2017ShelfRain.png "Shelf Rain Rate")  

Figure 4: Plot of Rain Rate vs. Time: Oregon Offshore Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/data/Offshore/2017OffshoreRain.png "Offshore Rain Rate")  

Figure 5 & 6: Correlation Graphs
## Currently Unfinished 


Figure 5: Monthly Wind Speed and Rain Rate Averages: Oregon Shelf Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/data/Shelf/2017ShelfAverage.png "Shelf Average") 

Figure 6: Monthly Wind Speed and Rain Rate Averages: Oregon Offshore Surface Mooring

![alt text](https://github.com/mmunson2/BME450-Project2-Meteorology/blob/master/Data/Offshore/2017OffshoreAverage.png "Offshore Average") 

# Analysis and Conclusions:

Assignment Questions - 

## 1.	What is the highest correlation and at what time lag for…

  a.	Wind Speed?  
  b.	Rain Rate? 


## 2.	What patterns do you see in the monthly averages?

 


## 3.	Which month had the highest rain rate? Which month had the lowest rain rate?



## 4.	Which month had the highest wind speed? Which month had the lowest wind speed?



# References:

[1]	Currents.soest.hawaii.edu. (2020). SEM_EDOF. [online] Available at: https://currents.soest.hawaii.edu/ocn_data_analysis/_static/SEM_EDOF.html [Accessed 21 Feb. 2020].

[2]	Ocean Observatories Initiative. (2020). METBKA. [online] Available at: https://oceanobservatories.org/instrument-series/metbka/ [Accessed 21 Feb. 2020].






