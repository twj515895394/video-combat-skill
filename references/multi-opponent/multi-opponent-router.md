# Multi-Opponent Combat Router

Use this layer when one protagonist fights 2+ opponents.

This layer does not replace:
- Fight Scene Archetype,
- base combat style,
- atomic mechanics,
- combination causality,
- directing grammar.

It solves the additional scheduling and spatial problems created by multiple opponents.

## Mandatory load for one-vs-many

When `archetypes/outnumbered.md` is selected, read this router.

Then load only the exact files needed:

| Problem | Route |
|---|---|
| 谁当前进攻、谁下一位切入、避免回合制 | `active-attacker-scheduling.md` |
| 主角路线、包围圈、通道压缩、柱子桌子门框 | `spatial-funneling.md` |
| 镜头始终围绕主角、敌人局部入镜、空间重建 | `protagonist-centric-directing.md` |
| 被打退敌人如何恢复重入、画外威胁与声音 | `recovery-reentry-and-sound.md` |

## Multi-opponent state classes

Every opponent should occupy one current state:

- ACTIVE_ATTACKER
- SUPPORTING_ATTACKER
- APPROACHING
- FLANKING
- BLOCKING_EXIT
- RECOVERING
- TEMPORARILY_DISPLACED
- DOWN / PHASED_OUT
- REENTERING

Do not let all enemies become ACTIVE_ATTACKER simultaneously.

## Default active-attacker budget

For short AI-video combat:
- usually 1 active attacker,
- occasionally 2 overlapping attackers,
- remaining opponents stay in movement/support states.

This creates continuous pressure without body merging or synchronized attacks.

## Core order of design

1. Define protagonist route through the scene.
2. Define environment choke points.
3. Assign enemy starting zones.
4. Schedule attack-right handoffs.
5. Define recovery/reentry states.
6. Only then choose individual techniques.
7. Design camera around protagonist and current threat.

## 10-second default

Prefer roughly:
- 0-3s: first pressure + second attacker already entering,
- 3-6s: route change / funnel / target handoff,
- 6-10s: renewed overlap, short reversal or breakout.

This is a flexible kinetic structure, not rigid timecode choreography.

## Key principle

Multi-opponent action is not:
`Enemy A attacks -> protagonist resets -> Enemy B attacks -> protagonist resets.`

It is:
`Enemy A attack is still resolving -> protagonist displacement opens/closes a lane -> Enemy B begins entry -> protagonist must redirect attention while Enemy A is recovering or re-positioning.`
