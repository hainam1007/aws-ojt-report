---
title: "Blog 3"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Nội dung bên dưới là phần tóm tắt và diễn giải lại blog AWS  
**“Reserve your seat: Microsoft workloads on AWS sessions at re:Invent 2024”**.  
Chỉ dùng để tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn, kể cả cảnh báo này.
{{% /notice %}}

# Đặt chỗ cho các phiên Microsoft workloads on AWS tại re:Invent 2024

*Dựa trên bài viết của David Pallmann (04/11/2024).*

---

## 1. re:Invent 2024 và nội dung dành cho Microsoft workloads

AWS re:Invent 2024 có hơn **2.400 phiên** trải rộng trên sáu địa điểm ở Las Vegas.  
Người tham dự đã đăng ký có thể vào **Attendee Portal** để đặt chỗ trước – rất quan trọng vì các phiên “hot” thường kín chỗ rất nhanh.

Bài blog gốc giúp bạn:

- Tìm nhanh các phiên liên quan đến **Windows Server, SQL Server, Active Directory, .NET**  
- Lên lịch để học cách **di chuyển, tối ưu và hiện đại hóa** khối lượng công việc Microsoft trên AWS.

---

## 2. Nhóm breakout session (phiên thuyết trình)

Breakout session là các phiên 45–60 phút, thường có phần Q&A cuối giờ.

Một số chủ đề tiêu biểu:

- **Hiện đại hóa .NET monolith**  
  Câu chuyện của Tessitura – nhà cung cấp phần mềm cho nghệ thuật & văn hóa – khi chuyển hệ thống .NET 20 năm tuổi sang kiến trúc cloud hiện đại, sử dụng phương pháp **Experience‑Based Acceleration (EBA)** để vừa thay đổi kỹ thuật vừa thay đổi văn hóa tổ chức.

- **Tối ưu chi phí và vận hành SQL Server trên AWS**  
  Thomson Reuters chia sẻ cách thiết kế lại nền tảng giao dịch dựa trên SQL Server để giảm ~40% chi phí vận hành và tăng hiệu quả vận hành gấp 5 lần, nhưng vẫn giữ được sự linh hoạt của việc quản lý hệ điều hành.

- **Bản quyền phần mềm thương mại trên AWS**  
  Giải thích các con đường license cho phần mềm Microsoft và các nền tảng thương mại khác, vai trò của **AWS Optimization and Licensing Assessment (OLA)**, cách xử lý end‑of‑support, cũng như lựa chọn thay thế bằng dịch vụ cloud‑native hoặc mã nguồn mở.

- **Khai thác dữ liệu Microsoft cho Amazon Q Business**  
  Trình bày cách dùng **SharePoint** và file server Windows (qua **Amazon FSx**) làm nguồn dữ liệu cho **Amazon Q Business**, bao gồm indexing, áp dụng guardrail dựa trên danh tính Active Directory và ví dụ ứng dụng generative AI an toàn.

- **Giảm chi phí SQL Server với tính năng Optimize CPU trên EC2**  
  Hướng dẫn áp dụng cấu hình vCPU linh hoạt cho workload SQL Server thiên về bộ nhớ/IO, kèm theo kết quả benchmark để cân bằng giữa hiệu năng và chi phí.

- **Chạy .NET trên Amazon EKS mà không cần sửa nhiều code**  
  Kinh nghiệm của Moody’s khi chuyển hàng chục ứng dụng .NET từ EC2 for Windows sang **Amazon EKS with Windows support**, những mẫu kiến trúc, thách thức và lợi ích đạt được.

- **Sử dụng generative AI để vận hành hạ tầng Microsoft**  
  Ví dụ dùng **Amazon Q** và **Amazon Bedrock** để phân tích log, phát hiện cấu hình sai và tự động hóa thao tác vận hành cho Windows workloads.

- **Hành trình đa vùng (multi‑Region) cho .NET workloads**  
  Verisk Analytics kể lại 8 năm hiện đại hóa .NET từ data center lên kiến trúc đa vùng sẵn sàng thảm họa, kèm các bài học về chi phí, warm pool và license Microsoft.

Ngoài ra còn có các phiên dành cho:

- Ngân hàng triển khai stack Microsoft trên AWS  
- Case study spin‑off Allspring Global Investments  
- Câu chuyện Bonterra di chuyển từ Azure sang AWS  
- Mindbody migrate hơn **60.000** database SQL Server sang AWS.

