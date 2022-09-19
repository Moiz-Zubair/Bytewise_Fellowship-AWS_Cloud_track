# AWS Trusted Advisor:
  ![image](https://user-images.githubusercontent.com/71292230/191078527-96d7e7fe-d422-42e8-938d-f81e577f0629.png)

  AWS Trusted Advisor is a service that helps in understanding if AWS services being used well. It does this by looking at **72** different *best practices* across **5** total categories, which include * Cost Optimization, Performance, Security, Fault Tolerance, and Service Limits/quotas*. 
  All AWS users have access to 7 of those best practices, while Business Support and Enterprise Support customers have access to all items in all categories. 
  
  ![image](https://user-images.githubusercontent.com/71292230/191079061-3b9ba0da-acac-4484-8ad3-f00d8a10f6b7.png)

## Categories:
### Cost Optimization:
  Cost Optimization category includes items related to the following services:
  - EC2 — Reserved Instance purchase recommendations, underutilized VMs, Reserved Instance lease expirations
  - Load Balancers — idle LBs
  - EBS — Underutilized volumes
  - Elastic IP — unassociated addresses
  - RDS — Idle databases
  - Route 53 — Inefficient latency record sets
  - Redshift — Underutilized clusters
  
  This list includes many of the services that are often the most expensive line items in an AWS account, but doesn’t take into account a large percentage of the AWS services available.
### Performance
  This category caters more towards production instances, as it aims to make sure the performance of your applications is not hindered due to overutilization. This includes:
  - EC2 — highly-utilized VMs, large number of security group rules (per instance or per security group)
  - EBS — SSD volume configuration, overutilized magnetic volumes, EC2 to EBS throughput
  - Route 53 — alias record sets
  - Cloudfront — CDN optimization, header forwarding, cache hit ratio, alternate domain names

  This category is one of the weakest in terms of services supported, so you may want to factor that in if you’re trying to make sure your production applications are performing well on alternative AWS services.

### Security:
  The security checks of AWS Trusted Advisor will look at the following items:
  - Security Groups — Unrestricted ports, unrestricted access, RDS access risk
  - IAM — Use of Roles/Users, key rotation, root account MFA, password policy
  - S3 — Bucket permissions
  - CloudTrail — logging use
  - Route 53 — MX and SPF record sets
  - ELB — Listener security, Security groups
  - Cloudfront — Custom SSL certificates, certificates on the origin server
  - Access keys — Exposed keys
  - Snapshots — EBS public snapshots, RDS public snapshots
     
### Fault Tolerance
  One of the main benefits of the cloud that often gets overlooked is the use of *distributed resources* to increase fault tolerance for your services. These items in the fault tolerance category are focused on increasing the redundancy and availability of your applications. 
    They include:
  - EBS — Snapshots
  - EC2 — Availability Zone balance
  - Load Balancer — optimization
  - VPN Tunnel — redundancy
  - Auto Scaling Groups — general ASG usage, health check
  - RDS — backups, multi-AZ configuration
  - S3 — bucket logging, bucket versioning
  - Route 53 — Name server delegations, record sets with high TTL or failover resources, deleted health checks
  - ELB — connection draining, cross-zone load balancing
  - Direct Connect — Connection / location / virtual interface redundancy
  - Aurora DB — instance accessibility
  - EC2 Windows — EC2Config agent age, PV driver versions, ENA driver versions, NVMe driver versions
  
  These AWS services really make sure that production applications have  *minimal **downtime** and minimal **latency**.* Additionally, some services like snapshots and versioning, help with recovering from problems in a timely fashion.

### Service Limits
  One of the hidden limitations that AWS puts on each account is a limit of how many resources you can spin up at any given time. This makes sense for AWS, so they don’t have new users unintentionally (or intentionally!) perform a DOS for other users. 
  These service limits can be increased if needed, but this is one of the few places where you can actually see if you’re coming close. The services covered are:
  - DynamoDB
  - EBS
  - EC2
  - Kinesis
  - RDS
  - Route 53
  - SES
  - VPC
  - ASG
  - CloudFormation
  - ELB
  - IAM

  AWS implements quotas to provide highly available and reliable service to all customers, and protects you from unintentional spend. Trusted Advisor will notify you once you reach more than 80% of a service quota.
  
 ## How It Works:
  
  ![image](https://user-images.githubusercontent.com/71292230/191081496-3341d5fe-672e-4a2e-8980-01e0b6ccb4e2.png)

# AWS Cloud Adoption Framework:
  AWS Cloud Adoption Framework (popularly known as **AWS CAF**) provides a comprehensive list of recommendations for *implementing, adapting, configuring, and maintaining* workflows associated with already deployed software.
  AWS CAF helps organizations build a *road map* to **cloud migration**, quickly bridge in-house IT knowledge gaps and deploy software in different environments.
  
  ## Main Phases:
   Main phases of AWS Professional Services Cloud Adoption Framework includes.
   
  ![image](https://user-images.githubusercontent.com/71292230/191082947-1304e3f5-cd15-4590-958a-669e2e3f48eb.png)

  1. Envision
  At this stage, you will be able to build a competent strategy for cloud migration, the implementation of which will require a minimum of time and money investment. You can also build long-term prospects for your business by choosing the optimal technology stack.

  2. Align
  This stage involves drawing up a clear action plan which, in addition to precisely describing the steps for cloud migration, will determine the specific benefits for your business. This will help you estimate all the risks associated with the moving process and choose the most effective approach for its implementation.

  3. Launch
  This phase of AWS CAF helps you build the workflows needed to deploy cloud services and add value to your business. As a result, you can quickly integrate new web services into your existing network infrastructure and benefit from them immediately after deployment.

  4. Realize Value
  This phase involves evaluating the effectiveness of innovations and planning a further strategy for your business. With its help, you can regularly compare the results of the updated workflows with the expected plans and adjust the chosen strategy.

## AWS CAF Perspectives:

![image](https://user-images.githubusercontent.com/71292230/191085750-656a694e-cb53-43ca-bad2-05361cee3600.png)


   Each AWS CAF Perspective is a list of responsibilities that specific employees in the company must perform. In essence, it is the standard that defines the safety and cost-effectiveness of migrating to the Amazon cloud.

  1. **Business Perspective:**
    Implementation of AWS CAF helps build a global business model with a long-term perspective to grow and adapt to changing market demands. Managers and business owners are benefitted with:
       - providing great planning opportunities.
       - maximizing the satisfaction of the end-user needs.
       - optimization of finances distribution.
       - end-to-end control of business risks, both external and strategic.
  
  2. **Governance Perspective:**
    This perspective helps in organizing and coordinating software and business processes outside of IT. It is helpful for IT managers, architects, and business analysts due to:
      - scheduling cloud workloads and properly prioritizing services.
      - choosing the right cloud migration methodologies.
      - cost optimization.
      - licenses management.
  
  3. **Operations Perspective:**
    This perspective of CAF AWS helps in managing workloads according to current and future business needs, resulting in quick planning and implementation of a new business strategy with minimal risk. This phase is crucial for **tech support operators** who benefit from the following:
      - service monitoring for getting assess the level of efficiency of IT operations and providing compliance with corporate requirements for operating software in the cloud.
      - resource inventory management to rationalize the use of virtual IT assets.
      - release/change management for intelligent selection of continuous integration/continuous delivery (CI/CD) methods.
      - reporting and analytics for performance monitoring.
      - creating backups and downtime assessment for continuous business processes.
    
  4. **Security Perspective:**
    AWS Cloud Adoption Framework security perspectives provide the recommendations for the right structure for management points and help reduce IT workloads for the Network Security team. Here are the AWS Cloud Adoption Framework security benefits they get:
      - Identity and Access Management (IAM), which provides extensive guidance on integrating AWS into user authentication and authorization processe.
      - Detective control, which is responsible for detecting suspicious network activity.
      - Infrastructure security, responsible for drafting regulations and security requirements.
      - Data protection, which helps you develop correct strategies to protect data during transfer and storage processes.
      - Incident response service that helps you instantly respond to abnormal network activity.
    
  5. **People Perspective:**
    This perspective helps HR specialists prepare the staff for the journey to the cloud. In particular, HR specialists receive:
      - the ability to predict new vacancies due to the modernized network architecture.
      - creating a common list of skills for cloud migration.
      - building a training plan for employees to carry out their usual tasks in an updated environment.
  
  6. **Platform Perspective:**
    The platform perspective serves to enhance the network infrastructure built with AWS. It plays a key role for network architects, CTOs, and managing members of the IT team. Here are the benefits they get:
      - understanding what requirements the design of the future system should meet;
      - the vision of prospects for scaling and building new workflows in the cloud;
      - aligning new business goals in the context of new computing power offered by the cloud.
      
![image](https://user-images.githubusercontent.com/71292230/191085497-c2400dcb-7b46-4ba9-9e81-8c8fc2f4ce57.png)

