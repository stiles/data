# #deletefacebook Twitter Dump

This dataset lists more than 100,000 tweets featuring the [#deletefacebook](https://twitter.com/search?q=%23deletefacebook&src=typd) hashtag.   

The data were scraped from Twitter using the [tweep](https://github.com/haccer/tweep) Python library. They range from midnight (UTC) Feb. 28 to 12:07 a.m. (UTC) March 24. 

The dataset has 108,608 tweets and nine fields. 

Field | Description
------------ | ------------- 
**id** | Twitter ID (i.e. *https://twitter.com/{{ user }}/status/{{ id }}*)
**date** | Date of tweet
**time** | Time of tweet
**timezone** | UTC
**user** | Username
**text** | Tweet text
**replies** | Number of replies
**retweets** | Number of retweets
**likes** | Number of likes
**hashtags** | List of hashtags used in tweet