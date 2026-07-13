---
title: "Worklog Tuần 3"
date: 2026-05-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Tìm hiểu cơ chế kết nối nâng cao giữa các VPC (VPC Peering và Transit Gateway).
* Thực hành kết nối SSH tới máy chủ trong Private Subnet qua Bastion Host.
* Triển khai các dịch vụ kết nối mạng hiện đại: NAT Gateway và EC2 Instance Connect Endpoint.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Học Module 02_02: VPC Peering (kết nối trực tiếp giữa các VPC) và Transit Gateway (kết nối tập trung nhiều VPC/tài khoản).<br>- Cách cấu hình route table để định tuyến kết nối giữa các VPC. | 01/05/2026   | 01/05/2026      | <https://youtu.be/BPuD1l2hEQ4> |
| 2   | - Thực hành Lab 03-04: Tạo EC2 trong Public/Private subnet.<br>- Cấu hình keypair và thiết lập cơ bản cho máy chủ EC2. | 02/05/2026   | 02/05/2026      | <https://000003.awsstudygroup.com/4-prerequisite/> |
| 3   | - Thực hành Lab 03-04: Kết nối SSH tới máy chủ Private qua Bastion Host.<br>- Cấu hình Route Table để EC2 Private ra ngoài Internet qua Internet Gateway. | 03/05/2026   | 03/05/2026      | <https://000003.awsstudygroup.com/4-prerequisite/> |
| 4   | - Thực hành Lab 03-04: Tạo và cấu hình NAT Gateway để EC2 Private truy cập Internet.<br>- Thiết lập EC2 Instance Connect Endpoint để quản lý kết nối an toàn. | 04/05/2026   | 04/05/2026      | <https://000003.awsstudygroup.com/4-prerequisite/> |
| 5   | - Tiếp tục thực hành Lab 03-04: Kiểm tra kết nối terminal tới EC2 Private thông qua EC2 Instance Connect Endpoint. | 04/05/2026   | 04/05/2026      | <https://000003.awsstudygroup.com/4-prerequisite/> |
| 6   | - Thực hành Lab 03-19: Setup VPC Peering kết nối 2 VPC.<br>- Cấu hình Security Group, NACL và Route Table để cho phép giao tiếp giữa 2 VPC; dọn dẹp tài nguyên sau thực hành. | 05/05/2026   | 05/05/2026      | <https://000003.awsstudygroup.com/3-prerequisite/> |

### Kết quả đạt được tuần 3:

* Nắm vững cách kết nối mạng giữa các VPC thông qua VPC Peering và Transit Gateway.
* Thành thạo kỹ thuật SSH tới private instance thông qua Bastion Host.
* Hiểu và triển khai thực tế NAT Gateway để đảm bảo private instance truy cập được internet.
* Triển khai thành công kết nối an toàn với EC2 Instance Connect Endpoint.
* Thực hành cấu hình đồng bộ Routing, Security Group và NACL để cho phép liên lạc an toàn giữa các VPC khác nhau.