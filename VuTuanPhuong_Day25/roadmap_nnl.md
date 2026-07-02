# 🗺️ Lộ Trình Phát Triển Sản Phẩm (Now / Next / Later Roadmap)

Dự án **SCIDEX** tập trung giải quyết bài toán cốt lõi là tự động hóa trích xuất dữ liệu bài báo khoa học có kiểm chứng trước khi mở rộng quy mô. Lộ trình phát triển được phân bổ như sau:

---

## 🚀 NOW (Hiện tại - Phase 1: Core MVP)
*Tập trung xây dựng core workflow: Upload PDF ➔ Trích xuất ➔ Kiểm chứng (HITL) ➔ Xuất dữ liệu.*

*   **PDF Ingestion & Local Parsing:** Hỗ trợ upload tệp PDF trực tiếp. Phân tách PDF thành các text chunks dựa trên số trang và phân đoạn bằng `PyMuPDF` và `Grobid`.
*   **Dynamic Extraction Template:** Cho phép người dùng tự định nghĩa các trường dữ liệu cần trích xuất (tên trường, kiểu dữ liệu, bắt buộc/tùy chọn, mô tả).
*   **Structured AI Extraction:** Sử dụng LLMs (GPT-4o-mini/Claude-3-5-Sonnet) để trích xuất dữ liệu có cấu trúc (JSON) dựa trên template đã định nghĩa.
*   **Evidence-linked Data Table:** Giao diện bảng kết quả trích xuất, hỗ trợ nhấp chuột vào ô bất kỳ để mở Panel dẫn chứng (Raw Quote + Số trang) từ tệp PDF gốc.
*   **Human Verification Guardrail (HITL):** Cơ chế đánh dấu trạng thái ô dữ liệu (AI Extracted, User Edited, Verified, Not Found, Conflict) và ghi log lịch sử chỉnh sửa (Audit Log).
*   **Data Export (CSV):** Xuất dữ liệu bảng trích xuất ra định dạng CSV phục vụ phân tích meta-analysis.

---

## 📈 NEXT (Trung hạn - Phase 2: Mở rộng tính năng)
*Tăng tốc quy trình nhập liệu và nâng cao công cụ kiểm duyệt chất lượng dữ liệu.*

*   **Open Academic Search API:** Tích hợp công cụ tìm kiếm bài báo trực tuyến từ các nguồn Semantic Scholar và OpenAlex. Tự động tải PDF nếu là tài liệu mở (Open-access).
*   **AI Conflict & Contradiction Auditor:** LLM-powered agent tự động quét toàn bộ bảng và các paper để phát hiện các số liệu mâu thuẫn nội bộ hoặc mâu thuẫn giữa các bài viết (ví dụ: cỡ mẫu không khớp, kết quả trái ngược).
*   **Interactive PDF Viewer Highlight:** Khi click vào ô dữ liệu, trình đọc PDF tự động cuộn đến và bôi màu (highlight) trực tiếp cụm từ chứa dẫn chứng trên canvas.
*   **Styled Excel/XLSX Export:** Hỗ trợ xuất file Excel định dạng đẹp mắt, giữ nguyên trạng thái màu sắc của ô dữ liệu và đính kèm hyperlink dẫn chứng.

---

## 🔮 LATER (Dài hạn - Phase 3: Tối ưu hóa & Cộng tác)
*Xây dựng hệ sinh thái trợ lý nghiên cứu thông minh và môi trường cộng tác nhóm.*

*   **LangGraph Multi-Agent Chat Assistant:** Trợ lý ảo hiểu ngữ cảnh toàn bộ dự án, hỗ trợ so sánh phương pháp nghiên cứu, tổng hợp nhanh các kết quả và tự động đề xuất thêm trường dữ liệu cho template.
*   **PDF OCR Fallback Service:** Tích hợp mô hình OCR chạy trên GPU phục vụ việc parse các tài liệu scan cũ hoặc chất lượng kém.
*   **Team Collaboration Workspace:** Cho phép nhiều nhà nghiên cứu cùng chia sẻ dự án, phân quyền (Owner, Reviewer) và đồng bộ hóa thao tác verify dữ liệu theo thời gian thực.
*   **Advanced Meta-Analysis Visualization:** Tự động vẽ các biểu đồ thống kê cơ bản như Forest Plot, Funnel Plot dựa trên dữ liệu đã trích xuất sạch.
