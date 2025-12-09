---
title: "Worklog Tuần 13"
date: 2025-07-09
weight: 5
chapter: false
pre: " <b> 1.13. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 13:
* Hoàn thành workshop

### Các công việc đã thực hiện:

| Thứ | Công việc | Ngày | Trạng thái |
|-----|-----------|------|------------|
| Hai | - Làm lại login lambda và thiết kế web cho login với hai loại tài khoản (Admin, manager) <br> - Tạo CRUD cho admin account | 01/12/2025 | ✅ Hoàn thành |
| Ba | - Fix bug login cho manager <br> - Fix 2 function ListRoom và UpdateRoom <br> - Tạo chart cho data <br> - Tạo mới create room với IoT core | 02/12/2025 | ✅ Hoàn thành |
| Tư | - Triển khai virtual IoT device trên laptop local để nhận và gửi data tới AWS | 03/12/2025 | ✅ Hoàn thành |
| Năm | - Fix một số bug trong UI và script python để mô phỏng IoT device | 04/12/2025 | ✅ Hoàn thành |
| Sáu | - Test và tối ưu web | 05/12/2025 | ✅ Hoàn thành |

### Kết quả đạt được:
* ✅ Triển khai Python script để mô phỏng local IoT device, thiết lập thành công giao tiếp MQTT hai chiều (Telemetry & Control) với AWS IoT Core
* ✅ Hoàn thành workshop

### Bài học chính:
* Triển khai multi-role authentication
* Tích hợp AWS IoT Core
* MQTT protocol cho device communication
* Mô phỏng IoT device bằng Python
* Trực quan hóa data với charts

### Thách thức:
* Role-based access control → Triển khai authentication logic phù hợp
* IoT Core bidirectional communication → Cấu hình MQTT topics đúng
* Debug Python script → Sửa vấn đề connection và data format

### Tổng kết:
Tuần cuối tập trung hoàn thành workshop với tích hợp IoT. Triển khai thành công virtual IoT device simulation và nâng cao admin features.