---
name: video-combat-director
description: Design physically continuous fight choreography and cinematic AI-video prompts for boxing, kickboxing, Muay Thai, Sanda, MMA, grappling, Chinese martial arts, wuxia, one-vs-many action and action cinema.
---

# Video Combat Director

Design body mechanics first, macro fight logic second, cinematography third.

## Mandatory runtime order

1. Resolve the brief: duration, participants, weapons, environment, initiator, combat style(s), realism/wuxia level, outcome and target format when relevant.
2. If a missing core point would materially change choreography, use `references/brief-confirmation.md`; otherwise do not ask.
3. Read `references/reference-router.md`.
4. Build the complete internal Load Manifest **before** specialized leaf reads.
5. Load only exact references authorized by the router and within its hard budget.
6. Build choreography + body-pose keyframes + spatial ledger.
7. Add cinematography only after physical continuity is valid.
8. Run compact `references/qc-gates.md`; load its specialized QC only when that module is active.
9. Output the user's requested format.

## Runtime loading rules

- Never recursively scan `references/`.
- Never follow a cross-reference from a leaf file automatically.
- Only authorized router/index files can open another reference.
- Do not read `README.md`, `sources.md`, `reference-schema.md`, `tests/`, `reference-ingestion-pipeline.md` or full `routing-contract.md` during ordinary generation.
- `routing-contract.md` is the full governance/audit specification; `reference-router.md` contains the runtime subset needed for generation.
- Stop loading once the manifest already supplies fight engine, movement language, continuity, space and required camera information.

## Composition model

`BRIEF + OPTIONAL ARCHETYPE + BASE STYLE(S) + OPTIONAL MULTI-OPPONENT + OPTIONAL PAIRING/COMBINATION + OPTIONAL CINEMATIC + OPTIONAL DIRECTING/PROFILE + OPTIONAL COMPOSER PROTOCOL + OPTIONAL ATOMIC/CORE`

**Optional means optional. Never populate every layer by default.**

## Universal choreography rules

### Biomechanical beat
`Starting State -> Initiating Limb -> Motion Path -> Defensive Response -> Contact/Miss -> Physical Result -> Exit State`

The exit state must physically support the next beat without reset.

### Mandatory internal Pose Packet
A named technique is not enough. Before writing an important action, internally resolve the body posture needed to perform it correctly.

For standard/complex actions, track:

`support base -> weight distribution -> feet orientation -> knees -> pelvis/hips -> torso -> shoulders/elbows/hands -> head/gaze -> center of mass -> action path -> recovery/exit`

For complex techniques use key poses:

`START -> LOAD / CHAMBER -> CONTACT / PEAK -> RECOVERY / LANDING -> EXIT`

Do not print this schema unless the user asks for technical diagnostics. Compress it into clear natural-language movement description.

#### Pose detail levels

**P0 — simple hand/guide action**
Examples: light parry, wrist guide, probing jab.
Need only stance/facing + limb path + immediate exit.

**P1 — standard power action**
Examples: straight punch, hook, palm, elbow, front kick.
Need support base + hip/torso contribution + limb path + contact posture + recovery.

**P2 — complex lower-body / rotational action**
Examples: side kick, round kick, low sweep, spinning technique.
Must establish start, chamber/load, support-foot/hip organization, peak/contact and landing/recovery.

**P3 — throw / takedown / aerial action**
Must establish entry, connection/control or push-off, off-balance/trajectory, execution peak, landing and final relative orientation.

### Body-pose invariants — mandatory

- Every major force-producing action has a readable support base.
- Large hip rotation needs a plausible support-foot pivot, heel release, stance adjustment or equivalent freedom of the hip.
- Supporting knee should broadly track the support-foot/load direction; avoid unexplained inward collapse or hyperextension.
- Hips/pelvis organize the force path; limbs do not move as detached appendages.
- Torso rotation/lean must remain compatible with the feet, pelvis and center of mass.
- Shoulder/elbow/wrist geometry must stay anatomically connected to the strike path.
- The non-striking hand has a plausible guard, balance or control role.
- Head/gaze remains opponent-aware except for a brief explicitly described rotational phase.
- Do not force chest-front orientation when a technique mechanically requires side-on hip rotation; preserve opponent awareness through head/gaze and attack line.
- One-leg actions need a clear support leg and compensating body position.
- A landing/recovery must restore a usable base before another high-force action.

Style references may vary stance width, guard, torso angle, chamber height, weight bias and recovery, but they should not violate basic anatomy or balance.

### Mandatory internal Impact Packet
Before writing every meaningful C1-C3 contact, internally resolve:

`attacker surface -> exact receiving point -> incoming path -> force vector -> local response -> receiver structural response -> balance/support response -> attacker contact response -> exit state -> next-action link`

Do not print this schema unless the user asks for diagnostics. Use it to make the final prose physically specific.

#### Contact classes

**C0 — brush / probe / light guide**
- exact contact point,
- attack-line change,
- immediate tactical result.

**C1 — defensive collision**
Examples: forearm check, shin check, crossed-arm block, hard frame.
Must show:
- incoming surface,
- defensive receiving surface,
- actual collision,
- both sides decelerate,
- defender structure compresses or redirects,
- attacker trajectory changes,
- next opening.

**C2 — solid body strike**
Examples: palm to sternum, fist to ribs, shoulder to upper chest, kick to torso/thigh.
Must show:
- exact striking surface,
- exact anatomical receiving point,
- force direction,
- local fabric/body compression,
- torso/shoulder/hip structural reaction,
- foot/balance consequence,
- attacker deceleration/recoil/follow-through,
- exit state.

