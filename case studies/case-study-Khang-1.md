# Case Study 01 - Agent Forge cho bộ phận Chăm sóc khách hàng

> **Hướng:** Agent tạo Agent  
> **Tên hệ thống đề xuất:** Customer Service Agent Forge (CS-AgentForge)  
> **Ý tưởng cốt lõi:** Từ website, tài liệu nội bộ và mẫu ticket của một doanh nghiệp, hệ thống tự phân tích quy trình chăm sóc khách hàng, tạo ra một AI Agent MVP chuyên biệt, kiểm thử agent và chỉ bàn giao khi đạt ngưỡng chất lượng.

## 1. Industry / Domain & Current Trend

### Lĩnh vực

Case study thuộc lĩnh vực chăm sóc khách hàng (Customer Service/Customer Support), tương ứng với nhóm quy trình **6.0 - Manage Customer Service** trong APQC Process Classification Framework (PCF).

### Xu hướng ứng dụng AI

- Doanh nghiệp chuyển từ chatbot theo kịch bản cố định sang trợ lý hội thoại có thể tra cứu tri thức, sử dụng công cụ và thực hiện nhiều bước.
- AI được dùng để phân loại ticket, tìm câu trả lời, tóm tắt hội thoại, đề xuất hành động và chuyển tiếp đúng bộ phận.
- Mỗi doanh nghiệp cần một agent khác nhau vì sản phẩm, chính sách, kênh hỗ trợ, quy trình xử lý và quyền truy cập khác nhau.
- Nhu cầu triển khai nhanh nhưng vẫn bảo đảm câu trả lời có căn cứ, đúng chính sách và không thực hiện hành động vượt quyền ngày càng quan trọng.

### Tiềm năng

Chăm sóc khách hàng có quy trình lặp lại, nhiều tài liệu nghiệp vụ và kết quả tương đối dễ đo bằng tỷ lệ xử lý thành công, thời gian phản hồi, tỷ lệ chuyển cấp và mức độ tuân thủ. Vì vậy đây là miền phù hợp để kiểm chứng ý tưởng "Agent tạo Agent" trong phạm vi đồ án tốt nghiệp.

## 2. Business Process / User Workflow

### Đối tượng tham gia

- Nhân viên triển khai AI hoặc quản trị hệ thống.
- Trưởng bộ phận chăm sóc khách hàng.
- Nhân viên hỗ trợ khách hàng.
- Khách hàng cuối.
- Các hệ thống liên quan: knowledge base, CRM, ticketing, quản lý đơn hàng.

### Quy trình hiện tại

1. Đội triển khai phỏng vấn doanh nghiệp để hiểu sản phẩm, chính sách và quy trình hỗ trợ.
2. Doanh nghiệp cung cấp FAQ, SOP, chính sách bảo hành/đổi trả và ticket mẫu.
3. Chuyên gia phân nhóm ý định người dùng và xác định tình huống agent được phép xử lý.
4. Kỹ sư viết system prompt, xây knowledge base và tích hợp API.
5. Nhóm dự án tự viết bộ câu hỏi kiểm thử và sửa prompt qua nhiều vòng.
6. Doanh nghiệp nghiệm thu, sau đó đưa agent vào một kênh thử nghiệm.

### Quy trình đề xuất

1. Người triển khai khai báo website doanh nghiệp và tải lên tài liệu được phép sử dụng.
2. Agent-Building-Agent thu thập, chuẩn hóa và phân loại tri thức theo sản phẩm, chính sách và quy trình.
3. Hệ thống ánh xạ nghiệp vụ vào APQC PCF 6.0 và suy luận các SOP chăm sóc khách hàng.
4. Hệ thống đề xuất phạm vi agent, tool cần dùng, quyền truy cập và tiêu chí thành công.
5. Sau khi người quản trị phê duyệt đặc tả, hệ thống sinh Customer Service Agent MVP.
6. Evaluation Agent tự sinh test suite, chạy kiểm thử và lập báo cáo lỗi.
7. Agent MVP chỉ được xuất bản sang môi trường thử nghiệm nếu vượt qua các quality gate.

## 3. Business Problem & Bottleneck

### Vấn đề hiện tại

- Việc khảo sát và chuyển tài liệu doanh nghiệp thành đặc tả agent chủ yếu làm thủ công.
- Tri thức nằm rải rác trong website, file chính sách, SOP và hệ thống ticket.
- Prompt và luồng xử lý khó tái sử dụng nguyên trạng giữa các doanh nghiệp.
- Bộ kiểm thử thường được xây sau khi agent đã hoàn thành nên dễ thiếu các tình huống biên.
- Một agent trả lời tự nhiên nhưng có thể sai chính sách, thiếu căn cứ hoặc gọi công cụ không đúng quyền.

### Nút thắt chính

