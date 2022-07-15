# Landfill_site_selection_gdal
Landfill site selection for Milos island using a host of parameters such as land-use, road network, conservation areas

Finding the most suitable location where a landfill can be located is a complex task which includes GIS analysis. It is often related to many parameters such as land-use, road network, conservation areas. The current study area is Milos island. 

In order to select the landfill area, 7 parameters were considered. These are:
* distance from coastline (further than 300 m),
* distance from crack regions whose potential is more than 400 units (further than 300 m),
* distance from conservation areas ("Natura" regions) (further than 200 m),
* the land use should not be forest or mixed forest,
* land fill should not be further from a buffer (300 m) of roads whose type is not residential.

Last but not least, there are also some limitations regarding the area of the proposed landfill. Its area should be larger than 1,000,000 m2; a  smaller area is not sufficient for the plants required.

**Methodology**

Firstly, study area was created via the coastline provided. The line was converted to a polygon. Secondly, buffers created for the criteria needed. Then, buffers were merged to find total excluded area. The next step was to run 'erase' command so that regions which are not suitable for landfill location can be eliminated. The last step was to run 'clip' command so that only areas whose distance from road network (whose type is not residential) is less than 100m can be selected. This decreased even further the suitable regions. 

