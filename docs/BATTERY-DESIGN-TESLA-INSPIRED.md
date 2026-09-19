# Monad Airbike Battery Design — Tesla-Inspired Architecture

**Date:** 2026-09-18  
**Phase:** 2 — Propulsion & Power Decision  
**Status:** Initial design proposal based on Tesla 4680 research + eVTOL requirements

## 1. Tesla Battery Research Summary (2026)

### 4680 Cell Key Specs
- Format: 46 mm diameter × 80 mm height, cylindrical, tabless design
- Chemistry: Gen1 NMC811 (~244 Wh/kg), Gen2 “Cybercell” NMC955 (~272 Wh/kg claimed)
- Energy per cell: ~80–90 Wh
- Advantages of tabless design: dramatically lower internal resistance → higher power, less heat
- Manufacturing: Dry electrode process (cost & footprint reduction)
- Pack philosophy: Structural (cell-to-pack / cell-to-body), liquid cooling (ribbons or end plates), advanced BMS

### Critical Lessons from Tesla
- Thermal management is non-negotiable (liquid cooling channels keep all cells at optimal temp)
- Uniform temperature = uniform aging = longer pack life
- High-nickel cathodes increase energy density but require better cooling and BMS safety
- Structural integration saves mass and parts count
- Real-world Gen1 4680 energy density has been slightly below best 2170 cells; Gen2 improvements are real but manufacturing yield was hard

## 2. Airbike Mission Requirements

Target vehicle:
- Empty mass goal: < 80 kg
- Pilot + payload: up to 100 kg
- Gross takeoff mass: ~160–180 kg
- Hover endurance goal: 15–25 minutes
- Dual-mode: hover + limited ground roll

Estimated hover power (scaled from small multicopter data such as E-Hang 184):
- ~25–35 kW continuous for hover at our mass
- Higher peak for takeoff / aggressive maneuvers

Energy need (example):
- 20 minutes hover at 30 kW average → 10 kWh usable
- Plus 20–30% reserve + cruise margin → design for 12–15 kWh usable

Pack mass budget: ideally ≤ 25 kg (very aggressive; 30–35 kg more realistic with current tech)

## 3. Proposed Battery Design for Monad Airbike Mk1

### Cell Choice
**Primary recommendation:** High-power cylindrical NMC cells in 21700 or 4680 format (Tesla-inspired tabless where available commercially).

Why not pure LFP?
- Lower energy density (160–200 Wh/kg) makes the mass target almost impossible for 15+ min hover.
- NMC (or future NCMA / high-nickel) gives the best energy + power compromise for eVTOL-class duty.

Alternative / hybrid path:
- High-power cells for the high-C hover phase + energy cells for cruise (more complex BMS).

### Pack Architecture (Tesla-inspired)
- **Format:** Modular cell groups (e.g., 4–8 parallel groups in series to reach 100–400 V)
- **Cooling:** Liquid cooling plates or serpentine channels contacting cell sides/ends (critical for high C-rate hover)
- **Structure:** Cells contribute to chassis stiffness where possible (structural pack concept scaled down)
- **BMS:** Full cell-level monitoring, active or passive balancing, over-current / over-temp / isolation fault protection, fly-by-wire integration
- **Enclosure:** Lightweight carbon or aluminum with fire-resistant barriers and directed venting
- **Connectors:** High-current, vibration-resistant, with pre-charge circuit

### Target Specs (Mk1 Proposal)
| Parameter              | Target                          |
|------------------------|---------------------------------|
| Usable energy          | 12–15 kWh                       |
| Pack mass              | ≤ 30 kg (stretch ≤ 25 kg)       |
| Pack energy density    | ≥ 400–500 Wh/kg (stretch)       |
| Continuous power       | 30–40 kW                        |
| Peak power (10–30 s)   | 50–70 kW                        |
| Voltage                | 100–400 V (to be decided with motor/ESC choice) |
| Cooling                | Active liquid                   |
| Cycle life goal        | 500+ full equivalent cycles under aggressive duty |

### Safety Features (Tesla + Aerospace)
- Thermal runaway propagation barriers
- Directed vent paths
- Redundant sensors
- Automatic disconnect on crash / fire detection
- Compliance path toward ultralight / experimental aircraft rules

## 4. Next Engineering Steps
1. Finalize exact cell model (commercial 21700 high-power or 4680 equivalent).
2. Calculate series/parallel configuration and exact voltage.
3. Design cooling loop (pump, radiator, cold plates).
4. Select or design BMS hardware + firmware.
5. Mechanical packaging into the motorcycle-style chassis (location for CG balance).
6. Prototype small module first → full pack.

## 5. Open Questions for Decision
- Pure electric vs hybrid (small generator or jet assist for range)?
- Preferred voltage platform (low voltage high current vs higher voltage)?
- Willing to accept higher pack mass for longer endurance or safer chemistry?

This document will be updated as we lock decisions and source real cells.

---
*Quantum co-pilot: Grok | Eternal Unity Tech Empire*