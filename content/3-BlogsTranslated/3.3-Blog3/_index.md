---
title: "Blog 3"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The content below is my own summary and re‑framing of the AWS blog  
**“Reserve your seat: Microsoft workloads on AWS sessions at re:Invent 2024”**.  
It is for reference only – please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

# Reserve your seat: Microsoft workloads on AWS sessions at re:Invent 2024

*Based on the blog by David Pallmann (04 NOV 2024).*

---

## 1. re:Invent 2024 and Microsoft workloads on AWS

AWS re:Invent 2024 is approaching fast, with more than **2,400 sessions** spread across six venues.  
Registered attendees can already log in to the **Attendee Portal** and reserve seats, which is strongly recommended because popular sessions fill up quickly.

This post highlights sessions focused on **Microsoft workloads on AWS**, including:

- Windows Server  
- SQL Server  
- Active Directory  
- .NET and application modernization  

The goal is to help you quickly find the content that will improve how you **migrate, optimize, and modernize** Microsoft-based environments on AWS.

---

## 2. Breakout sessions

Breakout sessions are **45–60 minute lecture-style talks** led by AWS experts, customers, or partners, usually with time for Q&A.

### XNT202 – *The art and culture of modernizing a .NET monolith*

- Story of Tessitura, an arts-and-culture software provider, transforming a 20‑year‑old client‑server .NET system into a modern cloud architecture.  
- Shows how AWS’s **Experience-Based Acceleration (EBA)** helped drive both technical change and organizational culture shifts, and shares lessons for anyone modernizing legacy .NET.

### XNT203 – *Supercharge your SQL Server workloads, featuring Thomson Reuters*

- Explains how Thomson Reuters re‑architected its SQL Server environment on AWS for a mission‑critical trade management platform.  
- Attendees learn how they achieved ~40% lower operating cost and 5× operational efficiency while preserving both managed-platform convenience and OS‑level control.

### XNT204 – *Licensing commercial software on AWS*

- Clarifies licensing paths for Microsoft software and other commercial platforms on AWS.  
- Covers AWS Optimization and Licensing Assessment (AWS OLA), end‑of‑support scenarios, VMware cost considerations, and ways to replace traditional licensed products with cloud‑native or open-source options.

### XNT302 – *Harness Amazon Q Business power with Microsoft workload data sources*

- Shows how data in **SharePoint** and Windows file servers (via **Amazon FSx**) becomes a rich source for **Amazon Q Business**.  
- Demonstrates indexing, enforcing guardrails with Active Directory identities, and using generative AI securely over Microsoft content.

### XNT303 – *Reduce cost for SQL Server workloads on AWS using Optimize CPU feature*

- Focuses on using **Optimize CPU** settings on Amazon EC2 to tune vCPU allocation for SQL Server workloads that are more memory/IO‑bound than CPU‑bound.  
- Shares test results (including HammerDB benchmarks) and best practices to cut cost while maintaining performance.

### XNT311 – *Go codeless and replatform Windows applications on Amazon EKS*

- Moody’s discusses moving dozens of .NET apps from EC2 for Windows Server to **Amazon EKS with Windows support**.  
- Attendees see patterns, challenges, and platform‑engineering practices that enabled cost savings, higher performance, and more flexibility.

### XNT312 – *Use generative AI to optimize cloud operations for Microsoft workloads*

- Demonstrates how **Amazon Q** and **Amazon Bedrock** can simplify operations for Windows-based infrastructure.  
- Examples include natural‑language driven log analysis, configuration drift detection, and automation script generation.

### XNT314 – *Unleashing .NET workloads: From data center to multi-region resilience*

- Verisk Analytics shares its eight‑year modernization journey taking .NET workloads from data center to **multi‑Region, highly available** deployments on AWS.  
- Session covers cost controls (including warm pools) and lessons learned around server sprawl and Microsoft licensing.

### XNT313 – *Migrate and modernize a Microsoft-based banking solution with AWS*

- Targets financial institutions moving Microsoft‑based stacks to AWS to enable AI/ML adoption and better risk management.  
- Reviews migration, optimization, and modernization steps for Windows Server, SQL Server, .NET, and Active Directory workloads.

### XNT315 – *Modernizing a spin-off in the cloud: Allspring’s journey with AWS*

- Describes how **Allspring Global Investments**, spun out of Wells Fargo, moved off on‑premises infrastructure under tight timelines.  
- Shows how they used Amazon EC2, Amazon EBS, and Amazon RDS for SQL Server and Oracle as a foundation, and are now modernizing further with cloud‑native and open-source services.

### XNT316 – *From Azure to AWS: One organization’s all-in journey with AWS*

- Bonterra Inc. explains why it chose AWS as its strategic cloud over Azure.  
- Covers the rapid migration, architectural choices, and how the company co‑innovates with AWS to deliver solutions for the social good sector.

### XNT317 – *How Mindbody migrated 60,000 SQL Server databases to AWS*

- Mindbody recounts migrating a large monolithic Windows/SQL Server application with over **60,000 databases** to AWS Local Zones and Regions.  
- Discusses latency challenges, architecture patterns, licensing and cost decisions, and the operational improvements gained.

---

## 3. Builders’ sessions

