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
    * Provides low latency for content delivery.
    * Global distribution even when it is hosted in a region.
    * Static and dynamic web content. How? Edge location to cache content. 

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
1. Fargate
    * Serverless compute engine for containers
    * Manages containers like Docker
    * Scaled automatically - and serverless
1. Lightsail
    * Quickly lauch all resources you need for small projects
    * Simple for folks with no cloud experience.
    * Low predictable fees
1. Outpost
    * Allows cloud services in the internal data center
    * Useful for latency or data sovereignty needs
    * Used for hybrid experience
1. Batch
    * Process large workloads in smaller chunks
    * Dynamically provisions instances based on volume
    * Example - send high volume email 1000 emails at a time.

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
1. Simple Storage Service ([S3](https://docs.aws.amazon.com/cli/latest/reference/s3/)) - Regional Service with global namespace
    * Fine Grained Security - ACLs, access point and bucket policies
    * Unique name across all buckets in AWS
    * 11 9s of durability: regional level redundancy
    * 4 9s of availability 
    * S3 does not automatically replicate across regions - it can be setup.
    * Use for static websites, data archivale, analytics such as redshift and athena. Upload with S3 transfer acceleration for file uploads from mobile applications.
1. S3 Storage Class
    * Standard
    * Intelligent Tiering: Unknown or changing access. Standard durability with 3 9s availability
    * Infrequent Access: For Long-Lived, Infrequently Accessed, Millisecond access when needed. Durable with 3 9s availability. 
    * One-Zone Infrequent Access: Cost 20% less than IA. Use if data is recreatable, infrequent millisecond access, availability is 99.5%.
    * Glacier: Data retrieval options 1-5 minutes, 3-5 hours, 5-12 hours. Multiple AZs. Standard durability. Cheap storage options.
    * Glacier Deep Archieve: 12hrs or 48hr retrieval options. Cheapest. Long-term data archivale accessed once or twice a year. No availability - but standard durability.
    * Outposts: Data that needs to be kept local. Demanding application performance needs.

1. Buckets: Root level 'folders' for file storage
    1. Folder
    1. Object Durability
    1. Object Availability
    1. Object Lifecycle
    1. Object sharing
    1. Object versioning
1. EC2 Storage
1. EBS (Elastic Block Storage): Raw volume. Good for database storage. HDD with an independent life from the instance it is attached to. Only one per instance.
1. EC2 Instance Store: Ephimeral Storage during the life of the instance. It is temporary block-level storage for instances. Local fastest I/O.
1. EFS (Elastic File System): EFS file system as a common data source for workloads and applications running on multiple instances. Regional serverless network file system. Like dropbox. Only for Linux filesystems. Shared directories. Expensive option.
1. Storage Gateway: Hybrid storage - some on the cloud, some local. File directory - some hosted locally some on the cloud. Moving backups to the cloud. Reduce costs by being selective, opt for low latency local files.
1. AWS Backup: Create a backup plan for all storage.


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
1. [CodePipeline](https://aws.amazon.com/codepipeline/): Automate release pipelines with CI-CD. 
    * AWS offers continuous integration and continuous delivery service
## Logs

1. [CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html): enable operational and risk auditing, governance, and compliance of your AWS account
    * Actions taken by a user, role, or an AWS service are recorded as events in CloudTrail. 
    * Events include actions taken in the AWS Management Console, AWS Command Line Interface, and AWS SDKs and APIs.
    * If a user terminates an EC2 instance via an API. Cloudtrail will be able to tell which user took that action.
1. [CloudWatch](https://aws.amazon.com/cloudwatch/): Observe and monitor resources and applications on AWS, on premises, and on other clouds
    * Amazon CloudWatch is a monitoring and management service for AWS, hybrid, and on-premises applications and infrastructure resources.
    * Performance and operational data in the form of logs and metrics 
    * monitor full stack (applications, infrastructure, network, and services) and use alarms, logs, and events data to take automated actions and reduce mean time to resolution (MTTR). 
