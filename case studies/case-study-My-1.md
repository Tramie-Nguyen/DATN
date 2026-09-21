Nguyễn Thị Trà My

# **AI-powered application**

## **1. Industry / Domain & Current Trend**

- **Lĩnh vực (Domain):** FoodTech (Công nghệ F&B), Personal Health & Workplace Wellness.

- **Xu hướng ứng dụng AI:** Tự động hóa khâu cá nhân hóa thực đơn (Personalized Meal Planning) dựa trên chỉ số sinh học; trích xuất dữ liệu thực đơn đa định dạng qua Computer Vision/OCR; và ứng dụng AI Agent/RAG trong tư vấn dinh dưỡng tiêu dùng.

- **Lý do tiềm năng:** Nhu cầu ăn uống lành mạnh (Healthy Lifestyle) của dân văn phòng tại các đô thị lớn bùng nổ mạnh mẽ. Tuy nhiên, việc duy trì chế độ ăn chuẩn dinh dưỡng bằng đồ ăn mua ngoài gặp rào cản lớn do tốn thời gian chọn món, thiếu thông tin Calo/Macro thực tế và chi phí giao hàng đắt đỏ khi đặt lẻ tẻ.

## **2. Business Process / User Workflow**

- **Quy trình nghiệp vụ hiện tại:**
  1.  Người dùng (Dân văn phòng) đến giờ nghỉ trưa phải mở các app giao đồ ăn lướt chọn món thủ công.

  2.  Việc chọn món diễn ra theo cảm tính, không kiểm soát được năng lượng (Calo) và thành phần dinh dưỡng (Protein/Carb/Fat).

  3.  Người dùng đặt đơn lẻ tẻ, chịu phí giao hàng (Shipping Fee) cao.

  4.  Đồng nghiệp trong cùng công ty/tòa nhà khó gom đơn chung do thiếu công cụ đồng bộ giỏ hàng thời gian thực.

- **Đối tượng tham gia:** Dân văn phòng (End-user), Quản lý/Chủ quán ăn đối tác (Merchant), Nhân viên giao hàng (Rider / Group Courier).

## **3. Business Problem & Bottleneck**

- **Vấn đề & Khó khăn:**
  - **Quyết định chọn món tốn thời gian (Decision Fatigue):** Tốn 20–30 phút mỗi ngày chỉ để nghĩ "Hôm nay ăn gì?".

  - **Mất cân bằng dinh dưỡng:** Khó duy trì mục tiêu sức khỏe (Giảm cân/Tăng cơ/Ăn kiêng) khi ăn đồ ngoài do menu các quán không công bố chỉ số Calo/Macro.

  - **Phí giao hàng cao & Tắc nghẽn giờ cao điểm:** Đặt đơn riêng lẻ gây lãng phí tiền ship và quá tải luồng giao nhận tại sảnh tòa nhà văn phòng lúc 11h30–12h00.

- **Vì sao cần giải quyết:** Tối ưu hóa thời gian nghỉ trưa, kiểm soát sức khỏe vóc dáng cho người lao động, đồng thời giảm chi phí logistics và tăng sản lượng đơn hàng cho đối tác F&B.

## **4. Proposed AI Solution (Dành cho AI-powered Application)**

- **Vị trí tích hợp AI:**
  - Tích hợp vào tính năng **"Phân tích Menu & Trích xuất Dinh dưỡng tự động (Nutritional Menu Parser)"** ở giao diện Quản lý Nhà hàng.

  - Tích hợp vào tính năng **"Trợ lý Lên thực đơn tuần Cá nhân hóa (Smart AI Meal Planner)"** trên ứng dụng người dùng.

- **Input của AI:**
  - Ảnh chụp hoặc file PDF Menu của các quán ăn đối tác.

  - Thông tin cơ thể người dùng (TDEE, BMR, Chiều cao, Cân nặng, Mục tiêu sức khỏe) + Sở thích/Khẩu vị/Dị ứng.

- **Output của AI:**
  - Dữ liệu Menu đã được cấu trúc hóa kèm chỉ số Calo và Macro (Protein, Carb, Fat) ước tính cho từng món ăn.

  - Thực đơn tuần (7 ngày) được phối hợp tối ưu, đáp ứng chính xác hạn mức Calo/Macro mục tiêu của người dùng.

- **Giải pháp giải quyết vấn đề:** Giúp người dùng đặt món chuẩn dinh dưỡng chỉ với 1-Click mà không cần tự tính toán thủ công; đồng thời tự động biến các menu dạng ảnh phức tạp của quán ăn thành dữ liệu dinh dưỡng có cấu trúc.

## **5. Proposed System**

- **Tên hệ thống: NutriLunch AI** – Nền tảng Đặt Món Dinh dưỡng Cá nhân hóa & Tối ưu Luồng Gom Đơn Văn phòng.

