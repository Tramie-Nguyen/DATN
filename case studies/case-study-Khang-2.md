# Case Study 02 - Không gian làm việc cá nhân tích hợp AI

> **Hướng:** AI-powered Application  
> **Tên hệ thống đề xuất:** ContextSpace - AI Personal Knowledge & Action Workspace  
> **Ý tưởng cốt lõi:** Một ứng dụng năng suất dùng hằng ngày, tương tự sự kết hợp giữa ứng dụng ghi chú, quản lý tài liệu và quản lý công việc. AI giúp người dùng biến nội dung rời rạc thành tri thức có cấu trúc, tìm lại thông tin theo ngữ nghĩa và chuyển ghi chú thành hành động cụ thể.

## 1. Industry / Domain & Current Trend

### Lĩnh vực

Case study thuộc lĩnh vực Productivity Software và Personal Knowledge Management. Đây là nhóm ứng dụng được cá nhân, sinh viên và nhân viên văn phòng sử dụng thường xuyên để:

- Ghi chú nhanh.
- Lưu tài liệu và đường dẫn.
- Theo dõi công việc.
- Viết nhật ký học tập hoặc nhật ký dự án.
- Quản lý tri thức cá nhân và làm việc nhóm.

### Xu hướng ứng dụng AI

- AI được tích hợp trực tiếp vào trình soạn thảo để tóm tắt, viết lại và mở rộng nội dung.
- Semantic search dần thay thế việc chỉ tìm kiếm theo từ khóa chính xác.
- Hệ thống có thể tự trích xuất chủ đề, thực thể, deadline và action item từ ghi chú.
- Trợ lý AI ngày càng sử dụng toàn bộ ngữ cảnh workspace thay vì chỉ xử lý một trang riêng lẻ.
- Người dùng quan tâm nhiều hơn đến nguồn gốc câu trả lời, quyền riêng tư và khả năng kiểm soát dữ liệu AI được phép đọc.

### Vì sao lĩnh vực này có tiềm năng?

Người dùng tạo ra nhiều nội dung nhưng thường không duy trì được hệ thống thư mục, tag và liên kết. Sau một thời gian, thông tin vẫn tồn tại nhưng khó tìm lại và ít tạo ra giá trị. AI phù hợp để giảm công sức tổ chức, nhưng ứng dụng vẫn phải bảo đảm người dùng kiểm soát nội dung và kiểm chứng được nguồn.

Đây cũng là bài toán dễ tiếp cận người dùng thử nghiệm trong môi trường đại học: sinh viên có thể dùng ứng dụng để quản lý môn học, đồ án, tài liệu, lịch họp và công việc cá nhân.

## 2. Business Process / User Workflow

### Đối tượng sử dụng

- Sinh viên quản lý bài học, đồ án và deadline.
- Nhân viên văn phòng quản lý ghi chú họp và công việc.
- Freelancer quản lý khách hàng, tài liệu và đầu việc.
- Nhóm nhỏ cần một workspace chung nhưng không muốn thiết lập quy trình phức tạp.

### Quy trình hiện tại

1. Người dùng ghi nội dung vào nhiều nơi như ứng dụng notes, tài liệu, chat cá nhân hoặc task manager.
2. Người dùng tự đặt tên, tạo folder, gắn tag và sắp xếp trang.
3. Sau cuộc họp hoặc buổi học, người dùng phải tự tóm tắt và chuyển nội dung thành task.
4. Khi cần thông tin cũ, người dùng tìm bằng từ khóa hoặc duyệt lại nhiều thư mục.
5. Nội dung liên quan thường không được liên kết với nhau.
6. Task được tạo nhưng thiếu bối cảnh hoặc không được cập nhật khi ghi chú thay đổi.
7. Những ghi chú quan trọng dần bị quên hoặc trở nên lỗi thời.

### Quy trình đề xuất với ContextSpace

