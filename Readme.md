# What is Apache Kafka?
> Apache Kafka is an open-source distributed event streaming platform used by thousands of companies for high-performance data pipelines, streaming analytics, data integration, and mission-critical applications.

https://kafka.apache.org/

# Apache Kafka Features
- High throughput
- High Availabilty
- Low latency
- Scability
- Storage
- Can be used for many languages

# Topics
Topics are segmented channels of information where stored information from producers and to make available for consumers read it.

![](./images/topics.png)

# Partitions
Partitions are ways the a topic to spread yours message in differents machines. Ensuring more resilience.


# Ensuring messages order
When the messages order is important, can be used the keys to unify the messages in one partition. That way, avoiding messages that need processed in determinate order fall in different partition

# Replicator factor
Indicates the amount of partitions will have in each broker. In case of a broker down, the messages will be safe in anothers replicas