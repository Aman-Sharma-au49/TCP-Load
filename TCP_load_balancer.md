# TCP Load Balancer   
A TCP Load Balancer uses transmission control protocol (TCP), which verifies information sent to internet protocol (IP) addresses. It ensures the data arrives error-free to non-HTTP applications. 

![alt text](image-1.png)

## Load Balancing 
In the world of computers and networks, load balancing is a similar idea. When you have a website or an application that many people want to access, load balancing helps distribute the incoming requests (like people wanting to see your website) evenly among multiple servers. This ensures that no single server is overloaded, leading to faster response times and a smoother experience for users.  

![alt text](image-2.png)  

## Load Balancing Algorithms 
Different load balancing algorithms provide different benefits; the choice of load balancing method depends on your needs:   
* Round Robin – Requests are distributed across the group of servers sequentially.   

* IP Hash – The IP address of the client is used to determine which server receives the request.  

* Least Connections – A new request is sent to the server with the fewest current connections to clients. The relative computing capacity of each server is factored into determining which one has the least connections.  

* Least Response Time – Sends requests to the server selected by a formula that combines the fastest response time and fewest active connections. Exclusive to NGINX Plus.    

* Least BandWidth – A load balancing virtual server configured to use the least bandwidth method selects the service that is currently serving the least amount of traffic, measured in megabits per second (Mbps). The following example shows how the virtual server selects a service for load balancing by using the least bandwidth method.   

![alt text](image-3.png)

# Benefits of Load Balancing   
**Reduced downtime** :-   
Load balancing distributes network traffic across multiple servers. In the event of a server failure or maintenance, the load balancer redirects traffic to healthy servers. This minimizes downtime, ensuring continuous availability of services and reducing the impact of potential disruptions.   

**Scalable**:-   
Load balancing allows for easy scalability as it can dynamically distribute incoming traffic among additional servers. This scalability is essential for handling increased demand, accommodating growth, and ensuring that the system can adapt to varying workloads without a significant drop in performance. 

**Redundancy** :-  
Load balancers provide redundancy by distributing traffic across multiple servers. If one server fails, the load balancer redirects traffic to other functioning servers, preventing a single point of failure. This redundancy enhances system reliability and minimizes the risk of service interruptions. 

**Flexibility** :-   
Load balancing offers flexibility in managing and adapting to changing network conditions. It can dynamically adjust the distribution of traffic based on server health, current load, and other parameters. This adaptability is crucial for optimizing resource utilization and maintaining consistent performance.
**Efficiency** :-   
Load balancing optimizes resource utilization by evenly distributing traffic across servers. This prevents individual servers from becoming overloaded while others remain underutilized. Efficient resource allocation ensures that the available capacity is maximized, contributing to cost-effectiveness and optimal system performance. 

# Various cloud-based balancers 

**Network Load Balancing** :-   
Network load balancing, as its name suggests, leverages network layer information to decide where to send network traffic. This is accomplished through layer 4 load balancing, which is designed to handle all forms of TCP/UDP traffic. Network load balancing is considered the fastest of all the load balancing solutions, but it tends to fall short when it comes to balancing the distribution of traffic across servers. 

**HTTP Load Balancing** :-   
HTTP(S) load balancing is one of the oldest forms of load balancing. This form of load balancing relies on layer 7, which means it operates in the application layer. HTTP load balancing is often dubbed the most flexible type of load balancing because it allows you to form distribution decisions based on any information that comes with an HTTP address. 

**Internal Load Balancing** :-   
Internal load balancing is nearly identical to network load balancing but can be leveraged to balance internal infrastructure. 

When talking about types of load balancers, it’s also important to note there are hardware load balancers, software load balancers, and virtual load balancers.

**Hardware Load Balancer** :-   
A hardware load balancer, as the name implies, relies on physical, on-premises hardware to distribute application and network traffic. These devices can handle a large volume of traffic but often carry a hefty price tag and are fairly limited in terms of flexibility. 
**Software Load Balancer** :-   
A software load balancer comes in two forms—commercial or open-source—and must be installed prior to use. Like cloud-based balancers, these tend to be more affordable than hardware solutions. 
**Virtual Load Balancer** :-   
A virtual load balancer differs from software load balancers because it deploys the software of a hardware load balancing device on a virtual machine. 

# What is a Network Load Balancer? 

Network Load Balancers use variables such as destination ports and IP addresses to distribute traffic. They function on OSI Layer 4, so they are not intended to be context-aware or to consider cues at the application layer such as cookie data, content type, user location, custom headers, or application behavior. Network Load Balancers consider only the network-layer information contained inside the packets they direct.   

## Network Load Balancers offer the following benefits: 
Ability to scale to millions of requests per second to handle volatile workloads   

Support for static IP addresses   

Ability to assign one elastic IP address per enabled subnet
Support registering targets including those outside the VPC by IP address   

Support routing requests on a single EC2 instance to multiple applications and registering each IP address or instance using multiple ports with the same target group   

Support independent monitoring of service health, with health checks defined at the target group level and many metrics reported there. 

![alt text](image-4.png)
# What Is a TCP Load Balancer? 
A TCP load balancer is a type of load balancer that uses transmission control protocol (TCP), which operates at layer 4 — the transport layer — in the open systems interconnection (OSI) model. TCP traffic communicates at an intermediate level between an application program and the internet protocol (IP). A TCP load balancing configuration provides a reliable and error-checked stream of packets to IP addresses, which can otherwise easily be lost or corrupted. Each application is assigned a unique TCP port number to enable delivery to the correct application and to provide health checks.

# How Does a TCP Load Balancer Work? 
TCP load balancers are for applications that do not use HTTP. When deployed in front of a database cluster, a TCP load balancer spreads requests across all available server configurations. Any application data destined for a server is forwarded to the available server over a new TCP connection. Separating (or proxying) the client to server connections allows for enhanced security, such as TCP protocol sanitization or DoS mitigation. It also provides better server performance and client connections.   

# Types of TCP Load Balancers: 
* **Software Load Balancers** :-   
Implemented as software on general-purpose servers. Examples include Nginx, HAProxy, and Apache Traffic Server. 
* **Hardware Load Balancers**:-   
Dedicated hardware appliances designed specifically for load balancing, such as those provided by F5 Networks and Citrix NetScaler. 
* **Cloud Load Balancers**  
:- Services offered by cloud providers (e.g., AWS Elastic Load Balancer, Google Cloud Load Balancer).
