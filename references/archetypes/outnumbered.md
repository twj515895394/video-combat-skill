# Outnumbered Fight

## Engine
One protagonist manages multiple attackers by controlling route, attack lanes, target handoffs and temporary displacement.

The protagonist is the dramatic/spatial center. Enemies create sustained pressure around that center.

## Macro rule
One-vs-many is not several independent 1v1 rounds.

Use overlapping threat handoff:
`current attack still resolving -> protagonist displacement changes the open lane -> next threat enters -> target switches before neutral reset`

## Default active pressure
At any instant:
- usually 1 immediate active attacker,
- occasionally 2 overlapping immediate threats,
- the remaining enemies stay spatially meaningful without all performing full attacks.

## Route-first design
Before individual techniques, define:
1. protagonist route,
2. environment choke points,
3. enemy approach lanes,
4. where pressure changes target,
5. the desired breakout / renewed-pressure end state.

Detailed scheduling, funneling, camera and reentry behavior are handled by the Multi-Opponent module selected by the root router.

## 3-phase structure for ~10 seconds

### Phase 1 — Encirclement pressure
The first attacker creates immediate danger while at least one additional threat is already approaching or positioning.

### Phase 2 — Route / lane change
The protagonist moves through geometry or displacement changes which enemies have access. Group pressure compresses into local 1v1 / 1v2.

### Phase 3 — Renewed overlap / breakout
A new or returning threat overlaps the tail of the current exchange. The scene ends during movement, breakout, damage recovery or renewed pressure rather than a static victory pose.

## Enemy state summary
Track each opponent with one current role/state such as:
- ACTIVE_ATTACKER
- SUPPORTING_ATTACKER
- APPROACHING
- FLANKING
- BLOCKING_EXIT
- RECOVERING
- TEMPORARILY_DISPLACED
- DOWN / PHASED_OUT
- REENTERING

## Environment principle
Environment exists mainly to rewrite access:
- narrow a lane,
- block one side,
- force detour,
- provide brief support,
- create collision,
- turn nominal 1-vs-many into local 1v1 / 1v2.

Do not turn the scene into a prop demonstration unless explicitly requested.

## Damage / persistence
The protagonist may get hit, grabbed, lose balance or fail an action.
Enemies may be staggered/displaced without being permanently removed.
These states must affect later movement.

## Directing principle
Camera priority remains:
1. protagonist,
2. current immediate threat,
3. next incoming threat,
4. lane / environment.

Not every enemy needs full-body or face coverage.

## Failure modes
- enemies politely wait in neutral poses,
- all enemies launch full attacks simultaneously,
- protagonist stands in the center and merely rotates through targets,
- displaced enemies vanish or teleport on reentry,
- every enemy is forced into the frame at once,
- environment interactions do not alter access or movement.

## Runtime note
This is an archetype leaf, not a router.
Do not follow any other reference because this file mentions a concept. The root router and `multi-opponent/multi-opponent-router.md` determine the actual specialized load set.
