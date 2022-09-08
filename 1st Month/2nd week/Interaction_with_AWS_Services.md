# Interaction with AWS Services:
  AWS provides many ways to interact with its services, which include:
  1. AWS Console
  2. AWS CLI
  3. AWS SDK's
  4. Cloudformation 


Many beginners find AWS console to be easy and user friendly so it is one of the primary method for interacting with the platform. We will discuss these methods one-by-one.

## AWS Console:
  A web based GUI, providing the ability to interact with the AWS services. We could use the console to launch, view, modify and remove any instance.
  As we login to the AWS portal we are provided with a simple and user friendly GUI from which we can search and use any service that we like.
  Prominent feature of AWS Console:
  - Easy to use and user friendly
  - displays recently used services
  - can easily pin most used services
  - easy selection of AWS region
  - Account information can be viewed easily
  - Easy approach to AWS documentation via accessible links

AWS console looks something like this:

![AWS Console](https://adamraffe.com/img/2018/07/aws-console.png)

## AWS CLI:
  Many have found AWS console to be a bit limiting in terms of speed and repeatability. So a more efficient way of interacting with the AWS services is using the command line interface the AWS CLI.
  CLI alows us to manage the AWS environment using a terminal rather than a graphical interface, which is more quicker and easier. We can also create a script that contains all the commands to interact with different sercvices, So a single script can perform multiple actions.
  All AWS CLI commands start with **aws** keyword 
  Examples of some of the uses of AWS CLI are as following:
  - List all S3 buskets in the account
  `aws s3 ls`
  - List all the EC2 instances
  `aws ec2 describe-instances`
  - Run a new EC2 instance using a specific Amazon Machine Image (AMI), t2.micro instance size and a key pair named MainKey.
  `aws ec2 run-instances --count 1 --image-id ami-a36f8dc4 --instance-type t2.micro --key-name MainKey`
  
## AWS SDK's:
  AWS provides a number of Software Development Kits (SDKs) that allows interaction with the platform via code.
  SDKs are available for all the major programming languages, including:
  - Java 
  - Python
  - Node.JS
  - Go.

![Modular AWS SDK for JavaScript](https://d2908q01vomqb2.cloudfront.net/0716d9708d321ffb6a00818614779e779925365c/2020/10/23/sdk-overview-v3.png)

## Cloudformation:
  It is a tool used to define ** *Infrastructure as Code* **. Cloudformation is the way to go if we want to define the desired infrastructure within AWS, quickly and in a repeatable manner.
  A single script using a descriptive language, defined locally and uploaded to AWS can provision all the AWS services required. The platform then reads the script and provisions the services and features that you have defined in the CloudFormatiom script.
  The main advantages of Cloudformations are:
  - Infrastructure defined as code
  - Extremely flexible and powerful

![AWS Cloudformation](https://blog.shikisoft.com/assets/images/post_imgs/20181105/aws-cloudformation-index.jpg)
 
Resources: [Interacting with AWS](https://adamraffe.com/2019/02/20/aws-fundamentals-part-3-interacting-with-aws/)
   
