# AWS Core Services
 The following concepts and list of AWS Core Services are essential to understand various layers of an architecture.
 For example, a web-based enterprise application will utilize most if no all the layers and select technologies.
## Architecture

1. Elasticity: The ability to add or remove resources based on demand.
1. Fault Tolerance
1. High Availability
1. Principle of least priviledge 
1. Scalability
1. Trusted Advisor 


## Billing
1. Consolidated billing
2. Organization 
## Security
1. Firewall
1. IAM Users
    1. Roles
1. Identity and Access Managment (IAM)
1. Security Group (SG)
1. User Credentials
1. Access Control List (ACL): A firewall layer on the subnet level.
## Networking and Content Delivery
1. Virtual Private Cloud (VPC)
1. DNS Server
1. Route53
1. Subnet
1. Cloud Front: A Content Delivery Network (CDN)

## Compute
1. Lambda
    * Serverless: write functions and deploy. AWS manages the servers but no direct access.
    * Scales automatically - no need to configure, patch or manage.
    * Use case: Real-time file processing, sending email notifications, Backend business logic
    * Supports Java, Go, PoweShell, Node.Js, C#, Python, and Ruby. Executes code in response to events, timers or other triggers. Lambda has a 15-minute timeout.
1. EC2
    * Auto scaling: automatic adding or removal for EC2 instances based on traffic demand. Horizontal scaling or scaling out reduces the impact of local failures. Vertical scaling or scaling up adds CPU or memory and does nothing to improve availability.
    * Virtual Servers in the Cloud 750hrs free tier - deploy a db or web server whatever you need
    * SSH securly connects with a key pair. SSH Client uses private key, the EC2 instance uses a public key
    * EIC is EC2 Instance Connect - uses IAM polices to control SSH access to your instances 
    * AWS Systems Manager- use a web browser, or AWS CLI to manage EC2 instances directly
1. ELB
    * Elastic Load  Balancing and Auto-Scaling is offered by EC2.
    * Automatically distribute load across servers - classic, application, gateway and network load balancers.    


## Operational Databases
1. DynamoDB
1. Relational Database Service (RDS)
## Cache
1. ElastiCache

## Analytics
1. RedShift: Data warehouse
1. Glue: Data Integration
1. Lake Formation: Data Lake
1. QuickSight: Business Analytics
1. Athena: S3 SQL

## Big Data and Search
1. EMR: Hadooplo
2. OpenSearch: Search petabytes of unstructured data

## Streams
1. Kinesis: Real-tiome videa and data streams
1. MSK: Managed Streaming for Apache Kafka
1.  

## Storage
1. Simple Storage Service (S3)
1. Storage Class    
1. Buckets: Root level 'folders' for file storage
    1. Folder
    1. Object Durability
    1. Object Availability
    1. Object Lifecycle
    1. Object sharing
    1. Object versioning


## Messaging
1. Publishers
1. Subscriptions
1. Topics
1. SNS: Simple Notification Service
    * Sends text messages and plain text emails from your applications
1. SES: Simple Email Service
    * Sends rich text HTML Emails from your applications
1. SQS: Simple Queue Service
    * Sends messages on a queue between publisher and a single subscriber

## Develop Tools
1. CodePipeline: Automate release pipelines with CI-CD. 
    * AWS offers continuous integration and continuous delivery service
## Logs

1. CloudTrail
1. CloudWatch
