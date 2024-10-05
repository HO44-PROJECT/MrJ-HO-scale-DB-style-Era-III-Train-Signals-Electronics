# Railway HO project Signals and electronics for my HO scale railway project

This is my own project for building model railway HO scale (1:87) Deutsche Bundesbahn (DB) style Era III (1945-1970) Train Signals following this specification.

This is part of a complete project involving:

- 3D printing ([Maker World](https://makerworld.com/en/models/682526#profileId-611046))
- Electronics (PCB design and soldering) ([github](https://github.com/HO44-PROJECT/MrJ-HO-scale-DB-style-Era-III-Train-Signals-Electronics))
- Arduino code (demo, DCC and JMRI integration) ([github](https://github.com/HO44-PROJECT/MrJ-HO-scale-DB-style-Era-III-Train-Signals-Arduino-Demo-Code))

# Resources

[wikipedia signals in Germany](https://en.wikipedia.org/wiki/Railway_signals_in_Germany)

These sites were a great source of inspiration:
* [stummi forum (DE)](https://www.stummiforum.de/t174376f21-Viessman-Signalbr-cke-mit-Arduino-gesteuert.html)
* [digital bahn (DE)] (https://www.digital-bahn.de/info_kompo/signale.htm)

# Project

This project contains Kicad project files and gerber to build PCBs using 1.8mm LEDs.

This PCB uses charlieplexing to reduce the number of wires. It is possible to build a block signal, input signal, or output signal with this PCB.
I designed my own wiring path to avoid using the POV effect to light multiple LEDs. Each situation for each signal is a simple combination of HIGH and LOW signals on all 4 pins.

It's possible to reduce the number of wires for the "Block Signal" (only 2 wires required) and the "Entry Signal" (only 3 wires required). See [documentation/] (documentation/)

I also need a special breadboard version to ease tests. This version allows soldering of resistors.

The **gerber.zip** files are enough to build the PCB from a manufacturer such as [jlcpcb](https://jlcpcb.com/). See [release/] (release/) directory.

# History

The version 2 is smaller than the version 1.
It solves the "shunting signal" Hp0 + Sh1 did not work because the right white LED did not light up.

This v3 is a better version as it fixes a distributed current problem.

# Source

The [source/] directory contains Kicad files

# BOM:
* a PCB per signal. I ordered mine 0.8mm thickness from jlcpcb.com simply by uploading the gerber.zip file.
* 2 to 4 60 to 100 ohm resistors 1/4 W from everywhere
* 1.8mm LEDs. I bought mine from aliexpress.com.
