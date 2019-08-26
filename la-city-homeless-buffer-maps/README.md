# City of Los Angeles homeless buffer maps

This repo contains datasets used to examine the effects of [proposed homeless sleeping restriction zones](https://www.latimes.com/california/story/2019-08-22/homeless-sidewalk-sleeping-ban-restrictions-boise-case-shelter) 500 feet around selected property types. The data folder contains original layers, layers with 500ft buffers and a final dissolved layer showing how the restrictions would limit large swaths of the city to the homeless.  

**They would essentially cut the city in half for the homeless population. After the buffers are applied, the city decreases from 478 square miles to 229 square miles.** 

## Targeted location types

* Public schools
* Children’s day care centers
* * Relate to parcels
* Public parks

## Potentially other targeted location types

* Homeless shelters (established recently)?
* Bicycle lanes?
* Large venues such as Staples Center? 
* Bridges and tunnels in school routes?
* Private schools?
* Sidewalk vending ordinance? 

## Data sources for locations

Some of these data sets — schools, for example — represent complete lists of properties. Others, such as those collected by Los Angeles County GIS officials for homeless shelters and child care centers, are compiled from official sources for private and government-related facilities, but they are not complete lists. 

* [L.A. County parcel boundaries](https://permitting.gis.lacounty.gov/permitting/rest/services/energovDev/ViewableDev/MapServer/8)
* [L.A. County land usage codes](http://egis3.lacounty.gov/dataportal/wp-content/uploads/2009/12/usecodes-chart.pdf)
* [LAUSD school boundaries](https://maps.lacity.org/lahub/rest/services/LAUSD_Schools/MapServer/2)
* [LA City parks](https://maps.lacity.org/lahub/rest/services/Recreation_and_Parks_Department/MapServer/5)
* [LA City homeless shelters](https://public.gis.lacounty.gov/public/rest/services/LACounty_Dynamic/LMS_Data_Public/MapServer/158)
* [LA City child care centers](https://public.gis.lacounty.gov/public/rest/services/LACounty_Dynamic/LMS_Data_Public/MapServer/149)
* [City of L.A. bikeways](http://geohub.lacity.org/datasets/230abc621b144dbc96cca83d65bd454d_0)

## Converted location layers

* la_city_boundary_3310.geojson
* la_city_gis_bikeways_3310.geojson
* la_city_parcels_3310.geojson
* la_city_parks_3310.geojson
* la_city_parks_buffer_500ft.geojson
* la_city_parks_schools_childcare_homeless_buffer_dissolved_4326.geojson
* la_city_parks_schools_childcare_homeless_buffer_dissolved.geojson
* la_city_parks_schools_childcare_homeless_buffer.geojson
* la_county_gis_childcare_3310.geojson
* la_county_gis_childcare_buffer_500ft.geojson
* la_county_gis_homeless_shelters_3310.geojson
* la_county_homeless_shelters_buffer_500ft.geojson
* lausd_schools_boundaries_3310.geojson
* lausd_schools_buffer_500ft.geojson

## Methodology 

Located layers for selected location types from LA City and LA County GIS portals. Projected the layers to *California Albers*, `ESPG: 3310`. Created a 500ft buffer around each layer. Dissolved the layers into one large layer, called `la_city_parks_schools_childcare_homeless_buffer_dissolved.geojson`. Returned the larger buffer layer back to `EPSG: 4326` for web mapping. 

[Batch data conversion](https://gist.github.com/stiles/1c4b46ef1ca5a8e9350b622aa8bc9110)

## Stories?

* Downtown/Skid Row essentially gone
* Venice, too
* Bunker Hill lone place in downtown
* Area in square miles: 
  * Before (478 sq miles)
  * After (229 sq miles)

## Maps: Orange regions would be restricted areas under the proposal.

### Downtown: 

![Downtown](https://raw.githubusercontent.com/stiles/data/master/la-city-homeless-buffer-maps/maps/downtown_dissolved_buffer.png)

### Citywide: 

![Citywide](https://raw.githubusercontent.com/stiles/data/master/la-city-homeless-buffer-maps/maps/city_dissolved_buffer.png)
