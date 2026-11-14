# A4T-C

An open-source 8-toolhead toolchanger for 3D printers, built around the [A4T toolhead](https://github.com/Armchair-Heavy-Industries/A4T).

This is currently in active development, so all files are likely to change. The current version is tested and working but is still considered BETA. 

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

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
