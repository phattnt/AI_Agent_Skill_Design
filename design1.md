# Design System: Neumorphism Soft UI Dashboard
**Style Origin:** Neumorphism (Soft UI) × Minimalist Dashboard
**Color Mode:** Light — Cool White-Blue Tonal Base
**Version:** 1.0

---

## 1. Visual Theme & Atmosphere

**Mood:** Tactile · Calm · Architecturally Precise · Softly Trustworthy

This interface does not sit *on top of* its background — it *grows out of it*. Every card, button, and panel feels as if it has been gently extruded from a slab of cool-tinted white polymer. The visual language is rooted in **Neumorphism (Soft UI)**: surfaces are defined not by borders or color contrast, but entirely by the disciplined play of paired shadows — a warm-dark shadow swept to the lower-right, and a cold-white highlight swept to the upper-left, simulating a consistent overhead-left light source.

Layered over this tactile material language is a **Minimalist Dashboard** philosophy: negative space is load-bearing, information density is deliberately restrained, and color is deployed with surgical purposefulness. A deep navy owns all interactive authority. A vivid electric blue communicates life and momentum. Everything else is near-neutral.

**Key Characteristics:**
- Cards and containers emerge from the background by shadow alone — no visible borders
- Heavy squircle geometry (`border-radius: 20px–28px`) softens every edge into a friendly curve
- A single dark featured card breaks the monochromatic rhythm and anchors visual hierarchy
- Progress and status elements pulse with saturated Cobalt Blue — the only high-energy color in the palette
- Generous padding and whitespace ensure the interface never feels crowded or anxious
- The cool-blue page background (`#EAF0F8`) is structurally critical — it is the contrast medium that makes white card surfaces visibly "lift"

**Density:** Medium-low. Cards breathe. Sections self-separate without borders.  
**Texture:** Smooth, matte, frictionless. Soft tonal shadows only — no painted gradients.  
**Personality Adjectives:** Sculpted · Airy · Clinical-Warm · Soft-Tech · Professional.

---

## 2. Color Palette & Roles

### Background Foundation
- **Glacial Mist** (`#EAF0F8`) — The primary page canvas. A barely-blue white that provides just enough contrast to make Pure Chalk cards visibly "float." This is not decorative — the cool undertone is structurally necessary for the Neumorphic effect to function. Without it, the white highlight shadow disappears.
- **Icy Veil** (`#F0F4F9`) — A softer alternative for secondary section backgrounds, modal overlays, or nested panel backgrounds where even less contrast is required.

### Surface / Cards
- **Pure Chalk** (`#FFFFFF`) — All card and container surfaces. Absolute white — no tinting — so the dual shadow pair can operate at full effectiveness. The very whiteness is what makes the embossed illusion work.

### Primary Accent — Authority & Navigation
- **Midnight Sapphire** (`#1C3B68`) — The dominant dark accent. Commands maximum visual weight. Used for: active navigation item fills, the featured Onboarding Task card, primary CTA button backgrounds, and any element that must communicate absolute authority. Evokes the depth of pressed indigo ink — confident, trustworthy, final.
- **Deep Dusk Blue** (`#1A365D`) — The pressed/hover state of Midnight Sapphire elements. A marginally deeper navy for interactive depth states and dark-surface inner shadow layering.

### Secondary Accent — Activity & Progress
- **Cobalt Pulse** (`#2563EB`) — Fully saturated vivid electric blue used sparingly but with intention. Signals active state, forward momentum, and live data. Appears in: progress bars, circular arc trackers, active tab indicators, and status chips. High energy — disciplined use only.
- **Blue Arc** (`#1D4ED8`) — The pressed/active variant of Cobalt Pulse. Used as the inner stroke of progress rings to create perceived depth within the ring, or as the active state of secondary interactive elements.

### Typography Colors — A Four-Level Hierarchy
- **Slate Ink** (`#1E293B`) — All primary headings and high-priority body text. A near-black with a blue undertone — never flat black. Reads modern and confident.
- **Steel Shadow** (`#334155`) — Secondary text: body copy, descriptions, list content. Lighter than Slate Ink to signal supporting role while remaining fully legible.
- **Cloud Detail** (`#64748B`) — Tertiary labels: metadata, subtitles, timestamps, idle state hints. Clearly subordinate without disappearing.
- **Whisper Gray** (`#94A3B8`) — The lightest text tier. Placeholders, UI ghost text, decorative labels. Should not compete for attention with any other text.

