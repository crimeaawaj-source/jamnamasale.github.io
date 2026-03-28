```markdown
# Design System Strategy: The Heritage Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Spice Merchant."** 

We are not building a generic e-commerce template; we are crafting a high-end, editorial experience that feels as rich and tactile as a hand-packed bag of premium saffron. The goal is to bridge the gap between "दादी-नानी" (grandmother's) traditional kitchen and a modern, luxury boutique.

To move beyond the standard grid, this system employs **Intentional Asymmetry**. We break the digital "box" by overlapping high-resolution spice photography with elegant Hindi typography. Surfaces should feel layered—not flat—utilizing a sophisticated tonal hierarchy that mimics the depth of organic textures like coarse turmeric and sun-dried chilies.

## 2. Colors & Tonal Depth

The palette is rooted in the earth: the deep crimson of Kashmiri Mirch, the golden glow of Haldi, and the soft, inviting cream of a muslin spice bag.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders for sectioning or containment. Traditional lines feel clinical and cheap. Instead, define boundaries through:
*   **Background Shifts:** Use a `surface-container-low` (#f7f3eb) section sitting directly against a `background` (#fdf9f1).
*   **Tonal Transitions:** Separate product categories using subtle background shifts rather than dividers.

### Surface Hierarchy & Nesting
Think of the UI as stacked sheets of fine, handmade paper. 
*   **Base:** `surface` (#fdf9f1).
*   **Floating Elements:** Use `surface-container-lowest` (#ffffff) for product cards to make them "pop" against the off-white background.
*   **Sunken Elements:** Use `surface-container-high` (#ece8e0) for search bars or secondary content areas to create a sense of tactile recession.

### The "Glass & Gradient" Rule
To add a "modern" edge to the "traditional" vibe, use **Glassmorphism** for floating navigation or sticky headers. Use `surface` colors at 80% opacity with a `20px` backdrop-blur. 
For primary CTAs, do not use flat colors. Apply a subtle linear gradient from `primary` (#80000a) to `primary-container` (#a31d1d) at a 135-degree angle to provide a velvet-like sheen.

## 3. Typography: The Editorial Voice

The typography is a dialogue between heritage and clarity.

*   **Display & Headlines (Noto Serif):** These are your "hero" moments. Use `display-lg` for evocative brand statements in Hindi. The serif reflects the elegance of old-world spice catalogs.
*   **Body & Titles (Manrope):** A clean, geometric sans-serif that ensures high legibility for product descriptions and prices. It provides the "trustworthy" and "modern" counterpoint to the decorative Hindi headers.

**Intentional Scaling:** Use high contrast between sizes. A `display-md` headline should often sit closely above a `body-sm` description to create an editorial, magazine-like feel.

## 4. Elevation & Depth

We avoid the "Material Design" shadow look in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by stacking. A `surface-container-lowest` card placed on a `surface-container-low` section creates a natural lift.
*   **Ambient Shadows:** If a floating action is required, shadows must be tinted. Use a blur of `32px` with an 8% opacity of `on-surface` (#1c1c17). This mimics natural light passing through a room, not a digital drop shadow.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke (e.g., in high-contrast modes), use `outline-variant` (#e2beba) at **15% opacity**. It should be felt, not seen.
*   **Signature Textures:** Incorporate hand-drawn spice patterns (curry leaves, peppercorns) as subtle SVG masks in the background of `surface-variant` sections.

## 5. Components

### Buttons
*   **Primary:** Roundedness `full`. Gradient of `primary` to `primary-container`. White text. Use `title-sm` for the label to maintain authority.
*   **Secondary:** Roundedness `full`. `outline` color with a `0.35rem` (1.5) horizontal padding. No fill.

### Cards (Product & Story)
*   **Styling:** Forbid divider lines. Use `spacing-6` (2rem) of vertical white space to separate content.
*   **Image Treatment:** Product images should have a `rounded-lg` (1rem) corner radius. Use a subtle `surface-dim` inner shadow on image containers to make products look "embedded" in the page.

### Chips (Spice Levels/Filters)
*   Use `secondary-container` (#fdc003) for active states. The vibrant yellow acts as a "highlight" much like a turmeric stain—bold and intentional.

### Input Fields
*   **Style:** Minimalist. No bounding box. Only a `primary` color bottom border (2px) that animates from the center on focus. Labels use `label-md` in `on-surface-variant`.

### Signature Component: The "Heritage Story" Carousel
An asymmetrical layout where a large, bleeding-edge image of a spice source (e.g., a field of chilies) overlaps a card containing a `headline-sm` in Noto Serif. This breaks the commerce-first flow with a brand-first moment.

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical margins. If the left margin is `spacing-8`, try a right margin of `spacing-12` for editorial sections.
*   **Do** lean into the "Soft Cream" background. Pure white should only be used for the most elevated surfaces (cards/modals).
*   **Do** use the `tertiary` (#543529) color for nutritional information or "origin stories" to evoke the color of fresh cloves and cinnamon.

### Don't:
*   **Don't** use 1px solid black or grey borders. This destroys the "homemade" premium vibe.
*   **Don't** crowd the space. If you think it needs more spice, it actually needs more white space (`spacing-16` or `20`).
*   **Don't** use generic icons. Use hand-drawn, "organic" style iconography that matches the brand logo's weight.
*   **Don't** use harsh transitions. Every interaction should feel like a slow, deliberate "pour"—use `ease-in-out` transitions for all hover states.

---
*Director's Note: Every pixel should feel like it was placed by hand. If it looks like a template, you haven't pushed the tonal layering far enough.*```