1. Người dùng nhập ghi chú, dán nội dung, tải tài liệu hoặc tạo biên bản họp.
2. AI phân tích nội dung và đề xuất tiêu đề, chủ đề, tag, thực thể và workspace phù hợp.
3. AI phát hiện action item, deadline và người liên quan; người dùng duyệt trước khi tạo task.
4. Hệ thống đề xuất liên kết với các ghi chú hoặc dự án có liên quan.
5. Người dùng đặt câu hỏi bằng ngôn ngữ tự nhiên và nhận câu trả lời kèm trích dẫn tới từng đoạn nguồn.
6. Daily Review tổng hợp task đến hạn, nội dung mới, ghi chú nên xem lại và các điểm chưa rõ.
7. Khi có nội dung mâu thuẫn hoặc lỗi thời, AI cảnh báo để người dùng xác nhận phiên bản đúng.

## 3. Business Problem & Bottleneck

### Vấn đề hiện tại

- Thông tin cá nhân bị phân mảnh giữa nhiều ứng dụng.
- Việc tổ chức folder, tag và backlink cần kỷ luật thủ công.
- Tìm kiếm từ khóa thất bại khi người dùng không nhớ đúng cụm từ đã viết.
- Ghi chú cuộc họp chứa nhiều nhiệm vụ nhưng người dùng dễ bỏ sót khi chuyển sang task manager.
- Công cụ AI viết lại hoặc tóm tắt thường không hiểu đầy đủ bối cảnh của workspace.
- Câu trả lời do AI tạo ra có thể nghe hợp lý nhưng không có nguồn hoặc dùng dữ liệu không còn mới.

### Nút thắt chính

Nút thắt không phải là khả năng tạo thêm văn bản. Người dùng đã có quá nhiều nội dung. Vấn đề thực sự là biến nội dung thành một vòng đời hữu ích:

```text
Capture -> Understand -> Organize -> Retrieve -> Act -> Review
```

Mỗi bước hiện cần thao tác thủ công, còn các tính năng AI đơn lẻ thường không duy trì được quan hệ nhất quán giữa note, knowledge và task.

### Lý do cần giải quyết

Một workspace có khả năng hiểu ngữ cảnh giúp người dùng giảm thời gian sắp xếp, tìm lại đúng thông tin và không bỏ sót hành động quan trọng. Giá trị của AI được thể hiện ngay trong quy trình hằng ngày thay vì tồn tại như một chatbot tách biệt.

## 4. Proposed AI Solution

AI được tích hợp vào các chức năng cốt lõi của ứng dụng, nhưng mọi thay đổi cấu trúc hoặc hành động quan trọng đều cần người dùng xác nhận.

### 4.1. Smart Capture - hiểu nội dung khi ghi chú

**Input:** văn bản người dùng nhập, Markdown, PDF hoặc transcript được cung cấp hợp lệ.

**Output:**

- Tiêu đề đề xuất.
- Loại ghi chú: meeting, idea, learning note, project update hoặc reference.
- Tag và chủ đề.
- Thực thể như người, dự án, môn học và tổ chức.
- Tóm tắt ngắn.
- Action item và deadline candidate.

AI trả về structured output. Người dùng có thể chấp nhận, sửa hoặc bỏ từng đề xuất.

### 4.2. Semantic Organization - tổ chức và liên kết tri thức

- Tìm các ghi chú tương đồng về ngữ nghĩa.
- Đề xuất backlink kèm lý do và đoạn nội dung liên quan.
- Gom nhóm note thành topic hoặc project nhưng không tự ý di chuyển khi chưa được duyệt.
- Phát hiện note gần trùng lặp.
- Gợi ý hợp nhất hoặc đánh dấu một note là phiên bản mới hơn.

### 4.3. Ask Your Workspace - hỏi đáp có căn cứ

**Input:** câu hỏi tự nhiên và phạm vi người dùng chọn, ví dụ một project hoặc toàn bộ workspace cá nhân.

**Output:** câu trả lời tổng hợp, danh sách nguồn, đoạn trích dẫn liên quan và thời điểm cập nhật của từng nguồn.

Hệ thống phải:

- Chỉ sử dụng nội dung người dùng được phép truy cập.
- Phân biệt nội dung có trong nguồn với phần suy luận.
- Từ chối hoặc hỏi lại khi không đủ bằng chứng.
- Cho phép mở trực tiếp ghi chú nguồn từ câu trả lời.

