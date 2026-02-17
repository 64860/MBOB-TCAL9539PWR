```markdown
# ⚡ MBOB-TCAL9539PWR

<div align="center">

![MBOB-TCAL9539PWR Render](Images/main_render.png) <!-- TODO: Add an actual render or photo of the PCB from the Images folder -->

[![GitHub stars](https://img.shields.io/github/stars/64860/MBOB-TCAL9539PWR?style=for-the-badge)](https://github.com/64860/MBOB-TCAL9539PWR/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/64860/MBOB-TCAL9539PWR?style=for-the-badge)](https://github.com/64860/MBOB-TCAL9539PWR/network)
[![GitHub issues](https://img.shields.io/github/issues/64860/MBOB-TCAL9539PWR?style=for-the-badge)](https://github.com/64860/MBOB-TCAL9539PWR/issues)
[![GitHub license](https://img.shields.io/github/license/64860/MBOB-TCAL9539PWR?style=for-the-badge)](LICENSE) <!-- TODO: Add a LICENSE file (e.g., MIT, CERN OHL) -->

**KiCad Design Files for a 16-bit I2C I/O Expander Breakout Board with Power-Up Reset (TCAL9539)**

</div>

## 📖 Overview

This repository contains the complete open-source hardware design files for the MBOB-TCAL9539PWR, a breakout board based on the **Texas Instruments TCAL9539**. The TCAL9539 is a high-performance 16-bit I2C I/O expander featuring power-up reset functionality, ensuring all I/O pins are at a known state (high-impedance) upon power-up.

This project aims to provide a reliable and easy-to-integrate solution for extending the General Purpose Input/Output (GPIO) capabilities of microcontrollers via the I2C interface, particularly for applications where a predictable startup state is crucial. The design includes both the schematic and PCB layout, ready for prototyping and integration into larger systems.

## ✨ Key Features & Specifications

-   🎯 **TCAL9539 Integration:** Designed around the [Texas Instruments TCAL9539 16-bit I2C I/O Expander](tcal9539.pdf) with power-up reset.
-   🔌 **I2C Interface:** Standard two-wire I2C communication protocol for easy interfacing with any microcontroller.
-   💡 **16 GPIO Pins:** Provides 16 general-purpose input/output pins, configurable as input or output.
-   ⚙️ **Power-Up Reset Functionality:** Ensures all I/O pins are in a high-impedance state immediately after power-up, preventing unintended initial states.
-   📐 **KiCad Design:** All design files are provided in the widely used KiCad EDA Suite format, enabling easy viewing, modification, and manufacturing.
-   📄 **Datasheet Included:** The TCAL9539 datasheet (`tcal9539.pdf`) is included for quick reference.

## 🛠️ Hardware Stack

**Design Software:**
-   [![KiCad](https://img.shields.io/badge/KiCad-EDA%20Suite-blue?style=for-the-badge&logo=kicad)](https://www.kicad.org/)

**Key Integrated Circuit:**
-   [![Texas Instruments](https://img.shields.io/badge/Texas%20Instruments-TCAL9539-blue?style=for-the-badge&logo=texas-instruments)](https://www.ti.com/product/TCAL9539) (16-bit I2C I/O Expander with Power-Up Reset)

## 📁 Project Structure

```
MBOB-TCAL9539PWR/
├── Images/                                 # Renders and images of the PCB (e.g., main_render.png)
├── MBOB-TCAL9539PWR-backups/               # Automatic KiCad project backup files
├── MBOB-TCAL9539PWR.kicad_pcb              # Main PCB layout file
├── MBOB-TCAL9539PWR.kicad_prl              # KiCad project-local preferences and settings
├── MBOB-TCAL9539PWR.kicad_pro              # Main KiCad project file (entry point)
├── MBOB-TCAL9539PWR.kicad_sch              # Main schematic file
├── SM04B-SRSS-TB(LF)(SN)--3DModel-STEP-269445.STEP # 3D model for a specific connector (likely JST SM04B-SRSS-TB)
├── fp-info-cache                           # KiCad footprint information cache file
└── tcal9539.pdf                            # Datasheet for the TCAL9539 IC
```

## 🚀 Getting Started with the Design

### Prerequisites
To open and work with these design files, you will need:
-   **KiCad EDA Suite:** Version 7.x or later is recommended.
    -   [Download KiCad](https://www.kicad.org/download/)

### Opening the Project

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/64860/MBOB-TCAL9539PWR.git
    cd MBOB-TCAL9539PWR
    ```

