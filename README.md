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

## Project Structure

| File | Description |
|---|---|
| `README.md` | This file — project goals, overview, and limitations |
| `Behaviour_rules_and_analysis.md` | Telemetry-based analysis of current vs target braking behaviour |
| `GT3_Braking_Telemetry_Analysis.xlsx` | Full telemetry data export — Test A, B, C comparison and raw channel data |

---

## Current Status

**Phase: Baseline analysis**

Telemetry testing has been completed on the unmodified Kunos AMG GT3 (2015) at Monza T1 using MoTeC i2 Pro. Three braking technique tests (A, B, C) have been logged and analysed. Key unrealistic behaviours have been identified and quantified. iRacing comparison data (Test D) is pending analysis.

See `Behaviour_rules_and_analysis.md` for full findings.
