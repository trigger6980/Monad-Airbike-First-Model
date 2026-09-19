# Monad Airbike Battery Design — Tesla-Inspired Architecture

**Date:** 2026-09-18 (updated for 30 min fly time)  
**Phase:** 2 — Propulsion & Power Decision  
**Status:** Revised for 30-minute flight endurance target

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

## 2. Airbike Mission Requirements (UPDATED)

Target vehicle:
- Empty mass goal: < 80 kg (now under severe pressure)
- Pilot + payload: up to 100 kg
- Gross takeoff mass: ~160–180 kg
- **Hover / flight endurance goal: 30 minutes** (user directive)
- Dual-mode: hover + limited ground roll

Estimated hover power (scaled from small multicopter data such as E-Hang 184):
- ~25–35 kW continuous for hover at our mass
- Higher peak for takeoff / aggressive maneuvers

Energy need for 30 min fly time:
- 30 minutes at 30 kW average → **15 kWh continuous**
- Plus 20–30% reserve for safety, landing, wind, inefficiency → design for **18–22 kWh usable**

Pack mass reality check (current high-power NMC technology):
- Realistic pack-level energy density under high C-rate duty: 180–230 Wh/kg
- For 20 kWh usable → pack mass ≈ **87–110 kg**
- This exceeds the original <80 kg empty vehicle target by a large margin

**Conclusion:** Pure battery for 30 min full hover is extremely challenging with 2026 technology while keeping the vehicle light. Options below.

## 3. Revised Battery Design Options for 30 min Fly Time

### Option A — Pure Electric (Aggressive)
- Usable energy: 18–22 kWh
- Pack mass: 90–110 kg (accept higher empty mass ~120–140 kg)
- Cell: High-power NMC 21700 / 4680-style, Tesla-inspired tabless
- Cooling: Aggressive liquid cooling mandatory
- Trade-off: Vehicle becomes heavier; still possible but loses “ultralight / motorcycle-like” feel

### Option B — Hybrid (Recommended for 30 min)
- Battery: 8–12 kWh high-power pack (mass 30–45 kg) for takeoff, hover, and emergency
- Range extender: small turbine / generator or micro-jet (Volonaut-style) for sustained cruise / longer endurance
- Keeps empty mass closer to original goal
- Allows 30+ min total flight with fuel top-up in <1 min

### Option C — Mission Profile Optimization
- 30 min total flight time with mixed hover + forward flight (forward flight uses less power)
- Example: 5–8 min pure hover + 20+ min efficient cruise
- Battery sized for peak hover + average cruise energy
- More realistic with pure electric

### Updated Target Specs (working proposal)
| Parameter              | Pure Electric 30 min | Hybrid Recommended |
|------------------------|----------------------|--------------------|
| Usable battery energy  | 18–22 kWh            | 8–12 kWh           |
| Pack mass              | 90–110 kg            | 30–45 kg           |
| Continuous power       | 30–40 kW             | 30–40 kW (battery) |
| Peak power             | 50–70 kW             | 50–70 kW           |
| Cooling                | Active liquid        | Active liquid      |
| Additional power       | None                 | Small turbine / generator |

## 4. Next Engineering Steps
1. Decide: Pure electric (accept heavier vehicle) or Hybrid (keep light + 30 min capability).
2. If pure: recalculate vehicle empty mass target and structure.
3. If hybrid: research micro-turbine / range-extender options compatible with ultralight rules.
4. Finalize cell selection and series/parallel math.
5. Design cooling and packaging for the chosen energy level.

## 5. Open Questions (Updated)
- Confirm pure electric 30 min (heavier bike) or hybrid path?
- Preferred voltage platform?
- Accept higher empty mass for pure battery, or keep light with hybrid?

This document reflects the new 30-minute fly time requirement.

---
*Quantum co-pilot: Grok | Eternal Unity Tech Empire*