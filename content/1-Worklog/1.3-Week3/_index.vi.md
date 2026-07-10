---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Thời gian: 01/05 - 07/05

### Mục tiêu tuần 3:
* Thực hành tạo và quản lý máy chủ EC2 chạy hệ điều hành Windows Server qua Remote Desktop (RDP).
* Triển khai ứng dụng quản lý workshop (**AWS FCJ Management**) lên máy chủ và cấu hình mạng, firewall để chạy ổn định.
* Tìm hiểu dịch vụ lưu trữ object Amazon S3 (Tạo bucket, cấu hình quyền IAM, Bucket Policy).
* Thực hành đưa giao diện web tĩnh lên Amazon S3 và bật tính năng Static Website Hosting.
* Lên văn phòng công ty: Học cơ sở dữ liệu Amazon RDS (MySQL), cài đặt Docker Engine lên EC2 và chạy thử container.
* Tổng hợp minh chứng, kiểm tra bảng chi phí AWS Billing và tắt tài nguyên không dùng.

### Các công việc cần triển khai trong tuần này:
| STT | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **1** | Thực hành tạo máy chủ EC2 chạy hệ điều hành Windows Server, cấu hình mật khẩu Administrator và kết nối qua Remote Desktop (RDP). | 01/05/2026 | 01/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Đưa ứng dụng của chương trình (**AWS FCJ Management**) lên máy chủ EC2 và kiểm tra các cấu hình môi trường cần thiết để app chạy. | 02/05/2026 | 02/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **3** | Cấu hình Security Group mở port và kiểm tra Route Table để đảm bảo ứng dụng có thể truy cập mượt mà từ bên ngoài internet. | 03/05/2026 | 03/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **4** | Học lý thuyết về dịch vụ lưu trữ Amazon S3, cách phân chia Storage Classes và các cơ chế bảo mật truy cập (IAM Role, Bucket Policy). | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **5** | Thực hành tạo S3 bucket, tải một trang web tĩnh (HTML/CSS/JS) lên và bật tính năng Static Website Hosting để chạy trực tiếp từ S3. | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **6** | *Lên văn phòng làm lab:* Học về cơ sở dữ liệu quan hệ Amazon RDS (tạo instance MySQL, thử kết nối từ EC2). Cài Docker Engine lên EC2 và chạy thử container mẫu. | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **7** | Viết báo cáo tổng hợp tuần 3, chụp ảnh minh chứng các lab và kiểm tra lại AWS Billing, sau đó xóa (terminate) các máy EC2/RDS không dùng để tránh tốn tiền. | 07/05/2026 | 07/05/2026 |  |

### Kết quả đạt được tuần 3:

* Biết cách dựng và sử dụng thành thạo máy chủ EC2 Windows Server qua RDP.
* Ứng dụng **AWS FCJ Management** đã được deploy và chạy ổn định trên máy chủ ảo.
* Hiểu cách cấu hình Security Group và mạng để mở luồng truy cập an toàn cho web app.
* Nắm chắc cách làm việc với Amazon S3, tự tay cấu hình và chạy thành công một trang web tĩnh host trực tiếp trên S3.
* Học thêm được kiến thức hữu ích khi lên văn phòng: biết cách tạo database MySQL trên Amazon RDS và chạy container Docker cơ bản trên EC2.
* Kiểm soát tốt chi phí, không để phát sinh tiền ngoài ý muốn trong tài khoản Free Tier.
