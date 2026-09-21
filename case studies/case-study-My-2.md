Nguyễn Thị Trà My

# **AI agent**

## **1\. Industry / Domain & Current Trend**

- **Lĩnh vực (Domain):** Software Engineering, Developer Tools (DevTools) & Automated Software Design.
- **Xu hướng ứng dụng AI:** Chuyển dịch từ AI hỗ trợ viết code đơn thuần (Code Completion) sang hệ thống **Multi-Agent tự vận hành (Agentic Workflows)** có khả năng phân tích yêu cầu nghiệp vụ, lập kế hoạch kiến trúc, tự kiểm tra quy chuẩn thiết kế và sinh tài liệu kỹ thuật hoàn chỉnh.
- **Lý do tiềm năng:** Giai đoạn thiết kế kiến trúc phần mềm (Software Architecture) đóng vai trò quyết định sự thành bại của dự án nhưng thường tốn nhiều thời gian họp bàn, dễ phát sinh sai sót logic giữa các tầng (Database - API - Business Logic) và thiếu tính nhất quán trong tài liệu. Việc tự động hóa khâu này giúp rút ngắn thời gian khởi tạo dự án từ vài tuần xuống vài phút.

## **2\. Business Process / User Workflow**

- **Quy trình nghiệp vụ hiện tại:**
  1. Business Analyst (BA) hoặc Product Owner (PO) thu thập yêu cầu nghiệp vụ và viết tài liệu SRS (Software Requirement Specification).
  2. Software Architect đọc tài liệu, phân tích thực thể và phác thảo mô hình CSDL (ERD/Schema).
  3. Lead Developer dựa trên CSDL để thiết kế danh sách API endpoints (Swagger/OpenAPI).
  4. Developers khởi tạo bộ khung source code (Boilerplate) và cấu hình dự án thủ công.
  5. Các bên họp rà soát (Review) để phát hiện mâu thuẫn giữa CSDL và API, điều chỉnh qua lại nhiều vòng.
- **Đối tượng tham gia:** Software Architects, Lead Developers, Business Analysts, System Engineers.

## **3\. Business Problem & Bottleneck**

- **Vấn đề & Khó khăn:**
  - **Tốn thời gian & Nguồn lực:** Mất từ 1–3 tuần cho giai đoạn System Design ban đầu cho mỗi dự án mới.
  - **Mất đồng bộ dữ liệu (Inconsistency):** Thiết kế API không khớp với Database Schema hoặc vi phạm các quy chuẩn thiết kế (RESTful standards, Indexing, Normalization).
  - **Thiếu tính linh hoạt:** Khi yêu cầu nghiệp vụ thay đổi, việc cập nhật thủ công đồng thời cả Schema, API Spec và Code Skeleton rất dễ bỏ sót.
- **Vì sao cần giải quyết:** Giúp các đội ngũ phát triển phần mềm tối ưu chi phí vận hành, chuẩn hóa kiến trúc ngay từ đầu và đẩy nhanh tốc độ tung sản phẩm ra thị trường (Time-to-Market).

## **4\. Proposed AI Agent Solution (Dành cho AI Agent)**

- **Vị trí tích hợp AI:** Toàn bộ lõi xử lý của hệ thống được xây dựng dưới dạng **Hệ thống Multi-Agent phối hợp tự động (Autonomous Collaborative Multi-Agent System)**.
- **Kiến trúc Multi-Agent bao gồm:**

1. **Requirements Analyst Agent:** Đọc văn bản yêu cầu nghiệp vụ (dạng thô), trích xuất danh sách Thực thể (Entities), Thuộc tính (Attributes), Luồng nghiệp vụ (Workflows) và Ràng buộc (Constraints).
2. **Database Architect Agent:** Đọc thông tin từ Analyst Agent để thiết kế Schema CSDL relational/non-relational, thiết kế chỉ mục (Indexing), chuẩn hóa dữ liệu và xuất file SQL Migration.
3. **API & Service Spec Agent:** Đọc Schema CSDL để tự động thiết kế chuẩn tài liệu OpenAPI 3.0 / Swagger (Routes, Request/Response Payload, Status Codes, Authentication).
4. **Architecture Validator & Reviewer Agent (Feedback Loop):** Đóng vai trò kiểm định, đối chiếu ngược API Spec với Database Schema và Requirements để phát hiện lỗi thiếu trường dữ liệu, sai kiểu dữ liệu hoặc vi phạm quy chuẩn RESTful. Nếu phát hiện lỗi, Agent này sẽ gửi thông điệp yêu cầu Database hoặc API Agent thiết kế lại.
5. **Code Boilerplate Generator Agent:** Nhận kết quả thiết kế đã được thẩm định để khởi tạo bộ khung Source Code chuẩn (Node.js/FastAPI/Spring Boot) sẵn sàng để chạy.

- **Cơ chế AgentIC:** Áp dụng **Pipeline Pattern kết hợp Reflection/Feedback Loop** và **Human-in-the-Loop** (cho phép con người xem và tinh chỉnh ở từng cột mốc).

## **5\. Proposed System**

