# Kafka

Kafka is a **Distributed** Message Streaming Platform that uses **Publish** and **Subscribe** mechanism to stream the records.<br>
Kafka was originally developed by **LinkedIn** and later denoted to apache foundation.<br>
Kafka is **open-source.**


### Types of Data Pipeline
1) Batch Data Processing
2) Near Real Time(NRT)
3) Real Time Data Processing
<br>
<br>

![batch_VS_Real_time](https://user-images.githubusercontent.com/88526990/224967357-eec4fba0-bece-466f-9371-36ec98893ef5.jpg)

#### Real-time Data Processing Examples
1) Bank Transactions
2) Twitter Hashtags
3) Application for live cricket scores and aggregation
4) Real-time dashboards of stocks, share market analysis

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

