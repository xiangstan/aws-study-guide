# Storage

## Elastic Compute Cloud Storage

### Amazon Elastic Block Store (EBS)

**EBS** provide persistent block storage volumes For **EC2** instances. 

1. Data persists when the instance is not running 
1. Can only attached to one instance in the same availability zone
1. Tie to one availability zone 
1. Direct attached
1. Quickly accessible data 
1. Running a database on an instance 
1. Long-term data storage 

#### Key Features

| Key Features | |
|--- |--- |
| High availability and durability | Suited for EC2 Instances.<br>Ensures data is preserved even if the instance crashes. |
| Scalability | Expands on-the-fly without any downtime. |
| Snapshot | Can take backups and also use these backups to create new volumes. |
| Persistent Storage | Data remains intact after stopping EC2 instance. |
| Encrypted | Data at rest and in transit is secure. |

#### EBS Use Cases

1. Hosting relational or NoSQL databases.
1. Data warehousing and big data analytics.
1. Enterprise Resource Planning (ERP) and Customer Relationship Management (CRM) applications.

#### EBS Volume Types

| SSD | HDD |
|--- |--- |
| Solid State Drive | Hard Disk Drive |
| Faster | Slower |
| More expensive | Less expensive |
| Ideal for high IOPS | Ideal for throughput tasks |

#### SSD Types

| General Purpose SSD | Provisioned IOPS SSD |
|--- |--- |
| gp3, gp2 | io2, io1, io2 block express |
| Low-latency interactive applications | High IOPS |
| 16,000 Max IOPS | 64,000 (io2, io1), 256,000 |
| Multi-attach not supported | Multi-attach supported |

#### HDD Types

| Throughput Optimized HDD volumes | Cold HDD volumes |
|--- |--- |
| st1 | sc1 |
| Big data | Lowest storage cost |
| 500 Max IOPS | 250 |
| 500 MiB/s max throughput | 250 MiB/s max throughput |

#### Snapshots

| Key features | |
|--- |--- |
| Incremental backups | Each snapshot only saves changes since the last one. |
| Restore & Launch | Use snapshots to quickly restore a volume. |
| Share or Sell | Snapshots can be shared with other AWS accounts. |
| Cost-effective | Snapshots only store block-level changes. |
| Cross-region Replication | Snapshots can be copied across AWS regions. |

### Amazon Elastic File System (EFS)

**EFS** is a scalable file storage system for EC2 and other AWS services.

#### Key Features

| Key Features | |
|--- |--- |
| Fully Managed | Removes the complexity of deploying and maintain file systems. |
| Automatic Scaling | Automatically scales on demand without disrupting applications. |
| Concurrent Access | Multiple EC2 instances can access an EFS system simultaneously. |

#### EFS Use Cases

1. Content management and web serving.
1. Data analytics applications.
1. Development and testing environments.

### Instance Stores

An **instance store** is local storage that is physically attached to the host computer and cannot be removed. 
 Unlike EBS, this storage is ephemeral. It's ideal for temporary data.

1. Storage on disks physically attached to an instance 
1. Storage is temporary since data loss occurs when the EC2 instance is stopped 
1. Faster with higher I/O speeds 
1. Temporary storage needs 
1. Data replicated across multiple instance

#### Key Features

| Key Features | |
|--- |--- |
| High I/O Performance | Offers very high input/output operations per second. |
| Temporary Storage | Data is lost if the instance is stopped or terminated. |
| No Extra Cost | They come as part of the instance. |

#### Instance Stores Use Cases

1. Temporary storage of cache and buffers.
1. Write and discard large amounts of data.
1. Storage for application that replicate data across multiple instances.

## Amazon Simple Storage Service (S3)

Amazon **S3** is object storage. It works with AWS Lambda, you can log activities, define alerts and automate workflows without managing additional infrastructure.

**S3** bucket names have to be global unique.

### Benefits of S3

| Benefits | |
|--- |--- |
| Durability | 99.999999999% (11 9s) durability |
| Scalability | Virtually unlimited |
| Security | Bucket policies<br>Access control lists |
| Versatility | Store images, videos, backups and big data |

### Wide range of storage classes

![Chart of S3 Storage Classes](../img/clf-c02-s3-storage-classes.png)

1. S3 Standard
   1. High throughput
   1. Low Latency
1. S3 Intelligent-Tiering
   1. Automatically moves data
   1. Savings
1. S3 Standard-IA
   1. Accessed less frequently
   1. Rapid access
1. S3 One Zone-IA
   1. One Availability zoon.
   1. Cost-effective
1. S3 Glacier Instant Retrieval
   1. Archive storage
   1. Instant retrieval
1. S3 Glacier Flexible Retrieval
   1. Archive storage, retrieve 1 time a year
   1. Not immediate
1. S3 Glacier Deep Archive
   1. Archive Storage
   1. Most cost-effective
   1. Slow, retrieve can take up 12-48 hours

### S3 Lifecycle Policy

**S3 Lifecycle Policy** defines when objects transition to another storage class and when objects expire.

### S3 Storage Class Analysis

Use **S3 Storage Class Analysis** to discover data that should move to a lower cost storage class based on access patterns. Use the data from the analysis to configure an **S3 Lifecycle policy** that makes the data transfer.

### S3 Object Lock

Objects are locked for the duration of the retention period that you define and are protected from deletion.

## FSx

1. **FSx** offers a fully managed Windows File System that's crafted for Windows specific workloads.
1. **FSx** is there for those unique workloads that require native Windows features.

## Elastic Disaster Recovery

1. **Elastic Disaster Recovery** is designed to minimize downtime and data loss, offering swift recovery times. It ensures everything remains operational.
1. Pay only for the servers you are actively replicating to AWS.

## Storage Gateway

| Key Benefits | |
|--- |--- |
| Cost-Effective | Reduces on=premises storage infrastructure |
| Secure | Data encryption for safe transfer and storage |
| Seamless Integration | Integrates with existing applications |

| Types | |
|--- |--- |
| S3 File Gateway | Keep your dta in cloud-native formats |
| Volume Gateway | Provides block storage volumes<br>Offers stored and cache volumes |
| Tape Gateway | For archiving data |
| FSx File Gateway | Extends on-premises file systems |

### Use Cases

1. Data backup
1. Disaster Recovery
1. Data Processing in AWS

## AWS Backup

AWS blocks up resources such as:

1. Elastic Computed Cloud Instances
1. Elastic Block Store Volumes
1. Relational Database Service Databases
1. DynamoDB Tables
1. Elastic File System File Systems
1. FSx File Systems
1. Storage Gateway Volumes

### Core Features

1. **Centralized Backup Management** - Simplifies overseeing backups
1. **Automated Backup Scheduling** - Provides policies you define
1. **Encryption & Compliance** - Keeps data secure
1. **Cross-Region & Account Backup** - Enhances disaster recovery

---

[[Back to Table of Content](README.md)]