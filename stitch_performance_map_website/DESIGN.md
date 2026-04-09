# Design System: High-End Theatrical Editorial

## 1. Overview & Creative North Star: "The Noir Stage"
This design system is built to evoke the tension, drama, and intimacy of a live theatrical performance. Our Creative North Star is **"The Noir Stage"**—a concept where the interface acts as a darkened theater, using light (color) and space (typography) to direct the user’s eye with the precision of a spotlight. 

To break the "template" look, we move away from rigid, boxed grids. Instead, we embrace **intentional asymmetry** and **tonal layering**. Elements should feel like they are floating in a dark void, occasionally overlapping to create depth. We prioritize the "breath" of the page; large amounts of whitespace (or "blackspace") are not empty—they are moments of dramatic silence.

---

## 2. Colors: Chromatic Spotlights
Our palette is rooted in a deep, obsidian base (`surface: #131313`) punctuated by "electric" highlights that mimic stage lighting.

### The "No-Line" Rule
**Standard 1px borders are strictly prohibited.** Boundaries must be defined solely through background shifts. To separate a section, transition from `surface` to `surface-container-low`. To highlight a feature, use `surface-container-high`. We create structure through "volumes" of color, not lines.

### Surface Hierarchy & Nesting
Treat the UI as a physical stage with depth:
*   **The Void (`surface-container-lowest`):** Use for the deepest background layers or immersive hero sections.
*   **The Floor (`surface`):** The primary canvas for content.
*   **The Podium (`surface-container-high`):** Use for interactive cards or elevated modals.

### The "Glass & Gradient" Rule
To add "soul," use subtle gradients for CTAs. A transition from `primary (#ffafd7)` to `primary-container (#e362ae)` creates a soft, glowing neon effect. For floating navigation or overlays, apply **Glassmorphism**: use `surface-container` at 70% opacity with a `24px` backdrop blur. This allows the dramatic imagery of the performance to bleed through the interface.

---

## 3. Typography: The Script
The typography is a dialogue between the sharp, geometric precision of modernism and the expressive weight of editorial design.

*   **Display & Headlines (Epilogue):** This is our "Lead Actor." It is bold and commanding. Use `display-lg` for performance titles, utilizing tight letter-spacing to create a high-fashion, cinematic feel.
*   **Titles & Body (Manrope):** Our "Supporting Cast." Manrope provides clean, neutral legibility. Use `title-lg` for act descriptions and `body-md` for synopsis text.
*   **Labels (Space Grotesk):** The "Stage Directions." Used for technical data (dates, times, seat numbers). The monospaced lean of Space Grotesk adds a modern, "ticket-stub" utility to the elegant layout.

---

## 4. Elevation & Depth: Tonal Layering
In a world without lines, depth is our only architecture.

*   **The Layering Principle:** Instead of shadows, we stack. A `surface-container-highest` card sitting on a `surface` background creates a natural "lift" that feels integrated into the stage.
*   **Ambient Shadows:** If an element must float (e.g., a ticket booking fab), use a shadow tinted with `primary`. Example: `box-shadow: 0 20px 40px rgba(255, 175, 215, 0.08);`. This mimics the way light spills across a stage floor.
*   **The "Ghost Border" Fallback:** For input fields, if a container is required, use `outline-variant` at **15% opacity**. It should be felt, not seen.
*   **Asymmetric Overlaps:** To break the "webby" feel, allow images to bleed off the edge of the screen or overlap typography, anchored by a `secondary (#75d4e8)` accent chip to pull the eye back to the center.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` background with `on-primary` text. No border. Use `rounded-sm` (0.125rem) for a sharp, architectural look.
*   **Secondary:** A "Ghost Button" using `outline-variant` at 20% opacity. On hover, transition to a subtle `surface-container-highest` fill.
*   **Tertiary:** Pure typography in `secondary` color, all caps, using `label-md` for a "Metadata" feel.

### Cards (The "Performance Frame")
*   **Prohibition:** No dividers or borders.
*   **Style:** Use `surface-container-low`. Content is separated by generous vertical spacing (at least `48px`). The image should be the focal point, using a subtle `primary` inner-glow on hover to signify interactivity.

### Chips (The "Ticket" Variant)
*   Used for genres or dates. Use `surface-container-high` with `secondary` text. Shape: `rounded-none`. The lack of rounding creates a brutalist, modern theatrical feel.

### Input Fields
*   **The Editorial Input:** A single underline using `outline-variant` at 30%. On focus, the underline expands and glows with the `secondary` color. Helper text should always use `label-sm` in `tertiary`.

### Additional Component: "The Spotlight Cursor"
*   In desktop views, implement a custom cursor that acts as a subtle radial gradient of `primary` at 5% opacity, following the mouse. It "lights up" the dark background as the user explores the page.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts. Place a headline on the left and the body text far to the right to create "tension."
*   **Do** use high-contrast imagery. Monochromatic photography with a single splash of `pink` or `blue` works best.
*   **Do** respect the "Blackspace." If the content feels crowded, add more `surface` space.

### Don't:
*   **Don't** use 1px solid borders. It shatters the "Noir Stage" illusion.
*   **Don't** use standard "web" rounding (like 20px). Stick to `sm` (2px) or `none` for a professional, sharp-edged feel.
*   **Don't** use pure white `#FFFFFF` for long-form body text. Use `on-surface-variant` to reduce eye strain against the black background while maintaining high contrast for headlines.