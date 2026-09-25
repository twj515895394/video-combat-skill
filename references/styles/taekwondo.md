---
id: taekwondo
family: kicking-striking
aliases: [Taekwondo, 跆拳道, TKD]
primary_range: long-kicking
secondary_range: mid
stance_bias: mobile-side-on
movement_signature: fast chambered kicks, high-line kicks, quick stance switches, long-range interception
primary_tools: [front kick, side kick, round kick, hook kick, back kick]
defensive_tools: [distance retreat, angle step, kick check/evade, counter-kick]
grappling_level: none
aerial_level: medium
ai_generation_risk: high
load_when: user wants kick-dominant long-range choreography
do_not_load_when: clinch, throws or hand-heavy pressure are the main identity
---

# Taekwondo — AI Choreography Model

Different Taekwondo rule sets and schools vary. This file focuses on visually recognizable long-range kicking mechanics.

## Style DNA
- Kicks dominate visual identity.
- Stance may be more side-on and mobile to support rapid leg chambering.
- High-line kicks and counter-kicks are more common than in many other combat systems.
- Spinning actions must be carefully constrained for AI stability.

## Range Model
long outside range -> chambered kick -> rapid retraction/landing -> reset through footwork, not idle posing.

## Action Cards

### TKD-ROUND-KICK
Support foot pivots; attacking knee chambers sharply; lower leg whips toward torso/head line.
Exit: retract quickly or land with facing restored.

### TKD-SIDE-KICK
Chamber knee compresses across body; support foot rotates; heel drives straight.
Useful for range denial.

### TKD-HOOK-KICK
Leg extends past target line then heel arcs across.
High AI risk: use readable full-body camera and adequate time.

### TKD-BACK-KICK
Must explicitly define turn:
opponent-facing -> shoulder look/pivot -> heel drives on direct backward line -> foot lands -> torso immediately reorients.
Never leave fighter permanently back-facing.

### TKD-CUT/INTERRUPT-KICK
Lead leg chambers quickly and extends short to interrupt opponent's forward step.
Purpose is spacing, not huge knockback.

## Combination Grammar
- lead interrupt kick stops advance -> rear round kick attacks as opponent re-enters.
- missed round kick lands forward -> body reorients -> side/back kick becomes available only if facing logic remains valid.
- opponent retreats linearly -> step/hop closes enough range for second kick.

## Tactical Failure Conditions
- opponent collapses into clinch,
- repeated spins in cramped space,
- AI changes kicking leg mid-action.

## Camera Proof
Full-body is mandatory for spinning/high kicks. Avoid close crop that hides support foot.

## Prompt Vocabulary
fast knee chamber, support-foot pivot, heel-driven side kick, high round kick, controlled back-kick pivot, immediate opponent-facing recovery.
