---
layout: post
title: Getting Started Working with Geographic Data
---

Making use of geographic data has always been intimidating to me, mostly because I never took the time to learn GIS programming. The [Geopandas](http://geopandas.org/#description) library makes working with geospatial data fairly straightforward in Pandas. To get started, we'll be opening a shapefile from the [US Census Bureau's Tiger/Line repository](https://www.census.gov/geo/maps-data/data/tiger-line.html):

```
import geopandas as gpd

fp = "/home/geo/Data/DAMSELFISH_distributions.shp"

# Read file using gpd.read_file()
data = gpd.read_file(fp)
```

