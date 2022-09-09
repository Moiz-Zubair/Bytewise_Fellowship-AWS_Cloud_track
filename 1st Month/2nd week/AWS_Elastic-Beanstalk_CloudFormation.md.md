# AWS Elastic Beanstalk:
  Elastic Beanstalk is an easy-to-use service for deploying and scaling web applicationa and services developed in Java, node php and similar languages on familiar servers Apache, Nginx or IIS.
Just upload the code, then Elastic Beastalk automatically handles the deployment. It handles  load balancing, capacity provisioning, auto-scaling and monitoring. 
We retain full control over the AWS resources powering the application and can access the underlying resources at any time.
Benefits of using Elastic Beanstalk are as following:
  
  
  **1. Fast and simple to begin:** 
      Easiest and fastest way to deploy application on AWS. You only provide the application code via git repo or an integrated IDE (eclipse/visual studio), the elastic beanstalk handles all the deployment and monitoring of the application. 
  Without setting up the infrastructure or configuration the application is ready for usage within minutes. 
  
  
  **2. Developer productivity:**
      Developer does not need to configure or manage the infrastructure or the under-lying architecture and is only concerned about the developemnt or the code of the application, which increases the developer productivity. 
      
  **3. Impossible to outgrow:**
      It automatically scales the application up or down according to the need or utilization whcih can be changed easily via adjustable Auto Scaling settings. It easily handles the workload while keeping the costs minimum. 
  
  **4. Complete resource control:**
      User have the complete control over the resources taht he/she wants to use. TheEC2 intance type is optional for the user to select and can easily take over some/all of the elements of your infrastructure by using Elastic Beanstalk's management capabilities.
      
#### Introduction to AWS Elastic Beanstalk:

https://user-images.githubusercontent.com/71292230/189417282-16e50680-c552-4401-b701-67d2f6805612.mp4  

# AWS Cloud Formation:
  It is a service that helps modelling and setting up AWS resources so that a developer can spend less time managing those resources and focus more on the applications. A template is created describing all the resources needed (like Amazon EC2 instances or Amazon RDS DB instances), 
  and CloudFormation takes care of provisioning and configuration. CloudFormation helps in following ways:
  
### 1. Simplify infrastructure management:
   Cloud Formation simplifies the overall infrastructure management. We only need to make a cloudformation template that has details of all the resources and their properties, this template is then converted into a stack
   that make all the resources available and running, and when we are done with the resources we can simple delete the stack that will automatically delete all the resources within the template.
    
### 2. Quickly replicate your infrastructure: 
   Incase of making your application available in multiple regions we need to replicate our resources and infrastructure within all those regions which require time and effort.
   So a simple solution is to use the same cloud formation template and replicate in the other region without the hasle of configuring multiple resources in the separate region. 

### 3. Easily control and track changes to your infrastructure:
   Cloud Formation templates are simplem text files which can be easily used to track chnges in thee infrastructure. We have complete control over the resources that we want to provision, we just describe the resource and its propertise in the template and within minutes it is ready for use.
   We can use a version control system to track changes in the template and can ealiy revert to the previous template settings.
   
The following image explains the AWS CloudFormation template structure:

![AWS Cloudformation Template](https://www.techielass.com/content/images/size/w1000/2022/04/GMT20220420-072512_Recording_1920x1080.00_00_00_00.Still001.png)
