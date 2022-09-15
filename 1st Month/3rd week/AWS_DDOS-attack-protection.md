# Distributed Denial of Service (DDoS) attack:

   ![image](https://user-images.githubusercontent.com/71292230/190482937-ad9c63ab-618f-49ad-85e9-36feca9b408c.png)
  
  A Distributed Denial of Service (DDoS) attack is a malicious attempt to make a targeted system, such as a website or application, unavailable to end-users. To achieve this, attackers use a variety of techniques that consume network or other resources, interrupting access for legitimate end-users.
  DDoS attacks can be segregated by layer of the OSI model they attack. They are most commonly found at the Network (layer 3), Transport (Layer 4), Presentation (Layer 6) and Application (Layer 7) Layers.
  OSI model is given as: 
  
  ![OSI Model](https://user-images.githubusercontent.com/71292230/190476823-909db103-508e-407b-a445-1daa537f1ee3.png)
  
  ## DDOS Attack Classification:
  1. **Infrastructure Layer Attacks:**
      
      These are Layer 3 and 4 attacks. Most common and easily detectable attacks as they have clear signs.  These attacks are large in volume and aimed at overloading the network. These attacks include **vectors like synchronized (SYN) floods** and **User Datagram Packet (UDP) floods** etc. e in volume and aim to overload the capacity of the network or the application servers. But fortunately, these are also the type of attacks that have clear signatures and are easier to detect.
  
  2. **Application Layer Attacks:**
      
      These are Layer 6 and 7 attacks. Less common, more sophisticated, small in volume and aimed to target particular expensive parts of the application. Example of these attacks are flood of HTTP requests to a login page, an expensive search API, or Wordpress XML-RPC floods(Wordpress pingback attacks).
      
  ## Protection Techniques:
  1. **Reduce Attack Surface Area:**
      
     Most common ways of protection against DDOS attacks is by minimizing the attack surface area so a limited or no area is left unprotected. This can be done by moving computational resources behind Content Distribution Networks (CDNs) or Load Balancers and restricting direct traffic, firewalls or Access Control Lists (ACLs) can also be used to control the traffic.
  
  2. **Plan for Scale:**
    
   - Bandwidth (or transit) capacity:
      Plan for ample redundant internet connectivity while architecting the application, allowing to handle large amount of internet traffic. Employing Content Distribution Networks (CDNs) and smart DNS resolution services, provide web applications with an additional layer of network infrastructure for serving content and resolving DNS queries. 
    
   - server capacity:
      Most DDoS attacks are volumetric attacks so add a provision for scaling up and down resources according to traffic. Load Balancers can also be used for monitoring and shifting loads between resources to prevent overloading any one resource
