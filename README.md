# kafka-connect-jdbc-example
kafka-connect-jdbc example project with kafka-connect-jdbc jar compiled

## Start Kafka and Zookeper (local node example)

bin/zookeeper-server-start.sh config/zookeeper.properties &

bin/kafka-server-start.sh config/server.properties &
## Start your connector

bin/connect-standalone.sg config/connect-standalone.properties myconnector.properties

## Enjoy your messages
bin/kafka-console-consumer.sh --new-consumer --bootstrap-server localhost:9092 --topic myconnector-queue --from-beginning
