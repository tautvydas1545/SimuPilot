# AC Behaviour Rules and Analysis

## AC Behaviour Rules

### Current Behaviour (Unmodified AC GT3)

- Sustained peak decel maintained at constant 100% brake throughout braking zone
- Steering input does not significantly reduce longitudinal G
- Proper braking technique is not rewarded — incorrect technique produces faster lap times

### Target Behaviour

- Peak decel occurs early in braking zone, decaying naturally as speed reduces
- Sustained 100% brake reduces braking efficiency over time
- Steering input significantly reduces longitudinal G (friction circle enforced)
- Proper trail braking technique improves lap performance

---

## Test A — T1 Fastest Lap
**Technique: 100% brake held throughout, steering applied while still at 100% brake**

- Entry speed: 273.6 kph

- Decel
    - Almost immediate peak of -2.2753 G
    - Average of -1.6395 G (brake > 30%)
    - While braking at 100% but before turning, G fluctuates between -2.2753 and -1.5969 G — stable, no decay
    - -1.5952 G at the start of steering (5.11°, brake 100.00%) — longitudinal G barely affected by steering input
    - Minimum speed: 69.0 kph
    - Distance at brake start: 757m
    - Distance at turn-in: 890m
    - Distance at min speed: 925m

- Tyre slip
    - Peak slip FL: -14.50%, FR: -14.73%
    - Mean slip FL during straight-line 100% brake phase: -9.19%
    - Mean slip FL during combined brake + steering: -7.97%

- Lap time: 1:51.516 (Fastest — Lap 7)

---

## Test A — T2 Second Fastest Lap
*Note: Driving error in T1 fastest lap — this lap used as the cleaner reference.*

- Entry speed: 255 kph

- Decel
    - Almost immediate peak of -1.9969 G
    - Average of -1.7534 G
    - While braking at 100% but before turning, G fluctuates between -1.9969 and -1.4177 G — stable, no decay
    - -1.6021 G at start of steering (-17.60°, brake 98.18%)
    - Minimum speed: 91.4 kph
    - Distance at brake start: 1978m
    - Distance at turn-in: 2091m
    - Distance at min speed: 2119m

---

## Test B — T1 Fastest Lap
**Technique: Proper technique — initial peak, threshold modulation, proper trail brake**

- Entry speed: 272.0 kph

- Decel
    - Peak decel: -1.7296 G
    - Average of -1.3334 G (brake > 30%)
    - Brake pressure never exceeds 85.8% — continuous modulation throughout; never holds peak
    - -1.2636 G at start of steering (6.16°, brake 65.52%) — already well into trail brake phase
    - Minimum speed: 66.3 kph
    - Distance at brake start: 726m
    - Distance at turn-in: 897m
    - Distance at min speed: 931m

- Tyre slip
    - Peak slip FL: -11.90%, FR: -12.76%
    - Mean slip FL while braking (brake >50%): -4.90%
    - Mean slip FL during combined brake + steering: -4.10%

- Lap time: 1:52.345 (Lap 6) — **0.829s slower than Test A despite correct technique**

---

## Test C — T1 Fastest Lap
**Technique: 100% brake in straight-line phase, early release before trail braking**

- Entry speed: ~272 kph (no GPS channel in this recording)

- Decel
    - Peak decel: -2.0812 G
    - Average of -1.5885 G (brake > 30%)
    - While braking at 100% but before turning, G fluctuates between -2.0812 and -1.5345 G — stable, no decay
    - -1.2655 G at start of steering (5.15°, brake 68.19%) — brake already partially released before turn-in
    - Braking duration: 3.95s

- Lap time: 1:51.986 (Lap 6)

---

## Key Findings

- **Friction circle not enforced:** Test A maintains -1.5952 G of longitudinal deceleration at turn-in while still at 100% brake. Steering input should directly reduce longitudinal capacity through the friction circle, but the data shows this barely occurs. This is the primary unrealistic behaviour in the unmodified AC tyre model.

- **No natural G decay under sustained braking:** Across Tests A and C, the longitudinal G profile is flat throughout the 100% brake phase — there is no early peak and decay. Realistic GT3 behaviour produces a sharp initial G peak that naturally reduces as tyre slip builds and speed decreases. AC does not replicate this.

- **Proper technique is slower:** Test B (threshold modulation + proper trail brake) is 0.829s per lap slower than Test A (sustained 100% brake with no technique). The physics actively penalises correct driving.

---

## Test D — iRacing GT3 T19 (End of Blanchimont)
*Note: Not directly comparable to AC tests — different circuit, entry speed, and GT3 car. Technique used is close to proper technique. To be analysed and compared separately.*

- Speed: 251 kph
