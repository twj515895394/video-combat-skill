# Combat Reference Schema

Every style/action reference must be written for choreography and AI-video generation, not as a martial-arts encyclopedia.

## Style header

```yaml
id:
family:
aliases:
primary_range:
secondary_range:
stance_bias:
movement_signature:
primary_tools:
defensive_tools:
grappling_level:
aerial_level:
ai_generation_risk:
load_when:
do_not_load_when:
```

## Style reference sections

### 1. Style DNA
Explain the visual/physical identity in 5-10 bullets.

### 2. Range Model
Define where the style wants to operate:
- outside,
- kicking,
- punching,
- trapping,
- clinch,
- takedown,
- ground.

Describe how it enters and exits range.

### 3. Base Stance & Weight
Specify:
- lead/rear relationship,
- torso angle,
- center-of-mass tendency,
- common weight transfer,
- guard geometry.

Avoid claiming one universal stance if the system varies.

### 4. Footwork Vocabulary
Each item should include:
- purpose,
- lead/rear foot order,
- direction,
- exit orientation,
- common AI error.

### 5. Action Cards
Do not store only move names.

Use the following schema when detail is needed:

```yaml
action_id:
name_cn:
name_en:
category:
range:
purpose:
pose_level: P0|P1|P2|P3
starting_state:
key_poses:
  start:
  load_or_chamber:
  peak_or_contact:
  recovery_or_landing:
  exit:
support_base:
weight_distribution:
foot_orientation:
knee_organization:
pelvis_hips:
torso:
shoulder_elbow_hand:
head_gaze:
center_of_mass:
motion_path:
contact_or_miss:
typical_defense:
physical_result:
exit_state:
camera_proof:
ai_failure_modes:
prompt_vocabulary:
```

Not every simple action needs every field explicitly written in prose. P2/P3 techniques should contain enough key-pose detail to prevent broken body geometry.

### 6. Defensive Cards
Use the same physical structure:
incoming line -> defensive start posture -> contact structure -> redirection/absorption -> exit posture -> counter opportunity.

### 7. Combination Grammar
Store **relationship patterns**, not frozen choreography.

Example:
`long straight -> opponent shells -> lead foot gains outside angle -> body attack becomes available`

This lets the director compose new sequences instead of copying a preset combo.

### 8. Tactical Failure Conditions
Explain when the style loses its preferred range or structure.

### 9. Camera Proof
Which framing best proves:
- footwork,
- hip rotation,
- hand fighting,
- clinch,
- throw,
- aerial trajectory,
- contact geometry.

For cinematic combat, identify whether an action is best proven by:
- full-body two-shot,
- single-attacker initiation,
- single-defender reaction,
- contact/detail insert,
- result/recovery shot.

### 10. Tempo Compatibility
Reference should indicate when an action should remain fast in a complete-body shot and what detail may be isolated if readability is needed.

Do not solve technical readability by making two full-body fighters perform slowly unless that slowness is inherent to the physical situation.

### 11. AI Failure Modes
List common generation errors and how to phrase around them.

Examples:
- unexplained back-facing,
- same-side arm duplication,
- feet sliding,
- kick leg changes mid-motion,
- support foot incompatible with hip rotation,
- knee collapse/hyperextension,
- airborne without push-off,
- throw before control/off-balance,
- slow turn-taking in master shot,
- simultaneous unrelated attacks.

### 12. Prompt Vocabulary
Provide precise English biomechanical verbs, but not a finished scene.

## Pose-source discipline

Separate:
- anatomical / biomechanical constraints,
- style-specific technical preference,
- cinematic exaggeration.

Do not claim one exact joint angle or stance is universal across all lineages/rule sets unless the source supports it.
Use conservative mechanically plausible posture when style-specific certainty is unavailable.

## Source discipline

Separate:
- **verified sport/rule boundaries**
- **movement mechanics**
- **cinematic inference**

Rules documents can confirm what a sport permits, but they do not automatically prove one universal technical execution.

Traditional martial arts have school/lineage variation. References must describe a useful choreography model, not claim to be the only authentic expression.

Wuxia references are explicitly cinematic and must not be presented as real competitive technique.
