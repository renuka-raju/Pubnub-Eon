# Pubnub-Eon
D3 powered pubnub eon spline chart that updates when it receives streaming data from a source.<br />

Include following dependencies<br />
<script src=https://cdn.pubnub.com/sdk/javascript/pubnub.4.0.11.min.js></script><br />
<script type="text/javascript" src="https://pubnub.github.io/eon/v/eon/1.0.0/eon.js"></script><br />
<link type="text/css" rel="stylesheet" href="https://pubnub.github.io/eon/v/eon/1.0.0/eon.css"/><br />

Streaming data is fetched from a freely available API - Alpha Vantage API <br />
Stock time series data -  returns the following daily time series data for equities in JSON format<br />
-Date<br />
-Daily open<br />
-Daily close<br />
-Daily high<br />
-Daily low<br />
-Daily volume<br />

URI used - https://www.alphavantage.co/query?function=TIME_SERIES_DAILY&symbol=<insert_symbol>&apikey=<insert_authKey><br />
Optional query parameter - outputsize<br />
By default, outputsize=compact. Strings compact and full are accepted with the following specifications: <br />
compact returns only the latest 100 data points<br />
full returns the full-length time series of up to 20 years of historical data. <br />
The equity symbol is taken as input from the user.<br />

Three Eon spline charts are generated<br />
-Open and Close for 100 dates back from today<br />
-High and low for 100 dates back from today<br />
-Volume for 100 dates back from today<br />
