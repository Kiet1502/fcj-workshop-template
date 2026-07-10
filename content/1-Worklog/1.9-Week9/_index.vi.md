---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Thời gian: 12/06 – 18/06

### Mục tiêu tuần 9:
* Tìm hiểu cơ chế quản trị tên miền (Route 53) và tường lửa bảo vệ ứng dụng web (AWS WAF).
* Tập trung phát triển Frontend: Xây dựng **Giao diện Tạo đề thi tự động bằng AI (AI Exam Builder UI)**.
* Lập trình trang Báo cáo thống kê và Biểu đồ kết quả thi trực quan cho giảng viên.
* Phối hợp với team backend để nối API Bedrock tạo ma trận câu hỏi ngay từ trình duyệt.

### Các công việc cần triển khai trong tuần này:
| STT | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **1** | Tìm hiểu nhanh lý thuyết về bảo mật ứng dụng với Amazon Route 53 và tường lửa AWS WAF. Các lab nặng về dữ liệu lớn (Glue/Athena) được thống nhất tìm hiểu qua lý thuyết để dành thời gian cho code Frontend. | 12/06/2026 | 13/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Lập trình **Giao diện Tạo đề thi AI (AI Exam Builder UI)**, làm tính năng cho phép giảng viên tải lên file tài liệu (PDF/DOCX) hoặc gõ chủ đề/yêu cầu đề thi. | 14/06/2026 | 15/06/2026 | |
| **3** | Phối hợp sát sao với team backend để nối API gọi sang Bedrock Agents/Lambda tự sinh ma trận đề thi. Xử lý hiển thị hiệu ứng tải (loading spinners) và cho phép giảng viên chỉnh sửa câu hỏi trước khi lưu. | 16/06/2026 | 17/06/2026 | |
| **4** | Thiết kế và code trang Báo cáo thống kê điểm thi (Analytics Dashboard) cho giảng viên, hiển thị biểu đồ phân bổ điểm số và tỷ lệ làm đúng/sai từng câu. | 18/06/2026 | 18/06/2026 | |

### Kết quả đạt được tuần 9:

* Nắm được nguyên lý bảo mật web với WAF và DNS Route 53 mà không bị mất thời gian vào các lab backend chuyên sâu.
* Hoàn thành màn hình Tạo đề thi tự động bằng AI cực kỳ trực quan, giúp giảng viên tạo ma trận câu hỏi chỉ trong vài giây.
* Dựng xong trang Báo cáo kết quả với các biểu đồ thống kê sinh động, dễ theo dõi.
* Sự phối hợp ăn ý giữa Frontend và Backend giúp các tính năng AI của đồ án **Aura Academic** chạy rất mượt mà trên môi trường thực tế.
