---
id: boxing
family: striking
aliases: [boxing, 拳击]
primary_range: punching
secondary_range: pocket
stance_bias: mobile bladed-to-semi-square
movement_signature: jab-led range management, head movement, pivots, angle exits
primary_tools: [jab, cross, hook, uppercut, body punch]
defensive_tools: [parry, slip, roll, step-back, high guard, pivot]
grappling_level: none
aerial_level: none
ai_generation_risk: low-medium
load_when: user explicitly requests boxing or punch-dominant footwork
do_not_load_when: kicks, throws or clinch knees are the main identity
---

# Boxing

## Style DNA
- Hands dominate offense.
- Feet and head movement create punching windows.
- Attacks usually preserve a structure from which the next punch/exit can occur.
- Range changes are small but frequent.
- Angles, pivots and body-level changes matter more than large acrobatics.
- Guard and shoulder position should remain readable.

## Range Model
Preferred: jab-to-pocket range.
Entry: jab step, double jab, feint-step, slip-entry.
Exit: pivot, short retreat, angle step, clinch/break only if choreography allows.

## Stance & Weight
Use one fighter-specific orthodox/southpaw choice.
Keep lead/rear relationship consistent.
Punching rotates hips/shoulders but should not magically square/reset after every strike.

## Action Cards

### BX-JAB
- purpose: probe, interrupt, measure, cover entry
- start: lead shoulder forward, lead foot available
- mechanics: small lead-foot pressure + lead hand straight path
- result: opponent parries/slips/shells or loses a small amount of space
- exit: lead hand retracts while feet remain ready for cross/angle
- camera proof: chest-to-knees or medium full-body if foot entry matters
- AI error: arm-only poke with frozen torso

### BX-CROSS
- purpose: power straight after line is opened
- mechanics: rear foot drives, hip/shoulder rotate, rear hand travels straight
- miss result: shoulder becomes extended and weight may load lead side
- exit options: lead hook, pivot, short retreat

### BX-LEAD-HOOK
- purpose: punish shell/angle, turn opponent
- mechanics: lead hip/foot rotate, elbow follows horizontal arc
- physical result: head/upper torso rotation or guard compression
- AI error: arm swings without hip rotation

### BX-BODY-HOOK
- purpose: level change at close range
- mechanics: knees flex, torso level lowers, hook arcs to body
- exit: loaded legs create head-level continuation or pivot

### BX-SLIP
- purpose: remove head from straight line without disengaging
- mechanics: knees/waist subtly shift head outside line
- exit: body remains loaded for counter
- AI error: whole body teleports sideways

### BX-PIVOT-EXIT
- purpose: leave pressure line while staying attack-ready
- mechanics: lead foot anchors, rear foot arcs, torso reorients opponent-facing
- AI error: fighter turns back and walks away

## Combination Grammar
- jab draws parry -> rear cross uses opened center.
- cross compresses guard -> lead hook turns around guard.
- opponent straight -> slip outside -> rear hand counter -> pivot exit.
- body hook lowers defense -> head hook becomes available.
- pressure backs opponent up -> short step maintains punching range.

## Tactical Failure Conditions
- opponent controls kicking range.
- clinch/throw range collapses hand rhythm.
- overcommitted cross leaves weight too far forward.

## Camera Proof
Use readable waist/full-body for angle footwork; close shots only after attack line is established.

## Prompt Vocabulary
lead-hand straight, rear-hand straight, outside slip, shoulder roll, lead-foot pivot, short lateral exit, body-level change, compact hook.
