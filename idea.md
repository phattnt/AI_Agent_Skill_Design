# Product Copy & App Structure: Ứng dụng Quay Video Đóng Hàng

## I. MỤC TIÊU & ĐỊNH VỊ (MARKETING CONTEXT)
- **Sản phẩm:** Phần mềm quay video bằng chứng đóng gói hàng hóa tự động.
- **Khách hàng Mục tiêu:** Các chủ shop bán hàng trên sàn Thương mại điện tử (Shopee, TikTok, Lazada).
- **Vấn đề giải quyết:** Nạn khách hàng khiếu nại "thiếu hàng", "nhầm hàng", bị hoàn tiền oan khiến chủ shop mất doanh thu. Việc bấm quay video thủ công bằng điện thoại quá mất thời gian và khó quản lý.
- **Giải pháp (Transformation):** Tự động hóa quá trình quay video qua Webcam tích hợp quét mã QR, tạo kho bằng chứng kháng nghị vô đối mà không làm chậm tốc độ đóng gói.

---

## II. COPYWRITING - LANDING PAGE (DÀNH CHO TRANG CHỦ)

### Above the Fold (Khu vực thu hút)
- **Headline (Tiêu đề chính):** Bằng Chứng Đóng Hàng Thép. Quét Mã Là Quay – Không Cần Chạm Tay.
- **Subheadline (Tiêu đề phụ):** Xóa sổ 100% rủi ro bị "hoàn tiền oan" từ các sàn TMĐT. Ứng dụng tự động kích hoạt Webcam qua mã vận đơn, giúp nhân viên đóng gói nhanh gấp đôi và bảo vệ doanh thu của bạn tuyệt đối.
- **Primary CTA:** Tạo Tài Khoản & Bắt Đầu Quay (Miễn phí)

### Core Benefits (Lợi Ích Thay Vì Tính Năng)
1. **Tự Động Hóa Quá Trình Quay:** Không cần bấm phím, không cần cầm điện thoại. Đưa mã vận đơn vào quét -> Tự động quay. Quét thẻ "Stop" -> Tự cắt video và sẵn sàng cho đơn tiếp theo. Quy trình đóng gói không bị gián đoạn dù chỉ 1 giây.
2. **Kháng Nghị Luôn Thắng lợi:** Truy xuất video đóng hàng cực nhanh bằng Mã Vận Đơn. Khi khách khiếu nại, bạn có ngay video sắc nét làm bằng chứng để gửi lên sàn.
3. **Kiểm Soát Tối Đa Qua Bảng Điều Khiển:** Theo dõi trực tiếp tiến độ đóng hàng trong ngày, đánh giá năng suất từng nhân viên ngay trên một màn hình duy nhất.

---

## III. CẤU TRÚC ỨNG DỤNG & UI COPYWRITING (6 MÀN HÌNH)

Dưới đây là đặc tả nội dung và ý tưởng hiển thị cho 6 màn hình lõi của ứng dụng (Dashboard):

### 1. Screen: Dashboard (Bảng Điều Khiển Trung Tâm)
*Là "đài quan sát" để chủ shop nắm bắt tình hình vận hành kho trong một ánh nhìn.*
- **Thông số cốt lõi (Hero Metrics):**
  - **Tổng đơn đã quay (Tháng này):** [XXXX] Đơn hàng được bảo vệ.
  - **Dung lượng lưu trữ (Storage):** Thanh tiến trình (Progress Bar) hiển thị dung lượng Cloud còn lại. *Nút CTA đi kèm: "Nâng cấp dung lượng".*
- **Hiệu suất nhân viên:** Bảng vinh danh/xếp hạng các nhân viên kho có số lượng đơn đóng gói nhiều nhất trong tháng.
- **Biểu đồ vận hành:** Đồ thị trực quan thể hiện số lượng đơn hàng đóng gói được mỗi ngày trong tuần qua.

### 2. Screen: Quay Đóng Hàng (Recording Studio)
*Màn hình công việc trực tiếp dành cho nhân viên kho.*
- **Camera View:** Luồng hiển thị trực tiếp từ Webcam với khung quét QR (QR Scanner target) ở trung tâm.
- **Trạng thái Thông minh:** Thông báo to, rõ ràng: *"Đang chờ mã đơn..."* -> *"Đang ghi hình đơn #10293"* -> *"Đã lưu video thành công!"*
- **Feed Công Việc (Real-time List):** Cột danh sách hiển thị các đơn đang được quay và lịch sử các đơn vừa hoàn thành xong trong ca làm việc, giúp nhân viên đối chiếu chéo.

### 3. Screen: Đơn Hàng (Order/Video Archive)
*Kho lưu trữ bằng chứng - nơi cứu rỗi doanh thu.*
- Bảng danh sách toàn bộ các đơn hàng đã đóng gói, đi kèm thẻ Video tương ứng.
- Tính năng **Tìm kiếm siêu tốc (Fast Search)** bằng Mã vận đơn hoặc Tên khách hàng để trích xuất ngay file MP4 đem đi kháng nghị.

### 4. Screen: Quản Lý Nhân Viên (Team Roster)
*Quản trị con người để tối ưu chi phí vận hành.*
- Danh sách liệt kê toàn bộ nhân viên kho.
- **Hồ sơ chi tiết (Detail View):** Khi click vào một nhân viên, hiển thị chi tiết số đơn người đó đã đóng, tốc độ quay trung bình, và lịch sử ca làm việc.

### 5. Screen: Sản Phẩm Bán Hàng (Product Catalog)
*Công cụ hỗ trợ chống đóng nhầm hàng.*
- Hiển thị lưới hình ảnh trực quan của các sản phẩm thuộc cửa hàng (Do cửa hàng tự upload/đồng bộ).
- Nhân viên đóng gói có thể xem hình ảnh hàng hóa ở góc phụ của màn hình quay video, giúp họ đối chiếu ngoại quan, tránh tình trạng lấy nhầm màu, nhầm size.

### 6. Screen: Cài Đặt Tài Khoản (Settings & Billing)
*Khu vực tùy chỉnh và nâng cấp ứng dụng.*
- Quản lý gói dịch vụ (Billing & Plans): Nơi chủ shop mua các gói nâng cấp, mở rộng dung lượng lưu trữ Cloud theo tháng/năm.
- Cài đặt cấu hình thiết bị (chọn Webcam, chọn độ nét Video) và thông tin cửa hàng cơ bản.
