### 1. Industry / Domain & Current Trend

- **Case study thuộc lĩnh vực nào?**
- Thuộc lĩnh vực **Thương mại điện tử (E-commerce)**, tập trung vào phân hệ **Vận hành đơn hàng (Operations)** và **Chăm sóc Khách hàng sau mua (After-sales Customer Service)**.

- **Xu hướng ứng dụng AI trong lĩnh vực đó:**
- Sự dịch chuyển từ Chatbot trả lời theo kịch bản cứng nhắc (Rule-based Chatbot) sang **Autonomous AI Agents (Tác tử AI tự trị)**.
- Ứng dụng LLM (Mô hình ngôn ngữ lớn) làm "bộ não" kết hợp với tính năng gọi hàm (Function Calling / Tool Use) để Agent có thể tự động giao tiếp với các phần mềm khác (hệ thống kho, đối tác vận chuyển, cổng thanh toán) và thực thi nghiệp vụ thay cho con người.

- **Vì sao lĩnh vực này có tiềm năng?**
- Doanh nghiệp E-commerce luôn đối mặt với lượng tin nhắn hỗ trợ khổng lồ. Tuy nhiên, 70-80% yêu cầu của khách hàng là những vấn đề lặp đi lặp lại (kiểm tra trạng thái đơn, xin đổi/trả hàng, thay đổi địa chỉ).
- Tự động hóa bằng AI Agent giúp doanh nghiệp đạt được "Siêu tự động hóa" (Hyper-automation): Hoạt động 24/7, dễ dàng mở rộng quy mô (Scale-up) trong các dịp Mega Sale mà không làm "phình to" chi phí nhân sự trực ca (OPEX), đồng thời mang lại trải nghiệm hỗ trợ tức thì (Real-time) cho khách hàng.

---

### 2. Business Process / User Workflow

_Lấy đại diện là Quy trình xử lý yêu cầu: Kiểm tra hành trình đơn hàng và Thay đổi thông tin nhận hàng._

- **Các đối tượng tham gia:** Khách hàng (Customer), Nhân viên CSKH (CS Staff), Nhân viên Kho/Vận chuyển (Ops/Warehouse Staff).
- **Những bước chính (Luồng xử lý thủ công hiện tại khi chưa có AI):**
- **Bước 1:** Khách hàng nhắn tin cho shop yêu cầu: _"Tôi muốn đổi địa chỉ nhận hàng cho đơn kính râm hôm qua sang công ty"_ hoặc _"Kính của tôi bao giờ giao tới?"_.
- **Bước 2:** Nhân viên CSKH đọc tin nhắn, tiếp nhận và xin khách hàng mã đơn.
- **Bước 3:** Nhân viên thu thập mã, mở phần mềm Quản lý đơn hàng (CRM/OMS nội bộ) để tra cứu.
- **Bước 4:** Nhân viên kiểm tra xem đơn hàng đã xuất kho chưa (Thường phải mở thêm một tab trình duyệt của hãng vận chuyển như GHTK, Viettel Post để check chéo).
- **Bước 5:** Đối chiếu quy định.
- Nếu đơn _chưa xuất kho_: Nhân viên tiến hành sửa địa chỉ trên hệ thống, lưu lại và báo cho bộ phận kho.
- Nếu đơn _đã giao cho shipper_: Nhân viên báo lại khách là không thể đổi, hoặc phải tạo một Ticket (phiếu yêu cầu) gửi hãng vận chuyển để xin hỗ trợ.
- **Bước 6:** Nhân viên chat phản hồi lại kết quả cuối cùng cho khách hàng.

---

### 3. Business Problem & Bottleneck

- **Vấn đề hoặc khó khăn hiện tại:**
- Dữ liệu bị phân mảnh qua nhiều hệ thống. Quy trình phụ thuộc 100% vào con người nên dễ xảy ra sai sót hoặc chậm trễ khi lượng tin nhắn quá tải.

- **Bước nào tốn nhiều thời gian, chi phí hoặc nhân lực?**
- **Các Bước 3, 4 và 5** (Tra cứu chéo dữ liệu đa nền tảng và thao tác sửa trên hệ thống) là nút thắt cổ chai lớn nhất. Việc chuyển đổi liên tục giữa các phần mềm (Context switching) khiến một nhân viên mất từ 5 - 15 phút xử lý cho một yêu cầu rất cơ bản.
- **Nút thắt chi phí:** Doanh nghiệp tốn kém ngân sách lớn để duy trì đội ngũ trực ca (đặc biệt là ca đêm/cuối tuần) chỉ để giải quyết những sự vụ mang tính "thủ công tay chân".

