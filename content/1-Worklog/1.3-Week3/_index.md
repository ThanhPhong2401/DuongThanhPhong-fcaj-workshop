---
title: "Week 3 Worklog"
date: 2026-05-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Learn advanced VPC connectivity mechanisms (VPC Peering and Transit Gateway).
* Practice SSH connection to instances in Private Subnets via Bastion Host.
* Implement modern networking services: NAT Gateway and EC2 Instance Connect Endpoint.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Learn Module 02_02: VPC Peering (direct VPC-to-VPC connection) and Transit Gateway (centralized VPC connectivity).<br>- Configure route tables to facilitate inter-VPC traffic. | 01/05/2026   | 01/05/2026      | <https://youtu.be/BPuD1l2hEQ4> |
| 2   | - Practice Lab 03-04: Deploy EC2 instances in Public/Private subnets.<br>- Set up keypairs and basic EC2 configurations. | 02/05/2026   | 02/05/2026      | <https://000003.awsstudygroup.com/4-prerequisite/> |
| 3   | - Practice Lab 03-04: SSH connection to Private instances via Bastion Host.<br>- Configure Route Tables for Private instances to access the Internet via Internet Gateway. | 03/05/2026   | 03/05/2026      | <https://000003.awsstudygroup.com/4-prerequisite/> |
| 4   | - Practice Lab 03-04: Create and configure NAT Gateway for Private EC2 internet access.<br>- Set up EC2 Instance Connect Endpoint for secure management. | 04/05/2026   | 04/05/2026      | <https://000003.awsstudygroup.com/4-prerequisite/> |
| 5   | - Continue Lab 03-04: Verify terminal connections to Private EC2 instances using EC2 Instance Connect Endpoint. | 04/05/2026   | 04/05/2026      | <https://000003.awsstudygroup.com/4-prerequisite/> |
| 6   | - Practice Lab 03-19: Setup VPC Peering between 2 VPCs.<br>- Configure Security Groups, NACLs, and Route Tables for cross-VPC communication; cleanup resources. | 05/05/2026   | 05/05/2026      | <https://000003.awsstudygroup.com/3-prerequisite/> |

### Week 3 Achievements:

* Mastered inter-VPC connectivity using VPC Peering and Transit Gateway.
* Proficient in SSH techniques for private instances using Bastion Hosts.
* Implemented NAT Gateway to enable internet access for instances in private subnets.
* Successfully deployed secure connections with EC2 Instance Connect Endpoint.
* Configured Routing, Security Groups, and NACLs to ensure secure communication between distinct VPCs.