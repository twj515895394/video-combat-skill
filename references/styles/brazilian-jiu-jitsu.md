---
id: brazilian-jiu-jitsu
family: ground-grappling
aliases: [BJJ, Brazilian Jiu-Jitsu, 巴西柔术]
primary_range: ground
secondary_range: clinch
stance_bias: adaptive
movement_signature: positional control, frames, guard, passes, hip escapes, submissions
primary_tools: [guard, pass, side control, mount, back control, choke/lock]
defensive_tools: [frame, hip escape, posture, guard recovery, hand fighting]
grappling_level: very-high
aerial_level: none
ai_generation_risk: very-high
load_when: user requests ground grappling / BJJ positional combat
do_not_load_when: short striking-only exchange
---

# Brazilian Jiu-Jitsu — AI Choreography Model

AI video often struggles with dense limb entanglement. Prefer simple, readable positional transitions.

## Style DNA
- Position precedes submission.
- Hips, frames and base matter more than dramatic upper-body pulling.
- Ground relationship must be explicit: who is top, bottom, side, mounted, or in guard.
- Complex leg-lock positions require dedicated reference footage and longer duration.

## Range Model
clinch/takedown -> guard/top position -> pass/control -> submission threat or escape.

## Action Cards

### BJJ-CLOSED/GUARD-FRAME
Bottom fighter uses legs/hips plus hands/forearms to control distance.
Top fighter maintains posture and hand placement.
Keep limb count visually simple.

### BJJ-HIP-ESCAPE
Bottom fighter plants foot/shoulder, shifts hips laterally away from pressure, creates knee/forearm frame.
Purpose: recover space.

### BJJ-GUARD-PASS-SIMPLE
Top fighter controls one leg/hip line, steps/knees around legs, settles chest/hip pressure to side.
Do not teleport from front to side.

### BJJ-SIDE-CONTROL
Top chest crosses torso, one or both knees/base points stabilize.
Bottom frames at shoulder/hip and attempts to turn.

### BJJ-MOUNT
Top knees straddle torso/hips with upright or low posture.
Bottom bridges/frames rather than lying motionless.

### BJJ-BACK-CONTROL
Use only with clear transition. Do not magically appear behind opponent.
Requires visible turn/exposure and reorientation.

## Combination Grammar
- takedown -> top settles -> bottom frames -> hip escape -> guard recovery attempt.
- top pressure -> bottom bridge creates space -> top posts -> position shifts.
- guard pass attempt -> bottom knee frame blocks -> top changes direction.

## Tactical Failure Conditions
- too many hidden limbs,
- instant submission from undefined position,
- bodies visually merge,
- camera orbits during entanglement.

## Camera Proof
Stable oblique/high-three-quarter angle. Show hips, knees, hands and relative top/bottom relationship.

## Prompt Vocabulary
hip escape, forearm frame, guard recovery, chest pressure, stable base, simple guard pass, side control, posted hand, positional transition.
