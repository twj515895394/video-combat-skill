---
name: video-combat-director
description: Design physically continuous fight choreography and cinematic AI-video prompts for boxing, kickboxing, Muay Thai, Sanda, MMA, grappling, Chinese martial arts, wuxia and action cinema. Use when the user asks for fight design, combat choreography, martial-arts action, wuxia combat, cinematic fight-camera design, one-vs-many action, action prompt generation, or analysis/repair of generated fight footage.
---

# Video Combat Director

Design the fight as a physical state machine first, then design the macro fight engine, then design how cinema reveals that action.

## Mandatory execution order

1. **Resolve the brief**
   - duration,
   - participants,
   - armed/unarmed,
   - environment,
   - initiator,
   - combat style(s),
   - realism / wuxia level,
   - desired outcome,
   - target generation format when relevant.
   - If a missing core point would materially change choreography, read `references/brief-confirmation.md` and ask only the minimum necessary clarification.
   - Never re-ask information already supplied.
   - Infer minor details and proceed.

2. **Read `references/reference-router.md`**

3. **Select the smallest useful reference set**
   - Never recursively scan `references/`.

4. **Choose one Fight Scene Archetype when macro structure benefits from it**
   - pressure,
   - counter,
   - pursuit,
   - confined space,
   - vertical terrain,
   - environment-driven,
   - outnumbered,
   - boss escalation,
   - peer duel,
   - wuxia courtyard.

5. **If one protagonist fights 2+ opponents, load the Multi-Opponent layer**
   - read `references/multi-opponent/multi-opponent-router.md`,
   - design protagonist route before enemy attacks,
   - maintain an active-attacker budget,
   - schedule overlapping target handoffs,
   - track recovery and reentry,
   - keep environment funneling explicit.

6. **Establish each fighter's Combat DNA**
   - base style,
   - effective range,
   - stance / weight bias,
   - primary tools,
   - preferred entry and exit,
   - defensive language.

7. **Select one Combination Pattern only when continuity needs one**

8. **Load Atomic Action detail only when mechanics need extra precision**

9. **Build spatial ledger**
   - screen side,
   - facing direction,
   - distance,
   - feet,
   - balance,
   - height,
   - obstacles.
   - For one-vs-many, track every enemy separately: lane, state, distance, recovery and next entry route.

10. **Choreograph with Zero Idle**
   - previous result -> next starting state.

11. **Assign shot function only after body mechanics are valid**
   - spatial proof,
   - biomechanics proof,
   - threat / POV,
   - impact insert,
   - momentum/result,
   - environment result.

12. **If cinematic shooting matters, route through `references/directing/directing-router.md`**

13. **If a film/director/choreographer reference is requested, load one analytical Style Profile and translate it into abstract visual grammar**

14. **Run QC from `references/qc-gates.md`**

15. **Output the user's requested prompt format**

## Composition model

`BRIEF + FIGHT ARCHETYPE + BASE STYLE(S) + OPTIONAL MULTI-OPPONENT SCHEDULING + COMBINATION CAUSALITY + OPTIONAL ATOMIC DETAIL + CINEMATIC LAYER + DIRECTING GRAMMAR + OPTIONAL STYLE PROFILE`

## Brief-confirmation rule

Clarify only high-impact ambiguity.

Ask when missing information changes:
- what systems are fighting,
- whether weapons exist,
- realism vs wuxia vs fantasy,
- participant count,
- who initiates / dominates,
- core environment,
- outcome,
- generation format.

Do not ask for:
- exact costume fabric,
- exact lens,
- minor props,
- exact cut count,
unless the user explicitly wants that production specificity.

One compact clarification message is better than a questionnaire.

If the user says “你自己定 / 直接做”, choose minimal reasonable assumptions and proceed.

## Fight-archetype rule

An archetype defines the macro scene engine, not the techniques.

For ~10 seconds:
- use one primary archetype,
- roughly three kinetic phases,
- one meaningful escalation,
- one readable end-state.

Do not stack multiple archetypes into a short clip.

## One-vs-many hard rules

When one protagonist fights multiple opponents:

### Protagonist is the visual and spatial anchor
The camera, enemy entries and environment are organized around the protagonist's route.

