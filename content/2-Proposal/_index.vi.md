---
title: "Bản đề xuất"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

## AURACADEMIC
### Nền tảng Thi trực tuyến và Giám sát bằng AI trên AWS

---

### 1. Tóm tắt điều hành  


AuraAcademic là nền tảng thi trực tuyến tích hợp giám sát AI (Powered by Bedrock & Rekognition/YOLOv8) nhằm đảm bảo tính công bằng và minh bạch cho các kỳ thi từ xa. Hệ thống ứng dụng mô hình YOLOv8 để phát hiện gian lận qua camera theo thời gian thực. Bằng việc kết hợp kiến trúc AWS (CloudFront, ECS Fargate, EC2 GPU Spot) và các dịch vụ Serverless/Managed Services, AuraAcademic cung cấp một giải pháp giám sát tự động với độ chính xác cao nhưng chi phí vận hành chỉ bằng một phần nhỏ so với việc thuê giám thị trực tiếp, phù hợp với nhu cầu tổ chức thi trực tuyến cho các cơ sở giáo dục.

---

### 2. Tuyên bố vấn đề  
**Vấn đề hiện tại:**  
Các nền tảng thi trực tuyến hiện nay thiếu cơ chế giám sát tự động hiệu quả, dẫn đến tình trạng gian lận dễ dàng xảy ra. Các giải pháp giám sát có ứng dụng AI trên thị trường (như Proctorio, Respondus) thường có chi phí cấp phép rất đắt đỏ, tích hợp phức tạp, và đòi hỏi băng thông lớn hoặc tài nguyên máy chủ khổng lồ.

**Giải pháp:**  
AuraAcademic giải quyết bài toán này bằng cách xây dựng một hệ thống hoàn chỉnh:  
- **Frontend (React.js):** Lưu trữ tĩnh trên Amazon S3 và phân phối qua CloudFront, mang lại trải nghiệm mượt mà.  
- **Backend Core API (Spring Boot):** Chạy trên ECS Fargate (hoặc EC2) để xử lý logic đề thi, bài làm và xác thực.  
- **AI Proctoring (YOLOv8/Rekognition):** Chạy trên máy chủ EC2 GPU (sử dụng Spot Instance để tiết kiệm chi phí đến 70%) nhằm phân tích video stream thời gian thực (phát hiện quay cóp, rời khỏi khung hình, có người lạ...).  
- **Video Streaming:** Luồng video từ webcam qua WebRTC/WebSocket được gửi sang service AI để kiểm tra gian lận ngay tại thời điểm thi.  
- **Xác thực và Bảo mật:** Sử dụng Amazon Cognito cho đăng nhập, kết hợp AWS WAF bảo vệ API.  

**Lợi ích và điểm nổi bật:**  
Hệ thống tự động phát hiện hành vi gian lận, giảm thiểu tối đa sức lực giám thị truyền thống. Bằng cách sử dụng Spot Instance cho xử lý AI và kiến trúc Serverless/Container linh hoạt, chi phí vận hành được tối ưu đáng kể, phù hợp cho các trường đại học và tổ chức giáo dục.

---

### 3. Kiến trúc giải pháp  
AuraAcademic áp dụng kiến trúc Microservices trên AWS, phân tách rõ ràng giữa Core API và AI Processing.

**Dịch vụ AWS sử dụng:**  
- **Amazon S3 & CloudFront:** Lưu trữ và phân phối ứng dụng web Frontend (React.js) toàn cầu với tốc độ cao.  
- **Amazon Cognito:** Quản lý định danh và xác thực người dùng (giảng viên, sinh viên) bằng JWT.  
- **ALB (Application Load Balancer):** Định tuyến request REST API tới ECS hoặc EC2 Backend.  
- **Amazon ECS Fargate:** Chạy Spring Boot Backend container đóng gói các API cốt lõi.  
- **Amazon EC2 (Spot - GPU):** Chạy Python AI service xử lý luồng video camera từ thí sinh.  
- **AWS WAF:** Tường lửa bảo vệ ứng dụng khỏi các cuộc tấn công DDoS và web exploits thông dụng.  
- **Amazon SES:** Gửi email thông báo, xác nhận đăng ký và cảnh báo vi phạm cho thí sinh.  
- **VPC, Public/Private Subnets & NAT Gateway:** Đảm bảo phân tách mạng an toàn cho các dịch vụ.  
- **Dịch vụ ngoại vi:** MongoDB Atlas (Database), Google Gemini API (Sinh câu hỏi tự động / hỗ trợ Bedrock).  

**Thiết kế thành phần:**  
- **Giao diện Web:** Sinh viên làm bài thi và bật webcam giám sát; Giảng viên quản lý đề thi và xem báo cáo vi phạm.  
- **Core API:** Xử lý logic kỳ thi, xử lý bài đăng và xác nhận quyền qua JWT, kết nối tới Database.  
- **AI Engine:** Nhận stream camera qua WebSocket/WebRTC, nhận diện gian lận bằng YOLOv8 và tự động cập nhật cảnh báo về cho Core API.

---

