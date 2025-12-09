---
title: "Worklog Tuần 6"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 6:
* Hiểu về database concepts trên AWS
* Biết cách tạo DB và kết nối DB với EC2
* Hoàn thành assignment hackathon

### Các công việc đã thực hiện:

| Thứ | Công việc | Ngày | Trạng thái |
|-----|-----------|------|------------|
| Hai | - Học về databases trên AWS (RDS, Aurora, Redshift, ElastiCache) <br> - Làm lab 05 | 09/12/2025 | ✅ Hoàn thành |
| Ba | - **Thực hành:** Tạo EC2 và RDS <br> - Deploy ứng dụng trên EC2 và kết nối RDS <br> - Học backup và restore | 10/12/2025 | ✅ Hoàn thành |
| Tư | - Học về distributed systems (network, TCP, HTTP, WebSocket) <br> - Ôn tập system architecture patterns | 11/12/2025 | ✅ Hoàn thành |
| Năm | - **Thực hành:** Tạo game tic-tac-toe chẵn/lẻ multiplayer <br> - Triển khai real-time communication | 12/12/2025 | ✅ Hoàn thành |
| Sáu | - **Thực hành:** Tiếp tục fix bugs và hoàn thiện game <br> - Deploy và test phiên bản cuối | 13/12/2025 | ✅ Hoàn thành |

### Kết quả đạt được:
* ✅ Hiểu các khái niệm database cơ bản (RDBMS, NoSQL, OLTP, OLAP)
* ✅ Học các dịch vụ database của AWS (RDS, Aurora, Redshift, ElastiCache)
* ✅ Tạo và cấu hình Amazon RDS instance thành công
* ✅ Kết nối EC2 với RDS và deploy ứng dụng
* ✅ Tạo game tic-tac-toe chẵn/lẻ multiplayer với tính năng real-time

### Bài học chính:
* Setup và cấu hình AWS RDS
* Database security groups và connectivity
* Cơ chế backup và restore của RDS
* Cơ bản về distributed systems (TCP, HTTP, WebSocket)
* Kiến trúc multiplayer game real-time

### Thách thức:
* Cấu hình RDS security group → Sửa inbound rules cho EC2 access
* WebSocket connection stability → Triển khai reconnection logic
* Đồng bộ game state → Dùng state management patterns phù hợp

### Tuần tới:
* Container services (ECS, EKS)
* Docker cơ bản
* Kiến trúc Microservices


