# Hypothetical Starbucks Location Closure In Riverside


**Goal:**
The goal of this project was to determine a hypothetical store closure in Riverside, California based on its service area, population within the serving area, and its demographics. This project was an assignment for the class GEOG 170 Advanced GIS.

## Methodology
OpenStreetMap data of the specified area (Left: -117.53, Right: -117.28, Top: 34.02, Bottom: 33.85) was downloaded via Overpass API. 
![Image of OSM specified area](/images/project-pages/starbucks/osm-screenshot.png)
The .osm file was loaded to ArcMap and converted into a network dataset. Then the Service Area and the Origin/Destination Matrix analyses were conducted with a mock starbucks closing store shapefile provided by the instructor. 

## Maps
[OD Matrix Map](/images/project-pages/starbucks/od-matrix.jpg)

[Total Service Area Map](/images/project-pages/starbucks/total-coverage.jpg)

[Coverage Area of Example Store](/images/project-pages/starbucks/example-store.jpg)

## Discussion
### Population and demographic characteristics

Store | Population | Median Household Income in the Past 12 Months | Median Age | Does service area overlap with other service areas? 
------------ | ------------- | ------------- | ------------- | -------------
5685 | 28768 | 61408 | 34.593333 | Yes
6616 | 27796 | 58182 |	33.464706 | Yes
11463 | 29577 | 104672 | 39.372727 | Yes

### Recommendation 
I recommend closing store 6616. First of all, it has the lowest population out of all stores in Riverside. Moreover, since Starbucks’ target customers are mostly high/mid-level income, it would be reasonable to close a store in the area with the lowest median household income. Starbucks’ target customers tend to be younger while ranging from 20-60. Therefore, the median ages of the service areas of stores 5685 and 11463 are appropriate indicators of the presence of Starbucks’ target customers. Lastly, overlapping with other service areas is also considered. considered. While 11463’s service area has the largest overlap, 104672’s high median income makes it viable to have more stores in the nearby areas to increase accessibility.
