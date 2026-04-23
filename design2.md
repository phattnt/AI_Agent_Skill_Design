# Design System: Blue-Tone Project Management Dashboard
**Style Reference:** Donezo Layout × Crextio Blue Palette
**Color Mode:** Light — Cool Arctic Blue Base

---

## 1. Visual Theme & Atmosphere

This interface strikes a balance between **data-dense productivity** and **visual calm** — it never feels cluttered, yet it packs substantial information into every section. The overall atmosphere is that of a **trusted command center**: a place where professionals manage work with quiet confidence.

The structural language comes from a clean, card-based sidebar layout where every component is clearly separated but visually related. Cards appear to float gently above a cool arctic-blue canvas — not through dramatic shadows, but through a whisper-soft elevation that simply communicates "this is a distinct object." The page breathes with generous whitespace, yet remains information-rich.

The color philosophy is resolute: one vivid electric blue owns all interactive authority and progress visualization. A deep midnight navy anchors the single featured card — a bold but disciplined contrast moment. Everything else is restrained neutral territory, letting the blue do its work with surgical precision.

**Key Characteristics:**
- Clean sidebar-plus-content layout; sidebar is white, content area rests on a cool arctic-blue canvas
- Cards are white with gentle, low-contrast shadows — they rise softly, not dramatically
- Bar chart bars are capsule/pill-shaped (rounded on all four corners), giving data a friendly, modern quality
- "Pending" or "inactive" data states use an SVG diagonal hatching pattern instead of a flat fill, adding visual texture without introducing new colors
- One featured dark card (Midnight Fleet navy) per layout breaks the all-white rhythm and immediately draws the eye
- Status chips use tinted backgrounds — never flat, high-saturation fills
- Avatar circles appear throughout as human presence markers in lists and collaboration sections

**Density:** Medium. Information-rich without crowding. Cards breathe with 24px internal padding.
**Texture:** Whisper-smooth. Subtle box shadows for elevation; diagonal hatching for inactive data states.
**Personality Adjectives:** Trustworthy · Crisp · Professional · Data-forward · Quietly Dynamic.

---

## 2. Color Palette & Roles

### Background Foundation
- **Arctic Canvas** (`#E8EDF6`) — The primary page background. A cool, barely-blue gray that feels like early morning sky. Provides the essential contrast that makes white cards visually "lift" off the surface. Not decorative — structurally necessary.
- **Frost Haze** (`#EBF2FA`) — A softer, slightly lighter tint for nested panel backgrounds, modal backdrops, or sidebar section spacing. Used where Arctic Canvas needs to be too prominent.

### Surface / Cards
- **Pure Cloud** (`#FFFFFF`) — All card, sidebar, and container surfaces. Absolute white. Paired with the soft elevation shadow to create the floating card effect without borders.

### Primary Accent — Interaction & Progress
- **Electric Cobalt** (`#2B6FE8`) — The undisputed accent of the entire system. Used for: active navigation highlights, primary CTA button fills, progress bar fills, the highlighted bar in charts, active tab underlines, and any element communicating "action" or "live state." Vivid, saturated, unmistakable — but applied with discipline so it never loses meaning.
- **Royal Azure** (`#1D5CD4`) — Electric Cobalt's pressed/hover companion. Appears when actively interacting with any cobalt-colored element. Also used as the inner depth layer in thick progress arcs to give them dimensionality.

### Featured Dark Accent — Anchoring Hierarchy
- **Midnight Fleet** (`#1C3461`) — Deep, rich navy used exclusively for the featured "stat hero" card and the Time Tracker widget. Never applied to multiple elements — its power comes from rarity. When it appears, the eye immediately finds it. Evokes the depth of a night sky over the ocean.
- **Abyss Deep** (`#152850`) — Midnight Fleet's shadow companion. Used as the `box-shadow` color for dark cards to give them ground-level depth, and as hover-state darkening on dark-surface elements.

### Typography Colors — Four-Level Text Hierarchy
- **Slate Navy** (`#1A2744`) — Primary text. All headlines, large numbers, card titles. A very dark navy-blue — richer than charcoal, cooler than true black. Reads as premium and technical simultaneously.
- **Steel Mist** (`#4A5568`) — Secondary text. Body copy, item descriptions, sidebar inactive labels. Clear and legible, subordinate to Slate Navy without fading away.
- **Cloud Drift** (`#94A3B8`) — Tertiary text. Metadata, timestamps, placeholder text, chart axis labels. Present but not competing.
- **Ghost Trace** (`#CBD5E8`) — The faintest text layer. Used sparingly for instructional placeholder text inside inputs and subtle UI hints.

