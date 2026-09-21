# Case Study 01 - AI Agent cho quy trình tuyển dụng end-to-end

> **Hướng:** AI Agent  
> **Tên hệ thống đề xuất:** HireFlow Agent – Nền tảng Tuyển dụng Thông minh đa tác nhân  
> **Ý tưởng cốt lõi:** Hệ thống Multi-Agent tự động hóa toàn bộ quy trình tuyển dụng từ phân tích Job Description, sàng lọc CV, sinh câu hỏi phỏng vấn phù hợp, đến đánh giá ứng viên sau phỏng vấn – giúp bộ phận HR tập trung vào phán quyết cuối thay vì công việc lặp lại.

## 1. Industry / Domain & Current Trend

### Lĩnh vực

Case study thuộc lĩnh vực **Human Resources Technology (HRTech)** và **Talent Acquisition**, tương ứng với nhóm quy trình **5.0 - Develop and Manage Human Capital** trong APQC Process Classification Framework (PCF). Đây là một trong những quy trình tốn nhiều nhân lực thủ công nhất ở các doanh nghiệp vừa và nhỏ tại Việt Nam.

### Xu hướng ứng dụng AI

- Thị trường HRTech toàn cầu đang chuyển dịch từ công cụ lọc CV theo từ khóa (ATS truyền thống) sang hệ thống đánh giá ngữ nghĩa dựa trên embedding và LLM.
- AI được dùng để tự động phân tích mức độ phù hợp giữa ứng viên và vị trí, giảm thiểu thiên kiến (bias) trong quá trình sàng lọc ban đầu.
- Các công ty lớn như LinkedIn, Workday, Greenhouse đang tích hợp AI Agent để tự động gửi email nhắc lịch, sinh câu hỏi phỏng vấn kỹ thuật và tổng hợp ghi chú sau buổi phỏng vấn.
- Xu hướng nổi bật 2025–2026: **Agentic Recruiting** – agent chủ động theo dõi pipeline ứng viên, phát hiện rủi ro (ứng viên sắp rút lui, vị trí sắp quá hạn) và đề xuất hành động tiếp theo.

### Tiềm năng

Tuyển dụng là bài toán có dữ liệu đầu vào phong phú (CV, JD, ghi chú phỏng vấn), kết quả đo được (tỷ lệ qua vòng, thời gian tuyển, retention rate) và quy trình lặp lại cao. Đây là miền phù hợp để kiểm chứng hệ thống Multi-Agent trong một quy trình nghiệp vụ thực tế.

## 2. Business Process / User Workflow

### Đối tượng tham gia

- HR/Recruiter: người đăng tin, sàng lọc hồ sơ và sắp xếp phỏng vấn.
- Hiring Manager: người đặt yêu cầu tuyển dụng và ra quyết định cuối.
- Ứng viên: người nộp hồ sơ.
- Ban lãnh đạo: theo dõi hiệu quả tuyển dụng theo báo cáo.

### Quy trình hiện tại

1. Hiring Manager mô tả nhu cầu tuyển dụng bằng văn bản hoặc họp trực tiếp với HR.
2. HR soạn thảo Job Description, đăng lên các kênh tuyển dụng thủ công.
3. CV từ nhiều nguồn (email, website, LinkedIn) được tập hợp vào một folder hoặc ATS cơ bản.
4. HR đọc từng CV, lọc thủ công và ghi chú cảm nhận ban đầu.
5. HR liên hệ từng ứng viên, sắp xếp lịch phỏng vấn qua email hoặc điện thoại.
6. Interviewer chuẩn bị câu hỏi phỏng vấn theo kinh nghiệm cá nhân.
7. Sau phỏng vấn, interviewer điền form đánh giá hoặc gửi nhận xét qua email.
8. HR tổng hợp ý kiến, trình Hiring Manager ra quyết định.

### Quy trình đề xuất với HireFlow Agent

1. Hiring Manager nhập yêu cầu tuyển dụng dạng tự nhiên hoặc upload tài liệu nội bộ.
2. **JD Analyst Agent** phân tích yêu cầu, sinh Job Description chuẩn và trích xuất danh sách tiêu chí kỹ năng bắt buộc / mong muốn.
3. Hệ thống tiếp nhận CV từ nhiều nguồn; **CV Parser Agent** trích xuất thông tin thành cấu trúc chuẩn.
4. **Matching & Screening Agent** đánh giá mức độ phù hợp của từng ứng viên theo tiêu chí đã trích xuất, tạo shortlist kèm lý do.
5. HR xem shortlist, điều chỉnh thứ tự ưu tiên nếu cần, phê duyệt danh sách mời phỏng vấn.
6. **Interview Prep Agent** sinh bộ câu hỏi phỏng vấn cá nhân hóa dựa trên CV và JD, kèm rubric chấm điểm.
7. Sau phỏng vấn, interviewer ghi chú ngắn; **Evaluation Synthesis Agent** tổng hợp ghi chú, so sánh với rubric và tạo báo cáo ứng viên.
8. Hiring Manager xem báo cáo tổng hợp và ra quyết định cuối.

