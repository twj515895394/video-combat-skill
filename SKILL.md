---
name: video-combat-director
description: Design physically continuous fight choreography and cinematic AI-video prompts for boxing, kickboxing, Muay Thai, Sanda, MMA, grappling, Chinese martial arts, wuxia and action cinema. Use when the user asks for fight design, combat choreography, martial-arts action, wuxia combat, cinematic fight-camera design, action prompt generation, or analysis/repair of generated fight footage.
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

5. **Establish each fighter's Combat DNA**
   - base style,
   - effective range,
   - stance / weight bias,
   - primary tools,
   - preferred entry and exit,
   - defensive language.

6. **Select one Combination Pattern only when continuity needs one**

7. **Load Atomic Action detail only when mechanics need extra precision**

8. **Build spatial ledger**
   - screen side,
   - facing direction,
   - distance,
   - feet,
   - balance,
   - height,
   - obstacles.

9. **Choreograph with Zero Idle**
   - previous result -> next starting state.

10. **Assign shot function only after body mechanics are valid**
   - spatial proof,
   - biomechanics proof,
   - threat / POV,
   - impact insert,
   - momentum/result,
   - environment result.

11. **If cinematic shooting matters, route through `references/directing/directing-router.md`**

12. **If a film/director/choreographer reference is requested, load one analytical Style Profile and translate it into abstract visual grammar**

13. **Run QC from `references/qc-gates.md`**

14. **Output the user's requested prompt format**

## Composition model

`BRIEF + FIGHT ARCHETYPE + BASE STYLE(S) + COMBINATION CAUSALITY + OPTIONAL ATOMIC DETAIL + CINEMATIC LAYER + DIRECTING GRAMMAR + OPTIONAL STYLE PROFILE`

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
- fighters keep chest/head/eyes oriented toward the opponent,
- 20-60 degree tactical side-on orientation is allowed,
- back-facing must be caused by a specifically described pivot/spin/impact/evasion and must resolve coherently.

## Zero Idle

Never:
`attack -> stop -> pose -> opponent attacks`

Use:
`attack -> deflection/impact/miss -> altered balance/position -> immediate continuation`

## Film-language rule

The camera does not need to show both fighters, both faces or full bodies in every shot.

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
- eyes snapping toward threat.

Partial/detail shots must inherit a previously understandable spatial relationship.

## Shot-function rule

- Wide/full-body: route, footwork, kicks, throws, qinggong, multiple fighters.
- Medium: attack-defense relationship, bridge/clinch, angle.
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
- no unexplained side swap or teleportation.

## Output principle

Reference material is a mechanics and directing vocabulary, not text to copy verbatim.
Translate selected knowledge into the user's exact fighters, space, duration, desired result and visual intent.
