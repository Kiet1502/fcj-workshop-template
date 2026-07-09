---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---



# Đảm bảo truy cập Hybrid an toàn đến S3 bằng cách sử dụng VPC endpoint

#### Tổng quan

**AWS PrivateLink** cung cấp kết nối riêng tư đến các dịch vụ aws từ VPCs hoặc trung tâm dữ liệu (on-premise) mà không làm lộ lưu lượng truy cập ra ngoài public internet.

Trong bài lab này, chúng ta sẽ học cách tạo, cấu hình, và kiểm tra VPC endpoints để cho phép workload của bạn tiếp cận các dịch vụ AWS mà không cần đi qua Internet công cộng.

Chúng ta sẽ tạo hai loại endpoints để truy cập đến Amazon S3: gateway vpc endpoint và interface vpc endpoint. Hai loại vpc endpoints này mang đến nhiều lợi ích tùy thuộc vào việc bạn truy cập đến S3 từ môi trường cloud hay từ trung tâm dữ liệu (on-premise).
+ **Gateway** - Tạo gateway endpoint để gửi lưu lượng đến Amazon S3 hoặc DynamoDB using private IP addresses. Bạn điều hướng lưu lượng từ VPC của bạn đến gateway endpoint bằng các bảng định tuyến (route tables)
+ **Interface** - Tạo interface endpoint để gửi lưu lượng đến các dịch vụ điểm cuối (endpoints) sử dụng Network Load Balancer để phân phối lưu lượng. Lưu lượng dành cho dịch vụ điểm cuối được resolved bằng DNS.

#### Nội dung

1. [Tổng quan về workshop](5.1-Workshop-overview/)
2. [Chuẩn bị](5.2-Prerequiste/)
3. [Truy cập đến S3 từ VPC](5.3-S3-vpc/)
4. [Truy cập đến S3 từ TTDL On-premises](5.4-S3-onprem/)
5. [VPC Endpoint Policies (làm thêm)](5.5-Policy/)
6. [Dọn dẹp tài nguyên](5.6-Cleanup/)

---

### Kết quả đạt được & Giá trị thực chiến (Workshop Outcomes & Key Takeaways)

Hoàn thành chuỗi bài thực hành **VPC Endpoint (AWS PrivateLink) cho Amazon S3**, học viên/kỹ sư đạt được các năng lực kỹ thuật và giá trị vận hành chuyên sâu sau:

#### 1. Năng lực Kỹ thuật & Kiến trúc đạt được (Technical Mastery)
* **Làm chủ kiến trúc Hybrid Cloud an toàn:** Hiểu sâu và thiết kế thành công mô hình kết nối bảo mật tuyệt đối giữa Trung tâm dữ liệu doanh nghiệp (On-premises / VPN Site-to-Site) và hệ sinh thái AWS Cloud.
* **Phân biệt & Triển khai 2 loại VPC Endpoint cho S3:**
  - **Gateway VPC Endpoint:** Thiết lập bảng định tuyến (Route Tables) điều hướng lưu lượng từ các EC2/Workload nội bộ trong VPC đến Amazon S3 bằng địa chỉ IP riêng (Private IP), với chi phí điểm cuối hoàn toàn **miễn phí (0 USD)**.
  - **Interface VPC Endpoint (AWS PrivateLink):** Sử dụng các Private IP trong Subnet và cấu hình phân giải DNS nội bộ để cho phép các máy chủ từ On-premises truy cập S3 một cách riêng tư mà không cần đi qua Internet công cộng hay VPN NAT.
* **Kiểm soát bảo mật tầng điểm cuối (VPC Endpoint Policies):** Viết và áp dụng thành công các chính sách IAM trên VPC Endpoint (Endpoint Policies), chỉ cho phép truy cập vào các S3 Bucket hợp lệ của tổ chức và chặn đứng mọi nỗ lực kết nối đến các S3 Bucket bên ngoài (chống thất thoát dữ liệu - **Data Exfiltration Prevention**).

#### 2. Giá trị Vận hành & Tối ưu hóa (Operational Value & Optimization)
* **Bảo mật tuyệt đối (Zero-Trust Network):** Loại bỏ hoàn toàn sự phụ thuộc vào Internet Gateway, NAT Gateway hay địa chỉ IP công cộng (Public IP) khi giao tiếp với Amazon S3, giảm thiểu tối đa diện tích tấn công mạng (DDoS, Man-in-the-Middle).
* **Tối ưu chi phí truyền dữ liệu (Data Transfer Cost Reduction):** Giảm đáng kể chi phí băng thông (NAT Gateway Data Processing Fee ~0.045 USD/GB) cho các hệ thống có lưu lượng đọc/ghi dữ liệu lớn trên S3 (như Big Data, Backup, Log Analytics).
* **Tăng tốc độ & Độ trễ ổn định:** Đường truyền dữ liệu đi qua hạ tầng mạng riêng trục chính (AWS Global Network) với băng thông cao và độ trễ thấp, đảm bảo hiệu suất tối đa cho các ứng dụng nghiệp vụ cốt lõi.