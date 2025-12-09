---
title: "Worklog Tuần 3"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 3:
* Hiểu sâu về EC2 và S3 services
* Học cách import virtual machines vào AWS
* Export virtual machines từ EC2 instance và AMI
* Mount file sharing trên on-premise machine

### Các công việc đã thực hiện:

| Thứ | Công việc | Ngày | Trạng thái |
|-----|-----------|------|------------|
| Hai | - Học EC2 cơ bản (instance types, user data, metadata) <br> - Tìm hiểu EC2 auto scaling (EFA/SR, Lightsail, MGN) | 18/11/2025 | ✅ Hoàn thành |
| Ba | - Tạo S3 bucket <br> - Upload objects <br> - Deploy web bằng S3 <br> - Tăng tốc static web với CloudFront | 19/11/2025 | ✅ Hoàn thành |
| Tư | - Tạo Storage Gateway <br> - Tạo File Shares <br> - Mount File Shares vào on-premise machine <br> - Tạo backup plan <br> - Thiết lập notifications | 20/11/2025 | ✅ Hoàn thành |
| Năm | - Học S3 nâng cao (access point, storage class, static website & CORS, Glacier, Snow Family, Storage Gateway, Backup) | 21/11/2025 | ✅ Hoàn thành |
| Sáu | - Import virtual machine vào AWS <br> - Deploy instance từ AMI <br> - Export VM từ EC2 instance và AMI qua S3 bucket | 22/11/2025 | ✅ Hoàn thành |

### Kết quả đạt được:
* ✅ Thành thạo các instance types và scaling options của EC2
* ✅ Tạo và cấu hình S3 buckets cho static website hosting
* ✅ Deploy CloudFront distribution để tăng tốc content
* ✅ Thiết lập Storage Gateway cho hybrid cloud storage
* ✅ Import/export virtual machines thành công

### Bài học chính:
* Sử dụng EC2 user data và metadata
* Các storage classes của S3 và tối ưu chi phí
* Cấu hình CloudFront CDN
* Các loại Storage Gateway (File, Volume, Tape)
* Quy trình import/export VM qua AWS CLI

### Thách thức:
* Cấu hình CORS cho S3 static website → Sửa policy settings
* Vấn đề kết nối Storage Gateway → Điều chỉnh security groups
* Lỗi format khi import VM → Convert sang định dạng OVA

### Tuần tới:
* Deploy RDS database
* Load balancing với ELB
* Auto Scaling groups