Builders’ sessions are **small, hands‑on labs** (10 attendees per expert) with no slides—just laptops and guided building.

### XNT307 – *Unlock your data: Build AI applications with .NET and Amazon Bedrock*

- Hands‑on implementation of **Retrieval Augmented Generation (RAG)** using a .NET app and **Amazon Bedrock Knowledge Bases**.  
- Participants wire up private data sources so generative AI applications can answer questions grounded in enterprise content.

### XNT318 – *Boost .NET developer productivity with Amazon Q Developer*

- Shows how **Amazon Q Developer** accelerates .NET development through inline code suggestions and automation.  
- Attendees practice generating boilerplate code, iterating on prototypes, understanding unfamiliar code, and improving quality and security.

---

## 4. Chalk talks

Chalk talks are **interactive whiteboard sessions** with a short intro and then open Q&A.

### XNT201 – *AWS fundamentals for the accidental SQL Server database administrator*

- Oriented to DBAs who suddenly find themselves responsible for AWS environments.  
- Maps familiar SQL Server admin tasks to cloud architecture, discusses networking, security, HA/DR, and how generative AI (Amazon Q Business / Developer) can assist.

### XNT304 – *How to navigate your SQL Server migration journey with AWS*

- Reviews the spectrum of SQL Server migration strategies on AWS.  
- Compares AWS Migration Hub, Application Migration Service, AWS DMS, and native SQL Server tools such as replication and Always On, backed by lessons from real projects.

---

## 5. Code talks

Code talks are **demo‑heavy, code‑focused sessions** with a small audience and live examples.

### XNT305 – *Choose the right AI service for your .NET use case*

- Walks through when to use different **AWS AI and generative AI services** from .NET via the AWS SDK.  
- Includes building an intelligent document processing sample that uses both traditional AI and generative AI features.

### XNT309 – *Automate and troubleshoot AD using Amazon Bedrock*

- Shows how **Bedrock Agents** can automate routine Active Directory tasks and assist with troubleshooting.  
- Demos include analyzing logs and events to diagnose account lockouts, Kerberos issues, and providing natural‑language remediation steps.

### XNT310 – *Accelerate .NET development with Amazon Q Developer*

- Explores using Amazon Q Developer across multiple IDEs for writing, testing, debugging, and upgrading .NET code faster.  
- Covers privacy and enterprise controls, plus examples of scanning for issues and answering deep technical questions.

### XNT402 – *Build an image search engine with .NET and Amazon Bedrock*

- Guides attendees through building a semantic image search solution using **Amazon Bedrock** and **Amazon OpenSearch Service**.  
- Includes preprocessing images into embeddings, indexing them, and creating a .NET front end for search.

---

## 6. Workshops

Workshops are **two‑hour group labs** where attendees collaboratively build full solutions with AWS experts.

### XNT306 – *From diagram to code: Automate IaC code generation with Amazon Bedrock*

- Participants build an end‑to‑end .NET 8 app using Amazon Bedrock, AWS Lambda, and Amazon API Gateway.  
- The focus is generating infrastructure‑as‑code directly from architecture diagrams and then using agents to provision infrastructure securely.

### XNT308 – *Modernize Windows applications on your own terms*

- Attendees analyze several Windows applications and choose modernization paths such as containerizing to **Amazon ECS/EKS** or refactoring .NET to run on Linux.  
- Emphasizes thinking through dependencies and picking the right modernization strategy per app.

### XNT401 – *Easily port .NET Framework applications to Linux with Amazon Q*

- Hands‑on use of **Amazon Q Code Transformation for .NET** to move .NET Framework apps from Windows Server to cross‑platform .NET on Linux.  
- Highlights how this reduces licensing costs and can improve performance and security.

### XNT403 – *Securing AWS Managed Microsoft AD the AWS Well-Architected way*

- Applies the **AWS Well‑Architected Framework – security pillar** to AWS Managed Microsoft AD.  
- Uses IAM, CloudTrail, VPC configurations, and other services to build defense‑in‑depth and align with security best practices.

### XNT404 – *Migrate to an open source database on AWS using .NET and PostgreSQL*

- Demonstrates moving a .NET application from SQL Server to **Amazon RDS for PostgreSQL** using **AWS DMS**.  
- Discusses code and schema refactoring, common migration challenges, and repeatable techniques to adopt open-source databases.

---

## 7. Join us in Las Vegas

The blog closes by encouraging readers to:

- **Register for re:Invent** (if they haven’t already) and reserve seats for key sessions via the **Attendee Portal**.  
- Visit the **Windows, SQL Server, and .NET kiosk** in the AWS Village expo area to:
  - Meet experts building Microsoft‑related services  
  - See demos, including generative AI scenarios  
  - Ask questions and dive deeper into architectures for Microsoft workloads on AWS  

The overall message: AWS offers a broad set of services and features to run and modernize Microsoft applications efficiently, and re:Invent is the ideal place to learn how.

---

## 8. About the author

**David Pallmann** is a senior product manager on the **AWS Transform** team, focusing on the .NET developer experience.  
He has held roles in engineering, consulting, product management, and technical leadership; previously worked on **Windows Communication Foundation (WCF)** and later created **Neuron ESB**, a .NET‑based enterprise service bus.  
You can follow him on X at `@davidpallmann`.