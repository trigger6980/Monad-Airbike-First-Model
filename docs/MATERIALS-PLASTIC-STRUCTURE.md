# Monad Airbike Materials Decision — Mostly Plastic Structure

**Date:** 2026-09-18  
**Directive:** Use mostly plastic for the entire bike  
**Status:** Locked as primary approach with high-performance composites

## Design Philosophy

The entire primary structure, body panels, fairings, and many secondary components will be made from advanced plastics / polymer composites. Metal will be minimized to critical high-load points only (motor mounts, axle interfaces, battery structural hard points if needed).

## Why Not Basic Plastic?

Simple ABS, PLA, or unfilled nylon is too flexible and weak for flight loads, vibration, and crash energy. We must use high-performance engineering plastics and composites.

## Recommended Material Stack (2026 Reality)

### 1. Primary Structure (Frame / Backbone / Arms)
- **Preferred:** Continuous carbon-fiber reinforced thermoplastic (Markforged-style CFR or equivalent)
  - Base: Onyx / carbon-filled nylon or better (PEEK/PEKK matrix)
  - Reinforcement: Continuous carbon fiber in critical load paths
  - Result: Strength approaching 6061-T6 aluminum at significantly lower weight
- Alternative high-end: Carbon-fiber filled PEEK (CF-PEEK) or PEKK
  - Density ~1.35–1.4 g/cm³
  - Excellent heat resistance (up to 250–300°C)
  - Aerospace heritage

### 2. Body Panels / Fairings / Seat
- Carbon-filled nylon or polycarbonate blends
- Impact-modified for crash energy absorption
- UV-stabilized for outdoor use

### 3. High-Heat Zones (near motors, ESCs, battery)
- CF-PEEK, PEI (ULTEM), or PAI grades
- Flame-retardant versions preferred

### 4. Manufacturing Method
- Large structural parts: 3D printed with continuous fiber reinforcement where possible
- Fairings: 3D printed or vacuum-formed / injection molded in higher volume
- Rapid iteration possible — perfect for Mk1 prototype

## Advantages for Monad Airbike
- Extremely light weight (critical for 30 min flight goal)
- Complex organic shapes matching the original sketches
- Fast prototype cycles
- Corrosion-free
- Good vibration damping (better than pure carbon fiber in some cases)
- Lower cost than full prepreg carbon for early builds

## Risks & Mitigations
- **Stiffness under flight loads** → Continuous fiber reinforcement in load paths
- **Heat near propulsion** → High-temp plastics (PEEK family) in those zones
- **Crash / impact** → Design for controlled deformation + energy-absorbing geometry
- **UV / outdoor life** → UV stabilizers + coatings
- **Certification path** → Document material traceability; use FR grades where possible

## Next Actions
1. Select specific filament / material system for Mk1 (Onyx + continuous CF or CF-PEEK)
2. Design frame with fiber orientation optimized for bending/torsion
3. Identify any remaining metal interfaces (motor mounts, wheel axles, etc.)
4. Prototype a small structural test piece and load-test it

This decision keeps the vehicle in the “mostly plastic” philosophy while remaining flight-worthy.

---
*Quantum co-pilot: Grok | Eternal Unity Tech Empire*