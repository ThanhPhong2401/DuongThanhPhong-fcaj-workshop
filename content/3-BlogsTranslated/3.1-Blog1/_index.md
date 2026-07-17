---
title: "Blog 1 - S&P Global’s innovative disaster recovery strategy using Amazon FSx for NetApp ONTAP snapshots"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

In the process of learning more about AWS, I came across an insightful blog post on the AWS Architecture Blog regarding how S&P Global Market Intelligence built its **Disaster Recovery (DR)** strategy using **Amazon FSx for NetApp ONTAP**.

Previously, I typically understood Disaster Recovery simply as data backup for restoration in case of an incident. However, after reading this article, I realized that in large-scale systems—especially financial ones—DR goes beyond just data backup. DR is also about designing the system to ensure it can continue to serve users in the shortest possible time when a primary Region or environment encounters an issue.

![Disaster Recovery Architecture](/images/anhKT-1.png)

## Article Overview

The article describes how S&P Global Market Intelligence deployed a DR solution for its Capital IQ platform. As this system serves financial data to global customers, requirements regarding availability, data consistency, RTO, and RPO are critical.

A highlight of this solution is the system's ability to failover to the DR environment in **read-only** mode in under 15 minutes. Subsequently, if full operations are required, the team can transition the DR environment to **read-write** mode following a controlled procedure.

## Core Architecture

The solution in the article is deployed using a multi-Region model:

* **US-East-1** acts as the Primary Region.
* **US-West-2** acts as the DR Region.
* SQL Servers run on Amazon EC2 and are organized in a Windows Server Failover Cluster.
* Each Region has an Amazon FSx for NetApp ONTAP file system.
* Data is synchronized from the primary Region to the DR Region using SnapMirror replication.
* FlexClone is used to create volumes from the latest snapshots in the DR Region, providing the system with data ready for read-only access.

## Key Components

### Amazon FSx for NetApp ONTAP
Amazon FSx for NetApp ONTAP is an AWS-managed file storage service that supports familiar NetApp ONTAP features such as snapshots, replication, and data cloning. In this use case, FSx for ONTAP serves as the primary storage layer for the SQL Server data that needs to be protected.

### Snapshot
A snapshot captures the state of data at a specific point in time. It provides the foundation for the system to create data copies for restoration or testing without having to manually copy all data.

### SnapMirror
SnapMirror is used for replicating data from the Primary Region to the DR Region. According to the article, replication is configured at 15-minute intervals, ensuring the DR Region always has data synchronized close to production.

### FlexClone
FlexClone is the most interesting feature to me in this article. Instead of having to rebuild the entire environment from scratch, the system can create a clone from the snapshot that has been replicated to the DR Region. This clone operates independently of the replication process, allowing it to provide read-only access without disrupting ongoing data synchronization.

## Recovery Procedure

The article divides the DR approach into two phases:

1. **Rapid failover to read-only:** Uses snapshots and FlexClone to provide a DR environment capable of accessing data within a short timeframe.
2. **Transition to read-write when necessary:** Ceases writes in the Primary Region, performs a final SnapMirror update, breaks the replication relationship, and migrates SQL Server resources to the DR Region.

This method allows users to continue accessing critical data while the technical team manages the full recovery process.

## Key Takeaways

As a student new to AWS, this article helped me better understand that when designing systems on the cloud, it is not enough to simply be concerned with deploying applications. I also need to consider scenarios such as:

* How to handle incidents when the system encounters an issue?
* How much data might be lost in the worst-case scenario?
* Will users still have access to critical data?
* How long does the system need for recovery?
* Are failover and fallback procedures tested in advance?

The article also helped me understand that Disaster Recovery is a combination of architecture, data, operations, and processes. Backup is a vital component, but it is not sufficient on its own to create a complete DR strategy.

## Conclusion

While I have not yet fully grasped all the technical aspects of this article, particularly regarding Amazon FSx for NetApp ONTAP, SnapMirror, and FlexClone, this is a highly recommended case study. It demonstrates how large-scale systems can be designed for DR—not just to recover data, but also to minimize downtime and maintain accessibility for users.

Reference Link: https://aws.amazon.com/vi/blogs/architecture/sp-globals-innovative-disaster-recovery-strategy-using-amazon-fsx-for-netapp-ontap-snapshots/