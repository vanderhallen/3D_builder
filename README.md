# 3D_builder — Forge

A single-file, browser-based **parametric CAD builder** built on Three.js, with a
natural-language **chat assistant** that drives the modeling tools from typed prompts.

No build step, no dependencies to install — `index.html` is the whole app.

## Features

- **Sketch** — rectangle / circle / polygon on datum planes, with editable dimensions
- **Extrude** — add / subtract / intersect (real boolean material removal)
- **Boolean** — unite / subtract / intersect between bodies
- **Hole** — ISO presets (M3–M10), counterbore & countersink, through / blind
- **Edge blend** — fillet / chamfer on extruded bodies
- **Pattern** — linear & circular arrays of a feature
- **Revolve** — new / add / subtract
- **Datums** — offset planes and reference axes
- Self-contained **CSG engine** (BSP) — no external libraries

### Chat assistant
Type commands like:
```
sketch rectangle 20x10 on top
extrude 6
hole M6 counterbore through
pattern circular 6 axis y
fillet 2
boolean subtract body 2 from body 1
```
Type `help` in the chat for the full list. The assistant runs fully in-page
(it parses commands locally — no API key, works offline).

## Run locally
Just open `index.html` in any modern browser. (Three.js loads from a CDN, so an
internet connection is needed the first time.)

## Publish on GitHub Pages
After pushing this repo, enable Pages:
**Settings → Pages → Build and deployment → Source: `Deploy from a branch` →
Branch: `main` / `(root)` → Save.**

The site will be live at:
```
https://vanderhallen.github.io/3D_builder/
```

## Controls
- **Right-drag** orbit · **Wheel** zoom · **Shift+Right-drag** pan
- Tool shortcuts: V S E B H L P R D O
- Enter finishes a sketch · Esc cancels · Delete removes the selection

---
Built with Three.js r128.
