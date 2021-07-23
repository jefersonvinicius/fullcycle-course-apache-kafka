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

# Partition leadership
The partitions have a leadership, and the consumers always will read from leader. When the leader partition down, the Apache automatically assign the leader replica as leader.

# Producer: ensure delivery message

## Acknowledgments Types:
**Ack 0 -> None**: producer send message and don't have response (Fire and Forget). 
Offer low ensurement, but the processing is more quickly

**Ack 1 -> Leader**: producer send message and wait for leader response.  
Offer middle ensurement, but reduces processing speed

**Ack -1 -> ALL**: producer send message and wait it be replicated on followers, and then, leader send response.  
Offer high ensurement, but reduces significantly processing speed

# Producer Idempotent
When the producer is idempotent, it ensure the message don't will be duplicated in case of some failure