## 3. Business Problem & Bottleneck

### Vấn đề hiện tại

- HR tốn trung bình 23 giờ mỗi vị trí chỉ để sàng lọc CV ban đầu (theo LinkedIn Talent Solutions 2024).
- CV ở nhiều định dạng (PDF, Word, ảnh scan) gây khó khăn khi xử lý hàng loạt.
- Tiêu chí sàng lọc không nhất quán giữa các lần tuyển hoặc giữa các HR khác nhau.
- Câu hỏi phỏng vấn được chuẩn bị theo cảm tính, không bám vào điểm cần xác minh trên CV.
- Ghi chú phỏng vấn rời rạc, thiếu cấu trúc, khó tổng hợp khi nhiều interviewer cùng đánh giá một ứng viên.
- Thời gian từ nhận CV đến ra quyết định kéo dài, ứng viên giỏi thường nhận offer từ công ty khác trước.

### Nút thắt chính

Nút thắt không phải là thiếu ứng viên, mà là **tốc độ và chất lượng của vòng sàng lọc – chuẩn bị – đánh giá**. Ba bước này chiếm phần lớn thời gian HR và phụ thuộc nhiều vào cá nhân, dẫn đến thiếu nhất quán và khó mở rộng quy mô khi tuyển nhiều vị trí cùng lúc.

### Lý do cần giải quyết

Rút ngắn time-to-hire, tăng tính nhất quán trong đánh giá và giảm tải cho HR để họ tập trung vào phán quyết cuối và trải nghiệm ứng viên là những lợi ích đo được trực tiếp. Với doanh nghiệp vừa và nhỏ không có ATS đắt tiền, một hệ thống Agent phù hợp sẽ mang lại giá trị thực tiễn ngay.

## 4. Proposed AI Solution

### Kiến trúc Multi-Agent

Hệ thống gồm Orchestrator và các agent chuyên trách:

| Agent | Trách nhiệm |
|---|---|
| JD Analyst Agent | Phân tích yêu cầu tuyển dụng thô, sinh JD chuẩn và trích xuất scorecards (tiêu chí bắt buộc, mong muốn, red flag) |
| CV Parser Agent | Trích xuất thông tin có cấu trúc từ CV đa định dạng (PDF, DOCX, ảnh): học vấn, kinh nghiệm, kỹ năng, dự án |
| Matching & Screening Agent | So khớp ngữ nghĩa giữa CV và scorecard, xếp hạng ứng viên và sinh lý do kèm trích dẫn từ CV |
| Interview Prep Agent | Sinh bộ câu hỏi phỏng vấn cá nhân hóa theo khoảng trống trong CV so với JD, kèm rubric chấm điểm |
| Evaluation Synthesis Agent | Tổng hợp ghi chú từ nhiều interviewer, ánh xạ vào rubric, tạo báo cáo ứng viên có cấu trúc |
| Pipeline Monitor Agent | Theo dõi trạng thái từng ứng viên, cảnh báo khi có rủi ro trễ hoặc ứng viên chưa nhận phản hồi |

### Input

- Yêu cầu tuyển dụng dạng văn bản hoặc tài liệu nội bộ.
- CV ứng viên từ email, upload trực tiếp hoặc webhook từ job board.
- Ghi chú phỏng vấn (văn bản hoặc transcript từ công cụ ghi âm).
- Scorecard và rubric do HR / Hiring Manager xác nhận.

### Output

- Job Description chuẩn kèm scorecard.
- Danh sách ứng viên được xếp hạng kèm điểm và lý do ngắn gọn có trích dẫn từ CV.
- Bộ câu hỏi phỏng vấn cá nhân hóa và rubric đánh giá.
- Báo cáo tổng hợp ứng viên sau phỏng vấn.
- Dashboard trạng thái pipeline tuyển dụng theo thời gian thực.

### Công cụ và tích hợp

- OCR và document parsing cho CV đa định dạng (PDF/DOCX/ảnh).
- Embedding và semantic search để so khớp CV – JD.
- LLM với structured output để sinh scorecard, câu hỏi và báo cáo.
- Human-in-the-loop tại các bước phê duyệt shortlist, xác nhận câu hỏi và ra quyết định cuối.
- Webhook / API để nhận CV từ job board (mock trong phạm vi đồ án).

