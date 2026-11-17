# library

Parts used by the PCBs, designed for 1.8 mm LEDs (D 1.8 mm, W 3.3 mm, H 2.4 mm).

| Folder | Content |
|---|---|
| `ho-signals.pretty/` | KiCad footprints: one per LED colour (red, green, orange, white), plus the unpopulated and the strap (wire link) variants. |
| `ho-signals.3dshapes/` | 3D models (`.wrl`) of the LEDs (off, lit, dim), the resistor (generic red-red-brown bands) and the pin header. |
| `LED_THT/` | Vector drawings (`.svg`) of the LEDs, off and lit, used to draw the Fritzing breadboard views. |

Add `ho-signals.pretty` to your KiCad footprint libraries if you want to edit the PCBs in [`../source`](../source).
