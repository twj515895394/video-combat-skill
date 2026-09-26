# Multi-Opponent Combat Router

Use this layer when one protagonist fights 2+ opponents.

This router solves scheduling and spatial problems unique to one-vs-many. It does not replace base style, biomechanics, combination causality or general directing.

## Runtime rule

Read this router only after `archetypes/outnumbered.md` is selected by the root router.

Then choose **1-2 specialized multi-opponent leaves by default**.
Do not load all four merely because they are available.

| Dominant problem | Route |
|---|---|
| 谁当前进攻、下一位如何提前切入、避免回合制 | `active-attacker-scheduling.md` |
| 主角路线、包围圈、通道压缩、柱子桌子门框 | `spatial-funneling.md` |
| 镜头必须围绕主角、局部敌人入镜、空间重建 | `protagonist-centric-directing.md` |
| 被打退敌人恢复重入、画外威胁、声音提示 | `recovery-reentry-and-sound.md` |

## Selection defaults

### Generic 1-vs-3 / 1-vs-4 choreography
Prefer:
- `active-attacker-scheduling.md`
- `spatial-funneling.md`

These two solve the most common AI failures: turn-taking and simultaneous body chaos.

### Camera-heavy one-vs-many
Prefer:
- `active-attacker-scheduling.md`
- `protagonist-centric-directing.md`

Do not additionally load generic framing unless the user asks for a special shot problem.

### Reentry / persistent enemies / off-screen threat emphasis
Prefer:
- one scheduling or spatial file,
- `recovery-reentry-and-sound.md`

## Opponent state classes

Every relevant opponent should occupy one current state:
- ACTIVE_ATTACKER
- SUPPORTING_ATTACKER
- APPROACHING
- FLANKING
- BLOCKING_EXIT
- RECOVERING
- TEMPORARILY_DISPLACED
- DOWN / PHASED_OUT
- REENTERING

## Default active-attacker budget

For short AI-video combat:
- usually 1 immediate active attacker,
- occasionally 2 overlapping immediate threats,
- remaining opponents stay in movement/support states.

## Core design order

1. Define protagonist route.
2. Define choke points / open lanes.
3. Assign enemy starting zones.
4. Schedule attack-right handoffs.
5. Define recovery/reentry only when it matters.
6. Choose individual techniques.
7. Design camera around protagonist and immediate threat.

## No transitive loading

This router may authorize the specialized files above.
The specialized leaf files themselves cannot authorize any further reference reads.
If another domain becomes necessary, return to the root `reference-router.md` and revise the Load Manifest.