- **Tên hệ thống:** **ArchAgent – Nền tảng Multi-Agent Tự động hóa Thiết kế Kiến trúc Phần mềm & API**.
- **Mục tiêu:** Biến mô tả yêu cầu nghiệp vụ dạng văn bản thô thành hệ thống sơ đồ kiến trúc, tài liệu API chuẩn mực và bộ khung Source Code thực thi được.
- **Đối tượng sử dụng:** Lập trình viên, Software Architect, Tech Lead, Sinh viên làm đồ án phần mềm.
- **Các chức năng chính:**
  - _Chức năng thông thường:_ Quản lý dự án thiết kế, Trình xem sơ đồ tương tác (Interactive Diagram Viewer), Xuất tài liệu (Export Swagger JSON/YAML, SQL File, Zip Source Code), Giao diện chỉnh sửa tinh chỉnh thủ công.
  - _Chức năng tích hợp AI Agent:_ Bóc tách yêu cầu tự động bằng Agent, Tự động sinh sơ đồ ERD & Sequence Diagram qua Mermaid.js, Tự kiểm tra & sửa lỗi thiết kế chéo giữa các Agent (Self-Correction Loop), Sinh bộ khung dự án (Boilerplate Code).
- **Công nghệ dự kiến sử dụng:**
  - _Frontend:_ ReactJS / Next.js, Mermaid.js (Hiển thị diagram), Swagger UI React.
  - _Backend & Agent Orchestration:_ Python (FastAPI), **LangGraph / AutoGen** (Quản lý trạng thái và luồng giao tiếp Multi-Agent), Model Context Protocol (MCP).
  - _Database & Storage:_ PostgreSQL (Lưu trữ dự án), Qdrant/Milvus (Vector Database lưu trữ Design Patterns/Standards cho RAG).
  - _LLM Provider:_ OpenAI API (gpt-4o / gpt-4o-mini), Anthropic Claude 3.5 Sonnet (Tối ưu cho sinh Code & JSON Schema).
- **Phạm vi dự kiến:** Tập trung hỗ trợ thiết kế các hệ thống Web Application / RESTful Web API tiêu chuẩn (Monolith hoặc Microservices cơ bản).

## **6\. Feasibility**

- **Tính khả thi dữ liệu & công nghệ:**
  - Các chuẩn định dạng như OpenAPI 3.0, SQL Syntax, Mermaid.js syntax đều có cấu trúc cực kỳ chặt chẽ, rất phù hợp để LLM sinh ra chính xác.
  - Framework LangGraph hiện tại đã hỗ trợ hoàn hảo việc quản lý trạng thái (State Management) và vòng lặp phản hồi (Feedback Loop) giữa nhiều Agent.
- **Model/API dự kiến sử dụng:** OpenAI gpt-4o-mini cho các tác vụ phân tích cơ bản, gpt-4o / Claude 3.5 Sonnet cho tác vụ thiết kế kiến trúc và đánh giá chéo.
- **Độ khó, Thời gian & Rủi ro:**
  - _Độ khó:_ **8.5/10 (Giỏi)** – Đòi hỏi hiểu biết sâu về Software Engineering, cách quản lý State trong Multi-Agent và xử lý Structured Output.
  - _Thời gian thực hiện:_ 6 tháng (24 tuần).
  - _Rủi ro:_ Agent bị lặp vô tận trong vòng lặp Feedback Loop khi không thỏa mãn được các ràng buộc thiết kế. _Giải pháp:_ Giới hạn số vòng lặp tối đa (Max Iterations = 3) và chuyển giao cho người dùng xử lý bằng giao diện Human-in-the-Loop.

## **7\. Evaluation**

- **Điểm mạnh:**
  - Tính thực tế và độc đáo cao, giải quyết trực tiếp bài toán kinh điển trong ngành Kỹ thuật phần mềm.
  - Thể hiện trọn vẹn sức mạnh của mô hình **Multi-Agent tự vận hành (Agentic AI)** thông qua cơ chế phân công vai trò, giao tiếp và tự sửa lỗi chéo.
  - Môi trường thực thi độc lập, an toàn tuyệt đối khi demo (không lo bị rào cản IP hay thay đổi DOM như các ứng dụng cào web).
- **Hạn chế:** Độ chính xác phụ thuộc vào mức độ chi tiết của văn bản yêu cầu đầu vào từ người dùng.
- **Mức độ tiềm năng:** Rất cao, có khả năng phát triển thành sản phẩm Commercial Developer Tool thương mại hóa.
- **Khả năng phát triển thành đồ án tốt nghiệp:** Cực kỳ hoàn hảo. Đáp ứng xuất sắc toàn bộ tiêu chí về độ phức tạp công nghệ, tính sáng tạo và giá trị kỹ thuật phần mềm.
- **Lý do nên chọn case study này:** Ghi điểm ở tính ứng dụng trực tiếp vào chuyên môn phần mềm; phân chia khối lượng công việc mạch lạc giữa việc xây dựng Agentic Engine, kiến trúc Backend và giao diện trực quan hóa.
