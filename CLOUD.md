# AWS Cloud Practitioner Notes

---

## Overview of AWS

AWS is the leading public cloud provider, offering a broad set of compute, storage, networking, and managed services.

* **Amazon Founded:** 1994 by Jeff Bezos
* **Current CEO:** Andy Jassy
* **AWS Founded:** 2004
* **CEO of AWS:** Adam Selipsky
* **CTO of AWS:** Werner Vogels

### Four Major Services of AWS (IaaS)

* **Compute:** Virtual computer that can run applications, programs, and code.
* **Networking:** Virtual network defining internet connections or network isolation between services.
* **Storage:** A virtual hard drive that stores files.
* **Databases:** For storing reporting data or a database for general-purpose web apps.

### Core Cloud Services Mapping

| Service | Description |
| --- | --- |
| **EC2** | Virtual compute for running applications |
| **EBS** | Block storage attached to EC2 |
| **RDS** | Managed relational databases |
| **VPC** | Isolated virtual network in the cloud |

---

## Cloud Service Models

* **SaaS (Software as a Service) for Customers:** A product that is run and managed by the service provider.
* **PaaS (Platform as a Service) for Developers:** Focus on the deployment of your apps. No configuring, provisioning, or understanding the hardware/OS.
* **IaaS (Infrastructure as a Service) for Admins:** Provides fundamental infrastructure like compute, storage, and networking, while the customer manages OS and applications.

---

## Deployment Models

* **Public Cloud (Cloud First):** Workloads run entirely on a cloud provider.

 *Path:* Internet → AWS → VPC → Public Subnet
 
 *Example:* Dropbox


* **Private Cloud:** Everything built on on-premise data centers.

  *Path:* Internet → On-premise Data Center → OpenStack → Public Subnet

  *Example:* Canada, AIG


* **Hybrid Cloud:** Combination of both public and private cloud, using both on-premise data centers and CSP.

  *Example:* Deloitte, KPMG


* **Cross Cloud or Multi-Cloud:** Using multiple Cloud Providers (Azure Arc, Anthos of GCP, etc.).

  *Example:* KPMG



> **Case Study: KPMG**
> * KPMG has adopted a **Hybrid Multi-Cloud** deployment model as its primary cloud strategy.
> * Relies heavily on **Microsoft Azure** (KPMG Clara -smart audit platform, Microsoft 365) and **Google Cloud** (AI-driven solutions).
> * The hybrid structure allows control over sensitive data in regulated environments while accessing the scalability of public clouds.
> 


--- 

## Key Management & Monitoring Tools

* **IAM (Identity and Access Management):** Controls authentication and authorization, ensuring least-privilege access to cloud resources.
* **CloudWatch:** Provides monitoring and observability by collecting metrics, logs, and events to track performance and cost.

---

## AWS Pricing Model

AWS follows a **pay-as-you-go** pricing model:where customers pay only for the resources they use.

* Convert Capital Expense (CapEx) into Operational Expense (OpEx).
* Scale up during peak demand; scale down when not needed.
* Avoid over-provisioning.
* Optimize costs using On-Demand, Reserved, or Spot pricing.

---

## Benefits & Advantages

### General Benefits

* Agility, Elasticity, Scalability, Global Reach, Security, Reliability, High Availability, Fault Tolerance, Pay-as-you-go.

### Six Major Advantages

1. Pay on Demand.
2. Sharing the cost with other customers.
3. Scale up or down whenever needed.
4. Focus on your own customers (no hardware maintenance).
5. Go global in minutes.

---

## AWS Global Infrastructure

Globally distributed hardware and data centers are physically networked together. Key terms: **Region, Availability Zones, Fault Tolerance, Fault Domain.**

### Connectivity & Delivery Services

* **Amazon CloudFront:** Content Delivery Network (CDN) that caches content at Edge locations.
* **Amazon S3 Transfer Acceleration:** Uses a special URL to upload files to Edge locations for faster transit to S3.
* **AWS Global Accelerator:** Finds the optimal path from the user to web servers via Edge locations.
* **AWS Direct Connect:** A private, dedicated connection between your data center and AWS.
* **AWS Ground Station:** Managed service to control satellite communications.
* **AWS Outposts:** Brings AWS services/infrastructure to virtually any on-premise data center.

