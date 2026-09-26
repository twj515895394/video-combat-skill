# Combat QC Gates

Run silently before final output.

## QC-0 Brief Integrity
- Are duration, participant count, weapons, environment, initiator, style/realism level and outcome sufficiently known?
- If a missing core point would materially change choreography, was a concise clarification asked?
- Was already-known information not asked again?
- Were minor inferable details allowed to remain inferred?

## QC-1 Runtime Routing Audit
Before judging choreography, audit the actual Load Manifest.

- Was `routing-contract.md` obeyed?
- Was the Load Manifest built before leaf reads?
- Can every loaded leaf be justified by one concrete user need?
- Did any leaf file trigger a transitive follow-up read? If yes: fail routing.
- Were sibling files avoided unless explicitly selected by a router?
- Were `README.md`, `sources.md`, `reference-schema.md`, `tests/` and `reference-ingestion-pipeline.md` excluded from normal generation?
- Is the task within the correct hard leaf budget?
- Could any loaded file be removed without reducing answer quality? If yes, remove it.

### Overlap / supersession checks
- Named Style Profile selected -> generic `cinematic/hong-kong-action-language.md` normally absent.
- `multi-opponent/protagonist-centric-directing.md` selected -> generic framing file absent unless a special framing problem exists.
- `qinggong.md` loaded only because an actual elevated movement is required, not merely because genre = wuxia.
- Combination loaded only for a specific transition problem, not because every fight needs continuity.
- Atomic file loaded only for one mechanic needing extra detail.
- Core repair file loaded only for an identified failure/edge case.
- `core/action-camera.md` and multiple detailed Directing files are not redundantly loaded by default.

## QC-2 Archetype Integrity
- Was at most one primary archetype selected for a short fight?
- Does it add macro structure beyond the user's brief?
- Do the main kinetic phases belong to that engine?
- Is escalation caused by action/spatial change rather than arbitrary shot variation?

If the user's brief already defines the macro fight engine clearly, it is valid to use no archetype leaf.

## QC-3 Multi-Opponent Scheduling
Only for one-vs-many:
- Was `multi-opponent/multi-opponent-router.md` used?
- Were only 1-2 specialized multi-opponent leaves loaded by default?
- Is the protagonist route defined before enemy attack allocation?
- Are there usually 1 active attacker and at most 2 overlapping immediate threats?
- Are non-active enemies approaching, flanking, blocking, recovering or reentering instead of freezing?
- Is there a spatial reason the whole group cannot attack simultaneously?
- Are target switches visible through head/chest/feet/camera reorientation?

Fail if enemies simply take neutral turns or all rush simultaneously without lane separation.

## QC-4 Multi-Opponent Spatial Continuity
For each relevant enemy:
- location / screen side known?
- lane known?
- state known?
- recovery/displacement known?
- next plausible entry route known?

Verify that displaced/downed enemies remain spatial conditions and do not teleport.

## QC-5 Body State Continuity
For every major beat:
- starting feet known when important?
- initiating limb known?
- motion path known?
- defender response known?
- contact/miss known?
- physical result known?
- exit state supports the next action?
- torso/facing remains plausible?

Fail if a major beat depends on reset or teleportation.

## QC-6 Combat Facing
- Active opponents remain visually aware of the immediate threat.
- No unexplained prolonged back-facing.
- Any pivot/spin has an entrance, temporary rotation and coherent recovery.
- In one-vs-many, protagonist target switching is readable.

## QC-7 Ground / Aerial Logic
- Major jump has a support leg/surface.
- Push-off direction matches trajectory.
- Landing is defined when important.
- No unsupported floating.
- Default one main airborne subject at a time unless a dual-air exchange is explicitly designed.

## QC-8 Zero Idle
- No attack-stop-pose-opponent-turn sequence.
- Misses create landing/overrotation/exposure/distance change.
- Blocks change line/structure.
- Impacts change posture, balance, position or initiative.
- A breathing beat remains physically active rather than resetting the fight.

## QC-9 Style Integrity
- Style is expressed through range, stance, tools and tactical choices, not just labels.
- Mixed-style fighters show different decision logic when that contrast matters.
- Cinematic/directing layers do not erase base style.

## QC-10 Combination Causality
If a Combination leaf was loaded:
- Does the next action exist because the previous state changed?
- Is continuation compatible with current distance and stance?
- If initiative flips, is there a physical reason?

If these answers were already obvious from the Style/archetype, the Combination file may have been unnecessary — re-check QC-1.

## QC-11 Directing Function
If detailed Directing was loaded:
- What is each shot's primary information?
- Does framing prove that information?
- If only one fighter/limb/no face is shown, is spatial context still recoverable?
- Does a detail shot preserve established attack direction?
- Is the shot adding information rather than decorative coverage?

For one-vs-many, camera priority remains protagonist -> current threat -> next threat -> lane/environment.

## QC-12 Impact / Camera / Environment
- Impact approach is established before contact/result.
- Body/material reaction occurs after contact and in the same force direction.
- Camera movement has a target/reason.
- Complex mechanics use simpler camera.
- Props exist before use.
- Damage occurs after contact and persists.
- Environment interaction changes route, lane or recovery rather than becoming a detached prop-show.

## QC-13 Style Profile Translation
If a named profile was loaded:
- only abstract mechanisms were transferred,
- no exact scene/shot-order copy,
- the profile improved staging/rhythm/subject selection instead of replacing choreography,
- generic Hong Kong fallback was not redundantly loaded.

## QC-14 AI Prompt Safety / Stability
When relevant:
- bare hands / gloves / weapons explicitly controlled,
- speed explicitly controlled,
- no unexplained screen-side swap,
- no random synchronized jumping,
- no simultaneous full-group rush unless lanes make it readable,
- no automatic pose reset after impact.

## QC-15 Duration Density
For ~10 seconds:
- roughly 3 main kinetic phases,
- limited readable action nodes,
- no overload of named techniques,
- every 2-3 seconds contains meaningful momentum, threat handoff, information or spatial change.
