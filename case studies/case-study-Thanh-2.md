# Case Study 02 - AI-powered Application gợi ý việc làm thêm và cơ hội freelance cho sinh viên

> **Hướng:** AI-powered Application  
> **Tên hệ thống đề xuất:** GigMatch – Nền tảng Gợi ý Cơ hội Việc làm thêm và Freelance cá nhân hóa cho Sinh viên  
> **Ý tưởng cốt lõi:** Ứng dụng web giúp sinh viên khai báo kỹ năng, kinh nghiệm và lịch rảnh một lần; AI liên tục gợi ý các cơ hội việc làm thêm, freelance và thực tập phù hợp từ nhiều nguồn – kèm giải thích lý do phù hợp và lộ trình kỹ năng cần bổ sung để tiếp cận cơ hội tốt hơn.

## 1. Industry / Domain & Current Trend

### Lĩnh vực

Case study thuộc lĩnh vực **EdTech / Career Development** và **Gig Economy Platform**, tập trung vào phân khúc sinh viên đang học đại học – nhóm người dùng có nhu cầu tìm kiếm thu nhập linh hoạt và xây dựng kinh nghiệm thực tế nhưng thiếu công cụ tìm kiếm phù hợp với lịch học và mức kỹ năng hiện tại.

### Xu hướng ứng dụng AI

- Nền kinh tế gig (gig economy) tăng trưởng mạnh tại Đông Nam Á sau 2022; Việt Nam có hơn 6 triệu lao động tự do (freelancer) tính đến 2024.
- Các nền tảng tuyển dụng lớn (LinkedIn, TopCV, ITviec) đang tích hợp AI để gợi ý việc làm theo profile, nhưng chưa tối ưu cho đặc thù sinh viên: lịch học thay đổi theo tuần, kỹ năng chưa hoàn chỉnh, mức lương mong đợi linh hoạt.
- Xu hướng 2025–2026: **Skill-based matching** thay thế keyword matching – AI đánh giá mức độ phù hợp dựa trên năng lực thực tế thay vì chức danh.
- AI đang được dùng để sinh **lộ trình kỹ năng** (skill roadmap) cá nhân hóa, giúp người dùng biết cần học gì để đủ điều kiện cho cơ hội mong muốn.

### Tiềm năng

Sinh viên đại học là nhóm người dùng đông, dễ tiếp cận qua kênh trường học và mạng xã hội, và có nhu cầu thực sự cấp bách (thu nhập + kinh nghiệm). Trong khi đó, các nền tảng hiện tại (Facebook Group, LinkedIn, TopCV) đều không được thiết kế dành riêng cho sinh viên với lịch học không đều và kỹ năng đang phát triển. Đây là khoảng trống thị trường rõ ràng và dễ kiểm chứng bằng user study trong trường đại học.

## 2. Business Process / User Workflow

### Đối tượng tham gia

- **Sinh viên:** người dùng chính, tìm kiếm cơ hội việc làm thêm / freelance / thực tập phù hợp.
- **Nhà tuyển dụng / khách hàng freelance:** đăng cơ hội ngắn hạn, bán thời gian hoặc dự án nhỏ.
- **Nhóm tốt nghiệp và đi làm sớm (early-career):** nhóm mở rộng nếu sản phẩm phát triển thêm.

### Quy trình hiện tại (không có hệ thống)

1. Sinh viên vào Facebook Group "Việc làm thêm TP.HCM", "Freelancer VN" và dò từng bài đăng thủ công.
2. Mở nhiều tab: TopCV, ITviec, Upwork, Fiverr đồng thời; tìm kiếm bằng từ khóa chung chung.
3. Đọc từng job description, tự đánh giá xem mình có đủ điều kiện không.
4. Ứng tuyển mà không biết cần bổ sung kỹ năng gì để tăng tỷ lệ được chọn.
5. Không có lịch sử theo dõi cơ hội đã ứng tuyển, kết quả ra sao.
6. Khi lịch học thay đổi theo kỳ mới, phải tìm lại từ đầu với bộ lọc thời gian mới.

### Quy trình đề xuất với GigMatch

