<div align="center">

```
 ██████╗  ██████╗ ██████╗ ██████╗ ███████╗    ███████╗ ██████╗ ██████╗  ██████╗ ███████╗
██╔════╝ ██╔════╝██╔═══██╗██╔══██╗██╔════╝    ██╔════╝██╔═══██╗██╔══██╗██╔════╝ ██╔════╝
██║  ███╗██║     ██║   ██║██║  ██║█████╗      █████╗  ██║   ██║██████╔╝██║  ███╗█████╗  
██║   ██║██║     ██║   ██║██║  ██║██╔══╝      ██╔══╝  ██║   ██║██╔══██╗██║   ██║██╔══╝  
╚██████╔╝╚██████╗╚██████╔╝██████╔╝███████╗    ██║     ╚██████╔╝██║  ██║╚██████╔╝███████╗
 ╚═════╝  ╚═════╝ ╚═════╝ ╚═════╝ ╚══════╝    ╚═╝      ╚═════╝ ╚═╝  ╚═╝ ╚═════╝ ╚══════╝
```

**Free · Browser-Based · No Upload · No Signup**

[![Live Demo](https://img.shields.io/badge/🚀%20Live%20Demo-gcodeforge.app-1565c0?style=for-the-badge)](https://gcodeforge.app/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Made With](https://img.shields.io/badge/Made%20With-WebGL%20%2B%20Three.js-ff6900?style=for-the-badge)](https://threejs.org/)
[![No Upload](https://img.shields.io/badge/Privacy-100%25%20Local-blueviolet?style=for-the-badge)](#privacy)

<br/>

> **The most powerful free online G-Code viewer, simulator & analyzer.**  
> View, analyze, and simulate G-code toolpaths in 3D/2D — runs entirely in your browser.  
> No file upload. No server. No account. **Free forever.**

<br/>

![GCode Forge Screenshot Placeholder](https://via.placeholder.com/900x450/1565c0/ffffff?text=GCode+Forge+—+3D+Toolpath+Viewer)

</div>

---

## 📋 Table of Contents

- [✨ Features](#-features)
- [🚀 Quick Start](#-quick-start)
- [🖥️ Views & Tabs](#️-views--tabs)
- [🔧 Left Panel Controls](#-left-panel-controls)
- [📤 Export Formats](#-export-formats)
- [🔌 Supported Firmware](#-supported-firmware)
- [⌨️ G-Code Command Support](#️-g-code-command-support)
- [🔐 Privacy](#-privacy)
- [🏗️ Architecture](#️-architecture)
- [📁 Project Structure](#-project-structure)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🎨 Visualization
- **3D Toolpath Viewer** — WebGL-powered via Three.js
- **2D Layer Map** — color-coded extrusion paths per layer
- **Perspective & Orthographic** projection modes
- **Named Views** — Top / Front / Side / Isometric (T/F/S/I)
- **Orbit, Pan, Zoom** — mouse & touch support
- **Legend overlay** — Extrusion / Travel / Retract color guide

</td>
<td width="50%">

### 🧠 Analysis
- **Print metrics dashboard** — layers, move counts, distance, estimated time
- **Per-layer extrusion chart** — visual bar graph per layer
- **Command frequency analyzer** — top G/M code usage
- **Model bounding box** — X/Y/Z ranges at a glance
- **Extrusion · Travel · Retract** move counters

</td>
</tr>
<tr>
<td width="50%">

### ✏️ Editor
- **Syntax-highlighted G-Code view** — color-coded commands
- **In-browser editor** — edit G-code directly, then re-render
- **Find & Replace** — modify values across entire file
- **Strip Comments** — remove all `;` comment lines
- **Normalize Whitespace** — clean up malformed files
- **Undo support** — revert edits step-by-step

</td>
<td width="50%">

### 📦 Export / Convert
- **G-Code** `.gcode` — re-download as-is
- **NC File** `.nc` — CNC machine format
- **STL** `.stl` — ASCII mesh from toolpath
- **OBJ** `.obj` — Wavefront 3D mesh
- **SVG** `.svg` — 2D vector top-down view
- **CSV** `.csv` — segment data table
- **JSON** `.json` — structured API-ready data
- **Plain Text** `.txt` — comments stripped

</td>
</tr>
</table>

---

## 🚀 Quick Start

### Option 1 — Use Online (Recommended)

Just go to **[gcodeforge.app](https://gcodeforge.app/)** and drop your file. Nothing to install.

### Option 2 — Run Locally

```bash
# Clone the repo
git clone https://github.com/yourusername/gcodeforge.git
cd gcodeforge

# No build step needed — it's a single HTML file!
# Open with any local server (to avoid CORS issues with file://):

# Python
python3 -m http.server 8080

# Node.js
npx serve .

# Then open:
# http://localhost:8080
```

> **Note:** You can also just open `index.html` directly in your browser — everything runs locally.

---

## 🖥️ Views & Tabs

GCode Forge has **6 tabs**, each with a distinct purpose:

| Tab | Description |
|-----|-------------|
| **🧊 3D View** | WebGL-rendered toolpath. Orbit with left mouse, pan with right mouse, zoom with scroll wheel. Camera presets: T/F/S/I |
| **⬛ 2D View** | Flat top-down layer map with color gradient per layer. Grid overlay for scale reference |
| **`</>` G-Code** | Full syntax-highlighted code view with line numbers. Toggle Edit Mode to modify directly |
| **📊 Analysis** | Dashboard with metrics cards, per-layer extrusion bar chart, and command frequency breakdown |
| **🔄 Convert** | Export to 8 formats. Also links to recommended slicers (Cura, PrusaSlicer) for STL → G-code |
| **❓ Help & FAQ** | Inline documentation, FAQ accordion, Arduino/GRBL guides, feature comparison table |

---

## 🔧 Left Panel Controls

```
┌─────────────────────────┐
│  📂 Drop Zone           │  ← Drag & drop .gcode / .nc / .g / .gc
├─────────────────────────┤
│  📄 File Info           │  ← Name, size, line count, layer count
├─────────────────────────┤
│  🎚️ Layer Filter        │  ← Min/Max sliders — isolate any layer range
├─────────────────────────┤
│  📐 Model Info          │  ← X/Y/Z bounds, extrusion/travel/retract counts
├─────────────────────────┤
│  📏 Model Scale         │  ← Scale X/Y/Z (10–300%). Show bounding box
├─────────────────────────┤
│  👁️ Visibility          │  ← Toggle: Extrusion · Travel · Retract · Axes · Grid
└─────────────────────────┘
```

### Layer Filter

Use the **Min** and **Max** sliders to isolate specific layers:
- Both 3D and 2D views update in real time
- Layer HUD in top-right of 3D viewport shows current range
- Essential for diagnosing adhesion issues or layer shifts

### Model Scale

Scale the visualization in X, Y, or Z:
- Click **Show BBox** to display a wireframe bounding box overlay
- Use **Reset** to return to 1:1 scale
- Note: scales the *visualization* only — use Find/Replace to scale actual coordinates

---

## 📤 Export Formats

| Format | Extension | Description |
|--------|-----------|-------------|
| G-Code | `.gcode` | Original file re-downloaded |
| NC File | `.nc` | Same as G-code, .nc extension for CNC controllers |
| STL | `.stl` | ASCII STL mesh built from extrusion segments |
| OBJ | `.obj` | Wavefront 3D mesh — open in Blender, MeshLab |
| SVG | `.svg` | 2D top-down vector export — open in Inkscape or browser |
| CSV | `.csv` | `layer, type, x1, y1, z1, x2, y2, z2` per segment |
| JSON | `.json` | Structured path data with print metrics — API-ready |
| Plain Text | `.txt` | Raw G-code, all `;` comments stripped |

> **STL/STEP/OBJ → G-Code?** That requires a **slicer** (separate app). GCode Forge links to [Ultimaker Cura](https://ultimaker.com/software/ultimaker-cura/) and [PrusaSlicer](https://www.prusa3d.com/prusaslicer/) from the Convert tab.

---

## 🔌 Supported Firmware

GCode Forge parses standard G-code and works with all major firmware:

| Firmware | Use Case |
|----------|----------|
| **Marlin** | FDM 3D printers (most common) |
| **Klipper** | High-speed 3D printing |
| **GRBL** | CNC routers, mills, laser cutters |
| **RepRap** | Open-source 3D printing |
| **Smoothieware** | Multi-axis CNC & 3D printing |
| **Duet / RRF** | Industrial & prosumer printers |
| **LinuxCNC** | Professional CNC machines |

---

## ⌨️ G-Code Command Support

### Motion Commands

| Command | Description |
|---------|-------------|
| `G0` | Rapid positioning (travel move — shown in grey) |
| `G1` | Linear move with extrusion (shown in blue) |
| `G2` / `G3` | Arc moves — clockwise / counter-clockwise |
| `G4` | Dwell / pause |
| `G28` | Home axes |
| `G29` | Auto bed leveling |

### Coordinate & Mode Commands

| Command | Description |
|---------|-------------|
| `G20` / `G21` | Inch / Metric mode |
| `G90` / `G91` | Absolute / Relative positioning |
| `G92` | Set position (commonly used to reset `E`) |
| `M82` / `M83` | Absolute / Relative extruder mode |

### Temperature & Machine Commands

| Command | Description |
|---------|-------------|
| `M104` / `M109` | Set / wait for hotend temperature |
| `M140` / `M190` | Set / wait for bed temperature |
| `M106` / `M107` | Fan on / Fan off |
| `M84` | Disable stepper motors |
| `M117` | Display message on LCD |

---

## 🔐 Privacy

**GCode Forge is 100% local. Your files never leave your device.**

```
Your G-code file
      │
      ▼
 Browser Memory  ──►  WebGL Renderer (Three.js)
      │                      │
      ▼                      ▼
  G-Code Parser         3D Viewport
      │
      ▼
  Local Export
 (download only)

  ❌ No server
  ❌ No upload
  ❌ No analytics on your files
  ❌ No signup required
```

All processing — parsing, rendering, export — happens in JavaScript and WebGL running entirely in your browser tab.

---

## 🏗️ Architecture

GCode Forge is a **single-file vanilla JavaScript application** with zero build steps and zero npm dependencies.

```
index.html
├── <head>
│   ├── SEO meta tags (Open Graph, Twitter Card, Schema.org JSON-LD)
│   │   ├── WebApplication schema
│   │   ├── FAQPage schema (8 questions)
│   │   ├── SoftwareApplication schema
│   │   └── HowTo schema
│   ├── Google Fonts (Inter + JetBrains Mono)
│   ├── Three.js r128 (CDN)
│   └── CSS (~700 lines — CSS variables, light theme, component styles)
│
├── <body>
│   ├── #topbar         — Logo + toolbar buttons + stats bar
│   ├── #app
│   │   ├── #left       — Drop zone · File info · Layer filter · Model info · Scale · Visibility
│   │   └── #main
│   │       ├── #vtabs  — 3D / 2D / G-Code / Analysis / Convert / Help
│   │       └── #view-area
│   │           ├── canvas#c3d      — Three.js WebGL canvas
│   │           ├── canvas#c2d      — 2D Canvas API layer map
│   │           ├── #v-code         — Syntax-highlighted code + editor toolbar
│   │           ├── #v-analysis     — Metrics cards + charts
│   │           ├── #v-convert      — Format picker + export actions
│   │           └── #v-help         — FAQ accordion + Arduino guides
│   └── #toast          — Notification toasts
│
└── <script> (~900 lines)
    ├── State object (S)            — Single source of truth
    ├── Three.js init & render loop — WebGL setup, lighting, camera
    ├── Mouse & touch bindings      — Orbit, pan, zoom, pinch-to-zoom
    ├── parseGcode()                — G-code parser (G0/G1/G2/G3, layer detection)
    ├── build3D()                   — BufferGeometry line segments from parsed data
    ├── draw2D()                    — Canvas 2D layer map renderer
    ├── renderCode()                — Syntax highlighter (regex-based)
    ├── renderAnalysis()            — Dashboard + bar charts
    ├── loadGcode()                 — File loader & UI updater
    ├── Drag/Drop + FileReader      — File input handling
    ├── doSample()                  — Built-in bioprinting scaffold sample
    ├── setView()                   — Tab switching
    ├── onLayerSlider()             — Layer filter with live re-render
    ├── toggleType()                — Show/hide extrusion · travel · retract
    ├── doExport()                  — Multi-format export (STL/OBJ/SVG/CSV/JSON)
    ├── buildSVG() / buildSTL() / buildOBJ() — Geometry builders
    ├── Editor functions            — Find, Replace, Strip Comments, Normalize, Undo, Apply
    ├── Model Scale & BBox          — Three.js group scale + wireframe overlay
    ├── Playback controls           — Line-by-line animation scrubber
    └── buildHelp()                 — Dynamic FAQ + Arduino guides
```

### Key Technical Decisions

- **No framework, no bundler** — ships as one `index.html`. Zero config, zero dependencies to manage.
- **Three.js via CDN** — `LineSegments` with `BufferGeometry` for efficient toolpath rendering. Each move type (extrusion/travel/retract) is a separate `LineSegments` object for toggle performance.
- **G-code parser** — single-pass, handles `G90`/`G91` absolute/relative switching, `M82`/`M83` extruder mode, `G92` E-reset, and layer detection by Z-height delta (`> 0.0005mm`).
- **Layer chart** — Canvas 2D bar chart (no Chart.js), drawn inline.
- **CSS variables** — full light theme via `:root` variables. Easy to fork into dark mode.

---

## 📁 Project Structure

```
gcodeforge/
└── index.html      ← Entire application (HTML + CSS + JS, ~105KB)
```

That's it. One file. Open in browser. Done.

---

## 🖱️ Keyboard & Mouse Controls

| Action | Control |
|--------|---------|
| Rotate 3D view | Left mouse drag |
| Pan 3D view | Right mouse drag |
| Zoom | Scroll wheel |
| Pinch to zoom | Touch (mobile) |
| Top view | Click **T** |
| Front view | Click **F** |
| Side view | Click **S** |
| Isometric view | Click **I** |
| Reset camera | Toolbar → **Reset View** |
| Fit to model | Toolbar → **Fit** |

---

## 🤝 Contributing

Contributions are welcome! Here's how:

```bash
# Fork the repo on GitHub, then:
git clone https://github.com/YOUR_USERNAME/gcodeforge.git
cd gcodeforge

# Make your changes to index.html
# Test in browser (no build step)

# Commit and push
git add index.html
git commit -m "feat: your feature description"
git push origin main

# Open a Pull Request on GitHub
```

### Ideas for Contributions

- [ ] Dark mode theme
- [ ] G2/G3 arc rendering in 3D view
- [ ] Print speed color visualization (slower = red, faster = green)
- [ ] Multi-file comparison
- [ ] Estimated filament weight calculator
- [ ] Klipper `PRINT_START` macro parsing
- [ ] Mobile-responsive left panel (collapsible)

---

## 📊 Comparison vs Alternatives

| Feature | **GCode Forge** | NCViewer | gcode.ws |
|---------|:-----------:|:--------:|:--------:|
| 3D Toolpath View | ✅ | ✅ | ✅ |
| 2D Layer View | ✅ | ✅ | ✅ |
| Layer Filtering | ✅ | ❌ | ❌ |
| G-Code Editor + Find/Replace | ✅ | ❌ | ❌ |
| Model Scale + BBox | ✅ | ❌ | ❌ |
| Print Analysis Dashboard | ✅ | ❌ | ❌ |
| Export STL / OBJ | ✅ | ❌ | ❌ |
| Export SVG / CSV / JSON | ✅ | ❌ | ❌ |
| Syntax Highlighting | ✅ | ❌ | ✅ |
| No Upload Required | ✅ | ✅ | ✅ |

| Arduino / GRBL Guide | ✅ | ❌ | ❌ |
| Single File, No Build | ✅ | ❌ | ❌ |

---

## 📄 License

```
MIT License

Copyright (c) 2026 GCode Forge

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software.
```

See [LICENSE](LICENSE) for full text.

---

<div align="center">

**Made with ❤️ for the CNC, 3D printing community**

[![gcodeforge.app](https://img.shields.io/badge/🌐-gcodeforge.app-1565c0?style=flat-square)](https://gcodeforge.app/)
&nbsp;
[![Twitter](https://img.shields.io/badge/Twitter-@gcodeforge-1da1f2?style=flat-square&logo=twitter)](https://twitter.com/gcodeforge)

*If GCode Forge saved you time, give it a ⭐ on GitHub!*

</div>
