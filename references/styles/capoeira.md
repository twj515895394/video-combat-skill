---
id: capoeira
family: evasive-kicking
aliases: [Capoeira, 卡波耶拉]
primary_range: long-mid
secondary_range: evasive
stance_bias: mobile-continuous
movement_signature: ginga-like weight shifts, inverted/low evasions, circular kicks, deceptive level changes
primary_tools: [circular kick, heel kick, low sweep, evasive lean, selected hand-supported movement]
defensive_tools: [esquiva-like body evasion, level drop, lateral movement]
grappling_level: low
aerial_level: medium
ai_generation_risk: very-high
load_when: user explicitly requests Capoeira movement
do_not_load_when: realism/stability requires simple direct exchanges
---

# Capoeira — AI Choreography Model

Capoeira contains cultural, game and combat dimensions. This file only captures movement mechanics useful for AI action choreography.

## Style DNA
- Continuous weight transfer and deceptive rhythm.
- Circular kicks emerge from body rotation.
- Low evasions and level changes are visually important.
- Hand-supported/inverted movement is optional and high-risk for AI.

## Action Cards

### CP-RHYTHMIC-WEIGHT-SHIFT
Feet alternate support while torso remains opponent-aware.
Use as movement base, not a dance interlude.

### CP-CIRCULAR-KICK
Support foot/body rotate; attacking leg traces broad arc.
Exit must identify landing and facing.

### CP-LOW-EVASION
Knees/hips lower and torso leans away from attack while one or both feet preserve recovery.
Do not collapse to ground without support.

### CP-HAND-SUPPORTED-EVASION
One/both hands contact floor briefly while hips/legs move through controlled path.
High AI risk: use only with clear camera and enough time.

## Combination Grammar
- opponent straight attack -> low evasive shift -> circular kick emerges from recovery.
- kick misses -> landing rotation feeds lateral movement rather than full reset.
- pressure closes range -> Capoeira fighter uses level/angle change to reopen space.

## Tactical Failure Conditions
- endless acrobatics,
- both characters synchronizing movements,
- repeated inversion without combat purpose.

## Camera Proof
Wide/full-body with floor visible. Do not crop hands/feet during inverted motion.

## Prompt Vocabulary
continuous weight shift, low evasive lean, broad circular kick, hand-supported transition, opponent-aware recovery.