1. Sinh viên tạo hồ sơ một lần: kỹ năng, môn học liên quan, kinh nghiệm, loại công việc mong muốn, lịch rảnh theo tuần và mức lương kỳ vọng.
2. AI phân tích hồ sơ, chuẩn hóa kỹ năng và sinh **Skill Profile** có cấu trúc.
3. Hệ thống thu thập cơ hội từ nhiều nguồn (job board tích hợp hoặc nguồn mock trong đồ án) và index theo kỹ năng, thời gian, loại hình.
4. **AI Matching Engine** gợi ý danh sách cơ hội phù hợp kèm **Match Score** và lý do cụ thể (kỹ năng nào khớp, kỹ năng nào còn thiếu).
5. Với các cơ hội sinh viên chưa đủ điều kiện hoàn toàn, AI gợi ý **Skill Gap & Roadmap**: cần học gì, tài nguyên nào, mất bao lâu.
6. Sinh viên lưu cơ hội quan tâm, đánh dấu đã ứng tuyển và ghi kết quả.
7. Hệ thống học từ lịch sử ứng tuyển và phản hồi để cải thiện gợi ý theo thời gian.

## 3. Business Problem & Bottleneck

### Vấn đề hiện tại

- Sinh viên mất 30–60 phút mỗi ngày dò tìm trên nhiều kênh, phần lớn là cơ hội không phù hợp với lịch học hoặc kỹ năng hiện tại.
- Không có cơ chế lọc theo **lịch rảnh thực tế** của sinh viên (thay đổi theo tuần, theo kỳ).
- Sinh viên không biết mình thiếu gì để đủ điều kiện cho các cơ hội tốt hơn.
- Nhà tuyển dụng cần người bán thời gian nhưng nhận CV thiếu thông tin về sự sẵn sàng (availability) thực tế.
- Không có nơi lưu trữ lịch sử cơ hội đã ứng tuyển và kết quả học được từ quá trình đó.

### Nút thắt chính

Nút thắt không phải là thiếu cơ hội – các cơ hội tồn tại rất nhiều. Vấn đề là **chi phí tìm kiếm quá cao và tỷ lệ phù hợp quá thấp** khi sinh viên phải tự lọc thủ công mà không có công cụ hiểu được đặc thù của họ (lịch học, kỹ năng đang phát triển, mức kỳ vọng linh hoạt).

### Lý do cần giải quyết

Giúp sinh viên tìm được cơ hội phù hợp nhanh hơn đồng thời biết cần phát triển kỹ năng gì là hai lợi ích có thể đo được: giảm thời gian tìm kiếm và tăng tỷ lệ ứng tuyển thành công. Về phía nhà tuyển dụng, tiếp cận đúng ứng viên sinh viên có kỹ năng phù hợp và sẵn sàng về thời gian cũng là giá trị rõ ràng.

## 4. Proposed AI Solution

AI được tích hợp vào bốn chức năng cốt lõi của ứng dụng. Người dùng luôn thấy lý do AI đưa ra và có thể điều chỉnh hồ sơ để thay đổi kết quả gợi ý.

### 4.1. Smart Profile Builder – Xây dựng hồ sơ kỹ năng thông minh

**Input:** Sinh viên điền thông tin tự do hoặc upload CV / LinkedIn URL.

**Output có cấu trúc:**

- Danh sách kỹ năng được chuẩn hóa theo taxonomy (lập trình, thiết kế, ngoại ngữ, kỹ năng mềm...).
- Mức độ thành thạo ước tính cho từng kỹ năng (beginner / intermediate / advanced).
- Loại công việc phù hợp dựa trên hồ sơ.
- Lịch rảnh được biểu diễn cấu trúc (ngày trong tuần + khung giờ).

Người dùng xem và chỉnh sửa từng mục trước khi hồ sơ được dùng để gợi ý.

### 4.2. AI Matching Engine – Gợi ý cơ hội cá nhân hóa

**Input:** Skill Profile của sinh viên + danh sách cơ hội đã index.

**Output:**

