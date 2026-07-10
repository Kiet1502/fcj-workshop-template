---
title : "Truy cập S3 từ VPC"
date : 2024-01-01 
weight : 3
chapter : false
pre : " <b> 6.3. </b> "
---

#### Sử dụng Gateway endpoint

Trong phần này, bạn sẽ tạo một Gateway endpoint để truy cập Amazon S3 từ một EC2 instance. Gateway endpoint sẽ cho phép tải một object lên S3 bucket mà không cần sử dụng Internet Công cộng. Để tạo endpoint, bạn phải chỉ định VPC mà bạn muốn tạo endpoint và dịch vụ (trong trường hợp này là S3) mà bạn muốn thiết lập kết nối.

![overview](/images/5-Workshop/5.3-S3-vpc/diagram2.png)

#### Nội dung

- [Tạo gateway endpoint](3.1-create-gwe/)
- [Test gateway endpoint](3.2-test-gwe/)

---

### Kết quả đạt được sau bước này (Step Outcomes)
* **Khởi tạo Gateway VPC Endpoint cho S3:** Thiết lập thành công Gateway Endpoint (`com.amazonaws.us-east-1.s3`) gắn trực tiếp vào bảng định tuyến (Route Table) của `VPC Cloud`.
* **Kiểm thử kết nối nội bộ thành công:** Đã tải thử nghiệm object lên S3 bucket từ EC2 Instance trong `VPC Cloud` hoàn toàn thông qua dải địa chỉ IP nội bộ, chứng minh lưu lượng không hề đi ra Internet công cộng hay đi qua NAT Gateway.
* **Tối ưu chi phí:** Khôi phục độ trễ mạng thấp tối đa cho ứng dụng nội bộ với mức phí điểm cuối bằng 0 (Gateway Endpoint không tốn phí duy trì giờ máy hay phí xử lý dữ liệu).
