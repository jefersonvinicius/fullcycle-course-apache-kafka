# Commands

## Create Topic
```
kafka-topics --create --topic=<topic-name> --bootstrap-server=localhost:9092 --partitions=<amount>
```

## List topics
```
kafka-topics --list  --bootstrap-server=localhost:9092 
```

## Describe topic
```
kafka-topics --bootstrap-server=localhost:9092 --topic=<topic-name> --describe
```

## Start topic consumer
```
kafka-console-consumer --bootstrap-server=localhost:9092 --topic=<topic-name>
Options:
    --from-beginning: Start read the messages from beginning
    --group=<groupname> : set a group to topic
``` 

## Start topic producer
```
kafka-console-producer --bootstrap-server=localhost:9092 --topic=<topic-name>
``` 

## Describe consumer groups
```
kafka-consumer-groups --bootstrap-server=localhost:9092 --group=x --describe
```