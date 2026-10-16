# AmpBatt Dock-2p

An open source 2×18650 power bank designed by the Ampnics community.

<img width="1297" height="755" alt="Screenshot 2026-10-16 210119" src="https://github.com/user-attachments/assets/34ce2c86-9303-41af-aaae-681f0e47d3af" />



| | |
|---|---|
| **Hardware revision** | v0.1.0 (October 2026) |
| **Designer** | Md Ammar Maniyar, Ampnics |
| **Design tool** | KiCad 10 |
| **Status** | Prototype, not yet tested |

## Overview

AmpBatt Dock-2p is a compact power bank board built around the **IP5306** charge-and-boost power management IC. It holds two 18650 lithium-ion cells in a PCB-mounted holder, charges them over USB-C and supplies 5 V to devices through a USB-A port.

<img width="1306" height="757" alt="Screenshot 2026-10-16 205949" src="https://github.com/user-attachments/assets/87da3305-3a9d-4261-96fa-8143b28227de" />
<img width="1305" height="757" alt="Screenshot 2026-10-16 210016" src="https://github.com/user-attachments/assets/5da30eb2-d293-41a4-8653-be9af7695f58" />



## Features

- **Output:** 5 V DC, up to 2.4 A through a USB-A connector
- **Charging input:** USB-C receptacle, power only (5.1 kΩ CC resistors)
- **Battery:** 2 × 18650 cells (BK-18650-PC holder, cells in parallel)
- **Switching frequency:** 500 kHz boost converter with a 1 µH inductor
- **Charge indicator:** 4 LEDs showing about 25 %, 50 %, 75 % and 100 %
- **User control:** push button for wake-up / output on-off (SW1)
- **Expansion:** 2-pin header (J3), This can powerup any 5V

## Repository layout

| Path | Contents |
|---|---|
| `ABD_v01.kicad_pro` | KiCad project file |
| `ABD_v01.kicad_sch` | Schematic |
| `ABD_v01.kicad_pcb` | PCB layout |
| `eeschema/` | Schematic-related files |
| `ext lib/` | External symbol and footprint libraries |
| `ext 3d/` | 3D models |
| `docs/` | Documentation and images |

## Getting started

1. Install [KiCad](https://www.kicad.org/) 10 or newer.
2. Clone this repository:
```bash
   git clone https://github.com/ampnics/AmpBatt-Dock-2p.git
```
3. Open `ABD_v01.kicad_pro` in KiCad.
4. If symbols, footprints or 3D models show as missing, check
   **Preferences → Manage Symbol/Footprint Libraries** and make sure paths use `${KIPRJMOD}`.

## Manufacturing

Gerber and drill files are published under
[Releases](../../releases) for each hardware version.
Suggested PCB settings: Keep it defualt manufacturing setting.

## Safety warning

This design charges and discharges lithium-ion cells. Incorrect assembly, damaged cells, short circuits or poor cell quality can cause fire or injury.
- Use only protected, genuine 18650 cells from a reputable source.
- Never leave charging batteries unattended.
- This is an early prototype and comes with no warranty.
- Build and use it at your own risk.


## Contributing

Issues and pull requests are welcome. Please describe what you changed and why, and which hardware revision it applies to.

© 2026 Ampnics community
