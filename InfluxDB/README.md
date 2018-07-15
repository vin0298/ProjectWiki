## What is InfluxDB ?

InfluxDB is one of many kind of Time Series Database(TSDB). TSDB is simply a database that handles data that is associated with a timestamp. It handles many action that you would like to do with time series data such as app performance overtime monitoring, network traffic monitoring, real-time analytics, and etc.

InfluxDB offers many advantages such as downsampling, automatic data expiring and deleting, and also sql-like query language for interacting with data, and also it is built upon Go language with no external dependencies, and the best thing about this database is that we don’t have to define the scheme up-front so it is more flexible.


## Installation

-	Mac OS(using Homebrew)
```
brew install influxdb
```

## Getting Started

Launch the influxd database process by using these commands:
-	If you want it to run in background and restart at login:
```
brew services start influxdb
```
-	If you don’t want a background service:
```
influxd -config /usr/local/etc/influxdb.conf
```
Start the influx to get in to the influx system:
```
Influx
```
Or this command to see the time column in RFC3339 format
```
Influx -precision rfc3339
```
Create your first Database
	```
	CREATE DATABASE “your-db-name”

Use “your-db-name”
```
## Writing data to the Database
	“INSERT <measurement>,[<tag-key>=<tag-value>,…,<tag-key-N>=<tag-value-N>] [<field-key>=<field-value>,…,<field-key-N>=<field-value-N>] [timestamp]”

	Where:
-	Measurement will be the sql table and timestamp as the primary key.
-	Tags and fields key will be the column name where tags are indexed and fields are not.

Sources:
-	Click [here]( https://docs.influxdata.com/influxdb/v1.6/introduction/getting-started/) for further reading.
-	And [here]( https://github.com/influxdata/influxdb) for the source code or github-related

