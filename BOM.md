# A4T-C Bill of Materials (BETA v4)

The initial BOM was created by Discord user **kral_pivex** as a [Google Sheet](https://docs.google.com/spreadsheets/d/1BpOGoed5-w5looXP_i0q-_DWB_vuSzNozRO246CXfhI/edit?gid=0#gid=0). Thank you!
This file is the BOM for BETA v4. It is based on that sheet, with the BETA v4 changes applied.

There are two lists:

- **[Main toolhead](#main-toolhead):** the main body (extruder, motor, gears) **plus one complete hotend tool**. Build this once.
- **[Additional toolhead](#additional-toolhead):** one more hotend tool. Build one for each extra tool.

Supported hotends: **Phaetus Rapido**, **Phaetus TZ V6**, **Dragon HF** (same mount as the TZ V6) and **X1C**.

> [!IMPORTANT]
> The 2× **M3x16 BHCS** for the dock must be **steel**, because the dock magnets have to attract them. Stainless steel (A2/A4) is not magnetic enough. Do not use it.

## Main toolhead

Includes **one hotend**.

### Electrical components

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 1 | EBB36 CAN v1.1 | 1× hotend output | |
| 1 | NEMA 14 stepper | | |
| 2 | 4010 fan | | |
| 1 | 2510 fan | Hotend fan | |
| 2 | D2F-L microswitch | | |
| 1 | Cartographer Beacon H | | |
| 1 | Hotend: Phaetus Rapido / TZ V6 / Dragon HF / X1C | | |
|---| Below are possible hotend output sources. You don't need all of them, see notes 1 and 2.  | --- | --- | 
| 1 | BTT Octopus v1.1 | 4× hotend outputs | |
| 1 | Pulsar 3D Hydra | 8× hotend outputs | |

### Magnets
> [!IMPORTANT]
> Magnets must be sufficiently strong. Use N52 magnets. Beware, many online sellers advertise weaker magnets as N52 magnets. 

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 2 | D6x6 magnet **or** 4× D6x3 | Dock magnets. Two D6x3 magnets stacked on top of eachother can substitute for one D6x6 magnet | |
| 8 | D6x3 magnet | Coupling | |

### Bearings

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 1 | 623 bearing | | |
| 2 | MR63 2Z bearing | | |
| 3 | D4 bearing ball | Can be harvested from 608 bearings, see note 5 | |

### Gears, shafts, spring

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 2 | Extruder gear 36T | Included in HGX/LGX Gear Set | |
| 1 | Gear 44T / 17T | Included in HGX/LGX Gear Set | |
| 2 | Shaft D3x16 | Included in HGX/LGX Gear Set | |
| 1 | Shaft D4x18 **or** D3x18 | Main gear shaft. D4x18 for the LGX/HGX v1 4 mm pin main body; D3x18 for the LGX/HGX v1 3 mm pin and HGX Lite main bodies. Included in LGX/HGX Gear Set | |
| 1 | Spring | Included in HGX/LGX Gear Set | |
| 6 | Shaft D2x6 | | |
| 1 | Shaft D3x20 | | | 

See note 3 on HGX/LGX gear sets.

### Heat inserts

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 12 | M3x4x5 heat insert | | |

### Screws and nuts

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 4 | M2.5x8 | Hotend screws for Rapido | |
| 4 | M2.5x10 | Hotend screws for TZ V6 / Dragon HF | |
| 2 | M3x16 SHCS | Hotend screws for X1C | |
| 2 | M3 DIN562 nut | Hotend nuts for X1C | |
| 1 | M3x10 SHCS | | |
| 4 | M3x5 SHCS | | |
| 4 | M3x8 SHCS | | |
| 3 | M3x15 SHCS | | |
| 3 | M3x25 SHCS | | |
| 2 | M3x16 SHCS | | |
| 2 | M5x10 SHCS | | |
| 3 | M3x8 BHCS | | |
| 2 | M3x16 BHCS, **steel** | Dock. Must be magnetic | |
| 1 | M3x25 BHCS | | |
| 1 | M3x16 BHCS | | |
| 4 | ST D2.5x8 | | |
| 3 | M5x10 FHCS | | |
| 5 | M5 T-nut | | |
| 2 | M3 T-nut | | |
| 2 | M3 hex nut | | |

## Additional toolhead

One more hotend tool.

### Electrical components

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 1 | 2510 fan | Hotend fan | |
| 1 | D2F-L microswitch | | |
| 1 | Hotend: Phaetus Rapido / TZ V6 / Dragon HF / X1C | | |

### Magnets

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 4 | D6x3 magnet | Coupling | |
| 2 | D6x6 magnet **or** 4× D6x3 | Dock magnets | |

### Bearings

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 3 | D4 bearing ball | Can be harvested from 608 bearings, see note 5 | |

### Screws and nuts

| Qty | Part | Notes | Link |
| ---: | --- | --- | --- |
| 4 | M2.5x8 | Hotend screws for Rapido | |
| 4 | M2.5x10 | Hotend screws for TZ V6 / Dragon HF | |
| 2 | M3x16 SHCS | Hotend screws for X1C | |
| 2 | M3 DIN562 nut | Hotend nuts for X1C | |
| 3 | M5x10 FHCS | | |
| 2 | M5x10 SHCS | | |
| 3 | M3x8 BHCS | | |
| 2 | M3x16 BHCS, **steel** | Dock. Must be magnetic | |
| 4 | ST D2.5x8 | | |
| 5 | M5 T-nut | | |
| 2 | M3 T-nut | | |

## Notes

1. Which controller you need depends on how your printer is already equipped and on the parts you already have. Each hotend needs its **own** heater output: two or more hotends cannot share one output. See [Before you build](README.md#before-you-build).

2. Example controller setups:
   - BTT Octopus + 4× EBB36 = 8 hotends
   - Any main board + Pulsar 3D Hydra = 8 hotends

3. Some of the gears and shafts are included in LGX/HGX gear sets. HGX is an LGX clone. 

4. The hotend screw rows depend on the hotend you choose. Buy only the screws for your hotend. Some hotend kits come with the required hotend screws.

5. 608 bearings typically have 7 balls, although they are slightly smaller than D4 ball bearings (3.969 mm).