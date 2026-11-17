# documentation

Renders and web pages of the three signal families (`bloc`, `entry`, `exit`), for two boards:
`prod/` (production PCB, solder wires) and `breadboard/` (pin headers).

Each folder contains:

| File | Content |
|---|---|
| `*-viewer.html` | Interactive 3D viewer: pick a family, then an aspect (all off, all on, Hp0, Hp1, tests...). |
| `*-states.html` | For each aspect and wiring test, which wire is at VCC (3.3 V) or GND. |
| `*-bare.svg` | The bare board, without components. |
| `<family>/png/` | Renders of every aspect, top and bottom, transparent background. |
| `<family>/svg/` | Vector breadboard view of every aspect, plus icon, schematic and PCB symbols. |
| `<family>/glb/` | 3D models loaded by the viewer. |

## Opening the pages

- `*-states.html` is self-contained: double-click it.
- `*-viewer.html` loads the 3D models on demand, so it must be **served over http**
  (GitHub Pages, or `python3 -m http.server` in this folder, then open
  `http://localhost:8000/prod/...`). Opened as a local file, the browser refuses to load the models.
  An internet connection is needed for the 3D library.

Files are generated from [`../source`](../source).