### Availability & Scaling

* **Elastic Load Balancer (ELB):** Evenly distributes traffic to one or more datacenters.
* **Auto Scaling Groups (ASG):** Automatically adds or removes servers based on defined metrics.
* **RDS Multi-AZ:** Backs up data in another Availability Zone for automated recovery.
* **CloudEndure Disaster Recovery:** Rapid migration/recovery (being superseded by AWS DRS).
* **Elastic Beanstalk / Route 53:** Services for app deployment and DNS management.

---

## Cloud Architecture Terminologies

* **Solutions Architect:** Architects technical solutions via research, documentation, and experimentation.
* **Cloud Architect:** A Solutions Architect focused on cloud services.

### Core Architecture Pillars

* **High Availability:** No single point of failure; ensures performance (ELB).
* **High Scalability:** Ability to increase capacity (Vertical/Horizontal scaling).
* **High Elasticity:** Ability to *automatically* scale based on demand (ASG).
* **Highly Fault Tolerant:** Preventing the chance of failure (RDS Multi-AZ).
* **High Durability:** Ability to recover from disaster and prevent data loss.

### Recovery Objectives

* **RTO (Recovery Time Objective):** Maximum acceptable delay for service restoration.
* **RPO (Recovery Point Objective):** Maximum acceptable time since the last data recovery point.

---

## FAQ & Concepts

### 1. What is Cloud Computing?

Cloud computing is the on-demand delivery of  computing resources like servers, storage, databases, and networking over the internet, with a pay-as-you-go pricing model. This helps organizations scale up quickly, reduce infrastructure costs, and focus more on the business values rather than managing hardware.


### 2. Why move to the cloud?

Scalability, cost optimization, reliability, and  faster time to market. Organizations adopt cloud to scale resources based on demand, reduce upfront infrastructure costs, and focus more on the business value rather than managing hardware.

### 3. IaaS vs. PaaS vs. SaaS

* **IaaS:** You manage OS and apps.
* **PaaS:** You focus on deployment; AWS manages OS.
* **SaaS:** Fully managed software for end users.

### 4. What is the Shared Responsibility Model?

In the AWS shared responsibility model, AWS is responsible for the security of the cloud, such as the physical data centers and infrastructure. While customers are responsible for the security in the cloud, including access control, data protection, and application security.

### 5. How does AWS ensure reliability?

AWS ensure reliability through its global infrastructure of regions and availability zones along with services that support redundancy, fault tolerance and automated scaling.
---
## Consultants' Quote:

Technology decisions should align with business goals, risk appetite, and scalability requirements.
---
## Architecture Principles & Patterns

### 5 Core Principles

1. **Scalability:** Horizontal and Vertical.
2. **High Availability:** Multiple AZs and redundancy.
3. **Fault Tolerance:** Recovery without downtime.
4. **Security:** Integrated into planning (IAM, Encryption).
5. **Cost Optimization:** pay-as-you-go, Right-sizing and Auto Scaling.

### Patterns

* **Stateless Architecture:** Applications do not store user state on the servers.
 (improves scalability).
* **Redundancy:** multiple copies of critical components. High availability, disaster recovery.
* **Loose Coupling:** Components are independent and communicate through well-defined interfaces. Easier changes, Better resilience.


---

## Cloud Migration

The process of moving digital assets, like data, applications, and IT resources, from on-premises servers or one cloud to another cloud environment (like AWS, Azure, or Google Cloud) to leverage benefits such as better scalability, cost-optimization, and performance

### The 6 Migration Methods (6 R's)

1. **Rehost:** Lift and shift.
2. **Replatform:** Minor optimizations.
3. **Refactor:** Redesign for cloud.
4. **Repurchase:** Move to SaaS.
5. **Retain:** keep certain applications on-premises.
6. **Retire:** Remove unused apps.

### Design Levels

* **HLD (High-Level Design):** overall system design, scalability, which tools/technologies, and databases to use.
* **LLD (Low-Level Design):** Detailed component behavior, APIs, and algorithms.

---

## Interview Questions & Strategy

* **Cloud Transformation:** Redesigning systems and processes to leverage automation and managed services.
* **DevOps Role:** Enables transformation through automation and CI/CD pipelines.
* **Assessment:** Start by understanding business objectives and auditing workloads for criticality and security.

