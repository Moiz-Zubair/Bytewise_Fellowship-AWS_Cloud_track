# Regions and Zones
  Amazon EC2 is hosted in multiple locations all over the world. These locations are divided into Regions, Availability Zones, Local Zones, AWS Outposts, and Wavelength Zones.
  - Region: Separate geographic area.
  - Availability Zones: Multiple, isolated locations within each Region.
  - Local Zones: Place resources(compute and storage), in multiple locations closer to end users.
  - AWS Outposts: Brings native AWS services, infrastructure, and operating models to virtually any data center.
  - Wavelength Zones: Allows developers to build applications that deliver ultra-low latencies to end users. Wavelength deploys standard AWS compute and storage services to the edge of telecommunication carriers.

## Region:
  Each Region is designed to be isolated from the other Regions. This provides the greatest possible fault tolerance and stability. Different Resouces are tied to a particular region
  This is because Regions are isolated from each other, and don't automatically replicate resources across all Regions.
  When you launch an instance, you must select an **AMI** that's in the same Region. If the AMI is in another Region, you can copy the AMI to the Region you're using.
  
  ![AWS Regions](https://l3snh1odsii3hndbd2rovotm-wpengine.netdna-ssl.com/wp-content/uploads/2017/09/aws_regions_map-1024x580.png)

## Availability Zones:
  Availability zones are highly available data centers within each AWS region. A region represents a separate geographic area. Each availability zone has independent power, cooling and networking. 
  When an entire availability zone goes down, AWS is able to failover workloads to one of the other zones in the same region, a capability known as “Multi-AZ” redundancy.
  Availability zones are highly available data centers within each AWS region. A region represents a separate geographic area. Each availability zone has independent power, cooling and networking. 
  When an entire availability zone goes down, AWS is able to failover workloads to one of the other zones in the same region, a capability known as “Multi-AZ” redundancy.
  
  ![availability zones in regions](https://cloud.netapp.com/hs-fs/hubfs/aws_regions-1.png?width=505&name=aws_regions-1.png)
  
## Local Zones:
   It is an extension of an AWS Region in geographic proximity to your users. Local Zones have their own connections to the internet and support AWS Direct Connect, so that resources created in a Local Zone can serve local users with low-latency communications.
  
  ![AWS Local Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/region-with-lzs.png)
   
## Wavelength Zones:
   A Wavelength Zone is an isolated zone in the carrier location where the Wavelength infrastructure is deployed. Wavelength Zones are tied to a Region. A Wavelength Zone is a logical extension of a Region, and is managed by the control plane in the Region.
  
  ![Wavelength Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/region-with-wavelength-zones.png)
   
## AWS Outposts:
   An Outpost is a pool of AWS compute and storage capacity deployed at a customer site. AWS Outposts is a fully managed service that extends AWS infrastructure, services, APIs, and tools to customers, by providing local access to AWS managed infrastructure.
  
  ![AWS Outposts](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/region-with-outpost.png)
   
   Resources used: [Regions and Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)
