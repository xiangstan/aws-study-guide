# AWS Practitioner (*CLF-C02*)

**Compute services**: EC2
**Storage services**: S3
**Networking services**: VPC
**Database services**: RDS
**Developer tools**: Code Family
**Migration services**: Migration Hub
**Machine learning services**: Rekognition
**Auditing services**: Trusted Advisor
**Security services**: IAM
**Pricing services**: PRicing Calculator

## CapEx vx. OpEx

**Capital Expenditures**: Capital expenditures are upfront purchases toward fixed assets.
**Operating Expenses**: Operating expenses are funds used to run day-to-day-operations.

## Advantages to Cloud Computing

1. **Go global in minutes**: You can deploy your applications around the world at the click of a button.
1. **No data centers spend**: You can focus on building your applications instead of managing hardware.
1. **Economies of scale**: Volume discounts are passed on to you, which provides lower pay-as-you-go prices.
1. **Speed and agility**: The provided services allow you to innovate more quickly and deliver your applications faster.
1. **Stop guessing capacity**: Your capacity is matched exactly to your demand.
1. **Trade capital expense for variable expense**: You pay for what you use instead of making huge upfront investments.

## Benefits of Cloud Computing

1. **High Availability**: Highly available systems are designed to operate continuously without failure for a long time. These systems avoid loss of service by reducing or managing failures.
1. **Elasticity**: With elasticity, you don't have to plan ahead of time how much capacity you need. You can provision only what you need, and then grow and shrink based on demand.
1. **Agility**: The cloud gives you increased agility. All the services you have access to help you innovate faster, giving you speed to market.
1. **Durability**: Durability is all about long-term data protection. This means your data will remain intact without corruption.

## Cloud Computing Models

1. **Infrastructure as a Service**: EC2, web hosting.
1. **Software as a Service**: Complete application, email provider.
1. **Platform as a Service**: Develop software using web-based tools without worrying about the underlying infrastructure, Cloud9, Storefront website.

## Cloud Deployment Models

1. **Private cloud**: On-premises, exists in your internal data center.
1. **Public cloud**: Offered by AWS, no physical hardware.
1. **Hybrid cloud**: Combination of public and private cloud, Direct connect.

## Availability Zone (AZ)

One or more discrete data centers with redundant power, networking, and connectivity in an AWS Region.

### Characteristics

1. Physical separated
1. Connect through low-latency links
1. Fault tolerant
1. Allows for high availability

## Edge Locations

Mini data center cache content for fast delivery to your users (CloudFront). Edge location uses AWS back bone network, caching data.

## Local Zones

Run applications on AWS infrastructure closer to your end users and workloads. Local zones are extensions of Regions providing millisecond latency for things like real-time gaming.

## Cloud Adoption Framework

Cloud adoption framework focuses on using AWS to digitally transform, and accelerate business outcomes.

### Perspectives and Foundational Capabilities

#### Security

1. Security
   1. Governance
   1. Assurance
   1. Application
1. Protection
   1. Infrastructure
   1. Data
1. Management
   1. Identity and Access
   1. Vulnerability
1. Incident Response
1. Threat Detection

#### Business

1. Management
   1. Strategy
   1. Portfolio
   1. Innovation
   1. Product
1. Data
   1. Data Monetization
   1. Data Science
1. Business Insight

#### Platform

1. Architecture and Engineering
   1. Platform
   1. Data
1. Continuous Integration/Continuous Delivery (CI/CD)
1. Modern Application Development
1. Provisioning and Orchestration

#### Operations

1. Management
   1. Event (AIOps)
   1. Incident and Problem
   1. Change and Release
   1. Performance and Capacity
   1. Configuration
   1. Patch
   1. Availability and Continuity
   1. Application
1. Observability

#### Governance

1. Management
   1. Program and Project Benefits
   1. Risk
   1. CloudFinancial
   1. Application Profile
1. Data
   1. Governance
   1. Curation

#### People

1. Transformation
   1. Leadership
   1. Workforce
1. Organization
   1. Design
   1. Alignment
1. Cloud Fluency
1. Change Acceleration
1. Culture Evolution

### Cloud Transformation Domains

| Domains | |
|-- |-- |
| Technology | Migrate and modernize |
| Process | Digitize, automate, and optimize |
| Organization | Reimagine orchestration |
| Product | Reimagine your business model |

### Cloud Transformation Journey

| Phases | |
|-- |-- |
| Envision | Benefits to business outcomes |
| Align | Gaps across perspectives |
| Launch | Deliver initiatives with value |
| Scale | Expand sustainable initiatives |

