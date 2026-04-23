# Stitch Prompts — Packing Video Recording App
> **IMPORTANT: ALL GENERATED UI TEXT MUST BE IN VIETNAMESE.** This includes all labels, buttons, placeholders, empty states, dummy data, and titles.
> 
> **Design System Context:** Follow the Crextio Soft UI aesthetic (smooth shadows, large border radii, cool tones).

---

## DESIGN SYSTEM (REQUIRED — Apply to all screens)

- **Platform:** Web app, Desktop-first, highly spacious layout with generous whitespace.
- **Theme:** Clean, modern, light mode, Crextio Soft UI style.
- **Background:** Frosty Cloud (`#EBF1F6`) — very soft, desaturated cool blue background.
- **Surface / Cards:** Pure White (`#FFFFFF`) featuring ultra-smooth, whisper-soft diffused shadows (`box-shadow: 0 4px 20px rgba(0, 0, 0, 0.03)`). Generously round border radii (`24px`). Absolutely NO hard borders or sharp corners.
- **Accents:** 
  - **Primary Action (Vivid Ocean Blue `#1A73E8`):** Active progress elements, notifications, and primary CTA buttons.
  - **Secondary (Soft Glacier Blue `#D9E6F6`):** Progress tracks, inactive pills, and subtle backgrounds.
  - **Highlight/Anchor (Deep Midnight Navy `#142A56`):** Featured dark cards, active navigation tabs.
- **Text:** Slate Navy (`#1E293B`) for primary text and large data; Misty Slate (`#64748B`) for secondary text, metadata, and dates.
- **Typography:** `Plus Jakarta Sans` or `Outfit`. Bold (700) for large numbers, Semi-bold (600) for headers, Regular (400) for body text.
- **Shapes/Geometry:** Buttons, badges, and progress tracks MUST be heavily pill-shaped (`rounded-full`). Charts use capsule elements.

---

## Screen 1 — Dashboard (Bảng Điều Khiển)

A highly modern, airy, and clean dashboard giving the store owner a quick overview of packing video activities. Open layout with borderless cards.

**Page Structure:**
1. **Header (Top Nav):**
   - Left: Rounded app logo.
   - Center: Pill-shaped navigation menu. Items: Dashboard (active - Deep Midnight Navy fill, white text), Orders, Team, Products, Settings (inactive - Slate Navy text, transparent).
   - Right: Notification bell icon, User Profile Avatar (circular).
2. **Welcome Section (Top Left):** 
   - Large greeting heading (Slate Navy).
3. **Stat Metrics Row:** 
   - Three floating cards showing key metrics: Total orders packed (large Bold number, e.g., 1248), Storage remaining (e.g., 50GB), Processing speed (e.g., 250 orders/day).
4. **Progress Chart Card (Main area):**
   - Bar chart showing weekly orders. Use pill-shaped capsule bars. Today's bar is filled with solid Vivid Ocean Blue and slightly wider; other days are lighter and thinner.
5. **Top Employees Card (Featured Dark Card):** 
   - Deep Midnight Navy background with `24px` rounded corners. Top edge shows a subtle translucent layering effect.
   - Displays top 3 performing employees in a list with white text and small light-colored pill buttons.
6. **Storage Usage Card (Arc/Circular Progress):**
   - A semi-circle/donut arc chart. Vivid Ocean Blue for the filled track, Soft Glacier Blue for the empty track. Large bold percentage in the center.

---

## Screen 2 — Recording Desk (Quay Đóng Hàng)

A highly focused, distraction-free operational screen for webcam recording. It auto-detects QR codes to start/stop the camera. State clarity is paramount.

**Page Structure:**
1. **Header (Top Nav):** Same as Screen 1, but "Recording Phase" tab is active.
2. **Camera Viewport (Left Column / 60% width):**
   - Massive Pure White card, `24px` border radius, soft drop shadow.
   - Live webcam feed centered inside. 
   - **Waiting State:** Blinking inset overlay with a prompt text in Misty Slate asking to scan a QR code.
   - **Recording State:** The camera frame glows with a Vivid Ocean Blue border to indicate live recording. 
   - Bottom badge indicating camera device ("Logitech Brio 4K - Active").
3. **Current Processing Order (Top Right / Featured Dark Card):**
   - Deep Midnight Navy (`#142A56`) background.
   - Shows current Order ID and customer name in white.
   - Giant real-time timer (00:00:15).
   - Two large pill-shaped buttons (Vivid Ocean Blue): "Start Manually" and "Stop".
