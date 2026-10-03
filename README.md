# Adaptive Mesh for Shock Capturing in CFD Analysis of Transonic Airfoil RAE2822

> **Academic Project of Excellence — Politecnico di Milano**  
> This repository contains the project for the *Computational Fluid Dynamics* course (A.Y. 2025–2026). The work achieved the **maximum possible score** and was so highly praised by the lecturer (Prof. Barbara Re) that it has been officially selected as a **reference model and practical example for future student**.

## Project Overview
This report presents a steady two-dimensional CFD analysis of the well-known transonic airfoil **RAE2822**, utilizing the open-source software suite **SU2**. The study investigates the complex flow phenomena and aerodynamic load variations induced by shock waves during transonic flight operations.

## Methodology & Computational Setup
*   **Flow Solver**: Steady compressible RANS equations solved via the open-source solver **SU2**.
*   **Adaptive Mesh Refinement**: Starting from an unstructured baseline grid generated with **Gmsh**, a pyAMG-based mesh adaptation strategy driven by Mach number gradients was implemented. This dynamically clustered nodes along shock waves, boundary layers, and wakes while keeping a coarse resolution elsewhere.
*   **Numerical Schemes**: Convective fluxes were discretized using the **Jameson-Schmidt-Turkel (JST)** central scheme with adaptive artificial dissipation to ensure robustness across discontinuities.
*   **Turbulence Modeling**: The one-equation **Spalart-Allmaras (SA)** model was selected to accurately predict shock positions and boundary-layer separation without excessive computational costs.

## Key Results & Validation
*   **Experimental Validation**: The numerical workflow was thoroughly validated against Airbus wind tunnel data (pETW facility, Case 450), showing exceptional agreement in both pressure coefficient ($C_p$) distributions and lift curves.
*   **Mach Sweep Analysis**: Extending the analysis up to supersonic speeds ($M = 1.2$) successfully captured lift and drag coefficient trends, aligning closely with **Prandtl-Glauert** (subsonic) and **Ackeret** (supersonic) linear theories.
*   **Flow Visualization**: High-fidelity **Numerical Schlieren** imaging successfully visualized complex compressible structures, including the detached bow shock wave at $M = 1.2$.
  
## Project Team & Academic Context

## Authors 
*   **Cuman Filippo** 
*   **Falsitta Simone**
*   **Farnetani Carlo**
*   **Fusari Filippo** 
*   **Gandini Simone** 

**Politecnico di Milano 1863**  
*School of Industrial and Information Engineering — M.Sc. in Aeronautical Engineering* (A.Y. 2025–2026)  
**Course**: *Computational Fluid Dynamics*
**Supervisors**: Prof. Barbara Re, Prof. Andrea Rausa  
