# Changelog

All notable changes to the A4T-C hardware are listed here, newest first.

## BETA v4

### Added

- **Printable parts.** STL files are now published in the repository, in [`STL/`](STL).
- **Dragon HF hotend support.** The TZ v6 hotend mount and cover now also fit the Dragon HF.
- **HGX Lite extruder kit support.** Bearing versions of the main module and left cover are in [`STL/Main Body/HGX Lite/`](<STL/Main Body/HGX Lite>).
- **Multicolor Rapido covers.** Covers for tools T0–T4 are in [`STL/Hotends/Rapido/Multicolor Covers/`](<STL/Hotends/Rapido/Multicolor Covers>), as 3MF files.
- **BOM in the repository.** [BOM.md](BOM.md) is based on the initial community BOM created by Discord user **kral_pivex**. Thank you! Changes from that sheet:
  - The main toolhead list now states that it includes one complete hotend tool.
  - Added Dragon HF as a hotend option. It uses the same mount and screws as the TZ V6.
  - Added 2× M3x8 BHCS and 2× M3 T-nut to each hotend tool, including the one in the main toolhead.
  - Dock magnets: 2× D6x6 **or** 4× D6x3.
  - The dock screws changed from 2× M3x20 BHCS to 2× **M3x16 BHCS**. They must be **steel**, so the dock magnets attract them.
  - The heat inserts are now specified as **M3x4x5**.

### Changed

- **Tolerances revised** across the printed parts.
- **CAD split into separate STEP files.** Instead of one full assembly, the CAD is now:
  - [`CAD/A4T-C Main Body.step`](<CAD/A4T-C Main Body.step>): the main body
  - [`CAD/Rapido_Hotend.step`](CAD/Rapido_Hotend.step): Rapido hotend variant
  - [`CAD/TZ v6 Dragon HF Hotend.step`](<CAD/TZ v6 Dragon HF Hotend.step>): TZ v6 / Dragon HF hotend variant
  - [`CAD/X1C Hotend.step`](<CAD/X1C Hotend.step>): X1C hotend variant

### Removed

- `CAD/A4T-C_BETA_Release_v3.step`. It is replaced by the STEP files above.

### Choosing the main body parts

Print every part in [`STL/Main Body/Common/`](<STL/Main Body/Common>). Then print **one** of these pairs:

| Extruder | Main module | Left cover |
| --- | --- | --- |
| LGX / HGX v1 | `LGX-HGX v1/Main module.stl` | `LGX-HGX v1/Left Cover.stl` |
| HGX Lite kit | `HGX Lite/Main module Bearing.stl` | `HGX Lite/Left Cover Bearing.stl` |

The HGX Lite parts replace only these two parts. All other parts are shared.

## BETA v3

- Gear and coupling realignment.
- Full assembly published as `CAD/A4T-C_BETA_Release_v3.step`.
