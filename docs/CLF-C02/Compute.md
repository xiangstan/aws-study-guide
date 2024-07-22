# Compute Technology and Services

Compute is used to describe concepts and services geared towards computation and processing. 

## Elastic Compute Cloud (EC2) 

**EC2** is a foundational service that you use to manage your virtual instances.

Allows you to rent and manage virtual servers in the cloud. 

### Elastic compute power 

***Elastic*** - can grow or shrink like a rubber band based on the needs or the load of the application. 

### Amazon Machine Image (AMI) 

1. Deploy a database 
1. Deploy a web application 

### EC2 Families of Instances

**EC2** offers six families of instances that re broken up into types, generations, and sizes.

1. General Purpose
1. Compute Optimized
1. Memory Optimized
1. Accelerated Computing
1. Storage Optimized
1. high Performance Computing (HPC) Optimized

### Pricing

| Type | Description | Use When | Capacity Reservations |
|--- |--- |--- |--- |
| **On-Demand** | Fixed price billed by the second | <ol><li>Low costs, no upfront payments or commitments</li><li>Cannot interrupt unpredictable workloads</li><li>Developing applications</li></ol> | hold capacity whether or not you run an instance |
| **Spot Instances** | Take advantage of unused EC2 capacity. | <ol><li>Not concerned with start or stop times</li><li>Can interrupt workload</li><li>Very low compute prices are needed</li><li>Cheapest option</li></ol> | Pay the price in effect at the beginning of the hour and save up to 90% off of On-Demand prices |
| **Dedicated Hosts** | Pay for a physical server that is fully dedicated to running your instances. | <ol><li>Bring your own server-bound software license like Microsoft or Oracle</li><li>Regulatory or corporate compliance requirements around tenancy</li></ol> | Up to 70% off On-Demand prices, No sharing your server with other customers. |
| **Reserved Instances** | Commit to a SPECIFIC instance type for 1 to 3 years. | <ol><li>Steady state usage and can commit</li><li>Pay money upfront</li><li>Application requires a capacity reservation</li></ol> | <ol><li>Up to 72% off of On-Demand prices with a CONTRACT. Reserve capacity in an AZ for any duration.</li><li>Pay all, partial or no upfront, but All Upfront offers the highest discount.</li><li>Convert instance types at 66% discount.</ol> |
| **Savings Plans** | Commit to compute usage for 1 to 3 years (measured per hour). | <ol><li>Lower your bill across multiple compute services.</li><li>Flexibility to change compute services, instance types, operating systems, or Regions.</li></ol> | <ol><li>72% off On-Demand prices.</li><li>Share savings across compute services.</li><li>No Capacity reservations.</li></ol> |

### Load Balancing

Automatically distribute incoming traffic across multiple healthy **EC2** instances.

| Load Balancing Types | |
|--- |--- |
| **Classic** | <ul><li>EC2-Classic network</li><li>Layer 4/7</li><li>Uses TCP, SSL/TLS, HTTP/HTTPS</li><li>Most of time, utilize other type of load balance</li></ul> |
| **Gateway** | <ul><li>Use for network logging and monitoring with third-party virtual appliances</li><li>Layer 3/4</li><li>Only has IP listener</li></ul> |
| **Application** | <ul><li>Flexible application management</li><li>Layer 7</li><li>HTTP/HTTPS, gRPC</li></ul> |
| **Network** | <ul><li>Extreme performance and static IP addresses</li><li>Layer 4</li><li>TCP/UDP, TLS</li></ul>

### Auto Scaling

**Auto Scaling** adds or replaces **EC2** instances automatically across AZs.

| Types of **Auto Scaling** | |
|--- |--- |
| Horizontal | Scaling out: reduce the impact of system failure and improve the availability of the application as it uses multiple AZ; it adds or remove instances |
| Vertical | Scaling up: upgrade **EC2** instances by adding more power, CPU and RAM |

### AWS Compute Optimizer

1. Help to right size compute instances 
1. Provide recommendations to improve performance
1. Streamline migration to AWS Graviton CPUs 

### Connect to EC2

1. AWS Management Console
1. EC2 Instance Connect (EIC)
1. Secure Shell (SSH) and Remote Desktop Protocol (RDP)
1. AWS System Manager (via web browser or CLI)

## Containers

### Benefits

1. Portability
1. Operational consistency
1. Efficiency
1. Application development
1. Less overhead

### Use Cases

1. Lift and shifts
1. Refactoring applications
1. Support for microservice architecture
1. Support for CI/CD deployments
1. Easier deployment of repetitive tasks.

### Amazon Elastic Container Registry (ECR)

Use the register to store, share and deploy container software. 

### Amazon Elastic Container Service (ECS)

1. Container orchestration services
1. Fully managed and serverless using Fargate
1. Can run with **EC2**, **Fargate**, **Outposts**, or **ECS Anywhere**
1. Supports ***Docker*** and Docker compose CLI

### Amazon Elastic Kubernetes Service (EKS)

1. Fully managed open-source system
1. Can run with **EC2**, **Fargate**, **EKS on Outposts**, "Local Zones**, **Wavelength**," or **EKS Anywhere**
1. Supports ***Kubernetes***

## Serverless Services

***Serverless*** is a cloud native development model that allows developers to build or run applications without having to manage servers.

Pretend the servers don't exists since someone else manages servers that builds or runs your applications.

## AWS Lambda

Serverless compute server that lets you run code without managing servers.

***Code*** your write is called a function. Language like `Python`, `Rust`, and `Ruby`, etc..

**Lambda** scales automatically.

### When to use **Lambda**

1. Real-Time File Processing
1. Send Email notifications
1. Backend business logic

### Pricing

1. Number of requests
1. Starts at invocation
1. Duration rounded up to 1 ms
1. ALWAYS FREE TIER, 1 million free request per month

## Fargate

**Fargate** is a pay-as-you-go auto-scaling compute engine. **Fargate** tasks do not share any underlying kernels, CPU, or memory resources or elastic network interfaces, with any other tasks, which provides isolation by design.

1. Build or select your container image, and define memory and compute resources
1. Run and manage containers that are launched using the image and resources specified.

### When to use **Fargate**

1. Message-drive workloads
1. Event-drive workloads
1. Need process to run longer than 15 minutes, use **Fargate** instead of **Lambda**

### Pricing

1. No upfront costs
1. PAy for resources used vCPU, memory, and storage
1. No FREE TIER

## Additional Compute Services

### Outposts

Allow you to run cloud services in your internal data center, meaning on-premises. Support hybrid workloads that need to remain on-premises due to latency or data sovereignty needs.

1. Outposts Rack
1. Outposts Servers

### Lightsail

Allow you to quickly launch all the resources you need for small projects, WordPress websites or small test environments. 

1. Launch small projects
1. Provide a simple UI
1. Bundle server monitoring, SSD-based storage, DNS management, one-click RDP and SSH access and a static IP address
1. Provide low, predictable monthly fees

### Batch

Allow you to process large workloads into smaller chunks or batches. Typically used for longer running jobs.

### Wavelength

Deliver ultra-low latency applications for devices using 5G networking (mobile networks).

---

[[Back to Table of Content](README.md)]