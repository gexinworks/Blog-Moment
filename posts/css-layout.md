---
title: A Guide to Modern CSS Layout
date: 2026-03-18
tags: [CSS, Design, Tutorial]
---

CSS layout has evolved dramatically. If you're still reaching for floats or reaching for a framework by default, it's time to reconsider.

## Flexbox: The One-Dimensional King

Flexbox excels at distributing space along a **single axis**:

```css
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1rem;
}
```

**When to use**: Navigation bars, card rows, centering, any single-axis alignment.

## Grid: The Two-Dimensional Powerhouse

CSS Grid handles rows AND columns simultaneously:

```css
.layout {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
}
```

### Named Grid Areas

For complex layouts, named areas are incredibly readable:

```css
.page {
  display: grid;
  grid-template-areas:
    "header header header"
    "sidebar main aside"
    "footer footer footer";
  grid-template-columns: 250px 1fr 200px;
}

.header  { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main    { grid-area: main; }
.aside   { grid-area: aside; }
.footer  { grid-area: footer; }
```

## Container Queries: The Game Changer

The newest addition lets components respond to their *container's* size, not just the viewport:

```css
.card-container {
  container-type: inline-size;
}

@container (min-width: 400px) {
  .card {
    display: grid;
    grid-template-columns: 200px 1fr;
  }
}
```

## The Decision Framework

- **Centering something?** → Flexbox
- **One row or one column?** → Flexbox
- **Complex 2D layout?** → Grid
- **Component-level responsive?** → Container Queries
- **Page-level responsive?** → Media Queries + Grid

---

*The best layout technique is the one that makes your CSS readable six months from now.*
