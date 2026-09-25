---
id: sambo
family: grappling-mixed
aliases: [Sambo, 桑搏]
primary_range: clinch-throw
secondary_range: ground
stance_bias: mobile-grappling
movement_signature: fast standing throws, leg attacks, trips, transitions; combat variant may include striking
primary_tools: [body lock, leg attack, trip, throw, ground control]
defensive_tools: [base recovery, grip fight, sprawl, turn, frame]
grappling_level: very-high
aerial_level: none
ai_generation_risk: high
load_when: user requests Sport Sambo or Combat Sambo
do_not_load_when: unspecified striking task with no grappling identity
---

# Sambo — AI Choreography Model

FIAS distinguishes Sport SAMBO and Combat SAMBO. The prompt must choose the intended variant rather than mixing them accidentally.

## Sport Sambo choreography
Focus:
- standing grips/contact,
- throws,
- trips,
- leg attacks,
- fast transition to ground control/submission threat.

## Combat Sambo choreography
May layer striking over the above grappling base when the user explicitly requests Combat Sambo.

## Action Cards

### SB-FAST-THROW-ENTRY
Grip/body contact is established while feet step rapidly into off-balance angle.
Throw occurs immediately after base is compromised.

### SB-LEG-ATTACK
Level drops, hands connect to leg(s), head/body position remains visible.
Receiver widens base/hops/frames.

### SB-TRIP-CHAIN
First throw attempt fails because opponent steps; attacker keeps contact and attacks the newly loaded support leg.

### SB-GROUND-TRANSITION
After throw, attacker follows balance into top control rather than resetting upright.

## Combination Grammar
- grip -> outside trip attempt -> opponent steps out -> second trip attacks new support.
- strike pressure (Combat variant) -> clinch contact -> standing throw.
- failed leg attack -> body lock/turn rather than disengagement.

## Tactical Failure Conditions
- unclear Sport vs Combat variant,
- telekinetic throws,
- overly complex rolling leg entanglements.

## Camera Proof
Full body through throw, then stable oblique ground angle.

## Prompt Vocabulary
rapid grip-to-throw transition, chained trip, visible leg attack, continuous top-control follow-through, Combat Sambo striking-to-clinch transition.
