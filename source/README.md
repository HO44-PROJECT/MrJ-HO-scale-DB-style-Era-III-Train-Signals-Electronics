# source

KiCad 10 projects of the signal boards (schematic + PCB). Open the `.kicad_pro` file in KiCad.

| Folder | Board |
|---|---|
| `prod/` | Production PCB, wires are soldered to the pads. |
| `breadboard/` | Same circuit with pin headers, for prototyping on a breadboard. |

Each folder contains the project (`.kicad_pro`), the schematic (`.kicad_sch`) and the PCB (`.kicad_pcb`).
The LED footprints and 3D models come from [`../library`](../library).

These files are the single source of truth: everything in `documentation/`, `fritzing/` and
`release/` is derived from them.
