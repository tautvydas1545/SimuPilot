# Assetto Corsa GT3 Realism Mod

## Overview

Assetto Corsa is highly regarded for its extensive moddability and has an active modding community. A few modders have attempted to alter the base-game GT3 driving and braking feel, but these efforts typically focus on general realism and do not reach the standard of top sim-racing titles such as iRacing.

Realistic GT3 driving and braking requires significantly more finesse and technique to fully extract the capabilities of these cars. This project aims to produce a mod for Assetto Corsa that brings overall driving and braking behaviour of GT3 cars as close to real-life as possible, while also taking reference from leading sim-racing titles.

---

## Goals

1. **Realistic GT3 driving behaviour** — braking, steering, car control, and overall dynamic feel
2. **Realistic GT3 lap times** — performance envelope consistent with real-world GT3 data
3. **Semi-realistic GT3 setup characteristics** — setup changes produce believable and meaningful effects

---

## Limitations

1. **Assetto Corsa's tyre model** is a key constraint — it is fundamentally different from many modern simulators and less advanced in how it handles combined load, slip, and tyre behaviour at the limit.
2. **The core tyre model is deeply embedded** in the simulation. Parameters and curves can be tuned and behaviour can be mimicked, but only within the bounds of what the Assetto Corsa tyre model architecture allows.

---
 
## Current Status
 
**Phase: v2 physics mod — pending test results**
 
Baseline telemetry testing completed on the unmodified Kunos AMG GT3 (2015) at Monza T1 using MoTeC i2 Pro. Three braking technique tests (A, B, C) were logged, analysed, and CSV-verified against MoTeC. Four key unrealistic behaviours were identified and quantified — longitudinal grip too stable, friction circle not enforced, ABS over-drive carrying no penalty, and proper technique being slower than incorrect technique.
 
A coordinated first physics mod (v2_braking_rework_1) has been implemented across `tyres.ini`, `electronics.ini`, `abs_control.lut`, and `aero.ini` targeting all four findings. Testing using the same A/B/C protocol at Monza T1 is pending.
 
See `analysis/behaviour_rules_and_analysis.md` for full baseline findings and `analysis/GT3_Braking_Telemetry_Analysis.xlsx` for telemetry data and implemented changes.
 
