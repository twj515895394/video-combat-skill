---
name: video-combat-director
description: Design physically continuous fight choreography and AI-video prompts for boxing, kickboxing, Muay Thai, Sanda, MMA, wrestling/grappling, Chinese martial arts, wuxia and cinematic action. Use when the user asks for fight design, combat choreography, martial-arts action, wuxia combat, fight-camera design, action prompt generation, or analysis/repair of generated fight footage.
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
   - primary weapons (hands, elbows, knees, legs, clinch, throws),
   - preferred entry and exit,
   - defensive language.
5. Build spatial ledger: screen side, facing direction, distance, feet, balance, obstacles.
6. Choreograph with Zero Idle:
   previous result -> next starting state.
7. Assign camera only after the body mechanics are valid.
8. Run QC from `references/qc-gates.md`.
9. Output the user's requested prompt format.

## Three-layer composition model

A fight request is normally composed from:

`BASE COMBAT STYLE + CHOREOGRAPHY LOGIC + CINEMATIC LAYER`

Examples:

- `boxing + pressure-vs-counter + grounded-modern-action`
- `muay-thai + clinch-pressure + gritty-ring-action`
- `sanda + kick-catch-throw + sports-action`
- `southern-nanquan + northern-longfist + grounded-wuxia`
- `bajiquan + close-range-crash + hong-kong-action-language`

**Wuxia is not a base martial art.** It is a cinematic transformation layer placed on top of a concrete movement system.

## Hard biomechanics rules

For every important action beat, specify:

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
- do not use vague "moves behind him" language without describing the path and opponent response.

## Zero Idle

Never write:
`attack -> stop -> pose -> opponent attacks`.

Write:
`attack -> deflection/impact/miss -> altered balance/position -> immediate continuation`.

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

Selective loading is mandatory.

For substantial tasks:
1. read `references/reference-router.md`,
2. choose one or two base-style files,
3. optionally choose one cinematic layer,
4. optionally choose one pairing file if the two fighters use meaningfully different systems,
5. load core biomechanics only when needed for ambiguity or repair.

Do not load sibling style files "for inspiration".

## Output principle

Reference material is a vocabulary and mechanics library, not text to copy verbatim.
Translate selected reference knowledge into the user's exact fighters, space, duration and desired result.
