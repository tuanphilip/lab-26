# 🎯 Mục Tiêu & Kết Quả Then Chốt (OKRs - Q3/2026)

Mục tiêu quản trị trong quý 3 năm 2026 của dự án **SCIDEX** tập trung hoàn toàn vào việc kiểm chứng chất lượng trích xuất dữ liệu học thuật, tối ưu hóa năng suất cho nhà nghiên cứu và chuẩn bị sẵn sàng hạ tầng kinh doanh.

---

## 🎯 Objective (Mục tiêu chiến lược)
> **Thiết lập SCIDEX thành nền tảng AI hỗ trợ trích xuất dữ liệu bài báo khoa học tiêu chuẩn, tối ưu hóa năng suất đọc hiểu và đảm bảo tính chính xác tuyệt đối của dữ liệu nghiên cứu.**

---

## 📊 Key Results (Kết quả then chốt đo lường được)

### 📈 Key Result 1: Tiết kiệm tối thiểu 95% thời gian trích xuất dữ liệu bài báo khoa học
*   **Mô tả:** Giảm thời gian trung bình để đọc hiểu, bóc tách dữ liệu và lập bảng so sánh cho một tập **5 bài báo khoa học (tổng khoảng 100 trang PDF) từ 4 giờ xuống dưới 10 phút** (bao gồm cả thời gian chạy AI và con người kiểm tra/verify).
*   **Cách đo lường:** Hệ thống ghi nhận thời gian từ lúc tạo project, upload PDF cho đến khi người dùng nhấn Export CSV/Excel.
*   **Target:** Thời gian trung bình E2E cho 5 PDFs < 10 phút đối với 80% số lượt chạy trong quý.

### 🛡️ Key Result 2: Đạt 100% tỷ lệ đối chiếu dẫn chứng (Evidence Coverage) và triệt tiêu Hallucination
*   **Mô tả:** Đảm bảo tất cả dữ liệu được AI điền vào bảng trích xuất (ngoại trừ các ô được gắn nhãn `[Not Found]`) đều phải có **bằng chứng cụ thể (Raw Quote + Số trang)** được trích trực tiếp từ văn bản gốc, không tự suy diễn.
*   **Cách đo lường:** Bộ kiểm duyệt tự động (Verifier Layer) rà soát 100% các ô dữ liệu trước khi lưu trữ vào cơ sở dữ liệu.
*   **Target:** 100% số ô có dữ liệu hiển thị trên giao diện đều có liên kết dẫn chứng hợp lệ.

### 👥 Key Result 3: Đạt tỷ lệ Verified Rate > 80% trước khi người dùng thực hiện xuất dữ liệu (Export)
*   **Mô tả:** Khuyến khích quy trình Human-in-the-loop (con người kiểm chứng). Đảm bảo người dùng thực hiện rà soát, chỉnh sửa và nhấn nút "Verify" cho phần lớn các ô dữ liệu trước khi tải báo cáo Excel/CSV về máy.
*   **Cách đo lường:** Hệ thống lưu vết Audit Log ghi nhận tỷ lệ số ô đã được xác nhận (Status = Verified) trên tổng số ô được xuất ra.
*   **Target:** Trung bình trên toàn hệ thống đạt tỷ lệ > 80% dữ liệu xuất ra đã qua bước kiểm duyệt của người dùng.
