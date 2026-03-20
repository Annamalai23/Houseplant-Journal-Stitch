# Design System Document: The Living Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Greenhouse."** 

We are moving away from the rigid, sterile grids of traditional utility apps. Instead, we are building an experience that feels like flipping through a high-end botanical journal. The layout must feel organic and "alive," utilizing intentional asymmetry, breathing room (negative space), and overlapping elements to mimic the layered growth of a forest floor. This system rejects the "boxed-in" look of standard mobile UI in favor of tonal depth and editorial elegance.

---

## 2. Colors: Botanical Depth
Our palette is rooted in the natural world, moving from deep chlorophyll greens to sun-baked terracotta.

### The "No-Line" Rule
**Strict Prohibition:** Designers are forbidden from using 1px solid borders to section content. Boundaries must be defined solely through background color shifts. Use `surface-container-low` (#f5f3ef) to define a section against a `surface` (#fbf9f5) background. If a container needs to stand out, use a tonal shift, never a stroke.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine paper. 
- **Base Level:** `surface` (#fbf9f5)
- **Secondary Content:** `surface-container-low` (#f5f3ef)
- **Interactive Cards:** `surface-container-lowest` (#ffffff) to create a subtle "pop" of clean white.
- **Deep Insets:** `surface-container-high` (#eae8e4) for recessed search bars or footer areas.

### The "Glass & Gradient" Rule
To elevate the "Organic" feel, use Glassmorphism for floating navigation bars or modal headers. Use `surface` at 80% opacity with a `20px` backdrop blur. For primary CTAs, apply a subtle linear gradient from `primary` (#154212) to `primary-container` (#2d5a27) at a 135° angle to add "soul" and dimension.

---

## 3. Typography: The Modern Herbalist
We pair a sophisticated serif with a highly legible sans-serif to bridge the gap between "Traditional Botany" and "Modern Technology."

*   **Display & Headlines (`notoSerif`):** Used for storytelling, plant names, and section headers. The serif conveys authority and warmth. Use `display-lg` (3.5rem) for hero moments with tight tracking (-0.02em) to feel like a magazine cover.
*   **Titles & Body (`plusJakartaSans`):** Used for navigation, labels, and long-form care instructions. This sans-serif provides a clean, neutral balance to the serif’s personality.
*   **Hierarchy Note:** Use `tertiary` (#6e1c0c) for small labels or "Warning" care tips—the soft terracotta provides high contrast without the "alarmist" feel of pure red.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "digital." We achieve depth through light and environment.

*   **The Layering Principle:** Place a `surface-container-lowest` card (Pure White) onto a `surface-container` (#efeeea) background. The change in hex code provides enough "lift" for the eye without structural clutter.
*   **Ambient Shadows:** When an element must float (e.g., a FAB or a detached navigation bar), use an ultra-diffused shadow: `Offset: 0, 8px | Blur: 24px | Color: #1b1c1a at 4% opacity`.
*   **The "Ghost Border" Fallback:** If accessibility requires a container edge, use `outline-variant` (#c2c9bb) at **15% opacity**. It should be felt, not seen.

---

## 5. Components: Soft & Approachable
All components leverage the **Roundedness Scale**, specifically `md` (1.5rem) and `lg` (2rem), to eliminate "sharp" edges.

### Buttons
*   **Primary:** Gradient from `primary` to `primary-container`. Corner radius `full`. Typography: `title-sm` (White).
*   **Secondary:** Background `secondary-container` (#fdcdbc). Typography: `on-secondary-container` (#795548). No border.
*   **Tertiary:** No background. `primary` text with an icon.

### Cards & Lists
*   **Rule:** Forbid divider lines. 
*   **Implementation:** Separate list items using `spacing-4` (1.4rem). For specialized plant cards, use `surface-container-low` with a `lg` (2rem) corner radius. Use asymmetrical image cropping (e.g., top-left corner `xl`, bottom-right corner `md`) to create a custom, high-end feel.

### Input Fields
*   **Style:** Use "Pill" shapes (`full` roundedness).
*   **Color:** `surface-container-high` background.
*   **Focus State:** Shift background to `surface-container-lowest` and add a soft 2px "Ghost Border" using `primary` at 20% opacity.

### Featured Component: "The Growth Progressor"
A bespoke slider for tracking plant growth. Use a `primary-fixed` (#bcf0ae) track with a `primary` (#154212) thumb shaped like a soft leaf (use the `lg` radius).

---

## 6. Do’s and Don’ts

### Do
*   **Do** use asymmetrical spacing. Align text to the left but allow images to "bleed" off the right edge of the screen to create movement.
*   **Do** use `secondary_fixed` (#ffdbcf) for background highlights behind plant photography to make greens pop.
*   **Do** use the `12` (4rem) and `16` (5.5rem) spacing tokens to create "Breathing Rooms" between major content blocks.

### Don’t
*   **Don’t** use pure black (#000000). Always use `on-surface` (#1b1c1a) for text to maintain a soft, organic contrast.
*   **Don’t** use `none` or `sm` corner radius. Sharp corners break the "approachable" brand promise.
*   **Don’t** stack more than three levels of surface containers. It leads to visual "muddiness." Keep the hierarchy shallow and clean.
*   **Don’t** use standard "Material Blue" for links. Use `tertiary` (#6e1c0c) for a sophisticated, earthy alternative.