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

## Main concepts and Terminology
An **event** records the fact that "something happened" in the world or in your business. It is also called record or message in the documentation. 
<br>
Here's an example event:
<br>
Event key: "Alice"<br>
Event value: "Made a payment of $200 to Bob"<br>
Event timestamp: "Jun. 25, 2020 at 2:06 p.m."
<br><br>
**Producers** are those client applications that publish (write) events to Kafka.<br>
**consumers** are those that subscribe to (read and process) events.
<br><br>
**Topics**<br>
A stream of message belonging to a particular category is called a topic.<br>
It is similar to a table in database.<br>
Unique Identifier of a topic is **NAME**<br>
Events are organized and durably stored in topics.<br>
Very simplified, a topic is similar to a folder in a filesystem, and the events are the files in that folder.
<br><br>
![Topic_Kafka](https://user-images.githubusercontent.com/88526990/225186658-c0dcd571-9414-4fb4-a5ee-8e838729f7f1.jpg)

## Properties of Topics
**1) Partitions**<br>
Topics are split in Partitions. Then the Partitions are distributed among the brokers using the Round Robin algorithm.
<br><br>
![Partitions_kafka](https://user-images.githubusercontent.com/88526990/225188062-e1e1bf0b-6d7b-4980-8403-c64ca407ae7c.jpg)
<br>
**fig.discription** Here Topics are splits into the Partitions P0, P1, P2

2) Replications

### Kafka Architecture
Kafka architecture consists of a **storage layer** and a **compute layer**. 
<br>
The storage layer is designed to store data efficiently.
The compute layer consists of four core components -
<br>
1) Producer
2) Consumer
3) Streams
4) Connector APIs

## Kafka Components

#### 1) Cluster
Combination of commodity hardwares or cluster is a group of servers.

#### 2) Brocker
A Broker is a Kafka server that runs in a Kafka Cluster.<br>
Kafka Brokers form a cluster<br>
It is data storage part.

#### 3) Topic
A space name given within kafka.
It is data storage part.


2) Topic
3) Partitions
4) Replicas
5) Offsets
6) Commits
7) Consumer groups
8) Parallelism 
9) Back pressure

