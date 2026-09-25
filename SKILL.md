---
name: video-combat-director
description: Design physically continuous fight choreography and AI-video prompts for boxing, kickboxing, Muay Thai, Sanda, MMA, grappling, Chinese martial arts, wuxia and cinematic action. Use when the user asks for fight design, combat choreography, martial-arts action, wuxia combat, fight-camera design, action prompt generation, or analysis/repair of generated fight footage.
---

# Video Combat Director

Design the fight as a physical state machine before writing cinematic prose.

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
5. If the sequence needs help becoming continuous, select one Combination Pattern.
6. Load Atomic Action detail only for mechanics that need extra precision.
7. Build spatial ledger: screen side, facing direction, distance, feet, balance, obstacles.
8. Choreograph with Zero Idle: previous result -> next starting state.
9. Assign camera only after body mechanics are valid.
10. Run QC from `references/qc-gates.md`.
11. Output the user's requested prompt format.

## Composition model

A fight is assembled as:

`BASE STYLE(S) + COMBINATION CAUSALITY + OPTIONAL ATOMIC DETAIL + CINEMATIC LAYER`

Examples:
- `boxing + counter-conversions + grounded-modern-action`
- `muay-thai + pressure-chains + grounded-modern-action`
- `sanda + clinch-throw-transitions`
- `southern-nanquan vs northern-longfist + range-conversions + grounded-wuxia`
- `bajiquan + pressure-chains + hong-kong-action-language`

**Wuxia is not a base martial art.** It is a cinematic transformation layer placed on top of concrete movement mechanics.

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

Misses, blocks, catches, stumbles, wall contact and landings are valuable choreography states.

## AI-video physical constraints

When appropriate:
- raw 1.0x real-time speed,
- zero slow-motion unless explicitly requested,
- explicit bare hands / no gloves / no weapons when required,
- one main airborne subject at a time by default,
- every jump has support -> push-off -> trajectory -> landing,
- no unsupported floating,
- no unexplained side swap or teleportation.

## Camera rule

Camera serves readable action.

Use shot functions:
- spatial proof,
- biomechanics proof,
- impact proof,
- momentum/result proof.

Not every shot needs both fighters.
Not every shot needs faces.
Feet, hips, hands, forearms, contact points, clothing momentum and landing can carry a shot.

Complex body mechanics -> simpler camera.
Complex camera move -> simpler body route.

## Reference routing

For substantial tasks:
1. read `references/reference-router.md`,
2. choose one or two base-style files,
3. optionally choose one pairing file,
4. optionally choose one combination-pattern file,
5. optionally choose one cinematic layer,
6. load atomic/core detail only when necessary.

Do not load sibling style files "for inspiration".

## Output principle

Reference material is a mechanics vocabulary, not text to copy verbatim.
Translate selected knowledge into the user's exact fighters, space, duration and desired result.