4. **Recent Activity List (Bottom Right):** 
   - Pure White card displaying the 5 most recently packed orders. 
   - Each row features a Vivid Ocean Blue circular checkmark, Order ID, and timestamp.

---

## Screen 3 — Order History (Quản Lý Đơn Hàng)

An open, grid-based list of recorded proof videos. Replaces traditional tables with floating, spacious modern rows.

**Page Structure:**
1. **Header:** "Orders" tab is active.
2. **Search & Filter Action Bar:** 
   - A wide, entirely borderless, unboxed pill-shaped search input with a magnifying glass icon. Very soft shadow. Placeholder prompts for Order ID or Customer name.
   - Adjacent Filter Chips: "Today", "This Week", "Sync Errors" (Soft Glacier Blue backgrounds, Vivid Ocean Blue text).
3. **Data List (Card-based Layout):** 
   - Instead of a rigid grid table, each order is a distinct Pure White row/card with immense breathing room, separated by Frosty Cloud background gaps.
   - Each row contains: Bold Order ID, a small rounded video thumbnail, timestamp (Misty Slate), and a pill-shaped status chip ("Success", "Pending Upload").
   - Right side features a 3-dot menu or minimal icon buttons for Download and Play.
4. **Pagination (Bottom):** Pill-shaped "Next" and "Prev" navigation buttons.

---

## Screen 4 — Team Management (Quản Lý Nhân Viên)

HR command center to track packing performance. Highly human-centric layout utilizing multiple circular avatars.

**Page Structure:**
1. **Header:** "Team" tab is active.
2. **Summary Stats (Top Cards):**
   - Row of 3 mini metric cards: Total staff, Active shift count, Weekly performance variance (+15%). Bold Slate Navy numbers.
3. **Employee Grid List (Masonry/Card View):** 
   - Massive, softly rounded Pure White cards (`24px` radius) arranged in a grid.
   - Top half of each card features a very soft, faint gradient background with a large circular avatar placed cleanly in the center (thick white border around avatar).
   - Bottom half displays the employee name (Slate Navy), Job Title/Role (Misty Slate).
   - Includes a small, pill-shaped progress bar showing tasks completed today vs shift goals (Ocean Blue fill).
4. **Add New Button:** Positioned as the first card in the grid—an empty state card with a dashed border, a plus icon, and a prompt to "Add Employee".

---

## Screen 5 — Products Showcase (Sản Phẩm Bán Hàng)

Visual gallery where store owners upload and manage product thumbnails for the system. 

**Page Structure:**
1. **Header:** "Products" tab is active.
2. **Header Title & Actions:** 
   - Page Title and a primary Deep Midnight Navy pill button to "+ Add New Product".
3. **Product Gallery (Masonry / Card View):** 
   - Ultra-clean square or vertical rectangle cards with enormous padding (`32px`).
   - The product image fills the top portion of the card seamlessly.
   - Below the image: Product Name (Semi-bold), Price (Bold, Slate Navy). Faint background chip for the SKU code.
   - Inside the top-right corner of the image (absolute positioning), a white circular floating action button (FAB) containing an Edit/3-dot icon.

---

## Screen 6 — Settings & Billing (Cài Đặt)

A 2-column configuration area focusing on account security, software setup, and clean, trustworthy subscription tier blocks.

**Page Structure:**
1. **Header:** "Settings" tab is active.
2. **Settings Layout (Dual Column):**
   - **Left Column (Sidebar navigation):** Encased entirely in a large Pure White card. Contains vertical pill-shaped menu items: Profile, Security, Billing/Plan (active), Device Integrations.
   - **Right Column (Main Form - Billing Context):** 
     - **Current Plan Status (Featured Dark Card):** Deep Midnight Navy background reporting current "Pro Plan - 100GB". Features a vivid blue donut progress tracker indicating storage usage.
     - **Settings Form (Pure White Container):** Form fields do NOT use traditional borders. Utilize 'inset' incredibly faint gray backgrounds for fields, with fully rounded (`rounded-full`) or heavily rounded corners. Misty Slate text.
     - A primary Vivid Ocean Blue pill button at the bottom for "Save Changes". Ensure large `24px+` vertical spacing between all form elements.
