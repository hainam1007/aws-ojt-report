---
title: "Worklog Tuần 9"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 9:
* Xây dựng demo web
* Kết nối S3 và CloudFront cho workshop
* Khám phá AI model cho dự án Hackathon

### Các công việc đã thực hiện:

| Thứ | Công việc | Ngày | Trạng thái |
|-----|-----------|------|------------|
| Hai | - Tạo app cơ bản, deploy fe trên S3 và CloudFront | 03/01/2025 | ✅ Hoàn thành |
| Ba | - Tạo API gateway và lambda function cho login logout <br> - Fix bugs về CORS | 04/01/2025 | ✅ Hoàn thành |
| Tư | - Khám phá về model AI <br> - Học cách chạy model này | 05/01/2025 | ✅ Hoàn thành |
| Năm | - Tạo web đơn giản với camera cho dự án <br> - Khám phá về model VSL mới | 06/01/2025 | ✅ Hoàn thành |
| Sáu | - Triển khai model AI VSL vào dự án | 07/01/2025 | ✅ Hoàn thành |

### Kết quả đạt được:
* ✅ Xây dựng thành công web đơn giản cho workshop và hackathon
* ✅ Kết nối thành công S3 và CloudFront để deploy fe
* ✅ Triển khai thành công model AI VSL vào web

### Bài học chính:
* Cấu hình S3 static website hosting
* Thiết lập CloudFront distribution và caching
* Tích hợp API Gateway và Lambda
* Xử lý CORS trong serverless architecture
* Tích hợp AI model (VSL - Vietnamese Sign Language)

### Thách thức:
* Cấu hình CORS → Sửa response headers của API Gateway và Lambda
* Vấn đề caching CloudFront → Thiết lập cache invalidation phù hợp
* Tích hợp AI model → Tối ưu model loading và inference

### Tuần tới:
* Hoàn thiện dự án Hackathon
* Tối ưu hiệu năng ứng dụng
* Testing và deployment cuối cùng


