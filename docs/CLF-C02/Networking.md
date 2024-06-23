# Networking

## Amazon Virtual Private Cloud (VPC)

**VPC** is a foundational service that allows to create a secure private network in the AWS cloud where you launch your resources. It includes the arrangement of workstations or subnets, access rules or **Security Groups** and connections to the outside world, like **Internet Gateways**.

**VPC** has subnets, which further segments VPC, allowing to organize the resources and add layers of security.

**Public subnet**: resources here can be accessed from the internet.

**Private subnet**: not directly accessible from the outside world.

**Internet gateway**: the conduit for traffic between VPC and the internet; responsible for routing outgoing requests and incoming traffic; 

**Route table**: have entries (routes) that determine where network traffic from the subnets should go; each subnet must be associated with a route table.

## Security group

1. **Security groups** make decisions about who can enter and exit. Operating at the instance level, **security groups** are like virtual firewalls that control inbound and outbound traffic for each instance.
1. **Security groups** allow to specify allowable protocols, ports, and source or destination IP ranges.
1. **Security groups** are stateful. This means if they allow traffic in one direction, the return traffic is automatically allowed regardless of the inbound rules.

## Network Access Control Lists (NACLs)

1. **NACLs** is a set of rules defined for controlling network traffic and reducing network attacks. ACLs are used to filter traffic based on the set of rules defined for the incoming or outgoing of the network. 
1. **NACLs** operate at the subnet level and provide a layer of defense for all instances within the subnet.
1. **NACLs** are stateless, which means they don't remember previous interactions. Inbound and outbound rules must be set separately to control the traffic entering and leaving the subnet.
1. **NACLs** can allow or deny traffic based on protocol, port, and source/destination IP addresses.

**VPC Peering**: allows to connect 2 VPC together.

## Domain Name System (DNS)

Amazon Route 53 is AWS DNS service. It also provides domain name registration and health checking web services.

### Route 53 Features

1. Sophisticated Traffic Routing (**Traffic flow**)
   * Geolocation routing, latency-based routing, and weighted round-robin routing.
1. Health Checks:
   * Performs health checks on your resources.
1. DNS Failover
   * Automatically redirect users to a secondary location.
1. Scalability ad integration
   * Scales automatically with your demand.
   * Integrates seamlessly with other AWS services.

### Practical Uses

1. Web application routing
1. Load Balancing
1. Global Traffic Management
1. Domain Name Registration and Management
1. Private DNS for Amazon VPC

## AWS Direct Connect

**AWS Direct Connect** provides a direct, private connection from on-premise data center to AWS, bypassing the public internet. This dedicated lane ensures faster and more reliable data transfer.

Not encrypted by default.

### Benefit of Using AWS Direct Connect

1. High-speed Data Transfer
   * Ideal for transferring large volumes of data quickly and consistently. This high-speed transfer is particularly advantageous for applications involving frequent large-scale data migrations, disaster recovery, or real-time data feeds.
1. Reduced Bandwidth Costs
   * Most cost-effective for extensive data transfer compared to internet-based transfers; especially if you're consistently moving large amounts of data to and from AWS.
1. Reliable Connection
   * Free from public internet disruptions. The private nature of the connection also means enhanced security for your sensitive data.

## AWS VPN

**AWS VPN** transports data safely on public internet. It encrypts your data, safeguarding it as it travels over the internet to AWS. 

### Two types of AWS VPNs

1. Site-to-Site VPN
   * Secure connection between your data center or branch office and your AWS.
   * Ideal for connecting entire networks.
1. Client VPN
   * Secure access to your AWS resources or your private network from any location.
   * Designed for individual remote access.

## VPN vs Direct Connect

| Direct Connect | VPN |
|-- |-- |
| Large-scale data transfer | Encrypted over public internet |
| Consistent performance | Cost-effective |
| Sensitive Data | Quick and easy setup, for temporary |

## Content Delivery and Networking (CDN)

### Amazon CloudFront

**Amazon CloudFront** caches your content in multiple data centers known as **edge locations**.

### AWS Global Accelerator

A networking service that sends your user traffic through AWS's global network infrastructure, enhancing your application's performance and availability.

Global Accelerator uses edge locations to find an optimal pathway to the nearest regional endpoint.

Built in DDoS protection, and automatic failover capabilities.

#### Benefits of AWS Global Accelerator

1. **Improved Performance**: Increase throughput by up to 60%.
1. **Simplified Traffic Management**: Users can access application endpoints through static IP addresses. This simplifies the way managing traffic across regions, optimizing for performance and costs without the need for complex DNS configurations.
1. **Security and Reliability**: DDoS resiliency, Automatic Reroute.
1. **Consistent Global User Experience**: Intelligent routing sends user traffic to the endpoint that provides the best performance.

**AWS Global Accelerator** is useful for business with a worldwide audience, like a streaming service, or an international online retailer.

---

[[Back to Table of Content](README.md)]