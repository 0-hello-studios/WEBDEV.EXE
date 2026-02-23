# WEBDEV.EXE

A browser-based visual web page builder by **0-HELLO Studios**.

## File Structure

```
📦 webdev-exe/
├── 📄 index.html              ← Main entry point
├── 📄 README.md
│
├── 📂 styles/                  ← CSS
│   ├── theme.css               ← CSS variables, reset, base
│   ├── workspace.css           ← Topbar, canvas, scrollbars, preview
│   └── components.css          ← Windows, forms, buttons, tool UI
│
├── 📂 config/                  ← Configuration
│   └── modules.js              ← Window system + module registry
│
├── 📂 utils/                   ← Helpers
│   ├── helpers.js              ← Core utility functions (gv, sv, toast, etc.)
│   └── storage.js              ← Undo/redo system
│
├── 📂 modules/                 ← Feature modules
│   ├── text.js                 ← Typography lab, text gradient, text editor
│   ├── color.js                ← Palette, gradient, glass, mesh, contrast, converter, colorblind
│   ├── effects.js              ← Shadow, filters, neumorphism, radius, noise, texture, cursor
│   ├── shape.js                ← Shapes, blob, wave, clip, pattern, icons, QR, favicon, mockup
│   ├── layout.js               ← Align, padding/margin, page size, grid, canvas, ratio, units, breakpoints
│   ├── animate.js              ← Animation builder, block anims, transitions, easing
│   ├── export.js               ← Project save/load, HTML/CSS export
│   ├── code.js                 ← Code editor, CSS cheat sheet
│   └── engine.js               ← Core page builder (selection, blocks, drag, resize, draw, preview, etc.)
│
└── 📂 assets/                  ← Resources (icons, presets — future use)
```

## Script Load Order

Scripts must load in this order (dependencies flow downward):

1. `config/modules.js` — Window system & module registry
2. `utils/helpers.js` — Core utilities used everywhere
3. `utils/storage.js` — Undo/redo
4. `modules/text.js` through `modules/code.js` — Tool modules (independent)
5. `modules/engine.js` — Core engine (depends on everything above)

## Development

Open `index.html` in a browser. All files are vanilla JS/CSS with no build step required.