- **Mục tiêu:** Tự động hóa khâu lập thực đơn dinh dưỡng cá nhân và tối ưu hóa luồng gom đơn đặt chung theo tòa nhà văn phòng.

- **Đối tượng sử dụng:** Nhân viên văn phòng, Quản lý/Chủ nhà hàng đối tác, Quản trị viên hệ thống (Admin).

- **Các chức năng chính:**
  - _Chức năng thông thường:_ Đặt đơn nhóm thời gian thực (Real-time Group Order via WebSockets), Gom đơn tự động theo tòa nhà/khu vực (Location-based Grouping), Quản lý ví/thanh toán, Báo cáo & Thống kê doanh thu cho nhà hàng đối tác.

  - _Chức năng tích hợp AI:_ Bóc tách & Nhận diện món ăn/dinh dưỡng từ ảnh Menu (OCR + Vision Engine), Sinh thực đơn tuần cá nhân hóa bằng AI RAG/LLM Agent, Recommendation Engine gợi ý món ăn thay thế có chỉ số dinh dưỡng tương đương.

- **Công nghệ dự kiến sử dụng:**
  - _Frontend:_ React Native / Flutter (Mobile App) + ReactJS / Next.js (Web Admin & Merchant Dashboard).

  - _Backend:_ Python (FastAPI) cho AI/Data Services + Node.js (NestJS) hoặc Go cho Core Business API.

  - _AI/Data Stack:_ VietOCR / PaddleOCR + OpenAI API / Llama-3 (Finetuned), Qdrant / Pinecone (Vector Database), LangChain / LangGraph.

  - _Architecture & Infrastructure:_ Microservices / Event-Driven Architecture (Apache Kafka / RabbitMQ), Redis (Caching & Distributed Lock), PostgreSQL + PostGIS (Truy vấn vị trí/không gian), Docker, Kubernetes, WebSockets.

- **Phạm vi dự kiến:** Tập trung phục vụ dân văn phòng và các đối tác F&B trong bán kính 3–5km tại các cụm văn phòng trọng điểm (như Quận 1, Quận 7, TP. Thủ Đức).

## **6. Feasibility**

- **Tính khả thi dữ liệu & công nghệ:** Thuật toán tính BMR/TDEE và phân bổ Macro chuẩn y khoa (Mifflin-St Jeor) rất rõ ràng và chuẩn xác.
  - OCR tiếng Việt và công nghệ Multimodal LLM (Vision) hiện tại xử lý đọc ảnh menu có độ chính xác cao.

  - Bài toán gom đơn (Group Order) và xử lý đồng thời (Concurrency) dựa trên các công nghệ Backend tiêu chuẩn (Redis, WebSockets).

- **Model/API dự kiến sử dụng:** OpenAI API <mark>(gpt-4o-mini</mark> / <mark>gpt-4o</mark> ), VietOCR cho bài toán bóc tách tiếng Việt, BGE-M3 (Embedding Model cho RAG).

- **Độ khó, Thời gian & Rủi ro:**
  - _Độ khó:_ **8.0/10 (Giỏi)** – Đòi hỏi xử lý bài toán Concurrency cao, kiến trúc Microservices phân tán và pipeline AI đa tầng.

  - _Thời gian thực hiện:_ 6 tháng (24 tuần)

  - _Rủi ro:_ Quán ăn hết món đột xuất hoặc ảnh menu quá mờ. _Giải pháp:_ Thiết kế cơ chế AI đề xuất món thay thế (Alternative Dish) tức thì và giao diện xác nhận lại cho chủ quán.

## **7. Evaluation**

- **Điểm mạnh:**
  - Bài toán thực tế, đánh đúng nhu cầu lớn của thị trường F&B và HealthTech đô thị.

  - Kỹ thuật: kết hợp toàn diện giữa Kiến trúc phần mềm nâng cao (Microservices, High Concurrency, Real-time Engine) và Xử lý dữ liệu chuyên sâu (Business Workflow, Data Pipeline, Analytics Dashboard).

  - Demo sinh động, dễ tương tác trực tiếp trước Hội đồng bảo vệ.

- **Hạn chế:** Phụ thuộc vào chất lượng ảnh chụp menu đầu vào của nhà hàng và độ ổn định kết nối mạng khi thực hiện Group Order thời gian thực.

- **Mức độ tiềm năng:** Rất cao, có khả năng thương mại hóa thành ứng dụng SaaS/Marketplace thực tế.

- **Khả năng phát triển thành đồ án tốt nghiệp:** Cực kỳ phù hợp. Đáp ứng hoàn hảo các tiêu chí khắt khe về tính quy mô, độ phức tạp công nghệ và tính hoàn thiện của sản phẩm.

- **Lý do nên chọn case study này:** Đề tài cân bằng xuất sắc giữa tính ứng dụng thực tế và độ sâu kỹ thuật
