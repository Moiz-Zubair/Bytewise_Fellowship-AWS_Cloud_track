# AWS Solutions Architect:
 ## General Info:
   ### Regions and Availability Zones:
   A **region** is a physical location in the world that comprises clusters of highly redundant data centers.
   Within each region there are **availability zones (AZs)**. An AZ consists of one to six data centers, with redundant power supplies and networking connectivity.
   In addition to regions and AZs, AWS offers edge locations. In AWS, the edge location is used to serve Amazon CloudFront and Amazon Route 53
   
 ## Compute:
  ### AWS EC2: 
   Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. AWS use Xen and Nitro Hypervisors.
   - On Demand
   - Reserved
   - Spot
   - Dedicated Hosts
    
   Standard Reserved Instances cannot be moved between regions. You can choose if a Reserved Instance applies to either a specific Availability Zone, or an Entire Region, but you cannot change the region.

   - Instance Meta-data

  ### Amazon EC2 Auto Scaling
   Amazon EC2 Auto Scaling helps in automatically scaling the Amazon EC2 instances up and down as per the policies you define.
   
  ### AWS Lambda:
   1. AWS Lambda enables you to run code without provisioning or managing any servers or infrastructure.
   2. You can also run code in response to event triggers such as Amazon S3 uploads, Amazon DynamoDB updates, Amazon Kinesis streams, Amazon API Gateway requests, and so on.
   3. The pricing for using AWS Lambda is simple. You pay only for the compute time when the code is getting executed; there is no charge when the code is not running.
   
   ### Amazon EC2 Container Service:
   There are no separate charges for Amazon ECS; you pay only for the AWS resources used such as Amazon EC2 instances, Amazon Elastic Block Storage (EBS) volumes, and so on. 
   
   ### Amazon Lightsail:
   - Amazon’s Website Hosting Service (Virtual Private Service).
   - Small Scale deployment

  ### AWS Elastic Beanstalk:
   - AWS Elastic Beanstalk lets you run and manage web applications without worrying about the underlying infrastructure.
   - AWS Elastic Beanstalk automatically handles deployment, load balancing, autoscaling, and application health monitoring. At the same time, you have full control over the AWS resource; you can access the underlying resources at any time using the console

  ### Security Groups:
  1. A security group acts as a virtual firewall for your instance to control inbound and outbound traffic. When you launch an instance in a VPC, you can assign up to five security groups to the instance.
  2. Security groups act at the instance level.
  3. Security groups are stateful.
  4. Evaluate all rules before deciding whether to allow traffic

----------------------------------------------------------------

  ## NETWORKING:
  ### Amazon Virtual Private Cloud:
   - A VPC spans all of the Availability Zones in the Region.
   - After creating a VPC, you can add one or more subnets in each Availability Zone.
   - If you have multiple Amazon VPCs, you can connect them as well using Amazon VPC peering.
   - Route Tables control traffic between subnets.
   - It must be noted that a subnet is tied to only one availability zone. Of course, within an AZ you can have multiple subnets.
   - /16 is the largest VPC, and smallest is /28.
   - AWS uses 5 IP addresses per subnet.
   - VPC Flowlogs — VPC Flow Logs is a feature that enables you to capture information about the IP traffic going to and from network interfaces in your VPC. VPC Flow Logs can be created at the VPC, subnet, and network interface levels.
   - Elastic IP Address — An Elastic IP address is a static IPv4 address designed for dynamic cloud computing. An Elastic IP address is a public IPv4 address, which is reachable from the internet.
   - Bastion or Jump Boxes — A Bastion host allows you to securely administer (via SSH or RDP) an EC2 instance located in a private subnet. Don’t confuse Bastions and NATs, which allow outside traffic to reach an instance in a private subnet.
   - VPC Endpoint — A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. There are two types of VPC endpoints: interface endpoints and gateway endpoints.
   - An interface endpoint is an elastic network interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service.
   - A gateway endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service. The following AWS services are supported: Amazon S3 and DynamoDB

 AWS DirectConnect and CrossConnect, Public Subnet, Private Subnet, Security Group —
    When we create a new security group, all outbound traffic is allowed by default. Security Groups operate at the instance level, they support “allow” rules only, and they evaluate all rules before deciding whether to allow traffic.
