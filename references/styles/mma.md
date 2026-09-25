---
id: mma
family: mixed
aliases: [MMA, 综合格斗]
primary_range: all
secondary_range: all
stance_bias: adaptive
movement_signature: strike-to-shot, cage/wall pressure, clinch transitions, ground continuation
primary_tools: [punches, kicks, knees, takedowns, clinch, positional grappling]
defensive_tools: [sprawl, frames, underhooks, guard, wall-post, footwork]
grappling_level: high
aerial_level: very-low
ai_generation_risk: high
load_when: mixed striking+takedown+ground logic matters
do_not_load_when: user wants stylized wuxia or one pure striking system
---

# MMA

## Style DNA
MMA is defined by transitions between ranges, not by one signature strike.
For short AI clips, choose a small number of phases; do not attempt every range in 10 seconds.

## Range Model
outside striking -> punching -> clinch -> takedown -> ground.
Reverse transitions are equally important.

## Action Cards

### MMA-STRIKE-TO-SHOT
Punch/feint occupies guard; attacker lowers level with knees/hips, head stays positioned, arms connect to legs/body.
Defender reacts with sprawl/frame/underhook.
Avoid instant tackle teleport.

### MMA-SPRAWL
Defender throws legs/hips back while upper body applies downward frame/pressure.
Result: shot stalls below hips; next state becomes front head/underhook/separation.

### MMA-WALL-PRESS
Attacker uses body/head/arm position to compress opponent to wall/cage-like surface.
Receiver frames, widens base, seeks underhook/turn.

### MMA-GROUND-CONTINUATION
Keep positions simple for AI:
top half/side-like control, posted hand, framed forearm, hip escape.
Avoid many limb entanglements unless reference footage exists.

## Combination Grammar
- jab/cross -> defender high guard -> level change -> takedown attempt.
- kick caught -> immediate balance battle -> takedown or release.
- failed shot -> clinch -> wall pressure -> turn.
- ground frame -> hip escape -> stand-up attempt.

## Tactical Failure Conditions
- too many transitions in too little time become limb hallucination,
- vague "grapples him" produces merged bodies,
- complex submissions require dedicated reference and more screen time.

## Camera Proof
Takedowns require full hips/feet/floor. Ground sequences benefit from stable oblique high angle, not spinning camera.

## Prompt Vocabulary
level change, double-leg entry, sprawl, underhook, overhook, body lock, wall pressure, hip escape, posted hand, technical stand-up.
