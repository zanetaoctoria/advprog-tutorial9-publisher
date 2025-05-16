**Reflection Module 9 - Publisher**

a. **How much data will your publisher program send to the message broker in one run?**
The publisher program will send 5 pieces of data to the message broker in a single execution.

b. **The URL "amqp\://guest\:guest\@localhost:5672" is the same as in the subscriber program. What does it mean?**
The URL `amqp://guest:guest@localhost:5672` used in both the publisher and subscriber programs indicates that they are connected to the same RabbitMQ server running on the local machine. Here, `guest:guest` is the default username and password for authentication, `localhost` means the broker is hosted on the same computer, and `5672` is RabbitMQ’s default port. Since both programs use the same URL, the publisher can send messages and the subscriber can receive messages from the same queue through this shared broker.

### Running RabbitMQ
![Running RabbitMQ as message broker](image/RunningRabbitMQ.png)

### Sending and Processing Event
![Sending and processing event](image/SendingAndProcessingEvent.png)
When the subscriber is connected to RabbitMQ and the publisher sends data, the subscriber will receive the data sent by the publisher.

### Monitoring Chart Based on Publisher
![Monitoring chart based on publisher](image/MonitoringChartBasedOnPublisher.png)
The purple graph on the message rate represents the Consumer ACK (acknowledgement), which is the confirmation from the subscriber to the message broker that the message has been successfully received and processed.