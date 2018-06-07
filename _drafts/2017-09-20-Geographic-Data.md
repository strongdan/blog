---
layout: post
title: Getting Started Working with Geographic Data
---

Making use of geographic data has always been intimidating to me, mostly because I never took the time to learn GIS programming. But by understanding some basic principles, it's fairly straightforward to work with geospatial data using Python. The data we'll be working with here will be in a shapefile format, which includes points, lines, polygons, and descriptive attributes to represent vector features. According to [Wikipedia](https://en.wikipedia.org/wiki/Shapefile), there are three essential files a shapefile needs:

* _.shp_ — shape format; the feature geometry itself
* _.shx_ — shape index format; a positional index of the feature geometry to allow seeking forwards and backwards quickly
* _.dbf_ — attribute format; columnar attributes for each shape, in dBase IV format


The [Geopandas](http://geopandas.org/#description) library makes working with geospatial data fairly straightforward in Pandas. To get started, we'll be opening a shapefile from the [US Census Bureau's Tiger/Line repository](https://www.census.gov/geo/maps-data/data/tiger-line.html):

```python
import geopandas as gpd
from zipfile import ZipFile

# specify shapefile URL
county_file_url = 'http://www2.census.gov/geo/tiger/GENZ2015/shp/cb_2015_us_county_500k.zip'

# open zip file from URL
zipfile = ZipFile(StringIO(urlopen(county_file_url).read()))

# Read file using geopandas
data = gpd.read_file(zi)

filenames = [y for y in sorted(zipfile.namelist()) for ending in ['dbf', 'prj', 'shp', 'shx'] if y.endswith(ending)] 
print(filenames)

dbf, prj, shp, shx = [StringIO(zipfile.read(filename)) for filename in filenames]

r = shapefile.Reader(shp=shp, shx=shx, dbf=dbf)
```

This code will 





