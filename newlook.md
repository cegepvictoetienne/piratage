# Design System – Lumen Syntax

Instructions for applying this look to a MkDocs Material site via `docs/css/extra.css`.

---

## Colour Palette

```css
:root {
  --ls-primary:        #0D9488;   /* teal */
  --ls-primary-dark:   #00685F;
  --ls-accent:         #89F5E7;   /* mint */

  --ls-surface-main:   #FFFFFF;
  --ls-surface-low:    #F8FAFC;
  --ls-surface-high:   #F1F5F9;

  --ls-text-headline:  #0F172A;
  --ls-text-body:      #334155;
  --ls-text-caption:   #64748B;

  --ls-alert:          #991B1B;

  --ls-code-bg:        #1E293B;
  --ls-code-header-bg: #0F172A;
}
```

---

## Material Theme Overrides

### Light mode (`default`)

```css
[data-md-color-scheme="default"] {
  --md-primary-fg-color:          #0D9488;
  --md-primary-fg-color--light:   #14B8A6;
  --md-primary-fg-color--dark:    #00685F;
  --md-primary-bg-color:          #FFFFFF;
  --md-accent-fg-color:           #0D9488;
  --md-default-bg-color:          #FFFFFF;
  --md-default-fg-color:          #334155;
  --md-default-fg-color--light:   #64748B;
  --md-default-fg-color--lighter: #94A3B8;
}
```

### Dark mode (`slate`)

```css
[data-md-color-scheme="slate"] {
  --md-primary-fg-color:        #89F5E7;
  --md-primary-fg-color--light: #A7F3D0;
  --md-primary-fg-color--dark:  #0D9488;
  --md-accent-fg-color:         #89F5E7;

  /* Text — must be light for readability */
  --ls-text-headline:  #F1F5F9;
  --ls-text-body:      #CBD5E1;
  --ls-text-caption:   #94A3B8;

  /* Surfaces — must be dark to avoid blinding table rows etc. */
  --ls-surface-main:   #1E293B;
  --ls-surface-low:    #263244;
  --ls-surface-high:   #2E3D52;
}
```

---

## Typography

Fonts: **Space Grotesk** for headings and body, **Inter** as fallback.
Load via MkDocs `extra_css` or Google Fonts.

- h1: 2.25rem, weight 700, line-height 1.15
- h2: 1.6rem, weight 600, bottom border `2px solid var(--ls-surface-high)`
- h3: 1.25rem, weight 600
- All headings: `letter-spacing: -0.02em`, colour `var(--ls-text-headline)`
- Body: `line-height: 1.75`, colour `var(--ls-text-body)`

---

## Top Navigation Bar

Light mint with glassmorphism effect:

```css
.md-header {
  background: rgba(45, 212, 191, 0.88) !important;
  backdrop-filter: blur(20px) saturate(160%);
  box-shadow: 0 1px 0 rgba(255,255,255,0.08), 0 4px 24px rgba(0,0,0,0.12);
}
```

Tabs bar (slightly darker):

```css
.md-tabs {
  background: rgba(20, 184, 166, 0.92);
  backdrop-filter: blur(12px);
}
```

Tab links: Space Grotesk, weight 500, opacity 0.82 → 1 on hover/active.

---

## Sidebar

- Background: `var(--ls-surface-low)`
- Section titles: `var(--ls-surface-high)`
- Active link: mint pill (`background: var(--ls-accent)`, `border-radius: 9999px`, dark text, weight 600)
- Hover: `rgba(137, 245, 231, 0.3)` rounded pill
- All transitions: 0.15s ease

---

## Code Blocks

Dark island style (dark even in light mode):

- Background: `#1E293B`, text `#CBD5E1`
- Border-radius: `0.5rem`
- Box shadow: `0 4px 24px rgba(0,0,0,0.18)`
- macOS-style "traffic light" header bar with three coloured dots (red/yellow/green) via CSS pseudo-element

Inline code (light mode): background `#F1F5F9`, colour `#00685F`, rounded `0.25rem`.

---

## Tables

Flat editorial style:

- Border: `1px solid var(--ls-surface-high)`, border-radius `0.5rem`, no box-shadow
- Header row: `var(--ls-surface-low)` background, Space Grotesk, weight 600, `2px` bottom border
- Alternating even rows: `var(--ls-surface-low)` background

> In dark mode, `--ls-surface-low` is overridden to `#263244` and `--ls-surface-high` to `#2E3D52`, keeping table rows readable without being too bright.

---

## Content Area

```css
.md-grid         { max-width: 100%; }
.md-content__inner { padding: 2rem 2.5rem; max-width: 860px; }
```

---

## Footer

Background: `#0F172A` (same as code block header).

---

## External Link Indicator

A small SVG arrow icon appended after any `<a href="http...">` inside `<article>` via `::after`.

---

## Admonition Custom Types

Two custom types defined with SVG icons:

| Type          | Border / icon colour | Background tint         |
|---------------|----------------------|-------------------------|
| `manuel`      | `#2B9B46` (green)    | `rgba(43,155,70,0.1)`   |
| `codesandbox` | `#AD03FC` (purple)   | `rgba(173,3,252,0.1)`   |

Usage in Markdown: `!!! manuel "Title"` / `!!! codesandbox "Title"`.

---

## Tooltips

Trigger element gets `border-bottom: 1px dotted`. Tooltip: dark background (`#0F172A`), white text, rounded, fades in on hover.

```html
<span class="tooltip">word<span class="tooltiptext">Explanation</span></span>
```
