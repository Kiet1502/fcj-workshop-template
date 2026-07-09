---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---


### Thời gian: 29/05 – 04/06

### Mục tiêu tuần 7:
* Đến công ty và thực hành các dịch vụ AWS.
* Tạo và cấu hình tài khoản IAM User quyền AdministratorAccess thay thế tài khoản Root.
* Triển khai Amazon Bedrock Knowledge Bases kết hợp mô hình Titan Embeddings G1 - Text v1.2 phục vụ RAG.
* Cấu hình Amazon S3 làm Data Source và thiết lập vector database qua Amazon OpenSearch Serverless.
* Thực hành gỡ lỗi quá tải yêu cầu (Error 429) và dọn dẹp OpenSearch Collections bị kẹt.

### Các công việc và kết quả triển khai trong tuần:
| STT | Nội dung công việc | Kết quả đạt được | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :--- | :---: | :---: | :--- |
| **1** | Đến công ty và học các dịch vụ bên dưới. | Trực tiếp tham gia học tập, trao đổi chuyên môn tại văn phòng công ty. | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Tạo và cấu hình tài khoản IAM User với quyền AdministratorAccess để thay thế tài khoản Root, đảm bảo tuân thủ nguyên tắc bảo mật. | Thiết lập thành công IAM User, bật MFA và ngừng hoàn toàn sử dụng Root account cho các thao tác hàng ngày. | 30/05/2026 | 30/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **3** | Triển khai Amazon Bedrock Knowledge Bases kết hợp mô hình Titan Embeddings G1 - Text v1.2 nhằm phục vụ kiến trúc RAG. | Cấu hình thành công Knowledge Bases trên Bedrock, kết nối với mô hình embedding Titan G1. | 31/05/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **4** | Cấu hình Amazon S3 làm nguồn cấp dữ liệu (Data Source) và thiết lập cơ sở dữ liệu vector tự động thông qua Amazon OpenSearch Serverless. | Tạo S3 Bucket chứa dữ liệu tài liệu, đồng bộ thành công sang OpenSearch Serverless Collection làm vector store. | 03/07/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **5** | Thực hành gỡ lỗi quá tải yêu cầu (Error 429) thông qua việc điều hướng khu vực triển khai (us-east-1) và dọn dẹp các OpenSearch Collections bị kẹt. | Xử lý triệt để lỗi Throttling (429) bằng cách chuyển vùng triển khai và xóa bỏ tài nguyên OpenSearch kẹt để tối ưu hiệu năng. | 04/07/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


