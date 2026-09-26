# Tempo + Shot Grammar Composer Protocol

This protocol controls how fight tempo is expressed through cinematography.

Purpose: prevent AI fight videos from becoming slow turn-taking two-shots where both fighters remain fully visible and trade one move at a time.

The compact mandatory rules live in `SKILL.md`. Load this detailed file only when cinematic pacing, shot variety, turn-taking failure, or stand-and-trade staging is a central problem.

## 1. Core principle

**Slow the observation, not the fight.**

When both fighters are fully visible and performing complete attack-defense movement, choreography should remain fast, overlapping and continuous.

If the audience needs more time to read one important event, change the shot:
- cut closer,
- isolate the striking limb,
- isolate the receiving point,
- isolate the support foot,
- isolate the defender reaction,
- isolate the environment result.

Do not solve readability by making two fully visible fighters perform slow, turn-based techniques.

## 2. Two-fighter full-body tempo rule

When both fighters are substantially visible in a wide / medium-wide / full-body two-shot:

- keep real-time body speed,
- favor chained attack-defense-counter movement,
- avoid pose resets,
- avoid one fighter waiting while the other completes a full technique,
- let the next threat begin from the physical result of the prior beat,
- use the shot to prove spatial route, footwork and continuous exchange.

A two-shot should normally contain **movement continuity**, not instructional demonstration.

Bad:
`A punches -> stops -> B blocks -> stops -> B punches -> A blocks -> both reset.`

Better:
`A drives the straight -> B's forearm collision redirects it -> the redirect already loads B's counter -> A's recovery foot becomes the next evasive step.`

## 3. Detail-shot emphasis rule

If one beat should feel slower, heavier or more readable, use a tighter shot instead of slowing the whole duel.

Suitable subjects:
- fist entering chest,
- palm heel compressing robe fabric,
- forearm colliding with shin,
- wrist control changing line,
- support foot pivot,
- boot skid,
- foot plant on pillar,
- shoulder hitting wall,
- ribs folding under impact,
- railing flexing,
- eyes acquiring the incoming threat.

The detail shot may momentarily simplify perceived time because the frame contains less information, while the action itself remains real-time unless explicit slow motion is requested.

## 4. Subject isolation is encouraged

Not every shot should show both fighters.

Valid fight shots include:

### Attacker-only initiation
Show one fighter launching the attack.
The opponent may be:
- off-screen,
- foreground shoulder blur,
- partial arm/leg at frame edge,
- hidden behind architecture.

### Defender-only response
Show:
- parry,
- slip,
- recoil,
- foot recovery,
- wall catch,
- landing,
without requiring the attacker fully visible.

### Contact-only shot
Show only:
- attacking limb,
- receiving surface,
- local body/material response.

### Result-only shot
Show:
- receiver stumbling,
- boot sliding,
- body hitting pillar,
- hand catching railing,
- debris falling,
while attacker is partly or fully out of frame.

The absent fighter must remain spatially inferable from established direction.

## 5. Attack-right overlap

Cinematic continuity should avoid strict alternating turns.

The next attack may begin while the previous action is resolving, provided body mechanics permit it.

Useful overlap patterns:
- parry becomes counter before the attacker's arm fully retracts,
- missed kick lands forward and immediately becomes hand range,
- defender retreats from impact while attacker follows the recovery step,
- blocker redirects a limb while the opposite hand is already entering the opened line,
- receiver catches balance on wall/rail while launching a short counter from that support.

This creates speed without requiring impossible simultaneous unrelated motion.

## 6. Shot-role sequence

A cinematic exchange can move through roles such as:

`SPATIAL ANCHOR -> ATTACK INITIATION -> CONTACT DETAIL -> RESULT / RECOVERY -> RE-ESTABLISH`

But this is not a mandatory five-shot recipe.
Skip roles that add no information.

The important rule is that each new shot shows **new information**.

## 7. Tempo by framing

### Wide / full-body two-shot
Primary use:
- route,
- style contrast,
- kicks,
- throws,
- footwork,
- rapid continuous exchange.

Tempo expectation:
**fast / continuous**.

### Medium two-subject shot
Primary use:
- close pressure,
- hand fighting,
- bridge/clinch,
- short combination.

Tempo expectation:
**fast to very fast**, unless a structural bind/grapple creates real resistance.

### Single-subject medium / close
Primary use:
- attack initiation,
- reaction,
- recovery,
- pursuit,
- environment interaction.

Tempo expectation:
may briefly hold attention on one action phase without making the whole fight slow.

### Contact close-up / extreme close-up
Primary use:
- impact,
- grip,
- foot plant,
- local material/body deformation.

