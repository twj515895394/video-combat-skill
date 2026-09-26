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

## QC-2 Body Pose / Technique Geometry
For every important P1-P3 action:
- support base is understandable,
- foot orientation supports the hip/pelvis action,
- supporting knee is mechanically plausible,
- pelvis/torso/shoulder chain matches the limb path,
- non-striking hand has a plausible guard/control/balance role,
- head/gaze remains opponent-aware except for a brief justified rotation,
- center of mass remains supported or follows a clear trajectory,
- recovery/landing leads to a usable exit state.

For P2/P3 actions, verify the key-pose chain:
`START -> LOAD/CHAMBER -> PEAK/CONTACT -> RECOVERY/LANDING -> EXIT`

Reject:
- kick with no support leg,
- impossible support-foot / knee / hip orientation,
- detached arm movement,
- accidental permanent back-facing,
- sweep with no lowered center/support base,
- throw before control/off-balance/body positioning,
- landing directly into another power move with no base recovery.

## QC-3 Body Continuity
For each important beat:
- initiating limb / body path is understandable,
- defense/contact/miss is understandable,
- physical result changes posture, balance, position, line or initiative,
- exit state can physically produce the next beat,
- no unexplained reset or teleportation.

## QC-4 Contact / Impact Physics
For every meaningful solid hit, block or collision:
- exact striking surface is understandable,
- exact receiving point is specified or visually implied precisely,
- force direction is coherent,
- local compression / deflection / sudden deceleration is described,
- receiver structure changes at contact,
- meaningful force reaches balance / feet / support,
- attacker also shows recoil, deceleration, redirection or follow-through,
- reaction starts after contact, not before,
- the resulting body state feeds the next action.

Reject weightless language such as:
- “hits him” with no receiving point,
- “blocks cleanly” with no collision effect,
- hard torso hit with receiver remaining rigid,
- generic backward glide with no foot recovery,
- identical reaction to every strike.

High action density is allowed. Do **not** reduce action count merely because the sequence is fast. Instead require the important contacts to remain mechanically distinct and physically consequential.

## QC-5 Facing / Ground / Aerial
- active opponents remain oriented toward the immediate threat,
- back-facing has a described cause and recovery,
- support/push-off/trajectory/landing are coherent for elevated motion,
- no unsupported floating,
- default one main airborne subject at a time unless explicitly designed otherwise.

## QC-6 Zero Idle / Tempo
- no attack-stop-pose-opponent-turn loop,
- misses/blocks/landings become usable next states,
- when both fighters are substantially visible and exchanging complete techniques, tempo is fast/continuous rather than instructional,
- slow emphasis is created primarily through tighter framing / detail / reaction / result shots, not slow full-body turn-taking,
- the next threat may begin during the physical resolution of the previous beat when mechanics permit it,
- selected style remains visible through range, stance, tools and decisions.

Reject:
- long static two-person master shot for most of the fight,
- one fighter waiting motionless while the other completes a full technique,
- every exchange returning to neutral spacing,
- artificial slowness used only to make actions readable.

## QC-7 Causal Continuity
If a Combination reference was loaded:
- next action exists because the prior state changed,
- current range/stance supports the continuation,
- initiative flips for a physical reason.

If the same logic was already obvious from Style/archetype, re-check whether the Combination leaf was unnecessary.

## QC-8 Basic Camera Readability
- important mechanics are visible at least once,
- partial/detail shots inherit known geography,
- attack direction remains coherent,
- camera does not hide required support foot / throw entry / landing,
- signature impacts show enough receiving-body information to read force transfer,
- not every shot is forced to show both fighters or both faces,
- single-attacker, single-defender, contact-only and result-only shots are allowed when spatial direction is preserved.

## QC-9 Stability / Duration
When relevant:
- weapons/gloves/bare hands are controlled,
- speed is controlled,
- no unexplained screen-side swap,
- no random synchronized jumping,
- ~10 seconds may contain dense action, provided it forms continuous kinetic phases rather than disconnected move lists.

## Conditional QC

### One-vs-many
If Multi-Opponent module is active, additionally load:
`qc/multi-opponent-qc.md`

### Detailed cinematography / Style Profile
If Directing or a named action-cinema Style Profile is active, additionally load:
`qc/directing-qc.md`

Do not load either specialized QC for a simple 1v1 that does not use those modules.
