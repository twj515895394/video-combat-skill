# Core Combat QC

Run this compact QC for every generated fight.
Load specialized QC only when its module is active.

## QC-0 Brief
- core brief is sufficiently known,
- only material ambiguity was clarified,
- known information was not re-asked.

## QC-1 Routing
- Load Manifest was decided before leaf reads,
- every loaded leaf has one concrete reason,
- no leaf triggered a transitive follow-up read,
- no unrelated sibling files were loaded,
- task stays within the hard leaf budget defined by `reference-router.md`,
- if one loaded leaf can be removed without reducing answer quality, remove it.

Common overlap failures:
- named Style Profile + generic Hong Kong fallback,
- qinggong loaded only because genre = wuxia,
- Combination loaded only because all fights need continuity,
- Atomic/Core loaded without a specific mechanic/failure,
- generic camera core + several detailed Directing files.

## QC-2 Body Continuity
For each important beat:
- initiating limb / body path is understandable,
- defense/contact/miss is understandable,
- physical result changes posture, balance, position, line or initiative,
- exit state can physically produce the next beat,
- no unexplained reset or teleportation.

## QC-3 Facing / Ground / Aerial
- active opponents remain oriented toward the immediate threat,
- back-facing has a described cause and recovery,
- support/push-off/trajectory/landing are coherent for elevated motion,
- no unsupported floating,
- default one main airborne subject at a time unless explicitly designed otherwise.

## QC-4 Zero Idle / Style
- no attack-stop-pose-opponent-turn loop,
- misses/blocks/landings become usable next states,
- selected style is visible through range, stance, tools and decisions,
- cinematic treatment does not erase the base movement system.

## QC-5 Causal Continuity
If a Combination reference was loaded:
- next action exists because the prior state changed,
- current range/stance supports the continuation,
- initiative flips for a physical reason.

If the same logic was already obvious from Style/archetype, re-check whether the Combination leaf was unnecessary.

## QC-6 Basic Camera Readability
- important mechanics are visible at least once,
- partial/detail shots inherit known geography,
- attack direction remains coherent,
- camera does not hide required support foot / throw entry / landing.

## QC-7 Stability / Duration
When relevant:
- weapons/gloves/bare hands are controlled,
- speed is controlled,
- no unexplained screen-side swap,
- no random synchronized jumping,
- ~10 seconds uses roughly 3 meaningful kinetic phases rather than too many disconnected moves.

## Conditional QC

### One-vs-many
If Multi-Opponent module is active, additionally load:
`qc/multi-opponent-qc.md`

### Detailed cinematography / Style Profile
If Directing or a named action-cinema Style Profile is active, additionally load:
`qc/directing-qc.md`

Do not load either specialized QC for a simple 1v1 that does not use those modules.