Nút thắt không chỉ là tạo câu trả lời, mà là chuyển đổi dữ liệu phi cấu trúc thành một **Agent Specification** đầy đủ gồm mục tiêu, phạm vi, prompt, knowledge, tools, quyền, workflow, escalation rules và success metrics. Công đoạn này cần nhiều tri thức nghiệp vụ và thời gian của chuyên gia.

### Lý do cần giải quyết

Tự động hóa phần lớn quy trình trên giúp đội triển khai phục vụ nhiều doanh nghiệp hơn, giảm thời gian tạo bản thử nghiệm và chuẩn hóa khâu đánh giá trước khi vận hành.

## 4. Proposed AI Solution

### Agent-Building-Agent thực hiện gì?

Hệ thống gồm một Orchestrator và các agent chuyên trách:

| Thành phần | Trách nhiệm |
|---|---|
| Enterprise Profiler Agent | Trích xuất sản phẩm, kênh hỗ trợ, chính sách và các bên liên quan từ nguồn dữ liệu được cấp quyền |
| Process Analyst Agent | Ánh xạ dữ liệu vào APQC PCF 6.0, suy luận intent và SOP |
| Agent Architect | Tạo Agent Specification và lựa chọn kiến trúc RAG/tool-calling phù hợp |
| Builder Agent | Sinh prompt, skill, cấu hình knowledge base, tool schema và routing rules |
| Evaluation Agent | Sinh test case, chạy đánh giá và chấm groundedness, correctness, compliance, safety |
| Critic Agent | Phân tích lỗi, yêu cầu Builder Agent sửa cấu hình và kiểm thử lại |

### Input

- URL website chính thức.
- FAQ, catalog sản phẩm, chính sách, SOP và hướng dẫn nội bộ.
- Ticket đã ẩn danh hoặc bộ tình huống mẫu.
- Danh sách API cho phép tích hợp và chính sách quyền truy cập.
- Ngưỡng chất lượng do doanh nghiệp xác nhận.

### Output

- Hồ sơ doanh nghiệp và knowledge map.
- Danh sách intent, quy trình và ranh giới phạm vi.
- Agent Specification có phiên bản.
- Customer Service Agent MVP có thể chạy.
- Bộ dữ liệu đánh giá và báo cáo đạt/không đạt quality gate.

### Công cụ và tích hợp

- RAG trên tài liệu doanh nghiệp, vector database và metadata filtering.
- MCP hoặc API connector cho CRM, ticketing và tra cứu đơn hàng giả lập.
- Crawler chỉ đọc các miền được cho phép.
- Sandbox để kiểm thử tool call.
- Human-in-the-loop cho bước duyệt đặc tả và các hành động có tác động bên ngoài.

## 5. Proposed System

### Mục tiêu hệ thống

Tạo một nền tảng bán tự động có thể rút ngắn quá trình xây Customer Service Agent MVP, đồng thời cung cấp bằng chứng rằng agent đáp ứng yêu cầu nghiệp vụ trước khi triển khai.

### Chức năng chính

1. Tạo workspace cho từng doanh nghiệp và quản lý nguồn dữ liệu.
2. Trích xuất, chuẩn hóa và hiển thị knowledge map.
3. Ánh xạ quy trình sang APQC PCF và cho phép người dùng sửa kết quả.
4. Sinh, chỉnh sửa và phiên bản hóa Agent Specification.
5. Sinh agent runtime từ specification.
6. Sinh test suite từ tài liệu, SOP và ticket mẫu.
7. Chạy evaluation, hiển thị trace và phân tích lỗi.
8. Quản lý quality gate và xuất bản agent sang môi trường sandbox/staging.h

### Kiến trúc mức cao

```text
Nguồn dữ liệu doanh nghiệp
          |
Enterprise Profiler -> Knowledge Map -> Process Analyst
                                            |
                                     Agent Architect
                                            |
                             Agent Specification (versioned)
                                            |
                                      Builder Agent
                                            |
                              Customer Service Agent MVP
                                            |
                        Evaluation Agent <-> Critic Agent
                                            |
                              Quality gate + Human approval
```

### Công nghệ dự kiến

- Frontend: Next.js/React.
- Backend: Python FastAPI.
- Orchestration: LangGraph hoặc OpenAI Agents SDK.
- LLM: model thương mại qua API hoặc model mã nguồn mở phù hợp ngân sách.
- Dữ liệu: PostgreSQL, pgvector hoặc Qdrant; object storage cho tài liệu.
- Quan sát hệ thống: OpenTelemetry và dashboard execution trace.
- Môi trường thực thi: Docker sandbox; mock CRM/ticketing API.

### Phạm vi đồ án

