# AWS DynamoDB:
  Amazon DynamoDB is AWS's fully managed non-relational database service. DynamoDB has high performance and scalability that wouldn’t be possible in a traditional data center. DynamoDB can automatically scale up and down to meet demands making it a cost-effective solution. It is also a fully managed option which means that AWS will provision what you need.
DynamoDB also has on-demand backup and point-in-time recovery capabilities that allow users to easily roll back if needed. 

![image](https://user-images.githubusercontent.com/71292230/190237379-a5e6e68e-3410-40b1-928e-fc041250f5d0.png)


 ## Benefits of DynamoDB:
  Benefits of using AWS DynamoDB are as following:
  - **Performance**
  - **Cross-region replication**
  - **Stream**
  - **Scalability**
  - **Data Model**
  - **Fine-grained access control**
  - **TTL (Time to leave)**

## Uses of DynamoDB:
- Used to build powerful web applications that automatically scales up and down. AWS DynamoDB also reduces the workload to maintain servers.
- Amazon DynamoDB is used to build the mobile app which is personalized for the smooth experience. It focuses on the operational tasks so that the user can focus on different applications.
- Devices can connect to the high-velocity, high-volume Internet of things data in Dynamo DB to Amazon Redshift and Amazon Quicksight.
- The user can create bidding platforms and recommendation engines with the scalability, throughput, and availability of DynamoDB.
- Flexible and reusable micro-services using AWS DynamoDB can build and for the fast performance.

# AWS DynamoDB vs AWS RDS:
  RDS and DynamoDB are both database services offered by AWS. Amazon RDS stands for **"Relational Database"**. RDS enables users to launch a *relational database* on AWS. But unlike DynamoDB — Relational Database Service is **NOT** the name of a database engine. It’s the name of a service that allows you to launch your *perfect relational database*.

## Comparison Table:
|DB Options| AWS RDS | AWS DYnamoDB |
| ---- | ---- | ---- |
|Type of Database|Relational Data-Base| key-value|
|Defining Features|Relational Data models, complex queries, joins and updates| unorganized data-models, used for transactions|
|Use Cases|traditionaol relational database for OLTP, well-informed data-structure, existing apps require RDS| Name/value pair data, unpredictable data-structure, High I/O needs, scales dynamically|
|Availablility|Multi-AZ enabled SLA: 99.95%| SLA: 99.99% |
|Scalability|Vertically scaling with interuptions in applications| Seamless on-demand horizontal scaling|
|Performance|Automatically optimized for the scenario by AWS System | Depends on Data-model, indexing, queries ran, storage optimization|
|Encryption|AES-256 encryption for dataon RDS DB server | AWS KMS for data encrypting data at rest |

  ### RDS vs DynamoDB Summed Up:
   > RDS makes it easy to set up, operate, and scale a relational database whereas DynamoDB is an AWS fully-managed, high-performance, NoSQL database.

# AWS Redshift:
  Redshift is a data warehousing service that uses SQL to analyze structured and semi-structured data across data warehouses, operational and analytical data sources, and data lakes.
  Redshift offers a wide range of features to manage and store large amounts of data in the AWS Cloud. It is highly-performant, by offering concurrency scaling to maximize throughout and table optimization through its use of AWS-designed hardware and machine learning.
  Amazon Redshift stores data at the petabyte scale. It is fully-managed by AWS, and highly-efficient at storing analytical and historical data.
  
  ## How it works:
  ![Redshift working](https://user-images.githubusercontent.com/71292230/190232876-03c0c7f9-1947-4f6f-b824-5c3d7dde2adc.png)
  
  ## Benefits of Using Redshift:
  - **High Performing** 🎭: Redshift utilizes columnar storage in its databases, where you can store frequently-accessed data. Columnar storage allows the databases to do a more precise search through searching values of specific columns,
  - **Scalable Horizontally** ⚖️: To ensure scalability, you can spin up additional Redshift nodes through the AWS Console or Cluster API, anytime there is a need for larger storage or increased speed. And those nodes can support workloads of up to eight petabytes of compressed data.
  - **Secure** 🔐: Redshift offers several security options like network Isolation, Cluster security groups creation within each Redshift Cluster, Data Encryption and You can also enable Cluster Encryption while launching a new Redshift cluster, encrypting all of the data stored within.
  - **Reasonable Pricing** 💲: Redshift is much cheaper than various on-premise solutions. Customers have the flexibility to determine the expense as operational or capital expenses.
  - **User-friendly** 🙂: The Redshift Query Engine (like the interface for PostgreSQL DB) is based on ParAccel. So if you have some experience with Postgres, Redshift is pretty easy to interact with.
  - **Vast Storage Range** 🗄️: Redshift deals with storing data beginning at the petabyte-range. Customers have the option to opt-in for Dense Storage compute nodes that give large storage space.

# Amazon DMS:
  AWS Database Migration Service, popularly known as AWS DMS, is a cloud-based service that makes it easy to migrate relational databases, data warehouses, NoSQL databases, and other types of data stores. You can use AWS DMS to migrate your data into the AWS Cloud or between combinations of cloud and on-premises setups.
  
  ![image](https://user-images.githubusercontent.com/71292230/190237161-88dd871f-a0a7-4875-8d8a-b38a90d62fa8.png)

  
  ## Benefits:
  - **Simple to use:** AWS DMS is simple to use. No need of installing any drivers or applications. You can also use this service for continuous data replication with the same simplicity.
  - **Minimal downtime:** DMS helps migration of databases to AWS with virtually no downtime. All data changes to the source database that occur during the migration are continuously replicated to the target allowing the source database to be fully operational during the migration process. 
  - **Supports widely used databases:** It can migrate your data to and from most of widely used commercial and open source databases. It supports data migration from homogenous and heterogenous databases alike. Migrations can be from on-premises databases to Amazon RDS or Amazon EC2, databases running on EC2 to RDS, from one RDS database to another RDS database. It can also move data between SQL, NoSQL.
  - **Low cost:** It is a low cost service. You only pay for the compute resources used during the migration process and any additional log storage.
  - **On-going replication:** An on-going replication task keeps your source and target databases in sync. Once set up, the on-going replication task will continuously apply source changes to the target with minimal latency.
  - **Reliable:** It is highly resilient and self–healing. It continually monitors source and target databases, network connectivity, and the replication instance. 
