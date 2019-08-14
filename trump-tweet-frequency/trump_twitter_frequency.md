## How often does President Trump tweet each day?


```python
import altair as alt
import pandas as pd
import psycopg2 as pg
import matplotlib as mpl
import numpy as np
import json
import altair_latimes as lat
alt.renderers.enable('notebook')
alt.themes.register('latimes', lat.theme)
alt.themes.enable('latimes')
```




    ThemeRegistry.enable('latimes')



### Local url for @realDonaldTrump scraped data: 2012 - Aug. 2019


```python
url = '/Users/mhustiles/Desktop/github/data/trump-tweet-frequency/trump_archive.json'
```

### Local url for @realDonaldTrump data, update for 8/13/19


```python
urladd = '/Users/mhustiles/Desktop/github/data/trump-tweet-frequency/trump_update.json'
```

### Read data, concatenate, remove duplicate tweets from update


```python
trumptweets = pd.read_json(url, orient='columns', lines=True)
trumptweetsnu = pd.read_json(urladd, orient='columns', lines=True)
trumpall = pd.concat([trumptweets, trumptweetsnu]).drop_duplicates('id').sort_values(['created_at'], ascending=False)
```

### Clean up data types in scraped data


```python
trumpall['retweet'] = trumpall['retweet'].astype(str)
trumpall['video'] = trumpall['video'].astype(str)
trumpall['user_id'] = trumpall['user_id'].astype(str)
trumpall['user_id'] = trumpall['user_id'].astype(str)
trumpall['id'] = trumpall['id'].astype(str)
trumpall['conversation_id'] = trumpall['conversation_id'].astype(str)
```

### Add columns parsing dates to dataframe


```python
trumpall['year'] = trumpall['date'].dt.year
trumpall['month'] = trumpall['date'].dt.month
trumpall['day'] = trumpall['date'].dt.day
```

### Get GMT time


```python
trumpall['hour_gmt'] = trumpall['created_at'].dt.hour
```

### Clean them up


```python
trumpall['year'] = trumpall['year'].astype(str)
trumpall['month'] = trumpall['month'].astype(str)
trumpall['day'] = trumpall['day'].astype(str)
trumpall['hour_gmt'] = trumpall['hour_gmt'].astype(str)
```

### What did he average each day in retweets, likes and replies


```python
trump_engagements_day = trumpall.groupby(['date']).mean().round(0).reset_index()
```

### Limit data to when Trump took office


```python
trumpall_prez = trumpall[trumpall.date >= '2017-01-20']
```

### Count daily tweets, create dataframe with results


```python
trump_tweets_day = trumpall_prez.groupby(['date']).size()
trump_tweets_day_prez_df = pd.DataFrame({'date': trump_tweets_day.index, 'count': trump_tweets_day.values})
```

### Sort table to see top days


```python
trump_freq_prez = trump_tweets_day_prez_df.sort_values(['count'], ascending=False)
```


```python
trump_freq_prez.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>date</th>
      <th>count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>889</th>
      <td>2019-07-11</td>
      <td>35</td>
    </tr>
    <tr>
      <th>902</th>
      <td>2019-07-24</td>
      <td>33</td>
    </tr>
    <tr>
      <th>890</th>
      <td>2019-07-12</td>
      <td>28</td>
    </tr>
    <tr>
      <th>882</th>
      <td>2019-07-04</td>
      <td>28</td>
    </tr>
    <tr>
      <th>874</th>
      <td>2019-06-26</td>
      <td>28</td>
    </tr>
    <tr>
      <th>922</th>
      <td>2019-08-13</td>
      <td>27</td>
    </tr>
    <tr>
      <th>916</th>
      <td>2019-08-07</td>
      <td>25</td>
    </tr>
    <tr>
      <th>825</th>
      <td>2019-05-08</td>
      <td>24</td>
    </tr>
    <tr>
      <th>905</th>
      <td>2019-07-27</td>
      <td>23</td>
    </tr>
    <tr>
      <th>887</th>
      <td>2019-07-09</td>
      <td>23</td>
    </tr>
  </tbody>
</table>
</div>



### Read all from today


```python
trump_tweets_today = trumpall[trumpall.date == '2019-08-13']
```

### Chart it!


```python
#bars

lines = alt.Chart(trump_freq_prez, title = '@realDonaldTrump tweet frequency since inauguration').mark_bar().encode(
    x = alt.X('date:T', axis = alt.Axis(title = '', format = ("%b %y"))),
    y = alt.Y('count:Q',
        scale=alt.Scale(domain=(0, 40)), axis = alt.Axis(tickCount=6, title = 'Daily tweet counts and mean')),
)

#rule showing mean

rule = alt.Chart(trump_freq_prez).mark_rule(color='red').encode(
    y='mean(count):Q'
)

#rule label -- would like to add "Average: " annotation
text = rule.mark_text(
    align='center',
    baseline='middle',
    dx=200,
    dy=10,
    fontWeight='bold',
).encode(
    text=alt.Text('mean(count):Q', format=".2"))

#go
( lines + rule + text ).properties(height=600,width=800)
```


    <vega.vegalite.VegaLite at 0x13128eba8>





    




![png](chart.png)



```python

```


```python

```
