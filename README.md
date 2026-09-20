# 446MHz Tape Measure Yagi

A rugged, portable, and high-gain 3-element Yagi-Uda antenna designed for the 70cm amateur radio band (446.000 MHz). It utilizes standard steel tape measure blades for the elements and a fully 3D-printable PLA/PETG main frame.

*(Insert Hero Image: Fully assembled black mount with the Baofeng UV-5R from your /Media folder)*

## Motivation

This project was built to combine a passion for 3D printing with hands-on RF engineering. The antenna is specifically tailored for Amateur Radio Direction Finding (ARDF), commonly known as fox hunting, as well as portable simplex operations. Tape measure elements offer a unique advantage in the field: they are highly directional for tracking signals, but they safely fold and snap back into place when walking through heavy brush or trees.

Beyond field performance, a major goal of this project was to design an accessible, beginner-friendly build that anyone can follow. The completely fastener-free 3D-printed frame allows the antenna to be rapidly assembled for deployments, and quickly disassembled for compact storage in a backpack. 

## Technical Specifications

| Parameter | Value |
| :--- | :--- |
| **Target Frequency** | 446.000 MHz (70cm National Simplex) |
| **Design Methodology** | DL6WU / G3SEK Optimization |
| **Estimated Gain** | ~7.3 dBi |
| **Feed Point Impedance** | ~50 Ohms (Direct RG-58 connection, no matching loop needed) |
| **Active Boom Length** | 208 mm |

## Bill of Materials (BOM)

| Component | Details |
| :--- | :--- |
| **Antenna Elements** | 16mm width steel tape measure |
| **Coaxial Cable** | RG-58 with SMA-Female connector (to match Baofeng UV-5R) |
| **Main Frame & Mounts** | 3D-printed in PLA or PETG (SolidWorks CAD files in `/CAD`) |

*(Note: This is a completely fastener-free design.)*

## Build Guide & Assembly

### 1. Element Cutting & Spacing
*   **Elements:** Cut the tape measure blades to length. The reflector is 347 mm, the director is 286 mm, and the driven element consists of two separate 153 mm halves.
*   **Spacing:** Print the main frame from the `/STL` directory. The correct element spacing (116 mm and 92 mm) is natively built into the CAD geometry. The slots are designed for a friction fit, so simply slide the tape measure blades into place. Mark the exact center point on your reflector and director elements, and slide them in until those marks align with the center alignment point built into the 3D-printed frame.

### 2. Feed Gap & Surface Preparation
*   **Alignment:** Ensure the two halves of the driven element are mounted with exactly an 8 mm air gap between them at the center.
*   **Sanding:** Use sandpaper to completely remove the yellow paint and clear coat from the inner feed-point edges of the driven elements to expose bare steel. *If you do not remove the clear coat, the solder will not bond.*

### 3. Soldering the Coax
*(Insert coax stripping and twisted braid photos from your /Media folder)*
*   **Tinning:** Apply flux and pre-tin the bare steel using a high-wattage iron.
*   **Preparation:** Strip your RG-58 coax, twist the copper shield into a tight pigtail, and pre-tin both the shield and center core. 
*   **Connection:** Solder the center conductor to one side of the 8 mm gap and the shielded pigtail to the other. Ensure they do not physically bridge the gap.
*   **Strain Relief:** Once the solder has completely cooled, apply Loctite 495 between the outer PVC jacket of the coax and the solid printed frame to protect the fragile solder joints from physical stress.

## Field Testing
*(Insert field testing photos against the transmission towers from your /Media folder)*
Ensure you test the antenna on a low power setting (1W) first before attempting full-power transmissions. 

## Repository Structure
*   `/CAD`: SolidWorks source files (`.sldprt`, `.sldasm`) so operators can adapt the mounts for different tape measure widths.
*   `/STL`: Ready-to-print 3D models for the completely 3D-printed main frame and mounts.
*   `/Docs`: 3G-Aerial DL6WU calculator outputs verifying the 116 mm and 92 mm spacing.
*   `/Media`: Build photos, coax soldering close-ups, and field testing documentation.

## License
This open hardware design is licensed under the CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P v2). See the `LICENSE` file for details.
