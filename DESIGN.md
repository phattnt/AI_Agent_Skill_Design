# Design System: Neumorphic Soft Dashboard
**Style Origin:** Neumorphism (Soft UI) × Minimalist Dashboard
**Color Mode:** Light — Cool White-Blue Tonal base

---

## 1. Visual Theme & Atmosphere

**Mood:** Calm, Tactile, Trustworthy, Technically Refined.

This interface feels as though it has been *pressed* from the same material as its background — neither floating above nor sinking below, but *emerging* from the surface. The overall atmosphere is clinical yet approachable: think of a precision-engineered instrument with the warmth of molded plastic. It does not shout. It invites.

The design language is deeply **Neumorphic** — surfaces appear to be sculpted from a single slab of cool-tinted white clay. Every card, button, and container casts paired shadows: a warm-dark shadow to the lower-right suggesting depth, and a cold-white highlight to the upper-left suggesting a light source from above-left. The result is a soft, three-dimensional illusion of embossment without any sharp lines or harsh borders.

Layered upon this, the layout follows a **Minimalist Dashboard** philosophy: generous whitespace, a strict reading grid, and a deliberate hierarchy of typographic weights. Color is used surgically — a reserved deep navy anchors key actions, and a vivid electric blue marks progress and status. Everything else is neutral.

**Density:** Medium-low. Cards breathe. Sections are clearly defined without feeling cluttered.
**Texture:** Smooth, matte, frictionless. No gradients that feel painted; only soft tonal shifts.
**Personality Adjectives:** Airy, Sculpted, Trustworthy, Soft-tech, Clinical-warm.

---

## 2. Color Palette & Roles

### Background
- **Glacial Mist** (`#EAF0F8`) — The foundational canvas. A barely-blue white that provides just enough contrast to make white cards visually "lift" from the surface. Never pure white; the cool undertone reinforces the technology-forward character.
- **Icy Veil** (`#F0F4F9`) — An even softer alternative for section backgrounds or modal backdrops. Used where even less contrast is needed.

### Surface / Cards
- **Pure Chalk** (`#FFFFFF`) — All card and container surfaces. When combined with the dual box-shadow technique, this becomes the medium from which elements appear extruded. The white is absolute — no tinting — so the shadow pairs can do their full work.

### Primary Accent — Action & Navigation
- **Midnight Sapphire** (`#1C3B68`) — The dominant dark accent. Used for: the active navigation button background, the Onboarding Task card fill, primary CTA button backgrounds, and any element that demands maximum visual authority. Conveys authority, depth, and trust. Feels almost like pressed indigo ink on white paper.
- **Deep Dusk Blue** (`#1A365D`) — A marginally darker Navy sibling to Midnight Sapphire. Used as the hover/pressed state for primary dark elements, or as a supplementary dark in gradients when a sense of depth within dark surfaces is needed.

### Secondary Accent — Status & Progress
- **Cobalt Pulse** (`#2563EB`) — A fully saturated, vivid electric blue used sparingly to communicate activity and progress. Seen in: progress bars, circular time-tracker arcs, status indicators, and active tab underlines. It creates an immediate focal point and signals "something is happening here." High energy but disciplined.
- **Blue Arc** (`#1D4ED8`) — A slightly deeper variant of Cobalt Pulse. Used for the pressed/active state of secondary interactive elements, or as the inner stroke of progress rings to create layered depth.

### Typography Colors
- **Slate Ink** (`#1E293B`) — Primary text color for all headings and body content. A very dark, slightly blue-tinted charcoal — never pure black. Reads as confident and modern.
- **Steel Shadow** (`#334155`) — Used for secondary body text and descriptive labels. Slightly lighter than Slate Ink, communicating lower hierarchy without losing legibility.
- **Cloud Detail** (`#64748B`) — Tertiary text: metadata, subtitles, timestamps, disabled states. Clearly subordinate without disappearing into the background.
- **Whisper Gray** (`#94A3B8`) — The lightest text tone in the system. Used for placeholders, decorative labels, and UI hints that should not compete for attention.

### State & Utility
- **Ghost White Highlight** (`#FFFFFF` at 70–80% opacity or as a CSS box-shadow value) — Not a surface; a weapon. This is the upper-left light-source shadow in the dual-shadow Neumorphic technique. Applied as `box-shadow: -4px -4px 10px rgba(255,255,255,0.85)` to simulate the lit side of a raised surface.
- **Cool Depth Shadow** (`rgba(166, 180, 200, 0.45)`) — The lower-right dark shadow in the dual-shadow technique. Applied as `box-shadow: 4px 4px 10px rgba(166, 180, 200, 0.45)`. This color is never pure black; it inherits the cool blue-gray of the palette to keep shadows feeling part of the same material.

