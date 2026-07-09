---
title: "Các bài blogs đã viết & chia sẻ"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Tại chuyên mục này là tổng hợp **3 bài blog kỹ thuật thực tế** mà nhóm chúng tôi đã nghiên cứu, biên soạn và chia sẻ thành công lên cộng đồng **AWS Study Group Vietnam** trong quá trình thực tập First Cloud Journey (FCJ) và phát triển dự án thực tế **Aura Academic | Smart Exam Engine**:

---

### [Blog 1 - Hành trình xây dựng Nền tảng Thi trực tuyến & Giám sát AI trên AWS Cloud (Serverless Architecture)](3.1-Blog1/)
* **Link bài viết gốc trên Facebook:** [Đọc bài viết trên cộng đồng AWS Study Vietnam](https://www.facebook.com/share/p/1D6dVxB4R3/?)  
* **Tóm tắt nội dung:** Chia sẻ hành trình kiến thiết và vận hành dự án thực tế **Aura Academic | Smart Exam Engine**. Bài viết tập trung vào việc áp dụng kiến trúc Cloud-Native và Serverless để tối ưu chi phí và hiệu suất: dùng **Amazon S3** và **Amazon CloudFront** để hosting static frontend với độ trễ siêu thấp, sử dụng **AWS Lambda** kết hợp **Amazon API Gateway** và **Amazon DynamoDB** để xử lý hàng nghìn request nộp bài/chấm điểm đồng thời mà không cần duy trì máy chủ vật lý (**Pay-as-you-go**).

---

### [Blog 2 - Tích hợp Trí tuệ Nhân tạo (Generative AI & Computer Vision) trong hệ thống Giám sát phòng thi](3.2-Blog2/)
* **Link bài viết gốc trên Facebook:** [Đọc bài viết trên cộng đồng AWS Study Group](https://www.facebook.com/photo/?fbid=1676460976896951&set=gm.2201043733993920&idorvanity=660548818043427)  
* **Tóm tắt nội dung:** Đào sâu vào cách tích hợp các dịch vụ AI/ML mạnh mẽ của AWS vào dự án EdTech thực tế. Chi tiết quy trình sử dụng **Amazon Bedrock** (LLMs) cho tính năng **Exam Builder** giúp tự động trích xuất kiến thức từ tài liệu DOCX/PDF thành ma trận đề thi chuẩn xác chỉ trong vài giây; đồng thời ứng dụng **Amazon Rekognition** (Computer Vision) để xây dựng hệ thống **AI Proctoring** nhận diện đa nhân diện, phát hiện gian lận real-time trong phòng thi bảo mật (**Secure Room**).

---

### [Blog 3 - Tự động hóa CI/CD Pipeline, Giám sát CloudWatch và Bảo mật Zero-Trust trên AWS](3.3-Blog3/)
* **Link bài viết gốc trên Facebook:** [Đọc bài viết trên cộng đồng AWS Study Vietnam](https://www.facebook.com/share/p/18uKARgWds/?)  
* **Tóm tắt nội dung:** Đúc kết kinh nghiệm từ các bài thực hành Lab chuyên sâu trong chương trình thực tập First Cloud Journey (FCJ). Bài viết hướng dẫn chi tiết cách thiết lập luồng CI/CD tự động hoá với **AWS CodePipeline & CodeBuild**, cấu hình tường lửa **AWS WAF** và **Amazon Route 53** bảo vệ API khỏi các lỗ hổng OWASP Top 10, cùng với việc xây dựng hệ thống giám sát thời gian thực bằng **Amazon CloudWatch Dashboard/Alarms** kết hợp thông báo qua **Amazon SNS**.