---
id: wrestling-grappling
family: grappling
aliases: [wrestling, grappling, 摔跤, 缠斗]
primary_range: clinch
secondary_range: ground
stance_bias: lowered center
movement_signature: hand fighting, level changes, body locks, trips, mat control
primary_tools: [single-leg, double-leg, body lock, underhook, trip, mat return]
defensive_tools: [sprawl, whizzer/overhook, frame, base widening, hip turn]
grappling_level: very-high
aerial_level: none
ai_generation_risk: high
load_when: standing takedown or ground control is important
do_not_load_when: only striking is requested
---

# Wrestling / Grappling

## Style DNA
- Contact and control determine motion.
- Throws/takedowns must have visible grips/body pressure.
- Base, hip position and head position are critical.
- AI readability is more important than technical complexity.

## Range Model
hand-fighting -> tie/body contact -> level change/lock -> takedown -> positional control.

## Action Cards

### WR-HAND-FIGHT
Forearms/hands make brief contact to control wrists/biceps/shoulders.
Purpose: create entry line.
Avoid static arm grabbing.

### WR-SINGLE-LEG
Attacker lowers level, steps close, connects arms around one leg while head/shoulder position controls torso.
Receiver hops, frames, sprawls partially or seeks overhook.
Finish only after balance is visibly compromised.

### WR-DOUBLE-LEG
Level change + penetration step + arms behind/around legs + forward/angle drive.
Receiver sprawls or widens base.
Do not depict shoulder-only tackle without leg connection.

### WR-BODY-LOCK-TRIP
Torso contact + arms lock around midsection + foot blocks/trips support while upper body rotates/presses.
Landing follows removed base.

### WR-SPRAWL
Hips drive backward/down while legs extend; upper body frames attacker.
Exit: stalled shot -> front control / separation / re-shot.

## AI simplification
Prefer:
- one clear takedown,
- one clear defense,
- one positional result.

Avoid:
- rapid chain wrestling with hidden legs,
- multiple simultaneous grips,
- intricate ground submissions in wide flowing clothing.

## Camera Proof
Full-body oblique angle for takedown entry. Floor must be visible. Stable camera around landing.

## Prompt Vocabulary
level change, penetration step, underhook, overhook, body lock, outside trip, sprawl, hip pressure, base widening, mat return.
