- [simple-kafka-cluster-using-docker](#simple-kafka-cluster-using-docker)
  - [Prerequisite](#prerequisite)
  - [How to run kafka cluster](#how-to-run-kafka-cluster)
  - [Topic](#topic)
    - [Get list of available topics](#get-list-of-available-topics)
    - [Create topic](#create-topic)
    - [Describe topic](#describe-topic)
  - [Produce message](#produce-message)
  - [Consume message](#consume-message)
# simple-kafka-cluster-using-docker

Contains docker compose file for simple kafka cluster and simple commands to publish and consume kafka message

## Prerequisite

1. Docker installed
2. docker-compose installed
3. Kafka installed

## How to run kafka cluster

```bash
docker-compose up
```

## Topic

### Get list of available topics

```sh
kafka-topics --zookeeper <zookeeper host>:2181 --list
```

### Create topic

```sh
kafka-topics --create --zookeeper <zookeeper>:<port> --topic <topic name> --replication-factor <replication count> --partitions <partition count>
```

### Describe topic

```sh
kafka-topics --describe --zookeeper <zookeeper>:<port> --topic <topic name>
```

## Produce message

```sh
kafka-console-producer --broker-list <broker>:<port> --topic <topic name>
```

## Consume message

```sh
kafka-console-consumer --bootstrap-server <broker>:<port> --topic <topic name> --group <group name>
```
