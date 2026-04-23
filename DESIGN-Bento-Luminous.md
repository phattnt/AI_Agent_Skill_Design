# Design System: Luminous Bento
**Project ID:** 2026-LUMINOUS-BENTO

## 1. Visual Theme & Atmosphere
**Mood:** Premium, Surgical, Weightless, and Hyper-focused.

This design system completely rejects the muddy, cluttered aesthetic of generic templates. Instead, it introduces a "Surgical Canvas" that creates an atmosphere of absolute tranquility. By stripping away heavy, exaggerated drop-shadows, the interface feels completely weightless and frictionless. Physical depth is replaced by strict micro-contrast and striking "luminous intersections"—vibrant, fluid gradients that instantly pull the user’s eye toward high-value actions. It is a masterclass in editorial elegance. Clarity over cleverness.

## 2. Color Palette & Roles
- **Surgical Canvas** (`#F9FAFB`) — The global background tone. A nearly-invisible, ultra-cool off-white that provides the microscopic contrast required to lift pure white components off the floor without shadows.
- **Absolute White** (`#FFFFFF`) — The uncompromising surface color for all Bento cards and containers.
- **Fluid Sapphire** (`Gradient: #1D4ED8 to #3B82F6`) — Used specifically for primary call-to-action buttons and active progress rings. This energetic transition injects life and motion into an otherwise utterly static canvas.
- **Deep Slate Anchor** (`#0F172A`) — The primary text color for large hero metrics and section headings. It radiates deep authority and uncompromising stability.
- **Cloud Detail** (`#64748B`) — The secondary text color. Used for micro-labels, dates, and subordinate data, supporting the main content without ever competing for visual attention.
- **Hairline Delineator** (`#E5E7EB`) — The precise stroke color used exclusively for 1px borders to mathematically carve out the Bento grid.

## 3. Typography Rules
**Font Family Strategy:** Command attention with Geometric Grotesque fonts for displays, grounded by high-legibility Sans-Serif fonts for data bodies.
- **Recommended Pairing:** *Plus Jakarta Sans* (Display) & *Inter* (Body).
- **Weight Usage:**
  - `800 / ExtraBold`: Reserved strictly for Hero statistics and paramount headings. It must roar.
  - `500 / Medium`: Deployed for button labels, actionable links, and primary data points.
  - `400 / Regular`: Standard body copy.
- **Letter-Spacing Character:**
  - Monumental headings: `letter-spacing: -0.03em`. Tight, confident, and dense.
  - Micro-tags and labels: `letter-spacing: 0.05em`. Airy and scannable at small sizes.

## 4. Component Stylings
- **Buttons (Primary CTAs):** Strictly pill-shaped (`border-radius: 9999px`). The background is filled with the *Fluid Sapphire* gradient, maintaining a ruthlessly flat profile with zero external drop-shadows. On hover, the internal gradient accelerates/shifts subtly to signal interactivity without relying on glowing effects.
- **Bento Cards/Containers:** Smooth, friendly curves (`border-radius: 16px to 24px`). Backgrounds are strictly *Absolute White*. Muddy shadows are entirely discarded; cards assert their boundaries via a crisp, 1px *Hairline Delineator* border.
- **Inputs/Forms:** Flat, pill-shaped wells (`border-radius: 9999px`) featuring the same subtle 1px border. Focus states transition the border to a vibrant blue to indicate active editing—eschewing heavy, outdated focus rings.
- **Badges/Tags:** "Ghosted" pills. They utilize an ultra-light translucent background (e.g., 8% opacity) paired with full-strength text of the exact same chromatic hue, creating a seamless "dyed-in" illusion.

## 5. Layout Principles
- **Minimalist Bento Grid:** The architectural soul of this system is a strict, interlocking Bento Box layout. Distinct functional blocks snap into an underlying asymmetric column grid effortlessly.
- **Mathematical Separation:** Delineate Bento cards using mathematically precise, uniform gutters (strictly `16px` or `24px`). Consistent sizing creates a rhythmic, predictable flow of information that reduces cognitive load instantly.
- **Micro-Contrast Structuring:** The global background (`#F9FAFB`) juxtaposed against pure white cards (`#FFFFFF`) ensures every Bento box is structurally distinct. This micro-contrast entirely eliminates the need for spacing "crutches" like shadows.
- **Editorial Whitespace:** Content must never suffocate against the edge of its container. A generous internal padding of at least `24px` within every card ensures that data breathes, remains legible, and feels inherently premium.