The purpose of an “Egress-Only Internet Gateway” is to allow IPv6 based traffic within a VPC to access the Internet, whilst denying any Internet based resources the possibility of initiating a connection back into the VPC. Further information:

  ### ROUTE TABLE
  You can associate multiple subnets with the same route table.
  When you create a VPC, Amazon VPC automatically creates the main route table.
  
  ### INTERNET GATEWAY
  - It must be noted that an IG is a horizontally scaled, redundant, and highly available component in VPC.
  
  ### NETWORK ADDRESS TRANSLATION
  - Using a NAT device, you can enable any instance in a private subnet to connect to the Internet
  - There are two types of NAT devices available within AWS. NAT instances and NAT Gateway
  
  ### Network ACLs
  - A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets.
  - Is stateless: Return traffic must be explicitly allowed by rules.
  - We process rules in number order when deciding whether to allow traffic
  
  ### Amazon Route 53
  Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service. You can use Route 53 to perform three main functions in any combination: domain registration, DNS routing, and health checking.

  Common DNS types


  Routing Policy -

  1. Simple routing policy
  2. Failover routing policy
  3. Geolocation routing policy
  4. Geoproximity routing policy
  5. Latency routing policy
  6. Multivalue answer routing policy
  7. Weighted routing policy
 

  ### ELB
  - Elastic Load Balancing supports three types of load balancers: Application Load Balancers, Network Load Balancers, and Classic Load Balancers.
  - You configure your load balancer to accept incoming traffic by specifying one or more listeners.
  
  ### AWS Direct Connect
  Using AWS Direct Connect, you can establish private, dedicated network connectivity from your data center to AWS.
  
  ---------------------------------------------------------------
  
  ## SECURITY AND COMPLIANCE
  ### AWS Identity and Access Management
   AWS Identity and Access Management (IAM) is used to create users, groups, and roles.
  ### AWS Certificate Manager
  ### Amazon Inspector
  
  ----------------------------------------------------------------
  
  ## STORAGE AND CONTENT DELIVERY
   Storage offerings of AWS can be divided in 3 categories
    1. Object — An object is a piece of data, like a document, image, or video that is stored with some metadata in a flat structure. As a example you can easily develop a web application which can call (API)content on top of Amazon S3
    2. File — In file storage, data is presented via a file system interface and with file system semantics to instances.
    3. Block — In block storage, data is presented to your instance as a disk volume.
    
   ### Amazon Simple Shared Storage (S3)
  - 99.999999999 percent durability
  - Object Storage
  - 100 buckets per account
  - You can store unlimited amount of data but each file size can’t exceed 5TB.
  - It is a regional service; that is, content is automatically replicated within a region for durability.
  - Amazon S3 supports multipart uploads
  - Amazon S3 is designed to provide 99.99 percent availability.
  - For DR Using cross-region replication, you can automatically replicate each S3 object to a different bucket in a different region.
  - Two type of consistency — read-after-write consistency/Eventual Consistency.
  - Access Control — Access Policies / Bucket Policies / ACL
  - lifecycle management — Transition action/Expiration Action

  ### Storage Class :-
  
  **Amazon S3 Standard** used for frequently accessed data, synchronously copied across three facilities and designed to sustain the loss of data in two facilities. Support SSL encryption of data in transit and at rest. Designed for 99.99% availability over a given year


  **Amazon S3 Intelligent-Tiering** (S3 Intelligent-Tiering) Automatically moves objects between two access tiers based on changing access patterns. Designed for 99.9% availability over a given year


  **Amazon S3 RRS** (Reduced Redundancy Storage) is a storage option that is used to store noncritical, non-production data.


  **Amazon S3 Standard-Infrequent Access** (IA) is an Amazon S3 storage class that is often used for storing data that is accessed less frequently. Support SSL encryption of data in transit and at rest. Designed for 99.9% availability over a given year


  **Amazon S3 One Zone-IA** is a new storage class for storing data that is accessed less frequently, but requires rapid access when needed. One Zone-IA stores data in a single AZ. Designed for 99.5% availability over a given year

   ### Amazon Glacier
   - Object Storage
   - expedited (1–5 mins), standard (hours), and bulk retrievals(day).
   - To upload a file in Glacier first, you need to create a vault

  **Amazon S3 Glacier Deep Archive** (S3 Glacier Deep Archive) S3 Glacier Deep Archive is Amazon S3’s lowest-cost storage class and supports long-term retention and digital preservation for data that may be accessed once or twice in a year.

  ### Elastic File System (EFS)
  - File Storage service that can be shared between EC2 instances
  - Support NFS v4
  - Data is stored across multiple AZ’s
  - Read after write consistency
  - **EFS Storage Classes** — Infrequent Access and Standard
  
  ### Elastic Block Storage (EBS)
  - Block Storage 3 TYPES (Amazon EC2 instance store , Amazon EBS SSD-backed volume, Amazon EBS HDD-backed volume)
  - Amazon EBS replication is stored within the same availability zone, not across multiple zones.
  - EBS Instance Store (Ephemeral Store)
  - A persistent storage (means the storage is independent outside the life span of an EC2 instance)
  - EBS, EFS, and FSx are all storage services base on Block storage
  - Snapshot goes to S3
  - AMI’s can be created from both Snapshot and Volumes
  - EC2 — Take Snapshot — Create AMI (Amazon Machine Images)from Snapshot — Use AMI to Launch Instance  
    
  ![image](https://user-images.githubusercontent.com/71292230/195424502-9ab13400-6167-43e8-abc1-b5fb894ac513.png)
  
  ### AWS Storage Gateway
   - AWS Storage Gateway is a hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage.
   - The service provides three different types of gateways — Tape Gateway, File Gateway, and Volume Gateway
   - The file gateway enables you to store and retrieve objects in Amazon S3 using file protocols, such as NFS. Objects written through file gateway can be directly accessed in S3.
   - The tape gateway provides your backup application with an iSCSI virtual tape library (VTL) interface, consisting of a virtual media changer, virtual tape drives, and virtual tapes. Virtual tape data is stored in Amazon S3 or can be archived to Amazon S3 Glacier
   - The volume gateway provides block storage to your applications using the iSCSI protocol. Data on the volumes is stored in Amazon S3. To access your iSCSI volumes in AWS, you can take EBS snapshots which can be used to create EBS volumes.
  
  ### Import/Export Options (Snowball)
   - Import-Export Disk’s
   - Puts data in S3 (and pulls from it if we want data exported out of AWS)
   - Snowballs come with two storage sizes: 50TB and 80TB
   - **Snowball** Edge is up to 100 TB and also has on-device compute capability. For example, the suitcase can run code to pull data in and store it.
   - **Snowmobile** is a truck, Exabyte scale data transfer. 100 PB storage limit.

   ### Amazon CloudFront
   - Amazon CloudFront is the global content delivery network (CDN) service of AWS.
   - Amazon CloudFront provides advanced CDN features such as SSL support, geographic restriction, and private content.

---------------------------------------------------------------------

  ## DATABASE
  - Multi AZ’s vs Read Replicas
  - OLTP vs OLAP
  - Two type of Backups — Automated and Snapshot
  - Restore version of DB will be always new instance with new end point.
  - Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run.
  
  ### RAID
  - Amazon Relational Database Service
  - Amazon Relational Database Service (Amazon RDS)- optimized for memory, performance or I/O — and provides you with six familiar database engines to choose from, including Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle Database, and SQL Server. You can use the AWS Database Migration Service to easily migrate or replicate your existing databases to Amazon RDS.
  - RDS runs on VMs. It’s not serverless.
  - Amazon RDS Multi-AZ deployment, automatically provisions and maintains a synchronous “standby” replica in a different Availability Zone.
  ### Amazon Aurora
  - Amazon Aurora is Amazon’s relational database built for the cloud. It supports two open source RDBMS engines: MySQL and PostgreSQL.
  - By default, the data is mirrored across three AZs, and six copies of the data are kept.
  ### Amazon DynamoDB
  - Amazon DynamoDB is a fully managed NoSQL database service of AWS.
  - Stored on SSD, Spread across 3 geographically distinct DCs. Eventual Consistent Reads and Strongly Consistent Reads
  ### Amazon Redshift
  - DWH
  - Redshift Spectrum is a feature of Amazon Redshift that enables you to run queries against exabytes of unstructured data in Amazon S3, with no loading or ETL required.
  ### Amazon ElastiCache
  - Amazon ElastiCache — offers fully managed Redis and Memcached. open source compatible in-memory data stores
  ![image](https://user-images.githubusercontent.com/71292230/195425498-0cb9fb5d-23e0-472f-891d-c0a65a97d542.png)

---------------------------------------------------------------------------------

  ## Analytics
  ### Amazon Athena
   - Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL.
   - Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run.
   - Athena is out-of-the-box integrated with AWS Glue Data Catalog, allowing you to create a unified metadata repository across various services, crawl data sources to discover schemas and populate your Catalog with new and modified table and partition definitions, and maintain schema versioning.
  ### Amazon EMR
   - EMR provides a managed Hadoop framework that makes it easy, fast, and cost-effective to process vast amounts of data across dynamically scalable Amazon EC2 instances
  ### Amazon CloudSearch
   - CloudSearch is a managed service in the AWS Cloud that makes it simple and cost-effective to set up, manage, and scale a search solution for your website or application.
  ### Amazon Elasticsearch
  Service makes it easy to deploy, secure, operate, and scale Elasticsearch to search, analyze, and visualize data in real-time.
  ### Amazon Kinesis
  Kinesis makes it easy to collect, process, and analyze real-time, streaming data so you can get timely insights and react quickly to new information.
  Kinesis Data Firehose, Kinesis Data Analytics, Kinesis Data Streams, and Kinesis Video Streams
  
  -------------------------------------------------------------------------------------------------------
 
  ## MANAGEMENT TOOLS
  ### AWS CloudFormation
  IaaC, Infrastructure as Code. The artifacts are called Templates
  ### AWS Service Catalog
  Manage a catalog of approved services for the AWS account. Used by enterprises
  ### Amazon CloudWatch
  - Used for monitoring performance
  - Can create CloudWatch Alarms
  - Standard Monitoring — 5 mins
  - Detailed Monitoring — 1 mins
  - Can create dashboards and alarms
  ### AWS CloudTrail
  - CCTV
  - CloudWatch is all about performance monitoring but CloudTrail is about auditing
  - CloudTrail monitors API calls

----------------------------------------------------------------------------------------------

  ## DEVELOPER TOOLS
  ### AWS CodeCommit
  AWS CodeCommit is a fully managed source control service that makes it easy to host highly scalable private Git repositories securely.
  ### AWS CodePipeline
  AWS CodePipeline builds, tests, and deploys code every time the code is modified, updated, and checked in based on the release process models you define.
  ### AWS CodeBuild
  Fully managed build service that builds and compiles source code, runs tests, and produces software packages that are ready to deploy,
  ### AWS CodeDeploy
  Automates code deployments








