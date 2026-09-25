---
id: wing-chun
family: chinese-traditional
aliases: [Wing Chun, 咏春, Yong Chun]
primary_range: trapping-close
secondary_range: punching
stance_bias: compact-centerline
movement_signature: centerline pressure, short straight hands, forearm contact, compact stepping
primary_tools: [straight punch, palm, forearm bridge, pak-like deflection, elbow]
defensive_tools: [short deflection, wedge/frame, contact sensitivity model, angle step]
grappling_level: low
aerial_level: none
ai_generation_risk: medium-high
load_when: compact centerline/hand-fighting choreography is requested
do_not_load_when: long kicks or acrobatics are the dominant identity
---

# Wing Chun — AI Choreography Model

Traditional schools vary. This reference focuses on visually recognizable close-range mechanics useful for video choreography.

## Style DNA
- Compact posture and short travel.
- Hands occupy centerline.
- Forearm contact is a transition, not decorative hand tapping.
- Footwork is small and purposeful.
- Long-range jumping attacks are not core to this model.

## Action Cards

### WC-STRAIGHT-HAND
Hand travels directly along centerline with limited wind-up.
Body/step supports forward pressure.
Exit keeps opposite hand available.

### WC-PAK-DEFLECTION
Open palm/forearm gives short lateral pressure to incoming wrist/forearm.
Purpose: clear line briefly.
Immediate continuation required.

### WC-WEDGE-ENTRY
Both forearms or one forearm creates a wedge/frame while step collapses distance.
Result: attack line opens or opponent posture compresses.

### WC-COMPACT-ELBOW
Only at genuine close range.
Shoulder and body position create short elbow path; no wide swing.

## Combination Grammar
- incoming straight -> short lateral deflection -> immediate straight/palm.
- forearm contact -> opponent pressure continues -> angle step changes line -> short strike.
- opponent retreats -> small advancing steps maintain close range.

## Tactical Failure Conditions
- long kicking distance,
- static “sticky hands” posing,
- rapid hand flutter with no body consequences.

## Camera Proof
Medium-close can show hand fighting, but keep hips/feet visible during entries.

## AI Failure Modes
- multiple extra hands,
- meaningless rapid patting,
- fighters standing chest-to-chest without foot adjustment.

## Prompt Vocabulary
compact centerline punch, short palm deflection, forearm wedge, small diagonal entry step, close elbow, continuous hand contact.
