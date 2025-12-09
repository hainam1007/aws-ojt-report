---
title: "Worklog Tuần 10"
date: 2025-07-09
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 10:
* Chuyển dự án sang gitlab
* Cấu hình CI/CD cho dự án
* Khám phá cách dịch liên tục các từ với model AI

### Các công việc đã thực hiện:

| Thứ | Công việc | Ngày | Trạng thái |
|-----|-----------|------|------------|
| Hai | - Tìm cách để model có thể dịch video dài với nhiều cử chỉ | 10/01/2025 | ✅ Hoàn thành |
| Ba | - Chuyển dự án từ Github sang Gitlab <br> - Học cách sử dụng Gitlab <br> - Cấu hình CI/CD | 11/01/2025 | ✅ Hoàn thành |
| Tư | - Triển khai sliding window trong be logic để dịch liên tục các từ | 12/01/2025 | ✅ Hoàn thành |
| Năm | - Fix bugs và test web | 13/01/2025 | ✅ Hoàn thành |
| Sáu | - Triển khai paused-based segmentation trong be | 14/01/2025 | ✅ Hoàn thành |

### Kết quả đạt được:
* ✅ Cấu hình thành công CI/CD cho gitlab tới S3 và Cloudfront
* ✅ Triển khai hai cách dịch continuous words vào web
* ✅ Test độ chính xác của hai cách

### Bài học chính:
* Cấu hình Gitlab CI/CD pipeline
* Automated deployment tới S3 và CloudFront
* Tối ưu AI model cho continuous translation
* Triển khai sliding window algorithm
* Kỹ thuật paused-based segmentation

### Thách thức:
* Setup Gitlab CI/CD pipeline → Cấu hình stages và deployment scripts phù hợp
* Độ chính xác continuous translation → Triển khai sliding window approach
* Hiệu năng model → Tối ưu với paused-based segmentation

### Tuần tới:
* Presentation Hackathon cuối cùng
* Tài liệu hóa dự án
* Tối ưu hiệu năng


