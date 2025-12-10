# Global Agriculture

## Analysis of Arable Land, African Cassava Crop Yield, and United States Fertilizer Use vs. Wheat Crop Yield
### Bridget Carl

# Our World in Data
The data used in this analysis was sourced from Our World in Data, from a 2017 article by Hannah Ritchie and Max Roser. The five individual data sets were compiled through a Github Tidy Tuesday posting, and was downloaded on March 17, 2021.

## Data Cleaning
First, I cleaned the data sets for ease of analysis. For each data set, I cleaned and shortened the column names. For the “land_use” data set, I converted the “year” variable to a numeric type. I then saved each cleaned data set as a new .csv file in the “data_processed” folder.

# Exploratory Analysis
## Research Questions
1. Which entity had the largest amount of arable land needed to produce a 1961-equivalent amount of agricultural output in 2014?

2. How has cassava crop yields in Nigeria changed over time?

3. How has the wheat yield in the United States changed between 2002 and 2014 as compared to fertilizer use in the same time period?

# Arable Land
Arable land is land that is capable of growing crops. In the “arable_land_analysis” data set, the measure “arable_land” refers to the area of arable land needed to produce an equivalent aggregate of crop production, relative to base year 1961. This measures how a entity’s amount of arable land, or agriculture potential, has changed over time. As it measures the amount of arable land needed to produce some base amount of agricultural output, this variable measures how a entity’s agricultural productivity has changed over time.


<img width="2088" height="1152" alt="image" src="https://github.com/user-attachments/assets/806a8bb5-eb0f-4bba-9996-9dfb46dc11f8" />


<img width="2088" height="1152" alt="image" src="https://github.com/user-attachments/assets/731fb1c4-56a2-4c6b-b9e4-4fb55f7acfcb" />


To begin, I found some centrality and variability measures for the “arable_land” variable. Across all observable entities in 2014, the mean measure of arable land was 0.6331678 and the median measure of arable land was 0.4444402. That is, the amount of arable land needed to produce a base-1961 aggregate of crops has decreased across countries and areas, on average. This ranges across an arable land index of 5.883782 with a standard deviation of 0.7179257, indicating great variation across areas. Further, the interquartile range is 0.4105596, meaning that the “middle 50%” of observations had an arable land index across 0.4105596. This variation is likely accounted for by the 15 outliers found in the above boxplot. As seen in the above histogram, the “arable_land” variable is unimodal, and most observations fell about the median observation of 0.4444402, below the mean observation. While the variable is not normally distributed, most observations do cluster about the center, except for the large amount of outliers.


<img width="2016" height="1152" alt="image" src="https://github.com/user-attachments/assets/5d4c9980-e447-473d-a591-75ef458fa2ad" />


To visualize this variable, I chose to use a lollipop chart to highlight the top 15 observations in 2014. I chose this type of chart to plot the measure across several categories, starting at zero as to ensure proportional visualization. I chose a lollipop chart over a bar chart since I am not highlighting a single entity and to reduce the amount of overpowering information on the plot. I also chose to only plot the top 15 observations since below that observation, there is little variation across observations. These observations are also the 15 outliers found in the above boxplot.

These 15 entities require the largest area of arable land to produce the same amount of crop than in 1961. That is, these entities have improved their agricultural productivity the least across time. All of these entities have an arable land index above 1, indicating that more land is needed to produce the same amount of base-1961 agricultural output. These entities are nearly all small islands with small economies, so it is challenging to compare these to countries like the United States or Mexico whose agricultural output account for a major portion of the economy.

# Nigerian Cassava Yield Over Time

How has the yield of cassava, a key Nigerian crop, changed over time? I knew that cassava was a major component of African agriculture, and chose to study Nigerian yields specifically as it remains the largest producer of cassava globally according to the Food and Agriculture Organization of the United Nations. While large scale production of cassava in Nigeria is rare, the country still accounts for 20% of the world’s cassava production and that crop is a major component of the Nigerian economy. The variable used in this analysis is “yield_ton_per_hectare” in the “key_crop_yields_analysis” data set. This variable measures the metric tonne output of the crop in question per hectare of land, or 1000 kg.


