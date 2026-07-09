---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---


### Thời gian: 19/06 – 25/06

### Mục tiêu tuần 10:
* Thực hành Machine Learning với Amazon SageMaker Studio (Jupyter Notebook).
* Xử lý thị giác máy tính với Amazon Rekognition, trích xuất văn bản OCR với Amazon Textract và phân tích cảm xúc với Amazon Comprehend.
* Xây dựng chatbot đa phương tiện với Amazon Lex và Amazon Polly.
* Phân tích dữ liệu thời gian thực với Amazon Kinesis Data Streams và Data Warehouse Amazon Redshift.
* Triển khai web app với AWS Elastic Beanstalk, tối ưu caching với Amazon ElastiCache (Redis) và điều phối workflow với AWS Step Functions.
* Định tuyến mạng biên với AWS Global Accelerator, truy cập an toàn qua SSM Session Manager và quản lý bảo mật nâng cao với KMS, CloudTrail, GuardDuty, Macie.

### Các công việc cần triển khai trong tuần này:
| STT | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **1** | Thực hành thiết lập môi trường máy học với Amazon SageMaker Studio, chạy thử nghiệm Jupyter Notebook để xử lý các tập dữ liệu mẫu. | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **2** | Khởi tạo luồng xử lý thị giác máy tính với Amazon Rekognition để tự động nhận diện khuôn mặt và gắn thẻ (tagging) hình ảnh. | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **3** | Tích hợp Amazon Textract để trích xuất văn bản từ tài liệu PDF (OCR), kết hợp với Amazon Comprehend để phân tích cảm xúc và từ khóa của đoạn văn. | 20/06/2026 | 20/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **4** | Xây dựng chatbot tương tác đa phương tiện bằng cách kết hợp Amazon Lex (xử lý ngôn ngữ tự nhiên) và Amazon Polly (chuyển đổi văn bản thành giọng nói). | 20/06/2026 | 20/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **5** | Phân tích luồng dữ liệu thời gian thực (Real-time streaming) thông qua kiến trúc của Amazon Kinesis Data Streams. | 21/06/2026 | 21/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **6** | Thực hành tải dữ liệu vào kho dữ liệu quy mô lớn (Data Warehouse) bằng Amazon Redshift và thực thi các truy vấn phân tích. | 21/06/2026 | 21/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **7** | Triển khai nhanh ứng dụng web thông qua nền tảng AWS Elastic Beanstalk, tự động hóa quá trình cấp phát tài nguyên tính toán. | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **8** | Tối ưu hóa tốc độ truy xuất dữ liệu bằng cách thiết lập bộ nhớ đệm (In-memory caching) với Amazon ElastiCache (sử dụng engine Redis). | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **9** | Điều phối (Orchestrate) các luồng quy trình phức tạp, kết nối nhiều hàm tính toán độc lập thành một workflow trực quan bằng AWS Step Functions. | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **10** | Đẩy nhanh tốc độ phân phối ứng dụng toàn cầu và giảm độ trễ bằng cách định tuyến lưu lượng qua mạng biên với AWS Global Accelerator. | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **11** | Sử dụng AWS Systems Manager (SSM) Session Manager để thiết lập kết nối an toàn vào máy chủ mà không cần mở cổng SSH (Port 22) ra môi trường internet. | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **12** | Quản lý vòng đời mã hóa dữ liệu với AWS KMS (Key Management Service), thực hành tự tạo và tự động xoay vòng khóa (CMK). | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| **13** | Thiết lập theo dõi dấu vết kiểm toán (Audit trail) cho toàn bộ tài khoản với AWS CloudTrail, kết hợp phát hiện mối đe dọa bằng Amazon GuardDuty và Amazon Macie. | 25/06/2026 | 25/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 10:

* Thiết lập SageMaker Studio hoàn chỉnh, chạy thành công Notebook xử lý và huấn luyện trên tập dữ liệu mẫu.
* Xây dựng pipeline tự động phân tích ảnh, nhận diện chính xác đối tượng và khuôn mặt.
* Trích xuất thành công văn bản từ PDF/ảnh bằng Textract và đưa vào Comprehend phân tích chính xác ngữ điệu, từ khóa chính.
* Tạo thành công Chatbot AI có khả năng hiểu hội thoại tự nhiên (Lex) và phát âm phản hồi bằng giọng nói tự nhiên (Polly).
* Thiết lập luồng Kinesis nhận và xử lý hàng nghìn sự kiện/giây theo thời gian thực với độ trễ cực thấp.
* Tạo cụm Redshift, tải tập dữ liệu lớn và thực hiện các câu truy vấn phân tích phức tạp với tốc độ cao.
* Deploy ứng dụng lên Elastic Beanstalk chỉ qua vài thao tác, hệ tự động cấu hình EC2, Load Balancer và Auto Scaling.
* Tích hợp ElastiCache Redis giúp giảm tải cho database chính, tăng tốc thời gian phản hồi API dưới 10ms.
* Vẽ và chạy thành công state machine trên Step Functions điều phối tuần tự các hàm Lambda xử lý đơn hàng/dữ liệu.
* Cấu hình Global Accelerator giúp tối ưu đường đi của gói tin qua mạng cáp quang riêng của AWS, giảm độ trễ đáng kể.
* Truy cập terminal EC2 trực tiếp trên trình duyệt qua Session Manager an toàn tuyệt đối, đóng hoàn toàn cổng 22.
* Tạo Customer Managed Key (CMK) trong KMS để mã hóa dữ liệu EBS/S3 và cấu hình tự động xoay vòng khóa định kỳ.
* Kích hoạt CloudTrail ghi log toàn bộ API calls, bật GuardDuty phát hiện hành vi bất thường và Macie quét bảo vệ dữ liệu nhạy cảm trên S3.



