
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

From my investigation, I learned that there is a minimal correlation between how safe someone feels and number of trees. I originally aggregated tree count and safety metrics at the block level, but soon realized that introduced too much noise into the data. Instead, I chose to approach my analysis from the zip code level which smoothed out the noise 

![correlation](https://github.com/lizkalina/smart-cities/blob/master/plots/correlation.jpg)

<img src="https://github.com/lizkalina/smart-cities/blob/master/plots/tree_count.jpg" width="425"/> <img src="https://github.com/lizkalina/smart-cities/blob/master/plots/streetscore.jpg" width="425"/> 


> “Streets and their sidewalks-the main public places of a city-are its most vital organs.”
> <br> ― Jane Jacobs, The Death and Life of Great American Cities
