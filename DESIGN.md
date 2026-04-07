```markdown
# Design System Document: The Precision Architect

## 1. Overview & Creative North Star
**Creative North Star: "The Architectural Ledger"**

This design system moves away from the static, boxed-in nature of traditional resumes to embrace an editorial, high-end technical aesthetic. It is designed to feel like a premium dossier—authoritative, meticulously organized, and hyper-legible. We achieve this not through lines and borders, but through **intentional negative space** and **tonal layering**.

The "Architectural Ledger" look relies on a sophisticated tension between the technical precision of the `Inter` typeface and the wider, more expressive proportions of `Manrope`. By utilizing asymmetric layouts—where data-heavy technical skills are offset by expansive professional narratives—we create a rhythm that guides a recruiter’s eye through the document with zero friction.

---

## 2. Colors: Tonal Architecture
The palette is a study in "Tech-Slate" and "Precision Blue." We do not use black; we use deep charcoals and muted navies to maintain a softer, more professional contrast ratio.

### The "No-Line" Rule
**Borders are prohibited for sectioning.** To separate a "Professional Experience" block from "Technical Skills," use a background shift. For example, place the primary content on `surface` (#f7f9fb) and use a `surface-container-low` (#f0f4f7) sidebar or header. Boundaries are felt through color transitions, not drawn with lines.

### Surface Hierarchy & Nesting
Treat the resume as a series of physical layers:
*   **Base Layer:** `background` (#f7f9fb) – The canvas.
*   **Content Blocks:** `surface-container-lowest` (#ffffff) – Used for high-priority cards like "Project Highlights."
*   **Structural Accents:** `surface-container-high` (#e1e9ee) – Used for subtle grouping of skill tags or metadata.

### The "Glass & Gradient" Rule
For digital-first views, use a subtle gradient for the header: `secondary` (#005bc4) transitioning to `secondary_dim` (#004fad) at a 135-degree angle. This adds "soul" to the technical profile. To elevate floating elements (like a "Contact Me" fab), apply a backdrop-blur of 12px with a semi-transparent `surface_container_lowest` at 80% opacity.

---

## 3. Typography: Editorial Hierarchy
We utilize a dual-font system to balance "Human" (Manrope) and "Technical" (Inter) attributes.

*   **Display & Headlines (Manrope):** Use `display-md` for the candidate's name. The wide tracking of Manrope conveys confidence. 
    *   *Directorial Note:* Set `headline-sm` in Semi-Bold for section titles to create an immovable anchor for the eye.
*   **Titles & Body (Inter):** Use `title-md` for Job Titles and `body-md` for descriptions. Inter’s tall x-height ensures that even dense technical bullet points remain breathable.
*   **Labels (Inter):** Use `label-md` in `on_surface_variant` (#566166) for metadata like dates or locations. This creates a clear visual distinction between *what* you did and *when* you did it.

---

## 4. Elevation & Depth: Tonal Layering
Traditional resumes feel "flat." We create depth through **Ambient Shadows** and **Ghost Borders**.

### The Layering Principle
Instead of a shadow, place a `surface-container-lowest` card on top of a `surface-container` background. The slight delta in hex value creates a "soft lift."

### Ambient Shadows
If a floating element is required (e.g., a "Download PDF" button), use:
*   **Blur:** 24px
*   **Spread:** -4px
*   **Color:** `on_surface` (#2a3439) at 6% opacity.
This mimics natural light rather than a "computer-generated" drop shadow.

### The "Ghost Border" Fallback
If contrast is needed for accessibility, use the "Ghost Border": `outline-variant` (#a9b4b9) at **15% opacity**. It provides a suggestion of a container without breaking the editorial flow.

---

## 5. Components

### Buttons (CTAs)
*   **Primary:** `secondary` (#005bc4) fill with `on_secondary` (#f9f8ff) text. Use `md` (0.375rem) roundedness for a modern, slightly sharp tech feel.
*   **Secondary:** `surface-container-high` fill with `on_surface`. No border.

### Skill Chips
*   **Selection Chips:** Use `secondary_container` (#d8e2ff) with `on_secondary_container` (#004eaa). 
*   **Shape:** `full` (9999px) pill shape.
*   **Styling:** Remove all borders. The color fill is the only boundary.

### Experience Cards
*   **Rule:** Forbid divider lines between jobs. 
*   **Execution:** Use 32px of vertical white space (Spacing Scale) between roles. Use a `surface-variant` (#d9e4ea) vertical accent bar (4px wide, `sm` roundedness) to the left of the "Current Role" to signify active status.

### Input Fields (For Contact Forms)
*   **Default:** `surface-container-lowest` fill, 1px "Ghost Border" (15% opacity).
*   **Active:** Transition border to `secondary` (#005bc4) at 100% opacity.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use `secondary_fixed_dim` (#c3d4ff) for subtle background highlights behind key technical keywords (e.g., "React," "AWS").
*   **Do** embrace asymmetry. A wide left column for experience and a narrow right column for skills creates a high-end layout.
*   **Do** use `primary` (#545f73) for body text to reduce eye strain compared to pure black.

### Don't:
*   **Don't** use 1px solid black or grey lines to separate sections. It looks like a spreadsheet, not a professional profile.
*   **Don't** use standard "Inter" for everything. If there is no font weight/size contrast, the visual hierarchy collapses.
*   **Don't** use high-saturation reds for error states. Use `error` (#9f403d) and `error_container` (#fe8983) for a more sophisticated, "muted-pro" alert system.

---

## 7. ATS Optimization Note
While this system uses sophisticated visual layering, the **DOM order** must remain linear. Ensure that even though elements may visually overlap or sit in asymmetric columns, the underlying code reads: `Header > Profile > Experience > Skills` to ensure 100% compatibility with Applicant Tracking Systems.```