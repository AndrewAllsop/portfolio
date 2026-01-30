---
title: "Modern CSS Techniques Every Developer Should Know"
description: "Explore powerful CSS features like Container Queries, CSS Grid, and Custom Properties that will transform how you write styles."
pubDate: 2024-01-20
tags: ["css", "webdev", "frontend"]
---

CSS has evolved dramatically over the past few years. Features that once required JavaScript or complex workarounds are now native to the language. Let's explore some modern CSS techniques that will level up your styling game.

## Container Queries

Container queries allow you to style elements based on their parent container's size rather than the viewport. This is a game-changer for component-based design.

```css
.card-container {
  container-type: inline-size;
}

@container (min-width: 400px) {
  .card {
    display: grid;
    grid-template-columns: 1fr 2fr;
  }
}
```

## CSS Custom Properties

Custom properties (CSS variables) have become essential for building maintainable stylesheets:

```css
:root {
  --color-primary: #3b82f6;
  --spacing-md: 1rem;
  --radius-lg: 0.75rem;
}

.button {
  background: var(--color-primary);
  padding: var(--spacing-md);
  border-radius: var(--radius-lg);
}
```

## The :has() Selector

The `:has()` pseudo-class is often called the "parent selector" – something developers have wanted for years:

```css
/* Style a card differently if it contains an image */
.card:has(img) {
  padding-top: 0;
}

/* Style a form label when its input is focused */
label:has(+ input:focus) {
  color: var(--color-primary);
}
```

## CSS Grid for Complex Layouts

CSS Grid makes complex layouts simple and intuitive:

```css
.dashboard {
  display: grid;
  grid-template-columns: 250px 1fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "sidebar header"
    "sidebar main"
    "sidebar footer";
  min-height: 100vh;
}
```

## Logical Properties

Logical properties help create layouts that work across different writing modes and directions:

```css
.element {
  /* Instead of margin-left and margin-right */
  margin-inline: 1rem;

  /* Instead of margin-top and margin-bottom */
  margin-block: 2rem;

  /* Instead of padding-left */
  padding-inline-start: 1rem;
}
```

## Conclusion

Modern CSS is incredibly powerful. These features reduce our reliance on JavaScript for styling and make our code more maintainable. Start incorporating them into your projects today!
