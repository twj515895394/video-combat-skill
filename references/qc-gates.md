# Combat QC Gates

Run silently before final output.

## QC-0 Routing Integrity
- Did the task go through reference-router?
- Were only necessary style / pairing / combination / action / cinematic / directing / core files selected?
- Was Wuxia used as a cinematic layer rather than replacing base mechanics?
- Were unrelated sibling files excluded?
- Was the reference budget kept minimal?

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
- Cinematic/directing layers do not erase base style.

## QC-6 Combination Causality
- Does action 2 exist because action 1 changed the state?
- Did a miss, block, impact, landing, catch, stumble or positional change create the next opening?
- Is continuation compatible with current distance and stance?
- If initiative flips, is there a physical reason?

Fail if choreography is just technique A + technique B + technique C with no causal bridge.

## QC-7 Directing Function
For every shot:
- What is the primary information?
- Does framing prove that information?
- If only one fighter/one limb/no face is shown, is spatial context still recoverable?
- Is the shot adding new information rather than decorative coverage?
- Does a detail shot preserve the established attack direction?
- Does a POV/attack-to-camera shot clearly belong to one side of the exchange?

## QC-8 Impact Insert Integrity
If using impact close-ups:
- approach was established,
- contact point is readable,
- body/material reaction occurs after contact,
- result inherits the same force direction,
- impact is not shown twice unless explicitly desired.

## QC-9 Camera Motion
- Camera movement has a target and reason.
- Complex mechanics use simpler camera.
- Whip-pan ends on readable subject.
- Landing intercept preserves trajectory.
- No unnecessary orbiting.
- Camera does not cross between fighters without re-establishing space.

## QC-10 Environment Continuity
- Props/obstacles exist before they are used.
- Damage occurs only after contact.
- broken/cracked state persists.
- debris and dust follow inertia.
- environment interaction changes route or provides useful physical feedback.

## QC-11 Style Profile Translation
If a filmmaker/choreographer profile was loaded:
- were only abstract mechanisms transferred?
- did the output avoid copying a specific scene/shot order?
- did the profile improve staging, rhythm or subject selection rather than replace choreography?
- did the final prompt translate the profile into descriptive film language?

## QC-12 AI Prompt Safety
When relevant:
- bare hands / gloves / weapons are explicitly controlled,
- speed is explicitly controlled,
- only one main airborne subject by default,
- no unexplained screen-side swap,
- no extra weapon props,
- no random synchronized jumping.

## QC-13 Duration Density
For ~10 seconds:
- use roughly 3 main kinetic phases,
- prefer a limited number of readable action nodes,
- do not overload with named techniques,
- every 2-3 seconds should contain meaningful momentum transfer, information change or spatial change.