### Data Visualization Colors
- **Electric Cobalt** (`#2B6FE8`) — Primary data fill. Active bars in bar charts, completed arc in donut/progress charts, filled progress bar tracks.
- **Pale Horizon** (`#94A3B8`) — Secondary/inactive bar fill. Used for non-highlighted bars in charts to provide context without stealing focus from the cobalt highlight bar.
- **Ice Track** (`#CBD5E8`) — Empty track/background for all progress bars and arc charts. The "not yet" zone.
- **Hatching Pattern** *(SVG diagonal lines, stroke `#CBD5E8` at 45°, spacing 4px)* — Used for "Pending" wedge in donut charts and de-emphasized bar segments. Adds texture without introducing a new color, keeping the palette pure.

### Status / Semantic Colors
- **Verdant Chip** (`#D1FAE5` background / `#047857` text) — "Hoàn thành / Completed" status. Calm green tint on chip.
- **Cobalt Chip** (`#DBEAFE` background / `#1D5CD4` text) — "Đang thực hiện / In Progress" status. Tinted Electric Cobalt family.
- **Amber Chip** (`#FEF3C7` background / `#92400E` text) — "Chờ duyệt / Pending" status. Warm amber tint.

---

## 3. Typography Rules

**Primary Font Family:** `"Sora"` or `"DM Sans"` — Geometric, optically balanced, with enough personality to feel designed rather than default. Reads with clarity at both the 11px chip scale and the 48px stat number scale. Avoid Inter (overused), Roboto (too neutral), or system fonts (too invisible).

**Secondary Font Family:** `"Nunito"` or `"Figtree"` — Softly rounded letterforms for body copy and metadata. Numbers render cleanly at small sizes, important for dense data labels.

**Monospace (Time Tracker only):** `"JetBrains Mono"` or `"IBM Plex Mono"` — Used exclusively for the digital clock display in the Time Tracker widget. Prevents digit-width jitter as numbers change.

### Weight Hierarchy
- **Bold (700):** Large stat numbers (e.g., "24", "41%"), page titles, card section headers
- **SemiBold (600):** Active navigation labels, button labels, card sub-headings, chart tooltip values
- **Medium (500):** Secondary card labels, table column headers
- **Regular (400):** Body copy, list item descriptions, inactive sidebar items

### Letter-Spacing Character
- **Page titles & large numbers:** `letter-spacing: -0.02em` — tight, confident, prevents sprawl at large sizes
- **Body text:** `letter-spacing: 0em` — natural, unmodified
- **Chips, badges, uppercase section labels:** `letter-spacing: 0.05em` — slightly open for legibility and editorial quality at small scale

### Line Height
- Display numbers / stat heroes: `1.1`
- Section headings: `1.25`
- Body copy and list items: `1.6`
- UI labels and metadata: `1.3`

---

## 4. Component Stylings

### Buttons

**Primary CTA (Electric Cobalt):**
Moderately rounded corners — not fully pill-shaped, not rectangular: `border-radius: 10px`. Filled with Electric Cobalt (`#2B6FE8`). White SemiBold label. Comfortable padding: `10px 20px`. Hover: background deepens to Royal Azure (`#1D5CD4`) with `box-shadow: 0 4px 14px rgba(43, 111, 232, 0.35)`. Press: slight inward scale `transform: scale(0.98)`.

**Secondary / Ghost:**
Same `border-radius: 10px`. Background Pure Cloud with `1.5px solid #CBD5E8` border. Label in Slate Navy. Hover: border transitions to Electric Cobalt, label color shifts to Electric Cobalt. No fill change on hover — restrained.

**Small Utility Buttons (e.g., "+ Mới", "Thêm Thành Viên"):**
Pill-shaped (`border-radius: 50px`). Ghost style with Electric Cobalt text. Compact padding: `6px 14px`. Used for secondary actions inside card headers.

**Icon Buttons (diagonal arrow links on stat cards):**
Circular ghost button (`border-radius: 50px`), 32px diameter. On white cards: border `1.5px solid #CBD5E8`. On dark (Midnight Fleet) card: border `1.5px solid rgba(255,255,255,0.3)`, icon white.

### Cards & Containers

**Standard Card:**
Pure Cloud (`#FFFFFF`) background. Gently rounded corners — `border-radius: 16px`. Soft elevation shadow: `box-shadow: 0 2px 8px rgba(26, 39, 68, 0.08)`. No visible border. On hover (interactive cards only): shadow lifts to `0 6px 20px rgba(26, 39, 68, 0.13)` with `transition: box-shadow 200ms ease`.

