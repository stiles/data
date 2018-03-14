# NICAR#18 Twitter Dump

This dataset lists more than 4,100 tweets featuring the [#NICAR18](https://twitter.com/search?q=%23NICAR18&src=typd) hashtag, which identified messages about IRE's annual [CAR Conference](https://ire.org/conferences/nicar18/).   

The data were scraped from Twitter using the [tweep](https://github.com/haccer/tweep) Python library. They range from Jan. 1 to March 14. 

The dataset has 7,700 tweets and nine fields. 

Field | Description
------------ | ------------- 
**id** | Twitter ID (i.e. *https://twitter.com/{{ user }}/status/{{ id }}*)
**date** | Date of tweet
**time** | Time of tweet
**timezone** | Timezone, which is UTC (you should adjust the times for Central during the conference itself, and remember that CST changed to CDT at 2 a.m. on Sunday, March 11)
**user** | Username
**text** | Tweet text
**replies** | Number of replies
**retweets** | Number of retweets
**likes** | Number of likes