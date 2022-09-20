# AWS Migration Strategies:
  ## Migration:
   Migration in simple words is defined as:
   > Moving your data from an on-premise data center to Cloud is called Migration
   
   Business is no easy task when it comes to handling situations like security, scaling up or down, etc. Let’s look at a few use cases where Migration could be needed:
   - Your project has started receiving a high volume of traffic overnight
   - Your clients want fast application implementation and deployment
   - It’s becoming expensive to manage the growing database needs
   - You are cautious about the mishap of data center going down
  
  If cloud migration is carried out then these problems mentioned above will get handled automatically.
  
  ## Phases of AWS Migration
   Data Migration seems an easy process because, in layman’s term, it means moving your data from one location to the other. However, it is more complex as the process involves different phases. These phases are defined as:
   
   ![image](https://user-images.githubusercontent.com/71292230/191332212-5f3ffd4c-1a81-473a-8606-94e07a13fac1.png)

  ### Phase 1: Discovery (Apps which can be moved to Cloud)
   There are times you need not require to move your entire business to the cloud. This is where segregation is important. You need to identify the applications which can be Migrated and which cannot.
  ### Phase 2: Assessment (Choosing Your Migration Method)
   Depending on the data, AWS provides different ways to Migrate your application e.g. AWS Snowball, AWS Snowmobile, AWS Direct Connect, etc. Once you have chosen an appropriate way to move your data, also look for the resources you’ll need for it.
  ### Phase 3: Proof of Concept (POC) for AWS Storage
   Once you know how and what you are migrating, next, you have to figure out how and where you will store it. The entire motive of moving to AWS is to minimize expenses. In this phase, you’ll test your workload and understand about AWS Storage Service, their benefits, limitations, and the necessary security controls.
  ### Phase 4: Application Migration to AWS
   Now that you have all the pre-requisites like the blueprint, Migration tools, list of assignments, backups and its synchronization with your on-premises data repositories. You can finally migrate your project to AWS Cloud. Once you have Migrated your project to cloud, reliability, and durability are the added benefits you get.
  ### Phase 5: Enterprise Cloud Operations
   At this point, you’ve already migrated to AWS, and AWS will bring updates that you’ll need to incorporate in your existing architecture. Hence, you must ensure that you have a 24×7 support team keeping track of system maintenance and upgrades after the Migration.

  ## The 6 R's of AWS Migration Strategies:
  
  ![image](https://user-images.githubusercontent.com/71292230/191335465-d73dae9a-c87a-4b78-9681-8c1e89153b1e.png)
  
   The complexity of migrating existing applications varies, depending on the architecture, Amazon came up with different strategies which they commonly termed as 6 R’s.
   
   1. **Rehost:-** You have your application ready and working then you can simply Rehost it on AWS. Also referred to **“Lift and Shift”**. You lift your services and applications from your hosting environment and shift them to cloud using a third party exporting tool.
   
   2. **Replatform:-** You have an outdated version of your application running on your hosting environment so you have to modify your application and then Rehost it. Replatform is a modification of “Lift and Shift”. It involves optimizing the cloud architecture to achieve the benefits **without changing the core architecture** of the application.
   
   3. **Repurchase:-** There would be certain applications that won’t be compatible with the new architecture. In that case, you need to purchase a new application for the new architecture. AWS Marketplace provides a wide range of services that too with a “Pay as you Use” model. Repurchase is also referred to as **“drop and shop”** where you upgrade, ease the implementation and accept the new architecture and make changes to the existing model.
   
   4. **Refactor:-** You want to add up new features, scale up the limits of the existing business model and performance that are difficult with the existing environment. You reconsider your needs, though the solution is a bit expensive. Improving business by **moving to a service-oriented architecture (SOA)** will benefit your business in the longer run.
   
   5. **Retire:-** After AWS Migration you can differentiate between useful and use less resources. Hence, you **cut off all the resources that are no longer useful** to the business and build a strategy around the new resources. This will cut down the extra cost. With lesser things to worry about, now you can focus on maintaining the resources used by the new business model.
   
   6. **Retain:-** As you know, the sections of your project you need to migrate. You can simply use any of the above-mentioned strategies. Then, **build a strategy to retain those applications**, which, according to your business model are yet not ready to be migrated to the cloud or the applications that were upgraded recently.


# AWS Snow Family:
  The AWS Snow family is the collection of physical devices that helps us to move the data into the AWS and vice versa. The SNOW Family contains three types for migrating a large amount of data in and out from the AWS. There are as following:
  - **Snowball**
  - **Snow Edge**
  - **Snowmobile**
  
  ![image](https://user-images.githubusercontent.com/71292230/191335955-34268868-a5fc-42a5-92ef-2df93434637f.png)

For all the SNOW Family devices, there is no need to worry about writing code or the network connection for allocating the data for the internet etc. When you are using these SNOW Family devices either you will get an empty device or full of the data in the device. When we want to get the data from AWS then we can copy the whole data in the device and then we can ship the device back. 
The data that is migrating will get full security and computing resources.

It is very easy to use the transfer of the data. We can transfer the terabytes of data within weeks. That is also in a very secure manner. We can use it to move things like databases, backups, archives, healthcare records, analytics datasets, IoT sensor data, and media content, 
especially when network conditions prevent realistic timelines for transferring large amounts of data both into and out of AWS.
  
  ## SNOW Family:
  1. **Snowball:**

   We can use snowball for both in and out data migration. When you want to migrate the data from the AWS then you will get a device that is full of data is shipped and you can ship back the device that contains the data. If you want to migrate the data into your AWS then an empty device is shipped and you can ship back the device with the empty device. This can be used when you want TB or PB amount of data to transfer. The data in the device is encrypted using KMS. We can use this when we need to transfer data from 10 TB to 10 PB. For the larger jobs and multiple locations we can’t use a single snowball device, we have to use multiple snowballs.

  2. **Snowball Edge:**

   We can use snowball Edge for both in and out data migration. This provides both storage and compute. It has a larger capacity than any other SNOW Family. For machine learning and processing we need a large set of data. In that case, we can use this. We can use this same when we use snowball, but when compute is needed we have to use snowball Edge. 
   We can use this for data collection.This supports some specific AWS services like EC2 instance and Lamda functions.

  3. **Snowmobile:**
  
   This is little among all the SNOW Family providers. This is a portable storage data center within a shipping container on a semi-truck. A Snowmobile will arrive at the customer location and it looks like a network-attached data store for more secure, high-speed data transfer. After data is transferred to Snowmobile, it is driven back to an AWS Region where the data is loaded into Amazon S3 and vice versa. The data inside the snowmobile is very secured. The data is encrypted using KMS. The truck is waterproofed and 24/7 it is under video surveillance. If the truck got any fire accident then also there is no need to worry, because the truck has fire suppression. It has GPS tracking for knowing the live tracking. We can transfer up to 100PB per Snowmobile. Snowmobile makes it easy to move massive volumes of data to the cloud, including video libraries, image repositories, or even a complete data center migration. Transferring data with Snowmobile is more secure, fast, and cost-effective. Optionally we can escort security vehicles while in the transfer.
  
 ## AWS Snow Family key features:
  All these key features are standard features across each device type. These features are listed as:
  
  - **Simple management and monitoring:**
    
    AWS OpsHub is a GUI available for easy setup and managing Snow devices. Rapidly deploy edge computing workloads and migrate data to the cloud.

  - **NFS endpoint:**
    
    NFS v3 and v4.1 are supported so you can easily use Snow devices with your existing on-premises servers and file-based applications.
  
  - **On-board computing:**
    
    Computing resources to collect and process data are made available on the devices. They run specific Amazon EC2 instances with processing and storage available to support applications and AWS IoT Greengrass functions.
    
  - **Encryption:**
    
    Devices are automatically encrypted with 256-bit encryption keys that are managed by the **AWS Key Management Service (KMS)**. These keys are never stored on the device so your data stays secure during transit.
  
  - **Anti-tamper & Tamper-evident:**
    
    Devices featured with **Trusted Platform Module (TPM)** providing hardware root of trust. Each device is inspected after each use to ensure integrity of the device and helps preserving confidentiality of data.
    
  - **End-to-end tracking:**
    
    A **E-Ink shipping label** is used for easy tracking and automatic label updates for return shipping using *Amazon Simple Notification Service (SNS), text messages, and via the AWS Console*
  
  - **Secure erasure:**
    
    After completion of data migration, a software erasure of the device that follows the **National Institute of Standards and Technology (NIST)** guidelines for media sanitization.
    
   ## Feature comparison matrix:
   
   ![image](https://user-images.githubusercontent.com/71292230/191339609-0a811c33-0480-46d4-80d7-a0519f245b06.png)

   
    
    