### 4.4. Notes to Actions - chuyển nội dung thành công việc

- Trích xuất task, deadline, priority và context từ meeting note hoặc daily note.
- Phát hiện task trùng với task đã tồn tại.
- Giữ liên kết hai chiều giữa task và đoạn ghi chú nguồn.
- Đề xuất chia một task lớn thành checklist.
- Không tự gửi thông báo, giao việc hoặc thay đổi deadline nếu chưa được người dùng duyệt.

### 4.5. Daily Review - chủ động đưa thông tin trở lại đúng lúc

Mỗi ngày, AI tạo một bản tổng hợp gồm:

- Task đến hạn hoặc có nguy cơ trễ.
- Ghi chú mới chưa được xử lý.
- Nội dung liên quan đến các công việc hôm nay.
- Câu hỏi còn bỏ ngỏ trong meeting note.
- Ghi chú cũ có khả năng cần cập nhật.

Đây là điểm khác biệt quan trọng: AI không chỉ trả lời khi được hỏi mà còn giúp duy trì workspace. Tuy nhiên người dùng có thể tắt từng loại gợi ý.

## 5. Proposed System

### Mục tiêu hệ thống

Xây dựng một web application chứng minh rằng AI có thể giảm công sức tổ chức tri thức và chuyển đổi ghi chú thành hành động, đồng thời vẫn bảo đảm khả năng kiểm chứng, quyền riêng tư và quyền quyết định của người dùng.

### Chức năng không sử dụng AI

1. Đăng ký, đăng nhập và quản lý hồ sơ.
2. Tạo workspace cá nhân hoặc workspace nhóm nhỏ.
3. Trình soạn thảo note hỗ trợ Markdown/rich text.
4. Quản lý page, folder, tag và backlink.
5. Quản lý project, task, deadline và trạng thái.
6. Tìm kiếm từ khóa và filter.
7. Version history và soft delete.
8. Phân quyền owner, editor và viewer.

### Chức năng tích hợp AI

1. Tự động phân loại và đề xuất metadata cho note.
2. Tóm tắt nội dung theo mục đích.
3. Trích xuất action item và deadline.
4. Đề xuất liên kết giữa các note.
5. Semantic search và hỏi đáp có trích dẫn.
6. Phát hiện nội dung gần trùng, mâu thuẫn hoặc có khả năng lỗi thời.
7. Sinh Daily Review dựa trên note và task có liên quan.
8. Thu nhận phản hồi accept/reject để đo và cải thiện chất lượng gợi ý.

### Kiến trúc mức cao

```text
Web/Mobile-friendly Client
          |
   Workspace API
     |          |
PostgreSQL   Object Storage
     |
AI Processing Pipeline
     |-- Content extraction
     |-- Metadata and action extraction
     |-- Embedding and semantic retrieval
     |-- RAG answer generation with citations
     |-- Link and stale-content recommendation
     |
Suggestion Review + Audit Log
```

### Mô hình dữ liệu cốt lõi

- `User`, `Workspace`, `Membership`.
- `Page`, `Block`, `PageVersion`.
- `Tag`, `Entity`, `PageLink`.
- `Project`, `Task`, `TaskSource`.
- `Attachment`, `SourceChunk`, `Embedding`.
- `AISuggestion`, `SuggestionDecision`, `AIExecutionLog`.

### Công nghệ dự kiến

- Frontend: Next.js/React; responsive để dùng tốt trên laptop và điện thoại.
- Backend: FastAPI hoặc NestJS.
- Database: PostgreSQL và pgvector.
- Editor: TipTap, Lexical hoặc BlockNote.
- AI: embedding model cho semantic retrieval; LLM có structured output cho phân loại, trích xuất và tổng hợp.
- Xử lý nền: job queue cho indexing, document processing và Daily Review.
- Triển khai: Docker và object storage tương thích S3.

### Phạm vi MVP

