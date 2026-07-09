---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---


### Thời gian: 05/06 – 11/06

### Mục tiêu tuần 8:
* Triển khai cơ sở dữ liệu NoSQL với Amazon DynamoDB (Table, Partition Key, Queries).
* Thiết lập luồng CI/CD tự động bằng AWS CodePipeline và AWS CodeBuild.
* Quản lý định danh người dùng với Amazon Cognito (User Pool login/signup).
* Hosting frontend web app lên AWS Amplify tự động CI/CD với Git repo.
* Quản lý container với Amazon ECR và Amazon ECS chạy Serverless qua AWS Fargate.

### Các công việc cần triển khai trong tuần này:
| STT | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **1** | Thực hành triển khai cơ sở dữ liệu NoSQL với Amazon DynamoDB, tìm hiểu cách thiết lập bảng, khóa phân vùng (Partition Key) và thực thi các thao tác truy vấn dữ liệu. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Nghiên cứu và thiết lập luồng CI/CD cơ bản bằng AWS CodePipeline và AWS CodeBuild để tự động hóa toàn bộ quá trình kiểm thử, đóng gói và triển khai mã nguồn. | 06/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **3** | Tìm hiểu dịch vụ Amazon Cognito để quản lý định danh người dùng, thực hành cấu hình User Pool cung cấp tính năng đăng nhập/đăng ký bảo mật cho ứng dụng web. | 07/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **4** | Thực hành triển khai (hosting) ứng dụng frontend lên AWS Amplify, kết nối trực tiếp với kho lưu trữ mã nguồn để tự động cập nhật giao diện khi có thay đổi code. | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **5** | Nghiên cứu dịch vụ quản lý container Amazon ECR (Elastic Container Registry) và Amazon ECS. Thực hành tải (push) image Docker lên ECR và cấu hình chạy container trên nền tảng Serverless thông qua AWS Fargate. | 10/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 8:

* Khởi tạo bảng DynamoDB, thiết kế Partition/Sort Key hiệu quả và thực hiện các câu truy vấn (Query/Scan) nhanh chóng.
* Thiết lập pipeline CI/CD hoàn chỉnh, code tự động build và deploy ngay khi push commit lên GitHub.
* Tích hợp thành công Cognito User Pool vào web app, hỗ trợ đăng ký, đăng nhập bảo mật (JWT Tokens).
* Hosting giao diện React/Vue/HTML thành công trên Amplify với HTTPS tự động và CI/CD siêu nhanh.
* Push thành công Docker image lên ECR và khởi chạy dịch vụ container ổn định trên ECS Fargate không cần quản lý EC2.



