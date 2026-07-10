---
title: "Workshop"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

# Secure Hybrid Access to S3 using VPC Endpoints

#### Overview

**AWS PrivateLink** provides private connectivity to AWS services from VPCs and your on-premises networks, without exposing your traffic to the Public Internet.

In this lab, you will learn how to create, configure, and test VPC endpoints that enable your workloads to reach AWS services without traversing the Public Internet.

You will create two types of endpoints to access Amazon S3: a Gateway VPC endpoint, and an Interface VPC endpoint. These two types of VPC endpoints offer different benefits depending on if you are accessing Amazon S3 from the cloud or your on-premises location
+ **Gateway** - Create a gateway endpoint to send traffic to Amazon S3 or DynamoDB using private IP addresses.You route traffic from your VPC to the gateway endpoint using route tables.
+ **Interface** - Create an interface endpoint to send traffic to endpoint services that use a Network Load Balancer to distribute traffic. Traffic destined for the endpoint service is resolved using DNS.

#### Content

1. [Workshop overview](5.1-Workshop-overview)
2. [Prerequiste](5.2-Prerequiste/)
3. [Access S3 from VPC](5.3-S3-vpc/)
4. [Access S3 from On-premises](5.4-S3-onprem/)
5. [VPC Endpoint Policies (Bonus)](5.5-Policy/)
6. [Clean up](5.6-Cleanup/)

---

### Workshop Outcomes & Key Takeaways

Upon completing the **VPC Endpoints (AWS PrivateLink) for Amazon S3** hands-on lab series, engineers and students achieve comprehensive mastery across cloud networking architecture and operational security:

#### 1. Technical Mastery & Architecture Validation
* **Mastering Secure Hybrid Cloud Connectivity:** Successfully designed and implemented zero-trust private connectivity architectures between corporate On-premises data centers (simulated via VPN Site-to-Site) and the AWS Cloud ecosystem.
* **Differentiating & Deploying Dual S3 Endpoint Types:**
  - **Gateway VPC Endpoint:** Configured VPC Route Tables to direct internal VPC traffic destined for Amazon S3 over private IP addresses, entirely at **zero endpoint cost ($0/month)**.
  - **Interface VPC Endpoint (AWS PrivateLink):** Provisioned private IP addresses inside subnets and enabled internal DNS resolution, allowing on-premises servers to securely access S3 buckets over VPN/Direct Connect without public internet exposure or NAT Gateways.
* **Implementing Endpoint-Layer Security Controls (VPC Endpoint Policies):** Formulated and applied IAM policies directly on VPC Endpoints to restrict access exclusively to authorized corporate S3 buckets while blocking access to external buckets (**Data Exfiltration Prevention**).

#### 2. Operational Value & Cost Optimization
* **Zero-Trust Network Security:** Completely eliminated dependencies on Internet Gateways, NAT Gateways, and Public IP addresses when accessing Amazon S3, drastically reducing network attack vectors (DDoS, Man-in-the-Middle).
* **Significant Data Transfer Cost Savings:** Bypassed expensive NAT Gateway data processing fees (~$0.045/GB) for data-heavy workloads interacting with Amazon S3 (e.g., Big Data analytics, backups, log aggregation).
* **High-Performance & Low-Latency Routing:** Routed data flows through the highly redundant AWS Global Network backbone, achieving superior throughput and consistent low-latency performance for critical enterprise applications.
