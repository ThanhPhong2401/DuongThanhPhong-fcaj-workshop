---
title: "Worklog Tuần 2"
date: 2026-04-24
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Tìm hiểu lý thuyết cốt lõi về dịch vụ mạng AWS VPC (Virtual Private Cloud) và các tính năng đi kèm.
* Phân biệt các loại tường lửa bảo mật trong hệ thống mạng AWS (Security Group và NACL).
* Thực hành khởi tạo hạ tầng mạng cơ bản (VPC, Subnet, Route Table, Internet Gateway) trên AWS Console.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Học Module 02_01: AWS VPC. Tìm hiểu vai trò môi trường mạng ảo riêng tư, độc lập trên Cloud.<br>- Lựa chọn Region Singapore để tối ưu độ trễ cho người dùng Việt Nam.<br>- Tìm hiểu quy tắc cấu hình CIDR IPv4/IPv6 và thiết lập VPC bao phủ tối thiểu 3 AZ. | 24/04/2026   | 24/04/2026      | <https://youtu.be/O9Ac_vGHquM?si=w4rXO8E9eY7so_Og> |
| 2   | - Tiếp tục học về VPC Subnet (Lớp mạng con) để phân chia hệ thống và kiểm soát bảo mật.<br>- Phân biệt và hiểu rõ công dụng của Public Subnet (có Internet, chạy Web server) và Private Subnet (không có Internet, chạy Database). | 25/04/2026   | 25/04/2026      | <https://youtu.be/O9Ac_vGHquM?si=w4rXO8E9eY7so_Og> |
| 3   | - Nghiên cứu tính năng Route Table (Bảng định tuyến) để chỉ đường cho các gói tin trong Public và Private Subnet.<br>- Tìm hiểu về Route Table mặc định của VPC (cho phép các subnet giao tiếp nội bộ với nhau). | 26/04/2026   | 26/04/2026      | <https://youtu.be/O9Ac_vGHquM?si=w4rXO8E9eY7so_Og> |
| 4   | - Tìm hiểu các thành phần kết nối mạng cốt lõi khác: ENI (Card mạng ảo gán cho EC2), VPC Endpoint, Internet Gateway (Cổng Internet) và NAT Gateway (Cổng dịch địa chỉ mạng). | 27/04/2026   | 27/04/2026      | <https://youtu.be/O9Ac_vGHquM?si=fI-T6CMmJfzIVo4> |
| 5   | - **Thực hành Lab 03 - Module 02:** Tự tay triển khai xây dựng sơ đồ mạng cơ bản trên AWS Console bao gồm: Tạo VPC, Tạo các Subnet, Tạo Route Table và Cấu hình Internet Gateway. | 28/04/2026   | 28/04/2026      | <https://000003.awsstudygroup.com/3-prerequisite/> |
| 6   | - Học Module 02_02: VPC Security. Tìm hiểu sâu về tường lửa **Security Group**.<br>- Nắm rõ tính chất Stateful (lưu trạng thái), áp dụng lên ENI, mặc định chặn mọi inbound rules và cho phép outbound rules. | 29/04/2026   | 29/04/2026      | <https://youtu.be/BPuD1l2hEQ4?si=YwiJjhpn0Nngdf8r> |
| 7   | - Tìm hiểu loại tường lửa thứ hai: **Network ACL (NACL)**.<br>- Nắm rõ tính chất Stateless (không lưu trạng thái, phải cấu hình cả 2 chiều), áp dụng ở cấp độ Subnet, mặc định mở tất cả và quét rule từ trên xuống dưới. | 30/04/2026   | 30/04/2026      | <https://youtu.be/BPuD1l2hEQ4?si=YwiJjhpn0Nngdf8r> |

### Kết quả đạt được tuần 2:

* Hiểu cách vận hành VPC làm môi trường mạng ảo, nắm vững thiết lập CIDR và đa vùng (3 AZs) tại Singapore.
* Phân biệt rõ mục đích và cách cấu hình giữa Public Subnet và Private Subnet trong hệ thống.
* Nắm vững cơ chế điều hướng gói tin của Route Table và cách kết nối Internet qua Internet Gateway.
* Phân biệt được tính chất Stateful của Security Group (tầng tài nguyên) và Stateless của NACL (tầng subnet).
* Thực hành thành công Lab 03, khởi tạo hạ tầng mạng cơ bản gồm VPC, Subnet, Route Table và Internet Gateway.