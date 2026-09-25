---
id: shuai-jiao
family: chinese-grappling
aliases: [Shuai Jiao, 中国跤, 摔跤]
primary_range: clinch
secondary_range: entry
stance_bias: stable-mobile
movement_signature: grip/contact, trips, reaps, hip/body turns, standing throws
primary_tools: [arm control, body grip, trip, reap, hip/shoulder turn]
defensive_tools: [base widening, grip fighting, hip turn, step recovery]
grappling_level: high-standing
aerial_level: none
ai_generation_risk: high
load_when: Chinese standing throwing is requested
do_not_load_when: prolonged ground fighting is central
---

# Shuai Jiao — AI Choreography Model

## Style DNA
- Standing off-balancing and throws.
- Visible grip/contact precedes displacement.
- Feet remove or obstruct support.
- Upper and lower body actions cooperate.
- After landing, choreography may disengage or continue according to cinematic need.

## Action Cards

### SJ-GRIP-ENTRY
Hand/forearm secures arm/upper garment/body contact while feet close range.
Avoid magical grip appearing after cut.

### SJ-OUTSIDE-TRIP
Upper body pulls/turns opponent while attacker's leg blocks/reaps outside support line.
Receiver falls because base is removed.

### SJ-INSIDE-TRIP
Attacker steps close and uses inside leg position to disrupt support while torso control guides fall.

### SJ-HIP/BODY-TURN
Attacker establishes body contact and lowers/positions center; torso turn carries opponent across compromised base.
Keep landing readable.

## Combination Grammar
- hand-fight -> opponent resists backward -> step closes -> trip uses resisting weight.
- failed strike -> arm contact remains -> grip -> off-balance -> throw.
- opponent widens stance -> change direction rather than forcing same throw.

## AI Failure Modes
- bodies merge,
- receiver levitates before leg contact,
- throw happens without off-balance,
- camera hides feet.

## Camera Proof
Full-body three-quarter view with floor visible from entry through landing.

## Prompt Vocabulary
standing grip fight, upper-body turn, outside trip, inside reap, support-leg removal, visible off-balance.