- Danh sách cơ hội được xếp hạng theo Match Score.
- Với mỗi cơ hội: lý do phù hợp (kỹ năng khớp, thời gian khớp), điểm cần chú ý (kỹ năng còn thiếu, yêu cầu kinh nghiệm cao hơn).
- Phân loại: "Phù hợp ngay", "Phù hợp sau khi bổ sung kỹ năng X", "Không phù hợp – lý do cụ thể".

Hệ thống cập nhật gợi ý khi sinh viên cập nhật hồ sơ hoặc lịch học thay đổi.

### 4.3. Skill Gap & Roadmap – Lộ trình phát triển kỹ năng

**Input:** Cơ hội sinh viên muốn nhắm đến + Skill Profile hiện tại.

**Output:**

- Danh sách kỹ năng đang thiếu so với yêu cầu của cơ hội.
- Gợi ý tài nguyên học (khóa học, chứng chỉ, dự án thực hành) cho từng kỹ năng.
- Ước tính thời gian cần thiết để đạt mức yêu cầu.

Người dùng có thể lưu roadmap và đánh dấu tiến độ.

### 4.4. Application Tracker với AI Insight – Theo dõi và học từ kết quả

**Input:** Lịch sử ứng tuyển và kết quả (được chọn / bị từ chối / chưa phản hồi).

**Output:**

- Tổng hợp tỷ lệ phản hồi theo loại cơ hội và mức Match Score.
- Gợi ý điều chỉnh hồ sơ dựa trên pattern ứng tuyển thành công.
- Nhắc nhở follow-up khi cơ hội chưa có phản hồi sau một số ngày.

## 5. Proposed System

### Mục tiêu hệ thống

Xây dựng web application giúp sinh viên tìm kiếm cơ hội việc làm thêm và freelance phù hợp nhanh hơn, đồng thời hiểu rõ lộ trình phát triển kỹ năng để tiếp cận cơ hội tốt hơn trong tương lai.

### Chức năng không sử dụng AI

1. Đăng ký, đăng nhập và quản lý hồ sơ sinh viên.
2. Nhà tuyển dụng đăng và quản lý cơ hội việc làm.
3. Tìm kiếm cơ hội bằng từ khóa và bộ lọc thủ công (loại, địa điểm, mức lương).
4. Lưu cơ hội quan tâm và quản lý danh sách đã ứng tuyển.
5. Thông báo khi có cơ hội mới phù hợp với bộ lọc đã đặt.
6. Xem chi tiết cơ hội và thông tin nhà tuyển dụng.

### Chức năng tích hợp AI

1. Phân tích và chuẩn hóa kỹ năng từ hồ sơ / CV đầu vào.
2. Gợi ý cơ hội cá nhân hóa theo Skill Profile và lịch rảnh.
3. Tính Match Score và giải thích lý do phù hợp / chưa phù hợp.
4. Phát hiện Skill Gap và sinh Roadmap học tập.
5. Phân tích lịch sử ứng tuyển và gợi ý cải thiện hồ sơ.
6. Tìm kiếm ngữ nghĩa trong kho cơ hội (hỏi "tìm việc liên quan đến thiết kế UI vào cuối tuần" thay vì chọn bộ lọc thủ công).

### Kiến trúc mức cao

```text
Web Client (sinh viên + nhà tuyển dụng)
          |
   Application API
     |           |
PostgreSQL   Object Storage
     |
AI Processing Pipeline
     |-- Profile parsing & skill normalization
     |-- Skill-based embedding & indexing
     |-- Matching Engine (semantic similarity + rule-based filter)
     |-- Skill Gap analysis & Roadmap generation
     |-- Application pattern analysis
     |
Feedback Loop (accept/reject gợi ý -> cải thiện ranking)
```

### Công nghệ dự kiến

- Frontend: Next.js / React; giao diện responsive phù hợp cả điện thoại.
- Backend: Python FastAPI.
- Database: PostgreSQL và pgvector.
- AI: embedding model cho semantic matching; LLM cho phân tích hồ sơ, giải thích Match Score và sinh Roadmap.
- Job indexing: crawler / mock data cho đồ án; có thể tích hợp API của TopCV hoặc ITviec nếu khả thi.
- Background jobs: Celery / Redis cho re-indexing và gợi ý định kỳ.
- Triển khai: Docker, VPS hoặc cloud free tier.