### Shadow System Colors (Applied to `box-shadow` Only — Never as Surface Fills)
- **White Highlight Shadow** (`rgba(255, 255, 255, 0.90)`) — The upper-left light-source shadow. Simulates the lit side of a raised element. Never a fill color — only a CSS shadow value.
- **Cool Depth Shadow** (`rgba(166, 180, 200, 0.45)`) — The lower-right gravity shadow. A blue-gray tone that inherits the palette's cool character — never pure black, which would feel foreign in this material.

---

## 3. Typography Rules

**Philosophy:** Precise geometric letterforms with enough humanist warmth to avoid feeling cold or sterile. The typeface must read cleanly at small dashboard sizes (11px badges, 12px metadata) without sacrificing display elegance at large heading sizes.

### Recommended Font Pairing
- **Display & Headings:** `"DM Sans"` or `"Plus Jakarta Sans"` — geometric, optically balanced, modern without being corporate-neutral. Avoid Inter (overused), Roboto (system-default feel), or Arial (legacy stigma).
- **Body & Data Labels:** `"Nunito"` or `"Figtree"` — softly rounded letterforms that architecturally echo the heavy squircle geometry of the UI. Numbers remain legible and clean at 11–12px.

### Weight Hierarchy

| Weight | Usage |
|--------|-------|
| `700` Bold | Dashboard section titles, card headlines, key metric values (e.g., large timer digits) |
| `600` SemiBold | Active navigation labels, sub-section headers, button labels, badge text |
| `400` Regular | Body copy, descriptions, list items |
| `300` Light | Timestamps, secondary subtitles, meta-information (use sparingly — too many light-weight elements feel weak) |

### Letter-Spacing Character
- **Headings:** `letter-spacing: -0.02em` — Tight and confident; prevents large text from feeling loose.
- **Body:** `letter-spacing: 0em` — Natural, unmodified.
- **Uppercase badges / chips / small labels:** `letter-spacing: 0.06em` — Slightly open tracking for legibility and editorial refinement at small scale.

### Line Height
- Display headings: `1.15`
- Body text: `1.6`
- UI labels and metadata: `1.2`

---

## 4. Component Stylings

### Buttons

**Primary (Dark — Maximum Authority)**  
Shape: Fully pill-shaped or near-pill (`border-radius: 50px`). Filled with Midnight Sapphire (`#1C3B68`). White SemiBold label. Casts a subtle outward Neumorphic shadow to appear lifted from the pale background. On hover: `transform: scale(1.02)` + increased shadow spread. On press: shadow transitions inward (pressed-in effect).

**Secondary / Ghost (Soft — Supporting Actions)**  
Same pill shape. Background is Pure Chalk (`#FFFFFF`) with the standard dual-shadow applied. Text in Slate Ink (`#1E293B`) or Cobalt Pulse (`#2563EB`). On hover: shadow inverts direction to simulate physical depression feedback.

**Active Navigation Item**  
Pill-shaped. Filled solidly with Midnight Sapphire — no outline, no underline. The fill alone is the selected state signal. White SemiBold label.

---

### Cards & Containers

All cards use Pure Chalk (`#FFFFFF`) with the **Raised Dual Shadow** applied:

```css
background: #FFFFFF;
border-radius: 24px;
box-shadow:
  -6px -6px 14px rgba(255, 255, 255, 0.90),
   6px  6px 14px rgba(166, 180, 200, 0.45);
```

**Corner Roundness:** Squircle-generous. Full cards: `border-radius: 20px–28px`. Internal chips/badges: `border-radius: 12px–16px`. Buttons: `border-radius: 50px` (pill). **No sharp corners exist anywhere in this design system.**

**Elevation States:**
- **Default (raised):** Standard dual outer shadow
- **Selected / Active (pressed-in):** Shadow pair inverts to inset — signals selection
- **Modal / Overlay:** Raised card with increased shadow multiplier for vertical lift

