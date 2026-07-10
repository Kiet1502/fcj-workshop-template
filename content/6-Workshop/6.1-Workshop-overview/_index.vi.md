---
title : "Giới thiệu"
date : 2024-01-01 
weight : 1
chapter : false
pre : " <b> 6.1. </b> "
---

#### Giới thiệu về VPC Endpoint

+ Điểm cuối VPC (endpoint) là thiết bị ảo. Chúng là các thành phần VPC có thể mở rộng theo chiều ngang, dự phòng và có tính sẵn sàng cao. Chúng cho phép giao tiếp giữa tài nguyên điện toán của bạn và dịch vụ AWS mà không gây ra rủi ro về tính sẵn sàng.
+ Tài nguyên điện toán đang chạy trong VPC có thể truy cập Amazon S3 bằng cách sử dụng điểm cuối Gateway. Interface Endpoint  PrivateLink có thể được sử dụng bởi tài nguyên chạy trong VPC hoặc tại TTDL.

#### Tổng quan về workshop
Trong workshop này, bạn sẽ sử dụng hai VPC.
+ **"VPC Cloud"** dành cho các tài nguyên cloud như Gateway endpoint và EC2 instance để kiểm tra.
+ **"VPC On-Prem"** mô phỏng môi trường truyền thống như nhà máy hoặc trung tâm dữ liệu của công ty. Một EC2 Instance chạy phần mềm StrongSwan VPN đã được triển khai trong "VPC On-prem" và được cấu hình tự động để thiết lập đường hầm VPN Site-to-Site với AWS Transit Gateway. VPN này mô phỏng kết nối từ một vị trí tại TTDL (on-prem) với AWS cloud. Để giảm thiểu chi phí, chỉ một phiên bản VPN được cung cấp để hỗ trợ workshop này. Khi lập kế hoạch kết nối VPN cho production workloads của bạn, AWS khuyên bạn nên sử dụng nhiều thiết bị VPN để có tính sẵn sàng cao.

![overview](/images/5-Workshop/5.1-Workshop-overview/diagram1.png)

---

### Kết quả đạt được & Năng lực chuẩn bị (Step Outcomes)
* **Nắm vững mô hình kiến trúc Hybrid Cloud:** Hiểu rõ sơ đồ luồng dữ liệu (Data flow) giữa 2 VPC riêng biệt (`VPC Cloud` chứa tài nguyên đích và `VPC On-Prem` mô phỏng trung tâm dữ liệu doanh nghiệp kết nối qua AWS Transit Gateway VPN).
* **Xác định mục tiêu bảo mật cốt lõi:** Định hình rõ sự cần thiết của việc tách biệt lưu lượng truy cập Amazon S3 ra khỏi Internet công cộng nhằm đảm bảo tuân thủ tiêu chuẩn bảo mật doanh nghiệp.

