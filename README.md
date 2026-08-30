# USB-A Physical Isolation Switch
---

## 📢 Current Update 
## (August 30, 2026)
### Overview & current update link: https://docs.google.com/document/d/1pLDk2mAq172Uoo87mN2TMu-KEBSsqmwrNO6xUET-iXo/edit?usp=drive_link

**Ver 2.0 Final Fabrication Release & Design Freeze**
* **TVS ESD Protection Integration**: Integrated an industrial-grade **SRV05-4** TVS diode array to clamp electrostatic discharge and voltage spikes during hot-plugging.
* **$D+/D-$ Signal Tuning**: Executed single-track serpentine length tuning on differential signal traces, achieving **$0.00\text{ mm}$ skew** to optimize USB 2.0 signal integrity.
* **100% Single-Sided Top Placement**: Re-engineered component placement, consolidating all connectors, switches, TVS ICs, and LEDs onto the Top Layer ($	ext{F.Cu}$) for an improved visual aesthetic and lower-cost single-sided SMT reflow.
* **Ground Copper Pour**: Replaced thin discrete ground tracks with continuous Top and Bottom Ground Planes to minimize impedance and lower EMI.
* **Manufacturing Package**: All production Gerber files, drill files have been verified via KiCAD DRC (0 Errors) and packaged for fabrication.

---

##  Product Overview

The **USB-A Physical Isolation Switch** is an air-gapped hardware security and power management device designed in KiCAD 9.0. Unlike software-based toggles that rely on OS drivers and remain vulnerable to remote exploits, this hardware module provides a physical "hard-cut" for USB-connected peripherals. It ensures absolute data privacy, prevents unauthorized data exfiltration, and offers convenient hardware resetting without the mechanical wear of repeated plugging/unplugging.

note: content will change over time based on latest updates

---

##  Key Features

* **Air-Gapped Privacy & Security**: Physical DPDT switch physically breaks $V_{BUS}$ power and $D+$ data lines for 100% reliable hardware-level isolation.
* **Sub-Nanosecond ESD Protection**: Integrated **SRV05-4** TVS diode array clamps voltage transients across $V_{BUS}$, $D+$, and $D-$ lines.
* **Matched Differential Pair ($0.00\text{ mm}$ Skew)**: Serpentine length tuning compensates for trace length differences caused by switch cutouts, maintaining data integrity.
* **Single-Sided SMT Layout**: Unified component layout on the top side simplifies assembly and provides a clean, professional finish.
* **Solid Grounding & EMI Reduction**: Continuous Ground Copper Pour (GND Zone) on both layers reduces ground loop impedance and improves heat dissipation.
* **Dual-LED Status Indication**:
  * 🟢 **Green LED ($ON\_GREEN$)**: Active connection ($V_{BUS}$ and data lines fully connected).
  * 🔴 **Red LED ($OFF\_RED$)**: Isolated/OFF state ($V_{BUS}$ disconnected from downstream port, routing through a $220\,\Omega$ resistor).

---

## 📁 File content

```text
.
├── final.zip                            # Complete manufacturing package (All Gerbers, Drill files etc)
├── USB-A switch overview.pdf            # Initial Ver 1.0 baseline documentation & overall project concept https://docs.google.com/document/d/1pLDk2mAq172Uoo87mN2TMu-KEBSsqmwrNO6xUET-iXo/edit?usp=drive_link
├── USB-A switch ver-xx.xx_update.pdf    # Updating report detailing new elements, technical iteration & design rationale https://docs.google.com/document/d/1X9TlPd9sVfkH2GCSMDSQgF4tiR_iDZ1_ytxDP3pgHG8/edit?usp=sharing
├── new_KiCAD_thing.kicad_pcb            # KiCAD PCB layout source file
├── new_KiCAD_thing.kicad_sch            # KiCAD schematic source file
├── PCB.png                              # High-resolution PCB Layout diagram preview
├── Schematic.png                        # High-resolution Schematic diagram preview
└── README.md                            # Project documentation
```


## 👤 Author & Acknowledgments

* **Author**: Haoyang Jiang
* **Date**: August 30, 2026
* **Designed With**: KiCAD EDA 9.0

---
