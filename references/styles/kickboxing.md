---
id: kickboxing
family: striking
aliases: [kickboxing, 踢拳, low kick]
primary_range: punching-kicking
secondary_range: pocket
stance_bias: balanced striking stance
movement_signature: punch-kick chaining, low-kick range control, compact resets
primary_tools: [straight punches, hooks, round kick, low kick, front kick]
defensive_tools: [high guard, parry, shin check, step-back, angle exit]
grappling_level: minimal
aerial_level: low
ai_generation_risk: medium
load_when: mixed punch-kick sport striking
do_not_load_when: prolonged clinch elbows/throws are central
---

# Kickboxing

## Style DNA
- Punches and kicks belong to one continuous range-management system.
- Kicks often begin/end in positions that feed hand combinations.
- Low kicks change stance stability and movement.
- More squared/balanced than pure boxing when kick defense must remain available.

## Range Model
Outside: front kick / round kick.
Mid: straight punches into kick.
Pocket: short punches; exit before prolonged grappling.

## Action Cards

### KB-LOW-KICK
Start: support leg stable, opponent's lead/rear thigh exposed.
Mechanics: support foot turns, hip swings, shin travels in an arc.
Result: receiver shifts weight, checks, withdraws leg or loses stance quality.
Exit: kicking leg retracts or lands deliberately.
AI error: kicking leg changes sides mid-swing.

### KB-ROUND-KICK
Mechanics: support foot pivots, hip turns through, shin/instep crosses target line.
Defense: forearm frame, step-back, shin check depending height.
Exit must name whether leg retracts or lands forward.

### KB-SHIN-CHECK
Mechanics: defender raises one knee while standing on opposite leg; shin turns toward incoming low kick.
Result: both fighters experience brief impact, then defender must replant foot.
Do not freeze in one-leg pose.

### KB-1-2-LOW
Grammar: lead straight occupies guard -> rear straight shifts guard backward -> rear/lead low kick attacks leg as hands recover.

### KB-FRONT-KICK
Purpose: interrupt forward pressure and restore space.
Result: receiver's torso or step line is displaced; kicker regains kicking distance.

## Tactical Failure Conditions
- leg is caught if choreography crosses into Sanda/MMA,
- prolonged clinch removes clean kickboxing rhythm,
- overcommitted kick creates landing vulnerability.

## Camera Proof
Full-body or knees-to-head for kick support leg. Impact insert can follow, not replace, the readable kick path.

## Prompt Vocabulary
support-foot pivot, shin arc, lead-leg check, rear round kick, short punch-to-kick transition, front kick restoring distance.
