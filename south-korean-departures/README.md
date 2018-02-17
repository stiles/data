# South Korean Departures: 2003-2017


This dataset inlcudes 15 years of records on the number South Koreans who leave the country for travel. The data include monthly observations from various air and port departure locations, and have been [melted](https://www.statmethods.net/management/reshape.html) from the [original long format](http://kosis.kr/statHtml/statHtml.do?orgId=314&tblId=DT_TRFF_DEP_AGG_MONTH&conn_path=I2&language=e) released by the [Korean Statistical Information Service](http://kosis.kr/end). 

The dataset has more than 2,100 observations and four fields: 

Field | Description
------------ | ------------- 
**id** | Unique ID
**date** | Month
**type** | Departures by type (port or air)
**value** | Number of monthly departures

*Description of the "type" field:*

Field | Description
------------ | ------------- 
**Total** | Total departures (AirTotal + PortTotal)
**AirTotal** | Total departures by air
**AirIncheon** | Departures by air from Incheon
**AirGimhae** | Departures by air from Gimhae
**AirGimpo** | Departures by air from Gimpo
**AirJeju** | Departures by air from Jeju
**AirOthers** | Departures by air from other locations
**PortTotal** | Total departures by port
**PortBusan** | Departures by port from Busan
**PortIncheon** | Departures by port from Incheon
**PortJeju** | Departures by port from Jeju
**PortOthers** | Departures by port from other locations