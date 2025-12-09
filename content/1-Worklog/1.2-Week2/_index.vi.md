---
title: "Worklog Tuần 2"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 2:
* Tìm hiểu sâu về VPC networking
* Học S3 storage và best practices
* Hiểu về IAM policies và roles

### Các công việc đã thực hiện:

| Thứ | Công việc | Ngày | Trạng thái |
|-----|-----------|------|------------|
| Hai | - Học VPC cơ bản (subnets, route tables, internet gateway) <br> - Tìm hiểu public vs private subnets <br> - Security Groups vs NACLs | 11/11/2025 | ✅ Hoàn thành |
| Ba | - Tạo custom VPC với public/private subnets <br> - Cấu hình route tables <br> - Setup NAT Gateway <br> - Test EC2 trong private subnet | 11/12/2025 | ✅ Hoàn thành |
| Tư | - Học S3 cơ bản (buckets, objects, storage classes) <br> - Tìm hiểu S3 security (bucket policies, ACLs) <br> - S3 versioning và lifecycle policies | 11/13/2025 | ✅ Hoàn thành |
| Năm | - Tạo S3 buckets <br> - Upload/download files qua Console & CLI <br> - Cấu hình bucket policies <br> - Bật versioning và encryption | 11/14/2025 | ✅ Hoàn thành |
| Sáu | - Học IAM cơ bản (users, groups, roles, policies) <br> - Tìm hiểu nguyên tắc least privilege <br> - Tạo IAM policies cho EC2 và S3 | 11/15/2025 | ✅ Hoàn thành |

### Kết quả đạt được:
* ✅ Tạo custom VPC với phân đoạn mạng hợp lý
* ✅ Deploy EC2 instances trong public và private subnets
* ✅ Cấu hình NAT Gateway cho private subnet truy cập internet
* ✅ Tạo và quản lý S3 buckets với bảo mật phù hợp
* ✅ Triển khai IAM policies theo nguyên tắc least privilege

### Bài học chính:
* Kiến trúc VPC và thiết kế subnet best practices
* Khác biệt giữa Security Groups (stateful) và NACLs (stateless)
* Các storage classes của S3 và chiến lược tối ưu chi phí
* Cấu trúc IAM policy và permission boundaries

### Thách thức:
* Vấn đề routing NAT Gateway → Sửa route table associations
* Lỗi cú pháp S3 bucket policy → Dùng AWS Policy Generator
* Lỗi IAM permission denied → Review CloudTrail logs

### Tuần tới:
* RDS và database management
* CloudFormation cơ bản
* Monitoring với CloudWatch