<img width="2088" height="1152" alt="image" src="https://github.com/user-attachments/assets/38ff9079-1765-4399-ad0d-54ffa33777e0" />


<img width="2088" height="1152" alt="image" src="https://github.com/user-attachments/assets/2a07f8e4-9404-4db0-89d0-cd88303cc53d" />


To begin, I found some centrality and variability measures for the “yield_ton_per_hectare” variable. In Nigeria from 1961 to 2018, the mean output of cassava was 10.1566 tonnes per hectare and the median output was 10 tonnes per hectare. This ranges across 5.1832 tonnes per hectare with a standard deviation of 1.06422. Further, the interquartile range is 1.400125, meaning that the “middle 50%” of yearly aggregate cassava yields fell across 1.400125 tonnes per hectare. Across 57 years, this does not indicate drastic variation. The above boxplot demonstrates this, as there is only one lower outlier. As seen in the above histogram, the “yield_ton_per_hectare” variable is unimodal, and most observations fell about the median observation of 10 and mean observation of 10.1566, but not tightly. While the observations do not cluster normally, the median and mean observations are very close.


<img width="2016" height="1152" alt="image" src="https://github.com/user-attachments/assets/2168aad5-dac8-4475-b44b-5dd772f28025" />


The Nigerian cassava yield is visualized in the above line plot. I chose to plot the cassava yield over time with this line plot to visualize a trend. Since the data does not tightly fall about the mean observation, I chose to include points for each year as to not allude to a tight trend line. I chose to highlight the trend line in red and the points in a light grey, since the research question directly refers to the change in cassava yields over time, i.e. the trend line. The y-axis is truncated. This works because there is little variation in the trend line in the early observable years, and there are no observations with zero cassava yields. I chose to not estimate a regression coefficient for the slope of the trend line, as that would require a much more robust analysis that is beyond the purview of this course.

As seen in the plot, Nigerian cassava yields increased, albeit slightly, between 1961 and 1999 with a drastic decline since then. This is not entirely surprising, since the Food and Agriculture Organization of the United Nations reported that major cassava production is rare in Nigeria and most production is from small family-operated farms. It is not implausible that over time there has been little engineering advancements in terms of cassava production if the production is not centered about a few major corporations. The Food and Agriculture Organization of the United Nations also reported challenges in exporting cassava in recent years, resulting in the decline seen in the above plot. Other countries with more centralized agricultural production has taken a competitive advantage in exporting cassava in recent years.

# United States Wheat Yield vs Fertilizer Use

How has the US wheat yield changed over time as compared to nitrogen fertilizer use from 2002 to 2014? (The sourced data set does not include fertilizer use information other than from 2002 to 2014.) I chose to study wheat specifically as it is a historically major component of agricultural output across the country. Nitrogen fertilizer is also an important component of the US wheat production, according to the Michigan State University College of Agricultural and Natural Resources. The wheat crop yield measure was found in the “key_crop_yields_analysis” data frame, as the “yield_ton_per_hectare” variable specified to US wheat crop. This variable measures yield in metric tonne per hectare, or 1000 kg. The nitrogen fertilizer use measure was found in the “fertilizer_analysis” data frame, as the “fertilizer_use” variable specifically to the US. This variable measures fertilizer use in kilograms per hectare.

## Wheat Crop Yield


<img width="2088" height="1152" alt="image" src="https://github.com/user-attachments/assets/eea860b2-35cc-44eb-b74a-3cbb81c11adb" />


<img width="2088" height="1152" alt="image" src="https://github.com/user-attachments/assets/c877e74b-72bb-433c-8f08-36efbcfa037d" />

