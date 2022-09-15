# Amazon Shared Responsibility Model:
  The AWS shared responsibility model defines that a client/user and AWS are responsible for when it comes to security and compliance of the application in AWS.
  Security and Compliance is a shared responsibility between AWS and the customer. This shared model can help relieve customer’s operational burdens as AWS operates, manages and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates.
  The customer assumes responsibility and management of the guest operating system including updates and security patches, other associated application software as well as the configuration of the AWS provided security group firewall.
  
  ## AWS Responsibility:
  AWS are responsible for **“ *Security of the Cloud* ”**.
  
  > AWS is responsible for protecting the infrastructure that runs all of the services offered in the AWS Cloud.

  > This infrastructure is composed of the hardware, software, networking, and facilities that run AWS Cloud services.

  ## Client Responsibility:
  Customers are responsible for **“ *Security in the Cloud* ”**.

  >For EC2 this includes network-level security (NACLs, security groups), operating system patches and updates, IAM user access management, and client and server-side data encryption.

The following figure demonstrates the *Security of the cloud* -> responsibility of AWS and *Security in the cloud* -> responsibility of the client:

![Shared Responsibility Model](https://user-images.githubusercontent.com/71292230/190472463-0273663e-9e95-4892-8eb0-d16705978da8.png)

## Inherited, Shared and Customer Specific Controls:
  1. **Inherited Controls:** Controls that a customer fully inherits from AWS.
    > Physical and Environmental controls.

  2. **Shared Controls:** Controls that apply to both the infrastructure layer and customer layers, but in completely separate contexts or perspectives.
    In the AWS shared security model, a shared control, AWS provides the requirements for the infrastructure and the customer must provide their own control implementation within their use of AWS services. .
    In shared responsibility model, AWS is responsible for the:
    
   - Patch Management: AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications.
   - Configuration Management: AWS maintains the configuration of its infrastructure devices, but a customer is responsible for configuring their own guest operating systems, databases, and applications.
   - Awareness & Training: AWS trains AWS employees, but a customer must train their own employees.

3. **Customer Specific:** Controls are solely the responsibility of the customer based on the application they are deploying within AWS services.
    Examples of customer-specific controls include:
    
    > Service and Communications Protection or Zone Security may require a customer to route or zone data within specific security environments.