Tempo expectation:
perceptually emphasized; actual slow motion only if explicitly requested.

## 8. Real slow motion

Default: **no slow motion**.

If slow motion is explicitly requested, prefer using it for:
- one decisive contact,
- one foot plant / push-off,
- one near-miss,
- one environment break,
- one receiving-body reaction.

Avoid slowing an entire wide two-person exchange unless the user explicitly wants stylized slow-motion choreography.

## 9. Cut on action

Good cut points:
- fist crossing foreground,
- kick near lens,
- sleeve wipe,
- forearm collision,
- foot landing,
- shoulder hitting pillar,
- body passing behind column,
- defender dropping below attack line.

The next shot inherits:
- direction,
- body phase,
- support foot,
- momentum,
- opponent relation.

## 10. No static master-shot dependency

A master wide shot is an anchor, not the entire scene.

Reject a sequence where:
- both fighters remain fully visible for most/all of the clip,
- camera remains frontally perpendicular to both fighters,
- attacks alternate cleanly one by one,
- every action returns to neutral spacing,
- the only cinematic variation is zooming the same two-shot.

## 11. Camera motion and tempo

Use camera movement to follow dominant displacement, not to create fake speed.

- lateral track: moving exchange,
- short backward retreat: pressure toward lens,
- whip-pan: sudden attack/escape direction change,
- landing intercept: airborne/throw/fall destination,
- low follow: footwork/sweep,
- static frame: complex impact/throw where body motion supplies energy.

Complex body action -> simpler camera.
Simple trajectory -> more expressive camera allowed.

## 12. AI-video prompt wording

Prefer concrete shot-language such as:
- `the camera stays low on the support foot as the heel pivots`,
- `cut tight to the forearm-shin collision`,
- `the attacker fills most of frame while the defender is only a shoulder edge`,
- `cut to the receiver's boot skidding across stone`,
- `return to a wide two-shot only after the spatial relationship changes`.

Avoid vague:
- `cinematic camera`,
- `dynamic angles`,
- `fast editing`,
without specifying what information each shot reveals.

## 13. QC failure modes

Reject / repair:
- slow turn-taking in full-body two-shot,
- both fighters waiting for each other,
- whole fight shown from one static master angle,
- every shot containing both faces and full bodies,
- close-up with no established spatial relation,
- fake slow motion caused by under-choreographed movement,
- cutting to a new angle but repeating the same information,
- detail shot that breaks attack direction,
- attacker disappearing spatially after a defender-only reaction shot,
- high-speed camera orbit used to compensate for slow body choreography.

## 14. Asymmetric Shot Duration

Do **not** divide a 10-second fight into equal-length shots by default.

Shot duration follows the information task, not a metronome.

A valid short fight may contain:
- one 2.5-4 second continuous high-speed exchange,
- one 0.3-0.8 second impact/result insert,
- one 1-2 second displacement / throw / environment event,
- several very short 0.2-0.6 second detail or reaction shots near escalation.

A long shot can be the **fastest** part of the fight if body action is dense and continuous.
A short shot can feel slower/perceptually heavier because it isolates one detail.

Reject:
- every shot receiving equal time regardless of information,
- cutting every second only because the clip is 10 seconds,
- shortening a coherent long exchange merely to create fake cinematic variety.

## 15. Information-Driven Cutting

Cut when the audience's information requirement changes.

Useful information changes:
- spatial relationship -> immediate threat,
- threat -> exact contact,
- contact -> receiving-body result,
- footwork route -> hand/limb detail,
- grounded exchange -> vertical displacement,
- body action -> environment consequence,
- one fighter's initiative -> the other's recovery/counter initiation.

Do not cut merely because:
- one technique ended,
- a fixed duration elapsed,
- every strike “needs its own shot.”

Internal question before every cut:
**What new information does the next shot reveal that the current shot cannot reveal as clearly?**

If the answer is “none,” keep the current shot.

## 16. Long-Take Density Rule

A continuous 2-4 second shot should not become slow just because it is long.

For a long action shot:
- attacks can enter from frame edges / foreground,
- the defender can remain the stable readable subject while threats change,
- movement may progress through several attack-defense nodes without neutral reset,
- one fighter may be only partially visible for portions of the shot,
- body movement supplies tempo; camera may remain relatively stable.

Long take does **not** require:
- both full bodies always visible,
- symmetrical staging,
- slower technique execution,
- one move per beat.

This is especially useful for:
- kick barrages,
- continuous close defense,
- pursuit exchanges,
- Taijiquan/Baguazhang-style redirection chains,
- one-vs-many active-attacker handoffs.
