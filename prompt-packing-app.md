# Cấu trúc Prompt Tối Ưu cho Stitch (Ứng dụng Quay Camera Đóng Hàng)

Tài liệu này chứa các Prompts đã được tinh chỉnh theo chuẩn `@enhance-prompt`. Mọi prompt đều được tích hợp chặt chẽ với Design System `Luminous Bento` để đảm bảo Stitch (hoặc bất kỳ AI sinh code UI nào) cho ra kết quả đồng bộ, cao cấp và không bị "rẻ tiền".

---

## 🛠 GLOBAL DESIGN SYSTEM (BẮT BUỘC)
*⚠️ Copy và dán đoạn Text này vào ĐẦU MỌI PROMPT để đảm bảo AI sinh ra UI đúng chuẩn Luminous Bento.*

```text
**DESIGN SYSTEM (REQUIRED):**
- Platform: Web, Desktop-first (Dashboard cho màn hình máy tính tại kho)
- Theme: Light, Luminous Bento (premium, surgical, weightless)
- Background: Surgical Canvas (#F9FAFB)
- Surface: Absolute White (#FFFFFF) for all cards (STRICTLY NO DROP-SHADOWS)
- Borders: Hairline Delineator (#E5E7EB) 1px solid for all cards/containers
- Primary Accent: Fluid Sapphire (Gradient from #1D4ED8 to #3B82F6) for CTAs & progress 
- Text Primary: Deep Slate Anchor (#0F172A) for metrics and headings
- Text Secondary: Cloud Detail (#64748B) for labels
- Typography: Plus Jakarta Sans (Headings), Inter (Body)
- Buttons: Strictly pill-shaped (rounded-full), flat profile, gradient fill
- Cards/Containers: Smoothly rounded corners (24px), 24px internal padding minimum
- Layout: Asymmetric Bento Box layout with strict 24px gutters.
```

---

## 🖥 CÁC PROMPT CHỨC NĂNG (TỪNG SCREEN CHI TIẾT)

### 1. Screen 1: Dashboard (Bảng Điều Khiển)
```text
A highly structured, analytics-focused dashboard for e-commerce shop owners to monitor packing operations.

[DÁN GLOBAL DESIGN SYSTEM VÀO ĐÂY]

**Page Structure:**
1. **Sidebar Navigation:** Left sidebar with logo, active "Dashboard" navigation pill, and links to (Recording, Orders, Team, Products, Settings).
2. **Top Header:** Welcome greeting, current date, and a primary CTA button "Start Recording".
3. **Hero Metrics (Top Bento Row):** 3 interlocking white cards showing:
   - Total Orders Recorded (large ExtraBold number).
   - Storage Remaining (Fluid Sapphire progress bar + "Upgrade" ghost button).
   - Today's Output (Number + positive trend indicator).
4. **Main Analytics (Split Bento):**
   - **Main Card (Left):** "Weekly Volume" bar chart showing orders packed per day.
   - **Side Card (Right):** "Top Performers" list showing 5 employee avatars, names, and packing count badges.
```

### 2. Screen 2: Recording Studio (Quay Đóng Hàng)
```text
A hyper-focused, distraction-free recording interface for warehouse staff.

[DÁN GLOBAL DESIGN SYSTEM VÀO ĐÂY]

**Page Structure:**
1. **Sidebar Navigation:** Standard left navigation panel with "Recording" active.
2. **Recording Canvas (Main Bento Box):** A massive central card displaying a webcam video feed. Include a subtle target overlay for QR scanning.
    - Large floating Status Badge at top: "Waiting for QR Code..." or "Recording Order #12345 (2:15s)".
3. **Activity Feed (Right Panel Bento Box):** A vertical card showing real-time packing history.
    - **Current:** Details of the active order being packed.
    - **History List:** Scrollable list of recent orders with green "Success" ghosted tags.
```

### 3. Screen 3: Order / Video Archive (Quản Lý Đơn Hàng)
```text
A pristine database screen to search and retrieve video proofs for e-commerce orders.

[DÁN GLOBAL DESIGN SYSTEM VÀO ĐÂY]

**Page Structure:**
1. **Sidebar Navigation:** Standard left navigation panel with "Orders" active.
2. **Header & Search:** Page title "Order Archive" with a large, pill-shaped search bar (Search by Tracking ID).
3. **Filter Bar:** Row of ghost pills to filter by (All, Shopee, TikTok, Lazada, Claimed).
4. **Data Table (Full-width Bento Card):**
   - Columns: Order ID, Date, Packed By, Platform, and Video Proof.
   - Video Proof column contains a small thumbnail and a "Play/Download" icon button.
   - Ensure the table has generous padding and borders separating rows, no zebra striping.
```

### 4. Screen 4: Team Roster (Quản Lý Nhân Viên)
```text
A clean personnel management screen to track warehouse employee performance.

[DÁN GLOBAL DESIGN SYSTEM VÀO ĐÂY]

**Page Structure:**
1. **Sidebar Navigation:** Standard left navigation panel with "Team" active.
2. **Header:** "Team Management" title with a "+ Add Employee" primary CTA button.
3. **Team Grid (Bento Layout):** Display employees as a grid of individual Bento cards.
   - Each card contains: Large perfect-circle Avatar, Name, Role, and two mini-stats (Total Orders Packed, Avg Time per Order).
   - Include an "Edit" icon in the top right of each card.
```

### 5. Screen 5: Product Catalog (Sản Phẩm Bán Hàng)
```text
A visual reference catalog to help packers identify the correct items visually.

[DÁN GLOBAL DESIGN SYSTEM VÀO ĐÂY]

**Page Structure:**
1. **Sidebar Navigation:** Standard left navigation panel with "Products" active.
2. **Header:** "Product Catalog" with a search bar and a "Upload New" button.
3. **Product Gallery (Grid Layout):** A clean masonry or uniform grid of product images.
   - Image cards have a crisp 1px border.
   - Below the image, show the SKU and Product Name in deep slate text.
```

### 6. Screen 6: Settings & Billing (Cài Đặt Tài Khoản)
```text
A structured settings page for hardware configuration and subscription management.

[DÁN GLOBAL DESIGN SYSTEM VÀO ĐÂY]

**Page Structure:**
1. **Sidebar Navigation:** Standard left navigation panel with "Settings" active.
2. **Settings Layout:** A two-column layout. A narrow left menu for settings categories (General, Hardware, Billing).
3. **Hardware Config (Bento Card):** 
   - Dropdown to select active Webcam.
   - Video resolution toggle.
4. **Billing & Plans (Bento Card):**
   - Current Plan detail (e.g., "Pro Plan - 500GB").
   - Large usage progress bar.
   - "Upgrade Plan" CTA button with Fluid Sapphire gradient.
```
