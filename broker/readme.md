
# Broker Design Pattern

The Broker Design Pattern is a messaging pattern that decouples communication between components or services in a distributed system by introducing an intermediary called a message broker. The message broker acts as an intermediary between senders and receivers of messages, allowing them to communicate without needing to know each other's identity.

The Broker Design Pattern is commonly used in large-scale systems where there are multiple services that need to communicate with each other. The message broker acts as a central hub that routes messages between services, ensuring that messages are delivered reliably and efficiently.

## How it works

In the Broker Design Pattern, messages are sent to a message broker, which then routes the messages to the appropriate destination. The message broker acts as a middleman between the sender and the receiver, allowing them to communicate without needing to know each other's identity.
![image](https://user-images.githubusercontent.com/43367262/236749516-24bfe50a-f2c0-43cd-b98e-08b0e1ad50cc.png)

The sender sends a message to the message broker, which then stores the message in a queue. The receiver subscribes to the queue and receives the message when it is available.

## Benefits

The Broker Design Pattern provides several benefits, including:

1. **Decoupling**: Services can communicate with each other without needing to know each other's identity, allowing them to be decoupled and independently developed, tested, and deployed.

2. **Scalability**: The message broker acts as a central hub that can handle large amounts of traffic, making it easier to scale the system as traffic increases.

3. **Reliability**: The message broker ensures that messages are delivered reliably, even in the event of network failures or service outages.

4. **Flexibility**: The message broker can be configured to route messages based on different criteria, such as message content or sender identity.

## Message Brokers

There are several message brokers available that implement the Broker Design Pattern, including:

1. **RabbitMQ**: An open-source message broker that supports multiple messaging protocols, including AMQP, MQTT, and STOMP.

2. **Apache Kafka**: A distributed streaming platform that can handle large amounts of data and supports both publish-subscribe and point-to-point messaging.

3. **AWS SQS**: A fully managed message queue service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

## Demo
You can find a simple demo application with apache kafka. Follow below steps to run it.
1. **run zookeeper**: ./apache-zookeeper-3.8.1-bin/bin/zkServer.sh  --config ./apache-zookeeper-3.8.1-bin/conf start
2. **install Kafka in this directory and run it. Because of file size contsraint it not attched here**
2. **run kafka**: ./kafka_2.12-3.4.0/bin/kafka-server-start.sh  ./kafka_2.12-3.4.0/config/server.properties 
3. **Run Consumer**: node consumer.js
4. **run Producer**: node producer.js
5. **test it**: Write a message on producer console and validate the message is received on consumer console

## Conclusion

The Broker Design Pattern is an effective way to decouple communication between services in a distributed system. By introducing a message broker as an intermediary, services can communicate with each other without needing to know each other's identity. This approach provides several benefits, including improved scalability, reliability, and flexibility.

When choosing a message broker, consider factors such as performance, scalability, and protocol support. RabbitMQ, Apache Kafka, and AWS SQS are popular message brokers that can be used to implement the Broker Design Pattern in your applications.
