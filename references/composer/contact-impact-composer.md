# Contact / Impact Composer Protocol

This is a composition protocol, not a style reference.

Purpose: prevent AI fight prompts from becoming weightless pose exchanges where limbs merely touch.

The compact mandatory version lives in `SKILL.md`. This file is the detailed authoring model for contact-heavy generation, repair and maintenance.

## 1. Core principle

A meaningful contact is a **force-transfer event**, not a verb.

Never compose a solid beat as only:
- punches the chest,
- palm-strikes him,
- blocks the kick,
- crashes into the pillar.

Compose the event as:

`approach -> exact contact geometry -> local material/body response -> structural interruption -> center-of-mass consequence -> support/foot consequence -> attacker recoil/follow-through -> continuation`

## 2. Mandatory internal Impact Packet

Before writing every meaningful solid contact, internally resolve:

```yaml
impact_packet:
  attacker_surface:
  receiver_point:
  incoming_path:
  force_vector:
  contact_quality:
  local_response:
  receiver_structure_response:
  balance_or_support_response:
  attacker_contact_response:
  sound_material:
  exit_state:
  next_action_link:
```

Do not print this YAML unless the user asks for structured diagnostics. Use it to author the final prose.

## 3. Contact classes

### C0 — Brush / probe / light hand contact
Minimum:
- contact point,
- line change,
- immediate tactical result.

Example:
`his left palm brushes the outside of the incoming wrist, shifting the punch just outside centerline and opening the inside lane.`

No large body recoil is needed.

### C1 — Defensive collision
Examples:
- forearm check,
- shin check,
- crossed-arm block,
- shoulder frame.

Minimum:
- incoming surface,
- receiving defensive surface,
- collision point,
- both limbs decelerate,
- defender structure compresses or redirects,
- attacker trajectory changes,
- next opening.

A block with no force consequence is invalid.

### C2 — Solid body strike
Examples:
- palm to sternum,
- fist to ribs,
- shoulder into upper chest,
- kick to torso/thigh.

Minimum:
- exact striking surface,
- exact anatomical receiving point,
- force direction,
- local fabric/body compression,
- torso/shoulder/hip reaction,
- balance/foot consequence,
- attacker's deceleration/follow-through,
- exit state.

### C3 — Signature heavy impact
Examples:
- hard kick drives receiver into pillar,
- shoulder crash folds receiver over railing,
- throw into floor/table.

Use sparingly.

Require the full chain:
- approach and acceleration,
- exact contact,
- receiving material/body deformation,
- posture break,
- center-of-mass travel,
- multi-step / hand-post / environment consequence,
- attacker's mass transfer and recovery,
- environment reaction if relevant,
- sound,
- continuation.

Heavy does not mean exaggerated flight.

### C4 — Near miss
Require:
- closest passing point,
- defender body evasion,
- air/cloth reaction where useful,
- attacker's overextension / forced landing / rotational carry,
- next opening.

A miss that changes nothing is not useful choreography.

## 4. Exact receiving points

Prefer precise, visible regions instead of generic `body` / `torso`.

Examples:
- upper sternum,
- left/right pectoral line,
- lower floating-rib region,
- shoulder cap / shoulder line,
- upper arm,
- forearm outside line,
- outer thigh,
- shin,
- hip line,
- upper back,
- side of torso.

For guarded impacts:
- crossed forearms at chest height,
- outside of lead forearm,
- raised shin,
- elbow/forearm frame.

For environment:
- right shoulder blade into wooden pillar,
- upper back into whitewashed wall,
- palm onto stone railing,
- hip onto bench edge.

## 5. Exact striking surfaces

Examples:
- palm heel,
- first two knuckles,
- outer forearm bone,
- elbow point / proximal forearm,
- shoulder mass,
- knee cap / upper shin line,
- shin,
- heel,
- ball/sole of foot.

Use only surfaces that match the chosen movement.

## 6. Force-vector discipline

The receiver reaction must follow the actual force vector.

Examples:

### Straight palm to sternum
Force:
`front-to-back through the torso`

Expected:
- sternum fabric dents,
- shoulder line recoils,
- spine inclines backward,
- weight transfers toward rear support,
- rear foot slides or steps to catch center.

### Palm / hook to ribs
Force:
`lateral / rotational through one side of torso`

Expected:
- local rib-side fabric folds,
- same-side elbow tightens,
- torso bends/rotates,
- hip and foot adjust to preserve balance.

### Side kick into crossed forearms
Force:
`horizontal through guard`

Expected:
- forearms compress toward chest,
- elbows bend,
- shoulders recoil,
- receiver base slides or widens,
- kicking leg decelerates / rebounds / redirects.

### Low kick to outer thigh
Force:
`lateral into loaded leg`

