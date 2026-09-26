# Core Biomechanics

Use when foot placement, weight transfer, impact reaction, landing or body orientation is ambiguous.

## State model

Every fighter state should be expressible as:

- lead_foot
- rear_foot
- stance_width
- torso_angle
- head/eye orientation
- center_of_mass
- dominant_support
- current_velocity
- opponent_distance
- environment_contact

## Strike grammar

A strike is not a label. It is:

`support -> weight transfer -> hip/shoulder linkage -> limb path -> exact receiving point -> contact/miss -> recoil/continuation -> new base`

### Straight hand strike
- rear foot drives or stance compresses,
- pelvis and shoulder advance,
- striking hand travels on a readable line,
- opposite hand/shoulder balances the rotation,
- miss creates extension and recovery path,
- contact changes receiver structure.

### Hooking strike
- pivot/hip rotation matters more than arm-only swing,
- elbow and fist follow an arc,
- torso must rotate with the strike,
- exit state often leaves shoulders rotated and creates a natural continuation.

### Kick
Always define:
- support leg,
- chamber or swing path,
- hip action,
- striking surface direction,
- exact receiving line,
- whether the leg retracts or lands forward,
- landing orientation.

## Receiving-point rule

For every meaningful contact, specify what actually receives the force.

Examples:
- palm heel -> upper sternum,
- straight punch -> left pectoral / shoulder line,
- body hook -> lower ribs,
- low kick -> outer thigh,
- forearm check -> attacking forearm or lower leg,
- shoulder bump -> upper chest / shoulder girdle,
- body collision -> wooden pillar / wall / railing.

Do not use generic “hits his body” when a more precise receiving point is visible and relevant.

## Defensive grammar

Defense must alter something.

- parry: changes attack line,
- forearm check: intercepts/redirects line,
- slip: changes head/torso location while feet remain usable,
- step-back: changes range,
- angle step: changes both line and range,
- shell/cover: absorbs force but changes posture/initiative,
- catch: captures limb and changes balance options.

Never use "blocks the attack" as a complete action description.

A block/check has its own collision physics:
`incoming limb -> exact defensive contact -> rapid deceleration -> guard/body structure compresses -> attack line changes -> next opening`

## Impact grammar

Readable impact:

`approach -> exact contact point -> local compression/deflection -> structural interruption -> center-of-mass reaction -> foot/balance consequence -> displacement or initiative change`

### Local response examples
- robe fabric dents under palm/fist,
- shoulder line jolts,
- ribs/torso fold slightly toward the struck side,
- guard angle collapses a few degrees,
- shin/forearm contact sharply decelerates both limbs.

### Whole-body response examples
- torso rotates,
- spine inclines backward,
- support heel lifts,
- rear foot slides,
- one recovery step catches balance,
- knee bends to absorb force,
- hand posts against environment.

Attacker also reacts to contact:
- striking limb decelerates,
- shoulder/hip follow-through compresses into the target,
- blocked limb rebounds or is redirected,
- support leg absorbs collision.

Avoid:
- zero-reaction hits,
- receiver reacting before contact,
- huge knockback from light contact,
- generic backward gliding with no foot mechanics,
- limb visually passing through body,
- impact sound before contact.

## Impact scale

### Minor check
Small line change / guard shift / slight posture reaction.

### Solid hit
Local compression + visible torso/shoulder response + weight/foot consequence.

### Heavy/signature hit
Full posture break, forced recovery steps or environment collision only when setup and force justify it.

Not every hit should produce the same reaction.

## Throws and takedowns

Specify:
- entry,
- grip/contact,
- off-balance direction,
- attacking leg/hip/body placement,
- support point,
- rotation or drive,
- landing relationship.

A throw should not look like telekinesis.

## Exit-state rule

After every major beat answer:
1. Which foot carries most weight?
2. Where is the other foot?
3. What direction is the chest facing?
4. What is the distance?
5. Is the fighter balanced, recovering or falling?
6. What physical effect from the last contact is still present?
7. What motion can happen next without reset?
