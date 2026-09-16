# d7-program

d7-program is a browser-based generative architectural tool for creating, exploring, and analyzing continuous sectional spatial diagrams composed of overlapping, rotated rectangular forms. It models architectural spatial assemblies where overlapping boundaries determine tonal fields and internal boundary linework, offering both individual parameter-driven variation exploration, vector/CAD exports, and a comparative 5 × 5 parameter matrix view.

## Features

- **Dynamic Sectional Spatial Generation**: Generates contiguous, connected sectional compositions from sharp-edged rectangular geometries with seeded randomness.
- **Overlap-Based Tonal Shading**: Visualizes spatial enclosure with layered opacity, where single-layer forms render at 10% grey and overlapping intersections darken progressively.
- **Precision Outline Depth Filtering**: Computes exact edge-to-edge polygon intersections and filters visible linework to isolate regions with specific overlapping shape depths.
- **Vector & CAD Exports**:
  - **SVG Export**: Layered vector files with distinct form fills and segmented outline paths for Adobe Illustrator and laser cutting.
  - **DXF Export**: Industry-standard Release 12 AutoCAD/Rhino 2D line geometry for instant architectural modeling.
  - **High-Res PNG Export**: Clean raster captures for portfolios and presentation drawings.
- **Display Themes**: Switch between Architectural Monochrome (Dark), Blueprint/Cyanotype (Navy/Cyan), and Paper/Light (Print Ready).
- **Interactive Viewport**: Mouse drag to pan, mouse wheel to zoom, with on-screen HUD controls and one-click view reset.
- **Comparative 5 × 5 Matrix View**: Cross-compares variations across two independent parameter axes while holding other parameters fixed. Click any cell to load it directly into the editor.
- **Local Variation Storage**: Allows users to save, inspect, and restore preferred spatial variations using browser localStorage.
- **Zero-Dependency Architecture**: Runs entirely client-side using native HTML5 Canvas and JavaScript without requiring build steps, external build dependencies, or server backends.

## Getting Started

1. Clone or download the repository:
   ```bash
   git clone https://github.com/emmasoucy/d7-program.git
   ```
2. Open `index.html` directly in any modern web browser, or serve it locally:
   ```bash
   python3 -m http.server 8000
   ```
3. Navigate to `http://localhost:8000` to interact with the generator.
4. Access the live version on GitHub Pages at [https://emmasoucy.github.io/d7-program/](https://emmasoucy.github.io/d7-program/).

## Controls

- **Scale Factor**: Choose height/tall or width/wide scaling and adjust the slider (50% – 220%) to scale the active dimension while keeping the base dimension constant.
- **Density / Complexity**: Set the exact number of rectangular forms in the composition (2 – 16 forms).
- **Overlap Depth**: Adjust pre-rotation contact depth (5% – 90%) relative to the smaller rectangle along its joining axis.
- **Angular Rotation**: Set the maximum rotation angle range (0° – 45°); each non-root form receives a deterministic rotation angle.
- **Outline Overlap Count**: Filter visible linework segments to show only edges where the exact specified number of forms overlap.
- **Display Style**: Toggle between Dark, Blueprint, and Print-Ready themes.
- **Generate Variation**: Generate a new random variation while preserving current slider parameters.
- **Save Variation**: Store the current configuration and seed in the local storage history.
- **5 × 5 Matrix**: Toggle a 5 × 5 parameter exploration grid with customizable horizontal and vertical criteria axes.
- **Export Tools**: One-click export to SVG, DXF, and PNG.
- **Pan & Zoom**: Click and drag on the viewport to pan; scroll to zoom in/out; use HUD buttons for quick adjustments.
