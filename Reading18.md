## Description 

* AWS API Gateway :
>_"A fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. APIs act as the "front door" for applications to access data, business logic, or functionality from your backend services. Using API Gateway, you can create RESTful APIs and WebSocket APIs that enable real-time two-way communication applications. API Gateway supports containerized and serverless workloads, as well as web applications. API Gateway handles all the tasks involved in accepting and processing up to hundreds of thousands of concurrent API calls, including traffic management, CORS support, authorization and access control, throttling, monitoring, and API version management. API Gateway has no minimum fees or startup costs. You pay for the API calls you receive and the amount of data transferred out and, with the API Gateway tiered pricing model, you can reduce your cost as your API usage scales."_
* AWS DynamoDB
>_DynamoDB is a key-value and document database with single-digit millisecond response times at any scale. It’s a fully managed durable database with built-in security, backup, and restore capabilities.
A keyword you’ll often hear with DynamoDB is that it is a NoSQL database, which simply means it doesn’t use the traditional SQL query language used in relational databases Its design is to reduce complexity between tables by consolidating objects into a common collection or “schemaless” table in a NoSQL database. These objects are then grouped together based on common themes, which will meet the conditions of the common queries of the application that you set._
* Dynamoose
>_Dynamoose is a modeling tool for Amazon's DynamoDB (inspired by  Mongoose
**Dynamoose is Sponsored by Dynobase**
Dynobase helps you accelerate your DynamoDB workflow with code generation, faster data exploration, bookmarks and more_

### How does DynamoDB store data?
_Although there is some rigidity within the service, DynamoDB supports two data models allowing for slightly different needs and some flexibility.
First is the key-value store, a scaled-up distributed hash table. The items within the table are uniquely identifiable by a key-value pair of attributes, which is used to **GET**, **SET**, **UPDATE** and **DELETE**. There are two types of attributes: the Primary Key, which works similarly to an item ID, and the Sort Key, which allows for ordering the items.
As we know, hash tables are reliable, consistent, and fast whatever their size, however, their drawback is that only one record can be retrieved at a time.
To combat this, DynamoDB can also be used as a wide-column store meaning that each row can have any number of columns at any time. This B-tree data structure and secondary index provide the option to find an item while also allowing for range queries. They can be used to reference and order items by different Primary Keys and Sort Keys. It’s also important to remember that DynamoDB is a schema-less database, in which items can have different sets of attributes._
### Setting up AWS DynamoDB
"Setting up DynamoDB is incredibly simple. In this example, we are going to use parameters and features available in the AWS Free Tier so you’re able to replicate a similar version if you’re just starting out."

### To create a NoSQL Table

1.  Head over to DynamoDB console, and click Create Table.
2.  You’ll then need to name the table itself.
3.  The Primary Key or Partition Key is used to spread data across partitions for scalability, so use a feature that has a range of values and will have evenly distributed access patterns.
4.  The Sort Key, allows just that, the ability to sort the data above. Another value that works across your data and can help dig into the table further is necessary here.
5.  To enable Auto Scaling, the Default Settings box needs to be unticked. By doing this, an AWS IAM role will automatically be created called DynamoDBAutoScaleRole, which will manage the auto-scaling process.
6.  Lastly, scroll all the way down and click Create.*
### Adding Data

1.  Under the Items tab, click Create Item.
2.  Add in the data for both the Primary and Sort Keys for each data entry, remembering to click Save each time.