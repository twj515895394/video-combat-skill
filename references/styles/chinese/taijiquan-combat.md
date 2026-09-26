---
id: taijiquan-combat
family: chinese-traditional
aliases: [Taijiquan, 太极技击, Tai Chi combat]
primary_range: contact-close
secondary_range: clinch
stance_bias: balanced-relaxed
movement_signature: yield-redirection, structure change, push/off-balance, controlled stepping
primary_tools: [forearm contact, palm, frame, pull, turn, off-balance]
defensive_tools: [body evasion, yield, redirect, rotate, step, frame]
grappling_level: medium
aerial_level: none
ai_generation_risk: high
load_when: user explicitly wants Tai Chi-inspired combat mechanics
do_not_load_when: user asks for fast hard striking without contact/redirection logic
---

# Taijiquan Combat — Choreography Model

Do not reduce this to slow-motion “push hands,” and do not use mystical force.

## Style DNA
- Contact can be used to redirect pressure.
- Body turn and step alter the opponent's line.
- Off-balancing should have visible mechanical cause.
- Speed follows the fight; no automatic slow motion.
- The defender often clears the body from the attack line **before or while** making guiding contact.
- The attacker may retain most of the original momentum; the defender changes its direction rather than stopping it dead.
- A successful redirection should leave the attacker with an overstep, overrotation, crossed recovery, exposed side or changed landing line.

## Core defensive principle — Body Evasion First

Do not default to arm-first blocking.

For fast incoming attacks, prefer this order when mechanically appropriate:

`incoming line -> torso/head leaves line -> feet/hips preserve balance -> hand/forearm makes secondary guiding contact -> attack continues past original target -> attacker must recover from changed line`

This creates a visually different defensive language from hard structural blocking.

### Requirements
- head/gaze still tracks the opponent,
- center of mass remains supported,
- torso shift is large enough to clear the attack but not an impossible bend,
- guiding contact happens on a limb already passing or nearly passing the body,
- the hand/forearm changes direction rather than magically stopping all momentum,
- next action begins from the attacker's overextension or the defender's angle.

### Bad
`kick arrives -> defender stands still and catches it with both hands -> attacker freezes.`

### Better
`defender shifts ribs/head outside the kick line; only after the body has cleared does the near forearm/palm meet the lower leg and guide it diagonally past, carrying the attacker's hips farther through the rotation.`

## Action Cards

### TJ-YIELD-STEP
Incoming pressure arrives; defender allows small torso/hip displacement while stepping to preserve base.
Result: attack line extends past original target.
Exit: defender remains balanced enough to redirect or counter without reset.

### TJ-BODY-CLEAR-AND-GUIDE
Purpose:
avoid a fast strike without absorbing its full force.

Mechanics:
- torso/head leaves attack line,
- hips/feet make the minimum adjustment needed to keep balance,
- near hand or forearm contacts the incoming limb only after the body is substantially safe,
- contact guides the limb farther past center.

Result:
attacker retains speed but must overstep, overrotate, land farther than intended or recover from the new line.

### TJ-FOREARM-REDIRECT
Forearm contact guides force laterally/diagonally while torso turns.
Contact remains brief and purposeful.
Do not freeze the limb at the contact point.

### TJ-PULL-AND-TURN
Requires actual arm/upper-body contact.
Defender draws opponent into overstep while turning hips/feet, causing balance shift.
The pull should add to an already committed direction rather than yanking a static opponent through space.

### TJ-PALM-OFF-BALANCE
Palm contacts upper torso/shoulder while foot/hip positioning removes stable alignment.
Receiver steps to recover; no invisible blast.

## Continuous Momentum Grammar

Taijiquan-inspired cinematic defense should often use the attacker's motor energy as the continuity engine.

Pattern:

`attacker owns forward/rotational momentum -> defender clears line -> guiding contact changes vector -> attacker keeps moving -> base no longer matches center of mass -> defender converts the recovery/overrotation into off-balance, turn, pull or counter`

This is not passive waiting.
It is a fast attack-defense conversion where the defender's actions are smaller than the attacker's visible momentum.

## Combination Grammar
- straight pressure -> body clears -> forearm/palm guides line -> attacker overextends -> palm/turn creates step-out.
- kick barrage -> torso/head repeatedly leave the line -> light guiding contacts keep each limb passing -> attacker eventually lands overcommitted -> defender converts landing/recovery into displacement.
- clinch-like contact -> pull changes base -> angle step -> release/push.
- opponent commits rotationally -> defender avoids the center of the arc -> guides limb/body continuation -> attacker overrotates -> next control begins before neutral recovery.

## Tactical Failure Conditions
- long kicking distance with no safe entry,
- no physical contact at all,
- supernatural knockback,
- slow decorative hand circles,
- arm-first blocks that ignore body evasion,
- redirection that stops the attacker dead instead of preserving momentum,
- defender touches lightly and attacker flies unrealistically.

## Camera Proof
Do not require both fighters to remain fully visible.
Useful choices:
- medium/full body when off-balancing and foot relationship matter,
- defender-focused medium shot while attacking limbs enter foreground,
- close contact insert only for a decisive guide / palm / off-balance point,
- result shot showing attacker overstep, overrotation or forced landing.

## Prompt Vocabulary
body clears the attack line first, yielding torso shift, guiding forearm contact, borrowed momentum, attacker overrotation, controlled pull-and-turn, palm-driven off-balance, continuous grounded reorientation, redirect rather than stop.
