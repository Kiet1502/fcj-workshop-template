---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---


### Thời gian: 29/05 – 04/06

### Mục tiêu tuần 7:
* Lên văn phòng họp nhóm khớp luồng code và thực hành tạo tài khoản IAM User quyền AdministratorAccess thay cho Root.
* Tìm hiểu nhanh lý thuyết về Bedrock Knowledge Bases và OpenSearch Serverless qua tài liệu hướng dẫn.
* Tập trung phát triển Frontend: Xây dựng **Giao diện Phòng thi trực tuyến (Exam Room UI)** cho thí sinh.
* Tích hợp khung hiển thị camera giám sát AI (Proctoring camera view) vào góc màn hình làm bài.
* Kiểm thử luồng dữ liệu thời gian thực giữa giao diện phòng thi và backend.

### Các công việc cần triển khai trong tuần này:
| STT | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **1** | *Lên văn phòng công ty:* Họp trực tiếp với team để khớp code Frontend/Backend. Thực hành tạo tài khoản IAM User có quyền AdministratorAccess để làm việc thay thế cho tài khoản Root đúng chuẩn bảo mật. | 29/05/2026 | 30/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Đọc hiểu cơ chế làm việc của Amazon Bedrock Knowledge Bases và OpenSearch Serverless để nắm được cách hệ thống RAG tra cứu tài liệu phía sau. | 31/05/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **3** | Lập trình **Giao diện Phòng thi trực tuyến (Exam Room UI)** với các tính năng chọn đáp án, chuyển câu hỏi mượt mà, lưu nháp bài làm và bộ đếm ngược thời gian. | 02/06/2026 | 03/06/2026 | |
| **4** | Tích hợp khung hiển thị camera (Webcam Stream) ngay góc màn hình phòng thi phục vụ cho tính năng giám sát AI (AI Proctoring), kết nối thử nghiệm luồng trả cảnh báo vi phạm từ backend. | 04/06/2026 | 04/06/2026 | |

### Kết quả đạt được tuần 7:

* Cấu hình thành công tài khoản IAM User bảo mật và hiểu rõ cách hoạt động của RAG trên OpenSearch.
* Hoàn thiện màn hình Phòng thi trực tuyến (Exam Room UI) với trải nghiệm làm bài trực quan, không bị giật lag khi chuyển câu.
* Ghép nối thành công khung webcam giám sát lên màn hình thi, tạo tiền đề để tích hợp với AI phát hiện gian lận.
* Buổi làm việc offline tại văn phòng giúp cả nhóm giải quyết nhanh gọn nhiều vướng mắc khi nối API thực tế.
