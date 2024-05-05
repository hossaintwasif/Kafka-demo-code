Command to start Kafka
1. Start zooeper first :  ./bin/zookeeper-server-start.sh ./config/zookeeper.properties 
2. Start Kafka :  ./bin/kafka-server-start.sh ./config/server.properties 
3. Create a topc to store data : $ bin/kafka-topics.sh --create --topic quickstart-events --bootstrap-server localhost:9092
4.  WRITE SOME EVENTS INTO THE TOPIC :$ bin/kafka-console-producer.sh --topic quickstart-events --bootstrap-server localhost:9092
                                        > This is my first event
                                        > This is my second event

5.  READ THE EVENTS : $ bin/kafka-console-consumer.sh --topic quickstart-events --from-beginning --bootstrap-server localhost:9092
                      This is my first event
                      This is my second event

Reference : https://kafka.apache.org/quickstart