---

## 3. Typography Rules

**Font Family Philosophy:** Sans-serif geometric with a humanist warmth. Prefer a font that sits between clinical and approachable — something with optical precision in its uppercase and legibility in dense data contexts.

**Recommended Pairing:**
- **Display / Headings:** `"DM Sans"` or `"Plus Jakarta Sans"` — geometric, friendly, and modern without being sterile. Avoid Inter (too ubiquitous), Roboto (too neutral), or Arial (too system-default).
- **Body / Data:** `"Nunito"` or `"Figtree"` — softly rounded letterforms that echo the squircle geometry of the UI. Numbers read cleanly at small sizes.

**Weight Usage:**
- `700 / Bold` — Dashboard section titles, card headlines, key metric values (e.g., the large time display in a tracker widget).
- `600 / SemiBold` — Navigation labels (especially the active state), sub-section headers, button labels.
- `400 / Regular` — Body copy, descriptions, list items.
- `300 / Light` — Meta information, timestamps, secondary subtitles. Use sparingly for contrast; too much light weight reads as weak.

**Letter-Spacing Character:**
- Headings: `letter-spacing: -0.02em` — Tight and confident, keeping large text from feeling airy.
- Body: `letter-spacing: 0em` — Natural, no modification.
- Uppercase labels / badges: `letter-spacing: 0.06em` — Slightly open tracking to give small-caps legibility and a refined editorial quality.

**Line Height:**
- Display headings: `1.15`
- Body text: `1.6`
- UI labels: `1.2`

---

## 4. Component Stylings

### Buttons

**Primary Button (Dark Action):**
Shape: Generously rounded — fully pill-shaped or near-pill (`border-radius: 50px`). Fills with Midnight Sapphire (`#1C3B68`). White label text at SemiBold weight. Casts a mild outward Neumorphic shadow to appear slightly raised from the background. On hover: subtle scale-up (`transform: scale(1.02)`) and increased shadow depth.

**Secondary / Ghost Button:**
Same pill-shape. Background is Pure Chalk (`#FFFFFF`) with the dual Neumorphic box-shadow applied. Text in Slate Ink or Cobalt Pulse. On hover: inverts shadow direction slightly (pressed-in effect) to simulate a push feedback — `box-shadow` pair swaps inward.

**Active Navigation Item:**
Pill-shaped, filled with Midnight Sapphire. White label. Acts as a visual anchor within the nav — the one element that is unambiguously "selected." No outline or underline; the fill alone communicates state.

### Cards / Containers

All cards use Pure Chalk (`#FFFFFF`) background with **dual Neumorphic shadows:**

```css
box-shadow:
  -5px -5px 12px rgba(255, 255, 255, 0.9),
   5px  5px 12px rgba(166, 180, 200, 0.45);
```

**Corner Roundness:** Squircle-generous. Approximately `border-radius: 20px–28px` on full cards. Inner nested elements (chips, badges) use `border-radius: 12px–16px`. Buttons use `border-radius: 50px` (pill). Nothing in this UI has a sharp corner.

**Elevation Hierarchy:**
- Default card: standard dual-shadow (raised)
- Active/selected card: inverted shadow (pressed-in) to signal selection state
- Modal/overlay: elevated card with increased shadow multiplier

**Featured Dark Card (e.g., Onboarding Task block):**
Filled with Midnight Sapphire (`#1C3B68`). All text inside is white. Shadow is softened and shifted to a dark-on-dark version: `box-shadow: 5px 5px 15px rgba(10, 20, 40, 0.4)`. This card breaks the monochromatic rhythm and draws the eye as the primary task surface.

### Inputs / Forms

**Text Inputs:**
No visible stroke border in resting state. Instead, the input field is styled as a Neumorphic-pressed (inward) well using an *inverted* dual-shadow:

```css
box-shadow:
  inset 3px 3px 7px rgba(166, 180, 200, 0.5),
  inset -3px -3px 7px rgba(255, 255, 255, 0.85);
```

Background: Pure Chalk. Placeholder text in Whisper Gray. Focused state: adds a 1.5px Cobalt Pulse (`#2563EB`) inner ring overlay using `outline` or pseudo-border to signal active editing without heavy stroke.

**Dropdown / Select:**
Same surface as inputs. Chevron icon in Cloud Detail (`#64748B`).

### Progress Indicators

**Linear Progress Bar:**
Thin track (height `6px`) in Glacial Mist (`#EAF0F8`) or a very light inset-shadow channel. Fill in Cobalt Pulse (`#2563EB`), with a subtle radiant glow: `filter: drop-shadow(0 0 4px rgba(37, 99, 235, 0.4))`. Rounded end-caps (`border-radius: 50px`).

