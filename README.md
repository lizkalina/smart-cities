
## [Smart Cities Hack](http://www.wimldsdatadive.com/hackathons/2) - Hosted by Women in Machine Learning & Data Science

### Questions Explored
Is there a correlation between tree count and perceived safety in NYC neighborhoods? Can this be modeled for various blocks and zip codes?

### Datasets Used
+ [2015 Tree Census Data](https://data.cityofnewyork.us/Environment/2015-Street-Tree-Census-Tree-Data/uvpi-gqnh) - Street tree data from the TreesCount! 2015 Street Tree Census
+ [MIT StreetScore](http://streetscore.media.mit.edu/data.html) - Perceived safety scores calculated with computer vision algorithms
+ [NYC 2010 Block Census GeoJSON](https://data.cityofnewyork.us/City-Government/2010-Census-Blocks/v2h8-6mxf)
+ [NYC Zip Code shapefiles](https://data.cityofnewyork.us/Business/Zip-Code-Boundaries/i8iw-xf4u/data)

### Tools Used
+ Pandas
+ GeoPandas
+ Matplotlib

## Discoveries

From my investigation, I learned that there is a minimal correlation between feeling safe and number of trees. I first aggregated by city block, but after realizing this introduced too much noise, I began working at the zip code level which provided much more of a signal. Some sections of the city (such as Brooklyn and Queens) have a stronger correlation between trees and safety. As next steps, I would like to focus my analysis on one borough and incorporate additional datasets — perhaps population, crime statistics and housing stock information — to see if they are better indicators.

![correlation](https://github.com/lizkalina/smart-cities/blob/master/plots/scatterplot.jpg)

There were clear outliers in the dataset particularly for tree count by block. In order to get a more accurate picture of the relationship between tree count and perceived safety, I removed data points more than 3 standard deviations from the mean for each metric.

<img src="https://github.com/lizkalina/smart-cities/blob/master/plots/tree_count.jpg" width="425"/> <img src="https://github.com/lizkalina/smart-cities/blob/master/plots/streetscore.jpg" width="425"/> 
