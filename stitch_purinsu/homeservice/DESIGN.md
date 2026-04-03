# Design System Strategy: The Kinetic Architect

## 1. Overview & Creative North Star

This design system is built to convey "The Kinetic Architect"—a philosophy where high-speed AI automation meets meticulous human craftsmanship. We are moving away from the "template-heavy" look of standard SaaS platforms. Instead, we are leaning into a **High-End Editorial** aesthetic that treats the screen like a digital broadsheet.

The visual identity is defined by **Intentional Asymmetry** and **Tonal Depth**. We prioritize breathing room (whitespace) to signal luxury, and we use high-contrast typography scales to establish an immediate, authoritative hierarchy. Elements should feel like they are floating in a pressurized, dark void, layered with precision.

## 2. Colors & Surface Philosophy

The color palette is rooted in a deep, nocturnal foundation, punctuated by "surgical" accents.

### The Foundation
- **Background (`#0e1322`):** Our true dark navy base.
- **Surface Tiers:** Use `surface_container_low` through `highest` to create logical groupings. 
- **Primary Accent (`#c8f135`):** This is your "Electric Lime." It represents action, energy, and intelligence. Use it sparingly to guide the eye.
- **Secondary Accent (`#38bdf8`):** The "Cool Electric Blue." Reserved for data visualization, subtle status indicators, and background glows.

### Core Visual Rules
- **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. To separate content blocks, use background color shifts (e.g., placing a `surface_container_low` card on a `background` section). 
- **The Glass & Gradient Rule:** For floating elements like navigation bars or floating action buttons, use "Glassmorphism." Apply a semi-transparent `surface_variant` color with a `backdrop-filter: blur(20px)`. 
- **Signature Textures:** Main CTAs should not be flat. Use a subtle linear gradient from `primary` (#ffffef) to `primary_container` (#c8f135) at a 135-degree angle to provide a "metallic" high-end sheen.

## 3. Typography: The Editorial Voice

We utilize a three-font system to balance technical precision with modern elegance.

| Level | Font Family | Character | Usage |
| :--- | :--- | :--- | :--- |
| **Display** | **Space Grotesk** | Aggressive, Technical | Hero statements and massive section headers. |
| **Headline** | **Space Grotesk** | Confident, Sharp | Page titles and primary card headers. |
| **Body** | **Plus Jakarta Sans** | Fluid, Approachable | Long-form descriptions and UI labels. |
| **Labels** | **Manrope** | Mathematical, Clean | Micro-copy, metadata, and technical specs. |

**Scale Tip:** Use `display-lg` (3.5rem) with a tight `letter-spacing: -0.04em` to create a dense, "boutique agency" impact. Conversely, body text should be `body-md` (0.875rem) with a generous line-height (1.6) to ensure readability against the dark background.

## 4. Elevation & Depth: Tonal Layering

In this design system, depth is a matter of light and material, not structural lines.

- **The Layering Principle:** Stacking determines importance.
    - Level 0: `background` (The foundation)
    - Level 1: `surface_container_low` (In-page sections)
    - Level 2: `surface_container_high` (Cards and content blocks)
    - Level 3: `surface_bright` (Floating elements/Modals)
- **Ambient Shadows:** Shadows must feel like natural light dispersion. Use a `12%` opacity version of `#000000` with a large blur (32px to 64px) and an Y-offset of 16px. Never use grey shadows; they muddy the navy foundation.
- **The "Ghost Border":** If a container requires a border for accessibility, use the `outline_variant` token at **15% opacity**. This creates a "glint" on the edge rather than a hard cage.

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary_container`). Black text (`on_primary`). No border. Roundedness: `md` (0.375rem).
- **Secondary:** Semi-transparent `secondary_container` with a `Ghost Border`. Text color: `secondary`.
- **Tertiary:** Text-only in `primary_fixed`, featuring a 1px underline that expands on hover.

### Cards
- **Construction:** No dividers. Use `title-md` for headers and `body-sm` for descriptions. 
- **Interaction:** On hover, a card should shift from `surface_container_high` to `surface_container_highest` and gain a subtle `Electric Blue` outer glow (4px blur).

### Input Fields
- **Default:** `surface_container_lowest` background. 
- **Active State:** The bottom edge receives a 2px `primary_container` (Lime) line. Avoid boxing in the entire input; keep it open and airy.

### Data Chips
- Use `manrope` for the text. Background: `surface_variant` at 30% opacity. For "Active" states, use a solid `secondary_container` (Electric Blue) with white text.

### Feature Component: The "Neural Pulse"
Unique to this system: Use a large, blurred radial gradient (30% opacity `secondary`) that follows the mouse cursor behind the content layer. This creates a sense of "active intelligence" within the interface.

## 6. Do's and Don'ts

### Do
- **Embrace Asymmetry:** Align text to the left but place supporting imagery or data points off-center to the right.
- **Use "Electric Lime" as a Surgical Tool:** Use it for the one thing you want the user to click, and nowhere else in that viewport.
- **Micro-interactions:** Elements should "lift" (shift upward by 4px) when interacted with, utilizing a `cubic-bezier(0.2, 0.8, 0.2, 1)` easing for a snappy, premium feel.

### Don't
- **Don't use Divider Lines:** If you feel the need for a line, increase your padding by 24px instead.
- **Don't use Pure White (#FFFFFF):** It is too harsh on a navy background. Use `on_surface` (#dee1f7) or `primary` (#ffffef) for a more sophisticated, "ink-on-paper" look.
- **Don't Over-corner:** Stick to `md` (0.375rem) or `lg` (0.5rem) roundedness. Avoid "pill" shapes for anything other than tags or buttons; they look too "consumer" for a high-end agency.