### Attack-right handoff replaces turn-taking
Do not write:
`Enemy A attacks -> reset -> Enemy B attacks.`

Use:
`Enemy A is still resolving -> protagonist movement changes the open lane -> Enemy B begins entering -> target handoff occurs before neutral reset.`

### Active-attacker budget
Default:
- 1 active attacker,
- occasionally 2 overlapping attackers,
- all others approach, flank, block exits, recover, route around obstacles or prepare reentry.

### Non-active enemies still act
They must not freeze. They should have a visible/current state such as approaching, flanking, blocked, recovering or reentering.

### Protagonist route first
Design protagonist movement path before assigning enemy techniques.
Environment should compress lanes so a large group repeatedly becomes local 1v1 / 1v2 pressure.

### Damage persists
The protagonist may get hit, grabbed, lose balance or fail an action.
Enemies may be staggered/displaced without being permanently eliminated.
All such states must affect subsequent movement.

### Reentry is spatially grounded
An enemy can return only from a physically plausible route consistent with prior displacement.

### Partial enemy visibility is valid
The next threat can be represented by:
- a hand at frame edge,
- shoulder behind pillar,
- leg entering foreground,
- half-body in background,
- silhouette in doorway.

Not every enemy needs full-body or face coverage.

### Off-screen sound is tactical information
Approaching footsteps, cloth movement, recovery sounds and obstacle contact can announce the next threat before visual reveal.

## Hard biomechanics rule

For every important action beat:

`Starting State -> Initiating Limb -> Motion Path -> Defensive Response -> Contact/Miss -> Physical Result -> Exit State`

Exit State must establish:
- foot placement,
- torso/facing direction,
- balance,
- distance,
- current momentum,
- environment relationship.

Never allow unexplained reset to stance.

## Combat-facing lock

During active close combat:
- fighters keep chest/head/eyes oriented toward the immediate threat,
- 20-60 degree tactical side-on orientation is allowed,
- back-facing must be caused by a specifically described pivot/spin/impact/evasion and must resolve coherently.

For one-vs-many, target switching must be visible through head, chest, feet or camera reorientation.

## Zero Idle

Never:
`attack -> stop -> pose -> opponent attacks`

Use:
`attack -> deflection/impact/miss -> altered balance/position -> immediate continuation`

## Film-language rule

The camera does not need to show both fighters, every enemy, every face or full bodies in every shot.

A valid action shot may isolate:
- fist approaching lens,
- shin meeting forearm,
- palm compressing chest fabric,
- wrist trap,
- support foot pivot,
- foot planting on pillar,
- shoulder hitting wall,
- wood splintering,
- robe/sleeve wiping frame,
- landing feet,
- eyes snapping toward threat,
- partial incoming enemy at frame edge.

Partial/detail shots must inherit a previously understandable spatial relationship.

## Shot-function rule

- Wide/full-body: route, footwork, kicks, throws, qinggong, multiple attackers.
- Medium: protagonist + current threat + readable next lane.
- Close: contact, grip, guard compression, reaction, foot plant.
- Extreme close: rare decisive detail only.

Complex body mechanics -> simpler camera.
Simple body route -> camera may be more expressive.

## Style-profile rule

Named filmmakers/choreographers may be used internally as analytical references.

Final prompt should translate to abstract mechanisms such as:
- kinetic new-wave Hong Kong wuxia,
- rhythmic widescreen staging,
- prop-driven action geometry,
- grounded full-body martial-arts proof,
- practical weighted stunt action.

Do not copy one exact scene or output only “in the style of [name]”.

## AI-video physical constraints

When appropriate:
- raw 1.0x real-time speed,
- zero slow-motion unless explicitly requested,
- explicit bare hands / no gloves / no weapons when required,
- one main airborne subject at a time by default,
- every jump has support -> push-off -> trajectory -> landing,
- no unsupported floating,
- no unexplained side swap or teleportation,
- no simultaneous full-group rush unless explicitly choreographed with clear lane separation.

## Output principle

Reference material is a mechanics and directing vocabulary, not text to copy verbatim.
Translate selected knowledge into the user's exact fighters, space, duration, desired result and visual intent.
