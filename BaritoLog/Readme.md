## Project Wiki Link  
https://github.com/BaritoLog/wiki  

## Barito Log  
Barito Log is a log management system that is inspired by the concept of timber rafting. Logs are converted into "timber" and grouped up before they were sent to the Kafka message queue.  

## How does Barito Log works  
When an app is registered on the Barito Market, it creates a blueprint.json file that will help to set up the enviroment where the data logs will be handled at. The data logs will created by the cookbook that will set up the individual components. The logs will be queued on Kafka before they were consumed to be stored in Elastic Search and visualised through Kibbana. 

## Flowchart  
![12-barito-convert-logs-to-timber-in-behind](https://github.com/BaritoLog/wiki/blob/master/images/12-barito-convert-logs-to-timber-in-behind.svg)


## Core Components of Barito Log
* Timber: 
A special format used by the data logs that is processed in the barito-flow. It's in json.