2.  **Open KiCad:** Launch the KiCad EDA Suite application.

3.  **Load the Project:**
    *   In the KiCad Project Manager, go to `File > Open Project...`
    *   Navigate to the directory where you cloned the repository.
    *   Select the `MBOB-TCAL9539PWR.kicad_pro` file and click "Open".

Once the project is loaded, you can open the schematic (`.kicad_sch`) using the Schematic Editor and the PCB layout (`.kicad_pcb`) using the PCB Editor.

## ⚙️ Manufacturing Files (Gerbers, BOM, Pick-and-Place)

To produce the board, you will need to generate manufacturing output files from KiCad. These files are typically not stored in the repository but generated on demand.

1.  **Open the project** in KiCad as described above.
2.  **Generate Gerbers & Drill Files (for PCB fabrication):**
    *   Open the PCB Editor (`MBOB-TCAL9539PWR.kicad_pcb`).
    *   Go to `File > Plot...`.
    *   Configure output directory, select desired layers (e.g., F.Cu, B.Cu, F.SilkS, B.SilkS, F.Mask, B.Mask, Edge.Cuts), and ensure Gerber format is selected. Click "Plot".
    *   Click "Generate Drill File" to create the necessary drill files.
3.  **Generate BOM (Bill of Materials - for component purchasing):**
    *   Open the Schematic Editor (`MBOB-TCAL9539PWR.kicad_sch`).
    *   Go to `Tools > Generate Bill of Materials...`
    *   Select your preferred output format (e.g., CSV, HTML) and click "Generate".
4.  **Generate CPL (Centroid / Pick & Place File - for automated assembly):**
    *   Open the PCB Editor (`MBOB-TCAL9539PWR.kicad_pcb`).
    *   Go to `File > Fabrication Outputs > Footprint Position (.pos) File...`.
    *   Configure settings like units and format, then click "Generate Position File".

## 🤝 Contributing

We welcome contributions from the hardware and open-source community! If you have suggestions for improvements, bug fixes, or new features, please follow these steps:

1.  **Fork** this repository.
2.  **Create a new branch** for your proposed changes (e.g., `feature/improved-power-routing` or `fix/typo-in-silk`).
3.  **Make your modifications** using KiCad.
4.  **Commit your changes** with clear and concise messages.
5.  **Push your branch** to your forked repository.
6.  **Open a Pull Request** against the `main` branch of this repository.

Please ensure your KiCad version is compatible with the project, and consider documenting any significant design decisions.

## 📄 License

This project is licensed under [LICENSE_NAME] - see the [LICENSE](LICENSE) file for details. <!-- TODO: Add a LICENSE file, e.g., MIT License for general hardware/software projects, or CERN Open Hardware Licence (OHL) for strictly hardware-focused projects. -->

## 🙏 Acknowledgments

-   **Texas Instruments** for the robust TCAL9539 I/O expander.
-   **KiCad EDA Suite** for providing an exceptional open-source platform for electronic design automation.

## 📞 Support & Contact

-   🐛 Issues: Feel free to report any issues or ask questions on the [GitHub Issues page](https://github.com/64860/MBOB-TCAL9539PWR/issues).

---

<div align="center">

**⭐ Star this repo if you find this hardware design helpful for your projects!**

Made with ❤️ by [64860](https://github.com/64860)

</div>
```
