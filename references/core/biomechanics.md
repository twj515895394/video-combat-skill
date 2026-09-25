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

`support -> weight transfer -> hip/shoulder linkage -> limb path -> contact/miss -> recoil/continuation -> new base`

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
- whether the leg retracts or lands forward,
- landing orientation.

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

## Impact grammar

Readable impact:
`approach -> exact contact -> momentary compression/interruption -> receiver reaction -> displacement or initiative change`

Avoid:
- zero-reaction hits,
- huge knockback from light contact,
- body moving before contact,
- impact sound before contact.

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
6. What motion can happen next without reset?