### Phạm vi MVP

- Web application responsive, ưu tiên mobile-friendly.
- Tập trung vào hai loại cơ hội: việc làm bán thời gian và dự án freelance ngắn hạn.
- Dữ liệu cơ hội từ nguồn mock hoặc crawl công khai từ các job board cho đồ án.
- Bốn tính năng AI bắt buộc: Smart Profile Builder, Matching Engine với Match Score, Skill Gap Roadmap và Application Tracker với insight.
- Semantic search là tính năng nâng cao nếu còn thời gian.
- Không xử lý thanh toán hay ký hợp đồng trong hệ thống.

## 6. Feasibility

### Dữ liệu và công nghệ

- Dữ liệu kỹ năng có thể xây dựng từ taxonomy công khai (ESCO skills, LinkedIn Skills taxonomy).
- Cơ hội việc làm mẫu có thể crawl từ TopCV, ITviec hoặc Facebook Group công khai (chỉ dùng cho nghiên cứu, ẩn danh nhà tuyển dụng).
- Embedding và semantic matching đã có thư viện sẵn; LLM structured output cho phân tích hồ sơ và sinh roadmap.
- Người dùng thử nghiệm dễ tuyển trong trường đại học (sinh viên IT, kinh tế, thiết kế...).

### Kế hoạch dữ liệu tối thiểu

- 200–300 hồ sơ sinh viên mẫu (nhóm tự tạo hoặc từ người tham gia tình nguyện, ẩn danh).
- 300–500 cơ hội việc làm thêm / freelance phân loại theo kỹ năng và loại hình.
- 100–150 cặp hồ sơ – cơ hội được gán nhãn mức độ phù hợp thủ công (ground truth cho Matching Engine).
- 20–30 kịch bản Skill Gap để đánh giá chất lượng Roadmap sinh ra.

### Độ khó và thời gian dự kiến

Mức độ khó: **Trung bình – phù hợp với đồ án có sản phẩm hoàn chỉnh và user study thực tế**.

| Giai đoạn | Thời lượng | Kết quả |
|---|---:|---|
| Khảo sát người dùng và thiết kế UX | 3 tuần | User flow, wireframe, persona sinh viên |
| Smart Profile Builder và skill normalization | 4 tuần | Hồ sơ cấu trúc, skill taxonomy |
| Matching Engine và job indexing | 5 tuần | Gợi ý có Match Score và giải thích |
| Skill Gap Roadmap và Application Tracker | 4 tuần | Roadmap cá nhân hóa, insight ứng tuyển |
| Đánh giá, tối ưu và hoàn thiện | 4 tuần | Benchmark, user study và prototype ổn định |

### Rủi ro và cách giảm thiểu

| Rủi ro | Giảm thiểu |
|---|---|
| Thiếu dữ liệu cơ hội thực | Xây mock dataset đa dạng, sau đó mở rộng bằng crawl có kiểm soát |
| Matching không chính xác với kỹ năng chưa chuẩn hóa | Cho phép sinh viên xác nhận / chỉnh sửa skill sau khi AI phân tích |
| Sinh viên không cập nhật hồ sơ định kỳ | Nhắc nhở tự động khi lịch học đổi kỳ; onboarding ngắn, dễ điền |
| Roadmap quá chung, không thực tế | Gắn tài nguyên học cụ thể (link Udemy, YouTube, GitHub) thay vì chỉ tên kỹ năng |
| Chi phí gọi LLM tăng khi nhiều người dùng | Cache profile analysis, batch Roadmap generation, dùng model nhỏ cho tác vụ đơn giản |

## 7. Evaluation

### Câu hỏi nghiên cứu

1. Gợi ý của AI có phù hợp hơn so với tìm kiếm từ khóa thủ công không (theo đánh giá của sinh viên)?
2. Match Score và lý do giải thích có giúp sinh viên ra quyết định ứng tuyển nhanh hơn không?
3. Skill Gap Roadmap có định hướng học tập thực tế và khả thi không?
4. Sinh viên có tiếp tục dùng hệ thống sau phiên đầu tiên không (retention)?