![Cloud Transformation Journey](img/cloud-transformation-journey.png)

## Well-Architected Framework

AWS Well-Architected helps cloud architects build secure, high-performing, resilient, and efficient infrastructure for a variety of applications and workloads. Built around six pillars.

### Operational Excellence

1. Plan for and anticipate failure.
1. Deploy smaller, reversible changes.
1. Script operations as code.
1. Learning from failure and refine.

Use AWS **CodeCommit** for version control to enable tracking of code changes and to version-control **CloudFormation** templates of your infrastructure.

### Security

Focus on protection of data, systems, and any assets used y your workload.

1. Automate security tasks.
1. Encrypt data in transit and at rest.
1. Assign only the least privileges required.
1. Track who did what and when.
1. Ensure security at all applications layers.

Configure central logging of all actions performed in your account using **CloudTrail**.

### Reliability

Focuses on architecting a workload to be consistent and able to recover quickly.

1. Recover from failure automatically.
1. Scale horizontally for resilience.
1. Stop guessing capacity.
1. Manage change through automation.
1. Test recovery procedures.

Use Multi-AZ deployments for enhanced availability and reliability of **RDS** databases.

### Performance Efficiency

Focuses on the ability to use computing resources efficiently to meet requirements.

1. Use serverless architectures first.
1. Use multi-region deployments.
1. Delegate tasks to a cloud vendor.
1. Experiment with virtual resources.

Use AWS **Lambda** to run code with zero administration.

### Cost Optimization

Focuses on the ongoing process of maintaining costs in the cloud.

1. Utilize consumption-based pricing.
1. Implement cloud financial management.
1. Measure overall efficiency.
1. Pay only for resources your application requires.

Use **S3** Intelligent-Tiering to automatically more your data between access tiers based on your usage patterns.

### Sustainability

Focuses on environmental impacts like energy efficiency and consumption.

1. Understand your impact.
1. Establish sustainability goals.
1. Maximize utilization.
1. Use Managed services.
1. Reduce downstream impact.

User **EC2** auto scaling to ensure you are maximizing utilization.

## Networking

### Amazon Virtual Private Cloud (VPC)

**VPC** is a foundational service that allows to create a secure private network in the AWS cloud where you launch your resources. It includes the arrangement of workstations or subnets, access rules or **Security Groups** and connections to the outside world, like **Internet Gateways**.

**VPC** has subnets, which further segments VPC, allowing to organize the resources and add layers of security.

**Public subnet**: resources here can be accessed from the internet.

**Private subnet**: not directly accessible from the outside world.

**Internet gateway**: the conduit for traffic between VPC and the internet; responsible for routing outgoing requests and incoming traffic; 

**Route table**: have entries (routes) that determine where network traffic from the subnets should go; each subnet must be associated with a route table.

### Security group

1. **Security groups** make decisions about who can enter and exit. Operating at the instance level, **security groups** are like virtual firewalls that control inbound and outbound traffic for each instance.
1. **Security groups** allow to specify allowable protocols, ports, and source or destination IP ranges.
1. **Security groups** are stateful. This means if they allow traffic in one direction, the return traffic is automatically allowed regardless of the inbound rules.

### Network Access Control Lists (NACLs)

1. **NACLs** is a set of rules defined for controlling network traffic and reducing network attacks. ACLs are used to filter traffic based on the set of rules defined for the incoming or outgoing of the network. 
1. **NACLs** operate at the subnet level and provide a layer of defense for all instances within the subnet.
1. **NACLs** are stateless, which means they don't remember previous interactions. Inbound and outbound rules must be set separately to control the traffic entering and leaving the subnet.
1. **NACLs** can allow or deny traffic based on protocol, port, and source/destination IP addresses.

**VPC Peering**: allows to connect 2 VPC together.

### Domain Name System (DNS)

Amazon Route 53 is AWS DNS service. It also provides domain name registration and health checking web services.

#### Route 53 Features

1. Sophisticated Traffic Routing (**Traffic flow**)
   * Geolocation routing, latency-based routing, and weighted round-robin routing.
1. Health Checks:
   * Performs health checks on your resources.
1. DNS Failover
   * Automatically redirect users to a secondary location.
1. Scalability ad integration
   * Scales automatically with your demand.
   * Integrates seamlessly with other AWS services.

#### Practical Uses

1. Web application routing
1. Load Balancing
1. Global Traffic Management
1. Domain Name Registration and Management
1. Private DNS for Amazon VPC

### AWS Direct Connect