Expected:
- thigh line shifts,
- knee softens or weight is unloaded,
- stance changes,
- next step is affected.

## 7. Receiver hierarchy

For a solid hit, describe at least two levels of consequence:

1. **local** — fabric, skin-safe compression, guard deformation, limb deflection,
2. **structural** — shoulder/spine/hip/guard alignment changes,
3. **support** — foot slide, recovery step, knee absorption, hand post.

For C2 solid impacts: normally use local + structural + support.
For C3 heavy impacts: use all three plus environment if applicable.

## 8. Attacker contact response

The attacker must not behave as if striking empty air.

Choose one or more:
- shoulder/hip visibly decelerates,
- striking limb compresses into target briefly,
- support leg absorbs reaction force,
- blocked limb rebounds,
- redirected limb changes path,
- body follows through into a new stance,
- grip/frame remains connected into next action.

Never let a limb visually pass through the receiver.

## 9. Timing rule

The order must be visually causal:

`approach -> contact frame -> receiver reaction begins -> displacement/recovery`

Never:
- receiver recoils before contact,
- dust/debris erupts before impact,
- impact sound occurs before visible contact.

For AI prompts, explicitly use phrases such as:
- `the reaction begins exactly at contact`,
- `no anticipatory recoil`,
- `the striking limb visibly decelerates on impact`.

Use only when needed; do not repeat after every light touch.

## 10. Impact diversity

Do not give every strike the same reaction.

Map reaction to:
- target point,
- force direction,
- strike mass,
- receiver stance,
- current momentum,
- environment.

Examples:
- sternum palm -> backward structure break,
- rib palm -> lateral fold/rotation,
- shoulder collision -> torso displacement,
- forearm check -> limb-line change,
- low kick -> stance disruption,
- wall collision -> compression/post/rebound.

## 11. High-density choreography rule

High action density is allowed.

Do **not** reduce the number of actions merely to make impacts more detailed.

Instead use three writing densities:

### Minor contact — compressed
`left forearm checks the wrist outward, shifting the punch off center.`

### Solid contact — medium detail
`his palm heel lands on the upper sternum; robe fabric dents, the shoulder line snaps backward and the rear foot skids half a step to catch balance.`

### Signature impact — full detail
Use the complete force-transfer chain.

This preserves rapid Hong Kong-style action while keeping the important hits heavy.

## 12. Block / parry distinction

### Parry / guide
- small contact,
- attack line changes,
- little body displacement.

### Structural block / check
- collision,
- both sides decelerate,
- guard/support structure takes load,
- trajectory changes.

### Hard collision
- guard compresses into body,
- stance is affected,
- attacker limb rebounds or changes route.

Do not describe every defense as a generic `block`.

## 13. Environment impact

For body -> environment:

`body region -> exact surface -> surface material response -> receiver compression/recoil -> support/recovery`

Examples:
- shoulder hits wood -> dull thud + wood vibration + shoulder/torso compression,
- back hits plaster -> powder sheds after contact + torso stops abruptly,
- palm posts on pillar -> shoulder/elbow compresses as hand accepts body weight.

Environment damage must be proportional and persistent.

## 14. Camera proof for signature impacts

A signature hit should be readable in at least one shot.

The camera may show:
- full-body force path,
- medium torso impact,
- close contact insert,
- foot recovery,
- environment result.

It does **not** need all of them.

Do not cut so tightly that the audience cannot tell whose limb hit whose body.

## 15. Sound as force evidence

Sound reinforces, but never substitutes for visual impact.

Examples:
- palm/fist to robe-covered torso -> dense short thud + cloth slap,
- forearm collision -> dry hard knock,
- shin/forearm -> sharper contact,
- shoulder/body -> deeper mass-heavy thump,
- body/wood -> dull structural impact + vibration,
- shoe/stone recovery -> sole scrape after displacement.

Synchronize sound exactly to contact.

## 16. Invalid fake-fight patterns

Reject or rewrite:
- `A hits B` with no receiving point,
- `B blocks` with no collision mechanics,
- hard strike but B stays perfectly upright,
- generic sliding backward with no support-foot logic,
- attack visually stops short of target,
- receiver reacts before touch,
- limbs pass through the body,
- every hit produces identical backward recoil,
- block looks like actors tapping arms,
- heavy hit followed by instant clean stance reset.

## 17. Final authoring test

For every important impact, ask:

1. What exact surface is striking?
2. What exact point receives it?
3. In what direction is force traveling?
4. What changes locally at contact?
5. What part of receiver structure is interrupted?
6. How does center of mass / support react?
7. How does the attacker react to resistance?
8. What physical state now makes the next action possible?

If the answer is missing for a solid/signature contact, the beat is incomplete.
