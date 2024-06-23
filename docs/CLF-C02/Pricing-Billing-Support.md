# Pricing, Billing, and Support

**Total Cost of Ownership**: Not only the cost of running workload, but also the associated costs of maintaining infrastructure.

## Optimizing the Cost of Compute

Auto Scaling

Reserved Instances: sign on 1 or 3 years contract.

### Three Reserved Instance (RI) Types:

1. **Standard RI**: Reserve capacity of a particular instance type for a significantly discounted hourly rate.
1. **Convertible RI**: Reserve capacity but retain flexibility on what instance types to use, resulting in a smaller overall discount.
1. **Scheduled RI**: Reserve a particular instance type. But only during defined time windows, resulting in a moderate discount.

## Spot Instances

**Spot instances** are available at a discount rate, but only when AWS has a huge surplus in available compute power. Workloads on spot instances may start or stop at unpredictable times.

Discounts can be up to 90%.

## Compute Optimizer

**Compute Optimizer** analyzes your CloudWatch logs and gives you recommendations on how to right-size your instances.

## Fully Embracing On-Demand

**AWS Lambda** has no idle cost and is great for serverless or event-driven workloads, or workloads with really unpredictable patterns in demand.

**AWS Fargate** is similar to **AWS Lambda**, but specifically for containerized workloads. (Kubernetes or ECS) 

## AWS Price List API

Allows to query the price of AWS services. 
1.  Query using JSON or HTML 
1. Receive price alerts when prices change 

## Optimize the cost of Storage

Infrequently accessed storage classes (**Glacier Instant Retrieval**, **S3 Standard-IA**, **S3 One Zone-IA**, **Glacier Flexible Retrieval** and **Glacier Deep Archive**) tends to be billed per gigabyte of data retrieved.

**Glacier Flexible Retrieval** and **Glacier Deep Archive**. Highly durable, and quite inexpensive for object storage. It can take hours and up to a day to retrieve objects stored with these storage classes.

### S3 Lifecycle Configuration

Create per-object policies that define transition actions and expiration actions, to allow you to move the object from one storage class to another to help you optimize costs. 

### S3 Intelligent Tiering

For cost savings on unknown access frequencies, use the **S3 Intelligent Tiering** storage class. This constantly analyzes the access patterns of your objects and move your objects between two different storage access tiers: frequent access and infrequent access.

### S3 Storage Lens

**S3 Storage Lens** can examine all the S3 buckets across your organization wide, and give you recommendations about storage class changes you can make across all of your accounts. 

| Feature | S3 Intelligent-Tiering | S3 Storage Lens |
|-- |-- |-- |
| Primary Purpose | Optimize storage costs automatically based on access patterns | Provide visibility and insights into storage usage and activity |
| Key Functionality | Moves data between access tiers based on access frequency | Offers metrics, dashboards, and recommendations for storage usage |
| Cost Optimization | Automatic cost savings by tiering storage | Identifies cost-saving opportunities via insights and recommendations |
| Metrics & Monitoring | Limited to monitoring access patterns for tiering | Comprehensive metrics and analytics for storage usage |
| Customization | None, automatic process | Customizable dashboards and reports |
| Use Case | Unpredictable or changing access patterns | Monitoring, analyzing, and optimizing storage usage |

## Understanding Data Transfer Cost

Inbound data transfer from the internet to AWS is always free.

### Types of Data Transfer

1. Public Internet
   * Outbound to the public internet is the most expensive type of data transfer on AWS. 
   * Tends to be about 10 cents per gigabyte, with discounts as you transfer more and more data.
   * In free tier, first 100 gigabytes of outbound data transfer is free.
1. Within On Region
   * Data transfer costs within one region tends to be very cheap, and can be free depending on the situation.
   * Data transfer between an EC2 and RDS is free when they are within a single **Availability Zone**.
1. Across Regions
   * Second most expensive data transfer is between regions.
   * Inter-Region data transfer is billed per gigabyte depending on the origin and destination.


## Monitoring and Predicting Costs on AWS

There are four stages in monitoring and Predicting costs on AWS.

### Assess your potential cloud costs

**Pricing Calculator**: allows you to assess your potential cloud costs. You provide your services and configurations, **Pricing Calculator** produces a **Cost Estimate Breakdown**. 

It is available to anyone. 

### Set up cost safety nets before you start to build

**Budgets**: allows you to set ***customized budgets*** and receive **SNS** alerts when you exceed your thresholds. You can also define automated ***cost saving responses*** and create ***reports***.

### Project and monitor actual cloud cost

**Cost Explorer** is a dynamic dashboard where you can ***gain insights*** on your AWS ***usage and projected spend***. ***Filter costs*** by attributes such as service or region. Create ***custom visual reports*** and drill down for ***detailed analysis***.

### Analyze historical cost data

**Cost and Usage Reports** give you the most detailed data on your cost and usage history. ***Generate reports***, store them in S3, and analyze them to gain insights on ***per-resource*** cost data.

## Managing Costs in a Multi-Account Environment

### AWS Organizations

**AWS Organizations** provide consolidated billing. Monitor costs across your organization from a single account, and take advantage of bulk discounts.

### Billing Conductor

**Billing Conductor** allows you to create ***billing groups*** within your **AWS Organization**. Distribute bulk discounts across billing groups and set custom pricing rates.

## Monitoring the Cost of Resource Groups

### Tags

1. **Tags** can be used to group resources in all kind of different ways.
1. **Tags** are key-value pairs that can apply to almost any resource on AWS.
1. Resources can be tagged by environment, by project name, by the application they're associated with.
1. **Tags** can help in monitoring costs.

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

[[Back to Table of Content](README.md)]