- Web application responsive, chưa cần native mobile app.
- Hỗ trợ text/Markdown và PDF có text; chưa xử lý audio/video trực tiếp.
- Tập trung vào workspace cá nhân; collaboration chỉ ở mức chia sẻ page hoặc workspace nhỏ.
- Chỉ triển khai 4 tính năng AI bắt buộc: smart metadata, action extraction, semantic search và grounded Q&A.
- Daily Review và phát hiện nội dung lỗi thời là tính năng nâng cao nếu còn thời gian.
- Không cố xây bản sao đầy đủ của Notion.
- Không cho AI tự chỉnh sửa hoặc xóa note gốc.

## 6. Feasibility

### Dữ liệu và công nghệ

- Có thể xây bộ dữ liệu thử nghiệm từ ghi chú do nhóm tự tạo hoặc người tham gia tự nguyện cung cấp sau khi ẩn danh.
- Dữ liệu meeting note và task có thể tạo từ các kịch bản học tập, đồ án và công việc văn phòng.
- Embedding, vector search, RAG và structured output đều có công nghệ sẵn có.
- Phần lõi của ứng dụng là CRUD, editor và search, phù hợp năng lực của nhóm phát triển web.

### Kế hoạch dữ liệu tối thiểu

- 300-500 note thuộc nhiều chủ đề và loại nội dung.
- 150-250 action item được gán nhãn thủ công.
- 100-150 cặp note có liên quan và một tập negative pairs.
- 80-120 câu hỏi kèm note nguồn và đáp án tham chiếu.
- Dữ liệu chia theo người dùng hoặc workspace để tránh note gần giống xuất hiện ở cả tập phát triển và tập kiểm thử.

### Độ khó và thời gian dự kiến

Mức độ khó: **Trung bình đến khá**, phù hợp với đồ án có cả sản phẩm phần mềm và phần đánh giá AI.

| Giai đoạn | Thời lượng | Kết quả |
|---|---:|---|
| Khảo sát người dùng và thiết kế UX | 3 tuần | User flow, wireframe và tiêu chí thành công |
| Xây chức năng workspace cơ bản | 5 tuần | Editor, page, tag, task và permission |
| Xây pipeline AI và indexing | 4 tuần | Smart metadata, action extraction, embedding |
| Semantic search và grounded Q&A | 4 tuần | Retrieval, citation và feedback flow |
| Đánh giá, tối ưu và hoàn thiện | 4 tuần | Benchmark, user study và prototype ổn định |

### Rủi ro và cách giảm thiểu

| Rủi ro | Giảm thiểu |
|---|---|
| Phạm vi trở thành một bản sao Notion quá lớn | Chọn một workflow chính: capture -> organize -> retrieve -> act |
| AI gắn tag hoặc tạo task sai | Hiển thị dưới dạng suggestion và yêu cầu xác nhận |
| Q&A hallucination | Bắt buộc citation, threshold retrieval và câu trả lời "không đủ thông tin" |
| Lộ ghi chú cá nhân | Phân quyền theo workspace, mã hóa, không dùng dữ liệu người dùng để huấn luyện ngoài phạm vi đồng ý |
| Dataset nhỏ hoặc thiếu đa dạng | Xây kịch bản chuẩn và tuyển người dùng thử thuộc nhiều nhóm |
| Chi phí gọi model | Cache embedding, batch background jobs và dùng model nhỏ cho tác vụ phân loại |
| Daily Review gây phiền | Cho phép cấu hình và đo tỷ lệ gợi ý được mở/chấp nhận |

## 7. Evaluation

### Câu hỏi nghiên cứu

1. AI có giảm thời gian người dùng tổ chức và tìm lại ghi chú so với keyword search và thao tác thủ công không?
2. Kết hợp semantic retrieval và workspace context có cải thiện khả năng tìm đúng nguồn không?
3. Người dùng có hoàn thành nhiều action item hơn khi task được trích xuất và liên kết với note nguồn không?
4. Citation và suggestion review có giúp người dùng tin tưởng và kiểm soát AI tốt hơn không?

### Baseline

