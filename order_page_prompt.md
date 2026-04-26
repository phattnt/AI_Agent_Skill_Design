Generate a complete desktop-first web application view for an "Order Archive Page" for the "Packing Video Proof App". This page helps E-commerce sellers view their history of packed orders and watch corresponding video proofs.

**DESIGN SYSTEM (Luminous Bento - STRICTLY FOLLOW THIS STYLE):**
- **Platform:** Web, Desktop-first
- **Theme:** Minimalist, flat, surgical, weightless. Absolutely NO drop-shadows.
- **Backgrounds:** Global app background is Surgical Canvas (#F9FAFB). All card/container surfaces are Absolute White (#FFFFFF).
- **Separation:** Use Hairline Delineator (#E5E7EB) 1px solid borders on all cards to create a crisp Bento layout.
- **Colors:** Primary Accent is Fluid Sapphire (Gradient from #1D4ED8 to #3B82F6) for primary CTA buttons. Text is Deep Slate (#0F172A) for headings, Cloud Gray (#64748B) for secondary labels.
- **Geometry:** Buttons and inputs must be strictly pill-shaped (rounded-full). Cards must have smoothly rounded corners (24px).
- **Spacing:** Use an asymmetric Bento Grid. Minimum 24px internal padding for cards and 24px gutters between layout blocks.

**PAGE STRUCTURE & COMPONENTS:**

**IMPORTANT:** Use the exact HTML structure and Tailwind classes provided below for the SideNavBar and TopNavBar to maintain strict consistency with the Dashboard layout. Note that the active state for the sidebar link should be moved to the "Đơn hàng" (Orders) item for this page.

### 1. SideNavBar Code
```html
    <aside
        class="h-[calc(100vh-48px)] w-64 glass-panel rounded-3xl fixed left-6 top-6 flex flex-col p-6 space-y-8 z-50">
        <div class="flex items-center gap-3">
            <div class="w-10 h-10 rounded-xl bg-primary-container flex items-center justify-center shadow-sm">
                <span class="material-symbols-outlined text-white"
                    style='font-variation-settings: "FILL" 1;'>package_2</span>
            </div>
            <div>
                <h1 class="text-xl font-bold tracking-tight text-gray-900 leading-none">PackProof AI</h1>
                <p class="text-[10px] uppercase tracking-widest text-gray-500 mt-1">Enterprise Logistics</p>
            </div>
        </div>
        <nav class="flex-1 space-y-2">
            <a class="flex items-center gap-3 px-4 py-2 text-gray-600 hover:bg-white/40 rounded-full text-sm font-medium tracking-tight transition-colors duration-200"
                href="#">
                <span class="material-symbols-outlined">dashboard</span>
                <span>Tổng quan</span>
            </a>
            <a class="flex items-center gap-3 px-4 py-2 text-gray-600 hover:bg-white/40 rounded-full text-sm font-medium tracking-tight transition-colors duration-200"
                href="#">
                <span class="material-symbols-outlined">videocam</span>
                <span>Phòng quay video</span>
            </a>
            <a class="flex items-center gap-3 px-4 py-2 text-blue-800 bg-white/50 shadow-sm rounded-full text-sm font-medium tracking-tight transition-all"
                href="#">
                <span class="material-symbols-outlined">receipt_long</span>
                <span>Đơn hàng</span>
            </a>
            <a class="flex items-center gap-3 px-4 py-2 text-gray-600 hover:bg-white/40 rounded-full text-sm font-medium tracking-tight transition-colors duration-200"
                href="#">
                <span class="material-symbols-outlined">groups</span>
                <span>Đội ngũ</span>
            </a>
            <a class="flex items-center gap-3 px-4 py-2 text-gray-600 hover:bg-white/40 rounded-full text-sm font-medium tracking-tight transition-colors duration-200"
                href="#">
                <span class="material-symbols-outlined">inventory_2</span>
                <span>Danh mục</span>
            </a>
        </nav>
        <div class="mt-auto pt-6 border-t border-white/30">
            <a class="flex items-center gap-3 px-4 py-2 text-gray-600 hover:bg-white/40 rounded-full text-sm font-medium tracking-tight transition-colors duration-200"
                href="#">
                <span class="material-symbols-outlined">settings</span>
                <span>Cài đặt</span>
            </a>
        </div>
    </aside>
```

### 2. Layout Shell & TopNavBar Code
Wrap the page content in the following layout structure (`<main class="... ml-80">`) to ensure side navigation spacing is preserved. Place the TopNavBar inside it.

```html
    <main class="min-h-screen pt-6 pr-6 pb-6 ml-80">
        <header class="h-16 glass-panel rounded-full sticky top-6 z-40 mb-8 flex justify-between items-center px-8">
            <div class="flex items-center shadow-sm rounded-full px-4 py-1.5 w-96 bg-white/20">
                <span class="material-symbols-outlined text-gray-500 text-sm">search</span>
                <input
                    class="bg-transparent border-none focus:ring-0 text-sm w-full font-inter placeholder:text-gray-500 text-gray-800"
                    placeholder="Tìm kiếm đơn hàng, video, hoặc nhân viên..." type="text" />
            </div>
            <div class="flex items-center gap-6">
                <div class="flex items-center gap-4">
                    <button class="text-gray-600 hover:text-blue-700 transition-all relative">
                        <span class="material-symbols-outlined">notifications</span>
                        <span class="absolute top-0 right-0 w-2 h-2 bg-red-500 rounded-full shadow-sm"></span>
                    </button>
                    <button class="text-gray-600 hover:text-blue-700 transition-all">
                        <span class="material-symbols-outlined">help_outline</span>
                    </button>
                </div>
                <div class="h-8 w-[1px] bg-white/50"></div>
                <div class="flex items-center gap-3">
                    <div class="text-right">
                        <p class="text-sm font-semibold text-gray-900 leading-none">Alex Rivera</p>
                        <p class="text-[11px] text-gray-600 mt-1">Ops Manager</p>
                    </div>
                    <img alt="User profile" class="w-10 h-10 rounded-full object-cover shadow-sm border border-white/50"
                        src="https://lh3.googleusercontent.com/aida-public/AB6AXuCqCERu0dE8OYuwtmS-Vc3OX0PtD4pxp83IU02pes-IOmN19K6ay6p9nc8ttnpDoUky5eyaokXJZqVO0998dwCp_vQ7p_l96hwRe0-hdouiKA4-2XoXQqH-T5ogff6XstbJnJodeKl4yrDM1yOKQa59g8GexZLz_4-kfDWN3ZG0HUzVv_YZDPHoaTnmh5lJ37v2d8jGCoski7AguuVQWVV6gp5jb5hvpon4ZQvYcIiR9LcwNJ3Fm_kPe8cxH_OkenY51mbMAbkHcrYP" />
                </div>
            </div>
        </header>
        
        <!-- NEW PAGE CONTENT GOES HERE -->
```

### 3. Order Page Content Area
For the actual Order page content inside the layout structure above, construct a crisp bento grid layout similar to the dashboard, containing:

1. **Header Card:** A clean top header bento card with the title "Order Archive". It must include a pill-shaped search bar for "Order ID / Customer" and active filter chips for platforms (e.g., "Shopee", "TikTok", "Lazada").
2. **Metrics Cards:** A row of 3 smaller Bento cards just below the header showing quick insights: (1) Total Orders Processed, (2) Videos Stored, (3) Disputed Claims.
3. **Order Table Card:** A large, full-width bento card holding a data table. The table should list: Order ID, Date, Platform Logo/Name, Customer Name, and a 'Play Video Proof' primary action button.
4. **Pagination:** A subtle pagination component at the bottom of the table card.

Please generate the foundational React components and Tailwind UI for this screen, ensuring strict adherence to the Luminous Bento design system and bento grid layout without any drop-shadows.
---
💡 **Tip:** For consistent designs across multiple screens, create a DESIGN.md file using the `design-md` skill. This ensures all generated pages share the same visual language.
