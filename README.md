# 🚀 Day 26 Lab — Fundraising Intelligence (SCIDEX Project)

Repository này chứa toàn bộ các tài liệu nghiệm thu cho bài thực hành **Day 26 Lab — Fundraising Intelligence Brief** của học viên **Vũ Tuấn Phương**. 

Dự án được chọn làm trọng tâm nghiên cứu và lập kế hoạch gọi vốn là **SCIDEX** — Nền tảng AI hỗ trợ trích xuất dữ liệu bài báo khoa học chuẩn hóa, chống hallucination (được phát triển từ Day 24 & Day 25).

---

## 📂 Các tài liệu bàn giao (Lab Deliverables)

Bài thực hành được hoàn thành đầy đủ thông qua 3 tài liệu chính tương ứng với các bước yêu cầu:

### 1. 📝 [Bước 1: Deal Case Brief — Elicit Series A](Deal_Case_Brief.md)
*   **Nội dung**: Nghiên cứu và phân tích thương vụ gọi vốn thực tế trị giá **$22M vòng Series A** (công bố 02/2025) của **Elicit** (nền tảng trợ lý nghiên cứu AI có cơ chế kiểm chứng tương tự SCIDEX).
*   **Trọng tâm**: Định vị thương vụ vào các framework đầu tư (*Stages of Startup Equity Funding* & *Venture Capital vs Private Equity*) và kiểm chứng tính biệt lập công nghệ (*AI Differentiation Check*) nhằm tránh bẫy quảng cáo AI sáo rỗng.

### 2. 🗺️ [Bước 2: Investor Mapping — SCIDEX Project](Investor_Mapping.md)
*   **Nội dung**: Lập bản đồ và nghiên cứu chi tiết **3 nhà đầu tư mạo hiểm (VC/Accelerator)** thực tế tại khu vực Đông Nam Á & Việt Nam phù hợp với dự án SCIDEX bao gồm: **Antler**, **500 Global**, và **Techstars**.
*   **Trọng tâm**: Phân tích sâu khẩu vị đầu tư (*Investment Thesis*), quy mô vé đầu tư điển hình (*Ticket size*), tiêu chí tuyển chọn và đánh giá rủi ro/cơ hội gọi vốn của SCIDEX.

### 3. 📈 [Bước 3: Market Positioning Memo — SCIDEX Project](Market_Positioning_Memo.md)
*   **Nội dung**: Bản phân tích chiến lược dài 1 trang đánh giá tính khả thi gọi vốn của SCIDEX dựa trên dữ liệu sụt giảm dòng vốn VC 2025 và sự lên ngôi của xu hướng AI Agent / SaaS Challengers (YC Summer 2026).
*   **Trọng tâm**: Giải quyết triệt để lỗi tài chính mơ hồ (*Unclear Financials*) bằng cách đưa ra mô hình kinh tế đơn vị cụ thể (**Unit Economics** với biên lợi nhuận gộp 80%), kế hoạch sử dụng vốn (**Runway 27 tháng**) và các chỉ số **KPIs** cam kết cho vòng tiếp theo.

---

## 📊 Sơ lược dự án đầu vào: SCIDEX (Day 25)
Các tài liệu phân tích được đối chiếu trực tiếp từ hồ sơ thiết kế của dự án SCIDEX tại thư mục [VuTuanPhuong_Day25](VuTuanPhuong_Day25/):
*   [🎯 Mục Tiêu & Kết Quả Then Chốt (OKRs)](VuTuanPhuong_Day25/okrs.md)
*   [🗺️ Lộ Trình Phát Triển Sản Phẩm (Roadmap)](VuTuanPhuong_Day25/roadmap_nnl.md)
*   [📊 Ma Trận RICE & Phân Tích Value-Effort](VuTuanPhuong_Day25/rice_matrix.md)
*   [🗺️ Sơ Đồ Phụ Thuộc & Đường Găng Dự Án (Dependency Map)](VuTuanPhuong_Day25/dependency_map.md)

---

## 🔍 Hướng dẫn rà soát nhanh chất lượng (Checklist Tốt vs Chưa Đạt)
Toàn bộ các tài liệu trên được thiết kế bám sát bộ quy chuẩn đánh giá của Lab:
*   **Không viết chung chung**: Mọi lập luận tài chính và đánh giá nhà đầu tư đều đi kèm con số và bằng chứng cụ thể có trích dẫn nguồn.
*   **Giải quyết lỗi "Unclear Financials"**: Chi tiết hóa chi phí gọi API LLM (Input/Output tokens) và hạ tầng để tính ra giá vốn hàng bán (COGS) thực tế trên mỗi user.
*   **Giải quyết lỗi "Unclear Differentiation"**: Làm rõ rào cản kỹ thuật của SCIDEX nằm ở khâu parse cấu trúc tài liệu PDF phức tạp và hệ thống kiểm duyệt HITL (Human-in-the-loop) chứ không phải chỉ là vỏ bọc API ChatGPT.