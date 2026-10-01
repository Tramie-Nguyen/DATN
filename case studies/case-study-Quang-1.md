### 1. Industry / Domain & Current Trend

- **Case study thuộc lĩnh vực nào?**
- Dự án thuộc lĩnh vực **Thương mại điện tử (E-commerce)** và **Bán lẻ Thời trang & Phụ kiện (Fashion Retail)**, cụ thể là phân ngách kinh doanh **Kính mắt (Eyewear)**.

- **Xu hướng ứng dụng AI trong lĩnh vực đó:**
- **Virtual Try-On (VTO - Thử đồ ảo):** Ứng dụng công nghệ Thị giác máy tính (Computer Vision) và Thực tế tăng cường (AR/3D) để khách hàng "đeo thử" sản phẩm ảo với độ chính xác cao qua màn hình.
- **Nhận diện & Phân tích khuôn mặt (Facial Mapping):** AI quét, phân tích các điểm neo trên khuôn mặt để xác định hình dáng (tròn, vuông, trái xoan, v.v.) và tái tạo bản đồ 3D.
- **Hệ thống đề xuất cá nhân hóa (Personalized Recommendation):** Tự động tư vấn các sản phẩm phù hợp nhất dựa trên đặc điểm sinh trắc học và sở thích của từng cá nhân.

- **Vì sao lĩnh vực này có tiềm năng?**
- Kính mắt là mặt hàng mang tính cá nhân hóa cao, quyết định mua hàng phụ thuộc rất lớn vào sự vừa vặn và tính thẩm mỹ đối với khuôn mặt.
- Rào cản lớn nhất của mua sắm online là khách hàng **không thể thử trực tiếp**. Ứng dụng AI giúp xóa bỏ rào cản này, mang lại trải nghiệm "chân thực như tại cửa hàng" (Online-to-Offline), giúp doanh nghiệp tạo ra lợi thế cạnh tranh bứt phá và gia tăng doanh số.

---

### 2. Business Process / User Workflow

Hệ thống bao gồm 2 đối tượng tham gia chính với các luồng nghiệp vụ như sau:

- **Đối tượng 1: Người dùng (Khách hàng - Customer Workflow)**
- **Bước 1 - Khám phá:** Truy cập website, xem danh sách sản phẩm và sử dụng công cụ tìm kiếm.
- **Bước 2 - Xem chi tiết:** Click vào xem chi tiết sản phẩm. Người dùng có thể: Chọn màu sắc khả dụng, xem đánh giá (số sao trung bình), đọc bình luận (comment) của người mua trước, và tham khảo các sản phẩm tương tự cùng hãng.
- **Bước 3 - Trải nghiệm AI (Điểm nhấn):** Khách hàng bật camera để quét khuôn mặt. Website định hình shape mặt, dựng mô hình 3D cho phép tương tác (xoay, lật). Người dùng tiến hành thử các "Kiểu dáng kính đại diện".
- **Bước 4 - Nhận đề xuất & Chọn hàng:** Sau khi chốt được kiểu dáng đại diện phù hợp, hệ thống xuất ra danh sách các sản phẩm thực tế có form dáng tương ứng. Người dùng tùy chỉnh số lượng và bấm "Mua ngay" hoặc "Thêm vào giỏ hàng".
- **Bước 5 - Quản lý giỏ hàng:** Tại trang giỏ hàng, người dùng kiểm tra lại, có thể điều chỉnh số lượng hoặc xóa sản phẩm.
- **Bước 6 - Thanh toán (Checkout):** Nhập thông tin cá nhân/địa chỉ giao hàng và hoàn tất thanh toán. Người dùng có quyền tùy chỉnh và cập nhật thông tin cá nhân trong hồ sơ của mình.

- **Đối tượng 2: Quản trị viên (Admin Workflow)**
- **Quản lý Kho hàng:** Cập nhật số lượng tồn kho của các sản phẩm, đảm bảo dữ liệu đồng bộ.
- **Quản lý Doanh thu:** Theo dõi đơn hàng, báo cáo dòng tiền và doanh thu kinh doanh.
- **Quản lý Hệ thống:** Kiểm soát tài khoản và phân quyền hạn cho các user khác trên hệ thống.

