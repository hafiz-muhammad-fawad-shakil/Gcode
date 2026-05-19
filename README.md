<div align="center">

```
 ██████╗  ██████╗ ██████╗ ██████╗ ███████╗    ██╗  ██╗
██╔════╝ ██╔════╝██╔═══██╗██╔══██╗██╔════╝    ╚██╗██╔╝
██║  ███╗██║     ██║   ██║██║  ██║█████╗       ╚███╔╝ 
██║   ██║██║     ██║   ██║██║  ██║██╔══╝       ██╔██╗ 
╚██████╔╝╚██████╗╚██████╔╝██████╔╝███████╗    ██╔╝ ██╗
 ╚═════╝  ╚═════╝ ╚═════╝ ╚═════╝ ╚══════╝    ╚═╝  ╚═╝
```

**Free · Browser-Based · No Upload · No Signup**

[![Live Demo](https://img.shields.io/badge/🚀%20Live%20Demo-gcodex.tech-1565c0?style=for-the-badge)](https://gcodex.tech/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Made With](https://img.shields.io/badge/Made%20With-WebGL%20%2B%20Three.js-ff6900?style=for-the-badge)](https://threejs.org/)
[![No Upload](https://img.shields.io/badge/Privacy-100%25%20Local-blueviolet?style=for-the-badge)](#privacy)
[![Product Hunt](https://img.shields.io/badge/Product_Hunt-Featured-DA552F?style=for-the-badge&logo=producthunt)](https://www.producthunt.com/products/gcodex)

<br/>

> **The most powerful free online G-Code viewer, simulator & analyzer.**  
> View, analyze, and simulate G-code toolpaths in 3D/2D — runs entirely in your browser.  
> No file upload. No server. No account. **Free forever.**

<br/>

### 🔗 [https://gcodex.tech/](https://gcodex.tech/)

<br/>

[![GCodex - Free online G-Code viewer & simulator for CNC and 3D printer | Product Hunt](https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=1147687&theme=dark&t=1779017966824)](https://www.producthunt.com/products/gcodex?embed=true&utm_source=badge-featured&utm_medium=badge&utm_campaign=badge-gcodex)

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
- [📊 Comparison vs Alternatives](#-comparison-vs-alternatives)
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

Just go to **[gcodex.tech](https://gcodex.tech/)** and drop your file. Nothing to install.


## 🖥️ Views & Tabs

| Tab | Description |
|-----|-------------|
| **🧊 3D View** | WebGL-rendered toolpath. Orbit / pan / zoom. Camera presets: T/F/S/I |
| **⬛ 2D View** | Flat top-down layer map with color gradient per layer |
| **`</>` G-Code** | Syntax-highlighted code view. Toggle Edit Mode to modify directly |
| **📊 Analysis** | Metrics dashboard, per-layer extrusion bar chart, command frequency |
| **🔄 Convert** | Export to 8 formats. Links to Cura & PrusaSlicer for STL→G-code |
| **❓ Help & FAQ** | Inline docs, FAQ accordion, Arduino/GRBL guides |

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
│  📐 Model Info          │  ← X/Y/Z bounds, move counters
├─────────────────────────┤
│  📏 Model Scale         │  ← Scale X/Y/Z. Show bounding box
├─────────────────────────┤
│  👁️ Visibility          │  ← Toggle: Extrusion · Travel · Retract · Axes · Grid
└─────────────────────────┘
```

---

## 📤 Export Formats

| Format | Extension | Description |
|--------|-----------|-------------|
| G-Code | `.gcode` | Original file re-downloaded |
| NC File | `.nc` | CNC machine format |
| STL | `.stl` | ASCII STL mesh from extrusion segments |
| OBJ | `.obj` | Wavefront 3D mesh — open in Blender, MeshLab |
| SVG | `.svg` | 2D top-down vector export |
| CSV | `.csv` | `layer, type, x1, y1, z1, x2, y2, z2` per segment |
| JSON | `.json` | Structured path data — API-ready |
| Plain Text | `.txt` | Raw G-code, comments stripped |

---

## 🔌 Supported Firmware

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

| Command | Description |
|---------|-------------|
| `G0` | Rapid positioning (travel move) |
| `G1` | Linear move with extrusion |
| `G2` / `G3` | Arc moves — CW / CCW |
| `G4` | Dwell / pause |
| `G20` / `G21` | Inch / Metric mode |
| `G28` | Home axes |
| `G90` / `G91` | Absolute / Relative positioning |
| `G92` | Set position (E-reset) |
| `M82` / `M83` | Absolute / Relative extruder mode |
| `M104` / `M109` | Set / wait for hotend temp |
| `M140` / `M190` | Set / wait for bed temp |
| `M106` / `M107` | Fan on / Fan off |

---

## 🔐 Privacy

**GCodex is 100% local. Your files never leave your device.**

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
  Local Export (download only)

  ❌ No server    ❌ No upload
  ❌ No analytics ❌ No signup
```

---

## 🏗️ Architecture

Single-file vanilla JS app — zero build steps, zero npm dependencies.

```
index.html
├── SEO meta (OG, Twitter Card, Schema.org JSON-LD)
├── Three.js r128 (CDN)
├── CSS (~700 lines)
└── JS (~900 lines)
    ├── parseGcode()   — G-code parser (G90/G91, M82/M83, G92)
    ├── build3D()      — Three.js BufferGeometry line segments
    ├── draw2D()       — Canvas 2D layer map
    ├── doExport()     — STL / OBJ / SVG / CSV / JSON export
    └── Editor         — Find, Replace, Strip Comments, Normalize
```

---

## 📁 Project Structure

```
Gcode/
├── index.html          ← Entire application
├── ads.txt             ← AdSense verification
├── site.webmanifest    ← PWA manifest
└── favicon.ico
```

---

## 🖱️ Controls

| Action | Control |
|--------|---------|
| Rotate 3D | Left mouse drag |
| Pan 3D | Right mouse drag |
| Zoom | Scroll wheel |
| Pinch zoom | Touch (mobile) |
| Top / Front / Side / Iso | T / F / S / I |
| Reset camera | Toolbar → Reset View |
| Fit model | Toolbar → Fit |

---

## 📊 Comparison vs Alternatives

| Feature | **GCodex** | NCViewer | gcode.ws |
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
| Single File, No Build | ✅ | ❌ | ❌ |

---

## 🤝 Contributing

```bash
git clone https://github.com/hafiz-muhammad-fawad-shakil/Gcode.git
cd Gcode
# Edit index.html — no build step
# Test in browser, then commit & push
```

**Ideas welcome:**
- [ ] Dark mode
- [ ] G2/G3 arc rendering in 3D
- [ ] Print speed color visualization
- [ ] Mobile-responsive panel
- [ ] Filament weight calculator

---

## 📄 License

MIT License — free to use, fork, and contribute.

---

<div align="center">

**Made with ❤️ for the CNC, 3D printing & bioprinting community**

[![gcodex.tech](https://img.shields.io/badge/🌐-gcodex.tech-1565c0?style=flat-square)](https://gcodex.tech/)
&nbsp;
[![Product Hunt](https://img.shields.io/badge/Product_Hunt-GCodex-DA552F?style=flat-square&logo=producthunt)](https://www.producthunt.com/products/gcodex?embed=true&utm_source=badge-featured&utm_medium=badge&utm_campaign=badge-gcodex)

*If GCodex saved you time, give it a ⭐ on GitHub!*

</div>
