# AWS: Events
### Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server
* Amazon’s API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale.
* With a few clicks you can create an API that acts as a “front door” for applications to access data, business logic, or functionality from your back-end services, such as workloads running on Amazon Elastic Compute Cloud (Amazon EC2), code running on AWS Lambda, or any Web application. Amazon API Gateway handles all the tasks involved in accepting and processing up to hundreds of thousands of concurrent API calls, including traffic management, authorization and access control, monitoring, and API version management.
* Express Gateway is an API Gateway that can sit at the heart of any microservices architecture, regardless of what language or platform you’re using. Express Gateway secures your microservices and exposes them through APIs using Node.js, ExpressJS and Express middleware.


## Serverless API:
Creates a collection of Amazon API Gateway resources and methods that can be invoked through HTTPS endpoints

- Triggers:
an AWS Lambda resource or resource in another service that you configure to invoke your function in response to lifecycle events, external requests or on a schedule, a function can have multiple triggers

- Dynamo vs Mongo:
DynamoDB is a fully managed AWS service ,supports limited data types and smaller item sizes; supports more data types and has fewer size restrictions

- Dynamoose vs Mongoose:
Dynamoose is a DynamoDB API structured like Mongoose, lets us provide a schema and perform CRUD operations against a DynamoDB table, installed via node and configured based on role

- SNS (Simple Notification Service)
Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication


## AWS SQS
A service from Amazon (Simple Queue Service) provides two Queue services, the first of which is Standard Queue, which is expandable based on use. Second, a FIFO queue will ensure that messages are sent in the correct sequence, and it will employ messaging groups to facilitate scalability.

##  AWS SNS
A Pub/Sub message (which sends messages from a publisher to a certain topic, then the sub receives a copy of all distinct messages) might include subscribers that are other AWS services like Lambda functions, SQS, or API. Async

SQS : Pull Mechanism – SQS messages are polled by consumers. SNS : Push Mechanism – SNS sends messages to users.

SQS: Messages are retained for a certain period of time if no consumer is present. The retention duration ranges from one minute to fourteen days. The default setting is four days. SNS: There is no perseverance. The message is delivered to whatever consumer is present at the moment of message arrival, and the message is destroyed. If there are no customers accessible, the message is lost. Message delivery is guaranteed in SQS but not in SNS.

AWS is used to create microservices.

Message Streams (AWS Kinesis) are distinct from message queues in that messages in streams are permanent (will not be removed). And we utilize it when we want to analyze the sequence of messages.

SQS : Pull Mechanism — Consumers poll messages from SQS. SNS : Push Mechanism — SNS pushes messages to consumers.



![](https://d2908q01vomqb2.cloudfront.net/1b6453892473a467d07372d45eb05abc2031647a/2018/06/13/edge-optimized-1024x513.png)


![](https://d2908q01vomqb2.cloudfront.net/1b6453892473a467d07372d45eb05abc2031647a/2018/06/13/lambda-in-vpc.png)







