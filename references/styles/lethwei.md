---
id: lethwei
family: striking-clinch
aliases: [Lethwei, 缅甸拳]
primary_range: punching-kicking-clinch
secondary_range: close
stance_bias: pressure-oriented
movement_signature: hard pressure, punches, kicks, knees, elbows, head contact in traditional rulesets
primary_tools: [punch, kick, knee, elbow, clinch, headbutt]
defensive_tools: [guard, parry, frame, clinch control, angle step]
grappling_level: clinch-medium
aerial_level: low
ai_generation_risk: medium
load_when: user explicitly requests Lethwei
do_not_load_when: safer sport striking or no-head-contact choreography is requested
---

# Lethwei — AI Choreography Model

Lethwei rule traditions can include headbutts. Use head contact only when the user's requested tone and platform context make it appropriate; otherwise omit it and preserve the broader striking/clinch identity.

## Style DNA
- Direct pressure.
- Punches, kicks, knees and elbows combine at changing ranges.
- Clinch contact can become immediate short strikes.
- Less emphasis on decorative movement; pressure and toughness dominate visual character.

## Action Cards

### LW-PRESSURE-ENTRY
Short advancing steps keep torso facing opponent while hands occupy guard line.

### LW-ELBOW/KNEE
Use only at true close range with frame/clinch relation.

### LW-HEAD-CONTACT
If explicitly used: forehead/upper head line travels a very short path from established clinch distance.
Never depict huge wind-up or reckless neck snapping.
Omit by default when not needed.

## Combination Grammar
- punch pressure -> opponent covers -> clinch/frame -> knee/elbow.
- kick lands/gets checked -> fighter steps down into hand pressure.
- failed close strike -> forearm frame preserves contact and continues.

## Tactical Failure Conditions
- abstract “brutal brawl” with no mechanics,
- random headbutts from long range,
- cinematic knockback without body contact.

## Camera Proof
Stable medium/close only after range is established; preserve feet during pressure transitions.

## Prompt Vocabulary
hard forward pressure, compact elbow, clinch knee, short forearm frame, close head contact when explicitly requested, immediate continuation.
