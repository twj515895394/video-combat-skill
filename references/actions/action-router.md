# Atomic Action Router

Do not load all action files by default.

Load only when a specific mechanic needs detail.

| Need | File |
|---|---|
| stepping, pivot, angle, stance transition | `footwork.md` |
| punches, palm, elbow, shoulder | `hand-strikes.md` |
| kicks, sweeps, knees | `kicks-knees.md` |
| parry, slip, check, catch, frame | `defense-counter.md` |
| wrist/arm/clinch/body control | `clinch-control.md` |
| throws, trips, shots, sprawl | `throws-takedowns.md` |

## Atomic action requirement

An atomic action is not only a move name.
For P1-P3 techniques, the leaf should clarify enough of the following to prevent broken posture:

`START -> LOAD / CHAMBER -> PEAK / CONTACT -> RECOVERY / LANDING -> EXIT`

Key pose fields may include:
- support foot / support leg,
- weight distribution,
- knee direction,
- pelvis / hip orientation,
- torso lean / rotation,
- shoulder / elbow / wrist relation,
- non-striking hand role,
- head / gaze,
- center of mass,
- recovery / landing.

Do not force every atomic card to be verbose if the action is simple.
Use more key-pose detail for kicks, sweeps, spinning actions, throws and aerial techniques.

## Precedence

Style reference chooses the tactical vocabulary and may modify stance/guard/weight bias.
Atomic action clarifies the biomechanical execution.
`composer/body-pose-composer.md` governs cross-style posture correctness when multiple techniques need detailed pose authoring.

Never use an atomic card to force a technique that the selected style should not emphasize.

Examples:
- Boxing request + exact pivot mechanics -> boxing.md + footwork.md.
- Sanda catch-and-throw -> sanda.md + defense-counter.md + throws-takedowns.md only if exact mechanics are required.
- Southern fist short palm -> southern-nanquan.md + hand-strikes.md only if extra biomechanics are needed.
- Several complex kicks all show broken posture -> prefer body-pose-composer.md instead of loading multiple atomic leaves.
