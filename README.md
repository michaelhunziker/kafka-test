# Kafka Tests

## docker-compose
Run docker-compose:
`docker-compose up -d`

## Create Kafka Topis
1. Log into Kafka docker:
`docker exec -it kafkatest_kafka_1 bash`

2. Create topic:
`kafka-topics.sh --zookeeper zookeeper:2181 --create --topic patient_needs --partitions 8 --replication-factor 1`

3. List topics:
`kafka-topics.sh --zookeeper zookeeper:2181 --list`


## MQTT 
Client: http://www.jensd.de/apps/mqttfx/1.7.0/