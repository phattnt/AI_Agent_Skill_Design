Generate a complete desktop-first web application for a "Packing Video Proof App". This app helps E-commerce sellers record packing videos via Webcam (triggered by scanning QR codes) to prevent false refund claims.

**DESIGN SYSTEM (Luminous Bento - STRICTLY FOLLOW THIS STYLE):**
- **Theme:** Minimalist, flat, surgical, weightless. Absolutely NO drop-shadows.
- **Backgrounds:** Global app background is Surgical Canvas (#F9FAFB). All card/container surfaces are Absolute White (#FFFFFF).
- **Separation:** Use Hairline Delineator (#E5E7EB) 1px solid borders on all cards to create a crisp Bento layout.
- **Colors:** Primary Accent is Fluid Sapphire (Gradient from #1D4ED8 to #3B82F6) for CTAs. Text is Deep Slate (#0F172A) for headings, Cloud Gray (#64748B) for secondary labels.
- **Geometry:** Buttons and inputs must be strictly pill-shaped (rounded-full). Cards must have smoothly rounded corners (24px).
- **Spacing:** Use an asymmetric Bento Grid. Minimum 24px internal padding for cards and 24px gutters between layout blocks.

**APPLICATION STRUCTURE & VIEWS:**
Create a persistent left Sidebar Navigation (Dashboard, Recording Studio, Orders, Team, Catalog, Settings) that dynamically loads the following 6 views:

1. **Dashboard:** Top row with 3 Bento cards: (1) Total Orders, (2) Cloud Storage progress bar, (3) Today's metrics. Below: A large chart card for "Weekly Volume" and a side card for "Top Performers" ranking.
2. **Recording Studio:** A massive central card displaying a webcam placeholder frame with a QR target overlay and a dynamic status badge ("Waiting for QR..." vs "Recording Order #12345"). Right-side panel showing "Current Order Details" and a "Recent History" list.
3. **Order Archive:** A top header with a pill-shaped search bar and filter chips (Shopee, TikTok, Lazada). Below it, a full-width data table listing Order ID, Date, Platform, and a 'Play Video Proof' action button.
4. **Team Roster:** A grid of employee profile cards. Each card contains a perfect-circle avatar, name, and two metrics (Total Packed, Avg Time).
5. **Product Catalog:** A masonry or standard grid of product reference images with SKUs underneath to help packers identify items.
6. **Settings:** A split layout showing Hardware configuration (Webcam source dropdown, Video resolution) and Billing details (Storage plan progress bar, Upgrade CTA).

Please generate the foundational React components, routing shell, and Tailwind UI for these screens using the requested design system.
