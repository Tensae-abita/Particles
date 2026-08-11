<div align="center">

# ✨ Particles

**A GPU-driven particle system built with Three.js — thousands of textured points animated in real time, with full control over size, color, and behavior.**

[![Three.js](https://img.shields.io/badge/Three.js-000000?logo=three.js&logoColor=white)](https://threejs.org)
[![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)](https://vitejs.dev)
[![lil-gui](https://img.shields.io/badge/lil--gui-debug%20UI-blue)](https://lil-gui.georgealways.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

</div>

## Overview

A real-time particle system built on Three.js's `BufferGeometry` and `Points`, rendering thousands of individually positioned, colored, and sized points in a single efficient draw call. Particles are textured using an alpha map for soft, circular sprites rather than hard-edged squares, and animated per-frame for organic motion.

A `lil-gui` debug panel exposes size, color, and count controls live, making it easy to explore how each parameter affects the final look without touching code.

## ✨ Features

- **Large-scale point rendering** — thousands of particles rendered in one draw call via `BufferGeometry`/`Points` for high performance
- **Textured particle sprites** — alpha-mapped textures give particles soft, circular edges instead of flat squares
- **Depth-aware blending** — additive blending and disabled depth-write configured for a glowing, layered look without visual artifacts
- **Per-frame animation** — particle positions update each frame for continuous motion (e.g. wave-like or drifting movement)
- **Live-tunable parameters** — particle count, size, and color adjustable in real time via GUI

## 🧱 Tech Stack

| Layer | Choice |
|---|---|
| 3D rendering | [Three.js](https://threejs.org) |
| Build tool | [Vite](https://vitejs.dev) |
| Debug UI | [lil-gui](https://lil-gui.georgealways.com/) |
| Language | Vanilla JavaScript (ES modules) |

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en/download/) (LTS recommended)

### Installation

```bash
git clone https://github.com/Tensae-abita/Particles.git
cd Particles
npm install
```

### Run locally

```bash
npm run dev
```

Vite will print a local URL in your terminal (typically `http://localhost:5173`) — open it in your browser to view the scene.

### Build for production

```bash
npm run build
```

Outputs an optimized, static build to the `dist/` directory, ready to deploy anywhere that serves static files (Netlify, Vercel, GitHub Pages, etc.).

## 📁 Project Structure

```
src/
├── script.js        # Scene setup, particle geometry/material, GUI bindings, animation loop
└── style.css         # Base page styling

static/
└── textures/          # Particle sprite/alpha map textures
```

## 🎨 Tuning the Particles

Open the `lil-gui` panel in the corner of the page to adjust parameters live — particle count, size, and color. For structural changes (texture swaps, blending mode, animation behavior), edit `src/script.js` directly.

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](./LICENSE) file for details.
