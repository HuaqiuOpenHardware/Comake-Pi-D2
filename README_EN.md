<h1 align="center">Comake Pi D2</h1>

<p align="center"><strong>Low-power edge AI development board based on SigmaStar SSC309QL</strong></p>

<p align="center">
  <strong>English</strong> |
  <a href="README.md">简体中文</a>
</p>

<p align="center">
  <a href="https://p.eda.cn/d-1377570469779079168">Original project</a> ·
  <a href="https://doc.comake.online/d2_sigdoc_en/customer/IPC/EnvironmentSetup/get_started_en.html">Official docs</a> ·
  <a href="hardware/pcb/">Hardware</a> ·
  <a href="hardware/bom/">BOM</a> ·
  <a href="docs/">Documents</a>
</p>

<p align="center">
  🛠️ <a href="https://github.com/HuaqiuOpenHardware/Comake-Pi-D2/issues/new">Report an issue</a>
  &nbsp;·&nbsp;
  ⭐ <a href="https://github.com/HuaqiuOpenHardware/Comake-Pi-D2">Star this project</a>
</p>

![Comake Pi D2 edge AI development board](assets/images/cover.png)

Comake Pi D2 is a compact edge AI development board from SigmaStar for portable cameras, AI wearables, smart-home devices and drones. This repository organizes the V1.0 and V2.0 hardware packages, core-board and carrier-board designs, BOMs, hardware guides and SSC309QL documentation for discovery, reproduction and derivative development.

> This repository contains multiple hardware revisions. Confirm the V1.0/V2.0 revision, core/carrier board and audio configuration before design or fabrication. Do not mix schematics, PCBs, BOMs and guides from different revisions.

## At a glance

| Item | Details |
| --- | --- |
| Main platform | SigmaStar SSC309QL |
| CPU | Dual Arm Cortex-A32 up to 1 GHz, plus a 200 MHz Cortex-M4 coprocessor |
| AI acceleration | 1.5 TOPS NPU, according to the original project and official documentation |
| Memory | 256 MB LPDDR4x |
| Software | Linux / Alkaid SDK ecosystem |
| Interfaces | MIPI RX, UART, I2C, SPI, PWM, SAR ADC, USB 2.0, eMMC/SDIO and RTC |
| Hardware assets | V1.0/V2.0 packages, core board, carrier board, BOM, PCB, schematic and guides |

These specifications are documentation references, not independent measurements by the repository maintainers. Verify power, AI performance, camera capability and compatibility against the exact hardware revision and official documentation.

## Choose the correct package

| Revision/resource | Entry point | Purpose |
| --- | --- | --- |
| V1.0 Demo | [`Comake-Pi-D2-V1.0_BGA8_9.5_Demo_20251215.zip`](hardware/pcb/Comake-Pi-D2-V1.0_BGA8_9.5_Demo_20251215.zip) | V1.0 source package and extracted files |
| V2.0 full Demo | [`Comake-Pi-D2-V2.0_BGA8_9.5_Demo_20260409.zip`](hardware/pcb/Comake-Pi-D2-V2.0_BGA8_9.5_Demo_20260409.zip) | Combined V2.0 package and guides |
| V2.0 core board | [`Comake-Pi-D2-V2.0_核心板.zip`](hardware/pcb/Comake-Pi-D2-V2.0_核心板.zip) | Core-board design package |
| V2.0 carrier board | [`Comake-Pi-D2-V2.0_载板.zip`](hardware/pcb/Comake-Pi-D2-V2.0_载板.zip) | Carrier-board design package |
| BOM | [`hardware/bom/`](hardware/bom/) | D2 and mainboard bills of materials |
| SSC309QL guide | [`SSC309QL_HW_USER_GUIDE_20251225.pdf`](docs/SSC309QL_HW_USER_GUIDE_20251225.pdf) | Chip hardware reference |
| Reading guide | [`资料阅读指南V1.1.pdf`](docs/资料阅读指南V1.1.pdf) | Recommended first document |
| Provenance | [`MANIFEST.json`](MANIFEST.json) | Original URLs, sizes and SHA256 checksums |

Official materials describe different V2.0 audio-path configurations. For TWS, WQ7036AX or SSC309QL audio routing, verify the physical board, BOM and revision-specific guide rather than relying on the “V2.0” label alone.

## Getting started

1. Read the [official quick start](https://doc.comake.online/d2_sigdoc_en/customer/IPC/EnvironmentSetup/get_started_en.html).
2. Select one hardware revision and keep its schematic, PCB, BOM, reference-designator drawing and I/O map together.
3. Use the original ZIP for provenance and the extracted files for browsing; duplicated content does not represent a separate revision.
4. Before fabrication, review substitutions, connector orientation, power, boot configuration, high-speed interfaces and RF-related design.
5. Label derivatives precisely as reviewed, fabricated or bench-tested. Do not present inferred behavior as a measurement.

## Repository layout

```text
.
├── assets/images/        # Cover and community images
├── docs/                 # SSC309QL and reading guides
├── enclosure/            # Mechanical-file status
├── hardware/
│   ├── bom/              # D2 and mainboard BOMs
│   └── pcb/              # V1.0/V2.0 packages and extracted files
├── MANIFEST.json         # Source URLs, sizes and SHA256 checksums
├── REVIEW_CHECKLIST.md
├── README.md
└── README_EN.md
```

## License and reuse boundary

The original Huaqiu Open Hardware Community page lists **GPL 3.0**. The repository also contains hardware designs, chip documentation, Office/PDF files and other upstream materials that may retain separate copyright notices or usage terms.

Before copying, modifying, manufacturing, redistributing or commercially using the materials, preserve upstream notices, inspect revision packages for separate terms, and confirm unclear rights with the project owner. Do not assume that every third-party document is GPL-3.0 solely because the project page displays that license.

## Community support

Scan the QR code to contact the **Huaqiu Open Hardware Assistant** for repository navigation, community-group access and project feedback guidance.

<p align="center">
  <img src="assets/images/wechat-assistant-qr.png" width="220" alt="Huaqiu Open Hardware Assistant WeChat QR code">
</p>

<p align="center"><strong>Include “Comake Pi D2” in your WeChat request.</strong></p>

## Sources and discovery terms

- Original project: [SigmaStar AI Development Board Comake Pi D2](https://p.eda.cn/d-1377570469779079168)
- Official documentation: [Comake Pi D2 Quick Start](https://doc.comake.online/d2_sigdoc_en/customer/IPC/EnvironmentSetup/get_started_en.html)

Related terms: Comake Pi D2, SigmaStar, SSC309QL, WQ7036AX, edge AI, AI development board, AI glasses, embedded Linux, NPU, hardware design, PCB, schematic and BOM.
