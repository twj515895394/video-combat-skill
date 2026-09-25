---
id: fanzi
family: chinese-traditional
aliases: [Fanziquan, 翻子拳, Fanzi]
primary_range: punching-close-mid
secondary_range: pressure
stance_bias: compact-mobile
movement_signature: rapid chained hand strikes, short advancing pressure, alternating hands
primary_tools: [straight/short punches, palm, forearm]
defensive_tools: [short parry, cover, angle step]
grappling_level: low
aerial_level: very-low
ai_generation_risk: medium-high
load_when: user explicitly requests Fanzi / 翻子拳
do_not_load_when: slow heavy single-strike choreography is intended
---

# Fanzi — AI Choreography Model

## Style DNA
- Fast chained hand rhythm.
- Compact advancing pressure.
- Alternating hands should remain connected to stance and torso.
- Speed must not become meaningless hand flutter.

## Action Cards

### FZ-CHAINED-STRAIGHTS
Lead/rear hands alternate on short direct paths while feet advance in small controlled steps.
Each strike has a target line and response.

### FZ-PARRY-TO-CHAIN
Short deflection clears line; next hand attacks immediately without retracting to pose.

### FZ-ADVANCING-HAND-PRESSURE
Lead foot advances, rear foot rebuilds base; hands continue alternating pressure.

## Combination Grammar
- opponent straight -> short parry -> immediate two-hand chain -> angle step.
- first punch draws cover -> second changes level/line -> third only if body state supports it.
- opponent retreats -> compact steps maintain range.

## Tactical Failure Conditions
- extra arms,
- hand blur with no torso/foot relationship,
- both fighters standing still trading rapid punches.

## Camera Proof
Medium shot including hips and hands; avoid extreme close-up for long chains.

## Prompt Vocabulary
rapid alternating short punches, compact advancing steps, immediate parry-to-strike chain, continuous pressure with readable hand paths.
