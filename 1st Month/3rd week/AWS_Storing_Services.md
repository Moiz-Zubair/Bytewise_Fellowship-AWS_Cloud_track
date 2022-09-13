# AWS Storing Services:

## Amazon S3:
  Amazon Simple Storage Service popularly known as Amazon S3 offers scalability, data availability, security, and performance based object storage service. It also provides management features enabling a user to optimize, organize, and configure access to data.
 
 ![S3 Working](https://user-images.githubusercontent.com/71292230/189979190-85a5f222-7a47-4b03-8b06-8e5d34bf84e0.png)
 
 ### AWS S3 Features:
  1. **Storage Management:**
    Storage MAnagement features can be used to manage costs, meet regulatory requirements, reduce latency, and save multiple distinct copies of your data for compliance requirements
     - S3 Lifecycle – Configure lifecycle policy to manage objects and store them cost effectively throughout their lifecycle, can transition objects to other S3 storage classes/expire objects that reach the end of lifetimes.
     - S3 Object Lock – Prevent Amazon S3 objects from being deleted or overwritten for a fixed amount of time or indefinitely and can add another layer of protection against object changes and deletions.
     - S3 Replication – Replicate objects and their respective metadata and object tags to one or more destination buckets in the same or different AWS Regions.
     - S3 Batch Operations – Perform operations such as Copy, Invoke AWS Lambda function, and Restore on millions or billions of objects.
  
  2. **Access Management:**
    Provides features for auditing and managing access to buckets and objects. We have access only to the S3 resources that we create. To grant granular resource permissions that support our specific use case or to audit the permissions of our Amazon S3 resources, we can use the following features.
      - S3 Block Public Access – Block public access to S3 buckets and objects. By default, Block Public Access settings are turned on at the account and bucket level.
      - AWS Identity and Access Management (IAM) – Create IAM users for your AWS account to manage access to your Amazon S3 resources.
      - Bucket policies – Use IAM-based policy language to configure resource-based permissions for your S3 buckets and the objects in them.
      - Amazon S3 access points – Configure named network endpoints with dedicated access policies to manage data access at scale for shared datasets in Amazon S3.
      
  3. **Data Processing:**
    Transform data and trigger workflows to automate a variety of other processing activities at scale, following features can be used:
      - S3 Object Lambda – Add own code to S3 GET requests to modify and process data as it is returned to an application. Filter rows, dynamically resize images, redact confidential data, and much more.
      - Event notifications – Trigger workflows that use Amazon Simple Notification Service (Amazon SNS), Amazon Simple Queue Service (Amazon SQS), and AWS Lambda when a change is made to S3 resources.
  
  4. **Storage logging and monitoring:**
    Provides logging and monitoring tools that you can use to monitor and control how your Amazon S3 resources are being used. **Amazon CloudWatch** (track operational health of S3 resources and configure billing alerts) and **AWS CloudTrail** (provide you with detailed API tracking for S3 bucket-level and object-level operations) are the 2 **Automated monitoring** tools while
    **Server access logging** (detailed records for the requests made to a bucket) and **AWS Trusted Advisor** (evaluate account to optimize AWS infrastructure, improve security and performance, reduce costs, and monitor service) are the 2 **Manual monitoring** tools.
  
  5. **Analytics and insights:**
    Helps gain visibility into storage usage, which empowers to better understand, analyze, and optimize storage at scale.
  
  6. **Strong consistency:**
    Provides strong read-after-write consistency for PUT and DELETE requests of objects in S3 bucket.

## Amazon EFS:
   Amazon Elastic File System popularly known as AWS EFS is a simple and serverless elastic file system built to scale on demand without disruptions and with automatic shrinking due to files. No provison or management of capacity for growth
 andn simple interface to create files quickly. It manages all the file storage infrastructure for you abd you only pay for storage used by your files with no minimum fee or setup cost.
 Amazon EFS offers a range of storage classes designed for different use cases. These include:
  - Standard storage classes – EFS Standard and EFS Standard–Infrequent Access (Standard–IA), which offer multi-AZ resilience and the highest levels of durability and availability.
  - One Zone storage classes – EFS One Zone and EFS One Zone–Infrequent Access (EFS One Zone–IA), which offer customers the choice of additional savings by choosing to save their data in a single Availability Zone.
 Features of EFS are as following:
  1. Automatic scalability.
  2. It can be used with multiple EC2 instances and across availability zones.
  3. High throughput supports heavy workloads.
  4. It is a complete managed service.

## EBS vs EFS vs S3:
  To better understand the differences and similarities between these 3, I have created an infographic comparison summarizing everything
![Storage services differences](https://miro.medium.com/max/700/1*oibvNbEBZn7Jp-AZSApRBQ.png)
 
## Amazon RDS:
  Amazon Relational Database Service (Amazon RDS) is a collection of managed services that makes it simple to set up, operate, and scale databases in the cloud.
  
 ### RDS features and benefits:
  1. SQL type of database.
  2. Can be used to perform complex queries and joins.
  3. Easy to set up, highly available, fault-tolerant and scalable.
  4. Used when data is clearly defined.
  5. Common use cases include online stores and banking systems.
  
  ### Amazon RDS supports the following database engines:
  - SQL Server.
  - Oracle.
  - MySQL Server.
  - PostgreSQL.
  - Aurora.
  - MariaDB.

  ### AWS RDS Services
   AWS Provides some special services to RDS instances. This forces people to use the AWS RDS service instead of installing the database into EC2 instances. The RDS service includes the following:

  - Security and patching of the DB instances.
  - Automated backup for the DB instances.
  - Software updates for the DB engine.
  - Easy scaling for storage and compute.
  - Multi-AZ option with synchronous replication.
  - Automatic failover for Multi-AZ option.
  - Read replicas option for read-heavy workloads.

  ### AWS RDS Working:
  Following image shows the working of AWS RDS:
  
  
  ![RDS working](https://user-images.githubusercontent.com/71292230/189983058-5fa469b8-fa08-40d6-8ba3-af02fd563894.png)


#### Resources:
  https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
  
  https://medium.com/programmingnotes/aws-database-rds-1836b275f525
  
  https://enlear.academy/aws-ebs-vs-efs-vs-s3-75bd5f3ce94d
  
  https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html
  
