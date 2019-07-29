# LACERA Board Travel Records

These data sets list hundreds of trips taken by board members under the [Los Angeles County Employees Retirement Association](https://www.lacera.com/home/index.html) education and travel policy — travel detailed in [this story](https://www.latimes.com/california/story/2019-07-28/la-me-pension-travel-costs-lacera) in the *Los Angeles Times*. 

The data were compiled from more than [1,300 pages of travels memos and expense vouchers](https://www.documentcloud.org/search/projectid:45052-LACERA) released by the association pursuant the California Public Records Act. 

The data show trips across the United States and oversees by members of the Boards of Investments and Retirement. The file `trips.csv` has details on 445 cases in nine fields.

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