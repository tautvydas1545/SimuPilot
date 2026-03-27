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
    - While braking at 100% but before turning (steer < 5°), G fluctuates between -2.2753 and -1.5969 G — stable, no decay
    - -1.5952 G at the start of steering (5.11°, brake 100.00%) — longitudinal G barely affected by steering input
    - Speed at brake release: 69.0 kph
    - Distance at brake start: 750m
    - Distance at turn-in: 881m
    - Distance at brake release: 916m

- Tyre slip
    - Peak slip ratio FL: -14.50%, FR: -14.73%
    - Mean slip FL during straight-line 100% brake phase: -9.19%
    - Mean slip FL during combined brake + steering (>20°): -8.00%

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

- Entry speed: 271.8 kph

- Decel
    - Peak decel: -1.9603 G
    - Average of -1.2253 G (brake > 30%)
    - Brake pressure never exceeds 90.81% — continuous modulation throughout; never holds peak
    - -1.1148 G at start of steering (6.43°, brake 55.66%) — already well into trail brake phase
    - Speed at brake release: 80.2 kph
    - Distance at brake start: 707m
    - Distance at turn-in: 886m
    - Distance at brake release: 917m

- Tyre slip
    - Peak slip ratio FL: -7.98%, FR: -10.35%
    - Mean slip FL while braking (brake >50%): -4.20%
    - Mean slip FL during combined brake + steering (>20°): -2.56%

- Lap time: 1:52.345 (Lap 7) — **0.829s slower than Test A despite correct technique**

---

## Test C — T1 Fastest Lap
**Technique: 100% brake in straight-line phase, early release before trail braking**

- Entry speed: 272.6 kph

- Decel
    - Peak decel: -2.0812 G
    - Average of -1.5885 G (brake > 30%)
    - While braking at 100% but before turning (steer < 5°), G fluctuates between -2.0812 and -1.5345 G — stable, no decay
    - -1.1608 G at start of steering (7.25°, brake 66.03%) — brake already substantially released before turn-in
    - Speed at brake release: 67.2 kph
    - Distance at brake start: 739m
    - Distance at turn-in: 896m
    - Distance at brake release: 911m

- Tyre slip
    - Peak slip ratio FL: -12.82%, FR: -13.84%
    - Mean slip FL during straight-line 100% brake phase: -9.15%

- Lap time: 1:51.986 (Lap 6)

---

## Key Findings

- **Longitudinal grip too stable under sustained braking:** Across Tests A and C, the G profile is flat throughout the entire 100% brake phase — Test A holds 2.2s at a mean of −1.8194 G, Test C holds 2.5s at −1.7807 G, with no systematic decay in either. Realistic GT3 behaviour produces a sharp initial G peak that naturally reduces as tyre slip builds and speed decreases. AC does not replicate this.

- **Friction circle not enforced — combined slip penalty too weak:** Test A maintains −1.5952 G of longitudinal deceleration at turn-in while still at 100% brake. The mean slip ratio shifts by only 1.19% when steering is added (straight: −9.19%, combined: −8.00%), meaning lateral demand barely reduces longitudinal capacity. The front tyres are not penalised for doing too much at once.

- **ABS over-drive carries no efficiency penalty:** Test A runs peak slip at −14.50% — deeper into the ABS working range than Test B at −7.98% — yet still produces 0.41 G more average decel. Test C also outperforms Test B by 0.36 G on average despite using cruder technique. In a real GT3, driving past the optimal slip window creates heat build-up, instability, and a measurable drop in braking efficiency. In AC the ABS absorbs it silently with no penalty.

- **Proper technique is slower:** Test B (threshold modulation + proper trail brake) is 0.829s per lap slower than Test A (sustained 100% brake). The three behaviours above compound to actively penalise correct driving — maximum slam-and-hold is the fastest approach in the unmodified AC tyre model.

---

## Test D — iRacing GT3 T19 (End of Blanchimont)
*Note: Not directly comparable to AC tests — different circuit, entry speed, and GT3 car. Technique used is close to proper technique. To be analysed and compared separately.*

- Speed: 251 kph
