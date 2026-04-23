# Stitch Prompts — Ứng Dụng Quay Video Đóng Hàng
> Ứng dụng quay video đóng hàng cho chủ cửa hàng thương mại điện tử
> Design system: xem `design1.md`
> **Ngôn ngữ giao diện: Tiếng Việt toàn bộ** — mọi nhãn, nút, placeholder, thông báo, tiêu đề đều dùng tiếng Việt

---

## Screen 1 — Dashboard (Trang Tổng Quan)

Trang tổng quan dạng dashboard cho chủ cửa hàng theo dõi hoạt động quay video đóng hàng trong tháng — yên tĩnh, đáng tin cậy, giàu thông tin nhưng không rối mắt. **Toàn bộ văn bản, nhãn, nút bấm dùng tiếng Việt.**

**Cấu Trúc Trang:**
1. **Left Sidebar Navigation (~220px fixed):**
   - App logo at top — pill-shaped icon mark in Midnight Sapphire on Pure Chalk softly embossed card
   - Navigation items: Dashboard (active), Quay Đóng Hàng, Đơn Hàng, Quản Lý Nhân Viên, Sản Phẩm, Cài Đặt
   - Active item filled with Midnight Sapphire pill, white SemiBold label; inactive items in Slate Ink with Glacial Mist hover tint
   - User avatar + name at bottom of sidebar
2. **Top Header Bar:**
   - Page title "Tổng Quan" in Bold Slate Ink
   - Month selector dropdown (tháng hiện tại) — pressed-inward inset style
   - Notification bell icon + user avatar — softly embossed pill buttons
3. **Stats Row — 4 Metric Cards (half-width grid, 2×2):**
   - **Card 1 — Tổng Đơn Trong Tháng:** Large Bold number (e.g., 1,248), subtitle "đơn hàng đã quay", small Cobalt Pulse upward trend arrow with percentage change vs last month
   - **Card 2 — Dung Lượng Còn Lại:** Circular arc progress tracker in Cobalt Pulse showing used vs total storage (e.g., "48.2 GB / 100 GB"), percentage in Bold center
   - **Card 3 — Nhân Viên Tích Cực Nhất:** Featured Dark Card in Midnight Sapphire — top employee avatar, name in white Bold, number of orders packed in white, gold star badge
   - **Card 4 — Đơn Hôm Nay:** Real-time counter with large Bold number, subtitle "đơn trong ngày", small green pulse dot signaling live data
4. **Biểu Đồ Đơn Theo Ngày Trong Tuần (full-width card):**
   - Horizontal bar chart or column chart — 7 bars for T2 → CN
   - Bars filled with Cobalt Pulse, rounded end-caps; background track in Glacial Mist inset channel
   - Y-axis labels in Cloud Detail, X-axis day labels in Steel Shadow SemiBold
   - Card title "Đơn Hàng Theo Ngày" in Bold Slate Ink top-left
