---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---


### Thời gian: 22/05 - 28/05

### Mục tiêu tuần 6:
* Nghiên cứu hệ thống giám sát và quản lý log trên Cloud qua Amazon CloudWatch.
* Thiết lập CloudWatch Dashboard theo dõi chỉ số CPU, Network.
* Cấu hình cảnh báo tự động CloudWatch Alarms kết hợp Amazon SNS gửi email khi vượt ngưỡng.
* Tìm hiểu tư duy Infrastructure as Code (IaC) và dịch vụ AWS CloudFormation.
* Thực hành Lab: Viết template CloudFormation (YAML) tự động hóa quy trình khởi tạo tài nguyên.

### Các công việc và kết quả triển khai trong tuần:
| STT | Nội dung công việc | Kết quả đạt được | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :--- | :---: | :---: | :--- |
| **1** | Nghiên cứu hệ thống giám sát và quản lý log trên môi trường Cloud thông qua dịch vụ Amazon CloudWatch. | Hiểu rõ kiến trúc thu thập Metrics và Log Groups của CloudWatch. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Thực hành thiết lập CloudWatch Dashboard để theo dõi các chỉ số hiệu suất (Metrics) cơ bản như CPU, Network của máy chủ. | Xây dựng thành công Dashboard trực quan, hiển thị real-time các biểu đồ hiệu suất EC2. | 23/05/2026 | 23/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **3** | Cấu hình hệ thống cảnh báo tự động (CloudWatch Alarms) kết hợp với Amazon SNS để gửi email thông báo khi tài nguyên vượt ngưỡng an toàn. | Tạo thành công SNS Topic và CloudWatch Alarm, tự động gửi email cảnh báo khi CPU vượt 80%. | 24/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **4** | Tìm hiểu tư duy Quản lý hạ tầng dưới dạng mã nguồn (Infrastructure as Code - IaC) và dịch vụ AWS CloudFormation. | Nắm vững triết lý IaC, cấu trúc template CloudFormation (Parameters, Resources, Outputs...). | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **5** | Thực hành Lab: Viết template CloudFormation (định dạng YAML) để tự động hóa toàn bộ quy trình khởi tạo tài nguyên, thay thế cho thao tác click chuột thủ công. | Viết và deploy thành công stack CloudFormation bằng YAML, khởi tạo toàn bộ hạ tầng chỉ trong vài phút. | 27/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


