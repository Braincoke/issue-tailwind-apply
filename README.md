# CSS issue with the tag <a>

This project is a minimal reproduction code for a specific CSS issue.

The starter is created with Gridsome and TailwindCSS.

## Files used in the project

### main.css

The file `/src/assets/css/main.css` contains the Tailwind directives and imports another css file:

```css
@tailwind base;
@tailwind components;

@import "./theme-pink.css";

@tailwind utilities;
```

### theme-pink.css

This file applies some Tailwind utilities to demonstrate the issue:

```css
// This one is correctly applied
div {
    @apply bg-pink-200;
}

// This one is not
a {
    @apply text-red-600;
}

// This one is correctly applied
a:hover {
    @apply text-blue-500;
}
```

## Issue

Every css in theme-pink.css is applied but the one with `a { @apply text-red-600; }`.
