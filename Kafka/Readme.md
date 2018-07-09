## Kafka Wiki 
Read official documentation on Kafka [here](https://kafka.apache.org/intro)  
Watch a youtube playlist about Kafka [here](https://www.youtube.com/watch?v=kDx8hZhvCQ0&index=7&list=PLkz1SCf5iB4enAR00Z46JwY9GGkaS2NON)  

## What is Kafka?
Kafka is a distributed streaming platform

## Why Kafka  
Advantages against other message queue systems: 

Insert image

## Core Components of Kafka
1. **Producer**  
Send messages to the Kafka cluster  
2. **Kafka Cluster**  
Bunch of brokers running in group of computers  
3. **Stream Processors**  
Constant stream of messages  
4. **Consumers**  
Reads, process the data and/or push it back to the Kafka cluster  
5. **Connectors**  
Imports data from the database to Kafka, including the other way around  

## Core Concepts of Kafka
1. **What is a producer?**  
It is an application that sends messages to Kafka (not a recipient address) where messages are small to medium sized piece of data  
2. **Consumer**  
The consumer is an application that reads data from Kafka by requesting messages from Kafka. The max nuumber of consumers in a group is equal to the number of partitions of a topic. Kafka does not allow two consumers to work at the same partition
3. **Broker**  
The broker is the Kafka server where it acts as the dealer or "broker" between the producer and consumer. It deals the data from the
producer that the consumer requests. Every broker must know the zookeeper's address which is essential to create a cluster  
4. **Cluster**  
It is a group of computers sharing workloads when processing the data  
5. **Topic**  
It's a unique name for a Kafka stream; it is an ID given to a Kafka stream that the consumer can use to request that specific group
of data from the producer  
6. **Offset**  
It's a sequence number to a partition. It's immutable and arranged in order of arrival  

**How to locate a message?**  
* Find the topic name -> Look at the partition number -> Find the offset

## Fault Tolerance in Kafka
When creating a topic, we are required to provide the **replication factor**. The replication factor refers to the number of copies of the partition that is being processed that is present in the cluster. In the cluster, there will always be a **leader** and **followers**, the total number of followers is dependent on the number of followers. For instance, if the replication factor is 3, then there will be 1 leader and 2 followers. If a leader ran into a problem when processing the data, the next follower will become the new leader.

Use bin/kafka-topics.sh --zookeeper localhost:2181 --describe --topic topicName to see the partitions, leaders and etc.  
Isr = In-sync replicas

## Setting up Kafka with barito-flow locally
* Install go: brew install go
* 

## Setting up Kafka on virtual machine (DO NOT FOLLOW THIS)
* Install virtual box and vagrant 
* Vagrant up (will execute the Vagrant File)
* Vagrant ssh  
* cd to /etc/kafka  
* To start the zookeeper:  
  * sudo /etc/kafka/kafka_2.11-0.11.0.1/bin/zookeeper-server-start.sh /etc/kafka/config/zookeeper.properties  
* To start the server:  
  * sudo /etc/kafka/kafka_2.11-0.11.0.1/bin/kafka-server-start.sh /etc/kafka/config/server.properties  
  
## Samara - Kafka library

## Additional Info to Learn
(Apache Flink) [https://flink.apache.org/]







