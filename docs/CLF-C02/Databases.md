# Databases

## Types of AWS Databases

1. <u>Relational Databases</u>: 
   1. Stores and provide access to data that is organized into rows and columns, like a table.
   1. Useful for E-Commerce, Mobile Backends, Healthcare Applications.
   1. AWS Services: **Amazon Relational Database** (**RDS**)
1. <u>NoSQL Databases</u>: 
   1. In NoSQL databases, key value pairs allow for a flexible and intuitive way to store and retrieve data.
   1. AWS Services: **DynamoDB**
1. <u>In-memory Databases</u>: 
   1. Store data in the computer's main memory or RAM, instead of slower disk-based storage, so that they can read and write data much faster than traditional databases.
   1. AWS Services: **ElastiCache**, **MemoryDB** for Redis.
1. <u>Graph Databases</u>:
   1. A graph database is a type of NoSQL database that uses a graph structure to represent data relationships. It's designed to store data that has complex connections and relationships, and is useful for representing connected data.
   1. Fraud detection, recommendation systems, drug discovery.
   1. AWS Services: **Neptune**

## AWS Database Migration Services (DMS)

A managed migration and replication service that helps move your database and analytics workloads to AWS quickly, securely, and with minimal downtime and zero data loss. AWS DMS supports migration between 20-plus database and analytics engines, such as Oracle to Amazon **Aurora** MySQL-Compatible Edition, MySQL to **RDS** for MySQL, Microsoft SQL Server to Amazon **Aurora** PostgreSQL-Compatible Edition, MongoDB to Amazon **DocumentDB** (with MongoDB compatibility), Oracle to Amazon **Redshift**, and Amazon **Simple Storage Service** (S3).

1. <u>Simple to Use</u>: No drivers or changes to the source database needed.
1. <u>Minimal Downtime</u>: Continuously replicate data during migration, keeping the source database operational. 
1. <u>Reliable</u>: Self-healing with constant monitoring.
1. <u>Database Consolidation</u>: Consolidate multiple databases into one.

### AWS Schema Conversion Tool (SCT)

A powerful tool that helps convert the database schema of your source database into a format compatible with AWS target databases.

1. Exam the existing database architecture, then create a new schema for your target AWS database. Also transforming the database code, including stored procedures, functions, and views to be AWS compatible.
1. Identify and address issues like incompatible data types or features unsupported in the target database. 

### DMS Use Cases

1. Migrating Between Database Platforms
1. Consolidating Multiple Databases into a Single Database
1. Continuous Data Replication
1. Migration Data to the Cloud for Analytics
1. Data Center Decommission

## Relational Database Service (RDS) 

A service that makes it easy to launch and manage relational databases. 

1. Supports popular database engines: Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle, MSFT SQL Server 
1. Offers high availability and fault tolerance using Multi-AZ deployment option. 
1. AWS manages the database with automatic software patching, automated backups, operating system maintenance, and more. 
1. Launch read replicas across regions in order to provide enhanced performance and durability. 

## Amazon Aurora 

Relational database compatible with MySQL and PostgreSQL that was created by AWS. 

1. Supports MySQL and PostgreSQL database engines. 
1. 5x faster than normal MySQL and 3x faster than normal PostgreSQL. 
1. Scales automatically while providing durability and high availability. 
1. Managed by RDS. 


## Amazon DynamoDB

A fully managed NoSQL database service.

### Key Features

1. <u>Performance at Scale</u>: Maintains consistent, single-digit millisecond response times.
1. <u>Fully Managed</u>: No server management or maintenance required.
1. <u>Built-in Security</u>: Data is encrypted at rest and in transit.
1. <u>Backup and Restore</u>: Supports on-demand and continuous backups.

### Use Cases

1. Web and Mobile Applications
1. Gaming Applications
1. IoT Applications
1. E-Commerce Platforms

## Amazon DocumentDB 

Fully managed document database that supports MongoDB. 

1. Document database 
1. MongoDB compatible
1. Fully managed and serverless
1. Non-relational

## Amazon ElastiCache

Fully managed in-memory datastore compatible with Redis or Memcached. 

1. In-memory datastore
1. Compatible with Redis or Memcached engines
1. Data can be lost

Offers high performance and low latency.

## Amazon MemoryDB for Redis

Memory-based databases store data in RAM instead of traditional storage. This allows much faster retrieval and processing, essential for applications requiring real-time access.

***Redis*** is an open source in-memory data store.

### Key Features

1. <u>Performance</u>: Delivers data with ultra-fast response times. Can handle more than 13 trillion requests per day; and peaks of 160 million requests per second.
1. <u>Data Durability</u>: Automatically replicates data across multiple AWS Availability Zones.

### Use Cases

1. Caching for Web Applications
1. Real-Time Analytics
1. Session Store for Applications
1. Leaderboards and Gaming
1. Geospatial Data Processing

## Amazon Neptune 

Fully managed graph database that supports highly connected datasets. 

1. Graph database service
1. Supports highly connected datasets like social media networks
1. Fully managed and serverless
1. Fast and reliable
