# Design System: Crextio HR Dashboard
**Project ID:** Crextio-Soft-UI

## 1. Visual Theme & Atmosphere
The interface embodies a **soft, airy, and ultra-modern** aesthetic that lies somewhere between flat design and Neumorphism. It feels weightless, clean, and highly approachable. It relies heavily on soft, cool-toned backgrounds to define space, using perfectly white cards that float with whisper-thin shadows. 

The mood is **calm, professional, yet distinctly high-tech**. The generous use of border radii (squircle shapes) and pill-shaped elements makes the interface feel tactile and friendly. The deep navy anchor card provides necessary weight and visual hierarchy against the otherwise light and floating components.

## 2. Color Palette & Roles

### Background & Surface
* **Frosty Cloud (#EBF1F6):** The primary app background. A very cool, highly desaturated light blue that provides just enough contrast for the white cards to pop. Structurally essential.
* **Pure White (#FFFFFF):** Used for all primary cards, containers, and elevated surfaces.

### Accents & Interactives
* **Vivid Ocean Blue (#1A73E8):** The primary energetic accent. Used for the active navigation pill, progress bar fills, highlighted statistics, and active checkboxes. 
* **Deep Midnight Navy (#142A56):** Used for the featured 'Onboarding Task' card to anchor the design and draw immediate attention to primary tasks. 
* **Soft Glacier Blue (#D9E6F6):** A light tint of the primary blue, used for inactive or secondary progress metrics, pill backgrounds, and subtle highlights.

### Typography
* **Slate Navy (#1E293B):** Primary text color for large numbers, section headers, and primary data points. Crisp and highly readable.
* **Misty Slate (#64748B):** Secondary text color used for subtitles, metadata (e.g., dates, 'Work Time'), and axis labels.

## 3. Typography Rules
**Font Family:** `Plus Jakarta Sans` or `Outfit` (Geometric, friendly, and highly legible).

* **Display/Stat Numbers:** Bold weight (700), tightly tracked (-0.02em). Used for the massive "92", "75", "315" stats to create impact.
* **Section Headers:** Semi-bold weight (600), standard tracking. Used for "Welcome in, Nixtio", "Progress", "Time tracker".
* **Body/Metadata:** Regular weight (400), slightly relaxed line-height (1.5). Used for dates, times, and small descriptive text.
* **Tabs/Nav:** Medium weight (500), slightly expanded letter-spacing for readability in small pill shapes.

## 4. Component Stylings

* **Navigation/Tabs (Top Header):** 
  * Active state is a pill-shape (`rounded-full`), filled with Deep Midnight Navy, white text.
  * Inactive state is transparent with Slate Navy text, no borders.
* **Cards/Containers:**
  * **Default Cards:** Pure White background, generously rounded corners (approx. `24px`), with a whisper-soft diffused shadow (`box-shadow: 0 4px 20px rgba(0, 0, 0, 0.03)`).
  * **Featured Dark Card (Onboarding):** Deep Midnight Navy background. The top edge features an interesting overlapping layer effect, creating a tab-like or folder-like depth.
* **Progress Bars (Top Left):**
  * Fully pill-shaped (`rounded-full`). The active fill is Vivid Ocean Blue, resting on a Soft Glacier Blue track.
* **Bar Charts (Progress Section):**
  * Capsule/pill shaped bars. Active day is Vivid Ocean Blue and slightly wider; inactive days are Slate Blue and thinner.
* **Profile Card (Bottom Left):**
  * Uses a soft gradient or image background that blends seamlessly. Features a glassmorphic or highly blurred overlay chip for the "$1,500" tag.

## 5. Layout Principles
* **Whitespace & Breathing Room:** Extremely generous padding within cards (mostly 24px-32px). The interface relies on margins and padding, rather than lines or borders, to separate content.
* **Grid Alignment:** Masonry-style or asymmetrical grid that allows different sized widgets to stack perfectly.
* **Corner Consistency:** There are absolutely no sharp corners in this UI. Everything from the main content wrappers to the tiniest progress bar uses heavy rounding.
