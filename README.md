\# AmpBatt Dock-2p



An open source 2×18650 power bank designed by the Ampnics community.



!\[AmpBatt Dock-2p 3D render](docs/render.png)



| | |

|---|---|

| \*\*Hardware revision\*\* | v0.1.0 (October 2026) |

| \*\*Designer\*\* | Md Ammar Maniyar, Ampnics |

| \*\*Design tool\*\* | KiCad 10 |

| \*\*Status\*\* | Prototype, not yet tested (TODO: update) |



\## Overview



AmpBatt Dock-2p is a compact power bank board built around the \*\*IP5306\*\* charge-and-boost power management IC. It holds two 18650 lithium-ion cells in a PCB-mounted holder, charges them over USB-C and supplies 5 V to devices through a USB-A port.



\## Features



\- \*\*Output:\*\* 5 V DC, up to 2.4 A through a USB-A connector

\- \*\*Charging input:\*\* USB-C receptacle, power only (5.1 kΩ CC resistors)

\- \*\*Battery:\*\* 2 × 18650 cells (BK-18650-PC holder, cells in parallel – TODO: confirm)

\- \*\*Switching frequency:\*\* 500 kHz boost converter with a 1 µH inductor

\- \*\*Charge indicator:\*\* 4 LEDs showing about 25 %, 50 %, 75 % and 100 %

\- \*\*User control:\*\* push button for wake-up / output on-off (SW1)

\- \*\*Expansion:\*\* 2-pin header (J3), TODO: describe its purpose



\## Repository layout



| Path | Contents |

|---|---|

| `ABD\_v01.kicad\_pro` | KiCad project file |

| `ABD\_v01.kicad\_sch` | Schematic |

| `ABD\_v01.kicad\_pcb` | PCB layout |

| `eeschema/` | Schematic-related files |

| `ext lib/` | External symbol and footprint libraries |

| `ext 3d/` | 3D models |

| `docs/` | Documentation and images |



\## Getting started



1\. Install \[KiCad](https://www.kicad.org/) 10 or newer.

2\. Clone this repository:

```bash

&#x20;  git clone https://github.com/ampnics/AmpBatt-Dock-2p.git

```

3\. Open `ABD\_v01.kicad\_pro` in KiCad.

4\. If symbols, footprints or 3D models show as missing, check

&#x20;  \*\*Preferences → Manage Symbol/Footprint Libraries\*\* and make sure paths use `${KIPRJMOD}`.



\## Manufacturing



Gerber and drill files are published under

\[Releases](../../releases) for each hardware version.

Suggested PCB settings: TODO (layers, thickness, finish, copper weight).



\## Safety warning



This design charges and discharges lithium-ion cells. Incorrect assembly, damaged cells, short circuits or poor cell quality can cause fire or injury.

\- Use only protected, genuine 18650 cells from a reputable source.

\- Never leave charging batteries unattended.

\- This is an early prototype and comes with no warranty.

\- Build and use it at your own risk.



\## Known limitations / roadmap



\- TODO: list tested and untested items

\- TODO: planned changes for v0.2.0



\## Contributing



Issues and pull requests are welcome. Please describe what you changed and why, and which hardware revision it applies to.



\## License



\- \*\*Hardware design files\*\* (schematics, PCB, libraries made by the authors): \[CERN-OHL-S-2.0](LICENSE)

\- \*\*Documentation and images:\*\* \[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

\- Third-party libraries and 3D models in `ext lib/` and `ext 3d/` keep their original licenses.



© 2026 Ampnics community

