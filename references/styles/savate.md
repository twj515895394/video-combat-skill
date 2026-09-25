---
id: savate
family: striking
aliases: [Savate, French Boxing, 法式踢拳]
primary_range: long-kicking-punching
secondary_range: boxing
stance_bias: mobile-upright
movement_signature: precise shoe-foot kicking lines, mobile fencing-like distance changes, boxing hands
primary_tools: [front/side/rounding kicks, straight punches, hooks]
defensive_tools: [distance retreat, angle step, parry, evasive footwork]
grappling_level: none
aerial_level: low
ai_generation_risk: medium
load_when: user explicitly requests Savate / French boxing
do_not_load_when: clinch or throws are central
---

# Savate — AI Choreography Model

## Style DNA
- Mobile long-range striking.
- Foot/shoe-based kicks are a distinctive visual language.
- Punching supports kicking range management.
- Footwork can feel light and measured, but should not become fencing cosplay.

## Range Model
long kick range -> punch entry -> lateral/diagonal exit.

## Action Cards

### SV-CHASSE-LINE
Chambered leg drives foot/heel in a piston-like straight/side line.
Support foot and torso orientation must remain clear.

### SV-ROUNDING-KICK
Hip/leg arc attacks from outside line with controlled retraction.

### SV-STOP-KICK
Lead leg interrupts advancing opponent, preserving space.

### SV-PUNCH-EXIT
Straight hand combination finishes with diagonal footwork restoring kicking distance.

## Combination Grammar
- stop kick interrupts advance -> straight punches touch range -> diagonal exit.
- punch pressure causes shell -> long kick attacks open flank/leg.
- missed kick lands -> immediate footwork rather than stationary reset.

## Tactical Failure Conditions
- opponent collapses into clinch,
- huge Muay-Thai-style shin swing replacing precise foot trajectory.

## Camera Proof
Medium-wide lateral framing for leg-line precision.

## Prompt Vocabulary
precise shoe-foot kick, piston-like chasse, mobile long-range step, diagonal exit, punch-to-kick distance management.
