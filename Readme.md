# AWS Certified Cloud Practitioner


## 1. Danh sách các dịch vụ cơ bản của AWS


------------------------------
### EC2: Virtual machine


1. Types:
   1. <span style="color:yellow">**General purose**</span> instances: <span style="color:red">**balance**</span> of computer, memory, and network resources.
   2. <span style="color:yellow">**Compute optimized**</span> instances: <span style="color:red">**high-performance processors**</span>.
   3. <span style="color:yellow">**Memory optimized**</span> instances: are designed to deliver fast performance for workloads that process <span style="color:red">**large datasets in memory**</span>.
   4. <span style="color:yellow">**Accelerated computing**</span> instances: use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs. Examples of these functions include <span style="color:red">**floating-point number calculations, graphics processing, and data pattern matching**</span>.
   5. <span style="color:yellow">**Storage optimized**</span> instances: are designed for workloads that require high, sequential read and write access to <span style="color:red">**large datasets on local storage**</span>.

2. Pricing:
   1. <span style="color:Orange ">**On-Demand**</span> instances: <span style="color:Pink">for short-term and you pay for only the compute time you use</span>.
   2. <span style="color:Orange ">**Savings Plans**</span> instances: enable you to reduce your compute costs by <span style="color:Pink">**committing to a consistent amount of compute usage for a 1-year or 3-year term**</span>. Savings of up to 66% over On-Demand costs.
   3. <span style="color:Orange ">**Reserved**</span> instances: <span style="color:Pink">cam kết 1 hoặc 3 năm, sẽ ưu đãi tới 75% các dịch vụ đám mây AWS. Các doanh nghiệp quan tâm đến chi phí hạ tầng đám mây thường sử dụng cách này</span>.
   4. <span style="color:Orange ">**Spot**</span> instances: <span style="color:Pink">are available at up to a 90% discount compared to On-Demand prices. Terminate after 2 minute alert</span>.
   5. <span style="color:Orange ">**Dedicated Hosts**</span> : <span style="color:Pink">physical servers with Amazon EC2 instance capacity that is fully dedicated to your use</span>. 



### S3: Simple Storage Service



1. Classes:
   1. <span style="color:yellow">**S3 Standard** :</span> **high durability, availability, and performance** object storage for frequently accessed data. [**General purpose**]
   2. <span style="color:yellow">**S3 Intelligent-Tiering** :</span> automatically reduces your storage costs on a granular object level by automatically moving data to the most cost-effective access tier based on access frequency.[**Unknown or changing access**]
   3. Infrequent access [Truy cập không thường xuyên]
      1. <span style="color:pink">**S3 Standard-IA**</span>: S3 Standard-Infrequent Access => data that is accessed less frequently, but requires rapid access when needed. [Truy cập không thường xuyên tuy nhiên truy cập nhanh]
      2. <span style="color:Orange">**S3 One Zone-Infrequent Access**</span>: Same Standard-IA, but stores data in a single zone and costs 20% less than S3 Standard-IA.
   4. Glacier [Sông băng]
      1. <span style="color:pink">**Glacier Instant Retrieval**</span>: can save up to 68% on storage costs compared to using the S3 Standard-Infrequent Access (S3 Standard-IA) storage class, **when your data is accessed once per quarter**.
      2. <span style="color:green">**S3 Glacier Flexible Retrieval** (S3 Glacier) </span>: up to 10% lower cost (than S3 Glacier Instant Retrieval), for archive **data that is accessed 1—2 times per year and is retrieved asynchronously**.
      3. <span style="color:red">**S3 Glacier Deep Archive**</span> : is Amazon S3’s lowest-cost storage class designed for long-term retention of data that will be retained for 7-10 years. Retrieval time within 12 hours.
      4. S3 Outposts: Amazon S3 on Outposts delivers object storage to your on-premises AWS Outposts environment.
   


### Database & Storage


1. Storage
   1. Amazon Elastic Block Store (Amazon EBS): temporary block-level storage for an Amazon EC2 instance.
   2. EBS snapshot is an incremental backup.
   3. Amazone EFS (file storage): is ideal for use cases in which a large number of services and resources need to access the same data at the same time.
   4. EBS volume stores data in **a single available zone** and **multiple available zones** for Amazon EFS.
2. Database
   1. <span style="color:pink">**Amazon RDS** [Relational Database Service]</span> : service that enables you to run **relational databases** in the AWS Cloud.
   2. <span style="color:green">**Amazon Aurora** </span>: enterprise-class relational database. It is **compatible with MySQL and PostgreSQL relational databases**.
   3. <span style="color:Orange">**Amazon DynamicDB** </span>: a nonrelational database.
   4. <span style="color:red">**Amazon Redshift**</span> : is a data warehousing service.
   5. **Amazon DocumentDB** : is a document database service that supports MongoDB workloads.
   6. **Amazon ElastiCache** : is a service that adds caching layers on top of your databases to help improve the read times of common requests. 
   7. **Amazon DynamoDB Accelerator** (DAX): is an in-memory cache for DynamoDB.
   8. **Amazon Neptune**: Amazon Neptune is a graph database service.


### Infrastructure & Networking


1. Infrastructure
   1. Amazon CloudFront: CDN with edge location.
   2. AWS Elastic Beanstalk: is an easy-to-use service for deploying and scaling web applications and services on familiar servers such as Apache, Nginx, Passenger, and IIS.
   3. AWS CloudFormation: lets you model, provision, and manage AWS and third-party resources by treating infrastructure as code.
2. Networking
   1. Amazon VPC: Virtual Private Cloud enables you to provision an isolated section of the AWS Cloud.
   2. Subnet: is a section of a VPC that can contain resources such as Amazon EC2 instances.
   
   ![alt text](./resources/Q_HnMl_BAEsDZGxf_NEblbQjD0vn0-pPU.png "VPC")

   3. Virtual private gateway: enables you to establish a virtual private network (VPN) connection between your VPC and a private network, such as an on-premises data center or internal corporate network.
   4. AWS Direct Connect: service that enables you to establish a dedicated private connection between your data center and a VPC. 
   5. **Stateless and allows** all inbound and outbound traffic.
   6. **stateful and deny**.
   7. Amazon Route 53: DNS web service.



### Responsibility & Security



1. Responsibility
   1. AWS responsibilities: **AWS operates, manages, and controls the components at all layers of infrastructure**.
      1. Physical security
      2. Hardware and software infrastructure
      3. Network infrastructure
      4. Virtualization infrastructure
   2. Customer responsibilities: remaining.

   ![alt text](./resources/sIlyltjk4kwKozZ1_eyqltDSWURM2V1xC.png "Responsibility")



2. Security
   1. IAM (AWS Identity and Access Management): enables you to manage access to AWS services and resources securely.
      1. IAM users: is an identity that you create in AWS
      2. IAM policies: is a document that allows or denies permissions to AWS services and resources.
      3. IAM groups: is a collection of IAM users.
      4. IAM roles: is an identity that you can assume to gain temporary access to permissions.
   2. Organizations
      1. AWS Organizations: Suppose that your company has multiple AWS accounts.
      2. SCPs (service control policies): enable you to place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access.




### Other
   1. AWS DMS (AWS Database Migration Service) enables you to migrate relational databases, nonrelational databases, and other types of data stores.
   2. Amazon SNS (Amazon Simple Notification Service): is queue.