---

## 3. Builders’ session (lab quy mô nhỏ)

Builders’ session là các lab hands‑on, mỗi bàn ~10 người, tập trung vào việc **tự tay xây dựng**.

Hai phiên nổi bật:

- **Xây ứng dụng AI với .NET và Amazon Bedrock**  
  Thực hành triển khai **Retrieval Augmented Generation (RAG)** dùng .NET và **Amazon Bedrock Knowledge Bases**, để ứng dụng có thể trả lời dựa trên dữ liệu riêng của doanh nghiệp.

- **Tăng năng suất lập trình .NET với Amazon Q Developer**  
  Học cách dùng Amazon Q Developer trong IDE để sinh code mẫu, refactor, hiểu code lạ, phát hiện bug và cải thiện bảo mật.

---

## 4. Chalk talk (thảo luận bảng trắng)

Chalk talk bắt đầu bằng phần giới thiệu ngắn, sau đó là **hỏi đáp tương tác**.

Ví dụ:

- **Kiến thức AWS cho “DBA SQL Server bất đắc dĩ”**  
  Giúp DBA làm quen với các khái niệm kiến trúc cloud, HA/DR, mạng, bảo mật trên AWS và cách dùng Amazon Q để hỗ trợ vận hành.

- **Lộ trình migrate SQL Server trên AWS**  
  So sánh các chiến lược và công cụ: AWS Migration Hub, Application Migration Service, AWS DMS, replication / Always On, cùng với kinh nghiệm thực tế.

---

## 5. Code talk (demo nhiều code)

Code talk là các phiên demo code trực tiếp cho nhóm nhỏ.

Một số chủ đề:

- Chọn dịch vụ AI / GenAI phù hợp cho từng use case .NET, ví dụ xử lý tài liệu thông minh.  
- Tự động hóa và xử lý sự cố Active Directory bằng Amazon Bedrock Agents.  
- Dùng Amazon Q Developer để viết, test, debug và nâng cấp ứng dụng .NET.  
- Xây search engine hình ảnh với .NET, Amazon Bedrock và Amazon OpenSearch Service.

---

## 6. Workshop (lab nhóm 2 giờ)

Workshops là nơi người tham dự làm việc nhóm để **xây trọn vẹn một giải pháp** với sự hướng dẫn của chuyên gia AWS.

Các ví dụ:

- Dùng Amazon Bedrock để sinh **Infrastructure as Code** trực tiếp từ sơ đồ kiến trúc.  
- Phân tích và chọn chiến lược hiện đại hóa cho nhiều ứng dụng Windows (container hóa, refactor sang Linux, v.v.).  
- Sử dụng **Amazon Q Code Transformation for .NET** để port .NET Framework từ Windows sang .NET cross‑platform trên Linux.  
- Áp dụng **AWS Well‑Architected Framework – security pillar** cho AWS Managed Microsoft AD.  
- Migrating ứng dụng .NET từ SQL Server sang **Amazon RDS for PostgreSQL** với AWS DMS.

---

## 7. Tham gia re:Invent và gặp gỡ chuyên gia Microsoft workloads on AWS

Bài blog kết luận bằng lời mời:

- Đăng ký re:Invent (nếu chưa), vào **Attendee Portal** để **giữ chỗ** cho các phiên quan trọng.  
- Ghé **khu Windows, SQL Server và .NET** trong AWS Village để:
  - Gặp gỡ đội ngũ xây dựng dịch vụ AWS cho Microsoft workloads  
  - Xem demo, bao gồm các tình huống dùng generative AI  
  - Trao đổi sâu hơn về kiến trúc và best practice khi chạy Microsoft trên AWS

Thông điệp chính: AWS có hệ sinh thái dịch vụ phong phú cho nền tảng Microsoft, và re:Invent là nơi tốt nhất để học cách khai thác tối đa các lựa chọn này.

---

## 8. Tác giả

**David Pallmann** là Senior Product Manager trong đội **AWS Transform**, tập trung vào trải nghiệm developer .NET trên AWS.  
Anh có nhiều kinh nghiệm ở các vai trò kỹ sư, tư vấn, quản lý sản phẩm và lãnh đạo kỹ thuật; từng tham gia phát triển **Windows Communication Foundation (WCF)** và sau đó tạo ra **Neuron ESB**, một nền tảng enterprise service bus dựa trên .NET.  
Bạn có thể theo dõi anh trên X tại `@davidpallmann`.
