---
name: video-combat-director
description: Design physically continuous fight choreography and cinematic AI-video prompts for boxing, kickboxing, Muay Thai, Sanda, MMA, grappling, Chinese martial arts, wuxia and action cinema. Use when the user asks for fight design, combat choreography, martial-arts action, wuxia combat, cinematic fight-camera design, action prompt generation, or analysis/repair of generated fight footage.
---

# Video Combat Director

Design the fight as a physical state machine first, then design how cinema reveals that action.

## Mandatory execution order

1. Resolve duration, participants, weapons, environment, initiator, outcome and requested combat style.
2. Read `references/reference-router.md`.
3. Select the smallest useful reference set. Never recursively scan `references/`.
4. Establish each fighter's Combat DNA:
   - base style,
   - effective range,
   - stance / weight bias,
   - primary tools,
   - preferred entry and exit,
   - defensive language.
5. Select Combination Pattern only when continuity needs one.
6. Load Atomic Action detail only for mechanics needing extra precision.
7. Build spatial ledger: screen side, facing direction, distance, feet, balance, obstacles.
8. Choreograph with Zero Idle: previous result -> next starting state.
9. Only after body mechanics are valid, assign shot function:
   - spatial proof,
   - biomechanics proof,
   - threat / POV,
   - impact insert,
   - momentum/result,
   - environment result.
10. If cinematic shooting matters, route through `references/directing/directing-router.md`.
11. If a film/director/choreographer reference is requested, load one analytical Style Profile and translate it into abstract visual grammar.
12. Run QC from `references/qc-gates.md`.
13. Output the user's requested prompt format.

## Composition model

A fight is assembled as:

`BASE STYLE(S) + COMBINATION CAUSALITY + OPTIONAL ATOMIC DETAIL + CINEMATIC LAYER + DIRECTING GRAMMAR + OPTIONAL STYLE PROFILE`

Examples:
- `boxing + counter-conversions + grounded-modern-action + impact-inserts`
- `sanda + clinch-throw-transitions + full-body throw proof`
- `southern-nanquan vs northern-longfist + range-conversions + grounded-wuxia + wuxia-spatial-chains + new-wave-HK-wuxia profile`

## Hard biomechanics rule

For every important action beat:

`Starting State -> Initiating Limb -> Motion Path -> Defensive Response -> Contact/Miss -> Physical Result -> Exit State`

Exit State must establish:
- foot placement,
- torso/facing direction,
- balance,
- distance,
- current momentum,
- environment relationship.

Never allow unexplained reset to stance.

## Combat-facing lock

During active close combat:
- fighters keep chest/head/eyes oriented toward the opponent,
- 20-60 degree tactical side-on orientation is allowed,
- back-facing must be caused by a specifically described pivot/spin/impact/evasion and must resolve coherently,
- do not use vague "moves behind him" language without describing path and opponent response.

## Zero Idle

Never:
`attack -> stop -> pose -> opponent attacks`

Use:
`attack -> deflection/impact/miss -> altered balance/position -> immediate continuation`

Misses, blocks, catches, stumbles, wall contact and landings are choreography states.

## Film-language rule

The camera does not need to show:
- both fighters,
- both faces,
- full bodies,
in every shot.

A valid action shot may isolate:
- fist approaching lens,
- shin meeting forearm,
- palm compressing chest fabric,
- wrist trap,
- support foot pivot,
- foot planting on pillar,
- shoulder hitting wall,
- wood splintering,
- robe/sleeve wiping frame,
- landing feet,
- eyes snapping toward threat.

But partial/detail shots must inherit a previously understandable spatial relationship and cannot hide mechanics that still need proof.

## Shot-function rule

Choose framing by what the audience must learn.

- Wide/full-body: route, footwork, kicks, throws, qinggong, multiple fighters.
- Medium: attack-defense relationship, bridge/clinch, angle.
- Close: contact, grip, guard compression, reaction, foot plant.
- Extreme close: rare decisive detail only.

Complex body mechanics -> simpler camera.
Simple body route -> camera may be more expressive.

## Style-profile rule

Named filmmakers/choreographers may be used internally as analytical references.

Final prompt should translate to abstract mechanisms such as:
- kinetic new-wave Hong Kong wuxia,
- rhythmic widescreen staging,
- prop-driven action geometry,
- grounded full-body martial-arts proof,
- practical weighted stunt action.

Do not copy one exact scene or output only “in the style of [name]”.

## AI-video physical constraints

When appropriate:
- raw 1.0x real-time speed,
- zero slow-motion unless explicitly requested,
- explicit bare hands / no gloves / no weapons when required,
- one main airborne subject at a time by default,
- every jump has support -> push-off -> trajectory -> landing,
- no unsupported floating,
- no unexplained side swap or teleportation.

## Reference routing

For substantial tasks:
1. read `references/reference-router.md`,
2. choose one or two base-style files,
3. optionally choose one pairing file,
4. optionally choose one combination-pattern file,
5. optionally choose one cinematic layer,
6. optionally choose directing files and one style profile,
7. load atomic/core detail only when necessary.

Do not load sibling files "for inspiration".

## Output principle

Reference material is a mechanics and directing vocabulary, not text to copy verbatim.
Translate selected knowledge into the user's exact fighters, space, duration, desired result and visual intent.
