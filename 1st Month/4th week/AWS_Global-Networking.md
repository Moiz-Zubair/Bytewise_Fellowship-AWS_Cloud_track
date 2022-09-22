# Global Network:
  The global infrastructure of AWS is designed with performance as a primary design factor. AWS has the largest global capital asset of any cloud provider, and this impact is continually growing to support customers in delivering better end-user experiences, expanding operations quickly to almost any region or nation, and satisfying their requirements for data locality and sovereignty. 
  To provide the greatest possible customer experience, a company that wants to service its consumers in Europe should allow them to chose from a wide range of European cities or data centres, such as Paris, London, Frankfurt, or Dublin.
  
  ### AWS Global Infrastructure:
  ![image](https://user-images.githubusercontent.com/71292230/191831017-fcd358f1-c5ae-40fb-a381-aba0dda3b783.png)
  
  ## Benefits:
  - **High Performance**:
    Eighty(80) Availability zones all around the globe provide high performace computing at a very fast pace. Each AZ consisits of multiple data centers and provide multiple hundreds of servers to provide fast and high performance.
    
  - **Flexible, Global Footprint**:
    AZs are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZs so it provides a global poot frint and multiple AZ's can give necessary computational resources.
    
# Subnets and Network Access Control list:
  ## Network Access Control List (ACL):
   It allows or denies specific inbound or outbound traffic at the subnet level. Default network ACL or a custom created network ACL (with rules for security groups in order to add an additional layer of security) can be used for VPN.
   Network ACL can generally be founded in the firewall router or in a router connecting two internal networks.
   The following diagram shows a VPC with two subnets. Each subnet has a network ACL. When traffic enters the VPC (for example, from a peered VPCs, VPN connection, or the internet), the router sends the traffic to its destination.
   
   ![image](https://user-images.githubusercontent.com/71292230/191830770-41934943-cc4b-45f6-bc64-b87faa93ae21.png)

   
   ## Network ACL Basics
   - Network ACL comes by default after the creation of a VPC
   - Without addition of rules all inbound and outbound traffic is denied by the customly created network ACL.
   - One Subnet can only be connected to a single ACL, but one ACL can be connected to multiple subnet's.
   - Inbound and outbound rules that can allow or deny traffic, these rules numbered are from 1 to 32766.
   - Network ACLs are stateless, which means that responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa).

  ## Network ACL rules:
  The following are the parts of a network ACL rule:
  - **Rule number**: Evaluated starting with lowest numbered rule and numbered from 1 to 32766.
  - **Type**: The type of traffic; for example, SSH.
  - **Protocol**: Specify any protocol that has a standard protocol number.
  - **Port range**: The listening port or port range for the traffic. For example, 80 for HTTP traffic.
  - **Source**: [Inbound rules only] The source of the traffic (CIDR range).
  - **Destination**: [Outbound rules only] The destination for the traffic (CIDR range).
  - **Allow/Deny**: Whether to allow or deny the specified traffic.

  ## Ephemeral ports:
  Ephemeral ports may also be used for continuation of communications with a client that initially connected to one of the services listening with a well-known port.
  The example network ACL in the preceding section uses an ephemeral port range of 32768-65535. However, you might want to use a different range for your network ACLs depending on the type of client that you're using or with which you're communicating.
  The client that initiates the request chooses the ephemeral port range. The range varies depending on the client's operating system.
  
  - Many Linux kernels (including the Amazon Linux kernel) use ports 32768-61000.
  - Requests originating from Elastic Load Balancing use ports 1024-65535.
  - Windows operating systems through Windows Server 2003 use ports 1025-5000.
  - Windows Server 2008 and later versions use ports 49152-65535.
  - A NAT gateway uses ports 1024-65535.
  - AWS Lambda functions use ports 1024-65535.
  
  
