# 📝 Market Positioning Memo — SCIDEX Project

Tài liệu này thực hiện **Bước 3** của Day 26 Lab: Soạn thảo bản Memo định vị thị trường và chứng minh khả năng gọi vốn (fundability) của dự án **SCIDEX** trong bối cảnh thị trường đầu tư mạo hiểm hiện nay.

---

## 🌐 1. Đánh Giá Tính Khả Thi Gọi Vốn (Fundability) Trong Bối Cảnh Hiện Tại

### A. Thách thức từ sự suy giảm của dòng vốn VC
Bối cảnh gọi vốn tại Việt Nam và Đông Nam Á đang trải qua giai đoạn sàng lọc khắt khe (theo số liệu từ slide 8 - 9):
*   **Dòng vốn VC suy giảm mạnh**: Giá trị giải ngân và số lượng thương vụ tại Việt Nam giảm liên tục (~30% vào cuối năm 2025 so với đỉnh điểm 2021).
*   **Ticket size thu nhỏ**: Các deal lớn trên $20M co cụm lại, nhường chỗ cho các deal quy mô nhỏ từ $0-1M (chiếm 31% số deal năm 2025) và $1-5M (chiếm 41% số deal năm 2025). Điều này cho thấy các nhà đầu tư đang thận trọng hơn, ưu tiên các vòng đầu tư nhỏ để kiểm chứng chất lượng trước khi rót vốn lớn.
*   **Lỗi thường gặp**: Nhiều startup bị từ chối do rơi vào bẫy *"Unclear Financials"* (Tài chính mơ hồ, không có dự toán kinh tế đơn vị rõ ràng) và *"Unclear Differentiation"* (Quá phụ thuộc vào mác AI mà không có moat thực tế).

### B. Cơ hội từ làn sóng AI Agent và xu hướng mới
Mặc dù thị trường chung ảm đạm, mảng công nghệ chuyên sâu vẫn nhận được sự quan tâm lớn:
*   **Dòng vốn chảy vào AI Agent bùng nổ**: Lũy kế đến năm 2024, đầu tư vào các công cụ tác tử AI (AI Agent) đạt **162 deal với giá trị lên tới 3.8 tỷ USD** (Slide 12).
*   **Định hướng mới từ Y Combinator (Summer 2026)**: Xu hướng dịch chuyển mạnh mẽ sang **AI-Native Service Companies** (các công ty bán dịch vụ trọn gói vận hành bằng AI thay vì chỉ bán phần mềm) và **Software for Agents** / **SaaS Challengers** (phần mềm thay thế các hệ thống SaaS truyền thống cồng kềnh) (Slide 14).
*   **Sự dịch chuyển dòng vốn**: Xu hướng rút khỏi các mô hình tiêu dùng khu vực (regional consumer) để chuyển sang doanh nghiệp công nghệ toàn cầu (global enterprise) như Airalo ($220M) hay Supabase ($200M) (Slide 11).

### 💡 Kết luận về Fundability của SCIDEX:
Dự án **SCIDEX** giải quyết bài toán trích xuất và kiểm duyệt dữ liệu bài báo khoa học. Ý tưởng này **hoàn toàn có khả năng gọi vốn (fundable)** vì:
1.  Nó thuộc nhóm **SaaS Challengers** và **Software for Agents** (tự động hóa quy trình nghiệp vụ nghiên cứu phức tạp).
2.  Nó giải quyết trực tiếp bài toán niềm tin dữ liệu (chống hallucination bằng Evidence-linked table), rất khớp với khẩu vị đầu tư thực tế hiện nay (thiên về tính chuẩn xác và thực chất hơn là quảng cáo cường điệu).
3.  Tuy nhiên, để gọi vốn thành công, SCIDEX phải chứng minh được lộ trình mở rộng từ tệp người dùng học thuật (biên lợi nhuận thấp) sang tệp doanh nghiệp R&D (dược phẩm, tư vấn, pháp lý) có khả năng chi trả cao.

---

