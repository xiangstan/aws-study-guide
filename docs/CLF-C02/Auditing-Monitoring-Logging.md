# Auditing, Monitoring, Logging, and Additional Technology and Services

## Metrics, logs and configurations

1. Metrics: Numerical representations of things like capacity and demands, tracked over time.
1. Logs: A record of what has happened, to make sense of errors or security events.
1. Configurations: Settings and guidelines across all of your cloud resources.

## Collecting Metrics

1. AWS services can publish metrics
1. Metrics help monitor workload health
1. Metrics inform design decisions
1. Common Examples:
   1. Lambda invocations or errors
   1. **EC2** CPU utilization
   1. **RDS** read latency
   1. Custom application metrics

## Log Producers

1. Metrics are derived from logs
1. Logs track actions on your infrastructure
1. Common Examples
   1. **VPC** flow logs
   1. **EC2** instance logs
   1. Account activity logs
   1. Application logs

## Configuration

1. Configurations are resource settings or standards.
1. Types and properties of resources can be standard across your AWS environment.
1. Seek guidance and enforce best practices with AWS services.

## Configuration Management

1. Configurations require monitoring
   1. Standardizing configurations requires both prevention and detection.
1. Automate Configurations at Scale
   1. Leveraging AWS services to automate enforcement and auditing of configurations.

## Well-Architected Framework

| Six Pillars | |
|--- |--- |
| **Security** | Tracking actions across your resources is integral to security on AWS. |
| **Cost Optimization** | Understanding the utilization of your provisioned resources through metrics is key to cost optimization. |
| **Performance Efficiency** | Metrics can help you ensure your workloads are fast and responsive. |
| **Operational Excellence** | Auditing configurations and collecting appropriate logs and metrics contribute to operational excellence. |
| **Reliability** | Visibility into the uptime and performance of your workloads is integral to reliability. |
| **Sustainability** | Metrics can help you more closely track your carbon footprint on AWS. |

## CloudWatch

1. Gives visibility to cloud resources and applications
1. Tracks metrics in dashboards
1. Stores logs from many sources
1. Trigger events with **CloudWatch** alarms
1. Lets you watch your cloud resources as your AWS ecosystem evolves

### CloudWatch Agent

1. For **EC2**, application and some instance metrics can't be collected unless you install the **CloudWatch** Agent on the instance.
1. Metrics Requiring **CloudWatch** Agent:
   1. Free Memory
   1. Percentage of Disc Space Used
   1. Custom Application Metrics
   1. Many more!

## CloudTrail

1. Provides accountability for actions taken in your account
1. Centralizes activity logs across regions in an **S3** bucket
1. Tracks only API activity in your AWS account
1. Creates a trail of breadcrumbs for any action in your account

### CloudWatch Dashboard

Amazon **CloudWatch** dashboards are customizable home pages in the CloudWatch console that you can use to monitor your resources in a single view, even those resources that are spread across different Regions. You can use **CloudWatch** dashboards to create customized views of the metrics and alarms for your AWS resources.

With dashboards, you can create the following:

1. A single view for selected metrics and alarms to help you assess the health of your resources and applications across one or more Regions. You can select the color used for each metric on each graph, so that you can easily track the same metric across multiple graphs.
1. An operational playbook that provides guidance for team members during operational events about how to respond to specific incidents.
1. A common view of critical resource and application measurements that can be shared by team members for faster communication flow during operational events.

## Manage Resources on AWS

### Tags

**Tags** are key/value pairs that you can apply to pretty much any cloud resource.

1. Give readable names
1. Define which project or environment belong to

### Systems Manager

1. Group resources on AWS, on premises, or on other cloud platforms
1. Take automated actions on resource groups
1. View aggregated operational data of resource groups
1. Systems Manager Parameter Store can securely store sensitive data:
   1. Passwords
   1. Database strings
   1. License keys

## Monitoring Service Health

| Tools | Description |
|--- |--- |
| **AWS Health Dashboard** | View the status of services and regions relevant to the workloads running in your AWS account |
| **AWS Health API** | Leverage the AWS Health API if you are building a custom observability application |

## Trusted Advisor

A one-stop shop for best practice advice. It can advise on performance, cost optimization, service limits, fault tolerance, operational excellence, and security.

### Free Trusted Advisor Checks

1. Do you have any open security groups?
1. Are you using **IAM** Users?
1. Do you have MFA enabled on your root user?
1. Are you getting close to any service limits?
1. Do you have any public **RDS** snapshots?
1. Do you have any public **EBS** volume snapshots?
1. Do you have any **S3** Bucket permissions that allow open access?

## Auditing on AWS

On AWS, Auditing is a continuous process. 

1. It is the continuous act of monitoring passive configurations for security and best practices.
1. Sometimes this is done against a set of standards to achieve industry-specific compliance.
1. Trust Advisor

### What types of things to audit?

1. Data Encryption
1. Secure CloudTrail
1. Public Access
1. Resource Provisioning
1. Network Security
1. Protect Credentials

### Config

**Trust Advisor** and other auditing tools on AWS primarily use one service, and that service is AWS **Config**. **Config** is the backbone of configuration auditing on AWS.

1. Leverages pre-defined recommendations or create custom rules.
1. Detects non-compliant resources and alert administrators in the console.
1. Dost not enforce standards, but audits adherence.

### Audit Manager

1. Centralize audit data from AWS Config and security services.
1. Find root causes of noncompliance and generate reports.
1. Provide pro-built auditing frameworks to meet industry standards:
   * HIPAA
   * NIST Cybersecurity
   * AWS Operational Best Practices
   * Many more, and custom ones

### The Well-Architected Tool

The AWS **Well-Architected Tool** access your workloads, learn about best practices, and generate action plans.

## Identifying Business and End User Services

### Amazon Connect

A cloud-based contact center.

Allow you to create a call center in the cloud, and this can be a distributed call center with agents and managers and cases tracked all around the globe.

### Amazon WorkSpaces

Virtual Desktop Environment for remote employees.

### Amazon AppStream

Host and manage an application in the cloud that can be accessed through a web browser. Converts applications to ***software-as-a-service*** for employees or end users.

---

[[Back to Table of Content](README.md)]