# Railway HO project - Signals - Electronics for my HO scale railway project

My Railway project tries to
## Deutsche Bahn Train Signals, Epoch III (1949-1970)

[wikipedia](https://en.wikipedia.org/wiki/Railway_signals_in_Germany)

These sites were a great source of inspiration:
* [stummi forum (DE)](https://www.stummiforum.de/t174376f21-Viessman-Signalbr-cke-mit-Arduino-gesteuert.html)
* [digital bahn (DE)](https://www.digital-bahn.de/info_kompo/signale.htm)

### [kicad_pcb_ho_db_signals_v1](#kicad_pcb_ho_db_signals_v1)

This directory contains Kicad project files to build PCBs using 1.8mm LEDs

This PCB uses charlieplexing to reduce the number of wires. It is also possible to build a block signal, input signal or output signal with this PCB.
I designed my own wiring path to avoid using the POV effect to light multiple LEDs. Each situation for each signal is a simple combination of HIGH and LOW signals on all 4 pins.

This project had a bias. The "Shunting Signal" Hp0 + Sh1 did not work because the right white LED did not light up.
So I made a v2 with a smaller PCB which fixes this problem: [kicad_pcb_ho_db_signals_v2](#kicad_pcb_ho_db_signals_v2)
The one from v1 was a little too wide. There was a gap between the LEDs

I also need a special breadboard version to ease tests: [kicad_pcb_ho_db_signals_breadboard_v2](#kicad_pcb_ho_db_signals_breadboard_v2)

The **gerber.zip** file is enough to build the PCB from a manufacturer such as [jlcpcb](https://jlcpcb.com/)

It's possible to reduce the number of wires for the "Block Signal" (only 2 wires required) and the "Entry Signal" (only 3 wires required). See [ho_db_signals_wiring/](ho_db_signals_wiring/)

### [kicad_pcb_ho_db_signals_v2](#kicad_pcb_ho_db_signals_v2)

This directory contains Kicad project files to build PCBs using 1.8mm LEDs

This PCB uses charlieplexing to reduce the number of wires. It is also possible to build a block signal, input signal or output signal with this PCB.
I designed my own wiring path to avoid using the POV effect to light multiple LEDs. Each situation for each signal is a simple combination of HIGH and LOW signals on all 4 pins.

This v2 is a smaller one than the v1. It also allows the "Shunting Signal" Hp0 + Sh1 to work.

The gerber.zip file is enough to build the PCB from a manufacturer such as [jlcpcb](https://jlcpcb.com/)

### [kicad_pcb_ho_db_signals_breadboard_v2](#kicad_pcb_ho_db_signals_breadboard_v2)

This directory contains Kicad project files to build a HO signal PCB using 1.8mm LEDs. This version is a test version of the kicad_pcb_ho_db_signals_v2 as it has room for resistors and rounded pins for use on a breadboard or directly on a UNO.

The gerber.zip file is enough to build the PCB from a manufacturer such as [jlcpcb](https://jlcpcb.com/)

BOM:
* a PCB per signal. I orderd mine 0.8mm thickness from jlcpcb.com simply by uploading the gerber.zip file
* 2 to 4 60 to 100 ohms resistors 1/4 W from everywhere
* 1.8mm LEDs. I bought mine from aliexpress.com
