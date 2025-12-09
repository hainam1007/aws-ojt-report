---
title: "Blog 1"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Nội dung bên dưới là phần tóm tắt và diễn giải lại blog AWS  
**“Build agentic systems with CrewAI and Amazon Bedrock”**.  
Chỉ dùng để tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn, kể cả cảnh báo này.
{{% /notice %}}

# Xây dựng hệ thống Agentic với CrewAI và Amazon Bedrock

*Dựa trên bài viết của Tony Kipkemboi, João (Joe) Moura, Karan Singh và Aris Tsakpinis.*

---

## 1. Giới thiệu

Các ứng dụng AI trong doanh nghiệp đang chuyển dịch từ mô hình gọi LLM đơn lẻ sang **hệ thống agentic** – nơi nhiều tác nhân (agent) phối hợp với nhau để hoàn thành các công việc phức tạp.

Các nghiên cứu thị trường cho thấy:

- Năm 2025, khoảng **25%** doanh nghiệp dùng GenAI sẽ triển khai AI agents;  
- Đến 2027 con số này có thể lên **50%** và thị trường AI agent tăng trưởng rất nhanh.

Bài blog giải thích cách kết hợp **framework mã nguồn mở CrewAI** với **Amazon Bedrock** để xây dựng các hệ thống multi‑agent sẵn sàng cho môi trường production.

---

## 2. Agentic system là gì?

**AI agent** là một thành phần tự động, sử dụng LLM và các khả năng AI khác để:

- Tự lập kế hoạch nhiều bước  
- Thích nghi với bối cảnh thay đổi  
- Gọi **các công cụ / API** bên ngoài  
- Tương tác với các agent khác để hoàn thành nhiệm vụ

So với các ứng dụng doanh nghiệp truyền thống (SaaS, workflow engine):

- Agentic system linh hoạt hơn, hiểu ngữ cảnh tốt hơn  
- Kết hợp được cả **tri thức miền (domain knowledge)** và **khả năng suy luận** của LLM  
- Phù hợp cho các quy trình động, nhiều ngoại lệ, khó viết rule cố định

Ví dụ:

- **Phát triển phần mềm:** nhiều agent cùng nhau phân tích yêu cầu, tạo code, review, kiểm tra bảo mật.  
- **Chuỗi cung ứng:** agent theo dõi thời tiết, rủi ro địa chính trị, tồn kho để tự đề xuất phương án vận chuyển.

---

## 3. CrewAI – framework multi‑agent

**CrewAI** là một framework Python (kèm bộ sản phẩm enterprise) cho phép:

- Định nghĩa **agents**, **tasks**, **tools** và **crews** (nhóm agent)  
- Cho phép các agent **cộng tác**, đặt câu hỏi, giao việc cho nhau  
- Kết hợp giữa mã Python thông thường, gọi LLM và các workflow phức tạp

Trong nhiều doanh nghiệp, CrewAI được dùng để:

- Tự động hóa các tác vụ lặp lại (chuẩn bị báo cáo, tổng hợp log, hỗ trợ khách hàng)  
- Xây dựng các vai trò mới dựa trên AI agents (AI researcher, AI analyst, v.v.)

---

## 4. Các khái niệm chính trong CrewAI

### 4.1 Flows

**Flow** là một luồng xử lý gồm nhiều bước:

- Có thể chứa: code Python, các lời gọi LLM đơn lẻ hoặc nhiều crew khác nhau  
- Hỗ trợ điều kiện rẽ nhánh, vòng lặp, lưu trạng thái  
- Phù hợp cho các quy trình phức tạp, nhiều bước phụ thuộc lẫn nhau

Khi dùng **Amazon Bedrock** làm backend cho LLM:

- Flow có thể route ticket hỗ trợ khách hàng đến đúng nhóm agent  
- Hoặc điều phối một chuỗi phân tích tài chính, phản ứng theo dữ liệu thị trường thời gian thực.

### 4.2 Crews, Agents, Tasks, Tools

- **Crew**: tập các agent hợp tác để đạt một mục tiêu chung.  
- **Agent**:
  - Có *role* (vai trò), *goal* (mục tiêu), *backstory* (bối cảnh)  
  - Có tập **tools** được phép sử dụng (HTTP API, DB, script, v.v.)  
  - Có thể giao việc, hỏi đáp lẫn nhau  
- **Task**:
  - Mô tả bằng ngôn ngữ tự nhiên “cần làm gì”  
  - Chỉ định agent chịu trách nhiệm thực hiện  
- **Tool**:
  - Giúp agent tương tác với thế giới bên ngoài (gọi REST API, truy vấn CSDL, đọc file…)  
  - Được thiết kế dạng module, gắn cho từng agent khi cần

---

## 5. Tích hợp CrewAI với Amazon Bedrock

Trong code Python, ta cấu hình LLM của CrewAI trỏ đến **Amazon Bedrock**:

