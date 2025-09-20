# RTL to GDSII Flow: SFAL-VSD Program

This repository documents my step-by-step journey through the complete RTL-to-GDSII flow for digital design, as part of the **VSD RISC-V SoC Tapeout Program**. It serves as a log for tool installations, setup configurations, workflow verification, and project progress.

---

## My Silicon Adventure: The VSD RISC-V Tapeout Journey

A new and exciting chapter begins!

I have embarked on a 10-week adventure to build a System-on-Chip from the ground up as part of the VSD RISC-V SoC Tapeout Program.
This is far more than a structured course; it is a collective movement, uniting thousands of aspiring engineers in a mission to advance India's capabilities in semiconductor design and innovation.

Each week, I will be conquering new parts of the design flow—from crafting RTL designs and synthesizing logic to tackling the intricate challenges of physical layout.
Every step brings us closer to that ultimate milestone: a successful tapeout ready for fabrication.

### Current Progress: Week 0 ✅
**Focus:** Foundation & Setup
This week involved configuring the essential open-source toolchain and laying the groundwork for this deep dive into silicon.
*   Proof of Installation: All required EDA tools have been successfully installed and verified.
*   Environment Setup: The project environment and dependencies are configured for a seamless workflow.

---

## Project Overview & Goals

**Objective:** To successfully implement a digital design from RTL (Register Transfer Level) to GDSII (final layout format) using a full open-source EDA toolchain.

**Key Milestones:**
1.  **RTL Design:** Creation and verification of HDL code.
2.  **Logic Synthesis:** Translating RTL into a gate-level netlist.
3.  **Physical Design:** Floorplanning, Placement, Clock Tree Synthesis, and Routing.
4.  **Verification:** Performing DRC (Design Rule Check) and LVS (Layout vs. Schematic).
5.  **Tapeout Prep:** Final sign-off and GDSII generation.

## Tools and Software

The following open-source tools are used in this flow:

| Tool | Purpose |
| :--- | :--- |
| **Yosys** | Logic Synthesis |
| **OpenLane** | Automated RTL-to-GDSII Flow |
| **GrayWolf** | Placement & Routing |
| **QFlow** | Digital Design Flow |
| **Magic** | VLSI Layout & DRC/LVS |
| **Netgen** | LVS and Netlist Comparison |
| **GTKWave** | Digital Waveform Viewer |


## Acknowledgments

I am truly thrilled to be part of this vibrant community of learners and creators. A special note of gratitude is due to the pioneers at **VSD**, led by **Kunal Ghosh**, for their vision and dedication in making this ambitious initiative possible.

Here is to seamless tapeouts, boundless learning, and pushing the boundaries of what we can achieve together!

Cheers!!
