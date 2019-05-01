# Los Angeles County demographics

Detailed demographics and voter/redistricting information in geographic formats (```shapefile``` and ```geojson```) for all 2,800 U.S. Census Bureau [tracts](https://en.wikipedia.org/wiki/Census_tract) in Los Angeles County. *This repo is a work in progress*. 

Questions? Email [matt.stiles@latimes.com](mailto:matt.stiles@latimes.com).

## Demographics table metadata

**FIELDNAME** | TYPE | DEFINITION
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

## Voters table metadata

**FIELDNAME** | TYPE | DEFINITION
---------------- | ---------- | ----------
**Shape** | Object | 
**RDU [Redistricting Unit]** | Int32 | Redistricting Unit
**RDU_NAME [RDU Name]** | String | RDU Name
**CITY [City]** | String | City
**COMM [Community]** | String | Community
**CITYCOMM [City and Community]** | String | City and Community
**DOJZ11 [Hispanic 18+ Citz]** | Double | Hispanic 18+ Citz
**DOJZ12 [Non-Hispanic White 18+ Citz]** | Double | Non-Hispanic White 18+ Citz
**DOJZ13 [Non-Hispanic AfrAm AfrAm-White 18+ Citz]** | Double | Non-Hispanic AfrAm AfrAm-White 18+ Citz
**DOJZ14 [Non-Hispanic Asian Asian-White 18+ Citz]** | Double | Non-Hispanic Asian Asian-White 18+ Citz
**DOJZ15 [Non-Hispanic AmInd AmInd-White 18+ Citz]** | Double | Non-Hispanic AmInd AmInd-White 18+ Citz
**DOJZ16 [Non-Hispanic PacIsd PacIsd-White 18+ Citz]** | Double | Non-Hispanic PacIsd PacIsd-White 18+ Citz
**DOJZ17 [Non-Hispanic Other Other-White 18+ Citz]** | Double | Non-Hispanic Other Other-White 18+ Citz
**DOJZ18 [Non-Hispanic Multi-Race 18+ Citz]** | Double | Non-Hispanic Multi-Race 18+ Citz
**DOJZ19 [Total Voting 18+ Citizen]** | Double | Total Voting 18+ Citizen
**M18P2 [Male Voting Age]** | Double | Male Voting Age
**F18P2 [Female Voting Age]** | Double | Female Voting Age
**MVACTZ2 [Male Voting Age Citizens]** | Double | Male Voting Age Citizens
**FVACTZ2 [Female Voting Age Citizens]** | Double | Female Voting Age Citizens
**RENTERS [Renteres]** | Double | RENTERS
**OWNERS [Owners]** | Double | OWNERS
**HOME1 [$0-200,000]** | Double | $0-200,000
**HOME2 [$200,000-399,000]** | Double | $200,000-399,000
**HOME3 [$400,000-749,000]** | Double | $400,000-749,000
**HOME4 [$750,000+]** | Double | $750,000+
**HINC1 [$0-$25,000]** | Double | $0-$25,000
**HINC2 [$25,000-49,999]** | Double | $25,000-49,999
**HINC3 [$50,000-100,000]** | Double | $50,000-100,000
**HINC4 [$100,000+]** | Double | $100,000+
**NSN [Not Classified Surname Registration]** | Double | Not Classified Surname Registration
**SSN [Spanish Surname Registration]** | Double | Spanish Surname Registration
**ASN [Asian Surname Registration (Total of Asian Nationalties)]** | Double | Asian Surname Registration (Total of Asian Nationalties)
**CSN [Chinese Surname Registration]** | Double | Chinese Surname Registration
**FSN [Filipino Surname Registration]** | Double | Filipino Surname Registration
**ISN [Indian Surname Registration]** | Double | Indian Surname Registration
**JSN [Japanese Surname Registration]** | Double | Japanese Surname Registration
**KSN [Korean Surname Registration]** | Double | Korean Surname Registration
**VSN [Vietnamese Surname Registration]** | Double | Vietnamese Surname Registration
**Male [Male Registration]** | Double | Male Registration
**Female [Female Registration]** | Double | Female Registration
**Unknown [Gender Unknown Registration]** | Double | Gender Unknown Registration
**DEM [Democratic Registration]** | Double | Democratic Registration
**REP [Republican Registration]** | Double | Republican Registration
**DS [Decline to State Registration]** | Double | Decline to State Registration
**AI [American Independent Registration]** | Double | American Independent Registration
**PF [Peace and Freedom Registration]** | Double | Peace and Freedom Registration
**GRN [Green Registration]** | Double | Green Registration
**LIB [Libertarian Registration]** | Double | Libertarian Registration
**OTH [Other Party Registration]** | Double | Other Party Registration
**age34 [Age 18 to 34 Registration]** | Double | Age 18 to 34 Registration
**age49 [Age 35 to 49 Registration]** | Double | Age 35 to 49 Registration
**age64 [Age 50 to 64 Registration]** | Double | Age 50 to 64 Registration
**age65 [Age 65 or older Registration]** | Double | Age 65 or older Registration
**DOJV1 [Total]** | Double | Total
**DOJV2 [Hispanic]** | Double | Hispanic
**DOJV3 [NH White]** | Double | NH White
**DOJV4 [NH White]** | Double | NH White
**DOJV5 [NH Asian Asian-White]** | Double | NH Asian Asian-White
**DOJV6 [NH AmInd AmInd-White]** | Double | NH AmInd AmInd-White
**DOJV7 [NH PacIsd PacIsd-White]** | Double | NH PacIsd PacIsd-White
**DOJV8 [NH Other Other-White]** | Double | NH Other Other-White
**DOJV9 [NH Multi-Race]** | Double | NH Multi-Race
**DOJV10 [Total 18+]** | Double | Total 18+
**DOJV11 [Hispanic 18+]** | Double | Hispanic 18+
**DOJV12 [NH White 18+]** | Double | NH White 18+
**DOJV13 [NH AfrAm AfrAm-White 18+]** | Double | NH AfrAm AfrAm-White 18+
**DOJV14 [NH Asian Asian-White 18+]** | Double | NH Asian Asian-White 18+
**DOJV15 [NH AmInd AmInd-White 18+]** | Double | NH AmInd AmInd-White 18+
**DOJV16 [NH PacIsd PacIsd-White 18+]** | Double | NH PacIsd PacIsd-White 18+
**DOJV17 [NH Other Other-White 18+]** | Double | NH Other Other-White 18+
**DOJV18 [NH Multi-Race 18+]** | Double | NH Multi-Race 18+
**INCT [Inclusive Total]** | Double | Inclusive Total
**INCH [Inclusive Hispanic]** | Double | Inclusive Hispanic
**INC_NH_W [Inclusive Non-Hispanic White]** | Double | Inclusive Non-Hispanic White
**INCB [Inclusive African American]** | Double | Inclusive African American
**INCI [Inclusive American Indian]** | Double | Inclusive American Indian
**INCA [Inclusive Asian]** | Double | Inclusive Asian
**INCP [Inclusive Pacific Islander]** | Double | Inclusive Pacific Islander
**INC_NH_O [Inclusive Non-Hispanic Other]** | Double | Inclusive Non-Hispanic Other
**TRACT [Census Tract]** | Double | Census Tract
**FIPS [Federal FIPS Code]** | Double | Federal FIPS Code
**SUP [2001 Supervisorial District]** | Double | 2001 Supervisorial District
**SUP_2001 [2001 Supervisorial District]** | Double | 2001 Supervisorial District
**RENT_OWN_TOTAL [Renter and Owners (Total)]** | Double | Renter and Owners (Total)
**HOME_TOTAL [Total number of Houses]** | Double | Total number of Houses
**HOME_PREP [Housing Value Preponderance]** | String | Housing Value Preponderance
**HINC_TOTAL [Income Result Counts]** | Double | Income Result Counts
**HINC_PREP [Income Preponderance]** | String | Income Preponderance
**EDUC [% No High School Diploma]** | Double | % No High School Diploma
**pov100 [% Below Povery Level]** | Double | % Below Povery Level
**LANG_NO_ENGLISH [% Not Fluent in English]** | Double | % Not Fluent in English
**LANG_ARABIC [% Arabic Primary Language]** | Double | % Arabic Primary Language
**LANG_ARMENIAN [% Armenian Primary Language]** | Double | % Armenian Primary Language
**LANG_CHINESE [% Chinese Primary Language]** | Double | % Chinese Primary Language
**LANG_CAMBOD [% Cambodian Primary Language]** | Double | % Cambodian Primary Language
**LANG_ENGLISH [% English Primary Language]** | Double | % English Primary Language
**LANG_FARSI [% Farsi Primary Language]** | Double | % Farsi Primary Language
**LANG_KOREAN [% Korean Primary Language]** | Double | % Korean Primary Language
**LANG_RUSSIAN [% Russian Primary Language]** | Double | % Russian Primary Language
**LANG_SPANISH [% Spanish Primary Language]** | Double | % Spanish Primary Language
**LANG_TAGOLOG [% Tagolog Primary Language]** | Double | % Tagolog Primary Language
**LANG_VIET [% Vietnamese Primary Language]** | Double | % Vietnamese Primary Language
**LANG_OTHER [% Other Primary Language]** | Double | % Other Primary Language
**Area_Sqmi** | Double | 
**OBJECTID** | Int32 | 
**REG_TOTAL [Total Voter Registration]** | Double | Total Voter Registration
**Shape.STArea()** | Double | 
**Shape.STLength()** | Double. | 

## Sources

Compiled and released by Los Angeles County GIS: [Demographics (via Esri demographics)](http://public.gis.lacounty.gov/arcgis/rest/services/Demographics/Predominance/MapServer/13) | [Voters (via 2010 Census)](http://public.gis.lacounty.gov/arcgis/rest/services/LACounty_Dynamic/Redistricting_Data_2011/MapServer)