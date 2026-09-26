# Outnumbered Fight

## Engine
One protagonist manages multiple attackers by controlling movement route, attack lanes, target handoffs and temporary displacement.

The protagonist is the dramatic and visual center.
Enemies create sustained pressure around that center.

## Core one-vs-many rule

Multi-opponent combat is not turn-based:

Bad:
`Enemy A attacks -> protagonist counters -> reset -> Enemy B attacks -> reset.`

Good:
`Enemy A is still resolving/recovering -> Enemy B is already entering -> protagonist movement changes which lane is open -> target handoff occurs before the scene becomes neutral.`

## Active attacker budget

At any instant:
- usually 1 active attacker,
- occasionally 2 overlapping attackers,
- remaining enemies approach, flank, block exits, recover, route around obstacles or prepare reentry.

The feeling should be continuous pressure without simultaneous body chaos.

## Protagonist-first staging

Design order:
1. protagonist route,
2. environment choke points,
3. enemy lanes,
4. attack-right handoffs,
5. recoveries/reentries,
6. techniques,
7. camera.

Do not begin by assigning one combo to every enemy.

## 3-phase structure for ~10 seconds

### Phase 1 — Encirclement pressure / first handoff
- protagonist is already moving or forced to move,
- Enemy A creates first immediate attack,
- Enemy B starts approaching before A fully resolves,
- other enemies occupy visible/supporting lanes.

### Phase 2 — Funnel / route change
- protagonist changes route through pillar, table, doorway, railing, wall or narrow gap,
- geometry temporarily reduces group pressure into local 1v1 or 1v2,
- one enemy becomes blocked/displaced/recovering,
- another gains the next open lane.

### Phase 3 — Renewed overlap / breakout
- a previous attacker may reenter,
- a new active attacker overlaps the tail end of the current exchange,
- protagonist gets clipped, stumbles, redirects or forces a gap,
- scene ends during continuing movement, breakout or renewed pressure rather than a static victory pose.

## Enemy state ledger

Track every opponent separately:
- screen side / approximate location,
- distance to protagonist,
- attack lane,
- current state,
- balance/recovery,
- next possible entry route.

Recommended states:
- ACTIVE_ATTACKER
- SUPPORTING_ATTACKER
- APPROACHING
- FLANKING
- BLOCKING_EXIT
- RECOVERING
- TEMPORARILY_DISPLACED
- DOWN / PHASED_OUT
- REENTERING

## Attack-right handoff

A new attacker often becomes active because:
- protagonist just evaded another attack into that attacker's lane,
- protagonist followed through after hitting one enemy,
- current attacker was redirected into obstacle,
- protagonist's recovery step exposes a side,
- environment blocks one enemy and opens another lane.

Target switching must be visible through head, chest, feet or camera reorientation.

## Spatial funneling

Environment compresses access rather than becoming a prop-show.

Useful:
- pillar prevents two enemies entering shoulder-to-shoulder,
- table forces one attacker around an edge,
- doorway narrows approach,
- crates split attackers into different paths,
- railing/wall protects one side,
- a fallen body temporarily blocks a lane.

The environment rewrites human trajectories.

## Environment interaction

Prefer short body-driven interactions:
- hand catches table for balance,
- shoulder glances pillar,
- back hits doorframe,
- protagonist squeezes through gap,
- enemy collides with wall/furniture,
- foot briefly uses stair/rail as support.

Avoid stopping the fight for long prop demonstrations unless explicitly requested.

## Protagonist failure / damage

The protagonist should not be perfect.

Valid continuity beats:
- gets hit,
- is briefly grabbed,
- attack fails,
- loses balance,
- collides with environment,
- must catch support,
- is forced to abandon one target because a new threat enters.

These states directly create the next action.

## Enemy damage / persistence

Not every enemy must be fully defeated.

Enemies can be:
- staggered,
- pushed away,
- temporarily blocked,
- knocked behind furniture,
- briefly down,
- recovering in background,
then later reenter.

A downed/displaced enemy remains part of spatial continuity.

## Breathing beats

Very short breathing beats are allowed:
- stumble,
- one sharp breath,
- head snap to next threat,
- foot adjustment after impact,
- hand catches wall/table,
- quick spatial read.

They are physical transition beats, not idle resets.

## Directing hierarchy

Camera priority:
1. protagonist,
2. current attacker,
3. next incoming threat,
4. attack lane/environment.

Current attacker must be readable.
Next attacker can appear partially:
- arm at frame edge,
- shoulder behind pillar,
- leg entering foreground,
- half-body in background,
- silhouette in doorway.

Do not force every enemy fully into frame.

## Camera strategy

During complex scheduling:
- medium / medium-wide protagonist-following frame is the safest anchor.

Use closer shots for:
- decisive impact,
- block/check,
- protagonist damage,
- recovery detail.

After a major spatial move, rebuild geography through camera movement or a brief wider frame.

If cutting:
cut by action paragraph / route change / target handoff, not every punch.

## Sound

Use synchronized:
- current hit/miss,
- protagonist footwork and breath,
- approaching enemy footsteps,
- clothing movement from off-screen threats,
- recovering enemy movement,
- environment contact.

Off-screen sound can announce the next threat before full visual reveal.

## Required companion reference

For one-vs-many choreography, read:
`../multi-opponent/multi-opponent-router.md`

Then load only the relevant specialized multi-opponent files.

## Failure modes

- enemies politely wait in neutral stance,
- all enemies attack simultaneously,
- protagonist stands in center and rotates through targets,
- attackers disappear after being hit,
- recovering attacker teleports to a new side,
- every enemy must be knocked out,
- all enemies are always fully framed,
- camera abandons protagonist to show unrelated background action,
- environment interactions become long prop gags,
- protagonist takes damage then instantly resets,
- off-screen threats have no spatially plausible origin.

## AI guidance

For short text-to-video generation:
- 3 attackers is a strong default,
- 4 can work with strong funneling and partial visibility,
- larger groups should be treated as background pressure unless the model/reference setup can support stable identities.
