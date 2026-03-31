# Design System Specification: Lumen Syntax (The Technical Editorial)

## 1. Overview & Creative North Star
**Creative North Star: "The Architectural Librarian"**

The "Lumen Syntax" design system is built for high-precision technical documentation. It rejects the cluttered, utility-first aesthetics of traditional documentation for a layout that feels curated, editorial, and architecturally sound. It prioritizes expansive negative space, high-contrast typography, and a "Tonal Layering" approach to hierarchy.

---

## 2. Visual Foundation

### 2.1 Color Palette
- **Primary (Action/Brand):** `#0D9488` (Teal 700) - Used for primary CTAs, active states, and brand accents.
- **Surface (Backgrounds):**
  - `Surface-Main`: `#FFFFFF` (White)
  - `Surface-Container-Low`: `#F8FAFC` (Slate 50) - Used for sidebars and secondary containers.
  - `Surface-Container-High`: `#F1F5F9` (Slate 100) - Used for subtle highlights and search inputs.
- **Text (Content):**
  - `Headline/Body-Emphasis`: `#0F172A` (Slate 900)
  - `Body-Standard`: `#334155` (Slate 700)
  - `Caption/Metadata`: `#64748B` (Slate 500)
- **Syntax/Accents (Code & Diagrams):**
  - `Accent-1`: `#00685F` (Deep Teal)
  - `Accent-2`: `#89F5E7` (Soft Mint)
  - `Warning/Alert`: `#991B1B` (Red 800)

### 2.2 Typography
- **Headings:** `Space Grotesk` (Bold/Medium)
  - *Rationale:* A geometric sans-serif that feels technical yet modern. High-impact for architectural clarity.
- **Body & Navigation:** `Inter` (Regular/Medium)
  - *Rationale:* Exceptional legibility at small sizes, perfect for dense documentation and UI labels.
- **Monospace:** `JetBrains Mono` or `Fira Code`
  - *Rationale:* High-clarity code presentation with clear distinction between characters.

---

## 3. Core Design Principles

### 3.1 Tonal Layering
Instead of relying on borders or heavy shadows, depth is achieved through "Tonal Shifts." 
- **Example:** A `#F8FAFC` sidebar sits adjacent to a `#FFFFFF` main content area without a divider line. This creates a "breathable" interface.

### 3.2 Progressive Complexity
Information is revealed in stages.
- **Tier 1:** High-level summary/overview.
- **Tier 2:** Structured headings and pull-quotes.
- **Tier 3:** Deep-dive code blocks and detailed diagrams.

### 3.3 Intentional Asymmetry
Layouts should feel balanced but not necessarily symmetrical. Use generous margins and staggered content alignment to guide the user's eye naturally through the technical narrative.

---

## 4. Component Standards

### 4.1 Side Navigation (SideNavBar)
- **Structure:** Vertical list with icon + label.
- **Active State:** Rounded-full pill background (`#89F5E7`) with dark teal text.
- **Hierarchy:** Use sub-indentation for module sections (e.g., Foundations -> Color Theory).

### 4.2 Top Navigation (TopNavBar)
- **Structure:** Brand on the left, primary navigation links centered, search and utility (Dark Mode/Global) on the right.
- **Style:** Minimal, fixed-top, using a subtle glassmorphism effect (`backdrop-blur-xl`).

### 4.3 Code Blocks
- **Theme:** Dark Mode (`#1E293B`) even in Light Mode layouts to provide a clear visual break for technical content.
- **Header:** Include a small "file tag" (e.g., `TAILWIND.CONFIG.JS`) and window controls (dots) for a desk-like feel.

---

## 5. Visual & Diagramming Standards (Mermaid.js / SVG)

### 5.1 Flowcharts
- **Nodes:** Minimalist boxes with rounded corners (`rounded-md`).
- **Connectors:** Thin slate lines (`#475569`) with small arrowheads.
- **Color Logic:** 
  - `Primary`: Teal fill for main actions.
  - `Secondary`: Light gray for passive steps.
  - `Status`: Green/Red for Success/Error gates.

### 5.2 Sequence Diagrams
- **Actors:** Small minimalist icons above labels.
- **Messages:** Horizontal teal lines with clear semantic labeling.

### 5.3 UML Class Diagrams
- **Style:** Flat, no shadows. Horizontal dividers for attributes and methods. One-pixel borders for technical precision.

---

## 6. Implementation Notes for Claude
- **CSS Strategy:** Use Tailwind CSS utility classes.
- **Spacing Scale:** Strict adherence to a 4px grid.
- **Interactions:** Subtle scale transitions (`scale-98`) on click and smooth opacity shifts on hover.