5. **Danh Sách Nhân Viên Tích Cực Tháng (full-width card, bottom):**
   - Ranked list: rank number, avatar, name, order count, progress bar (relative to #1)
   - Top 3 ranks shown with subtle gold/silver/bronze tinted chips
   - "Xem tất cả →" ghost pill button bottom-right

**Mood:** Trung tâm chỉ huy yên tĩnh. Mỗi con số đều có không gian thở. Dark card neo giữ mắt người dùng ngay lập tức.

---

## Screen 2 — Quay Đóng Hàng (Recording Screen)

Màn hình tác nghiệp tập trung vào webcam trực tiếp. QR code tự động kích hoạt bắt đầu/dừng quay. Phản hồi trạng thái phải tức thì và rõ ràng — nhân viên luôn biết mình đang ở trạng thái nào. **Toàn bộ văn bản dùng tiếng Việt.**

**Cấu Trúc Trang:**
1. **Left Sidebar Navigation:** Same as Dashboard. "Quay Đóng Hàng" item active.
2. **Main Content Area — split into two columns:**

   **Left Column — Live Camera Feed (dominant, ~65% width):**
   - Large softly embossed Pure Chalk card containing the webcam viewport
   - Camera feed fills a 16:9 rounded rectangle (`border-radius: 20px`) inside the card
   - **Recording Active State:** Glowing Cobalt Pulse border ring around camera feed (`box-shadow: 0 0 0 3px #2563EB, 0 0 20px rgba(37,99,235,0.3)`), pulsing subtly
   - **Recording Idle State:** Camera feed with a neutral muted border, "Chờ quét QR bắt đầu..." status label in Cloud Detail below
   - **QR Scan Indicator:** When QR detected — a brief flash overlay on camera feed (semi-transparent Cobalt Pulse wash, 200ms), then auto-recording starts
   - **Order ID Display:** Large Bold Slate Ink text showing current scanned order code (e.g., `#ORD-20240421-0047`) directly below camera feed inside the card
   - **Recording Timer:** Digital clock format (00:02:34) in Bold DM Sans, Cobalt Pulse color, bottom of camera card
   - **Stop Indicator:** "Quét QR stop để dừng" hint text in Cloud Detail Ghost, subtle

   **Right Column — Order Activity Feed (~35% width):**
   - Section title "Phiên Làm Việc Hôm Nay" in Bold Slate Ink
   - **Đang Quay Card:** Featured Dark Card (Midnight Sapphire) — current order being recorded. Order ID in white Bold, employee name in white Regular, elapsed time in Cobalt Pulse, pulsing red dot "ĐANG QUAY" status chip
   - **Danh Sách Đã Quay:** Vertical list of completed orders — each row is a softly embossed Pure Chalk mini-card: order ID, timestamp, duration, green "Hoàn Thành" chip. Scrollable list.
   - **Session Summary (bottom):** Small card — "Tổng hôm nay: 24 đơn" in Bold, "Thời gian hoạt động: 3h 12m" in Regular

3. **Bottom Status Bar (optional, full width below content):**
   - Camera device name, resolution indicator, storage remaining indicator (Cobalt Pulse mini-bar)

**Mood:** Tập trung, rõ ràng trong vận hành. Camera chiếm ưu thế. Trạng thái luôn hiển thị tường minh. Không trang trí thừa.

---

## Screen 3 — Đơn Hàng (Orders Management)

Danh sách tất cả đơn hàng đã quay, có thể tìm kiếm và lọc, kèm thumbnail video, chip trạng thái và nút thao tác nhanh. **Toàn bộ văn bản dùng tiếng Việt.**

**Cấu Trúc Trang:**
1. **Left Sidebar Navigation:** "Đơn Hàng" active.
2. **Page Header:**
   - Title "Đơn Hàng" in Bold Slate Ink
   - Stats inline: "Tổng: 1,248 đơn" · "Tháng này: 312" · "Hôm nay: 24" — in Steel Shadow Regular
3. **Filter & Search Bar (full-width card, pressed-inward style):**
   - Search input (pressed-in inset shadow) with magnifying glass icon — placeholder "Tìm theo mã đơn, nhân viên..." in Whisper Gray
   - Filter pills: Tất cả · Hôm nay · Tuần này · Tháng này — pill-shaped, active pill in Midnight Sapphire fill
   - Status filter dropdown: Hoàn thành / Đang quay / Lỗi
   - Date range picker (two inset-style inputs, calendar icon)
4. **Orders Table / Card Grid (main content area):**
   - Each order row is a softly embossed Pure Chalk card with subtle lift on hover
   - **Columns per row:**
     - Video thumbnail (blurred preview, 80×45px, rounded `12px`) with play icon overlay on hover
     - Mã đơn hàng (Bold, Slate Ink) + tên sàn TMĐT (Shopee / TikTok Shop / Lazada — small colored chip)
     - Nhân viên (avatar + name)
     - Thời lượng video (duration, Cloud Detail)
     - Thời gian quay (timestamp, Cloud Detail)
     - Trạng thái chip: "Hoàn Thành" (pale green tint + deep green text) · "Đang Quay" (pale blue tint + Cobalt Pulse text, pulsing dot) · "Lỗi" (pale red tint + red text)
     - Action icons: Play (watch video), Download, Delete — softly embossed icon buttons
5. **Pagination (bottom):**
   - Pill-shaped page number buttons; active page in Midnight Sapphire fill
   - "← Trước" / "Tiếp →" ghost pill buttons

**Mood:** Bảng dữ liệu sạch sẽ. Hàng có không gian thở. Thumbnail giúp quét nhìn đơn hàng nhanh chóng.

---

## Screen 4 — Quản Lý Nhân Viên (Employee Management)

Màn hình hai cột: danh sách nhân viên có thể tìm kiếm bên trái, panel hồ sơ chi tiết bên phải hiện ra khi click vào từng nhân viên. **Toàn bộ văn bản dùng tiếng Việt.**

**Cấu Trúc Trang:**
1. **Left Sidebar Navigation:** "Quản Lý Nhân Viên" active.
2. **Page Header:**
   - Title "Quản Lý Nhân Viên" in Bold Slate Ink
   - "Thêm Nhân Viên +" primary pill button (Midnight Sapphire fill) top-right
3. **Main Content — Two-Column Layout:**

   **Left Panel — Employee List (~40% width):**
   - Search bar (inset shadow input) — "Tìm nhân viên..." placeholder
   - Filter chips: Tất cả · Đang làm · Nghỉ phép · Ngừng hoạt động
   - Scrollable list of employee cards — each a softly embossed Pure Chalk card:
     - Avatar (circular, 48px) + full name (Bold Slate Ink) + role label (Cloud Detail)
     - Order count this month (Cobalt Pulse small badge)
     - Last active timestamp (Whisper Gray)
     - Active status dot (green) or idle dot (Whisper Gray)
   - Selected employee card shifts to pressed-inward inset shadow to show selection

   **Right Panel — Employee Detail (~60% width, featured card):**
   - Large avatar (80px circular) + name (Bold 700, large) + role + status chip
   - **Thống Kê Cá Nhân (2-column mini stat grid):**
     - Đơn trong tháng (large Bold number + Cobalt Pulse small trend)
     - Tổng đơn đã quay (lifetime)
     - Thời gian làm việc tháng này
     - Hạng trong tháng (#2 với gold chip)
   - **Biểu Đồ Hoạt Động (7 ngày gần nhất):** Small column chart, Cobalt Pulse bars
   - **Lịch Sử Đơn Hàng (scrollable mini list):** last 10 orders — mã đơn, thời gian, duration, status chip
   - **Action Buttons (bottom):** "Chỉnh Sửa" (ghost pill) · "Vô Hiệu Hóa" (danger ghost pill, pale red tint)

**Mood:** Bảng quản lý nhân sự. Danh sách trái cho phép quét nhanh. Panel phải thưởng người dùng bằng thông tin chi tiết khi click.

---

## Screen 5 — Sản Phẩm Bán Hàng (Products)

Trang gallery sản phẩm trực quan để chủ cửa hàng quản lý hình ảnh sản phẩm — lưới ảnh gọn sạch với thêm/sửa/xóa. Chủ cửa hàng tự tải ảnh lên. **Toàn bộ văn bản dùng tiếng Việt.**

**Cấu Trúc Trang:**
1. **Left Sidebar Navigation:** "Sản Phẩm" active.
2. **Page Header:**
   - Title "Sản Phẩm Bán Hàng" in Bold Slate Ink
   - Subtitle "Quản lý hình ảnh sản phẩm của cửa hàng" in Cloud Detail Regular
   - "Thêm Sản Phẩm +" primary pill button (Midnight Sapphire fill) top-right
3. **Search & Filter Bar:**
   - Search input (inset shadow) — "Tìm theo tên sản phẩm..."
   - View toggle: Grid view / List view (softly embossed icon toggle pills, active in Midnight Sapphire)
   - Sort dropdown (inset style): Mới nhất · Tên A–Z · Giá tăng dần
4. **Product Grid (main content — responsive 4-column grid):**
   - Each product is a softly embossed Pure Chalk card with `border-radius: 20px`
   - **Product image:** square format filling card top, `border-radius: 16px 16px 0 0` if flush, or padded square inset
   - **Product info below image:** Product name (SemiBold Slate Ink) · Price (Bold Cobalt Pulse) · Category chip (pale tint pill)
   - **Hover state:** card lifts subtly (`scale(1.015)`) + three action icons appear with gentle fade-in: Chỉnh Sửa (pencil), Xem (eye), Xóa (trash)
   - Empty state (no products yet): centered illustration placeholder + "Chưa có sản phẩm" in Cloud Detail + "Thêm sản phẩm đầu tiên" Midnight Sapphire pill button
5. **Add/Edit Product Modal (overlay):**
   - Modal is an elevated Pure Chalk card (`border-radius: 28px`) with increased shadow multiplier
   - Fields: Product name input, Price input, Category dropdown, Image upload dropzone (dashed inset-shadow border, "Kéo thả ảnh hoặc nhấn để tải lên" in Whisper Gray)
   - CTA: "Lưu Sản Phẩm" (Midnight Sapphire pill) · "Hủy" (ghost pill)

**Mood:** Gallery ảnh sạch sẽ. Hình ảnh sản phẩm tự lên tiếng. UI hỗ trợ âm thầm phía sau.

---

## Screen 6 — Cài Đặt Tài Khoản (Account & Subscription Settings)

Trang cài đặt kết hợp quản lý hồ sơ tài khoản và chọn gói dịch vụ — chuyên nghiệp, bảng giá rõ ràng, dễ tự nâng cấp. **Toàn bộ văn bản dùng tiếng Việt.**

**Cấu Trúc Trang:**
1. **Left Sidebar Navigation:** "Cài Đặt" active.
2. **Page Header:**
   - Title "Cài Đặt Tài Khoản" in Bold Slate Ink
3. **Settings Layout — Two-Column (Left nav tabs + Right content panel):**

   **Left Tab Menu (~240px):**
   - Vertical pill-style tab list: Thông Tin Tài Khoản · Gói Dịch Vụ · Bảo Mật · Thông Báo
   - Active tab: Midnight Sapphire pill fill. Inactive: Slate Ink text, Glacial Mist hover.

   **Right Content Panel (fluid):**

   **Tab: Thông Tin Tài Khoản**
   - Avatar upload area (circular, 96px, softly embossed ring, camera icon overlay on hover)
   - Form fields in inset-shadow style: Tên cửa hàng, Email, Số điện thoại, Địa chỉ
   - "Lưu Thay Đổi" primary pill button (Midnight Sapphire)

   **Tab: Gói Dịch Vụ (highlight this as the featured settings tab)**
   - Current plan banner: Featured Dark Card (Midnight Sapphire) showing plan name, storage used (Cobalt Pulse arc), expiry date, "Đang dùng" white chip
   - **Pricing Cards Grid (3 columns):**
     - **Cơ Bản:** softly embossed Pure Chalk card — storage amount, order limit/month, price/month in Bold Slate Ink, feature list with checkmark chips, "Chọn Gói" ghost pill button
     - **Chuyên Nghiệp (highlighted / recommended):** Featured Dark Card (Midnight Sapphire) — "Phổ Biến Nhất" Cobalt Pulse chip at top, same info in white, "Nâng Cấp Ngay" white pill button
     - **Doanh Nghiệp:** softly embossed Pure Chalk card — same structure, custom pricing "Liên Hệ", "Tư Vấn" ghost pill button
   - Payment history table below: Date, Plan, Amount, Status chip (Thành Công green / Thất Bại red), Download receipt icon

   **Tab: Bảo Mật**
   - Change password form — 3 inset-shadow inputs: Mật khẩu hiện tại, Mật khẩu mới, Xác nhận mật khẩu
   - Two-factor authentication toggle (pill-shaped toggle switch, active state Cobalt Pulse fill)
   - Active sessions list with device info + "Đăng Xuất Thiết Bị Này" danger ghost button

**Mood:** Truyền sự tin tưởng và bình tĩnh. Phần gói dịch vụ là tâm điểm — dark card kéo mắt về gói được đề xuất.

---

## Ghi Chú Chung (Áp Dụng Cho Toàn Bộ App)

- **Ngôn ngữ:** Toàn bộ giao diện dùng **tiếng Việt** — nhãn nav, nút bấm, placeholder, thông báo lỗi, tiêu đề, chip trạng thái
- **Design system:** Tuân theo `design1.md` — Neumorphism Soft UI, màu sắc, typography, shadow patterns
- **Không dùng border** để phân chia khu vực — dùng whitespace + shadow + background contrast
- **Neumorphic press animation:** khi nhấn bất kỳ button/card nào, shadow chuyển từ outward sang inset trong 130ms
- **Card entrance:** fade + slideUp 8px, staggered 60ms per card
- **Corner consistency:** card `24px`, badge/chip `50px` pill, input `16px`, không có góc nhọn bất cứ đâu
- **Font pairing:** `DM Sans` cho heading, `Nunito` cho body — gọi từ Google Fonts