```python
from crewai import Agent, LLM

llm = LLM(
    model="bedrock/anthropic.claude-3-5-sonnet-20241022-v2:0",
    aws_access_key_id=os.getenv('AWS_ACCESS_KEY_ID'),
    aws_secret_access_key=os.getenv('AWS_SECRET_ACCESS_KEY'),
    aws_region_name=os.getenv('AWS_REGION_NAME')
)

security_analyst = Agent(
    role="Security Analyst",
    goal="Phân tích rủi ro bảo mật trên hạ tầng AWS",
    backstory="Chuyên gia bảo mật cloud",
    llm=llm
)
```

Lợi ích của việc dùng Bedrock:

- Truy cập các foundation model mạnh (Anthropic Claude, Amazon Titan/Nova, v.v.)  
- Bảo mật, tuân thủ và quản trị tập trung trên AWS  
- Dễ tích hợp với các dịch vụ AWS khác trong cùng tài khoản.

---

## 6. Agents & Knowledge Bases của Amazon Bedrock

Bên cạnh việc dùng Bedrock chỉ như “LLM backend”, CrewAI còn có thể:

### 6.1 Gọi **Bedrock Agents**

- **Bedrock Agents** là các agent fully‑managed, serverless trên AWS.  
- CrewAI có tool `BedrockInvokeAgentTool` để một agent CrewAI gọi Bedrock Agent trong workflow.

```python
from crewai_tools.aws.bedrock.agents import BedrockInvokeAgentTool

agent_tool = BedrockInvokeAgentTool(
    agent_id="your-agent-id",
    agent_alias_id="your-agent-alias-id"
)
```

### 6.2 Truy vấn **Bedrock Knowledge Bases**

- Knowledge Base giúp kết nối model/agent với dữ liệu doanh nghiệp (tài liệu, file trên S3…).  
- Tool `BedrockKBRetrieverTool` cho phép agent truy vấn dữ liệu này bằng ngôn ngữ tự nhiên.

```python
kb_tool = BedrockKBRetrieverTool(
    knowledge_base_id="your-kb-id",
    number_of_results=5
)
```

Nhờ đó, agents có thể trả lời dựa trên **nguồn dữ liệu tin cậy**, giảm hiện tượng “bịa” (hallucination).

---

## 7. Ví dụ use case: Cloud Security Posture Management

Bài blog minh họa một giải pháp **đánh giá bảo mật hạ tầng AWS** bằng đội ngũ 3 agent:

1. **Infrastructure mapper** – quét tài nguyên AWS, xây bản đồ hạ tầng.  
2. **Security analyst** – phân tích rủi ro, so sánh với best practice.  
3. **Report writer** – tổng hợp thành báo cáo ưu tiên khắc phục.

Các bước chính:

- Dùng một **tool quét hạ tầng** (AWS SDK) để lấy thông tin EC2, S3, IAM, RDS, VPC…  
- Đưa dữ liệu quét cho security analyst để phân tích lỗ hổng và mức độ ưu tiên.  
- Agent report writer sinh ra báo cáo với:
  - Tóm tắt điều hành  
  - Ma trận rủi ro  
  - Danh sách bước khuyến nghị chi tiết

Toàn bộ quy trình vận hành nhờ CrewAI (điều phối agents và tasks) và Bedrock (mô hình nền).

---

## 8. Quan trắc và vận hành (Observability)

Vì agentic system kết hợp cả logic quyết định và suy luận xác suất của LLM, nên **theo dõi hoạt động** là cực kỳ quan trọng:

- **Cấp ứng dụng:** kiểm tra workflow tổng thể có chạy đúng không, lỗi ở bước nào.  
- **Cấp model:** độ chính xác, latency, throughput… của model Bedrock.  
- **Cấp agent:** hành vi của từng agent, nội dung message trao đổi.

Trên AWS có thể dùng:

- **Amazon CloudWatch** để log và metric  
- Logging sẵn có của CrewAI (`verbose=True` để xem chi tiết)  
- Các nền tảng quan trắc LLM khác (AgentOps, Arize, LangFuse, …) nếu cần.

---

## 9. Kết luận

Từ bài blog có thể rút ra:

- Hệ thống **agentic** là bước tiến tiếp theo của ứng dụng GenAI trong doanh nghiệp,  
  cho phép xử lý các quy trình phức tạp, nhiều bước và phụ thuộc lẫn nhau.  
- **CrewAI** mang lại framework multi‑agent linh hoạt;  
  **Amazon Bedrock** cung cấp hạ tầng model, Agents, Knowledge Bases và bảo mật cấp enterprise.  
- Khi thiết kế, cần đặc biệt chú ý:
  - Phân tách agent theo vai trò rõ ràng  
  - Lựa chọn tool phù hợp cho từng agent  
  - Thêm guardrails, logging và monitoring để hệ thống an toàn, dễ debug.

Nhờ sự kết hợp này, tổ chức có thể đi từ các demo LLM đơn giản đến những **hệ thống multi‑agent production‑ready trên AWS**, phục vụ nhiều bài toán như bảo mật, tự động hóa quy trình, hỗ trợ ra quyết định, v.v.
