---
title : "Access S3 from VPC"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 6.3. </b> "
---

#### Using Gateway endpoint

In this section, you will create **a Gateway eendpoint** to access **Amazon S3** from **an EC2 instance**. **The Gateway endpoint** will allow upload an object to S3 buckets without using **the Public Internet**. To create an endpoint, you must specify the VPC in which you want to create the endpoint, and the service (in this case, S3) to which you want to establish the connection.

![overview](/images/5-Workshop/5.3-S3-vpc/diagram2.png)

#### Content

- [Create gateway endpoint](3.1-create-gwe/)
- [Test gateway endpoint](3.2-test-gwe/)

---

### Step Outcomes & Verification
* **Gateway VPC Endpoint Provisioned:** Successfully created and attached the S3 Gateway Endpoint (`com.amazonaws.us-east-1.s3`) to the route tables of `VPC Cloud`.
* **Internal Connectivity Verified:** Confirmed object upload capability to S3 from the EC2 instance inside `VPC Cloud` entirely via private internal routing without public internet or NAT traversal.
* **Zero Cost Impact:** Achieved high-speed internal S3 transfer at zero hourly or data processing endpoint costs.
