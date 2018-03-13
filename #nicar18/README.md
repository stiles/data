# NICAR#18 Twitter Dump

This dataset lists more than 4,100 tweets featuring the [#NICAR18](https://twitter.com/search?q=%23NICAR18&src=typd) hashtag, which identified messages about IRE's annual [CAR Conference](https://ire.org/conferences/nicar18/).   

The data were scraped from Twitter using the [tweep](https://github.com/haccer/tweep) Python library. They range from Jan. 1 to March 12. 

The dataset has 4,712 tweets and nine fields. 

Field | Description
------------ | ------------- 
**id** | Twitter ID [https://twitter.com/stiles/status/<< ID HERE >>](https://twitter.com/stiles/status/972770526316900352)
**date** | Date of tweet
**time** | Time of tweet
**timezone** | Timezone, which is UTC (you might adjust the times for Central during the conference itself)
**user** | Username
**text** | Tweet text
**replies** | Number of replies
**retweets** | Number of retweets
**likes** | Number of likes