- **Vì sao cần giải quyết vấn đề này?**
- Tốc độ phản hồi quyết định trải nghiệm người dùng trong E-commerce. Việc để khách chờ đợi lâu dễ dẫn đến bức xúc, làm tăng tỷ lệ hủy đơn, bom hàng (Return rate) và nhận các đánh giá 1 sao.
- Giải quyết nút thắt này sẽ giải phóng hoàn toàn nhân viên CSKH, để họ tập trung vào các nghiệp vụ tạo ra doanh thu như: Tư vấn bán chéo (Upsell/Cross-sell) hoặc xử lý các ca khiếu nại phức tạp cần sự đồng cảm của con người.

---

### 4. AI Agent (Tác tử AI tự động hóa)

- **Agent sẽ thực hiện hoặc hỗ trợ công việc nào?**
- Đóng vai trò như một **Nhân viên Hỗ trợ & Điều phối đơn hàng tuyến 1 (Tier-1 Ops & Support Agent)** túc trực đa kênh (Website, Zalo, Fanpage).
- Giải quyết trọn gói các nghiệp vụ Hậu mãi (Post-purchase): Tra cứu hành trình đơn hàng thời gian thực, thay đổi thông tin (địa chỉ, SĐT), tự động xét duyệt và xử lý quy trình Hủy đơn/Hoàn tiền/Đổi trả theo đúng luật của doanh nghiệp.

- **Agent có thể tự động thực hiện những bước nào?**
- _(Luồng tự động hóa End-to-End không cần con người)_
- **1. Tự động nhận diện ý định & Trích xuất:** Hiểu yêu cầu từ ngôn ngữ tự nhiên (kể cả khách chat sai chính tả hoặc viết tắt). Tự bóc tách ra các biến số như "Mã đơn hàng", "Địa chỉ mới".
- **2. Tự động tra cứu đa hệ thống:** Tự động kết nối vào ERP nội bộ và hệ thống của bên Vận chuyển để xem trạng thái đơn hàng.
- **3. Tự động suy luận & Ra quyết định (Reasoning):** Dựa vào trạng thái đơn, Agent tự đối chiếu với "Luật" của doanh nghiệp. (Ví dụ: Agent "tự biết" chỉ được phép sửa địa chỉ khi kiện hàng có status là _Chưa đóng gói_. Nếu đã _Bàn giao shipper_, nó sẽ từ chối khéo léo).
- **4. Tự động thực thi hành động (Action/Tool Use):** Agent "tự tay" gọi lệnh sửa thông tin địa chỉ trực tiếp trên Database, hoặc tự động kích hoạt lệnh Hủy đơn/Hoàn tiền mà không cần Admin duyệt.
- **5. Tự động chuyển giao (Human Handoff):** Nếu gặp khách hàng đang tức giận (Phân tích cảm xúc) hoặc yêu cầu vượt quá thẩm quyền, Agent lập tức tóm tắt toàn bộ lịch sử chat và tự động tạo Ticket chuyển cho đúng nhân viên con người xử lý.

- **Agent cần sử dụng công cụ, database hoặc API nào?**
  Để Agent có thể "suy nghĩ" và "có tay chân để hành động", nó cần được cung cấp quyền truy cập vào:
- **Bộ não (LLM Core):** Các mô hình mạnh về Tool Calling như GPT-4o, Claude 3.5 Sonnet hoặc Gemini.
- **Databases (Cơ sở dữ liệu):**
- _Vector Database (VD: Pinecone, Milvus):_ Chứa tài liệu Chính sách công ty, FAQ nội bộ để Agent tham chiếu (ứng dụng công nghệ RAG giúp Agent trả lời chuẩn xác, không bịa đặt).
- _Customer/Order Database:_ CSDL SQL/NoSQL nội bộ lưu trữ lịch sử mua sắm, trạng thái tồn kho.

- **APIs (Công cụ thực thi nghiệp vụ):**
- _OMS/E-commerce API (Shopify, Haravan, Magento...):_ Lệnh đọc/ghi để Agent có thể `get_order_status()`, `update_shipping_address()`, `cancel_order()`.
- _Logistics API (GHTK, Viettel Post, Ninja Van):_ Lệnh `track_shipment()` để lấy tọa độ vận đơn thực tế.
- _Payment Gateway API (VNPay, Momo, Stripe):_ Để Agent thực hiện lệnh hoàn tiền `process_refund()`.
- _Ticketing API (Zendesk, Freshdesk):_ Tạo phiếu hỗ trợ `create_ticket()` khi cần chuyển giao cho nhân sự con người.