## 5. Proposed System

### Mục tiêu hệ thống

Xây dựng nền tảng tuyển dụng tích hợp Multi-Agent, giúp HR rút ngắn thời gian xử lý từng giai đoạn, đảm bảo tính nhất quán trong đánh giá và cung cấp khả năng kiểm chứng đầy đủ cho mọi quyết định.

### Chức năng không sử dụng AI

1. Quản lý vị trí tuyển dụng (tạo, cập nhật, đóng vị trí).
2. Tiếp nhận và lưu trữ hồ sơ ứng viên.
3. Quản lý pipeline ứng viên theo giai đoạn (Applied → Screened → Interview → Offer → Hired).
4. Lịch phỏng vấn và nhắc nhở.
5. Phân quyền HR, Hiring Manager và Interviewer.
6. Báo cáo và thống kê tuyển dụng (time-to-hire, nguồn ứng viên, tỷ lệ chuyển đổi).

### Chức năng tích hợp AI Agent

1. Tự động sinh JD và scorecard từ yêu cầu tuyển dụng thô.
2. Trích xuất thông tin cấu trúc từ CV đa định dạng.
3. Xếp hạng và giải thích mức độ phù hợp ứng viên – vị trí.
4. Sinh câu hỏi phỏng vấn cá nhân hóa và rubric đánh giá.
5. Tổng hợp ghi chú phỏng vấn thành báo cáo có cấu trúc.
6. Cảnh báo rủi ro pipeline (ứng viên chưa được liên hệ, vị trí sắp quá hạn).

### Kiến trúc mức cao

```text
Nguồn CV (email, upload, job board webhook)
            |
      CV Parser Agent
            |
   Matching & Screening Agent  <-- JD Analyst Agent (từ yêu cầu HR)
            |
        HR Review (Human-in-the-loop: phê duyệt shortlist)
            |
  Interview Prep Agent (sinh câu hỏi + rubric)
            |
   Interviewer ghi chú sau phỏng vấn
            |
 Evaluation Synthesis Agent (tổng hợp báo cáo)
            |
Hiring Manager ra quyết định cuối  <-- Pipeline Monitor Agent
```

### Công nghệ dự kiến

- Frontend: Next.js / React.
- Backend: Python FastAPI.
- Orchestration: LangGraph hoặc CrewAI.
- LLM: model thương mại qua API (GPT-4o-mini cho parsing, GPT-4o cho synthesis và câu hỏi phỏng vấn).
- Embedding & Vector Search: pgvector hoặc Qdrant để so khớp ngữ nghĩa CV – JD.
- Document Parsing: PyMuPDF, python-docx; OCR với Tesseract hoặc Cloud Vision API (cho CV dạng ảnh).
- Database: PostgreSQL.
- Quan sát hệ thống: LangSmith hoặc OpenTelemetry cho trace agent.

### Phạm vi đồ án

- Tập trung vào một loại vị trí tuyển dụng (ví dụ: lập trình viên hoặc nhân viên kinh doanh).
- Thử nghiệm với 3–5 vị trí mẫu và 50–100 CV giả lập hoặc dữ liệu đã ẩn danh.
- Không tích hợp với hệ thống email thật; dùng mock webhook.
- Không huấn luyện foundation model mới; dùng LLM có sẵn qua API.
- Không tự động gửi email mời phỏng vấn; chỉ đề xuất và chờ HR xác nhận.

## 6. Feasibility

### Dữ liệu và công nghệ

- CV mẫu có thể tổng hợp từ dataset công khai (Kaggle Resume Dataset) hoặc nhóm tự tạo kịch bản.
- JD mẫu lấy từ các job board thực tế đã công khai (LinkedIn, TopCV, ITviec).
- Embedding, semantic matching, LLM structured output và multi-agent orchestration đều có thư viện sẵn.
- Bộ dữ liệu đánh giá có thể xây dựng bằng cách gán nhãn thủ công mức độ phù hợp CV–JD.

### Độ khó và thời gian dự kiến

Mức độ khó: **Trung bình cao – khả thi trong 6 tháng nếu giới hạn loại vị trí và số lượng agent**.

| Giai đoạn | Thời lượng | Kết quả |
|---|---:|---|
| Khảo sát quy trình HR và thiết kế dữ liệu | 3 tuần | Schema ứng viên, scorecard mẫu, test corpus |
| JD Analyst và CV Parser Agent | 4 tuần | JD sinh tự động, CV trích xuất cấu trúc |
| Matching Agent và xếp hạng ứng viên | 4 tuần | Semantic ranking, lý do có trích dẫn |
| Interview Prep và Evaluation Synthesis Agent | 4 tuần | Câu hỏi cá nhân hóa, báo cáo tổng hợp |
| Pipeline Monitor, giao diện và thực nghiệm | 5 tuần | Prototype hoàn chỉnh, kết quả đánh giá |

