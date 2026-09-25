---
id: karate
family: striking
aliases: [Karate, 空手道]
primary_range: punching-kicking
secondary_range: countering
stance_bias: variable-structured
movement_signature: sharp entry-exit, direct linear attacks, compact counter timing, selective kicks
primary_tools: [straight punch, reverse punch, front kick, round kick, side kick]
defensive_tools: [parry, forearm block, distance withdrawal, angle step]
grappling_level: low
aerial_level: low
ai_generation_risk: medium
load_when: user requests karate-style sharp entry/counter striking
do_not_load_when: prolonged clinch, elbows/knees, or ground fighting define the sequence
---

# Karate — AI Choreography Model

Karate contains many schools and competition formats. This file stores a useful cross-school choreography model rather than one definitive technical doctrine.

## Style DNA
- Clear start/stop body acceleration without idle posing.
- Direct linear hand attacks are visually important.
- Entry and exit can be sharper and more discrete than boxing pressure.
- Kicks are usually used from deliberate range rather than constant kick-chaining.
- Counter timing is a strong cinematic identity.

## Range Model
outside -> explosive entry -> punching/kicking contact -> short exit or angle change.

## Action Cards

### KR-REVERSE-PUNCH
Rear hand drives straight as hips rotate and rear heel/foot contributes.
Often follows a lead step, parry or opponent overextension.
Exit: shoulders stay opponent-aware; stance remains usable.

### KR-FRONT-KICK
Support leg stabilizes, knee chambers, foot extends directly.
Purpose: interrupt advance or attack centerline.
Exit: retract or land forward.

### KR-SIDE-KICK
Support foot turns; chambered knee aligns; heel drives laterally.
High readability when full body is visible.

### KR-COUNTER-STEP
Opponent enters -> defender withdraws/angles just enough -> planted foot immediately returns distance with straight counter.
Avoid exaggerated backward hopping.

## Combination Grammar
- opponent lunges -> short parry/withdrawal -> reverse punch counter.
- lead straight draws guard -> rear straight -> angle exit.
- front kick interrupts pressure -> kicking foot lands forward -> hand attack continues.

## Tactical Failure Conditions
- long static pose between exchanges,
- unsupported dramatic spins,
- boxing-style continuous head weaving replacing structured footwork.

## Camera Proof
Medium-wide/full body for entry distance; short impact insert may emphasize clean counter contact.

## Prompt Vocabulary
sharp linear entry, reverse straight punch, chambered front kick, short counter-step, crisp angle exit, structured stance recovery.