- **B1 - Manual:** người dùng tự gắn tag, tạo task và tìm bằng folder.
- **B2 - Keyword:** full-text search/BM25, không sử dụng embedding.
- **B3 - Generic AI:** LLM chỉ nhận note hiện tại, không có workspace retrieval.
- **Proposed:** AI tích hợp workspace context, semantic retrieval, citation và suggestion review.

### Chỉ số đánh giá chức năng AI

| Chức năng | Chỉ số đề xuất |
|---|---|
| Metadata suggestion | Precision@k, Recall@k, F1 và acceptance rate |
| Action extraction | Precision, recall, F1 cho task; MAE hoặc accuracy cho deadline |
| Related-note recommendation | Precision@k, Recall@k và nDCG@k |
| Semantic search | Success@k, MRR và thời gian tìm được đúng note |
| Grounded Q&A | Answer correctness, citation precision/recall và hallucination rate |
| Daily Review | Open rate, useful-item rate và dismissal rate |

### Đánh giá trải nghiệm người dùng

- Tuyển 12-20 người dùng mục tiêu.
- Chuẩn bị các nhiệm vụ: lưu một ghi chú, tìm lại thông tin, tạo task từ meeting note và trả lời câu hỏi dựa trên workspace.
- Mỗi người thực hiện với phiên bản baseline và phiên bản có AI; đảo thứ tự để giảm learning effect.
- Đo task completion time, số thao tác, tỷ lệ hoàn thành đúng và số lần phải sửa gợi ý.
- Thu thập SUS score, perceived usefulness, trust và mức tải nhận thức.

### Success criteria tham khảo

- Giảm ít nhất 25% thời gian tìm lại đúng ghi chú so với keyword search trong bộ thử nghiệm.
- Action extraction đạt F1 tối thiểu 0,80 trên tập test đã gán nhãn.
- Ít nhất 80% câu trả lời Q&A có citation đúng nguồn; hallucination rate dưới ngưỡng nhóm xác định trước.
- Ít nhất 70% gợi ý metadata/action trong user study được chấp nhận hoặc chỉ cần chỉnh sửa nhỏ.
- SUS score của prototype đạt từ 70 trở lên.

Các ngưỡng trên là giả thuyết ban đầu và cần được khóa trước khi chạy thực nghiệm chính thức.

### Điểm mạnh

- Đúng hướng áp dụng AI vào một ứng dụng người dùng có thể sử dụng hằng ngày.
- Có đầy đủ phần xây dựng software: editor, database, search, task và permission.
- AI nằm trong workflow chính, không phải chatbot gắn thêm cho có.
- Có nhiều chức năng đo được bằng cả benchmark offline và user study.
- Dễ tuyển người dùng thử trong trường đại học.

### Hạn chế

- Thị trường ứng dụng ghi chú và productivity đã có nhiều sản phẩm mạnh.
- Khó cạnh tranh về số lượng tính năng; đồ án phải tập trung vào một trải nghiệm cốt lõi.
- Giá trị của hệ thống tăng theo lượng dữ liệu, trong khi thử nghiệm ngắn hạn có thể chưa phản ánh thói quen lâu dài.
- Dữ liệu cá nhân đòi hỏi thiết kế bảo mật và quyền riêng tư nghiêm túc.

### Mức độ tiềm năng

**Cao về khả năng tạo sản phẩm và kiểm thử với người dùng thật.** Tính mới thấp hơn hướng Agent tạo Agent, nhưng tính ứng dụng, UX và khả năng hoàn thành tốt hơn.

### Lý do nên chọn

ContextSpace thể hiện rõ mô hình **AI-powered Application**: một ứng dụng thông thường vẫn hoạt động được khi không có AI, nhưng AI giúp các workflow ghi chú, tìm kiếm và quản lý công việc nhanh và thông minh hơn. Đề tài cân bằng giữa phát triển web, AI/NLP, information retrieval và nghiên cứu người dùng.

## Tài liệu định hướng

- `../Tom-tat-de-tai-AI transformation.pdf` - tham khảo cách xác định quy trình, chức năng AI, evaluation và success metric.
- `../PHÂN CÔNG.md` - cấu trúc nội dung bắt buộc của case study.