## 📊 2. Giải Quyết Lỗi "Unclear Financials" (Tài Chính Sơ Bộ Của SCIDEX)

Để thuyết phục các nhà đầu tư ở vòng Seed, dưới đây là mô hình tài chính đơn giản của SCIDEX dựa trên các ước tính thực tế:

### A. Kinh tế đơn vị sơ bộ (Unit Economics)
Chúng tôi giả định mô hình doanh thu đăng ký định kỳ (B2B SaaS Subscription) với mức ARPU (Doanh thu trung bình trên mỗi người dùng) pha trộn giữa tệp Học thuật (Academic) và Doanh nghiệp (Enterprise R&D):
*   **Doanh thu trên 1 khách hàng (ARPU)**: **30 USD / tháng**
*   **Chi phí phục vụ 1 khách hàng (Cost to Serve)**: **6 USD / tháng**
    *   *Chi phí API LLM (GPT-4o-mini & Claude 3.5 Sonnet)*: Ước tính một người dùng active trung bình xử lý 20 tài liệu nghiên cứu/tháng (~150,000 input tokens và ~30,000 output tokens mỗi tài liệu). Chi phí API trung bình là **4.40 USD / tháng**.
    *   *Chi phí hạ tầng và Cloud storage (Cloudflare R2, Supabase database, Grobid parser server)*: **1.60 USD / tháng**.
*   **Biên lợi nhuận đóng góp (Contribution Margin)**:
    $$\text{Contribution Margin} = 30 \text{ USD} - 6 \text{ USD} = 24 \text{ USD / người dùng / tháng}$$
    *(Tương đương biên lợi nhuận gộp đạt **80%**, một chỉ số rất tốt cho các mô hình phần mềm SaaS).*

### B. Nhu cầu vốn & Lộ trình sử dụng vốn (Cash Needs & Runway)
SCIDEX đặt mục tiêu gọi vốn vòng **Pre-Seed / Seed** trị giá **180,000 USD** (phù hợp với quy mô đầu tư của Antler hoặc 500 Global Vietnam).
*   **Lộ trình chi tiêu hàng tháng (Burn Rate)**: **6,500 USD / tháng**
    *   *Nhân sự*: 4,000 USD (Hỗ trợ sinh hoạt phí cho 1 founder và thuê 2 kỹ sư backend/AI part-time).
    *   *Hạ tầng, API & Công cụ*: 1,500 USD.
    *   *Marketing & Phát triển thị trường*: 1,000 USD.
*   **Thời gian sống sót (Runway)**:
    $$\text{Runway} = \frac{180,000 \text{ USD}}{6,500 \text{ USD/tháng}} \approx 27.6 \text{ tháng}$$
    *(Hơn 27 tháng runway là khoảng thời gian rất an toàn để hoàn thiện Core MVP và đạt được các chỉ số Traction quan trọng).*

### C. Chỉ số đo lường chính cho vòng tiếp theo (KPIs to Next Round)
Trước khi tiến hành gọi vốn vòng tiếp theo (Series Seed chính thức), SCIDEX cam kết đạt được các cột mốc:
1.  **Quy mô người dùng (Traction)**: Đạt tối thiểu **1,500 Monthly Active Users (MAU)** trong giới nghiên cứu học thuật và có ít nhất **50 tài khoản doanh nghiệp dùng thử (Pilot Corporate Teams)** từ các viện nghiên cứu dược phẩm hoặc công ty tư vấn.
2.  **Chất lượng sản phẩm (Product Quality)**: Đạt tỷ lệ **Verified Rate > 85%** (dữ liệu được con người xác nhận chính xác trước khi xuất file) và tỷ lệ **Evidence Linkage = 100%** (không có trường dữ liệu nào bị hallucinate không nguồn dẫn).
3.  **Tài chính**: Đạt mốc **2,500 USD MRR** (Doanh thu định kỳ hàng tháng) để chứng minh khách hàng thực sự sẵn sàng chi trả cho giải pháp.
