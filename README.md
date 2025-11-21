# Tailwind CSS Practice Project

A minimal setup using **Vite** and **Tailwind CSS (v4)**.  
This project is meant for practicing Tailwind utilities, custom layers, theming, and small UI components.

## Features
- Vite development server with fast hot-reload
- Tailwind CSS v4
- Custom `@theme`, `@layer`, and `@apply` usage
- Responsive utilities and dark mode examples
- Clean project structure

## Requirements
- Node.js 16+
- npm / yarn / pnpm

## Installation

```bash
npm install
```

## Running the Dev Server

```bash
npm run dev
```

Then visit:

```
http://localhost:5173
```

## Project Structure

```
project/
│── index.html
│── vite.config.js
│── postcss.config.mjs
│── tailwind.config.cjs
└── src/
    ├── index.css       # Tailwind + custom CSS
    └── main.js         # Entry file (if required)
```

## How Tailwind Works Here
- `@import "tailwindcss";` loads the Tailwind engine.
- Custom styling uses:
  - `@theme` for custom variables (e.g., colors)
  - `@layer base` for global element styles
  - `@layer components` for reusable UI blocks
- All HTML/CSS/JS inside the `content` paths in `tailwind.config.cjs` is scanned so unused classes get removed automatically.

## VS Code Notes
If you see warnings like `Unknown at rule @apply` or `@theme`, update `.vscode/settings.json`:

```json
"css.lint.unknownAtRules": "ignore"
```

This prevents the CSS language server from flagging Tailwind-specific rules.

## Build

```bash
npm run build
```