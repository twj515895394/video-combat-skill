# Combat QC Gates

Run silently before final output.

## QC-0 Routing Integrity
- Did the task go through reference-router?
- Were only necessary style/cinematic/core files selected?
- Was Wuxia used as a cinematic layer rather than replacing base mechanics?
- Were unrelated sibling styles excluded?

## QC-1 Body State Continuity
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

## QC-2 Combat Facing
- Active opponents remain visually aware of each other.
- No unexplained prolonged back-facing.
- Any pivot/spin has entrance, temporary back phase and recovery.
- No vague "moves behind" without path.

## QC-3 Ground Contact
- Major jump has support leg.
- Push-off direction matches trajectory.
- Landing foot is specified when important.
- Feet do not slide independently of body weight.
- No unsupported aerial motion.

## QC-4 Zero Idle
- No attack-stop-pose-opponent-turn sequence.
- Misses create overrotation, landing, exposed line or distance change.
- Blocks change line or structure rather than zeroing force.
- Impact changes balance, posture, position or initiative.

## QC-5 Style Integrity
- Style is expressed through range, stance, tools and tactical choices, not just labels.
- Mixed-style fighters have visibly different decision logic.
- Cinematic layer does not erase base style.

## QC-6 Camera Readability
- Camera has a purpose.
- Body-complex moment uses readable framing.
- Impact point is not hidden.
- Major footwork can be understood.
- Not every shot is forced to show faces.
- Not every shot is forced to show both fighters.
- No unnecessary orbiting during complex choreography.

## QC-7 AI Prompt Safety
When relevant:
- bare hands / gloves / weapons are explicitly controlled,
- speed is explicitly controlled,
- only one main airborne subject by default,
- no unexplained screen-side swap,
- no extra weapon props,
- no random synchronized jumping.

## QC-8 Duration Density
For ~10 seconds:
- use roughly 3 main kinetic phases,
- prefer a limited number of readable action nodes,
- do not overload with named techniques,
- every 2-3 seconds should contain a meaningful momentum transfer or spatial change.
