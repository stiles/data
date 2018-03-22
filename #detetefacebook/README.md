# #deletefacebook Twitter Dump

This dataset lists more than 59,000 tweets featuring the [#deletefacebook](https://twitter.com/search?q=%23deletefacebook&src=typd) hashtag.   

The data were scraped from Twitter using the [tweep](https://github.com/haccer/tweep) Python library. They range from Feb. 28 to March 21. 

The dataset has 59,213 tweets and nine fields. 

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