---
id: northern-longfist
family: chinese-traditional-broad
aliases: [Changquan, 长拳, 北拳, northern long fist]
primary_range: long-striking
secondary_range: mid
stance_bias: extended-mobile
movement_signature: long open strikes, broad leg vocabulary, circular transitions, dynamic level changes
primary_tools: [long punch, straight kick, side kick, sweep, extended palm, selected jumps]
defensive_tools: [distance evasion, long parry, angle step, low/high level change]
grappling_level: low
aerial_level: medium
ai_generation_risk: medium-high
load_when: broad northern long-fist / long-range Chinese movement is requested
do_not_load_when: close rooted southern system is the intended identity
---

# Northern Long Fist — Choreography Model

Broad movement family inspired by long-range northern Wushu/Changquan characteristics; not a universal representation of every northern school.

## Style DNA
- Open extended postures.
- Long attack lines.
- Greater leg vocabulary and spatial travel.
- Circular momentum can connect strikes.
- Selected leaps/level changes may appear, but should remain AI-readable.

## Range Model
outside-long -> kicking/punching -> lateral/diagonal reposition.
Prefers room to extend.

## Action Cards

### CQ-LONG-STRAIGHT
Lead/rear foot advances; shoulder/hip extend through a longer line than compact southern striking.
Exit preserves forward route for kick or second long strike.

### CQ-FRONT/STRAIGHT-KICK
Support leg stabilizes; knee chambers; lower leg extends on direct line.
Landing must be specified.

### CQ-SIDE-KICK
Support foot pivots; knee chambers across body; heel drives laterally.
Useful for range denial.

### CQ-SWEEP
Support lowers; sweeping leg travels a broad low arc.
Opponent response must lift/step/lose base; do not make both characters jump.

### CQ-LEAP-ENTRY
One support leg compresses and pushes off; trajectory is simple; aerial duration short; landing creates next attack.

## Combination Grammar
- long hand attack pushes opponent backward -> kick uses preserved distance.
- missed kick lands forward -> circular hand action continues rotation.
- opponent closes distance -> angle step restores extension space.

## Tactical Failure Conditions
- trapped at very close bridge/clinch range,
- aerial movement without enough space,
- oversized motions in cramped corridor.

## Camera Proof
Full-body wide/medium-wide is essential for long lines and kicks. Close-ups should follow a readable proof shot.

## Prompt Vocabulary
extended long-range strike, heel-driven side kick, broad low sweep, long diagonal step, open posture, short controlled leap.
