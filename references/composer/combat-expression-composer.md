# Combat Expression / Gaze Composer Protocol

This protocol controls facial expression, gaze and breathing when a fighter's face is visually readable.

Purpose: prevent cinematic fight shots from showing blank, beauty-pose or emotionally disconnected faces during active combat.

This is not an acting-style library. Expression must follow the fighter's current physical and tactical state.

## 1. Core rule — Face Visibility -> Expression Obligation

If the face is clearly readable in a medium-close, close-up or extreme close-up shot, the expression must communicate the current combat state.

If the face is tiny, motion-blurred, obscured or not important to the shot, do not waste prompt budget describing facial detail.

Do not force facial close-ups merely to show expression.

## 2. Default combat focus

The default face during active combat is **focused and threat-aware**, not neutral and not permanently enraged.

Useful cues:
- eyes locked on opponent / incoming threat,
- slight brow tension,
- jaw set or lips lightly parted for controlled breathing,
- facial muscles alert rather than relaxed,
- head angle follows the opponent / attack line,
- no vacant stare into space,
- no casual smile or beauty-model expression.

## 3. Expression states by action state

### F0 — Tactical focus
Use during tracking, spacing, guard, waiting for an opening.

Show:
- concentrated eyes,
- restrained brow tension,
- controlled breathing,
- jaw relaxed enough to move but not slack.

### F1 — Attack commitment / exertion
Use during a committed strike, throw, hard push-off or explosive entry.

Possible cues:
- eyes remain on target,
- brow tightens briefly,
- jaw / cheek / neck tension increases,
- lips part on a short exhale,
- expression peaks only around the effort phase.

Do not hold a frozen snarl through the whole fight.

### F2 — Immediate threat / evade
Use when a strike passes close to face/head or the fighter rapidly changes line.

Possible cues:
- eyes snap toward the incoming limb,
- brief squint / blink if a limb passes extremely close,
- brow tightens,
- mouth/jaw stays controlled,
- head movement and gaze remain causally linked.

Avoid exaggerated fear unless story demands it.

### F3 — Impact reaction
Use when the face is visible during or immediately after a meaningful hit.

Reaction begins **after visible contact**, not before.

Possible cues depend on impact:
- sharp blink / squint,
- jaw opens or clamps briefly,
- breath is knocked out,
- cheek / neck / brow tension changes,
- eyes momentarily lose perfect lock then reacquire opponent.

Do not use the same reaction for every hit.

### F4 — Recovery / reacquisition
Use after stumble, landing, wall catch, failed attack or heavy defense.

Show:
- quick breath recovery,
- eyes reacquire opponent,
- jaw resets,
- focus returns before the next action.

Recovery is brief; do not turn it into a pose.

### F5 — Control / dominance
Use during successful wrist control, pin, clinch advantage or clear tactical upper hand.

Show:
- calm concentration,
- eyes tracking the controlled limb / opponent,
- restrained confidence if appropriate,
- no unnecessary grin unless character/story explicitly calls for it.

## 4. Expression continuity

Expression must inherit the physical state across cuts.

Examples:
- near-miss close-up -> eyes stay on the passing limb / opponent in the next shot,
- rib impact -> breath disruption / facial tension persists briefly into recovery,
- wall collision -> dazed micro-reaction may persist until gaze reacquires threat,
- attack exertion -> face relaxes only after the effort phase ends.

Do not reset the face to neutral at every cut.

## 5. Gaze is part of combat-facing

When face is visible, gaze should usually track:
- opponent's head / torso,
- incoming limb if it becomes the immediate threat,
- controlled wrist / arm during grappling detail,
- landing / environment contact only when mechanically necessary.

Avoid:
- staring into camera without POV motivation,
- eyes looking away from the active threat,
- frozen gaze while head/body turns elsewhere.

## 6. Breathing as acting detail

Breathing can sell effort without exaggerated acting.

Use sparingly:
- short exhale on committed strike,
- breath interruption after torso impact,
- visible inhale/exhale during brief recovery,
- controlled heavy breathing after sustained exchange.

Do not make every strike accompanied by a scream.

## 7. Shot-size rules

### Wide / full-body
Expression usually not worth describing unless face remains unusually readable.
Prioritize body mechanics and space.

### Medium / medium-close
Use simple combat-focus cues when face is visible.

### Close-up
Expression should be state-specific and dynamic.
Use close-up for:
- threat recognition,
- attack commitment,
- impact reaction,
- recovery/reacquisition,
- control tension.

### Extreme close-up
Use rarely.
Eyes / jaw / breath / micro-reaction should reveal one decisive piece of information.

## 8. Avoid overacting

Reject:
- blank mannequin face during active danger,
- permanent angry snarl,
- constant screaming,
- beauty-model calm while being hit,
- smiling during neutral combat unless character-specific,
- identical grimace after every impact,
- exaggerated fear that contradicts fighter skill / story,
- facial reaction before physical contact,
- head/gaze disconnected from opponent direction.

## 9. AI prompt compression

Do not write a paragraph of facial acting for every shot.

Use compact state phrases when enough:
- `focused eyes locked on the opponent, jaw set, controlled breathing`,
- `brief exertion grimace at impact, short exhale`,
- `eyes snap to the incoming kick, brow tightens`,
- `impact knocks the breath out; eyes briefly squint then reacquire`,
- `calm focused control, gaze fixed on the trapped wrist and opponent`.

Expression is secondary to body mechanics unless the shot explicitly makes the face the information target.
