---
title: "Week 2 Worklog"
date: 2026-04-24
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Study core concepts of AWS VPC (Virtual Private Cloud) and its networking features.
* Distinguish between security firewalls in AWS networking (Security Groups and NACLs).
* Practice building a basic network infrastructure (VPC, Subnet, Route Table, Internet Gateway) on the AWS Console.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Learn Module 02_01: AWS VPC. Understand the role of a private, isolated virtual network environment on the Cloud.<br>- Select the Singapore Region to optimize latency for Vietnamese users.<br>- Study CIDR notation for IPv4/IPv6 and design a VPC covering at least 3 AZs. | 24/04/2026   | 24/04/2026      | <https://youtu.be/O9Ac_vGHquM?si=w4rXO8E9eY7so_Og> |
| 2   | - Continue studying VPC Subnets to divide the network for better organization and security control.<br>- Differentiate and understand the usage of Public Subnets (with Internet, for Web servers) and Private Subnets (no Internet, for Databases). | 25/04/2026   | 25/04/2026      | <https://youtu.be/O9Ac_vGHquM?si=w4rXO8E9eY7so_Og> |
| 3   | - Research Route Tables to direct network traffic for both Public and Private Subnets.<br>- Learn about the default Route Table of a VPC (which allows all subnets to communicate internally). | 26/04/2026   | 26/04/2026      | <https://youtu.be/O9Ac_vGHquM?si=w4rXO8E9eY7so_Og> |
| 4   | - Learn other key networking components: ENI (Virtual network card attached to EC2), VPC Endpoints, Internet Gateways, and NAT Gateways. | 27/04/2026   | 27/04/2026      | <https://youtu.be/O9Ac_vGHquM?si=fI-T6CMmJfzIVo4> |
| 5   | - **Practice Module 02 - Lab 03:** Successfully deploy a basic network topology on the AWS Console, including: Creating a VPC, creating Subnets, setting up Route Tables, and configuring an Internet Gateway. | 28/04/2026   | 28/04/2026      | <https://000003.awsstudygroup.com/3-prerequisite/> |
| 6   | - Learn Module 02_02: VPC Security. Deep dive into **Security Groups**.<br>- Understand the Stateful nature, application on ENIs, and how it blocks all inbound traffic by default while allowing outbound traffic. | 29/04/2026   | 29/04/2026      | <https://youtu.be/BPuD1l2hEQ4?si=YwiJjhpn0Nngdf8r> |
| 7   | - Study the second layer of defense: **Network ACLs (NACLs)**.<br>- Master the Stateless nature (requires configuring both directions), application at the Subnet level, and how rules are processed from top to bottom. | 30/04/2026   | 30/04/2026      | <https://youtu.be/BPuD1l2hEQ4?si=YwiJjhpn0Nngdf8r> |

### Week 2 Achievements:

* Understood VPC operations as a virtual network, including CIDR design and multi-AZ (3 AZs) setup in Singapore.
* Clearly distinguished between the purpose and configuration of Public Subnets versus Private Subnets.
* Mastered Route Table traffic routing and Internet Gateway connectivity.
* Differentiated between the Stateful nature of Security Groups (resource-level) and the Stateless nature of NACLs (subnet-level).
* Successfully completed Lab 03, deploying a core network infrastructure including VPC, Subnets, Route Tables, and Internet Gateways.