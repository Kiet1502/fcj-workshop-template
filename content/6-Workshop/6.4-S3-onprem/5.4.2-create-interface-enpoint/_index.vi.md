---
title : "T?o m?t S3 Interface endpoint"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 6.4.2 </b> "
---

Trong ph?n này, b?n s? t?o và ki?m tra Interface Endpoint  S3 b?ng cách s? d?ng môi tru?ng truy?n th?ng mô ph?ng.

1. Quay l?i Amazon VPC menu. Trong thanh di?u hu?ng bên trái, ch?n Endpoints, sau dó click Create Endpoint.

2. Trong Create endpoint console:
+ Ð?t tên interface endpoint
+ Trong Service category, ch?n **aws services** 

![name](/images/5-Workshop/5.4-S3-onprem/s3-interface-endpoint1.png)

3.  Trong Search box, gõ S3 và nh?n Enter. Ch?n endpoint có tên com.amazonaws.us-east-1.s3. Ð?m b?o r?ng c?t Type có giá tr? Interface.

![service](/images/5-Workshop/5.4-S3-onprem/s3-interface-endpoint2.png)

4. Ð?i v?i VPC, ch?n VPC Cloud t? drop-down.
+ M? r?ng **Additional settings** và d?m b?o r?ng Enable DNS name *không* du?c ch?n (s? s? d?ng di?u này trong ph?n ti?p theo c?a workshop)

![vpc](/images/5-Workshop/5.4-S3-onprem/s3-interface-endpoint3.png)

5. Ch?n 2 subnets trong AZs sau: us-east-1a and us-east-1b

![subnets](/images/5-Workshop/5.4-S3-onprem/s3-interface-endpoint4.png)

6. Ð?i v?i Security group, ch?n SGforS3Endpoint:

![sg](/images/5-Workshop/5.4-S3-onprem/s3-interface-endpoint5.png)

7. Gi? default policy - full access và click Create endpoint

![success](/images/5-Workshop/5.4-S3-onprem/s3-interface-endpoint-success.png)

Chúc m?ng b?n dã t?o thành công S3 interface endpoint. ? bu?c ti?p theo, chúng ta s? ki?m tra interface endpoint.
