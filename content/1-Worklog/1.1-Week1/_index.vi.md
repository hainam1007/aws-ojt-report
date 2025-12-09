---
title: "Worklog Tuần 1"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 1:
* Làm quen với team First Cloud Journey
* Học AWS cơ bản và thiết lập môi trường

### Các công việc đã thực hiện:

| Thứ | Công việc | Ngày | Trạng thái |
|-----|-----------|------|------------|
| Hai | - Gặp gỡ team FCJ <br> - Đọc hướng dẫn thực tập <br> - Setup môi trường dev | 04/11/2025 | ✅ Hoàn thành |
| Ba | - Học các nhóm dịch vụ AWS (Compute, Storage, Networking, Database) <br> - Tìm hiểu cơ sở hạ tầng toàn cầu AWS | 05/11/2025 | ✅ Hoàn thành |
| Tư | - Tạo tài khoản AWS Free Tier <br> - Thiết lập MFA <br> - Cài đặt AWS CLI v2 | 06/11/2025 | ✅ Hoàn thành |
| Năm | - Học EC2 cơ bản (instance types, AMI, Security Groups) <br> - Tìm hiểu các phương thức kết nối SSH | 07/11/2025 | ✅ Hoàn thành |
| Sáu | - Khởi chạy EC2 instance (t2.micro, Ubuntu) <br> - Cấu hình Security Group <br> - Kết nối SSH <br> - Gắn EBS volume | 08/11/2025 | ✅ Hoàn thành |

### Kết quả đạt được:
* ✅ Tạo thành công tài khoản AWS với MFA
* ✅ Cài đặt và cấu hình AWS CLI
* ✅ Khởi chạy EC2 instance đầu tiên
* ✅ Kết nối SSH thành công
* ✅ Mount EBS volume vào `/data`

### Bài học chính:
* Các nhóm dịch vụ AWS và use cases
* Tầm quan trọng của cấu hình Security Group
* Quản lý EC2 instance cơ bản
* Các lệnh AWS CLI để quản lý tài nguyên

### Thách thức:
* Vấn đề IAM permission → Sửa bằng cách tạo IAM user phù hợp
* SSH timeout → Thêm inbound rules đúng vào Security Group

### Tuần tới:
* VPC networking
* S3 storage
* IAM policies


