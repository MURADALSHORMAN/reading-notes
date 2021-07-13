# What is Event-Driven Architecture (EDA)?
Most of the nodejs core modules like Http, fs, timers are built around event-driven architecture and we can, of course, use this architecture to our advantage in the code we write. and this concept of events in nodejs is very simple.
In nodejs, there are certain Objects called events emitters that emit named events as soon as something important happens in the app like a request hitting a server or a timer expiring, or a file finished to read. These events are picked up by and event listeners that we developers set up which will fire up callback functions that are attached to each listener. i.e, on one hand, we have event emitters, on the other hand, we have event listeners that will react by calling callbacks.
Let’s briefly look at an example. So when we want to create a server, we use the create server method
```
const server = http.createServer();

 server.on('request', (req, res) => {
  console.log('request receved');
  res.end('request receved');
 });
 ```
 
-  What’s the difference between a FIFO and a standard queue? 
-  FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers

- How can the server be assured a message was properly received? 
- we can use the socket.io’s acknowledgements.

- What classic design pattern is best represented by event driven programming? 
- Event-driven from end to end

- How do you test an event driven system?

    -  Ensure supporting topics exist
    -  Start the application under test (“application” here could mean Kafka Streams, Kafka connectors, Samza, etc.)
    - Send some input events
 
 
 


![](https://d2908q01vomqb2.cloudfront.net/1b6453892473a467d07372d45eb05abc2031647a/2017/11/20/introducing_sns_message_filtering_image_4.png)

### AWS SNS and SQS:
Amazon Simple Queue Service (SQS) and Amazon SNS are both messaging services within AWS, which provide different benefits for developers. Amazon SNS allows applications to send time-critical messages to multiple subscribers through a “push” mechanism, eliminating the need to periodically check or “poll” for updates.
### What is Amazon Simple Notification Service (Amazon SNS)?
 Amazon Simple Notification Service (Amazon SNS) is a web service that makes it easy to set up, operate, and send notifications from the cloud. It provides developers with a highly scalable, flexible, and cost-effective capability to publish messages from an application and immediately deliver them to subscribers or other applications. It is designed to make web-scale computing easier for developers. Amazon SNS follows the “publish-subscribe” (pub-sub) messaging paradigm, with notifications being delivered to clients using a “push” mechanism that eliminates the need to periodically check or “poll” for new information and updates. With simple APIs requiring minimal up-front development effort, no maintenance or management overhead and pay-as-you-go pricing, Amazon SNS gives developers an easy mechanism to incorporate a powerful notification system with their applications.
### What are the benefits of using Amazon SNS?
Instantaneous, push-based delivery (no polling)
Simple APIs and easy integration with applications
Flexible message delivery over multiple transport protocols
Inexpensive, pay-as-you-go model with no up-front costs
Web-based AWS Management Console offers the simplicity of a point-and-click interface



#  Preview 
- Which 3 things had you heard about previously and now have better clarity on?
Event Driven Programming, Call Stack, Sockets
- Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
The complexities of Socket Io and other uses, Building a chat between 2 people, building a fully operation all that renders and updates information realtime
- What are you most excited about trying to implement or see how it works?
Rendering and updating apps in real time
