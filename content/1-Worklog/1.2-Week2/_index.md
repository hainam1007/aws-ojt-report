---
title: "Week 2 Worklog"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:
* Deep dive into VPC networking concepts
* Learn S3 storage service and best practices
* Understand IAM policies and roles

### Tasks carried out:

| Day | Task | Date | Status |
|-----|------|------|--------|
| Mon | - Study VPC basics (subnets, route tables, internet gateway) <br> - Learn about public vs private subnets <br> - Security Groups vs NACLs | 11/11/2025 | ✅ Done |
| Tue | - Create custom VPC with public/private subnets <br> - Configure route tables <br> - Setup NAT Gateway <br> - Test EC2 in private subnet | 11/12/2025 | ✅ Done |
| Wed | - Learn S3 fundamentals (buckets, objects, storage classes) <br> - Study S3 security (bucket policies, ACLs) <br> - S3 versioning and lifecycle policies | 11/13/2025 | ✅ Done |
| Thu | - Create S3 buckets <br> - Upload/download files via Console & CLI <br> - Configure bucket policies <br> - Enable versioning and encryption | 11/14/2025 | ✅ Done |
| Fri | - Learn IAM basics (users, groups, roles, policies) <br> - Study principle of least privilege <br> - Create IAM policies for EC2 and S3 access | 11/15/2025 | ✅ Done |

### Achievements:
* ✅ Created custom VPC with proper network segmentation
* ✅ Deployed EC2 instances in public and private subnets
* ✅ Configured NAT Gateway for private subnet internet access
* ✅ Created and managed S3 buckets with proper security
* ✅ Implemented IAM policies following least privilege principle

### Key Learnings:
* VPC architecture and subnet design best practices
* Difference between Security Groups (stateful) and NACLs (stateless)
* S3 storage classes and cost optimization strategies
* IAM policy structure and permission boundaries

### Challenges:
* NAT Gateway routing issues → Fixed route table associations
* S3 bucket policy syntax errors → Used AWS Policy Generator
* IAM permission denied errors → Reviewed CloudTrail logs

### Next Week:
* RDS and database management
* CloudFormation basics
* Monitoring with CloudWatch
