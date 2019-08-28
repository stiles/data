# City of Los Angeles homeless buffer maps

This repo contains datasets and code used to examine the effects of [proposed homeless sleeping restriction zones](https://www.latimes.com/california/story/2019-08-22/homeless-sidewalk-sleeping-ban-restrictions-boise-case-shelter) around selected property types.

To perform the spatial analysis, the Times used the Python programming language and a popular open-source spatial library, GeoPandas, to plot parks, schools, day care centers and some special venues — and then to draw 500-foot buffers around them. The results were then clipped by neighborhood, and the percentage of buffered area for each location was calculated.

**The analysis shows that at least 40% the city would be excluded for sleeping under the proposed rules. After the buffers are applied, the city in effect decreases from 475 square miles to 196 square miles.**

The analysis is documented in a Jupyter Notebook [here](https://nbviewer.jupyter.org/github/stiles/data/blob/master/la-city-homeless-buffer-maps/la-homeless-buffers.ipynb). The results of the neighborhood-specific buffer area calculations are [here](https://github.com/stiles/data/blob/master/la-city-homeless-buffer-maps/buffered/hood-breakdown.csv). A **rough** draft of the restricted area map is [here](https://api.mapbox.com/styles/v1/latimes/cjzsnpky006e81cns4x2pnywm.html?fresh=true&title=true&access_token=pk.eyJ1IjoibGF0aW1lcyIsImEiOiJjajhvcXRraGUwNnlwMzNyczR3cTBsaWh1In0.0cPKLwe2A0ET4P5CtWSiLQ#11.12/34.0205/-118.3413).

## Targeted location types included:

The proposal isn't yet specific, so we made some assumptions about the types of locations to include. The data for these locations come from city and county GIS portals, and they've been clipped to the city's boundaries before the analysis. **We drew 500-foot buffers around these places:** 

* All public schools (polygons from the city)
* Private schools (polygons extracted from the countywide parcel file)
* Children’s day care centers (points from the county's DPSS file)
* City, county and state parks (polygons from the county's file) within city limits
* Special venues (polygons extracted manually from the county's parcel file)
  * Staples Center (AIN# 5138016913)
  * Los Angeles Veterans Memorial Coliseum (5037027937)
  * Hollywood Bowl (5549009903)
  * Dodger Stadium (5415018016/5415018015)
  * Universal Studios (2424043034/2424043021)
  * El Pueblo de Los Angeles Historical Monument (5408008900)
  * Hollywood Walk of Fame (Hollywood Blvd from La Brea to Gower)

## Places we could also include:

* Relate childcare points to parcels (perhaps just use points)
* Homeless shelters (must acquire list of recent locations)
* City bike and recreational paths
* Bridges and tunnels in school routes (must acquire)

## Data sources for locations

Both raw and processed data for this project are available in this repo. 

Some of these data sets — schools, for example — represent complete lists of properties. Others, such as those collected by Los Angeles County GIS officials for homeless shelters and child care centers, are compiled from official sources for private and government-related facilities, but they are not complete lists. 

* [L.A. County parcel boundaries](https://permitting.gis.lacounty.gov/permitting/rest/services/energovDev/ViewableDev/MapServer/8)
* [L.A. County land usage codes](http://egis3.lacounty.gov/dataportal/wp-content/uploads/2009/12/usecodes-chart.pdf)
* [LAUSD school boundaries](https://maps.lacity.org/lahub/rest/services/LAUSD_Schools/MapServer/2)
* [LA city/county parks](https://egis3.lacounty.gov/dataportal/2016/10/25/department-of-parks-and-recreation-county-parks-and-open-space/)
* [LA City homeless shelters](https://public.gis.lacounty.gov/public/rest/services/LACounty_Dynamic/LMS_Data_Public/MapServer/158)
* [LA City child care centers](https://public.gis.lacounty.gov/public/rest/services/LACounty_Dynamic/LMS_Data_Public/MapServer/149)
* [City of L.A. bikeways](http://geohub.lacity.org/datasets/230abc621b144dbc96cca83d65bd454d_0)

## Raw data location layers

* la_city_county_parks.geojson
* la_city_gis_childcare_clipped.geojson
* la_city_parks_1566703413127.geojson
* la_city_special_venues.geojson
* la_county_private_school_parcels.geojson
* la-county-neighborhoods-current.geojson
* lausd_schools_boundaries_1566703408821.geojson
* la_county_gis_homeless_shelters_1566703407847.geojson
* la_city_boundary.geojson
* la_city_bikeways.geojson

## Processed data location layers

* special_venues_3310.geojson
* private_schools_3310.geojson
* public_schools_3310.geojson
* parks_3310.geojson
* childcare_3310.geojson
* bikeways_3310.geojson
* homeless_3310.geojson
* city_3310.geojson

[Batch data conversion sketching](https://gist.github.com/stiles/1c4b46ef1ca5a8e9350b622aa8bc9110)

## Stories?

* Downtown limited
* Venice cut by 50%
* Koreatown cut by 50%
* Area in square miles: 
  * Before (475 sq. miles)
  * After (196 sq. miles)

## Maps: Orange regions would be restricted areas under the proposal.

### Downtown: 

![Downtown](https://raw.githubusercontent.com/stiles/data/master/la-city-homeless-buffer-maps/maps/downtown.png)

### Citywide: 

![Citywide](https://raw.githubusercontent.com/stiles/data/master/la-city-homeless-buffer-maps/maps/citywide.png)

### Skid Row: 

![Downtown](https://raw.githubusercontent.com/stiles/data/master/la-city-homeless-buffer-maps/maps/skid-row.png)

### Venice: 

![Downtown](https://raw.githubusercontent.com/stiles/data/master/la-city-homeless-buffer-maps/maps/venice.png)
