---
title : "Kiểm tra DynamoDB, indexes và PITR"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5 </b> "
---

### Mục tiêu
Phần này kiểm tra các bảng DynamoDB của TaskManager, index phục vụ truy vấn và cấu hình Point-in-Time Recovery (PITR).

### Kiểm tra danh sách bảng DynamoDB
1. Mở **Amazon DynamoDB** console.
2. Chọn **Tables**.
3. Kiểm tra các bảng có prefix `TaskManager`.

![Hình](/images/5.5a-dynamodb.png)

Các bảng chính bao gồm:
* `TaskManager-ActivityLogs-dev`
* `TaskManager-Boards-dev`
* `TaskManager-Notifications-dev`
* `TaskManager-Tasks-dev`
* `TaskManager-Users-dev`

Các bảng đều ở trạng thái **Active** và sử dụng capacity mode **On-demand**, phù hợp với workload chưa ổn định vì không cần cấu hình read/write capacity thủ công.

### Kiểm tra Global Secondary Index
Mở bảng `TaskManager-Users-dev`, chọn tab **Indexes**.

![Hình](/images/5.5b-indextables.png)

Trong ảnh, bảng `TaskManager-Users-dev` có GSI:
* **Index name:** `EmailIndex`
* **Partition key:** `email`
* **Status:** Active
* **Capacity:** On-demand

Index này giúp hệ thống tìm user theo email nhanh hơn mà không phải scan toàn bộ bảng.

### Kiểm tra PITR trên từng bảng
Point-in-Time Recovery giúp DynamoDB giữ continuous backup tối đa 35 ngày. Tính năng này hữu ích khi dữ liệu bị ghi sai hoặc xóa nhầm.

![Hình](/images/5.5c-pitr-edit.png)

Trong màn hình **Edit point-in-time recovery settings**, PITR được bật với backup recovery period là 35 ngày.
##### Board table
![Hình](/images/5.5d-pitr-board.png)

* **Bảng `TaskManager-Boards-dev`:**
    * Partition key: `boardId`
    * Capacity mode: On-demand
    * Table status: Active
    * PITR: On

##### Task table
![Hình](/images/5.5e-pitr-tasks.png)

* **Bảng `TaskManager-Tasks-dev`:**
    * Partition key: `boardId`
    * Sort key: `taskId`
    * Capacity mode: On-demand
    * Table status: Active
    * PITR: On    

##### User table
![Hình](/images/5.5f-pitr-users.png)

* **Bảng `TaskManager-Users-dev`:**
    * Partition key: `userId`
    * Capacity mode: On-demand
    * Table status: Active
    * PITR: On

### Kết luận
DynamoDB đã được cấu hình đúng cho TaskManager: nhiều bảng tách theo domain, có index phục vụ truy vấn email, dùng on-demand capacity và bật PITR cho các bảng quan trọng.