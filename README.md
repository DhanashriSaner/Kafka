# Kafka

Kafka is a **Distributed** Message Streaming Platform that uses **Publish** and **Subscribe** mechanism to stream the records.<br>
Kafka was originally developed by **LinkedIn** and later denoted to apache foundation.<br>
Kafka is an**open-source.**


### What is Event Streaming?
Event streaming is the practice of capturing data in real-time from event sources like databases, sensors, mobile devices, cloud services, and software applications in the form of streams of events

### What can I use event streaming for?
1) To process payments and financial transactions in real-time, such as in stock exchanges, banks, and insurances.
2) To track and monitor cars, trucks, fleets, and shipments in real-time, such as in logistics and the automotive industry.
3) To continuously capture and analyze sensor data from IoT devices or other equipment, such as in factories and wind parks.
4) To collect and immediately react to customer interactions and orders, such as in retail, the hotel and travel industry, and mobile applications.
5) To monitor patients in hospital care and predict changes in condition to ensure timely treatment in emergencies.
6) To connect, store, and make available data produced by different divisions of a company.

### Apache Kafka is an event streaming platform. What does that mean?
Kafka combines three key capabilities so you can implement your use cases for event streaming end-to-end 
<br>
1) To **publish** (write) and **subscribe** to (read) streams of events, including continuous import/export of your data from other systems.
2) To **store** streams of events durably and reliably for as long as you want.
3) To **process** streams of events as they occur or retrospectively.<br>

### How does Kafka work in a nutshell?
Kafka is a distributed system consisting of **servers** and **clients** that communicate via a high-performance TCP network protocol. It can be deployed on bare-metal hardware, virtual machines, and containers in on-premise as well as cloud environments.<br><br>
**Servers:** Kafka is run as a cluster of one or more servers that can span multiple datacenters or cloud regions. Some of these servers form the storage layer, called the brokers. Other servers run Kafka Connect to continuously import and export data as event streams to integrate Kafka with your existing systems such as relational databases as well as other Kafka clusters.<br>
**Clients:** They allow you to write distributed applications and microservices that read, write, and process streams of events in parallel, at scale, and in a fault-tolerant manner even in the case of network problems or machine failures. 

# Main concepts and Terminology

## Event
An event records the fact that "something happened" in the world or in your business. It is also called record or message in the documentation. 
<br>
<br>
Here is an example of event:
<br>
**Event key:** "Alice"<br>
**Event value:** "Made a payment of $200 to Bob"<br>
**Event timestamp:** "Jun. 25, 2020 at 2:06 p.m."

## Topics
A stream of message belonging to a particular category is called a topic.<br>
It is similar to a table in database.<br>
Unique Identifier of a topic is **NAME**<br>
Events are organized and durably stored in topics.<br>
Very simplified, a topic is similar to a folder in a filesystem, and the events are the files in that folder.
<br><br>
![Topic_Kafka](https://user-images.githubusercontent.com/88526990/225186658-c0dcd571-9414-4fb4-a5ee-8e838729f7f1.jpg)

### Properties of Topics
**1) Partitions**
<br><br>
![Partitions_kafka](https://user-images.githubusercontent.com/88526990/225188062-e1e1bf0b-6d7b-4980-8403-c64ca407ae7c.jpg)
<br>
**fig.discription:** Here Topic **'MyTopic** is split into the three Partitions P0, P1, P2 respectively.
<br>
<br>
![Partitions_kafka_p0](https://user-images.githubusercontent.com/88526990/225223862-30b98f3c-f8e0-4b17-9e9c-e8cefd4184b2.jpg)<br>
**fig.discription:** Partition **P0** is transfer from topic 'MyTopic' into the **Brocker 1**<br>
<br>
<br>
![Partitions_kafka_p1](https://user-images.githubusercontent.com/88526990/225224668-b61a4a6c-1043-48e8-af12-fcf12430b57e.jpg)<br>
**fig.discription:** Partition **P1** is transfer from topic 'MyTopic' into the **Brocker 2**
<br>
<br>
![Partitions_kafka_p2](https://user-images.githubusercontent.com/88526990/225224751-2d7cf43b-cf71-41a5-93b8-8619c8a2f9f6.jpg)<br>
**fig.discription:** Partition **P2** is transfer from topic 'MyTopic' into the **Brocker 1**
<br>
The Partitions are distributed among the brokers using the **Round Robin** algorithm.
<br>
<br>

**2) Replications**
<br>
In case of Kafka, the replica means backup of partitions. Here the copy of partition from the topic is store inside the different brokers.<br>
Consider below given fig. <br>

![replica_kafka](https://user-images.githubusercontent.com/88526990/225344847-03b0c60b-ee1c-4958-944a-6bb611fccaf8.jpg)<br>
**fig.discription:** Partition = **3** and Replication Factor = **2**<br>
<br>
The partitions are replicated inside the brockers, as shown in below given fig.
<br><br>
![replication_factor_kafka](https://user-images.githubusercontent.com/88526990/225348535-b2c99e64-d8ed-42c1-8d72-8956ac33a986.jpg)<br>
**fig.discription:** Partitions **P0, P1, P2** are replicated inside the Brokers.

## Producers

Producers are the applications which write/publish data to the topics within a cluster using the Producing APIs.<br>
Producers can write data either on topic level(All the Partitions of that topic) or specific partitions of the topic.

## Consumers
Consumers are the applications which read/consume data from the topics within a cluster using the Consuming APIs.<br>
Consumers can read data either on topic level(All the Partitions of that topic) or specific partitions of the topic.<br>
Consumers are associated with exactly one **Consumer Group**.<br>
A Consumer Group is a group of related consumers that perform a task.

## Brokers
Brokers are simple software processes who maintain and manage the published messages.<br>
Brokers are also known as **Kafka Servers**.<br>
Brokers also manage the **Consumer-offsets** and are responsible for the delivery of messages to the right consumers.<br>
A set of brokers who are communicating with each other to perform the management and maintenance task are collectively known as **Kafka Cluster.**<br>
We can add more brokers in a ready running kafka cluster without any downtime, which ensures that the horizontal scalability is possible.

## Zookeeper
Zookeeper is used to **monitor Kafka Cluster** and co-ordinate with each broker.<br>
It is used for controller election within kafka cluster.<br>
A set of Zookeepers nodes working together to manage other distributed systems is known as Zookeeper Cluster or **"Zookeeper Ensemble".**<br>
Keeps all the metadata information related to kafka cluster in the form of a key-value-pair.<br>
Metadata includes<br>
1. Configuration Information.<br>
2. Health status of each broker.
<br>

![Kafka-Cluster-Architecture-1024x544](https://user-images.githubusercontent.com/88526990/225487146-f62174cc-1678-40c0-8b55-c4374af8cfe9.png)







 