### Thiết kế thực nghiệm

So sánh ba phương án:

- **Baseline A:** Tìm kiếm thủ công trên Facebook Group và job board hiện tại.
- **Baseline B:** Tìm kiếm từ khóa trong GigMatch (không có AI gợi ý).
- **Proposed:** GigMatch với AI Matching, Match Score giải thích và Skill Gap Roadmap.

### Chỉ số đánh giá

| Chức năng AI | Chỉ số đề xuất |
|---|---|
| Smart Profile Builder | Accuracy của skill extraction; tỷ lệ sinh viên chỉnh sửa ít hơn 3 mục sau khi AI phân tích |
| Matching Engine | Precision@5 / Recall@10 so với ground truth; thời gian tìm được cơ hội phù hợp đầu tiên |
| Skill Gap Roadmap | Tỷ lệ roadmap được đánh giá là "thực tế và khả thi" trong user study; tài nguyên học được click |
| Application Tracker | Tỷ lệ insight được người dùng áp dụng; thay đổi Match Score trước/sau khi cập nhật hồ sơ |
| Trải nghiệm tổng thể | SUS score; thời gian từ onboarding đến ứng tuyển lần đầu; 7-day retention rate |

### Success criteria tham khảo

- Gợi ý AI đạt Precision@5 ≥ 0,70 so với ground truth do sinh viên gán nhãn.
- Sinh viên tìm được cơ hội phù hợp đầu tiên nhanh hơn ≥ 35% so với tìm kiếm thủ công.
- ≥ 70% Roadmap được đánh giá là "thực tế và có thể thực hiện được" trong user study.
- SUS score ≥ 70; 7-day retention ≥ 40%.

### Điểm mạnh

- Người dùng mục tiêu là sinh viên đại học – dễ tuyển, nhiều người có nhu cầu thực tế, phản hồi nhanh.
- Bài toán có thể demo trực tiếp và dễ quan sát kết quả trong user study ngắn hạn.
- Kết hợp tốt giữa phát triển web (profile, search, tracker), AI/NLP (skill parsing, matching) và UX research.
- Dữ liệu có thể xây dựng từ nguồn công khai và đóng góp tình nguyện từ sinh viên trong trường.
- Hướng phát triển rõ ràng: sau MVP có thể mở rộng sang mobile app và tích hợp API job board thật.

### Hạn chế

- Chất lượng gợi ý phụ thuộc mạnh vào độ phong phú và cập nhật của nguồn cơ hội – cần chiến lược data acquisition rõ ràng.
- Vấn đề cold start: sinh viên mới chưa có lịch sử thì gợi ý kém hơn; cần onboarding đủ thông tin.
- Cạnh tranh gián tiếp với LinkedIn và TopCV vốn có nguồn cơ hội lớn hơn nhiều.

### Mức độ tiềm năng

**Cao về khả năng tạo sản phẩm và kiểm thử với người dùng thật.** Đây là bài toán mà nhóm có thể tuyển người dùng thử ngay trong trường đại học, thu thập feedback thực và cải thiện trong vòng 1–2 sprint. Nếu hệ thống hoạt động tốt, tiềm năng thương mại hóa hoặc spin-off thành startup cũng rất khả thi.

### Lý do nên chọn

GigMatch thể hiện rõ mô hình **AI-powered Application**: ứng dụng hoạt động được khi không có AI (tìm kiếm, lọc thủ công), nhưng AI biến trải nghiệm từ dò tìm mệt mỏi thành gợi ý có giải thích rõ ràng và lộ trình phát triển cụ thể. Đề tài cân bằng giữa phát triển web, AI matching, semantic search và nghiên cứu người dùng – và có lợi thế lớn là **người dùng thử nghiệm ở ngay trong trường đại học**.

## Tài liệu định hướng

- `../PHÂN CÔNG.md` – cấu trúc nội dung bắt buộc của case study.