**Featured Dark Card (e.g., Onboarding Task Block):**  
Filled with Midnight Sapphire (`#1C3B68`). All inner text in Pure Chalk white. Shadow adjusted for dark surface:

```css
background: #1C3B68;
border-radius: 24px;
box-shadow:
  -4px -4px 10px rgba(255, 255, 255, 0.06),
   6px  6px 16px rgba(10, 22, 50, 0.50);
```

This card is the sole high-contrast element — it anchors visual hierarchy and signals primary user task.

---

### Inputs & Forms

**Text Input (Resting State):**  
No visible stroke border. The field is styled as a pressed-in well using an *inverted* dual-shadow:

```css
background: #FFFFFF;
border-radius: 16px;
box-shadow:
  inset 3px  3px 7px rgba(166, 180, 200, 0.50),
  inset -3px -3px 7px rgba(255, 255, 255, 0.85);
```

Placeholder text: Whisper Gray (`#94A3B8`).

**Focus State:**  
Adds a 1.5px Cobalt Pulse (`#2563EB`) ring via `outline` to signal active editing — enough presence to confirm focus, restrained enough not to break the Neumorphic surface feeling.

**Dropdown / Select:**  
Same surface treatment as inputs. Chevron icon in Cloud Detail (`#64748B`).

---

### Progress Indicators

**Linear Progress Bar:**  
Track height: `6px`. Track background: Glacial Mist (`#EAF0F8`) or a softly inset channel. Fill: Cobalt Pulse (`#2563EB`) with a subtle glow:

```css
fill-color: #2563EB;
border-radius: 50px;
filter: drop-shadow(0 0 4px rgba(37, 99, 235, 0.4));
```

**Circular / Arc Progress Tracker:**  
SVG ring. Track stroke: `#D1DCE8` (muted cool gray). Progress stroke: Cobalt Pulse (`#2563EB`). Arc depth: Blue Arc (`#1D4ED8`) for inner ring to create layered dimensionality. Animated via `stroke-dashoffset`. Widget container follows standard Neumorphic card styling.

---

### Badges, Chips & Status Tags

Pill-shaped (`border-radius: 50px`). Backgrounds use diluted tints of the semantic color (e.g., a pale blue-tint for "In Progress"). Text is the deeper shade of that color. **Never flat, high-saturation fills for chips — always tinted.** Typography: SemiBold weight, `letter-spacing: 0.04em`, size `11–12px`.

---

## 5. Layout Principles

### Grid & Structure
- **Max content width:** `1440px`
- **Base grid:** 12-column. Typical dashboard split: 1 fixed sidebar (~220px) + fluid main content area
- **Card grid:** Full-width, half-width (2-col), or 1/3 (3-col) depending on widget content density
- **Base spacing unit:** `8px` — all spacing follows `8, 16, 24, 32, 48, 64px` multiples

### Whitespace Strategy (Load-Bearing)

This design uses whitespace and shadow — not borders — to define every spatial zone.

| Zone | Spacing |
|------|---------|
| Card internal padding | Min `24px` all sides |
| Between cards | `20–28px` gap |
| Between major sections | `48–64px` vertical |
| Edge margins | `24px` mobile · `40px` tablet · `48px` desktop |

### Visual Hierarchy Flow
1. **Featured dark card** (Midnight Sapphire) — highest visual weight; signals primary task
2. **Metric / tracker cards** — secondary priority; data at a glance
3. **List / table sections** — supporting detail
4. **Navigation sidebar** — ambient; never competing

### Alignment Philosophy
- Primary content — left-aligned
- Metric values in widgets — centered or right-aligned per widget type
- Section titles — consistent left edge aligned with card padding
- **Borders carry no spatial information** — all zone separation is achieved through: whitespace + shadow + background contrast

### Responsive Behavior
- Sidebar collapses to bottom navigation bar at narrow viewports
- Cards stack vertically in single-column layout on mobile
- Neumorphic shadow values remain constant — they do not scale with breakpoints
- Touch targets: minimum `44×44px` for all interactive elements (WCAG compliant)

---

## 6. Motion & Interaction Principles

