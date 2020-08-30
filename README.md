<!-- TOC -->autoauto- [simple-kafka-cluster-using-docker](#simple-kafka-cluster-using-docker)auto- [Prerequisite](#prerequisite)auto- [How to run kafka cluster](#how-to-run-kafka-cluster)auto- [Get list of available topics](#get-list-of-available-topics)auto- [Crete topic](#crete-topic)autoauto<!-- /TOC -->

# simple-kafka-cluster-using-docker

Contains docker compose file for simple kafka cluster and simple commands to publish and consume kafka message

# Prerequisite

1. Docker installed
2. docker-compose installed
3. Kafka installed

# How to run kafka cluster

```bash
docker-compose up
```

# Get list of available topics

```sh
kafka-topics --zookeeper <zookeeper host>:2181 --list
```

# Topic

## Create topic

```sh
kafka-topics --create --zookeeper <zookeeper>:<port> --topic <topic name> --replication-factor <replication count> --partitions <partition count>
```

## Describe topic

```sh
kafka-topics --describe --zookeeper <zookeeper>:<port> --topic <topic name>
```

# Produce message

```sh
kafka-console-producer --broker-list <broker>:<port> --topic <topic name>
```

# Consume message

```sh
kafka-console-consumer --bootstrap-server <broker>:<port> --topic <topic name> --group <group name>
```