### Rủi ro và cách giảm thiểu

| Rủi ro | Giảm thiểu |
|---|---|
| LLM sinh câu hỏi không phù hợp hoặc lặp lại | Thêm bước HR review và duyệt trước khi gửi interviewer |
| CV parser sai với định dạng phức tạp hoặc ảnh chất lượng thấp | Hiển thị kết quả parse và để HR chỉnh sửa thủ công |
| Matching Agent thiên kiến theo từ ngữ thay vì năng lực thực | Dùng embedding ngữ nghĩa, thêm rule-based check và giải thích lý do |
| Dữ liệu CV nhạy cảm | Ẩn danh toàn bộ dữ liệu thử nghiệm, phân quyền chặt và không lưu PII không cần thiết |
| Scope quá rộng (quá nhiều loại vị trí) | Cố định một nhóm nghề và giới hạn scorecard template |

## 7. Evaluation

### Câu hỏi nghiên cứu

1. Hệ thống Multi-Agent có rút ngắn thời gian sàng lọc CV so với quy trình thủ công không?
2. Danh sách shortlist do Agent tạo có tương quan với đánh giá của HR chuyên nghiệp không?
3. Câu hỏi phỏng vấn do Agent sinh ra có phù hợp và đủ thách thức so với câu hỏi do interviewer chuẩn bị thủ công không?
4. Báo cáo tổng hợp ứng viên có đủ thông tin để Hiring Manager ra quyết định không cần đọc lại toàn bộ ghi chú?

### Thiết kế thực nghiệm

So sánh ba phương án:

- **Baseline A:** Sàng lọc thủ công toàn bộ (không có AI).
- **Baseline B:** ATS theo từ khóa truyền thống (keyword matching).
- **Proposed:** HireFlow Multi-Agent với shortlist, câu hỏi và báo cáo tổng hợp.

### Chỉ số đánh giá

| Nhóm | Chỉ số đề xuất |
|---|---|
| Hiệu quả | Thời gian từ nhận CV đến có shortlist; số phút HR tiêu tốn mỗi ứng viên |
| Chất lượng shortlist | Precision / Recall so với đánh giá của HR chuyên nghiệp làm ground truth |
| Câu hỏi phỏng vấn | Relevance score (LLM-as-judge + human rating); tỷ lệ câu hỏi được interviewer giữ nguyên |
| Báo cáo tổng hợp | Completeness, factual accuracy so với ghi chú gốc; thời gian Hiring Manager đọc để ra quyết định |
| Trải nghiệm người dùng | SUS score với HR và Hiring Manager; acceptance rate của gợi ý AI |

### Điểm mạnh

- Quy trình tuyển dụng có đầu ra cụ thể và dễ đo, phù hợp thiết kế thực nghiệm.
- Đề tài có thể demo sinh động: nhập JD, tải 10 CV và xem agent tạo shortlist + câu hỏi trong thời gian thực.
- Kết hợp tốt giữa kỹ thuật (document parsing, semantic matching, multi-agent) và nghiệp vụ (HR workflow).
- Không phụ thuộc vào dữ liệu nhạy cảm vì có thể dùng CV tổng hợp.

### Hạn chế

- Khó đánh giá khách quan "chất lượng câu hỏi phỏng vấn" nếu không có interviewer thực tế tham gia user study.
- Matching Agent có thể thiên kiến theo từ ngữ nếu không được thiết kế cẩn thận.
- Hệ thống chỉ xử lý tốt CV tiếng Anh hoặc tiếng Việt chuẩn; CV lẫn lộn ngôn ngữ cần xử lý riêng.

### Mức độ tiềm năng

**Cao.** Bài toán thực tiễn, có thị trường rõ ràng (SME, startup), kết quả demo trực quan và đủ độ phức tạp kỹ thuật để thể hiện năng lực Multi-Agent orchestration trong đồ án tốt nghiệp.

### Lý do nên chọn

HireFlow Agent không chỉ là công cụ lọc CV. Đóng góp chính là quy trình agent có cấu trúc kết nối toàn bộ pipeline tuyển dụng từ yêu cầu đến quyết định, với human-in-the-loop ở các bước quan trọng và khả năng giải thích mọi đề xuất bằng trích dẫn từ dữ liệu gốc.

## Tài liệu định hướng

- `../PHÂN CÔNG.md` – cấu trúc nội dung bắt buộc của case study.
