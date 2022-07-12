# kafka-server
Simple Kafka server with Sasl Plain mechanism

#Steps to follow
Create a kafka user on your linux machine

Download the source from https://dlcdn.apache.org/kafka/3.2.0/kafka_2.13-3.2.0.tgz

unzip it
tar -xzf kafka_2.13-3.2.0.tgz
rename the new folder kafka_2.13-3.2.0 to kafka


Download this repo 
git clone https://github.com/zeb0x01/kafka-server/
then exchange the bin and config folders in kafka with the repo folders

run commands
To start a the zookeeper server
1. bin/zookeeper-server-start.sh [-daemon (if want to run in background)] config/zookeeper.properties

On another terminal 
To start the kafka server
2. bin/kafka-server-start.sh [-daemon (if want to run in background)] config/server.properties

To check if the servers are configured properly and messages can be transfered producer -> consumer
1. bin/kafka-console-consumer.sh --topic test-topic --from-beginning --consumer.config=config/consumer.properties --bootstrap-server=localhost:9092
2. bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test-topic --producer.config=config/producer.properties

