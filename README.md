# react_workshop

## pre-requisites (optional)

### install git-cli

### create a user accout on git-hub

### clone the repository: git clone https://github.com/skwalie/react_workshop.git

### install react  

## write the app
### 1/ ticker-selector
- implement a combo-box taking data from the REST api endpoint https://api.kraken.com/0/public/Ticker
```
documentation about this http request can be found at: 
https://docs.kraken.com/api/docs/rest-api/get-ticker-information

only the property name (AssetTickerInfo from the documentation) has to be taken into account
the other properties (a, b, c, v, p, t, l, h, o) are not important 
```
- display the selected ticker name (AssetTickerInfo) into a label below the combo-box

### 2/ ticker-chart
- take the selected ticker name and call the http request https://api.kraken.com/0/public/Trades?pair=[TICKER_NAME]&since=[UNIX_TIME_SECONDS]

```
where TICKER_NAME is the selected ticker name in ticker-selector
and UNIX_TIME_SECONDS is 60 minutes before the current UTC unix time (in seconds)

documentation about this http request can be found at: 
https://docs.kraken.com/api/docs/rest-api/get-recent-trades
(the price is the first element of each array)

example of url: https://api.kraken.com/0/public/Trades?pair=XXBTZUSD&since=1735595745
```

- take the price and the time from the response payload and draw a chart where X-axis is the time and Y-axis is the price 

## push your code to git-hub
- git add .
- git commit -m "YOUR_MESSAGE"
- git push

