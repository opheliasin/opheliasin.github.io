# An Investigation In Transportation, Pollution, And Income In LA

**Geographic scope of project**
The focus of this project will be the city of Los Angeles in California. This project excludes unincorporated areas or the Greater Los Angeles areas. A total of 1151 census tracts are included. 

**Topics of interest: LA’s Green New Deal**
The City of Los Angeles aims to reach ambitious urban sustainability goals. By 2035, the City of Los Angeles envisions 50% of its residents to rely on walking, biking, or taking public transit. 

**Purpose**
Using certain parameters, we shall attempt to understand the disparity of transit options, physical health, and the degree of traffic burden and pollution among LA residents living in different census tracts.

**Data sources** 
* LA City Geohub (Bike lanes, City of LA boundary )UCLA Geoportal (US major roads) 
* CalEnviroScreen 3.0 (Pollution burden)
* Los Angeles Metro Bikeshare (Bikeshare station locations)
* Los Angeles Metro (Rail lines and Rail stations)
* US Census Bureau
  * American Community 5-year survey (Median Income per household, Mean time to travel to work)
  * US Tiger/Lines (Census tracts)
  * Poverty Threshold 2018

## Web Maps 

[Metro (railway) network in the City of Los Angeles](https://www.arcgis.com/apps/MapJournal/index.html?appid=99b6f3d97b21430a889023a71889ccad)

[City of LA: Pollution Burden vs Median Household Income](https://arcg.is/15uquW)

[Mean Time to Travel and Public Transit Accessiblity](https://www.arcgis.com/apps/MapSeries/index.html?appid=e576a890a98b46d0a6e9ad81b3e863e1)

[Bikeshare stations, bikeways and Los Angeles](https://www.arcgis.com/apps/MapSeries/index.html?appid=b400a16ac0e442b49d629c1e8b598b52)


## Methodology 
* 9 maps were created in total for analysis and displayed in ArcGIS Online. However, before uploading zipped shapefiles to ArcGIS Online, multiple steps were taken to create and organize the data that was required in ArcMap. 
* Most of the data were large datasets, ranging from state to county level. It was necessary to use a City of Los Angeles shapefile downloaded from the City Geohub to geoprocess the larger datasets using clip or intersect. New shapefiles were then created. 
* A join was done between the census tract shapefiles from the US Census Bureau and selected variables from ACS 5-year estimates data profiles DP03 (Economic characteristics). Before conducting the table join, null values and ‘-‘ values are replaced by 0. 
* Dissolved buffer zones were created for both metro (railroad) stations and metro bikeshare stations. The metro (railroad) station buffer had a radius of ½ miles and the metro bikeshare stations had a radius of 1,000 feet. The radiuses were decided according to data published by the National Association of City Transportation Officials. In order to reduce the repetition of creating buffers for metro (railroad) stations, stations from different metro lines were merged into one file before conducting a buffer operation. 
* A selection by attribute operation was done to select census tracts that had a median income below the poverty threshold of 2018 ($25,701) in reference to data provided by the US Census Bureau. A new shapefile was created. 
* Intersect operations were used to evaluate the relationships between various datasets. The operation was done between (1) bikeshare stations and low-income census tracks, (2) railroad stations and low-income census tracts; (3) bikeshare station buffers and all census tracts, and (4) railroad station buffers and census tracts. Using the selected data, I was able to calculate the average mean time to travel among tracts within the buffer zones. 
* I also calculated the total length of bikelanes in the CIty of LA using the geometry tool. The outcome was then compared to the total distance of streets in LA. 
* An extra step was taken when categorizing census tracts that were narrowed down. In order to preserve consistency of the categorization between the original data and the subsets, categories for the subsets were adjusted manually.

## Conclusion
* Less than 10% of streets are paved with bikelanes. 
* Bikeshare stations are not exclusive to middle/high-income neighborhoods.
* A neighborhood’s accessibility to public transit does not lead to a rise in the predominant socio-economic class of its residents.
* On average, living next to a bikeshare station or a railroad station will not reduce your commuting time.

## Sources
https://plan.lamayor.org/targets/targets_plan.html  
https://nacto.org/wp-content/uploads/2015/09/NACTO_Walkable-Station-Spacing-Is-Key-For-Bike-Share_Sc.pdf
