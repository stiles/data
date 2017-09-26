# South Korea Foreigner Population, by Geographic Areas: 2015

This data set contains population totals for registered foreigners living in South Korea inside two levels of geography — also known as [administrative divisions](https://en.wikipedia.org/wiki/Administrative_divisions_of_South_Korea). These include cities and provinces (Seoul and its surrounding Gyeonggi Province, for example) but also counties, cities and districts within them (Yongsan District in Seoul, for example, and Suwon City inside Gyeonggi). 

The data do not include submunicipal categories, such as neighborhoods or villages.

The [data set](http://kosis.kr/statHtml/statHtml.do?orgId=110&tblId=TX_11025_A001&language=en&conn_path=I3), courtesy the KOrean Statistical Information Service, or [KOSIS](http://kosis.kr/eng/), contains IDs to allow for joins with geographic or other data. I've also calculated a foreign rate for each geographic category.

Fields: 

**GEOID:** Main identification number, shorter for broader geography levels (Seoul = 11; Yongsan District = 11030. The ID together = 1111030)
**CityProvinceID:** ID for city or province
**CityProvince:** City or province name
**MunicipalityID:** ID for "municipality", which can mean district or county, depending on whether the main geographic division is a major city (Seoul) or a province (Gyeonggi)
**Municipality:** Municipality name
**TotalPopulation:** 2015 total population in each place
**ForeignPopulation:** 2015 total registered foreign population (the foreigners who have told the government they are here, including Chinese Koreans, migrant workers, foreign spouses, others foreigners like me, etc.)
**ForeignerRate:** Percentage of foreigners in each place


*Notes: 1. Seoul and some other large cities are autonomous from adjacent or surrounding provinces. 2. Sejong, a special self-governing city, is included as both a city/province and as a municipality. 3. **[South Korean geography](https://en.wikipedia.org/wiki/Administrative_divisions_of_South_Korea) is hard.***