### 4. Triển khai kỹ thuật  
**Các giai đoạn triển khai (Dự kiến thực tập 3 tháng):**  
- **Tháng 1 (Khởi tạo & Thiết kế):** Phân tích kiến trúc VPC, thiết lập database (MongoDB Atlas), chuẩn bị model YOLOv8/Bedrock.  
- **Tháng 2 (Phát triển Backend & AI):** Lập trình Spring Boot API, tích hợp Cognito, dựng service AI trên EC2 Spot.  
- **Tháng 3 (Hoàn thiện & Triển khai):** Xây dựng UI React.js, dựng hạ tầng S3 + CloudFront + WAF + ALB, kiểm thử tải và hoàn thiện tài liệu.  

**Yêu cầu kỹ thuật:**  
- **Frontend:** React.js, Tailwind CSS, Axios, WebRTC client.  
- **Backend:** Spring Boot, Spring Security, kết nối MongoDB Atlas.  
- **AI Processing:** Python, FastAPI, YOLOv8/OpenCV/Rekognition, xử lý stream camera thời gian thực.  
- **AWS Infrastructure:** S3, CloudFront, Cognito, ECS Fargate, EC2 Spot, ALB, WAF, SES, VPC.

---

### 5. Lộ trình & Mốc triển khai  
- **Tuần 1-2:** Phân tích thiết kế hệ thống, thiết kế sơ đồ VPC và luồng dữ liệu.  
- **Tuần 3-5:** Phát triển Core API với Spring Boot và cấu hình Cognito xác thực người dùng.  
- **Tuần 6-8:** Xây dựng Frontend UI và tích hợp luồng thi trực tuyến kèm AI Proctoring.  
- **Tuần 9-10:** Triển khai hạ tầng AWS (ECS Fargate, EC2 Spot, CloudFront, WAF) và kiểm thử end-to-end.  
- **Tuần 11-12:** Tối ưu hóa hiệu năng, đánh giá chi phí và viết báo cáo thực tập hoàn kết.

---

### 6. Ước tính ngân sách  
Sử dụng mô hình chi phí của AWS với chiến lược Spot Instance và Serverless cho môi trường thực tế (~100 sinh viên đồng thời):  
- **Frontend (S3 + CloudFront):** ~$1.00 USD/tháng (Free Tier / chi phí truyền tải rất thấp).  
- **ECS Fargate Spot (Backend):** ~$3.00 - 5.00 USD/tháng.  
- **EC2 GPU Spot (AI Engine - g4dn.xlarge):** ~$0.15 - 0.20 USD/giờ (chỉ bật khi có lịch thi, ước tính ~$8.00 - 12.00 USD/tháng).  
- **NAT Gateway (Tùy chọn / hoặc VPC Endpoints):** ~$10.00 - 15.00 USD/tháng.  
- **Application Load Balancer (ALB):** ~$16.00 USD/tháng.  
- **MongoDB Atlas:** ~$0.00 USD/tháng (Gói Free Tier M0).  
- **SES & WAF:** ~$2.00 USD/tháng.  
👉 **Tổng ước tính:** Khoảng **30 - 50 USD/tháng** (Có thể sử dụng AWS Credits để bao phủ hoàn toàn chi phí thực hành).

---

### 7. Đánh giá rủi ro  
**Ma trận rủi ro:**  
- **Spot Instance bị thu hồi đột ngột:** Ảnh hưởng: Trung bình | Khả năng xảy ra: Cao | *Ghi chú: Cần cấu hình Auto Scaling Group hoặc fallback sang On-Demand.*  
- **Độ trễ luồng camera lớn:** Ảnh hưởng: Trung bình | Khả năng xảy ra: Trung bình | *Ghi chú: Tối ưu độ phân giải khung hình và cấu hình WebSocket/WebRTC phù hợp.*  
- **Quá tải chi phí (Billing Surge):** Ảnh hưởng: Cao | Khả năng xảy ra: Thấp | *Ghi chú: Thiết lập CloudWatch Billing Alarms và tắt EC2 GPU ngay sau khi ca thi kết thúc.*  

**Chiến lược giảm thiểu:**  
- **Spot Instance:** Cấu hình Auto Scaling Group cùng chiến lược đa vùng (Multi-AZ) và đa loại instance, tự động chuyển sang On-Demand nếu Spot không khả dụng.  
- **Độ trễ camera:** Chỉ gửi các khung hình (frames) quan trọng hoặc nén luồng video xuống độ phân giải vừa đủ cho AI nhận diện.  
- **Chi phí AWS:** Đặt mức cảnh báo ngân sách AWS Budget và cấu hình tự động dừng máy chủ AI ngoài giờ thi.

---

### 8. Kết quả kỳ vọng  
- **Cải tiến kỹ thuật:** Cung cấp giải pháp giám sát thi tự động với độ chính xác cao bằng AI trên nền tảng AWS, tốc độ phản hồi nhanh và bảo mật tốt.  
- **Giá trị kinh nghiệm:** Nâng cao kỹ năng tự động hóa, thiết kế kiến trúc Cloud Microservices và vận hành hệ thống thực tế tối ưu chi phí cho môi trường giáo dục.