To begin, I found some centrality and variability measures for the “yield_ton_per_hectare” variable. In the US from 2002 to 2018, the mean output of wheat was 2.895646 tonnes per hectare and the median output was 2.9422 tonnes per hectare. This ranges across 0.8106 tonnes per hectare with a standard deviation of 0.2281828. Further, the interquartile range is 0.1944, meaning that the “middle 50%” of yearly aggregate wheat yields fell across 0.1944 tonnes per hectare. Across 16 years, this suggests some variation across observations. The above boxplot demonstrates this, as there is only one lower outlier. As seen in the above histogram, the “yield_ton_per_hectare” variable is bimodal, and most observations fell above the mean and median observation. While the observations do not cluster normally, the median and mean observations are very close.

## Fertilizer Use

<img width="2088" height="1152" alt="image" src="https://github.com/user-attachments/assets/aedfdaec-1567-4cce-9292-af86c1f76246" />

<img width="2088" height="1152" alt="image" src="https://github.com/user-attachments/assets/4cd05f32-93e4-4076-a0ed-c371d7f4614a" />


Next, I found some centrality and variability measures for the “fertilizer_use” variable. In the US from 2002 to 2014, the mean use of fertilizer was 70.59562 kg per hectare and the median use was 70.08 kg per hectare. This ranges across 15.18 kg per hectare with a standard deviation of 4.700416. Further, the interquartile range is 7.9775, meaning that the “middle 50%” of yearly aggregate fertilizer usage in the US fell across 7.9775 kg per hectare. Across 14 years, this suggests some variation. The above boxplot demonstrates this, as there are no outliers but the middle 50% of observations spread a large amount of observations. As seen in the above histogram, the “yield_ton_per_hectare” variable is unimodal, and most observations fell below the median observation of 70.08 and the mean of 70.59562. While the observations do not cluster normally, the median and mean observations are very close.

## Fertilizer Use vs. Wheat Yield

To visualize how the US wheat yield has changed over time as compared to fertilizer use, I merged the “key_crop_yields_analysis” and “fertilizer_use_analysis” data frames to create the “fertilizer_wheat2” data frame. This merged data frame includes variables for entity, year, crop, crop yield, and fertilizer use. I also added the variables “yield_change” and “fertilizer_change” that measures the percent change of wheat yields and fertilizer use from 2002, respectively.


<img width="1440" height="2016" alt="image" src="https://github.com/user-attachments/assets/785b7cd1-4224-4c9a-b95e-21aa15bc0972" />


To visualize the relationship between fertilizer use and wheat yield, I used the above line graph including the specific points for the yearly observations over time. I chose a theme with minimal grid lines and labeled the lines individually to limit distracting information on the plot. I chose to plot each curve in red and steel blue since this color scheme represents two distinct entities and are opposing in the color wheel. I also chose to plot the percent change to each measure rather than the discrete measure since the discrete measures differ so greatly in scale between the two variables. With a common scale, very little variation could be seen between the two measures (the variables differ by a magnitude of 1000.) The pattern does not follow a logarithmic pattern, so a log scale would be inappropriate. By measuring it this way, I can still estimate how the two values change in relation to each other while not altering the scale in a poor way.

As seen in the overlaying line graphs, the change to US wheat yield tends to follow the trend for change to nitrogen fertilizer use, as compared to 2002. This is what I would have expected, given the information from MSU College of Agriculture and Natural Resources. Nitrogen fertilizer increases wheat crop yields to a certain point, alluding that if too much nitrogen is used there will be a decline in crop yields. That may have occurred in 2006, where the change to wheat yields declined sharply after a sharp increase in the change to fertilizer use. The overall trend is also entirely logical as agricultural production tends to be large-scale and corporate-based in the US, thus there is more centralized decision making in the agricultural production process. The corporations involved in wheat production make informed, profit-oriented decisions that best utilize fertilizer use to optimize output.











