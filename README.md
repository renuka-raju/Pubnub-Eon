# Pubnub-Eon
D3 powered pubnub eon spline chart that updates when it receives streaming data from a source.

Include following dependencies
<script src=https://cdn.pubnub.com/sdk/javascript/pubnub.4.0.11.min.js></script>
<script type="text/javascript" src="https://pubnub.github.io/eon/v/eon/1.0.0/eon.js"></script>
<link type="text/css" rel="stylesheet" href="https://pubnub.github.io/eon/v/eon/1.0.0/eon.css"/>

Streaming data is fetched from a freely available API - Alpha Vantage API 
Stock time series data -  returns the following daily time series data for equities in JSON format
-Date
-Daily open
-Daily close
-Daily high
-Daily low
-Daily volume

URI used - https://www.alphavantage.co/query?function=TIME_SERIES_DAILY&symbol=<insert_symbol>&apikey=<insert_authKey>
Optional query parameter - outputsize
By default, outputsize=compact. Strings compact and full are accepted with the following specifications: 
compact returns only the latest 100 data points
full returns the full-length time series of up to 20 years of historical data. 
The equity symbol is taken as input from the user.

Three Eon spline charts are generated
-Open and Close for 100 dates back from today
-High and low for 100 dates back from today
-Volume for 100 dates back from today
