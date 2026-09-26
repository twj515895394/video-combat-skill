# Combat QC Gates

Run silently before final output.

## QC-0 Brief Integrity
- Are duration, participant count, weapons, environment, initiator, style/realism level and outcome sufficiently known?
- If a missing core point would materially change choreography, was a concise clarification asked?
- Was already-known information not asked again?
- Were minor inferable details allowed to remain inferred?

## QC-1 Routing Integrity
- Did the task go through reference-router?
- Was at most one primary archetype selected for a short fight?
- If one-vs-many, was `multi-opponent/multi-opponent-router.md` loaded?
- Were only necessary style / pairing / combination / action / cinematic / directing / multi-opponent / core files selected?
- Was Wuxia used as a cinematic layer rather than replacing base mechanics?
- Were unrelated sibling files excluded?
- Was the reference budget kept minimal?

## QC-2 Archetype Integrity
- Does the scene have one clear macro engine?
- Do the main kinetic phases belong to that engine?
- Is escalation caused by action/spatial change rather than arbitrary shot variation?
- Did the archetype stay subordinate to user intent?

## QC-3 Multi-Opponent Scheduling
For one-vs-many:
- Is the protagonist the route and visual anchor?
- Is the protagonist movement path defined before enemy attack allocation?
- Are there usually only 1 active attacker and at most 2 overlapping active attackers?
- Does the next attacker begin entering before the current threat fully resolves when appropriate?
- Are non-active enemies doing something meaningful: approaching, flanking, blocking, recovering, routing around obstacles, or reentering?
- Is there a physical/spatial reason why all enemies cannot attack simultaneously?
- Are target switches visible through head/chest/feet/camera reorientation?

Fail if enemies simply take turns from neutral poses or all rush simultaneously without lane separation.

## QC-4 Multi-Opponent Spatial Continuity
For each enemy:
- location / screen side known?
- current lane known?
- current state known?
- recovery/displacement known?
- next plausible entry route known?

Also verify:
- environment funnels attackers rather than decorating the set,
- fallen/displaced enemies remain spatial conditions,
- recovering enemies do not teleport,
- blocked attackers route around actual obstacles.

## QC-5 Body State Continuity
For every major beat:
- starting feet known?
- initiating limb known?
- motion path known?
- defender response known?
- contact/miss known?
- physical result known?
- exit feet known?
- torso facing known?
- next action can physically start from that state?

Fail if any important beat depends on reset or teleportation.

## QC-6 Combat Facing
- Active opponents remain visually aware of the immediate threat.
- No unexplained prolonged back-facing.
- Any pivot/spin has entrance, temporary back phase and recovery.
- In one-vs-many, protagonist target switching is readable.

## QC-7 Ground Contact
- Major jump has support leg.
- Push-off direction matches trajectory.
- Landing foot is specified when important.
- Feet do not slide independently of body weight.
- No unsupported aerial motion.

## QC-8 Zero Idle
- No attack-stop-pose-opponent-turn sequence.
- Misses create overrotation, landing, exposed line or distance change.
- Blocks change line or structure rather than zeroing force.
- Impact changes balance, posture, position or initiative.
- A breathing beat remains physically active: stumble, breath, glance, support catch or threat recognition.

## QC-9 Style Integrity
- Style is expressed through range, stance, tools and tactical choices, not just labels.
- Mixed-style fighters have visibly different decision logic.
- Cinematic/directing layers do not erase base style.

## QC-10 Combination Causality
- Does action 2 exist because action 1 changed the state?
- Is continuation compatible with current distance and stance?
- If initiative flips, is there a physical reason?

## QC-11 Directing Function
- What is each shot's primary information?
- Does framing prove that information?
- If only one fighter/limb/no face is shown, is spatial context still recoverable?
- In one-vs-many, does camera priority remain protagonist -> current attacker -> next threat -> lane/environment?
- Can supporting enemies appear partially instead of being forced into full group coverage?
- Is the shot adding new information rather than decorative coverage?
- Does a detail shot preserve attack direction?

## QC-12 Multi-Opponent Reentry & Sound
- Are displaced enemies allowed to recover/reenter instead of disappearing?
- Does every reentry follow a plausible route?
- Do protagonist hits/failures persist into the next beat?
- Can off-screen footsteps/cloth/recovery sounds announce the next threat from a plausible direction?
- Are sound cues synchronized to contact, movement and environment interaction?

## QC-13 Impact Insert Integrity
If using impact close-ups:
- approach was established,
- contact point is readable,
- body/material reaction occurs after contact,
- result inherits the same force direction.

## QC-14 Camera Motion
- Camera movement has a target and reason.
- Complex mechanics use simpler camera.
- Whip-pan ends on readable subject.
- Landing intercept preserves trajectory.
- No unnecessary orbiting.
- In one-vs-many, camera does not abandon protagonist to follow unrelated background action.

## QC-15 Environment Continuity
- Props/obstacles exist before they are used.
- Damage occurs only after contact.
- broken/cracked state persists.
- debris and dust follow inertia.
- environment interaction changes attack lanes, route or recovery rather than becoming a prop-show detour.

## QC-16 Style Profile Translation
- only abstract mechanisms transferred,
- no exact scene/shot-order copy,
- profile improves staging/rhythm/subject selection rather than replacing choreography.

## QC-17 AI Prompt Safety
When relevant:
- bare hands / gloves / weapons explicitly controlled,
- speed explicitly controlled,
- only one main airborne subject by default,
- no unexplained screen-side swap,
- no extra weapon props,
- no random synchronized jumping,
- no simultaneous full-group rush unless explicitly designed with readable lanes.

## QC-18 Duration Density
For ~10 seconds:
- roughly 3 main kinetic phases,
- limited readable action nodes,
- no overload of named techniques,
- every 2-3 seconds contains meaningful momentum, threat handoff, information or spatial change.