**Circular / Arc Progress:**
SVG-based ring. Track stroke in softened gray (`#D1DCE8`). Progress stroke in Cobalt Pulse. Uses `stroke-dasharray` and `stroke-dashoffset` for animation. The ring itself sits within a circular card widget following the same Neumorphic card styling.

### Badges / Chips / Tags

Small, pill-shaped (`border-radius: 50px`). Backgrounds are light tints of the semantic color (e.g., a light blue-tint chip for "In Progress"). Text is the deeper shade. Never use flat, high-saturation fills for chips — always tinted. Font: SemiBold, `letter-spacing: 0.04em`, small size (`11–12px`).

---

## 5. Layout Principles

**Grid:** 12-column base. Dashboard sections typically split into: 1 narrow sidebar (~220px fixed) + main content area. Within main content: cards span either full-width, half-width (2-col), or 1/3 (3-col) depending on content density.

**Whitespace Strategy:** Generous and intentional. Minimum `24px` padding inside all cards. Between card components: `20px–28px` gap. Section vertical rhythm follows an `8px` base unit (e.g., `16, 24, 32, 48px` spacings).

**Visual Hierarchy Flow:**
1. Dark featured card / primary task block — highest visual weight
2. Metric / tracker cards — secondary reading priority
3. List and table sections — supporting detail
4. Navigation sidebar — ambient, not competing

**Alignment:** Left-aligned primary content. Numbers in metric cards are right-aligned or centered depending on widget type. Section titles maintain consistent left edge with card padding.

**Responsive Behavior:** At narrower viewports, the sidebar collapses to a bottom navigation bar. Cards stack vertically. The Neumorphic shadow values remain unchanged — they do not need to scale with breakpoints.

**Spacing Philosophy:** The design does not use borders to define zones. Instead, whitespace + shadow + background contrast carry all spatial division duties. Every region should feel like it has room to breathe — content never touches the edge of its container.

---

## 6. Motion & Interaction Principles

**Core Feel:** Interactions feel like gently pressing soft material — not mechanical clicks, but tactile depressions.

**Hover States:**
- Raised cards: subtle scale `transform: scale(1.015)` + increased shadow spread
- Buttons: `scale(1.02)` + shadow amplification
- Navigation items (inactive): background tints to a very light Glacial Mist fill

**Click / Active States (Neumorphic Press):**
The most characteristic motion in this system. When pressing a raised button or card, the dual outward shadow transitions to an inward (inset) shadow over `100–150ms`:

```css
/* Raised */
box-shadow: -5px -5px 12px rgba(255,255,255,0.9), 5px 5px 12px rgba(166,180,200,0.45);
/* Pressed */
box-shadow: inset 3px 3px 8px rgba(166,180,200,0.5), inset -3px -3px 8px rgba(255,255,255,0.85);
```

Transition: `box-shadow 120ms ease, transform 120ms ease`

**Progress Animations:**
Progress bars and arc trackers animate their fill on mount with an `ease-out` curve over `600–800ms`. This communicates "live data" and draws the eye on load.

**Page/Section Entrance:**
Cards fade and slide up `8px → 0px` with `opacity 0 → 1` over `300ms`, staggered at `60ms` per card. Keeps the load feel smooth without being theatrical.

---

## 7. Neumorphic Shadow Reference (Implementation)

The soul of this design system lives in these two CSS patterns. Apply them consistently.

### Raised Element (Default Embossed Card/Button)
```css
background: #FFFFFF;
border-radius: 20px;
box-shadow:
  -6px -6px 14px rgba(255, 255, 255, 0.90),
   6px  6px 14px rgba(166, 180, 200, 0.45);
```

### Pressed / Inset Element (Input fields, Active selection)
```css
background: #FFFFFF;
border-radius: 20px;
box-shadow:
  inset 4px  4px 10px rgba(166, 180, 200, 0.50),
  inset -4px -4px 10px rgba(255, 255, 255, 0.88);
```

### Dark Variant Card (Midnight Sapphire surface)
```css
background: #1C3B68;
border-radius: 24px;
box-shadow:
  -4px -4px 10px rgba(255, 255, 255, 0.06),
   6px  6px 16px rgba(10,  22, 50,  0.50);
```

> **Critical rule:** The background color of the page (`#EAF0F8`) and the card (`#FFFFFF`) *must* maintain enough contrast for the white highlight shadow to be visible. If both surfaces are pure white, the Neumorphic effect collapses. The cool-tinted page background is not decorative — it is structurally essential.
