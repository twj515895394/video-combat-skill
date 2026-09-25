---
id: muay-thai
family: striking-clinch
aliases: [Muay Thai, 泰拳]
primary_range: kicking-clinch
secondary_range: punching
stance_bias: upright balanced
movement_signature: pressure, checks, knees, elbows, clinch frames
primary_tools: [round kick, teep, knee, elbow, punches]
defensive_tools: [check, long guard, frame, catch, clinch control]
grappling_level: clinch-high
aerial_level: low
ai_generation_risk: medium
load_when: user wants Thai-style striking, elbows, knees or clinch
do_not_load_when: sport is pure boxing or throw-heavy Sanda
---

# Muay Thai

## Style DNA
- Stable posture supports kicks, knees, checks and clinch.
- Teep manages distance.
- Round kicks use strong hip rotation.
- Elbows and knees become important as distance collapses.
- Clinch is an active fighting range, not a resting embrace.

## Range Model
Outside: teep / long kick.
Mid: round kick / punches.
Close: elbow / knee.
Clinch: head/arm frames, posture control, knees, turns.

## Action Cards

### MT-TEEP
Support leg carries weight; other knee chambers forward; sole/ball of foot pushes target.
Purpose: interrupt entry or reset distance.
Result: receiver steps back or posture shifts.
Exit: kicking foot retracts and replants.

### MT-ROUND-KICK
Support foot pivots strongly; hip drives shin through target line.
Receiver may check, brace with forearms, step out or absorb and counter.
Do not depict a ballet spin.

### MT-KNEE
Close range; one leg supports while hips drive forward/up.
Upper body uses frame/clinch contact to control distance.
Exit: knee retracts or steps down into continued clinch.

### MT-HORIZONTAL-ELBOW
Shoulder/hip rotate; elbow point travels short horizontal line at close range.
Must have believable range.
Avoid huge arm swing.

### MT-CLINCH-FRAME
Hands/forearms control head/arms/shoulders while fighters remain chest-aware.
Posture changes create knee/turn opportunities.
AI error: static hugging.

## Combination Grammar
- teep stops rush -> opponent regains stance -> round kick catches re-entry.
- punch shell -> elbow enters as distance collapses.
- kick caught/absorbed -> fighter frames into clinch rather than resetting.
- clinch posture broken -> knee -> opponent posts/framing response -> turn.

## Tactical Failure Conditions
- side angles undermine square pressure,
- caught kick can lead to Sanda/MMA-style off-balance,
- failed elbow at long range leaves overextension.

## Camera Proof
Use full-body for kicks/checks; medium close for elbow/clinch only after body relationship is established.

## Prompt Vocabulary
lead teep, shin-driven round kick, raised-shin check, collar-frame, short horizontal elbow, forward knee, clinch turn.
