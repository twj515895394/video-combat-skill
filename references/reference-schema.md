# Combat Reference Schema

Every style reference must be written for choreography and AI-video generation, not as a martial-arts encyclopedia.

## Required header

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

## Required sections

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
Each item must include:
- purpose,
- lead/rear foot order,
- direction,
- exit orientation,
- common AI error.

### 5. Action Cards
Do not store only move names.

Use:

```yaml
action_id:
name_cn:
name_en:
category:
range:
purpose:
starting_state:
mechanics:
contact_or_miss:
typical_defense:
physical_result:
exit_state:
camera_proof:
ai_failure_modes:
prompt_vocabulary:
```

### 6. Defensive Cards
Use the same physical structure:
incoming line -> body/limb response -> redirection/absorption -> new position.

### 7. Combination Grammar
Store **relationship patterns**, not frozen choreography.

Example:
`long straight -> opponent shells -> lead foot gains outside angle -> body attack becomes available`

This lets the director compose new sequences instead of copying a preset combo.

### 8. Tactical Failure Conditions
Explain when the style loses its preferred range or structure.

This is essential for believable style-vs-style choreography.

### 9. Camera Proof
Which framing best proves:
- footwork,
- hip rotation,
- hand fighting,
- clinch,
- throw,
- aerial trajectory.

### 10. AI Failure Modes
List common generation errors and how to phrase around them.

Examples:
- unexplained back-facing,
- same-side arm duplication,
- feet sliding,
- kick leg changes mid-motion,
- airborne without push-off,
- simultaneous unrelated attacks.

### 11. Prompt Vocabulary
Provide precise English biomechanical verbs, but not a finished scene.

## Source discipline

Separate:
- **verified sport/rule boundaries**
- **movement mechanics**
- **cinematic inference**

Rules documents can confirm what a sport permits, but they do not automatically prove one universal technical execution.

Traditional martial arts have school/lineage variation. References must describe a useful choreography model, not claim to be the only authentic expression.

Wuxia references are explicitly cinematic and must not be presented as real competitive technique.
