# Kafka Tests

## Santa Clause Scenario
1. Child 23 publishes its wish to Santa Claus' MQTT topic /wishes with payload:
    ```
    {
        child: 23,
        present: 'bobbycar'
    }
    ```
2. MQTT message is forwarded to Kafka: https://howtoprogram.xyz/2016/07/30/apache-kafka-connect-mqtt-source-tutorial/
3. .....

## Docker
Run docker-compose:
`docker-compose up -d`

## Create Kafka Topis
1. Log into Kafka docker:
`docker exec -it kafkatest_kafka_1 bash`

2. Create topic:
`kafka-topics.sh --zookeeper zookeeper:2181 --create --topic wishes --partitions 8 --replication-factor 1`

3. List topics:
`kafka-topics.sh --zookeeper zookeeper:2181 --list`

## MQTT 
Client: http://www.jensd.de/apps/mqttfx/1.7.0/