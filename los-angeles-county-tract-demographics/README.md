# Los Angeles County demographics

Detailed demographics and voter information in geographic formats (```shapefile``` and ```geojson```) for all 2,800 tracts in Los Angeles County. *This repo is a work in progress*. 

Questions? Email [matt.stiles@latimes.com](mailto:matt.stiles@latimes.com).

## Demographics table metadata

**FIELDNAME &darr;** | TYPE | DEFINITION
---------------- | ---------- | ----------
**OBJECTID** | OID | OBJECTID
**GEOID10** | String | GEOID1011
**CT10** | String | CT106
**LABEL** | String | LABEL7
**X\_Center** | Double | X_Center
**Y\_Center** | Double | Y_Center
**ID** | String | ID256
**sourceCountry** | String | sourceCountry256
**ORIG\_ID** | Integer | ORIG_ID
**aggregationMethod** | String | aggregationMethod256
**HasData** | Integer | HasData
**TOTPOP\_CY** | Double | 2017 Total Population
**POPDENS\_CY** | Double | 2017 Population Density
**TOTPOP10** | Double | 2010 Total Population
**POPDENS10** | Double | 2010 Population Density
**HISPPOP\_CY** | Double | 2017 Hispanic Population
**NHSPWHT\_CY** | Double | 2017 Non-Hispanic White Pop
**NHSPBLK\_CY** | Double | 2017 Non-Hispanic Black Pop
**NHSPAI\_CY** | Double | 2017 Non-Hispanic American Indian Pop
**NHSPASN\_CY** | Double | 2017 Non-Hispanic Asian Pop
**NHSPPI\_CY** | Double | 2017 Non-Hispanic Pacific Islander Pop
**NHSPOTH\_CY** | Double | 2017 Non-Hispanic Other Race Pop
**NHSPMLT\_CY** | Double | 2017 Non-Hispanic Multiple Race Pop
**MINORITYCY** | Double | 2017 Non-Hispanic Pop of 2+ Races
**DIVINDX\_CY** | Double | 2017 Diversity Index
**RACEBASECY** | Double | 2017 Population by Race Base
**MEDVAL\_CY** | Double | 2017 Median Home Value
**CIVLBFR\_CY** | Double | 2017 Civ Pop 16+/Labor Force
**EMP\_CY** | Double | 2017 Employed Civilian Pop 16+
**INDBASE\_CY** | Double | 2017 Emp 16+ by Industry Base
**UNEMP\_CY** | Double | 2017 Unemployed Population 16+
**UNEMPRT\_CY** | Double | 2017 Unemployment Rate
**NOHS\_CY** | Double | 2017 Education: < 9th Grade
**SOMEHS\_CY** | Double | 2017 Education: High School/No Diploma
**HSGRAD\_CY** | Double | 2017 Education: High School Diploma
**GED\_CY** | Double | 2017 Education: GED
**SMCOLL\_CY** | Double | 2017 Education: Some College/No Degree
**ASSCDEG\_CY** | Double | 2017 Education: Associate's Degree
**BACHDEG\_CY** | Double | 2017 Education: Bachelor's Degree
**GRADDEG\_CY** | Double | 2017 Education: Grad/Professional Degree
**EDUCBASECY** | Double | 2017 Educational Attainment Base
**TOTHU\_CY** | Double | 2017 Total Housing Units
**OWNER\_CY** | Double | 2017 Owner Occupied HUs
**RENTER\_CY** | Double | 2017 Renter Occupied HUs
**VACANT\_CY** | Double | 2017 Vacant Housing Units
**TOTHH\_CY** | Double | 2017 Total Households
**MEDHINC\_CY** | Double | 2017 Median Household Income
**Shape** | Geometry | Shape
**LT\_HS\_CY** | Double | LT_HS_CY
**PCT\_MINORITY\_POP\_WholeNum** | Double | 2017 Minority Population - pct. (whole num)
**HS\_OR\_LESS\_CY\_PCT** | Double | 2017 Education: High School or less (pct.)
**NHSPWHT\_CY\_PCT** | Double | NHSPWHT_CY_PCT
**Shape.STArea()** | Double | Shape.STArea()
**Shape.STLength()** | Double | Shape.STLength()

## Source

Los Angeles County GIS