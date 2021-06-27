# Selecting A Campsite Location In East San Diego Using Raster Operations
**Goal:** The goal of this project was to locate possible campground sites in the Laguna and Cuyamaca Mountains in San Diego.

## Methodology
A terrain-based scoring index out of 10 was developed, wherein locations receiving higher scores are better suited (according to the specified criteria) to be used for development of campgrounds. The index is based on two criteria – the terrain elevation (out of 5 points) and the terrain slope (out of 5 points). The scores are computed based on the void-filled DEM from USGS Earth Explorer of the area.

Areas that receive an overall 8+ score that are also located within 2 miles from a major road are shown in the second map and considered as possible campground locations. 

## Maps
![San Diego Mountain Relief Map](/images/project-pages/raster-operations/San Diego Mountain Relief Map.jpg)

![Possible Campground Locations Map](/images/project-pages/raster-operations/Possible Campground Locations Map.jpg)

## Discussion
They are mostly above 5500 feet (a score of 4 or 5 in the terrain elevation category) and have a slope between 0 and 3 (a score of 4 or 5 in the terrain slope category). Small parts of the locations identified overlap with roads.