- Chỉ tập trung vào một miền là chăm sóc khách hàng.
- Thử nghiệm với 2-3 hồ sơ doanh nghiệp giả lập hoặc dữ liệu đã ẩn danh.
- Chỉ triển khai 2 tool có khả năng ghi: tạo ticket và tạo yêu cầu chuyển cấp; mặc định chạy ở chế độ giả lập.
- Không tự động triển khai vào hệ thống production.
- Không huấn luyện foundation model mới.

## 6. Feasibility

### Dữ liệu và công nghệ

- Có thể tạo bộ dữ liệu từ website công khai, tài liệu chính sách mẫu và ticket tổng hợp.
- RAG, structured output, tool calling và multi-agent orchestration đã có thư viện hỗ trợ.
- APQC PCF tạo khung tham chiếu để giảm tính tùy ý khi suy luận quy trình.
- Có thể thay API thật bằng mock service để đánh giá an toàn trong phạm vi sinh viên.

### Độ khó và thời gian dự kiến

Mức độ khó: **Khá cao nhưng khả thi nếu giới hạn miền**.

| Giai đoạn | Thời lượng | Kết quả |
|---|---:|---|
| Khảo sát và thiết kế dữ liệu | 3 tuần | Schema doanh nghiệp, subset PCF, test corpus |
| Enterprise profiling và process mapping | 4 tuần | Knowledge map và SOP extraction |
| Agent specification và generator | 5 tuần | Agent MVP được sinh tự động |
| Evaluation và repair loop | 4 tuần | Test generator, quality gate, trace |
| Giao diện, thực nghiệm và báo cáo | 4 tuần | Prototype hoàn chỉnh và kết quả so sánh |

### Rủi ro và cách giảm thiểu

| Rủi ro | Giảm thiểu |
|---|---|
| Suy luận sai SOP do thiếu dữ liệu | Gắn mức tin cậy, trích dẫn nguồn và yêu cầu người dùng phê duyệt |
| Dữ liệu nhạy cảm | Ẩn danh, phân quyền theo workspace, mã hóa và audit log |
| Agent gọi sai công cụ | Allowlist tool, sandbox, giới hạn tham số và xác nhận của con người |
| Evaluation thiên lệch khi LLM tự chấm | Kết hợp rule-based checks, gold set và đánh giá thủ công |
| Scope quá lớn | Cố định APQC 6.0, giới hạn 2 tool và 2-3 bộ dữ liệu |

## 7. Evaluation

### Thiết kế thực nghiệm

So sánh ba phương án:

- **Baseline A:** một prompt chung và RAG, không sinh đặc tả riêng.
- **Baseline B:** chuyên gia cấu hình agent thủ công.
- **Proposed:** Agent Forge tự sinh agent, có evaluation/repair loop và bước duyệt của con người.

### Chỉ số đánh giá

| Nhóm | Chỉ số đề xuất |
|---|---|
| Hiệu quả triển khai | Thời gian từ dữ liệu đầu vào đến agent MVP; số phút chuyên gia can thiệp |
| Chất lượng trả lời | Correctness, groundedness, citation accuracy |
| Nghiệp vụ | Tỷ lệ phiên thành công = solved / (total - out-of-scope) |
| Phạm vi | Intent classification F1; tỷ lệ từ chối đúng với yêu cầu ngoài phạm vi |
| Tuân thủ và an toàn | Policy violation rate; unauthorized tool-call rate; prompt-injection success rate |
| Hiệu năng | Latency, token cost và số vòng repair trên mỗi agent |

### Điểm mạnh

- Bám sát bài toán Agent-Building-Agent trong tài liệu tham khảo.
- Có giá trị kinh doanh và kết quả dễ trình diễn.
- Có thể tạo thí nghiệm rõ ràng giữa thủ công và tự động.
- Kết quả trung gian như specification, test suite và trace đều kiểm tra được.

### Hạn chế

- Khó chứng minh khả năng tổng quát nếu chỉ thử trên ít doanh nghiệp.
- Chất lượng phụ thuộc mạnh vào dữ liệu đầu vào.
- Cần thiết kế permission và evaluation cẩn thận để tránh demo tốt nhưng không an toàn.

### Mức độ tiềm năng

**Rất cao.** Đây là case study gần nhất với định hướng của tài liệu "Agent tạo Agent", đồng thời có thể thu hẹp thành một prototype đủ sâu cho đồ án tốt nghiệp.

### Lý do nên chọn

Đề tài không dừng ở chatbot chăm sóc khách hàng. Đóng góp chính là quy trình có cấu trúc để tự động sinh, kiểm thử và quản trị vòng đời một agent chuyên biệt từ dữ liệu của doanh nghiệp.

## Tài liệu định hướng

- `../Tom-tat-de-tai-AI transformation.pdf` - định hướng Agent-Building-Agent, APQC PCF, pipeline ND1-ND5 và success metric.
- `../PHÂN CÔNG.md` - cấu trúc nội dung bắt buộc của case study.

