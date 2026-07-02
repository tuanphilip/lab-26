# 📊 Ma Trận RICE & Phân Tích Value-Effort (SCIDEX)

Dưới đây là bảng chấm điểm RICE và ma trận 2x2 Value-Effort áp dụng cho các tính năng của dự án **SCIDEX (AI Research Data Extraction for Systematic Review)**.

---

## 1. Bảng Chấm Điểm RICE (RICE Matrix)

Để chấm điểm các tính năng, chúng ta giả định tập người dùng mục tiêu ban đầu là **1,000 nhà nghiên cứu hoạt động tích cực mỗi tháng**.
*   **Reach (Độ phủ):** Số lượng người dùng sử dụng tính năng trong một tháng.
*   **Impact (Mức độ tác động):** Điểm đánh giá tác động (3 = Rất lớn, 2 = Lớn, 1 = Trung bình, 0.5 = Thấp, 0.25 = Rất thấp).
*   **Confidence (Độ tin cậy):** Xác suất thành công về kỹ thuật và giá trị (100% = Rất cao, 80% = Cao, 50% = Trung bình).
*   **Effort (Công sức):** Số tháng-người (Person-Months) cần để hoàn thành tính năng.

**Công thức RICE:**
$$\text{RICE Score} = \frac{\text{Reach} \times \text{Impact} \times \text{Confidence}}{\text{Effort}}$$

| STT | Mã | Tính năng / Tác vụ | Reach | Impact | Confidence | Effort (PM) | RICE Score | Ưu tiên |
| :---: | :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | **F-004** | **PDF Ingestion & Parsing** (Parse text theo trang/phân đoạn) | 1,000 | 2.0 | 90% | 1.0 | **1,800.0** | **#1** |
| 2 | **F-006** | **Structured AI Data Extraction** (Trích xuất dữ liệu tự động) | 1,000 | 3.0 | 85% | 1.5 | **1,700.0** | **#2** |
| 3 | **F-007** | **Evidence-linked Table** (Bảng đối chiếu evidence nguồn) | 1,000 | 3.0 | 80% | 2.0 | **1,200.0** | **#3** |
| 4 | **F-009** | **Conflict & Missing Detection** (Cảnh báo mâu thuẫn/thiếu số liệu) | 700 | 2.0 | 70% | 1.2 | **816.7** | **#4** |
| 5 | **F-012** | **Interactive Chat Assistant** (Chatbot RAG hỏi đáp từng paper) | 800 | 1.5 | 75% | 2.5 | **360.0** | **#5** |

---

## 2. Ma Trận 2x2 Value-Effort (Value-Effort Matrix)

Phân loại các tính năng dựa trên giá trị mang lại cho người dùng và nỗ lực phát triển kỹ thuật:

```
          HIGH VALUE
          ┌───────────────────────────────────┬───────────────────────────────────┐
          │                                   │                                   │
          │            QUICK WINS             │             BIG BETS              │
          │                                   │                                   │
          │  * F-004: PDF Ingestion & Parsing │  * F-006: Structured Extraction   │
          │  * F-011: Export CSV/Excel        │  * F-007: Evidence-linked Table   │
          │  * Default Template Setup         │  * F-002: Open Academic Search    │
          │                                   │                                   │
          │                                   │                                   │
          ├───────────────────────────────────┼───────────────────────────────────┤
          │                                   │                                   │
          │            FILL-INS               │          THANKLESS TASKS          │
          │                                   │                                   │
          │  * F-003: Project Folders & Notes │  * F-012: Multi-agent Chat (RAG)  │
          │  * Dashboard stats & analytics    │  * Custom OCR pipeline (PDF scan) │
          │                                   │                                   │
          │                                   │                                   │
          └───────────────────────────────────┴───────────────────────────────────┘
LOW EFFORT                                                                    HIGH EFFORT
                                      LOW VALUE
```

### Chi tiết phân loại:

1.  **Quick Wins (Giá trị cao, Công sức thấp - Triển khai ngay):**
    *   **PDF Ingestion & Parsing:** Tính năng bắt buộc phải có để hệ thống hoạt động. Sử dụng thư viện có sẵn (PyMuPDF, Grobid) giúp rút ngắn thời gian.
    *   **Export CSV/Excel:** Cực kỳ cần thiết cho workflow học thuật nhưng code rất đơn giản và ổn định.
    *   **Default Template Setup:** Cung cấp sẵn các trường phổ biến (Study Type, Sample Size) để người dùng chạy ngay không cần tự cấu hình.

2.  **Big Bets (Giá trị cao, Công sức cao - Cần lập kế hoạch và đầu tư nguồn lực):**
    *   **Structured AI Extraction:** Trái tim của sản phẩm. Phải thiết kế prompt phức tạp, xử lý format JSON, bảo vệ chống hallucination.
    *   **Evidence-linked Table:** Giao diện bôi vàng text tương tác với PDF viewer (tọa độ canvas) đòi hỏi thiết kế frontend công phu nhưng mang lại lòng tin (Trust) tuyệt đối cho người dùng.
    *   **Open Academic Search:** Tích hợp API Semantic Scholar và OpenAlex, deduplicate dữ liệu bằng DOI để nhập paper nhanh.

3.  **Fill-ins (Giá trị thấp, Công sức thấp - Làm khi rảnh):**
    *   **Folders & Notes:** Quản lý folder phân cấp và ghi chú cá nhân giúp quản trị tốt hơn nhưng không thuộc core workflow trích xuất.
    *   **Dashboard Stats:** Biểu đồ hiển thị tiến độ và thống kê cơ bản.

4.  **Thankless Tasks / Money Pit (Giá trị thấp, Công sức cao - Tránh hoặc tối ưu hóa):**
    *   **Multi-agent Chat Assistant (LangGraph):** Rất tốn kém token và tài nguyên, latency cao, khó debug. Nên tối ưu hóa thành single agent + RAG đơn giản để tiết kiệm chi phí trước khi làm multi-agent.
    *   **Custom OCR Pipeline:** Xử lý các paper dạng scan hình ảnh chất lượng thấp cần cài đặt máy chủ GPU OCR. Thay vào đó, hãy khuyến khích người dùng upload PDF digital-born ở phiên bản đầu tiên.
