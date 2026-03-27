```markdown
# Design System Strategy: The Automated Architect

## 1. Overview & Creative North Star
The design system is built for an Automation Specialist who operates at the intersection of technical precision and seamless execution. The Creative North Star for this system is **"The Digital Schematic."**

We are moving away from the "generic SaaS" look of cluttered dashboards and toward a high-end editorial experience. This design system treats the UI as a living network: precise, interconnected, and expansive. We break the rigid, boxed-in "template" feel by utilizing intentional asymmetry, expansive whitespace, and a sophisticated layering of tonal surfaces rather than structural lines. The goal is to make the user feel like they are interacting with a high-performance engine that has been polished into a work of art.

## 2. Colors & Surface Logic
The palette is a deep, obsidian-based spectrum anchored by a technical gold accent. This is not just a "Dark Mode"; it is a curated environment designed to reduce eye strain and highlight premium content.

### The "No-Line" Rule
To achieve a high-end editorial feel, **1px solid borders are strictly prohibited for sectioning.** Conventional dividers create visual noise. Instead, boundaries must be defined through:
- **Background Color Shifts:** Use a `surface-container-low` section sitting against a `surface` background.
- **Tonal Transitions:** Define areas using subtle changes between `surface-container` tiers (Lowest to Highest).

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of smoked glass. 
- Use `surface-container-lowest` (#0e0e11) for the deep background.
- Use `surface-container` (#1f1f22) for primary content blocks.
- Use `surface-container-highest` (#353438) for interactive elements like hover states or nested cards.
This nesting creates a "natural lift" that feels architectural rather than flat.

### The Glass & Gradient Rule
Floating elements (modals, dropdowns, navigation) should utilize a **Glassmorphism** effect. Apply `surface-container` with a 70-80% opacity and a 20px backdrop-blur. 
For primary calls to action, use a **Signature Texture**: a linear gradient from `primary` (#f9c068) to `primary-container` (#dba550) at a 135-degree angle. This provides a tactile "soul" that a flat hex code cannot achieve.

## 3. Typography
The typography strategy bridges the gap between technical documentation and premium branding.

- **Display & Headlines (Space Grotesk):** This typeface is our "Technical Signature." Its geometric rigor reflects the automation aspect. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero sections to create an authoritative, editorial impact.
- **Body & Titles (Manrope):** We use Manrope for all functional reading. Its humanist qualities balance the coldness of the grid. 
- **The Hierarchy Philosophy:** We use high-contrast scales. A massive `display-lg` headline should be paired with a much smaller, widely-spaced `label-md` (#71717A) to create a sense of scale and breathing room.

## 4. Elevation & Depth
In this design system, elevation is conveyed through **Tonal Layering** rather than traditional structural shadows.

- **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section to create a soft, recessed depth. The eye perceives the shift in value as a change in physical plane.
- **Ambient Shadows:** When a floating effect is required (e.g., a primary card or modal), shadows must be extra-diffused. Use a blur of 40px-60px with an opacity of 6%. The shadow color must be a tinted version of the background (#000000 at 40%), never a generic grey.
- **The Ghost Border Fallback:** If a border is required for accessibility, use the "Ghost Border" technique: `outline-variant` (#504537) at 15% opacity. It should be felt, not seen.
- **Motion-Integrated Depth:** As users scroll, use slight parallax on different surface tiers to reinforce the idea of stacked layers.

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary-container`), `md` (0.75rem) roundedness. Text is `on-primary` (#442c00), bold.
- **Secondary:** Ghost style. No fill, `outline-variant` Ghost Border. On hover, transition to `surface-container-high`.
- **Tertiary:** Text-only with an animated underline that expands from the center on hover.

### Cards
Cards must use the `xl` (1.5rem) roundedness scale. **Never use dividers inside a card.** Separate the header, body, and footer using the Spacing Scale (e.g., `8` (2.75rem) gap between sections). Use a background of `surface-container-low` against the main `surface`.

### Chips & Nodes
Given the "Automation" and "Network" aesthetic, chips should look like data points. Use `label-sm` typography, `full` roundedness, and a `surface-container-highest` background. For active "nodes," use a 4px `primary` dot next to the text.

### Input Fields
Inputs should feel like part of the surface. Use `surface-container-lowest` with a bottom-only Ghost Border. Focus states should not change the border color to a thick line; instead, increase the background brightness to `surface-container-high`.

### Custom Component: The Connection Path
To lean into the "Automation Specialist" persona, use subtle SVG "paths" (light strokes of `outline-variant` at 10% opacity) that occasionally "connect" cards or sections, mimicking a node-based workflow or circuit board.

## 6. Do's and Don'ts

### Do
- **Embrace Asymmetry:** Align a small technical label to the far right while the headline sits on the left.
- **Use "Optical" Spacing:** Use the `20` (7rem) and `24` (8.5rem) spacing tokens for top/bottom section padding. Give the content room to breathe.
- **Tint your Grays:** Ensure all neutral tones have a slight warmth/brown tint to match the gold `primary` accent.

### Don't
- **Don't use 100% White:** For body text, use `on-surface-variant` (#d4c4b2) to maintain a premium, subdued feel. Reserve `#FFFFFF` for high-impact headlines only.
- **Don't use Box Shadows on everything:** Only one "Hero" element per screen should have a shadow. Everything else stays flat through tonal layering.
- **Don't crowd the Grid:** If a component feels tight, increase the spacing by two increments on the scale. Accessibility and luxury both require space.

---
*Note: This design system is a living document. It prioritizes the "feel" of a bespoke, high-end experience over the rigid constraints of a generic UI library.*```