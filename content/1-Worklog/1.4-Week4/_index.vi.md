---
title: "Worklog Tuần 4"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 4:
* Hiểu cơ bản về bảo mật trên AWS
* Biết cách quản lý tài nguyên bằng tags
* Biết tạo IAM role và policy

### Các công việc đã thực hiện:

| Thứ | Công việc | Ngày | Trạng thái |
|-----|-----------|------|------------|
| Hai | - Tạo CloudFormation stack <br> - Amazon Tag (DSD & ABAC) <br> - Bật shadow copies, user storage quotas và continuous access share <br> - Scale storage và throughput capacity | 25/11/2025 | ✅ Hoàn thành |
| Ba | - Học các dịch vụ security trên AWS (Shared Responsibility Model, IAM, Amazon Cognito, AWS Organizations, KMS) | 26/11/2025 | ✅ Hoàn thành |
| Tư | - Bật Security Hub <br> - Tạo tags cho instances <br> - Tạo role cho Lambda function <br> - Quản lý tài nguyên bằng tags và resource groups | 27/11/2025 | ✅ Hoàn thành |
| Năm | - Tạo IAM policy và role <br> - Tạo Restriction Policy và IAP limited user <br> - Tạo key management service, AWS CloudTrail và Amazon Athena <br> - Share encrypted data trên S3 | 28/11/2025 | ✅ Hoàn thành |
| Sáu | - Tạo IAM Groups, IAM User <br> - Cấu hình role condition <br> - Truy cập ứng dụng qua accesskey và IAM role trên EC2 | 29/11/2025 | ✅ Hoàn thành |

### Kết quả đạt được:
* ✅ Hiểu về AWS security fundamentals (Shared Responsibility Model, IAM, Cognito, Organizations, KMS)
* ✅ Tạo và cấu hình IAM roles và policies
* ✅ Triển khai chiến lược resource tagging để quản lý tốt hơn
* ✅ Thiết lập AWS Security Hub để giám sát bảo mật
* ✅ Cấu hình CloudTrail cho audit logging

### Bài học chính:
* Nguyên tắc AWS Shared Responsibility Model
* Cấu trúc IAM policy và best practices
* Resource tagging cho phân bổ chi phí và tổ chức
* Security Hub findings và compliance checks
* Phân tích CloudTrail logs với Athena

### Thách thức:
* Lỗi cú pháp IAM policy → Dùng AWS Policy Simulator để test
* Áp dụng tags → Triển khai Service Control Policies (SCPs)
* KMS key rotation → Cấu hình automatic key rotation

### Tuần tới:
* Load balancing và Auto Scaling
* CloudWatch monitoring và alarms
* Lambda serverless functions


