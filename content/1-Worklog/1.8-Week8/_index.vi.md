---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


### Thời gian: 05/06 – 11/06

### Mục tiêu tuần 8:
* Tìm hiểu cơ chế quản lý định danh Amazon Cognito và dịch vụ hosting ứng dụng web AWS Amplify.
* Tập trung phát triển Frontend: Tích hợp luồng xác thực (Login, Sign-up, JWT Token) của Cognito trực tiếp vào app.
* Cấu hình CI/CD tự động build và deploy trang web Frontend lên AWS Amplify từ GitHub.
* Họp nhóm rà soát, kiểm thử tính năng phân quyền giữa giảng viên và sinh viên trên toàn hệ thống.

### Các công việc cần triển khai trong tuần này:
| STT | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **1** | Tích hợp thành công luồng xác thực (Đăng ký, Đăng nhập, Quên mật khẩu) vào code Frontend của dự án. Xử lý lưu trữ JWT Token an toàn và phân quyền bảo vệ trang (Protected Routes). | | | |
| **2** | Kết nối kho code Frontend trên GitHub với dịch vụ AWS Amplify, thiết lập CI/CD tự động deploy trang web mỗi khi có commit mới push lên nhánh chính. | | | |
| **3** | Họp nhóm kiểm tra chéo các chức năng, rà soát tính năng phân quyền (Sinh viên với Giảng viên) và thử nghiệm giao diện trên màn hình máy tính lẫn điện thoại di động. | | | |

### Kết quả đạt được tuần 8:

* Hiểu cách hoạt động của Cognito và biết cách dùng AWS Amplify để host trang web tự động.
* Tích hợp trọn vẹn luồng đăng nhập, đăng ký và phân quyền bảo mật trực tiếp vào code Frontend dự án nhóm.
* Trang web của dự án **Aura Academic** đã có link HTTPS chạy live thực tế trên AWS Amplify, tự động cập nhật khi push code git.
* Phân quyền chính xác: sinh viên chỉ vào được phòng thi/lịch sử của mình, còn giảng viên vào được trang quản lý đề thi và xem báo cáo.
