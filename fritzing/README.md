# fritzing

[Fritzing](https://fritzing.org) parts of the signals, to use them in a breadboard sketch.

Two sets of parts:

| Folder | Use |
|---|---|
| `prod/` | The normal signal, as on the production PCB (solder wires). |
| `breadboard-fritzing/` | The test case: the breadboard version, without pin headers (the Fritzing part brings its own connectors). |

Each folder holds 24 parts, one per situation of each family (`bloc`, `entry`, `exit`):

| Suffix | Situation |
|---|---|
| none | All LEDs lit (also the part icon). |
| `-off` | All LEDs off. |
| `-Hp0`, `-Hp1`, `-Hp2`, `-Hp0+Sh1` | The nominal aspects. |
| `-test-w1`, `-test-w2`... | Wiring tests: the listed wires at 3.3 V, the others at GND. |

## Install

In Fritzing: *File > Import > Part...*, then choose a `.fzpz` file.
The supply is 3.3 V and the resistors are 470 ohm (1 kohm for a 5 V supply).

To see which wire must be at VCC or GND for each situation, open the `*-states.html` page in
[`../documentation`](../documentation).
