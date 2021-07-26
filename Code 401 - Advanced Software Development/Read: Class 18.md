# AWS: API, Dynamo and Lambda
## 1. What are serverless functions?
A serverless function is a programmatic function written by a software developer for a single purpose. It’s then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier.

## 2. If you were to create a system that emulated Lambda functions, how would you do it?
a. Open the Functions page on the Lambda console.

b. Choose Create function.
## 3. Under Basic information, do the following:
For Function name, enter my-function.

For Runtime, confirm that Node.js 14.x is selected. Note that Lambda provides runtimes for .NET (PowerShell,C#) Go, Java, Node.js, Python, and Ruby.

## 4. Choose Create function.


API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends. It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services. It can also generate API references from your definitions and make them available to your users as API documentation.

API Gateway integrates with many other AWS services like AWS Lambda, AWS SNS, AWS IAM, and Cognito Identity Pools. These integrations allow for fully managed authentication and authorization layers, as well as detailed metrics and tracing for API requests.

## AWS DynamoDB Guide
DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS). It offers:

reliable performance even as it scales.
a managed experience, so you won’t be SSH-ing into servers to upgrade the crypto libraries;
a small, simple API allowing for simple key-value access as well as more advanced query patterns.
DynamoDB is a particularly good fit for the following use cases:

Applications with large amounts of data and strict latency requirements. As your amount of data scales, JOINs and advanced SQL operations can slow down your queries. With DynamoDB, your queries have predictable latency up to any size, including over 100 TBs!

Serverless applications using AWS Lambda. AWS Lambda provides auto-scaling, stateless, ephemeral compute in response to event triggers. DynamoDB is accessible via an HTTP API and performs authentication & authorization via IAM roles, making it a perfect fit for building Serverless applications.

Data sets with simple, known access patterns. If you’re generating recommendations and serving them to users, DynamoDB’s simple key-value access patterns make it a fast, reliable choice.




### What is DynamoDB? 
“is a hosted NoSQL database offered by Amazon Web Services (AWS)”.

It offers :
- reliable performance.
- a managed experience.
- a small, simple API.
Benefits:
- Performance at scale.
- No servers to manage.
- Enterprise ready.



# Vocabulary Terms
Serverless Functions :
- serverless function is a programmatic function written by a software developer for a single purpose. It’s then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier.
## Cloud Storage :
Cloud storage is a cloud computing model that stores data on the Internet through a cloud computing provider who manages and operates data storage as a service. It’s delivered on demand with just-in-time capacity and costs, and eliminates buying and managing your own data storage infrastructure. This gives you agility, global scale and durability, with “anytime, anywhere” data access.
## CDN :
is a highly-distributed platform of servers that helps minimize delays in loading web page content by reducing the physical distance between the server and the user.