**Stat Hero Card (Featured — Midnight Fleet):**
Dark featured card filled with Midnight Fleet (`#1C3461`). Same `border-radius: 16px`. Deeper shadow: `box-shadow: 0 6px 20px rgba(21, 40, 80, 0.40)`. All text inside: Pure Cloud white for headings, `rgba(255,255,255,0.70)` for supporting text. Accent tag inside uses Electric Cobalt tinted on dark background.

**Sidebar:**
Pure Cloud (`#FFFFFF`). No shadow on sidebar itself — separation from content area is achieved through the background contrast (Arctic Canvas vs. white). Internal structure divided by `8px` section labels in uppercase Cloud Drift text.

### Navigation (Sidebar)

**Active Navigation Item:**
Background fill in Electric Cobalt (`#2B6FE8`), `border-radius: 10px`. Icon and label in Pure Cloud white, SemiBold weight. No underline, no left-border indicator — the fill alone communicates selection.

**Inactive Navigation Item:**
No background. Label in Steel Mist (`#4A5568`), Regular weight. Hover: background tints to a very soft Cobalt Chip tint (`#DBEAFE`), label deepens to Slate Navy.

**Section Labels (MENU, GENERAL):**
Uppercase, Cloud Drift (`#94A3B8`), `font-size: 11px`, `letter-spacing: 0.05em`. Non-interactive, purely structural.

### Bar Chart

Bars are **capsule / pill-shaped** — rounded on all four corners with `border-radius: 50px`. This is critical to the visual character of this design system; rectangular bars would be wrong.

- **Highlighted bar** (current day / peak): Electric Cobalt (`#2B6FE8`) fill, full opacity. Optional tooltip above in a small Midnight Fleet rounded rectangle showing the exact value in white.
- **Standard bars**: Pale Horizon (`#94A3B8`) solid fill, or diagonal hatching pattern for "inactive" periods.
- Bar width: uniform, with generous whitespace between bars.
- X-axis labels: Cloud Drift, Regular, `font-size: 12px`.
- No grid lines — clean and uncluttered.

### Donut / Progress Chart

SVG-based ring chart:
- **Completed arc:** Electric Cobalt (`#2B6FE8`) solid stroke. `stroke-linecap: round`.
- **In Progress arc:** Pale Horizon (`#94A3B8`) solid stroke.
- **Pending arc:** SVG diagonal hatching — `stroke: #CBD5E8`, diagonal lines at 45°, 4px spacing. Gives textural presence without adding a new color.
- Center text: Large Bold percentage in Slate Navy, smaller label in Cloud Drift below.
- Ring thickness: `stroke-width: 18px` (chunky, clearly readable).

### Progress Bars (Linear)

Track: Ice Track (`#CBD5E8`), height `8px`, `border-radius: 50px`.
Fill: Electric Cobalt (`#2B6FE8`), same height and radius. End cap is naturally rounded.
Segmented multi-fill bars (like onboarding progress): segments separated by a 2px Pure Cloud gap, each filled with Electric Cobalt at varying opacity levels to show stages.

### Inputs & Forms

**Text Input:**
Background Pure Cloud. `border: 1.5px solid #CBD5E8`. `border-radius: 10px`. Padding `10px 14px`. Placeholder text in Ghost Trace (`#CBD5E8`).
Focus: border transitions to Electric Cobalt (`#2B6FE8`) with `box-shadow: 0 0 0 3px rgba(43,111,232,0.15)`.

**Search Bar (Header):**
Slightly different — background `#F0F4FB` (very light blue tint), no visible border, `border-radius: 10px`. Magnifying glass icon in Cloud Drift on the left. Keyboard shortcut badge (`⌘F`) sits inside the right edge: `background: #E8EDF6`, `border-radius: 6px`, `font-size: 11px`, Cloud Drift text.

**Dropdown / Select:**
Same border and rounding as text input. Chevron icon in Steel Mist on the right.

### Status Chips / Badges

All chips are pill-shaped (`border-radius: 50px`). Compact padding: `3px 10px`. SemiBold `font-size: 12px`, `letter-spacing: 0.04em`.

- **Completed / Hoàn Thành:** Background `#D1FAE5`, text `#047857`
- **In Progress / Đang Thực Hiện:** Background `#DBEAFE`, text `#1D5CD4`
- **Pending / Chờ Duyệt:** Background `#FEF3C7`, text `#92400E`

Never use flat, high-saturation fills for chips — always tinted backgrounds with a deeper text shade of the same color family.

### Time Tracker Widget (Dark Card Variant)

Filled with Midnight Fleet (`#1C3461`). `border-radius: 16px`. Optional subtle animated wave/swirl texture in background using slightly lighter navy tones (`#1E3D6E` at low opacity).
- Label "Bộ Đếm Thời Gian" in Pure Cloud white, SemiBold.
- Digital time display in `"JetBrains Mono"` Bold, `font-size: 36px`, Pure Cloud white.
- Control buttons: circular pill buttons (`border-radius: 50px`), 40px diameter. Pause: Pure Cloud white fill with dark icon. Stop: Red (`#EF4444`) fill with white icon.

