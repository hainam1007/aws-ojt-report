---
title: "AI/ML/GenAI on AWS"
date: 2025-07-09
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

# Báo cáo tổng kết: "Workshop AI/ML/GenAI trên AWS"

### Thông tin sự kiện

**Tên sự kiện:** Workshop AI/ML/GenAI trên AWS  
**Ngày:** Thứ Bảy, 15 tháng 11, 2025  
**Thời gian:** 8:30 sáng – 12:00 trưa  
**Địa điểm:** Văn phòng AWS Việt Nam  
**Thời lượng:** 3.5 giờ

---

### Tổng quan Workshop

Workshop thực hành này cung cấp giới thiệu toàn diện về các dịch vụ trí tuệ nhân tạo và machine learning của AWS, với trọng tâm đặc biệt vào Generative AI sử dụng Amazon Bedrock. Buổi học kết hợp lý thuyết với các demo thực tế, giúp người tham gia hiểu cách xây dựng ứng dụng được hỗ trợ bởi AI trên AWS.

---

### Các chủ đề chính được đề cập

#### 1. Dịch vụ AI của AWS

Workshop giới thiệu sáu dịch vụ AI cốt lõi của AWS giải quyết các vấn đề kinh doanh phổ biến:

**Amazon Rekognition** – Thị giác máy tính
- Phân tích hình ảnh và video tự động
- Phát hiện khuôn mặt và so sánh chúng
- Nhận dạng đối tượng, cảnh và hoạt động
- Lọc nội dung không phù hợp

**Amazon Polly** – Chuyển văn bản thành giọng nói
- Chuyển đổi văn bản viết thành giọng nói tự nhiên
- Lựa chọn từ nhiều giọng và ngôn ngữ
- Tạo các ứng dụng có khả năng giọng nói

**Amazon Transcribe** – Chuyển giọng nói thành văn bản
- Chuyển đổi âm thanh thành văn bản tự động
- Hoạt động theo thời gian thực hoặc batch mode
- Hỗ trợ nhiều ngôn ngữ

**Amazon Comprehend** – Xử lý ngôn ngữ tự nhiên
- Phân tích văn bản để hiểu cảm xúc
- Trích xuất thông tin quan trọng (tên, địa điểm, ngày tháng)
- Phát hiện ngôn ngữ được sử dụng

**Amazon Translate** – Dịch ngôn ngữ
- Dịch văn bản giữa các ngôn ngữ bằng AI
- Xử lý theo thời gian thực hoặc batch lớn
- Sử dụng từ vựng tùy chỉnh cho các ngành cụ thể

**Amazon Lex** – AI hội thoại
- Xây dựng chatbot cho dịch vụ khách hàng
- Tạo trợ lý giọng nói
- Kết nối với các dịch vụ AWS khác dễ dàng

#### 2. Generative AI với Amazon Bedrock

**Amazon Bedrock là gì?**
Amazon Bedrock là nền tảng của AWS để xây dựng ứng dụng với foundation models (các mô hình AI lớn) mà không cần quản lý hạ tầng.

**So sánh các Foundation Models**

| Mô hình | Điểm mạnh | Tốt nhất cho |
|---------|-----------|--------------|
| **Claude** | Suy luận mạnh, an toàn | Tác vụ phức tạp, tạo nội dung |
| **Llama** | Mã nguồn mở, có thể tùy chỉnh | Giải pháp tùy chỉnh, tiết kiệm chi phí |
| **Titan** | AWS-native, đáng tin cậy | Tích hợp AWS chung |

**Cơ bản về Prompt Engineering**

Học cách viết prompt hiệu quả để nhận phản hồi AI tốt hơn:

- **Hướng dẫn rõ ràng**: Cụ thể về những gì bạn muốn
- **Chain-of-Thought**: Yêu cầu AI giải thích lý do từng bước
- **Few-shot learning**: Đưa ra ví dụ về đầu ra bạn muốn

Ví dụ:
```
Prompt xấu: "Viết về mèo"
Prompt tốt: "Viết một bài báo 200 từ về hành vi mèo dành cho chủ nuôi thú cưng, tập trung vào lý do tại sao mèo đánh đổ đồ vật"
```

**Retrieval-Augmented Generation (RAG)**

RAG giúp các mô hình AI sử dụng dữ liệu của riêng bạn để tạo ra câu trả lời chính xác hơn:

1. Lưu trữ tài liệu của bạn trong knowledge base
2. Khi người dùng đặt câu hỏi, tìm tài liệu liên quan
3. Gửi cả câu hỏi và tài liệu đến AI
4. Nhận câu trả lời chính xác, phù hợp với ngữ cảnh

**Bedrock Agents**

Tạo các AI agent có thể:
- Chia nhỏ tác vụ phức tạp thành các bước
- Sử dụng công cụ và API để hoàn thành tác vụ
- Đưa ra quyết định dựa trên thông tin

**Guardrails**

Bảo vệ ứng dụng AI của bạn với:
- Lọc nội dung (chặn nội dung có hại)
- Hạn chế chủ đề (giữ trong các chủ đề được phê duyệt)
- Che giấu thông tin nhạy cảm (ẩn dữ liệu cá nhân)

