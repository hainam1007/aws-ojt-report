---
title: "Week 3 Worklog"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:
* Understand EC2 and S3 services in depth
* Learn to import virtual machines to AWS
* Export virtual machines from EC2 instance and AMI
* Mount file sharing on on-premise machine

### Tasks carried out:

| Day | Task | Date | Status |
|-----|------|------|--------|
| Mon | - Learn EC2 basics (instance types, user data, metadata) <br> - Study EC2 auto scaling (EFA/SR, Lightsail, MGN) | 11/18/2025 | ✅ Done |
| Tue | - Create S3 bucket <br> - Upload objects <br> - Deploy web using S3 <br> - Accelerate static web with CloudFront | 11/19/2025 | ✅ Done |
| Wed | - Create Storage Gateway <br> - Create File Shares <br> - Mount File Shares to on-premise machine <br> - Create backup plan <br> - Set up notifications | 11/20/2025 | ✅ Done |
| Thu | - Learn S3 advanced (access point, storage class, static website & CORS, Glacier, Snow Family, Storage Gateway, Backup) | 11/21/2025 | ✅ Done |
| Fri | - Import virtual machine to AWS <br> - Deploy instance from AMI <br> - Export VM from EC2 instance and AMI through S3 bucket | 11/22/2025 | ✅ Done |

### Achievements:
* ✅ Mastered EC2 instance types and scaling options
* ✅ Created and configured S3 buckets for static website hosting
* ✅ Deployed CloudFront distribution for content acceleration
* ✅ Set up Storage Gateway for hybrid cloud storage
* ✅ Successfully imported/exported virtual machines

### Key Learnings:
* EC2 user data and metadata usage
* S3 storage classes and cost optimization
* CloudFront CDN configuration
* Storage Gateway types (File, Volume, Tape)
* VM import/export process via AWS CLI

### Challenges:
* CORS configuration for S3 static website → Fixed policy settings
* Storage Gateway connectivity issues → Adjusted security groups
* VM import format errors → Converted to supported OVA format

### Next Week:
* RDS database deployment
* Load balancing with ELB
* Auto Scaling groups