**AWS Direct Connect** provides a direct, private connection from on-premise data center to AWS, bypassing the public internet. This dedicated lane ensures faster and more reliable data transfer.

Not encrypted by default.

#### Benefit of Using AWS Direct Connect

1. High-speed Data Transfer
   * Ideal for transferring large volumes of data quickly and consistently. This high-speed transfer is particularly advantageous for applications involving frequent large-scale data migrations, disaster recovery, or real-time data feeds.
1. Reduced Bandwidth Costs
   * Most cost-effective for extensive data transfer compared to internet-based transfers; especially if you're consistently moving large amounts of data to and from AWS.
1. Reliable Connection
   * Free from public internet disruptions. The private nature of the connection also means enhanced security for your sensitive data.

### AWS VPN

**AWS VPN** transports data safely on public internet. It encrypts your data, safeguarding it as it travels over the internet to AWS. 

#### Two types of AWS VPNs

1. Site-to-Site VPN
   * Secure connection between your data center or branch office and your AWS.
   * Ideal for connecting entire networks.
1. Client VPN
   * Secure access to your AWS resources or your private network from any location.
   * Designed for individual remote access.

### VPN vs Direct Connect

| Direct Connect | VPN |
|-- |-- |
| Large-scale data transfer | Encrypted over public internet |
| Consistent performance | Cost-effective |
| Sensitive Data | Quick and easy setup, for temporary |

### Content Delivery and Networking (CDN)

#### Amazon CloudFront

**Amazon CloudFront** caches your content in multiple data centers known as **edge locations**.

#### AWS Global Accelerator

A networking service that sends your user traffic through AWS's global network infrastructure, enhancing your application's performance and availability.

Global Accelerator uses edge locations to find an optimal pathway to the nearest regional endpoint.

Built in DDoS protection, and automatic failover capabilities.

##### Benefits of AWS Global Accelerator

1. **Improved Performance**: Increase throughput by up to 60%.
1. **Simplified Traffic Management**: Users can access application endpoints through static IP addresses. This simplifies the way managing traffic across regions, optimizing for performance and costs without the need for complex DNS configurations.
1. **Security and Reliability**: DDoS resiliency, Automatic Reroute.
1. **Consistent Global User Experience**: Intelligent routing sends user traffic to the endpoint that provides the best performance.

**AWS Global Accelerator** is useful for business with a worldwide audience, like a streaming service, or an international online retailer.






## Support Plans

There are 4 support plans.

### Basic Support Plan

Include for free for all AWS accounts.

1. Account and billing.
1. Service limit increases.
1. 24/7 access via email only.

### Developer Support Plan

Support starts at $29 a month and it is recommended for testing and development.

1. Account and billing.
1. Service limit increases.
1. Technical support.
1. 1 Primary Contact.
1. Unlimited cases.
1. Cloud Support Associate: Business-hours access via email only.
1. Response Times: <24 hours general guidance. <12 hours system impaired.

### Business Support Plan

Support start at $100 a month and it is recommended for production workloads.

1. Account and billing.
1. Service limit increases.
1. Technical support.
1. Unlimited contacts, unlimited cases, full set of **Trusted Advisor** checks.
1. Cloud Support Associate: 24/7 access via email only, phone, or chat.
1. Response Times: <24 hours general guidance. <12 hours system impaired, <4 hours production system impaired, <1 hour production system down.

### Enterprise Support Plan

Support starts at $15,000 a month and it is recommended for business or mission-critical production workloads.

1. Account and billing.
1. Service limit increases.
1. Technical support.
1. Unlimited contacts, unlimited cases, full set of **Trusted Advisor** checks, **Technical Account Manager** (TAM), **Concierge Support Teams**, **Infrastructure Event Management**.
1. Cloud Support Associate: 24/7 access via email only, phone, or chat.
1. Response Times: <24 hours general guidance. <12 hours system impaired, <4 hours production system impaired, <1 hour production system down, <15 minutes business-critical system down.

### Support Case Types
1. Account and billing: Account-related and billing cases can be opened by all customers (free).
1. Service limit increases: Default service quota (or limit) increases can be opened by all customers. Essential the guardrail that AWS places on your account so that you don't end up with a huge bill.
1. Technical support: Can only be opened by customers on the Developer, Business or Enterprise plans.

AWS Support does not allow cases for code development, debugging custom software, or performing system administration tasks.




---

## Exam question breakdown

| Category | Percentage |
|--- |--- |
| Cloud Concepts | 24% |
| Security and Compliance | 30% |
| Cloud Technology and Services | 34% |
| Billing, Pricing, and Support | 12% |





---

Goto [Main Content](../README.md)