#### 3. Demo Trực tiếp

Điểm nổi bật là xây dựng một **chatbot Generative AI** sử dụng Amazon Bedrock:

- Kết nối với foundation model (Claude)
- Thêm knowledge base với tài liệu công ty
- Triển khai guardrails để đảm bảo an toàn
- Kiểm thử các cuộc hội thoại thực tế

---

### Những gì tôi học được

#### Hiểu về dịch vụ AI của AWS

Trước workshop, tôi không chắc nên sử dụng dịch vụ AWS nào cho các tác vụ AI khác nhau. Bây giờ tôi biết:
- Sử dụng **Rekognition** để phân tích hình ảnh/video
- Sử dụng **Polly** để thêm giọng nói vào ứng dụng
- Sử dụng **Comprehend** để hiểu phản hồi khách hàng
- Sử dụng **Bedrock** cho ứng dụng AI tùy chỉnh

#### Prompt Engineering thực tế

Học prompt engineering là một trải nghiệm mở mang. Những thay đổi nhỏ trong cách bạn đặt câu hỏi có thể cải thiện đáng kể phản hồi AI. Kỹ thuật Chain-of-Thought đặc biệt hữu ích cho các vấn đề phức tạp.

#### Lợi ích của kiến trúc RAG

Hiểu về RAG cho tôi thấy cách tạo ứng dụng AI có thể:
- Sử dụng thông tin đặc thù của công ty
- Luôn cập nhật mà không cần đào tạo lại
- Đưa ra câu trả lời chính xác và phù hợp hơn

#### Xây dựng ứng dụng AI an toàn

Phần về guardrails dạy tôi tầm quan trọng của:
- Ngăn chặn tạo nội dung có hại
- Bảo vệ quyền riêng tư người dùng
- Giữ phản hồi AI đúng chủ đề

---

### Kỹ năng đạt được

Sau workshop này, giờ tôi có thể:

✅ Chọn dịch vụ AI AWS phù hợp cho các use case khác nhau  
✅ So sánh các foundation model và lựa chọn mô hình phù hợp  
✅ Viết prompt hiệu quả cho phản hồi AI tốt hơn  
✅ Hiểu kiến trúc RAG và khi nào sử dụng nó  
✅ Xây dựng chatbot Generative AI cơ bản với Bedrock  
✅ Triển khai các biện pháp an toàn sử dụng Guardrails  

---

### Cách tôi sẽ áp dụng điều này

#### Ứng dụng ngắn hạn
- Thử nghiệm với các foundation model khác nhau trên Bedrock
- Luyện tập các kỹ thuật prompt engineering
- Xây dựng prototype chatbot đơn giản để kiểm thử

#### Mục tiêu dài hạn
- Đề xuất tính năng được hỗ trợ AI cho dự án hiện tại
- Triển khai RAG cho hệ thống tìm kiếm knowledge base
- Tích hợp các dịch vụ AI AWS vào ứng dụng hiện có

---

### Trải nghiệm sự kiện

Workshop được tổ chức tốt và thân thiện với người mới bắt đầu. Các diễn giả giải thích các khái niệm phức tạp một cách rõ ràng và demo thực hành làm cho mọi thứ trở nên thực tế. Có 3.5 giờ là hoàn hảo—đủ thời gian để đề cập các chủ đề quan trọng mà không cảm thấy vội vã.

Văn phòng AWS Việt Nam cung cấp một môi trường học tập tuyệt vời với cơ sở vật chất tốt và cơ hội kết nối với các người tham gia khác quan tâm đến AI/ML.

#### Điều tôi thích
- Cách tiếp cận thực hành với demo trực tiếp
- So sánh rõ ràng các dịch vụ AI khác nhau
- Ví dụ thực tế từ các dự án thực
- Truy cập tài liệu workshop để tham khảo sau này

#### Hình ảnh sự kiện
*Thêm hình ảnh sự kiện của bạn tại đây*

---

### Tài nguyên được cung cấp

- Links tài liệu dịch vụ AI AWS
- Hướng dẫn bắt đầu với Bedrock
- Cheat sheet prompt engineering
- Ví dụ triển khai RAG
- Code mẫu từ demo chatbot

---

### Kết luận

Workshop này đã cho tôi nền tảng vững chắc về các dịch vụ AI/ML AWS và Generative AI. Sự kết hợp của tổng quan dịch vụ, prompt engineering, kiến trúc RAG và demo thực hành cung cấp cả chiều rộng và chiều sâu kiến thức.

Tôi rất hào hứng khám phá các công cụ này sâu hơn và tìm cách tích hợp khả năng AI vào các dự án của mình. Workshop đã chứng minh rằng xây dựng ứng dụng AI trên AWS dễ tiếp cận hơn tôi nghĩ.

**Đánh giá: ⭐⭐⭐⭐⭐ (5/5)**

---

*Để biết thêm thông tin về dịch vụ AI AWS, truy cập: [Dịch vụ AI AWS](https://aws.amazon.com/ai/)*
