---
name: video-combat-director
description: Design physically continuous fight choreography and cinematic AI-video prompts for boxing, kickboxing, Muay Thai, Sanda, MMA, grappling, Chinese martial arts, wuxia, one-vs-many action and action cinema.
---

# Video Combat Director

Design the fight as a physical state machine first, then decide the macro fight engine, then decide how cinema reveals the action.

## Mandatory runtime order

1. Resolve the brief: duration, participants, weapons, environment, initiator, combat style(s), realism/wuxia level, desired outcome and target format when relevant.
2. If a missing core point would materially change choreography, use `references/brief-confirmation.md`; otherwise do not ask.
3. Read `references/routing-contract.md`.
4. Read `references/reference-router.md`.
5. Build the complete internal Load Manifest **before** reading specialized leaf references.
6. Load only the exact leaf files authorized by the router and within budget.
7. Build choreography and spatial ledger.
8. Add cinematography only after body mechanics and continuity are valid.
9. Run `references/qc-gates.md`.
10. Output the user's requested format.

## Runtime routing hard rules

- Never recursively scan `references/`.
- Never follow a cross-reference from a leaf file automatically.
- Only router/index files listed in `routing-contract.md` may authorize another read.
- Do not read `README.md`, `sources.md`, `reference-schema.md`, `tests/` or `reference-ingestion-pipeline.md` during normal generation.
- Stop loading when the current Load Manifest already answers the fight engine, movement language, causal continuity, spatial continuity and required camera information.

## Composition model

`BRIEF + OPTIONAL ARCHETYPE + BASE STYLE(S) + OPTIONAL MULTI-OPPONENT LAYER + OPTIONAL PAIRING/COMBINATION + OPTIONAL CINEMATIC + OPTIONAL DIRECTING/PROFILE + OPTIONAL ATOMIC/CORE DETAIL`

Optional means optional. Do not populate every layer by default.

## Universal choreography rules

### Hard biomechanics
For every important action beat:

`Starting State -> Initiating Limb -> Motion Path -> Defensive Response -> Contact/Miss -> Physical Result -> Exit State`

Exit State should establish enough of:
- foot placement,
- torso/facing direction,
- balance,
- distance,
- current momentum,
- environment relationship,
for the next action to begin without reset.

### Combat-facing lock
During active close combat:
- head/chest/eyes remain oriented toward the immediate threat,
- tactical side-on angles are valid,
- back-facing must be caused by a described pivot/spin/impact/evasion and resolve coherently.

### Zero Idle
Never design:
`attack -> stop -> pose -> opponent attacks`

Prefer:
`attack -> block/miss/impact -> changed body/spatial state -> immediate continuation`

Misses, catches, stumbles, wall contact and landings are usable choreography states.

### Ground and aerial logic
When elevation occurs:
`support -> compression -> push-off -> trajectory -> landing -> absorption -> continuation`

Default to one main airborne subject at a time unless the user explicitly requests a carefully choreographed dual-air exchange.

## Conditional modules

### One-vs-many
If one protagonist fights 2+ opponents:
- select `archetypes/outnumbered.md`,
- read `multi-opponent/multi-opponent-router.md`,
- load only the 1-2 specialized multi-opponent leaf files required by the actual scene problem.

The detailed scheduling, funneling, directing, recovery and reentry rules live in that module and are not global 1v1 context.

### Mixed styles
Load `pairings/style-vs-style.md` only when the tactical contrast between systems matters to the fight engine.

### Combination grammar
Do not load by default. Baseline continuity is already covered by Zero Idle.
Use Combination only for a specific transition problem.

### Atomic actions
Load only when a specific move needs extra biomechanical precision beyond the chosen Style reference.

### Cinematic layers
Use only when the user requests a world/stunt transformation such as grounded wuxia, qinggong or grounded modern action.
Qinggong is not automatically implied by wuxia.

### Directing
Ordinary video generation does not automatically require the Directing library.
Load it when the request specifically depends on framing, POV, impact inserts, camera movement, editing rhythm, occlusion, damage photography or another cinematography problem.

### Action-cinema style profiles
Use at most one named Style Profile unless the user explicitly asks to compare or hybridize traditions.
Translate the profile into abstract staging/camera/rhythm mechanisms; do not copy one specific scene.

### Core repair
Core files are diagnostic/repair references, not default context.
Load only the exact failed domain.

## Universal shot-function rules

The camera does not need to show every fighter, every face or full bodies in every shot.

Choose framing by information:
- wide/full-body: route, footwork, kicks, throws, qinggong, group geography,
- medium: attack-defense relationship, bridge/clinch, tactical angle,
- close: contact, grip, guard compression, reaction, foot plant,
- extreme close: rare decisive detail.

Valid action subjects include:
- fist approaching lens,
- shin meeting forearm,
- palm compressing torso fabric,
- support-foot pivot,
- landing feet,
- shoulder hitting wall,
- sleeve wiping frame,
- partial incoming threat.

Partial/detail shots must inherit understandable spatial continuity.

Complex body mechanics -> simpler camera.
Simple body trajectory -> more expressive camera may be used.

## AI-video defaults

When relevant:
- raw 1.0x real-time speed,
- zero slow-motion unless explicitly requested,
- explicit bare hands / gloves / weapons constraints,
- no unsupported floating,
- no unexplained side swap or teleportation,
- no automatic pose reset after impact.

## Output principle

Reference material is a mechanics/directing vocabulary, not text to copy verbatim.
Translate only the selected knowledge into the user's exact fighters, duration, space, desired result and visual intent.
