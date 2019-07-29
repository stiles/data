# LACERA Board Travel Records

This dataset lists hundreds of trips taken by board members at the [Los Angeles County Employees Retirement Association](https://www.lacera.com/home/index.html). 

The data, obtained under the Califnornia Public Records Act, were used to report [this story](https://www.latimes.com/california/story/2019-07-28/la-me-pension-travel-costs-lacera) in the Los Angeles Times. 

They document trips across the United States and oversees by members of the Boards of Investments and Retirement. 

The dataset has details on 445 trips, which are detailed in nine fields. 

Field | Description
------------ | ------------- 
**attendee** | Board member name
**title** | Name event
**start** | Travel start date
**end** | Travel end date
**status** | Attended or cancelled
**location** | Event location
**fiscal** | Fiscal year
**overseas** | y/n
**region** | Abbreviated codes for regions (if overseas)

Also included in this repo are simple summary tables with [counts](https://github.com/stiles/data/blob/master/lacera-board-travel-expenses/places.csv) of locations attended `places.csv` and [spending totals](https://github.com/stiles/data/blob/master/lacera-board-travel-expenses/attendees.csv) by current and past board members `attendees.csv`. 

The data were compiled from more than [1,300 pages of travels memos and expense vouchers](https://www.documentcloud.org/search/projectid:45052-LACERA) released by the association under the California Public Records Act. 