---

### 3. Business Problem & Bottleneck

- **Vấn đề hoặc khó khăn hiện tại:**
- Khi mua kính online bằng cách xem ảnh 2D tĩnh, khách hàng thường mang tâm lý e ngại, không biết khuôn mặt mình hợp với form gọng nào. Sự thiếu chắc chắn này khiến họ dễ bị "ngợp" trước hàng trăm mẫu mã.

- **Bước nào tốn nhiều thời gian, chi phí hoặc nhân lực?**
- **Về phía khách hàng (Nút thắt chuyển đổi):** Bước **Cân nhắc & Ra quyết định** tốn rất nhiều thời gian. Sự đắn đo dẫn đến tỷ lệ thoát trang và tỷ lệ bỏ rơi giỏ hàng (Cart Abandonment) rất cao.
- **Về phía doanh nghiệp (Nút thắt chi phí):** Tốn nhiều chi phí Logistics (vận chuyển 2 chiều, lưu kho) và nguồn lực nhân sự (CSKH) để xử lý các đơn hàng hoàn trả (Return & Refund) do khách nhận kính đeo không hợp nên trả lại.

- **Vì sao cần giải quyết vấn đề này?**
- Gỡ bỏ được nút thắt "thử kính" sẽ trực tiếp làm **tăng tỷ lệ chuyển đổi (Conversion Rate)** từ người xem thành người mua.
- Giảm thiểu tối đa **tỷ lệ hoàn trả (Return Rate)**, qua đó tiết kiệm chi phí vận hành.
- Tạo ra Lợi thế bán hàng độc nhất (USP) giúp giữ chân khách hàng lâu dài.

---

### 4. AI-powered Application

- **AI được tích hợp vào chức năng nào của website?**
- Được tích hợp trực tiếp tại **Trang chi tiết sản phẩm** hoặc tạo thành một phân hệ **"Phòng thử kính 3D (Virtual Fitting Room)"** liên kết chặt chẽ với **Hệ thống đề xuất sản phẩm (Recommendation System)**.

- **Input và Output của AI là gì?**
- **Input (Đầu vào):**
- Dữ liệu hình ảnh/video trực tiếp từ Camera quét khuôn mặt người dùng.
- Lựa chọn "Kiểu dáng kính đại diện" (Form prototype) mà người dùng tương tác.

- **Output (Đầu ra):**
- _Về hình ảnh/3D:_ Kết quả định hình dáng mặt (Ví dụ: Khuôn mặt vuông). Xuất ra **mô hình 3D khuôn mặt của chính người dùng** (cho phép tương tác 360 độ). Đi kèm là hình ảnh 3D của dáng kính đại diện được đeo khớp lên mô hình theo tỷ lệ kích thước thực.
- _Về dữ liệu (Recommendation):_ Danh sách các mã sản phẩm (SKU) kính thực tế đang có sẵn trong kho, tương ứng với kiểu dáng đại diện mà khách hàng vừa chốt.

- **AI giúp giải quyết vấn đề như thế nào?**
- **Thay thế trí tưởng tượng bằng hình ảnh trực quan:** Người dùng không phải đoán mò nữa. Việc nhìn thấy chính bản thân (dưới dạng 3D) đang đeo kính ở nhiều góc độ giúp mang lại sự tự tin tuyệt đối, dẹp bỏ sự do dự để click "Mua ngay".
- **Đóng vai trò như phễu lọc thông minh (Chống quá tải lựa chọn):** Thay vì bắt khách hàng thử hàng trăm sản phẩm thật, AI đóng vai trò như một chuyên gia tư vấn: Đi từ bước _Chọn dáng đại diện_ -> _Đề xuất sản phẩm thực_. Điều này thu hẹp phạm vi lựa chọn, giúp hành trình mua sắm trở nên chính xác, mượt mà và hệ thống website cũng tải nhẹ nhàng hơn (do không phải render 3D toàn bộ kho hàng).
- **Tăng tính tương tác (Gamification):** Trải nghiệm thử kính 3D thú vị sẽ giữ chân người dùng ở lại trang web lâu hơn, tạo ra cảm xúc tích cực thúc đẩy quyết định chi tiền.
