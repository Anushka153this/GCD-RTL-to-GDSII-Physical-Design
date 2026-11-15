# GCD Processor — RTL-to-GDSII Physical Design Using OpenROAD

## 1. Project Overview

This project implements the physical design of a Greatest Common Divisor (GCD) processor using the OpenROAD digital implementation flow and the Nangate45 standard-cell library.

The project covers the physical-design stages from a synthesized design through floorplanning, placement, clock and routing stages, parasitic extraction, timing analysis, and layout inspection.

The final layout was exported in GDSII format and inspected using KLayout.

## 2. Tools and Technologies

| Tool / Technology | Purpose |
|---|---|
| OpenROAD | Physical design implementation |
| Yosys | RTL synthesis |
| Nangate45 | Standard-cell library |
| KLayout | GDSII layout inspection and DRC |
| SPEF | Parasitic extraction data |
| SDC | Timing constraints |
| Ubuntu 22.04 / WSL2 | Development environment |

## 3. Physical Design Flow

The following stages were performed:

1. **RTL Synthesis:** Converted the GCD design into a gate-level netlist using Yosys.
2. **Floorplanning:** Defined the core and die dimensions and prepared the floorplan.
3. **Power Distribution Network:** Generated the power distribution structure.
4. **Placement:** Placed standard cells within the floorplan.
5. **Timing Optimization:** Performed timing analysis and optimization.
6. **Global Routing:** Estimated routing paths and checked routing congestion.
7. **Detailed Routing:** Completed detailed interconnect routing.
8. **Parasitic Extraction:** Extracted resistance and capacitance information into SPEF.
9. **Static Timing Analysis:** Evaluated setup and hold timing.
10. **Layout Export and Inspection:** Generated and inspected the GDSII layout using KLayout.
11. **DRC Screening:** Ran the KLayout FreePDK45 DRC rule deck.

## 4. Implementation Results

### Placement and Routing

| Parameter | Result |
|---|---:|
| Technology | Nangate45 |
| Placement utilization | 63% |
| Standard-cell placement rows | 19 |
| Synthesized cell area | 450.604 µm² |
| Placement area | 481 µm² |
| Global-routing nets | 355 |
| Global-routing wire length | 10,598 µm |
| Global-routing vias | 2,890 |
| Global-routing usage | 27.47% |
| Global-routing overflow | 0 |
| Detailed-routing wire length | 8,778 µm |
| Detailed-routing vias | 4,190 |

*Note: These values are from the manual physical-design flow.*

### Static Timing Analysis (Manual Flow)

The timing analysis was performed using a 1.00 ns clock period.

| Parameter | Result
