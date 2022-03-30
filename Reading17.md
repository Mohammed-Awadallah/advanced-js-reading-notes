# Reading 17 
## AWS Lambda 
_AWS Lambda is an event-driven, serverless computing platform provided by Amazon as a part of Amazon Web Services. It is a computing service that runs code in response to events and automatically manages the computing resources required by that code. It was introduced in November 2014._

## How does it work ? 
_When you send your code to Lambda, you are actually deploying it in a container. The container, however, is itself created, deployed, and managed entirely by AWS. You do not need to be involved in the creation or management of the container, and in fact, you do not have access to any of the infrastructure resources that might allow you to take control of it. The container is simply a location for your code._


## What makes it different ? 

1. Pay-as-you-go for great cost savings
> Just like other public cloud services, Lambda has a pay-as-you-go pricing model with a generous free tier, and it is one of the most appealing for cost savings. Lambda billing is based on used memory, the number of requests and execution duration rounded up to the nearest 100 milliseconds. This is a huge leap for fine-grained billing in order not to pay for spare compute resources compared to the second based billing of EC2.

2. Completely event-driven
>While most of the PaaS offerings are designed to be running 24/7, Lambda is completely event-driven; it will only run when invoked.
This is perfect for application services which have quiet periods followed by peaks in traffic.

3. Fully scalable
> When it comes to scalability, Lambda can instantly scale up to a large number of parallel executions, controlled by the number of concurrent executions requested. Scaling down is handled by automatically; when the Lambda function execution finishes, all the resources associated with it are automatically destroyed.

4. Supports multiple languages and frameworks
> Lambda comes with native support for a number of programming languages: Java, Go, PowerShell, Node.js, C#, Python, and Ruby code, and provides a Runtime API which allows you to use any additional programming languages to author your functions. There are additional open-source frameworks for rapid development and deployments, like Serverless, Apex and Sparta to name a few.


### Some Killer AWS lambda cases
1. Operating serverless websites
> This is one of the killer use cases to take advantage of the pricing model of Lambda and S3 hosted static websites.
Consider hosting the web frontend on S3 and accelerating content delivery with Cloudfront caching.
The web frontend can send requests to Lambda functions via API Gateway HTTPS endpoints. Lambda can handle the application logic and persist data to a fully-managed database service (RDS for relational, or DynamoDB for a non-relational database). 
You can host your Lambda functions and databases within a VPC to isolate them from other networks. As for Lambda, API Gateway and S3, you pay only after the traffic incurred, the only fixed cost will be running the database service.

2. Rapid document conversion
>If you are providing documents (for example, specifications, manuals, or transaction records) to your users, they may not always want them in one standard format. While many users may be happy with an HTML page, others may want to download a PDF or may need the document in a more specialised format.
You could, of course, store copies of each document in all formats that are likely to be requested. But storing static documents can take up a considerable amount of space, and it is not practical if the content of the documents change frequently, or in response to user inputs. It is often much easier to generate the documents on the fly. This is exactly the kind of task that an AWS Lambda application can handle rapidly and easily—retrieving the required content, formatting and converting it, and serving it either for display in a webpage or for download.

3. Automated backups and everyday tasks
>Scheduled Lambda events are great for housekeeping within AWS accounts. Creating backups, checking for idle resources, generating reports and other tasks which frequently occur can be implemented in no time using the boto3 Python libraries and hosted in AWS Lambda.

### How to write AWS Lambda functions 

Our input will look similar to that shown below, and we’ll use this example to execute a test case against each of the Lambdas we create:
<>
{
   "Number1": 10,
   "Number2": 20
}
<>
**we’ll be looking to receive the following in response:**
<>
{
   "Number1": 10,
   "Number2": 20,
   "Sum": 30,
   "Product": 200,
   "Difference": 10,
   "Quotient": 0.5
}
<>
