---
id: judo
family: grappling-throwing
aliases: [Judo, 柔道]
primary_range: grip-clinch
secondary_range: ground
stance_bias: upright-mobile
movement_signature: grip fighting, off-balancing, foot sweeps, hip/leg throws, transition to pins/ground control
primary_tools: [grip, foot sweep, reap, hip throw, shoulder turn, pin]
defensive_tools: [grip break, base recovery, hip turn, step-out, frame]
grappling_level: very-high
aerial_level: none
ai_generation_risk: high
load_when: user requests judo throws or grip-based standing grappling
do_not_load_when: striking dominates
---

# Judo — AI Choreography Model

This reference follows the broad throwing / groundwork identity of competitive judo while simplifying mechanics for AI-video readability.

## Style DNA
- Grip/contact precedes most meaningful throws.
- Off-balancing is the bridge between grip and throw.
- Foot sweeps/reaps and hip/shoulder turning are key visual families.
- Floor transition may continue into control but should remain simple in short AI clips.

## Range Model
hand/grip contact -> off-balance -> throw/sweep -> landing -> optional hold/control.

## Action Cards

### JD-FOOT-SWEEP
Attacker establishes upper-body grip/contact.
As opponent steps, attacker's foot sweeps the moving/supporting foot while arms guide upper body in the same timing.
Result: base disappears rather than body being lifted magically.

### JD-OUTER-REAP
Upper body is drawn/turned while attacking leg reaps outside opponent's support leg.
Camera must show both upper-body control and lower-body reap.

### JD-HIP-THROW
Attacker turns in with grip, places hips across opponent's center, bends/loads through legs and rotation.
Receiver passes over hip only after contact and off-balance are visible.

### JD-SHOULDER-TURN
Attacker enters under/inside arm line, turns body and places shoulder/back structure as fulcrum.
High AI risk; use stable camera and simple grip.

### JD-PIN-CONTINUATION
After landing, top fighter settles chest/hip pressure with visible base.
Avoid complex submission chains in short video.

## Combination Grammar
- grip fight -> opponent steps to recover -> foot sweep catches moving base.
- opponent resists backward -> attacker changes direction into forward hip/shoulder turn.
- failed reap -> keep grip/contact -> step to new angle -> second throw family.

## Tactical Failure Conditions
- throw begins with no grip/contact,
- receiver levitates before base is removed,
- robes merge limbs during complex turns.

## Camera Proof
Three-quarter full-body view from entry through landing. Floor and feet must remain visible.

## Prompt Vocabulary
visible grip fight, off-balancing pull-and-step, moving-foot sweep, outside reap, hip fulcrum, shoulder turn, weighted mat landing.
