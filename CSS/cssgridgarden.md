---
tags: [css, grid, frontend]
---

# CSS Grid Garden

## Grid Lines
Lines are numbered from 1. A 5-column grid has **6 lines**.
Line 1 is the left/top edge of the container.
---

## Placing Items

```css
grid-column-start: 3;        /* start at line 3 */
grid-column-end: 5;          /* end at line 5 */
grid-column-end: span 2;     /* span 2 columns */
grid-column: 2 / 5;          /* shorthand: start / end */
grid-row: 1 / 3;             /* same but for rows */
grid-area: 1 / 1 / 3 / 6;   /* row-start / col-start / row-end / col-end */
```

---

## Negative Line Numbers

```css
grid-column-start: -3; /* 3rd line from the right */
```

> [!tip] Negative lines count from the **end** of the grid, so `-1` is always the last line.

---

## `order`

```css
.water  { order: 0; }  /* default for all items */
.poison { order: -1; } /* renders before water — lower = earlier */
```

> [!note] All items default to `order: 0`. Negative order = rendered first.

---

## `fr` Unit

Divides **leftover space** after fixed units (px, %) are subtracted.

```css
grid-template-columns: 1fr 5fr;               /* 1/6 and 5/6 */
grid-template-columns: 50px 1fr 1fr 1fr 50px; /* fixed edges, equal middle */
grid-template-columns: 75px 3fr 2fr;          /* fixed left, 3/5 and 2/5 remaining */
```

---

## `repeat()`

```css
grid-template-columns: repeat(5, 20%);  /* same as 20% 20% 20% 20% 20% */
grid-template-rows: repeat(4, 12.5px);
```

---

## `grid-template` shorthand

```css
/* rows / columns */
grid-template: 60% 40% / 200px 1fr;
```

---