**C3 — signature heavy impact**
Examples: hard kick drives receiver into pillar, shoulder crash folds receiver over railing, throw into floor/table.
Use sparingly and show the full force-transfer chain including environment response when relevant.

**C4 — near miss**
Show:
- closest passing line,
- defender evasion,
- missed limb overextension / forced landing / rotational carry,
- resulting opening.

### Contact / impact force-transfer — mandatory
A meaningful hit, block or body collision is not complete at the word `hit`.

For every **solid contact**, describe at least:
`striking surface -> exact receiving point -> force direction -> local compression/deflection -> posture/balance consequence -> continuation`

The attacker must also show contact physics: deceleration, recoil, redirected limb path or body follow-through.

For a **block/check**, show actual collision and line change; do not write a weightless `clean block`.

For a **near-miss**, show the missed limb's overextension/landing and the defender's body/cloth reaction to the passing line.

Do not make every contact huge. Minor checks can have small reactions; decisive hits need a complete force-transfer chain.

### Impact reaction timing
The visual order must be causal:

`approach -> visible contact -> receiver reaction begins -> displacement/recovery`

Reject:
- anticipatory recoil before touch,
- impact sound before contact,
- debris/dust before body-environment contact,
- a fist stopping centimeters short while the receiver reacts anyway.

For important impacts, the striking limb should visibly reach the receiving surface and decelerate on contact.

### Impact diversity
Do not reuse the same generic backward recoil for every hit.

Match the reaction to contact geometry:
- sternum strike -> backward shoulder/spine recoil + rear support consequence,
- rib-side strike -> lateral fold/rotation + same-side elbow/hip reaction,
- low kick -> loaded-leg disruption + stance change,
- forearm block -> guard compression + attack-line redirection,
- shoulder collision -> center-of-mass displacement,
- body-to-pillar -> abrupt stop/compression + post/rebound/recovery.

### High-density action is allowed
Do **not** reduce action count merely because the sequence is fast.

Instead vary description density:
- P0/C0 minor action/contact: concise,
- P1/C1/C2 important action/collision: enough posture and force detail to remain readable,
- P2/P3/C3 complex/signature action: explicit key poses and full physical chain.

Fast Hong Kong-style choreography may contain many actions as long as important techniques have correct body organization and important contacts remain distinct, consequential and causally connected.

### Combat-facing
Active fighters remain oriented toward the immediate threat. Temporary back-facing requires a described pivot/spin/impact/evasion and coherent recovery.

### Zero Idle
Avoid:
`attack -> stop -> pose -> opponent attacks`

Prefer:
`attack -> block/miss/impact -> changed body/spatial state -> continuation`

Misses, catches, stumbles, environment contact and landings are usable choreography states.

### Aerial logic
`support -> compression -> push-off -> trajectory -> landing -> absorption -> continuation`

Default to one main airborne subject at a time unless a dual-air exchange is explicitly requested and carefully designed.

## Conditional modules

### One-vs-many
Use `archetypes/outnumbered.md` + `multi-opponent/multi-opponent-router.md`, then normally only 1-2 specialized Multi-Opponent leaves.

### Mixed styles
Use Pairing only when different systems create a meaningful tactical conflict.

### Combination
Baseline continuity is already provided by Zero Idle. Load Combination only for a specific transition problem.

### Atomic Action
Load only when one move needs more biomechanical detail than its Style reference provides.

### Body Pose Composer
The compact Pose Packet above applies to every generation without a leaf read.
Load `references/composer/body-pose-composer.md` only when:
- the user explicitly prioritizes technically correct body posture,
- P2/P3 actions are central and need exact key-pose authoring,
- a previous generation shows broken kick/sweep/throw/landing geometry,
- the task is specifically auditing movement posture.

### Contact Impact Composer
The compact Impact Packet above applies to every generation without a leaf read.
Load `references/composer/contact-impact-composer.md` only when hard-hitting / realistic impact is a central authoring need or previous output looked like fake contact.

### Cinematic
Load only for an actual world/movement transformation. Wuxia does not automatically imply Qinggong.

### Directing
Ordinary video output does not automatically require the Directing library. Load it for explicit/critical framing, POV, impact, camera movement, editing, occlusion or environment-photography needs.

### Style Profile
Use at most one named action-cinema profile unless the user explicitly requests comparison/hybridization. Translate mechanisms; do not copy one exact scene.

### Core repair
Core files are diagnostic, not default context. Load only the failed domain.

If hits/blocks/collisions look fake, weightless or like actors touching each other, load `references/core/contact-impact-physics.md`.

## Universal shot-function rules

The camera does not need every fighter, every face or full bodies in every shot.

- wide/full-body: route, footwork, kicks, throws, qinggong, group geography,
- medium: attack-defense relationship, bridge/clinch, tactical angle,
- close: contact, grip, reaction, support/landing detail,
- extreme close: rare decisive information only.

Partial/detail shots must inherit understandable geography.
Complex body mechanics -> simpler camera.
Simple body trajectory -> more expressive camera may be used.

## AI-video defaults

When relevant:
- raw 1.0x real-time speed,
- zero slow-motion unless requested,
- explicit bare-hands / gloves / weapon state,
- no unsupported floating,
- no unexplained side swap or teleportation,
- no automatic pose reset after impact,
- no impact reaction before visual contact,
- no limbs passing through the receiving body,
- no impossible joint orientation or detached-limb motion.

## Output principle

References are mechanics/directing vocabulary, not prose to copy. Use only the selected knowledge for the user's exact fighters, duration, space and visual intent.
