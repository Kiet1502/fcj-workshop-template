---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Thời gian: 24/04 – 30/04

### Mục tiêu tuần 2:
* Học lý thuyết và thực hành tự tay dựng một mạng ảo riêng Amazon VPC (Subnet, Internet Gateway, Route Table).
* Tìm hiểu và thực hành quản trị máy chủ ảo EC2 chạy hệ điều hành Linux (Amazon Linux/Ubuntu).
* Thử nghiệm tạo máy chủ với các cấu hình kích thước khác nhau (t3.nano, t3.micro) để kiểm tra mức độ tiêu thụ tài nguyên.
* Cài đặt web server (`httpd`), chạy thử trang web mẫu và cấu hình Security Group để truy cập từ trình duyệt.

### Các công việc cần triển khai trong tuần này:
| STT | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **1** | Học lý thuyết về hạ tầng mạng trên AWS và thực hành tạo một Amazon VPC hoàn chỉnh gồm Public/Private Subnets, Internet Gateway và Route Table. | 24/04/2026 | 24/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Tìm hiểu cách làm việc với máy chủ EC2 Linux (Amazon Linux 2023), học cách tạo SSH Key Pair và kết nối vào terminal qua SSH/Session Manager. | 25/04/2026 | 26/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **3** | Thực hành tạo thử vài máy chủ EC2 Linux với các cấu hình t3.nano và t3.micro để quan sát sự khác biệt về RAM/CPU, sau đó tắt (terminate) các máy không dùng. | 27/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **4** | Cài đặt Apache Web Server (`httpd`) trên EC2 Linux, đưa một trang web HTML mẫu lên máy chủ và mở port 80/443 trên Security Group để truy cập thành công từ internet. | 29/04/2026 | 30/04/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 2:

* Nắm rõ cách hoạt động của VPC, Subnet, Route Table và tự tạo được mạng ảo VPC riêng trên AWS.
* Biết cách tạo SSH Key Pair, kết nối vào máy chủ Linux và sử dụng các lệnh terminal cơ bản.
* Hiểu được cách chọn cấu hình EC2 (Instance Type) phù hợp với nhu cầu để không bị lãng phí chi phí.
* Tự tay cài đặt web server Linux và chạy thành công trang web đầu tiên có thể truy cập qua Public IP từ trình duyệt.
