Generate a complete desktop-first web application for a "Packing Video Proof App". This app helps E-commerce sellers record packing videos via Webcam (triggered by scanning QR codes) to prevent false refund claims.

**DESIGN SYSTEM (Luminous Bento - STRICTLY FOLLOW THIS STYLE):**
- **Theme:** Minimalist, flat, surgical, weightless. Absolutely NO drop-shadows.
- **Backgrounds:** Global app background is Surgical Canvas (#F9FAFB). All card/container surfaces are Absolute White (#FFFFFF).
- **Separation:** Use Hairline Delineator (#E5E7EB) 1px solid borders on all cards to create a crisp Bento layout.
- **Colors:** Primary Accent is Fluid Sapphire (Gradient from #1D4ED8 to #3B82F6) for CTAs. Text is Deep Slate (#0F172A) for headings, Cloud Gray (#64748B) for secondary labels.
- **Geometry:** Buttons and inputs must be strictly pill-shaped (rounded-full). Cards must have smoothly rounded corners (24px).
- **Spacing:** Use an asymmetric Bento Grid. Minimum 24px internal padding for cards and 24px gutters between layout blocks.

**APPLICATION STRUCTURE & VIEWS:**
Create a persistent left Sidebar Navigation (Tổng quan, Phòng quay video, Đơn hàng, Khiếu nại, Đội ngũ, Danh mục, Cài đặt) that dynamically loads the following 7 app views, plus 1 external Marketing Landing Page:

1. **Dashboard (Tổng quan):** Top row with 3 Bento cards: (1) Total Orders, (2) Cloud Storage progress bar, (3) Today's metrics. Below: A large chart card for "Weekly Volume" and a side card for "Top Performers" ranking.
2. **Recording Studio (Phòng quay video):** A massive central card displaying a webcam placeholder frame with a QR target overlay and a dynamic status badge ("Waiting for QR..." vs "Recording Order #12345"). Right-side panel showing "Current Order Details" and a "Recent History" list.
3. **Order Archive (Đơn hàng):** A top header with a pill-shaped search bar and filter chips (Shopee, TikTok, Lazada). Below it, a full-width data table listing Order ID, Date, Platform, and a 'Play Video Proof' action button.
4. **Dispute Center (Trung tâm Khiếu nại - Tính năng MỚI để tối đa hóa doanh thu):** Bảng Kanban theo dõi các yêu cầu hoàn tiền gian lận. Các cột: "Cần xử lý", "Đang chờ sàn", "Thắng kiện (Đã thu hồi tiền)". Mỗi thẻ hiển thị số tiền khiếu nại, mã khách hàng, và nút CTA: "Tạo Link Bằng Chứng" (Sử dụng động từ mạnh thúc đẩy hành động).
5. **Team Roster (Đội ngũ):** A grid of employee profile cards. Each card contains a perfect-circle avatar, name, and two metrics (Total Packed, Avg Time).
6. **Product Catalog (Danh mục):** A masonry or standard grid of product reference images with SKUs underneath to help packers identify items.
7. **Settings (Cài đặt):** A split layout showing Hardware configuration (Webcam source dropdown, Video resolution) and Billing details (Storage plan progress bar, Upgrade CTA).

**EXTERNAL MARKETING PAGE (Chiến lược Copywriting tối đa chuyển đổi):**
8. **Landing Page (Trang Bán hàng):** Trang nội dung công khai (Public Site) được thiết kế chuyên biệt để bán phần mềm, ứng dụng copy rõ ràng, mạnh mẽ:
   - **Hero Section:** 
     - *Headline (Nêu bật nỗi đau lớn nhất):* "Chấm dứt nạn hoàn hàng gian lận trên Shopee & TikTok."
     - *Subheadline (Cung cấp giải pháp cụ thể):* "Hệ thống tự động quay và lưu trữ video đóng gói. Giành chiến thắng 100% trong các vụ khiếu nại với bằng chứng video không thể chối cãi."
   - **Primary CTA:** "Bảo vệ Doanh thu ngay (Dùng thử Miễn phí)" - *Tập trung vào giá trị khách hàng nhận được thay vì chữ "Đăng ký" thông thường.*
   - **Social Proof Section (Xây dựng lòng tin):** "Đang bảo vệ hơn 50.000+ đơn hàng an toàn mỗi ngày cho các Top Seller."
   - **How it Works (Đơn giản hóa rào cản thao tác):** (1) Quét Mã QR đơn, (2) Tự động ghi hình chuẩn, (3) Trích xuất link bằng chứng chỉ với 1 click.

Please generate the foundational React components, routing shell, and Tailwind UI for these screens using the requested design system.
