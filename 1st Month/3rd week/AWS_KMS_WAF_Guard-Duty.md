# Amazon KMS:
  AWS Key Management Services (KMS) is used to encrypt data across AWS workloads, digitally sign data, encrypt within applications using AWS Encryption SDK, and generate and verify message authentication codes (MACs).

## KMS Features:
  - Managed service that enables you to easily create and control the keys used for cryptographic operations.
  - A shared key management infrastructure with FIPS 140–2 Level 2 compliance
  - Currently supports 50+ AWS services.
  - A regional service
  - Highly Available (HA). Keys are kept as multiple copies in a single region to make sure its durability and reliability.
  - It integrates fully with IAM and CloudTrail for Permission Management and Auditing respectively.
  - Supports both symmetric and asymmetric key encryption. Until 2019, it only supported symmetric but now it supports both key encryption aspects [3]. With the support of asymmetric key encryption, it widened the aspect of interoperability by being able to connect to many other Key Management Infrastructures in the market
    
## KMS Working:
  AWS Key Management Service (AWS KMS) lets you create, manage, and control cryptographic keys across your applications and more than 100 AWS services.

![Working](https://d1.awsstatic.com/Security/aws-kms/Group%2017aws-kms.6dc3dbbbe5b75b46c4f62218d0531e5bed7276ce.png)

## KMS supported keys:
  KMS supports 2 types of keys:

   1. Customer Master Keys (CMK)
   2. Data Encryption Keys.
  
 By default, CMK can encrypt data up to 4KB. If data to be encrypted is more than 4KB, you have to use (CMK + Data Encryption Key) combination, which is known as the KMS Two Tier Architecture. 

### CMK Keys:
   There are three types of CMK.

  - **Customer Managed CMK** — Keys used by AWS on a shared basis across many AWS accounts. You normally do not interact with this CMK.
  - **AWS Managed CMK** — Used as the default CMK within most of the AWS services and named under the AWS service name (aws/<service-name>). You are not able to manage or change its configurations (Key Policies, Rotation)
  - **AWS owned CMK** — You are able to create your own CMK. You are allowed to rotate keys, key policies can be defined and can be enabled / disabled. Customer Managed CMKs are regional specific and if you want to use in another region you need to use a different CMK in the target region.
  
# AWS Web Application Firewall:
  AWS Web Application Firewall also popularly know as AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits and bots.
  You have the authority to create security rules to control the traffic flow reacing your web application. You can deploy AWS WAF on Amazon CloudFront as part of your CDN solution, the Application Load Balancer that fronts your web servers or origin servers running on EC2, Amazon API Gateway for your REST APIs, or AWS AppSync for your GraphQL APIs.
  
  ## Benefits of AWS WAF:
  1. Agile protection against web attacks
  2. Save time with managed rules
  3. Improved web traffic visibility
  4. Ease of deployment & maintenance
  5. Easily monitor, block, or rate-limit bots
  6. Security integrated with how you develop applications
  
 ## How it works:
  
  ![working](https://user-images.githubusercontent.com/71292230/190488317-94d88c86-5547-4018-a33a-07f89c70a754.png)

# AWS Guard Duty:
  Amazon GuardDuty is a threat detection service that continuously monitors your AWS accounts and workloads for malicious activity and delivers detailed security findings for visibility and remediation.
  It Continuously monitor your AWS accounts, instances, container workloads, users, and storage for potential threats.
  It expose threats quickly using anomaly detection, machine learning, behavioral modeling, and threat intelligence feeds from AWS and leading third-parties, 
  and mitigate threats early by initiating automated responses.
  
 ## Working of AWS Guard-Duty:
  
  ![image](https://user-images.githubusercontent.com/71292230/190488794-f8351048-84be-4320-8e64-a31897e4385d.png)

Following image illustrates the architecture to use Amazon GuardDuty and AWS Web Application Firewall to automatically block suspicious hosts:
  
  ![image](https://user-images.githubusercontent.com/71292230/190489502-a23350c0-991b-44f9-8989-f98424f8f3c5.png)
