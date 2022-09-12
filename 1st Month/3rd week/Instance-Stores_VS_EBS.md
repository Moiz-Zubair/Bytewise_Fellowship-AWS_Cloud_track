# Instance Stores Vs Amazon Elastic Block Store(EBS):

## AWS Instance Stores:
  AWS Instance Store provides temporary blovk-level storage for EC2 instances, located on disk attached to host computer. It is ideal for temporary storage of information that changes frequently (buffers, caches, scratch data, temporary content) 
An instance store typically consists of one or more instance store volumes exposed as block devices. The size of an instance store as well as the number of devices available varies by instance type, these virtual devices are refered as ephemeral[0-23].
A typical Instance store on a particular system can be seen as:

![AWS Instance Store](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/instance_storage.png)

## AWS Elastic Block Store:
  Amazon Elastic Block Store most commonly known as Amazon EBS is an easy-to-use, scalable, high-performance block-storage service designed for Amazon Elastic Compute Cloud (Amazon EC2).
 It is used with EC2 cloud service to store persistent data, the data is kept on the AWS EBS servers even when the EC2 instances are shut down. EBS allows users to scale storage capacity at low subscription-based pricing model. The data volumes can be dynamically attached, detached and scaled with any EC2 instance, just like a physical block storage drive.

### How EBS works:
![EBS working](https://d1.awsstatic.com/product-marketing/Storage/EBS/Product-Page-Diagram_Amazon-Elastic-Block-Store.5821c6ee4297f3c01cba37e304922451c828fb04.png)

## Instance Stores VS AWS EBS:
|              Instance Stores          |           AWS Elastic Block Store |
|                 -----------           |           -----------             |
| Local to Instacne                     |  Persistent block-storage volumes |
| Non-Persistent data store             | 99.99999% availability            |
| No replication of Data (by default)   |  Automatically replicated within its Availability Zone |
| No snapshot support                   | Point-in-time snapshot support |
| SDD or HDD                            | Modify Volume type as needs change  |
|                                       |   Auto recovery                   |
|   ![image](https://user-images.githubusercontent.com/71292230/189718642-bd9660a8-a2e3-40df-b435-3dc844c57673.png) | ![image](https://user-images.githubusercontent.com/71292230/189718739-c929b635-d11b-4568-9f7d-bdebe4c894c4.png)    |


### Resources:
https://aws.amazon.com/ebs/


https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html


https://www.youtube.com/watch?v=F7bhICTuz6k
