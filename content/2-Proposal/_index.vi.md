---
title: "Bản đề xuất"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Aura Academic | Smart Exam Engine  
## Nền Tảng Thi Trực Tuyến & Giám Sát Tự Động Hóa Bằng Trí Tuệ Nhân Tạo Trên AWS Cloud  

*Sản phẩm được phát triển và triển khai thực tế tại link:* [Aura Academic Frontend AWS S3 Hosting](http://aura-academic-fe-2024.s3-website-ap-southeast-1.amazonaws.com/vi/)

---

### 1. Tóm tắt điều hành (Executive Summary)  
**Aura Academic (Smart Exam Engine)** là nền tảng thi trắc nghiệm trực tuyến thông minh thế hệ mới, được nhóm chúng tôi phát triển nhằm giải quyết triệt để bài toán bảo mật, giám sát gian lận và tối ưu hóa quy trình tổ chức thi cử cho các trường đại học, trường phổ thông, trung tâm đào tạo và giảng viên. Nền tảng tích hợp sâu các công nghệ Trí tuệ nhân tạo (**AI Proctoring**, **Generative AI**) và được xây dựng trên kiến trúc **AWS Cloud & Serverless** hiện đại, đảm bảo tính khả mở cao (high scalability), độ trễ cực thấp và chi phí vận hành tối ưu.  

### 2. Tuyên bố vấn đề (Problem Statement)  
* **Vấn đề hiện tại:**  
  - **Giám sát lỏng lẻo:** Các kỳ thi trực tuyến hiện nay thường thiếu cơ chế giám sát chặt chẽ, dễ xảy ra tình trạng gian lận (nhờ người thi hộ, tra cứu tài liệu trái phép, rời khỏi vùng camera, mở tab/ứng dụng khác).  
  - **Biên soạn đề thi thủ công:** Giảng viên mất hàng giờ đồng hồ để trích xuất, định dạng và tạo ngân hàng câu hỏi từ các tài liệu thô (DOCX, PDF) hoặc sách giáo khoa.  
  - **Hạ tầng truyền thống dễ quá tải:** Các hệ thống quản lý thi (LMS) cũ thường bị nghẽn mạng hoặc sập server khi hàng nghìn sinh viên truy cập làm bài đồng thời, thiếu báo cáo phân tích chuyên sâu sau kỳ thi.  

* **Giải pháp đột phá - Aura Academic:**  
  - **AI Camera / Proctoring AI Đỉnh Cao:** Ứng dụng công nghệ Computer Vision để nhận diện khuôn mặt thời gian thực, phát hiện đa nhân diện, đổi người thi, rời khỏi camera hoặc xuất hiện tạp âm bất thường trong phòng thi khép kín (**Secure Room**).  
  - **Exam Builder / Biên Soạn Đề Thi Siêu Tốc:** Tích hợp mô hình ngôn ngữ lớn (**LLMs / Generative AI**) cho phép tự động trích xuất kiến thức từ tài liệu DOCX, PDF và tạo ma trận đề thi phân hóa chỉ với 1 lần chạm.  
  - **Auto Report & Phân Tích Phổ Điểm:** Hệ thống chấm điểm tự động tức thì, thống kê nhật ký kiểm toán (**Audit Logs**) minh bạch và trực quan hóa phổ điểm chi tiết bằng biểu đồ động giúp giảng viên đánh giá chất lượng câu hỏi.  

* **Lợi ích & Hoàn vốn đầu tư (Benefits & ROI):**  
  - Tiết kiệm tới **80%** thời gian chuẩn bị đề thi và chấm điểm cho giảng viên.  
  - Đảm bảo **99%** sự công bằng, minh bạch và bảo mật trong các kỳ thi trực tuyến.  
  - Tận dụng kiến trúc Cloud Native & Serverless của AWS (Amazon S3, CloudFront, Lambda, Bedrock...) giúp giảm chi phí đầu tư phần cứng ban đầu, chỉ trả phí theo lưu lượng sử dụng thực tế (**Pay-as-you-go**).  

### 3. Kiến trúc giải pháp (Solution Architecture & AWS Cloud Integration)  
Hệ thống **Aura Academic** áp dụng kiến trúc Serverless hiện đại trên hệ sinh thái Amazon Web Services (AWS), cho phép dễ dàng chịu tải hàng nghìn thí sinh thi đồng thời mà không cần quản lý máy chủ vật lý:  

* **Frontend Hosting & CDN:**  
  - Giao diện người dùng (xây dựng bằng Next.js/React hiện đại, hỗ trợ Dark Mode/Light Mode mượt mà) được đóng gói và triển khai hosting tĩnh trên **Amazon S3**.  
  - Kết hợp với mạng biên phân phối nội dung toàn cầu **Amazon CloudFront**, đảm bảo tốc độ tải trang cực kỳ nhanh và chống tấn công DDoS hiệu quả (tên miền trực tiếp đang live: `http://aura-academic-fe-2024.s3-website-ap-southeast-1.amazonaws.com/vi/`).  

* **AI & Machine Learning Layer:**  
  - **Amazon Bedrock:** Cung cấp các mô hình Foundation Models (FMs/LLMs) tiên tiến phục vụ module **Exam Builder** (tự động phân tích nội dung tài liệu học tập, sinh câu hỏi trắc nghiệm và giải thích đáp án).  
  - **Amazon Rekognition:** Xử lý và nhận diện luồng video/hình ảnh thời gian thực từ webcam của thí sinh (**AI Proctoring**), tự động chốt lỗi vi phạm khi có dấu hiệu gian lận.  

* **Serverless Backend Layer:**  
  - **AWS Lambda & Amazon API Gateway:** Xử lý toàn bộ logic nghiệp vụ (quản lý mã phòng thi, xác thực kết nối, nộp bài, tính điểm) dưới dạng kiến trúc microservices không máy chủ.  
  - **Amazon DynamoDB:** Cơ sở dữ liệu NoSQL với độ trễ phản hồi dưới mili giây, lưu trữ ngân hàng câu hỏi, trạng thái phòng thi real-time và Audit Logs.  
  - **Amazon S3 (Data Storage):** Lưu trữ an toàn tài liệu đề thi gốc và các hình ảnh chụp minh chứng vi phạm của thí sinh trong kỳ thi.  

* **Security & Identity:**  
  - **Amazon Cognito:** Quản lý định danh và bảo mật đăng nhập cho các nhóm đối tượng (Giảng viên, Sinh viên, Quản trị viên nhà trường).  

### 4. Triển khai kỹ thuật & Quy trình vận hành khép kín  
* **Quy trình 4 bước toàn diện của Aura Academic:**  
  1. **Khởi tạo & Tạo đề (Exam Builder):** Giảng viên tải tài liệu lên hệ thống hoặc sử dụng ngân hàng câu hỏi có sẵn; AI tự động gợi ý ma trận đề thi chuẩn xác.  
  2. **Thiết lập phòng thi bảo mật (Secure Room):** Giảng viên tạo phòng thi, cài đặt các quy tắc giám sát (yêu cầu camera, micrô, khóa chuyển tab) và gửi mã phòng cho sinh viên.  
  3. **Vận hành & Giám sát AI (Live Exams & AI Proctoring):** Thí sinh truy cập phòng thi; hệ thống AI theo dõi liên tục thời gian thực, ghi nhận sự cố mất kết nối và tự động khôi phục bài làm an toàn.  
  4. **Báo cáo & Phân tích (Auto Report & Smart Grading):** Ngay sau khi kết thúc giờ làm bài, hệ thống xuất báo cáo phổ điểm, danh sách thí sinh vi phạm kèm hình ảnh minh chứng cụ thể.  

### 5. Lộ trình & Mốc triển khai (Khớp với lộ trình thực tập AWS 11 Tuần)  
- **Giai đoạn 1 (Tuần 1 – Tuần 3):** Khảo sát yêu cầu bài toán, thiết kế giao diện UI/UX trực quan và triển khai hosting Frontend lên **Amazon S3 + CloudFront**.  
- **Giai đoạn 2 (Tuần 4 – Tuần 7):** Nghiên cứu chuyên sâu và tích hợp các dịch vụ AI/ML của AWS (**Amazon Bedrock** cho tạo đề thi, **Amazon Rekognition** cho giám sát camera).  
- **Giai đoạn 3 (Tuần 8 – Tuần 10):** Hoàn thiện Backend Serverless (**AWS Lambda, API Gateway, DynamoDB**), xây dựng hệ thống phòng thi bảo mật (Secure Room) và luồng tự động hóa CI/CD.  
- **Giai đoạn 4 (Tuần 11 & Tương lai):** Kiểm thử chịu tải thực tế, hoàn thiện tài liệu kiến trúc, đóng góp bài viết cho cộng đồng AWS Study Group và sẵn sàng đưa hệ thống vào ứng dụng tại các trường học.  

### 6. Ước tính ngân sách hạ tầng (Budget Estimation on AWS Cloud)  
Nhờ tận dụng tối đa kiến trúc Serverless và gói tài nguyên **AWS Free Tier / Credits**, chi phí vận hành hệ thống được tối ưu ở mức thấp nhất:  
- **Amazon S3 & CloudFront (Frontend hosting & CDN):** ~1.50 USD/tháng.  
- **AWS Lambda & API Gateway (Backend API):** ~0.50 USD/tháng (trong hạn mức miễn phí hàng triệu request).  
- **Amazon DynamoDB (NoSQL Database):** ~1.00 USD/tháng (On-Demand capacity mode).  
- **Amazon Bedrock & Rekognition (AI Services):** ~5.00 – 15.00 USD/tháng (tùy theo tần suất sinh đề thi tự động và số lượng sinh viên thi đồng thời).  
- **Tổng chi phí dự kiến cho môi trường Lab / Triển khai thực tế quy mô vừa:** **~8.00 – 18.00 USD/tháng**, tiết kiệm hơn 85% so với việc thuê và duy trì các máy chủ riêng (Dedicated Server / VPS) truyền thống.  

### 7. Đánh giá rủi ro & Kế hoạch giảm thiểu (Risk Assessment & Mitigation)  
- **Rủi ro rớt mạng/mất kết nối của thí sinh:** Hệ thống tích hợp cơ chế lưu dữ liệu bài làm tự động xuống bộ nhớ trình duyệt (Local Storage / IndexedDB) và tự động đồng bộ ngay lập tức khi đường truyền internet được khôi phục.  
- **Rủi ro nhận diện nhầm của AI Proctoring:** AI đóng vai trò giám sát, cờ báo (flagging) và lưu trữ bằng chứng (log/hình ảnh); quyền quyết định xử lý kỷ luật cuối cùng luôn thuộc về giảng viên để đảm bảo tính công bằng tuyệt đối.  

### 8. Kết quả kỳ vọng & Giá trị dài hạn  
* **Cải tiến kỹ thuật:** Thay thế hoàn toàn quy trình coi thi, ra đề và chấm thi thủ công bằng giải pháp công nghệ tự động hóa độ trễ thấp trên AWS.  
* **Giá trị dài hạn:** Xây dựng hệ sinh thái công nghệ giáo dục (EdTech) tiên tiến, tạo tiền đề mở rộng tích hợp cho hàng trăm trường học và cơ sở đào tạo trên toàn quốc.