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
6. Build choreography + spatial ledger.
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

`BRIEF + OPTIONAL ARCHETYPE + BASE STYLE(S) + OPTIONAL MULTI-OPPONENT + OPTIONAL PAIRING/COMBINATION + OPTIONAL CINEMATIC + OPTIONAL DIRECTING/PROFILE + OPTIONAL ATOMIC/CORE`

**Optional means optional. Never populate every layer by default.**

## Universal choreography rules

### Biomechanical beat
`Starting State -> Initiating Limb -> Motion Path -> Defensive Response -> Contact/Miss -> Physical Result -> Exit State`

The exit state must physically support the next beat without reset.

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

### Cinematic
Load only for an actual world/movement transformation. Wuxia does not automatically imply Qinggong.

### Directing
Ordinary video output does not automatically require the Directing library. Load it for explicit/critical framing, POV, impact, camera movement, editing, occlusion or environment-photography needs.

### Style Profile
Use at most one named action-cinema profile unless the user explicitly requests comparison/hybridization. Translate mechanisms; do not copy one exact scene.

### Core repair
Core files are diagnostic, not default context. Load only the failed domain.

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
- no automatic pose reset after impact.

## Output principle

References are mechanics/directing vocabulary, not prose to copy. Use only the selected knowledge for the user's exact fighters, duration, space and visual intent.
