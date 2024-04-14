# ACF584-Quarto-Assignment-GN
Tableau Dashboard coded using R.
Economic Development Impact on Standard of Living

library(tidyverse)
library(readr)

#data
unicef_indicator_1 <- read_csv("unicef_indicator_1.csv")
View(unicef_indicator_1)

unicef_metadata_Regions_Added <- read_csv("unicef_metadata_Regions_Added.csv")
View(unicef_metadata_Regions_Added)

#Introduction
This quatro document investigates Global inequality is a critical issue affecting lives that demands a global response. Global inequality can be defined as inequality between different country's populations.
By exploring the connection between global economic growth and the global standard of living, we can gain a deeper understanding of how the world's resources are distributed and how we can work to create a fairer, more equitable society. Additionally, trends in global development can be found which will allow for action and global response to negative global development trends. 




#Bar Chart 
Average_Observation_Value <- c (0.2876, 0.0244, 0.1927, 0.00484, 0.00250, 0.00011)
Continent <- c (1, 2, 3 , 4, 5, 6) 

Latin America and the Caribbean, South America, Europe)

1 = Africa
2 = Oceania
3 = Asia
4 = Latin America and the Caribbean
5 = South America
6. Europe

barplot(Average_Observation_Value, xlab = 'Continent', ylab = "Observation Value", main="% of children under 5 suffering from 3 or more deprivations.", names.arg = Continent)

Bar Chart
The bar chart shows that global inequality affects childhood development, with regional differences in the percentage of young children suffering from three or more deprivations being revealed.
The percentage of children suffering from three deprivations or more differs from region to region with massive differences between Europe (lowest percentage) when compared to Africa or Oceania (highest percentage). 


#MAP
world_map <- map data ("world")

#Merging Map Data and Indicator
merged_data <- full_join (world_map, unicef_indicator_1, by c = "region = "country")

#Map Attempt
ggplot(data = merged data) +
aes(x = long, y =lat, group =group fill) +
geom_polygon()



#Time Series
ggplot(data = unicef_indicator_1) +
  aes(x = year, y = Life expectancy, color = continent) +
  geom_line()
  

#Scatterplot
ggplot(data = unicef_indicator_1) +
  aes(x = gdpPercap, y = lifeExp, color = continent) +
  geom_point()
  
 This scatterplot investigates the connection between lower life expectancy and suffering deprivation during childhood. 
This scatterplot would have shown a positive relationship between children who suffer deprivations in childhood and lower life expectancy. 
 
Conclusion
Global Inequality is a growing problem that has long-term implications for society. Global Inequality increases the likelihood of young children suffering from deprivations, which has further implications such as lower life expectancy and lower standards of living. 
The traditional view that rising global economic growth leads to global prosperity for all is put into question by the findings displayed in this dashboard. Some regions of the world (Africa and Asia) are falling significantly behind global averages for GDP per capita and life expectancy which may lead to future generations of children suffering from deprivations in societies struggling to economically develop. 
Resolving global inequality will need a global solution that is more than global aid aimed at increasing economic development across the world, due to a decreasing correlation between economic growth and life expectancy. Thus, increasing investment into global healthcare, nutrition, and sanitation and creating long-term economic growth, particularly in the poorer regions of the world would seem to be the most effective solution to end global inequality.
 
  

