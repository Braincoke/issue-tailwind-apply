# CSS issue with the tag `<a>`

This project is a minimal reproduction code for a specific CSS issue.

The starter is created with Gridsome and TailwindCSS.

## Starting the project

Install the dependencies with `npm install` and run `gridsome develop`.

You might need to install gridsome cli with `npm install --global @gridsome/cli`.

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

If move the problematic line in `main.css` then our style is applied:

```css
@tailwind base;
@tailwind components;

@import "./theme-pink.css";

@tailwind utilities;

a {
    @apply text-red-600;
}
```

You can test this in the branch `workaround`.