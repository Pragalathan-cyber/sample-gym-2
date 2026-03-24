```markdown
# Design System Strategy: Kinetic Friction

### 1. Overview & Creative North Star
**Creative North Star: "Kinetic Friction"**
This design system moves away from the "friendly fitness" aesthetic and leans into the raw, uncompromising world of high-performance athletics. It is built on the concept of **Kinetic Friction**—the energy generated when heavy elements collide. We achieve this through a "Digital Brutalist" lens: massive typography, zero-radius corners, and a high-contrast palette that mimics the heat of an intense workout.

This is not a template; it is a visual manifesto. We break the grid through intentional asymmetry—overlapping text over imagery and using "Inference Orange" as a spotlight rather than a mere accent. The layout should feel like a high-end sport editorial: raw, urgent, and professional.

---

### 2. Colors
Our palette is anchored by the void of the gym floor and the heat of the "Inferno."

*   **Primary (Inferno):** Use `primary` (#ff8f70) and `primary_container` (#ff7852) to signify action, heat, and intensity.
*   **Neutrals:** The background is a deep, monolithic `surface` (#0e0e0e). Hierarchy is defined by "heat" (brightness) rather than borders.

**The "No-Line" Rule**
Traditional 1px borders are strictly prohibited. They feel "app-like" and cheap. Instead, define boundaries through background shifts. A `surface_container_low` (#131313) card should sit on a `surface` (#0e0e0e) background. The shift is felt, not seen as a line.

**Surface Hierarchy & Nesting**
Treat the UI as a series of stacked, monolithic slabs. 
*   **Base:** `surface`
*   **Sectioning:** `surface_container_low`
*   **Interactive Elements:** `surface_container_high`
This nesting creates a "carved" look, as if the interface was milled from a single block of charcoal.

**The "Glass & Gradient" Rule**
To prevent the UI from feeling "flat," use `primary` to `primary_container` gradients on hero CTAs to simulate glowing embers. Use **Glassmorphism** (backdrop-blur: 20px) with 40% opacity `surface_variant` for floating navigation bars to maintain the "Industrial" look while adding depth.

---

### 3. Typography
We use **Lexend** exclusively. Its geometric clarity provides a technical, engineered feel that balances the raw brutalism of the layout.

*   **Display (The Hammer):** `display-lg` and `display-md` should be used with tight letter-spacing (-0.05em). These are your "shouting" moments—workout titles, heavy PRs, and hero slogans.
*   **Headlines (The Instruction):** `headline-lg` is for high-level navigation and section headers.
*   **Body (The Detail):** `body-lg` provides a readable but sturdy voice for descriptions.
*   **Labels (The Data):** `label-md` should be used for technical specs (weight, sets, reps), often paired with all-caps for a "technical blueprint" feel.

The typography is the primary architecture of the layout. Don't be afraid to let a `display-lg` title bleed off the edge of the container.

---

### 4. Elevation & Depth
In this system, depth is a product of **Tonal Layering**, not structural shadows.

*   **The Layering Principle:** Physicality is achieved by stacking. Place `surface_container_highest` (#262626) elements on top of `surface_dim` (#0e0e0e) to create a natural, "lit from above" hierarchy.
*   **Ambient Shadows:** If an element must float (e.g., a modal), use an ultra-diffused shadow. 
    *   *Spec:* `0px 20px 50px rgba(0, 0, 0, 0.5)`. No hard drop shadows.
*   **The "Ghost Border" Fallback:** For accessibility in input fields, use `outline_variant` at 20% opacity. This provides a "hint" of a boundary without breaking the brutalist flow.
*   **Hard Edges:** The Roundedness Scale is strictly `0px`. Everything is a sharp corner. This conveys precision and uncompromising performance.

---

### 5. Components

*   **Buttons:**
    *   *Primary:* `primary` background, `on_primary` text. Rectangular, no radius. High-energy.
    *   *Secondary:* `surface_container_highest` background with `on_surface` text.
    *   *Interaction:* On hover, buttons should shift to a subtle gradient of `primary` to `primary_fixed_dim`.
*   **Chips:**
    *   Use `surface_variant` for inactive chips. Use `primary_container` for active states. Use `label-md` typography.
*   **Input Fields:**
    *   Background: `surface_container_low`. 
    *   Border: None. 
    *   Focus State: A 2px bottom-bar of `primary`.
*   **Cards:**
    *   No dividers. Use `surface_container_high` on a `surface` background. Use `spacing-8` (2.75rem) to separate content chunks internally.
*   **Progress Bars (The "Heat" Bar):**
    *   Background: `surface_container_highest`. 
    *   Fill: A gradient from `primary` to `secondary`.
*   **Data Grids:**
    *   For workout logs, use raw typography alignment. Use `surface_container_low` for alternating rows (zebra striping) instead of divider lines.

---

### 6. Do’s and Don’ts

**Do:**
*   **Do** use massive, overlapping typography for hero sections.
*   **Do** use the full range of `surface-container` tokens to create depth.
*   **Do** use `0px` border-radius on every single element.
*   **Do** use white space (`spacing-16` or `spacing-20`) as a structural element to allow the "Inferno Orange" to breathe.

**Don’t:**
*   **Don’t** use shadows to define cards; use background color shifts.
*   **Don’t** use 1px solid borders for sectioning.
*   **Don’t** use rounded corners, even for "soft" elements like tooltips.
*   **Don’t** use thin font weights. Stay within the Medium to ExtraBold range of Lexend to maintain the "Power" vibe.
*   **Don’t** use icons as the primary way to communicate; let the bold typography lead. Icons should be "Technical/Utility" style only.

---
**Director's Note:** Every pixel should feel like it was built to withstand a 500lb deadlift. If a component feels "delicate," it doesn't belong here. High contrast. High energy. No compromises.```