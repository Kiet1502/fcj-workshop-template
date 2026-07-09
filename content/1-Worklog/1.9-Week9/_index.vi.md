---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---


### Thời gian: 12/06 – 18/06

### Mục tiêu tuần 9:
* Khởi tạo tác nhân AI tự động bằng Amazon Bedrock Agents tích hợp AWS Lambda (Action Groups).
* Triển khai hệ thống Event-Driven với Amazon SQS và Amazon EventBridge decouple microservices.
* Quản trị DNS và bảo mật nâng cao với Amazon Route 53 và AWS WAF chống OWASP Top 10.
* Phân tích dữ liệu phi cấu trúc bằng AWS Glue Crawler và truy vấn SQL trực tiếp qua Amazon Athena.
* Bảo mật thông tin nhạy cảm (CSDL, API Keys) bằng AWS Secrets Manager và tự động xoay vòng khóa.

### Các công việc cần triển khai trong tuần này:
| STT | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **1** | Thực hành kiến trúc AI Agents: Khởi tạo và định cấu hình tác nhân AI tự động bằng Amazon Bedrock Agents; thiết lập các Action Groups tích hợp với hàm AWS Lambda để AI có thể tự động phân tích yêu cầu và gọi API thực thi tác vụ. | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Triển khai hệ thống Event-Driven (Hướng sự kiện): Thực hiện chuỗi Lab cấu hình hàng đợi tin nhắn bằng Amazon SQS và thiết lập bus sự kiện trung tâm với Amazon EventBridge để tách rời (decouple) các thành phần trong hệ thống microservices. | 13/06/2026 | 13/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **3** | Quản trị DNS và Bảo mật nâng cao: Thực hiện phân giải tên miền và định tuyến lưu lượng với Amazon Route 53; triển khai tường lửa ứng dụng web AWS WAF để bảo vệ các API endpoint và CloudFront phân phối nội dung khỏi các lỗ hổng phổ biến (OWASP Top 10). | 14/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **4** | Phân tích dữ liệu phi cấu trúc (Data Analytics): Chạy bài Lab thiết lập AWS Glue Crawler để tự động quét siêu dữ liệu (metadata) từ các file log trên Amazon S3, sau đó sử dụng Amazon Athena để viết lệnh SQL truy vấn trực tiếp dữ liệu thô này mà không cần tải vào database. | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **5** | Quản lý thông tin nhạy cảm: Triển khai AWS Secrets Manager nhằm bảo mật chuỗi kết nối cơ sở dữ liệu và các API Keys quan trọng, thực hành cơ chế tự động xoay vòng khóa (Secret rotation) để thay thế hoàn toàn việc lưu trữ biến môi trường (environment variables) dạng văn bản thuần. | 17/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 9:

* Xây dựng thành công AI Agent trên Bedrock biết tự động phân tích câu lệnh người dùng và gọi hàm Lambda tương ứng để thực hiện tác vụ thực tế.
* Thiết lập thành công mô hình Event-Driven, kết nối ổn định SQS và EventBridge giúp hệ thống microservices hoạt động bất đồng bộ, chịu tải cao.
* Cấu hình Route 53 trỏ tên miền chính xác, tích hợp thành công tường lửa WAF chặn hiệu quả các cuộc tấn công SQL Injection và XSS.
* Crawler quét thành công metadata từ log S3 tạo Data Catalog, viết câu lệnh SQL trên Athena truy vấn dữ liệu thô nhanh chóng, chính xác.
* Bảo mật tuyệt đối mật khẩu DB và API Keys trong Secrets Manager, ứng dụng lấy secret qua API an toàn, loại bỏ hoàn toàn hardcode/plaintext.



