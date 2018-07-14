## Project Wiki Link  
https://github.com/BaritoLog/wiki  

## Barito Log  
Barito Log is a log management system that is inspired by the concept of timber rafting. Logs are converted into "timber" and grouped up before they were sent to the Kafka message queue.  

## How does Barito Log works  
When an app is registered on the Barito Market, it creates a blueprint.json file that will help to set up the enviroment where the data logs will be handled at. The logs will be queued on Kafka before they were consumed to be stored in Elastic Search and visualised through Kibbana.

## Flowchart  


## Core Components of Barito Log
* Timber: 
A special format used by the data logs that is processed in the barito-flow.
