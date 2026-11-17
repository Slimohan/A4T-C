# A4T-C

An open-source 8-toolhead toolchanger for 3D printers, built around the [A4T toolhead](https://github.com/Armchair-Heavy-Industries/A4T).

This is currently in active development, so all files are likely to change. The current version is tested and working but is still considered BETA. 

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

## Before you build

> [!IMPORTANT]
> A toolchanger needs more control electronics and much more power than a single-toolhead printer. Read both sections below before you buy parts.

### 1. You need additional MCU outputs

Every tool needs its **own dedicated** pins on a controller:

- a heater output
- a thermistor input
- fan outputs (hotend fan and part-cooling fan)

These **cannot be shared** between tools. Most printer main boards have only a few heater outputs, and that number caps how many tools you can run. To run A4T-C, or any other toolchanger, plan on a **separate MCU** to control the tools, such as a spare main board with extra heater outputs.

### 2. You need a much larger power supply

A toolchanger's power demand is substantial. A typical 200 W power supply **will be overloaded quickly**, which can cause it to shut down, fail, or worse. You need one of these:

- **Replace** your power supply with one rated for the number of tools you plan to run, or
- **Add a second** power supply dedicated to the tools.

### Reference power calculation

> [!WARNING]
> **This calculation is for reference only.** You are responsible for calculating your own printer's power requirements using the actual ratings of your parts, and you build and operate your printer **at your own risk**.

Plan for the worst case: **every tool heating at the same time**, as can happen when all tools preheat at the start of a print.

```
Tool load    = number of tools × (heater W + fan W per tool)
Total load   = tool load + base printer load
Minimum PSU  = total load × 1.25        (25% safety margin)
```

- **Heater W:** the wattage printed on your heater cartridge. 24 V hotend heaters are commonly 40–60 W, and high-flow heaters can be higher.
- **Fan W per tool:** the hotend fan plus the part-cooling fan. Volts × amps from the fan's label. High-output blowers can draw 10 W or more.
- **Base printer load:** stepper motors, main board(s), host computer, and lights. Use your own figure. 75 W is used below as a placeholder.
- **Heated bed:** if your bed is a DC bed on the same supply, add its full rated wattage. An AC (mains) bed does not draw from the DC supply.

**Example: 8 tools, 24 V, 60 W heaters, 10 W of fans per tool, AC bed**

| | Calculation | Result |
| --- | --- | --- |
| Tool load | 8 × (60 W + 10 W) | 560 W |
| Base printer load | placeholder | 75 W |
| Total load | 560 W + 75 W | 635 W |
| Minimum PSU rating | 635 W × 1.25 | **~800 W** |
| Current at 24 V | 635 W ÷ 24 V | ~26.5 A |

The current is why supply size alone isn't enough. Your wiring, connectors, and fuses must also be rated for the current they will carry.

## Scope

This repository covers the **hardware** side of A4T-C: CAD, printable parts, PCBs, and the bill of materials.

Klipper macros, printer configs, and the Mosaic tools will live in a separate repository, which will be linked here once it has a name.

## Files

| Path | Contents |
| --- | --- |
| [`CAD/A4T-C_BETA_Release.step`](CAD/A4T-C_BETA_Release.step) | Full A4T-C assembly (STEP AP214), BETA release |

## Bill of materials

The BOM for the main toolhead and the additional toolheads is kept as a live Google Sheet:
**[A4T-C BOM (Google Sheets)](https://docs.google.com/spreadsheets/d/1BpOGoed5-w5looXP_i0q-_DWB_vuSzNozRO246CXfhI/edit?gid=0#gid=0)**

The BOM is maintained by Discord user **kral_pivex**. The sheet is the most current version; refer to it rather than to any copy.

## Project creators

- **[@Slimohan](https://github.com/Slimohan)**
- **[@cdanisor](https://github.com/cdanisor)**

The full list of credits is in [AUTHORS.md](AUTHORS.md).

## Based on A4T

A4T-C is a derivative of **A4T**, a toolhead designed by [DW-Tas](https://github.com/DW-Tas) and published by [Armchair Heavy Industries](https://github.com/Armchair-Heavy-Industries/A4T).
The original A4T project also credits:

- The Crew and Contributors at Voron Design
- [yellowfish543](https://github.com/yellowfish543/StdToolheadOpenfoam/) for CFD insights
- weaslus, for the name "backflow inhibitors"
- [Corunir](https://github.com/Corunir) for the configurator wizard

If A4T is useful to you, consider supporting DW-Tas through [Ko-fi](https://ko-fi.com/O5O5OCC0K).

A4T-C is an independent derivative. The original A4T creators do not endorse it.

## License

This work is licensed under the same license as A4T:
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].
The full text is in [LICENSE](LICENSE).

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

The A4T project clarifies its non-commercial term as follows. The term covers cases where the design itself is the product: selling it as a product requires a commercial license from the original creators. Using it in a printer that provides commercial services, such as a print farm, is allowed.

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
