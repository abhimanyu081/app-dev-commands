
## Install Zookeeper

```
sudo apt-get install zookeeperd

```

```
telnet localhost 2181

```

```
netstat -nltu

```

# KAFKA

```
sudo chown -R kafka:nogroup /opt/kafka
sudo chown -R kafka:nogroup /var/lib/kafka
sudo /opt/kafka/bin/kafka-server-start.sh /opt/kafka/config/server.properties
sudo tar -xvzf kafka_2.11-2.0.0.tgz  --directory /opt/kafka --strip-components 1

```
## Create Topic

```
/opt/kafka/bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test

```
## list topics

```
/opt/kafka/bin/kafka-topics.sh --list --zookeeper localhost:2181

```
## Console producer
```
/opt/kafka/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test

```
## Console Consumer

```
/opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning

```
## Start Kafka Service
```
sudo systemctl start kafka.service
sudo systemctl enable kafka.service
sudo systemctl status kafka.service
sudo systemctl start kafka.service
```