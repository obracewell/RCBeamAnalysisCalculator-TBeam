# RC Beam Analysis Calculator - Singly Reinforced T-Beam

## Overview
This is a web-based calculator for analyzing singly reinforced T-beams in reinforced concrete design. It calculates:
- Depth of equivalent rectangular stress block (`a`)
- Neutral axis depth (`c`)
- Tension strain in steel reinforcement
- Maximum internal moment (`Mₙ`)
- Design capacity moment (`φMₙ`)

Additionally, the tool plots the stress and strain diagrams of the section for visualization.

---

## Features
- **User Inputs:**
  - Concrete compressive strength (`f'c`) in psi
  - Steel yield strength (`fᵧ`) in psi
  - **Option 1:** Direct input of cross-sectional area of steel (`As`) in in²
  - **Option 2:** Bar size (selectable #3 to #18) and number of bars (auto-calculates `As`)
  - Depth of steel (`d`) in inches
  - Width of beam base (`b`) in inches
  - Web width ('bw') in inches
  - Effective flange width ('beff') in inches
  - Flange Height ('hf') in inches

- **Automatic Checks & Outputs:**
  - Minimum steel area compliance check
  - Tension strain classification (Ductile section, Transition zone, or non-compliant)
  - Case-based calculation for flange/web contributions
  - Full set of calculated parameters displayed
  - Error messages for non-compliant sections (displayed alongside results)

- **Graphical Outputs:**
  - Visualizes the T-beam cross-section
  - Stress diagram
  - Strain distribution
  - Force vectors (tensile and compressive)
  
- Built using **HTML, CSS, JavaScript, and Plotly.js**

---

## How to Use
1. **Open the `HTML` file** in any modern web browser.
2. Enter the required beam properties:
   - Concrete compressive strength (`f'c`)
   - Steel yield strength (`fᵧ`)
   - Either:
     - Directly input steel area (`As`), **OR**
     - Select a bar size and input the number of bars (the calculator will compute `As`)
   - Depth of steel reinforcement (`d`)
   - Width of the beam base (`b`)
   - Web width ('bw') in inches
   - Effective flange width ('beff') in inches
   - Flange Height ('hf') in inches
3. Click **"Calculate"**.
4. View:
   - Calculated values
   - Compliance checks
   - Stress & strain diagram
   
---

## Bar Size to Area Mapping
The following standard bar sizes and their corresponding areas (in²) are supported:

| Bar Size | Area (in²) |
|---------|---------|
| #3      | 0.11    |
| #4      | 0.20    |
| #5      | 0.31    |
| #6      | 0.44    |
| #7      | 0.60    |
| #8      | 0.79    |
| #9      | 1.00    |
| #10     | 1.27    |
| #11     | 1.56    |
| #14     | 2.25    |
| #18     | 4.00    |

---

## Dependencies
- **Plotly.js** (for graph plotting)
  - Included via CDN in the HTML `<head>`:
    ```html
    <script src="https://cdn.plot.ly/plotly-2.24.1.min.js"></script>
    ```

---

This project is free to use and modify. Attribution appreciated.
Developed by Olivia Bracewell (obracewell).