**Core Feel:** Pressing any interactive element should feel like gently depressing a soft silicone key — not a mechanical click, but a satisfying tactile depression.

### Hover States
- **Raised cards:** Subtle lift via `transform: scale(1.015)` + increased outward shadow spread
- **Primary buttons:** `transform: scale(1.02)` + shadow amplification
- **Inactive navigation items:** Background tints to a very light Glacial Mist fill (`#EAF0F8`) over `150ms`

### Press / Active States — The Characteristic Neumorphic Interaction

When any raised button or card is pressed, the outward dual-shadow transitions to an inward inset-shadow in `100–150ms`:

```css
/* Raised default */
box-shadow:
  -6px -6px 14px rgba(255, 255, 255, 0.90),
   6px  6px 14px rgba(166, 180, 200, 0.45);

/* Pressed / active */
box-shadow:
  inset 4px  4px 10px rgba(166, 180, 200, 0.50),
  inset -4px -4px 10px rgba(255, 255, 255, 0.88);

transition: box-shadow 130ms ease, transform 130ms ease;
```

### Progress Animations
Progress bars and arc trackers animate their fill `0% → actual value` on mount using an `ease-out` curve over `700ms`. This communicates "live data being loaded" and draws the eye on initial render.

### Page / Section Entrance
Cards fade and slide up: `opacity: 0 → 1` + `translateY(8px → 0px)` over `300ms ease-out`, staggered at `60ms` per card. Keeps the page load feel smooth and sequential without theatrical excess.

---

## 7. Neumorphic Shadow Reference (Implementation Ready)

The entire character of this design system is encoded in three CSS shadow patterns. Apply them consistently and exclusively.

### Pattern A — Raised Element (Default: Cards, Inactive Buttons)
```css
background: #FFFFFF;
border-radius: 24px;
box-shadow:
  -6px -6px 14px rgba(255, 255, 255, 0.90),
   6px  6px 14px rgba(166, 180, 200, 0.45);
```

### Pattern B — Pressed / Inset Element (Inputs, Active Selection)
```css
background: #FFFFFF;
border-radius: 16px;
box-shadow:
  inset 4px  4px 10px rgba(166, 180, 200, 0.50),
  inset -4px -4px 10px rgba(255, 255, 255, 0.88);
```

### Pattern C — Dark Variant Card (Midnight Sapphire Surface)
```css
background: #1C3B68;
border-radius: 24px;
box-shadow:
  -4px -4px 10px rgba(255, 255, 255, 0.06),
   6px  6px 16px rgba(10, 22, 50, 0.50);
```

> **Critical structural rule:** The page background (`#EAF0F8`) and the card surface (`#FFFFFF`) *must* maintain sufficient contrast for the white highlight shadow to remain visible. If both surfaces converge toward the same lightness, the Neumorphic emboss effect collapses entirely. The cool-tinted page background is an engineering decision, not a decorative one.

---

## 8. Design System Reference — Prompt Language

When generating new screens consistent with this system, always use **descriptive visual language** (not technical class names):

| Technical Value | Descriptive Language for Prompting |
|-----------------|-------------------------------------|
| `border-radius: 24px` | "Generously squircle-rounded corners" |
| Pattern A shadow | "Softly embossed — raises from the page" |
| Pattern B shadow | "Gently pressed inward, like a soft-material depression" |
| `#1C3B68` fill | "Midnight Sapphire — deep navy authority" |
| `#2563EB` | "Cobalt Pulse — vivid electric blue signal" |
| `#EAF0F8` page | "Glacial Mist — cool white-blue canvas" |
| `#FFFFFF` + shadow | "Pure Chalk card, softly lifted from the background" |

### Component Prompt Examples
- *"Create a metrics card in Pure Chalk with softly embossed Neumorphic shadows, generously squircle-rounded corners, 24px internal padding, and a bold Midnight Sapphire headline value."*
- *"Design a circular arc progress tracker: Cobalt Pulse arc on a muted cool-gray SVG track, centered in a raised Chalk card, animated on load with an ease-out fill curve."*
- *"Add a featured task block as a Dark Variant Card filled with Midnight Sapphire: white SemiBold heading, white secondary text, white pill-shaped ghost button with subtle white highlight shadow."*
