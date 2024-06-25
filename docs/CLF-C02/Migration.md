# Migration and Transfer Technology and Services

## Snow Family

**Snow Family** are physical devices design to securely and efficiently transfer large amounts of data (>10TB) to AWS.

Typically use these devices when your network bandwidth cannot handle an online migration efficiently.

| Snow Family | |
|--- |--- |
| Snowcone | Small and portable, military grade 8 TB HDD or 14 TB SSD storage. Weighs under 5 lbs |
| Snowball | >= 10 TB of data to migrate |
| Snowball Edge | >= 10 TB of data to migrate and you need local compute |
| Snowmobile |  >= 10 PB of data to migrate |

## AWS Database Migration Service (AWS DMS)

**AWS DMS** is used to migrate databases and analytics workloads to AWS. Workloads may be on-premises, on **8EC2**, or in **RDS**.

**AWS Schema Conversion Tool** (AWS SCT) can converts from one database schema to another.

| From | To |
|--- |--- |
| MySQL | RDS for MySQL |
| SQL Server | Aurora for PostgreSQL |
| MongoDB | DocumentDB |
| Oracle | RedShift |

## AWS Transfer Family

Business-to-business file transfer using protocols like SFTP, AS2, FTPS and FTP. Files are transferred into and out of AWS storage like **Simple Storage Service** (S3) or **Shared File Storage** (EFS).

| Protocols | |
|--- |--- |
| SFTP | SSH File Transfer Protocol. Uses SSH security and authentication. |
| AS2 | Applicability Statement 2, uses HTTP/HTTPS. |
| FTPS | File Transfer Protocol over SSL. Uses industry standard TLS to encrypt traffic. |
| FTP | File Transfer PRotocol, clear text, no encryption. Not recommended! |

## AWS DataSync

1. Allows for online data transfer from on-premises to AWS storage services like S2, EFS, or FSx. 
1. Migrates a large amount of data with high data throughput.
1. Avoid human error by automation.
1. Support NFS, SMB shared file systems, object stores.
1. Pay-per-GB transfer.

### Use Cases

1. Securely migrate data over to AWS. 
1. Cost effectively replicate data your data using AWS storage. 
1. Archive historical data to low cost AWS storage.
1. Support hybrid or multi-cloud workflows.

## AWS Application Discovery Service

**Application Discovery Service** discovers you application servers and databases. A discovery tool gathers data about your existing setup. The data is collected and sent over to AWS over an encrypted connection; and stored in AWS **Migration Hub**.

### It collects the following with Application Discovery Agent

1. Server inventory
1. Configuration data
1. Operating system version
1. Capacity utilization
1. InBound and outbound network connections

A virtual appliance can be deployed on VMware vCenter system to avoid using an agent.

## AWS Application Migration Service

Automated Lift-and-Shift.

1. Migration from VMware vCenter or Physical servers to AWS
1. From other Cloud Providers
1. Between AWS regions or between AWS accounts.

### How does it work?

1. Install the AWS replication agent on each application server that you want to migrate.
1. The **Application Migration Service** performs continuous replication of the source servers to the destination servers in AWS.

The traffic is encrypted to keep all data private. The system can be used normally while the replication process is running.

**Application Migration Service** is free from any cost in 90 days.

## AWS Migration Hub

1. A central location to gather application and server inventory information
1. Enables you to assess, plan, and track migrations to AWS.
1. Logically group servers together for migration.
1. A central place to manage the migration of applications and data into AWS.

**AWS Migration Hub** integrate with **Application Discovery Service**, **Application Migration Service**, and **Database Migration Service**. It also makes recommendations about modernizing applications.