---

## 5. Layout Principles

### Grid & Structure
- **Max content width:** `1440px` for large displays; comfortable at `1280px`
- **Overall layout:** Fixed left sidebar (~200px) + fluid main content area
- **Content area background:** Arctic Canvas (`#E8EDF6`) — the sidebar is white and the content area is Arctic Canvas, creating a clear structural separation without any border or shadow between them
- **Card grid:** Responsive 12-column within content area; stat cards span 3 cols each (4 across); chart and secondary cards span 6 or 4 columns
- **Base spacing unit:** `8px` — all spacing is a multiple: `8, 16, 24, 32, 48, 64px`

### Whitespace Strategy
- **Card internal padding:** `24px` on all sides — generous, never cramped
- **Between cards (gap):** `20px` — gives each card room to breathe without excess
- **Sidebar item padding:** `10px 16px` per item
- **Section vertical rhythm:** `32px` between major content rows; `48px` between layout sections
- **Edge margins (content area):** `32px` padding on all sides inside the main content zone

### Sidebar Layout
- Sidebar is always full-height, white, with a fixed width of ~200px
- Logo + name in top section with `24px` vertical padding
- Navigation items grouped by `MENU` and `GENERAL` section labels
- A dark featured promo card (Midnight Fleet) lives at the very bottom of the sidebar — smaller, self-contained, with white text and an Electric Cobalt CTA button

### Visual Hierarchy Flow
1. **Dark featured card** (Midnight Fleet stat hero or Time Tracker) — highest visual weight; found first
2. **Electric Cobalt elements** (active nav, primary buttons, progress fills) — guide action
3. **Standard white metric cards** — data at a glance
4. **List and table sections** — supporting detail, lower visual priority
5. **Sidebar navigation** — ambient, never competing with content

### Alignment Philosophy
- All primary content: left-aligned flush with card padding
- Large stat numbers: left-aligned within their cards (not centered)
- Chart labels: left-aligned section title, axis labels follow chart margins
- Sidebar items: left-aligned with icon + text label inline
- **No full-width dividers or borders separating major sections** — whitespace and card grouping do all structural separation

### Responsive Behavior
- At viewport < 1024px: sidebar collapses to icon-only strip or bottom navigation
- Card grid collapses: 4-col → 2-col → 1-col as viewport narrows
- Shadows and colors remain constant across breakpoints
- Touch targets: minimum `44×44px` for all interactive elements

---

## 6. Design System Notes for Prompt Generation

When generating new screens using this design system, use the following descriptive language (never raw CSS class names):

| Element | Prompt Language |
|---------|-----------------|
| Page background | "Cool arctic-blue canvas (`#E8EDF6`)" |
| Cards | "White cards with whisper-soft elevation shadow, gently rounded corners (16px)" |
| Featured dark card | "Midnight Fleet deep navy card (`#1C3461`) with white text and deep shadow" |
| Primary buttons | "Moderately rounded Electric Cobalt button (`#2B6FE8`), white SemiBold label" |
| Active nav item | "Electric Cobalt filled block, gently rounded corners, white label" |
| Bar chart bars | "Capsule / pill-shaped bars, fully rounded on all four corners" |
| Donut pending | "Diagonal hatching texture in light gray for the pending arc segment" |
| Progress bar | "Ice Track (`#CBD5E8`) empty track, Electric Cobalt fill, pill end-caps" |
| Status chip | "Tinted pill chip — pale background tint with deeper-shade text, no solid fill" |

### Component Prompt Examples
- *"Create a stats row of four cards on Arctic Canvas: the first card is Midnight Fleet dark navy with a large white Bold number and Electric Cobalt trend tag; the remaining three are Pure Cloud white with whisper-soft shadows and a large Slate Navy Bold number each."*
- *"Design a weekly bar chart with pill-shaped capsule bars: the peak day bar is Electric Cobalt, surrounding days alternate between Pale Horizon solid fill and diagonal hatching; no grid lines."*
- *"Add a Time Tracker dark card in Midnight Fleet navy at the bottom right: monospace Bold white clock digits, circular Pause and Stop control buttons, optional subtle wave texture in the background."*
- *"Build a left sidebar: Pure Cloud white, 200px wide, Electric Cobalt filled active nav item with gently rounded corners, second section group labeled in uppercase Cloud Drift, Midnight Fleet promo card at the bottom with an Electric Cobalt pill CTA button."*
