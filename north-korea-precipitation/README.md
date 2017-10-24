# Precipitation in North Korea

These data includes historic precipitation totals for several locations around North Korea. The data were scraped from Weather Underground's monthly history pages listing weather conditions at a dozen monitoring stations across the country. The data include more than 10,000 monthly observations from January 2005 to October 2017.

The locations of each weather station are included in the table below, with links to the monthly reports from October 2017. Changing the URL structure (the year or month or station ID) will return different records, depending on the date and location.

The stations were geocoded using common tools, such as Google Maps. North Korean geography can be tricky, however, so please [let me know](mailto:mattstiles@gmail.com) if you spot any errors. The location spellings were pulled directly from Weather Underground and may differ from more common (or prefered) romanized versions of North Korean names.

Station/URL | Latitude | Longitude | Province | Location Name | Agricultural Area
------------ | ------------- | ------------- | ------------- | ------------- | -------------
[47052](https://www.wunderground.com/history/wmo/47052/2017/10/01/MonthlyHistory.html) | 38.8400001 | 126.91999817 | Kangwon | Ch'ongyong | n
[47055](https://www.wunderground.com/history/wmo/47055/2017/10/01/MonthlyHistory.html) | 39.377778 | 127.380278 | Kangwon | Ach'igon-ni | n
[47061](https://www.wunderground.com/history/wmo/47061/2017/10/01/MonthlyHistory.html) | 38.890556 | 127.942778 | Kangwon | Agal-li | n
[47075](https://www.wunderground.com/history/wmo/47075/2017/10/01/MonthlyHistory.html) | 38.38000107 | 127.51999664 | Kangwon | Ach'im-ni | n
[47041](https://www.wunderground.com/history/wmo/47041/2017/10/01/MonthlyHistory.html) | 39.95000076 | 126.9199981 | South Pyongyan | Ch'anghyol-li | y
[47058](https://www.wunderground.com/history/wmo/47058/2017/10/01/MonthlyHistory.html) | 39.23 | 126.09 | South Pyongyan | Am-dong | y
[47060](https://www.wunderground.com/history/wmo/47060/2017/10/01/MonthlyHistory.html) | 38.68999863 | 125.47000122 | South Hwanghae | Chunggi-ri | y
[47065](https://www.wunderground.com/history/wmo/47065/2017/10/01/MonthlyHistory.html) | 38.464 | 125.568 | South Hwanghae | Chunggo | y
[47067](https://www.wunderground.com/history/wmo/47067/2017/10/01/MonthlyHistory.html) | 38.95917 | 125.75139 | Pyongyang | Han-ch'on | y
[47068](https://www.wunderground.com/history/wmo/47068/2017/10/01/MonthlyHistory.html) | 38.240833 | 125.298889 | South Hwanghae | Chunggisan | y
[47050](https://www.wunderground.com/history/wmo/47050/2017/10/01/MonthlyHistory.html) | 39.525 | 125.198889 | North Pyongan | Aedo-nodongjagu | y
[47070](https://www.wunderground.com/history/wmo/47070/2017/10/01/MonthlyHistory.html) | 38.065833 | 126.374167 | South Hwanghae | Hadongjin | y

The locations are mapped [here](https://fusiontables.google.com/embedviz?q=select+col1+from+1j_xU66hgKuES1RzuHIspQwuWcC51GThR-RRJR-v1&viz=MAP&h=false&lat=38.87106450954273&lng=127.00479346093745&t=4&z=7&l=col1&y=2&tmplt=2&hml=TWO_COL_LAT_LNG).

The data have numerous fields combined from two relational tables into one flat file: 

**station:** Station ID listed by Weather Underground (in url)
**date_original:** The date pulled by the scraper
**precip_sum:** The monthly precipitation, either rain or snow, in millimeters
**year:** year extracted from date_original
**month:** month extracted from date_original
**lat:** latitude (some more precise than others)
**long:** longitude (some more precise than others)
**province:** province (or city, such as Pyongyang) as the weather station
**name:** name of station listed by Weather Underground
**agarea:** y=a province in the south or west, the main farming regions


