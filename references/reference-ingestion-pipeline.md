# Reference Ingestion Pipeline

Use only when the user asks to learn from a source, expand the library, or determine whether a new reference contains reusable combat knowledge.

## Goal

Convert raw martial-arts / fight-film material into reusable choreography knowledge without turning the repository into an unstructured archive.

## Source classes

### Tier A — Official rule / federation material
Use for:
- discipline boundaries,
- legal/illegal technique categories,
- competition terminology,
- event definitions.

Examples: IWUF, World Boxing, WAKO, IMMAF, UWW, IJF, WT, IBJJF, FIAS.

Do not infer one universal technical execution from rules alone.

### Tier B — Coaching / technical instruction
Use for:
- stance,
- footwork,
- limb path,
- common defense,
- combination mechanics.

### Tier C — Fight / sparring / demonstration footage
Use for:
- observed movement patterns,
- transition logic,
- realistic timing,
- range changes,
- failure/recovery states.

### Tier D — Film / stunt / wuxia references
Use for:
- camera grammar,
- action rhythm,
- environment interaction,
- cinematic exaggeration,
- qinggong/wire-like spatial design,
- multi-opponent scheduling and blocking.

Never silently merge Tier D into real martial-art technique files.

## Classification before writing

Every candidate must be classified into exactly one primary target:

1. **STYLE** — changes a style's tactical identity, preferred range, or style-specific combination grammar.
2. **ATOMIC ACTION** — reusable biomechanical primitive across styles.
3. **COMBINATION** — reusable causal chain connecting states across multiple actions.
4. **ARCHETYPE** — reusable macro fight-scene engine such as pressure, pursuit, confined-space or outnumbered structure.
5. **MULTI-OPPONENT** — reusable one-vs-many scheduling, funneling, reentry, state-ledger or protagonist-centric directing logic.
6. **DIRECTING** — reusable shot, framing, camera, editing, impact-insert or environment-photography mechanism.
7. **STYLE PROFILE** — reusable analytical action-cinema grammar distilled from multiple works/sources; never one exact scene copy.
8. **CINEMATIC** — stunt/world transformation such as grounded wuxia or qinggong.
9. **PAIRING** — style-vs-style interaction pattern.
10. **CORE** — universal physical or AI-generation constraint.

## ARCHETYPE vs MULTI-OPPONENT vs COMBINATION vs DIRECTING

Use ARCHETYPE when the reusable knowledge answers:
- what drives the whole fight,
- who owns macro initiative,
- how the scene escalates across phases,
- how space is used across the sequence.

Use MULTI-OPPONENT when the reusable knowledge specifically answers:
- how many attackers are active at once,
- how attack-right handoffs overlap,
- how supporting enemies approach/flank/recover,
- how protagonist route compresses attack lanes,
- how displaced enemies reenter,
- how camera/sound preserve crowd pressure around one protagonist.

Use COMBINATION when the knowledge explains a local causal action chain between techniques.

Use DIRECTING when it explains how the audience sees a shot or cut independent of the number of attackers.

## STYLE vs COMBINATION vs DIRECTING

Use DIRECTING when the reusable asset answers:
- what should the camera show,
- which subject/body part is framed,
- how camera moves,
- where a cut is motivated,
- how impact/environment result is photographed.

Use STYLE PROFILE when:
- the value comes from a recurring body of film/choreography language,
- multiple sources/works support the abstraction,
- the result can be translated into general mechanisms.

Do not store a single exact movie shot sequence as a Style Profile.

Use STYLE when:
- the pattern is characteristic of one style's tactical identity.

Use COMBINATION when:
- the pattern is reusable across multiple styles,
- the value lies in state transition rather than the named technique.

## Candidate decision

### ADD
A genuinely new reusable mechanic or routing concept.

### MERGE
Same underlying mechanic exists but source adds useful detail, failure mode or camera proof.

### EXISTING
Already represented adequately.

### HOLD
Potentially useful but insufficiently clear or too source-specific.

### REJECT
Contradictory, non-reusable, purely decorative, unsupported, or would pollute category boundaries.

## Deduplication rule

Deduplicate atomic actions by mechanics and exit state, not technique name.

Deduplicate combinations by:
- trigger state,
- changed state,
- continuation opportunity,
- tactical purpose.

Deduplicate multi-opponent assets by:
- active-attacker scheduling pattern,
- lane/funnel logic,
- state transition,
- reentry mechanism,
- protagonist/camera relationship.

## Extraction template — reusable action

```yaml
candidate_name:
source_class:
source_context:
target_type:
target_file:
action_id:
aliases:
purpose:
range:
starting_state:
support:
initiating_limb:
motion_path:
defender_response:
contact_or_miss:
physical_result:
exit_state:
camera_proof:
ai_failure_modes:
style_constraints:
confidence:
decision: ADD|MERGE|EXISTING|HOLD|REJECT
```

## Extraction template — reusable multi-opponent asset

```yaml
candidate_name:
source_class:
target_type: MULTI-OPPONENT
target_file:
protagonist_route:
active_attacker_budget:
current_attacker_state:
next_attacker_entry:
supporting_enemy_states:
attack_lane_logic:
environment_funnel:
displacement_and_reentry:
camera_priority:
offscreen_sound_cues:
ai_failure_modes:
confidence:
decision: ADD|MERGE|EXISTING|HOLD|REJECT
```

## Extraction template — reusable directing asset

```yaml
candidate_name:
source_class:
target_type: DIRECTING
target_file:
shot_purpose:
subject_selection:
framing:
camera_position:
camera_movement:
action_trigger:
continuity_requirements:
best_use:
ai_failure_modes:
confidence:
decision: ADD|MERGE|EXISTING|HOLD|REJECT
```

## Extraction template — reusable combination

```yaml
candidate_name:
source_class:
target_type: COMBINATION
target_file:
trigger_state:
first_action:
defender_response:
changed_state:
continuation_opportunity:
compatible_style_families:
incompatible_conditions:
camera_proof:
ai_failure_modes:
confidence:
decision: ADD|MERGE|EXISTING|HOLD|REJECT
```

## Traditional martial-arts policy

Do not claim:
- one school equals the entire style,
- one demonstration is universal,
- film choreography is historical technique.

Use wording such as:
- choreography model,
- common visual/mechanical pattern,
- one useful representation,
- school variation exists.

## Video ingestion

When the user supplies fight footage:
1. identify actual visible body mechanics,
2. ignore move names unless independently known,
3. segment into action beats,
4. extract support/trajectory/contact/exit,
5. separately extract causal transitions between beats,
6. if 1-vs-many, extract active-attacker states, protagonist route, funnel geometry, target handoffs and reentry,
7. identify camera-specific effects separately,
8. route each candidate,
9. dedupe only against the exact target file,
10. write approved ADD/MERGE items.

Never scan the entire reference tree for every candidate.

## Quality gate

Before writing:
- mechanic is physically describable,
- target category is correct,
- base style and cinematic layer are not conflated,
- atomic action and combination causality are not duplicated,
- multi-opponent scheduling is not misfiled as a martial-art technique,
- action has an exit state,
- combination has trigger -> changed state -> continuation,
- multi-opponent asset has protagonist route + enemy states + attack-lane logic,
- wording is AI-video usable,
- duplicate check is target-local,
- source confidence is recorded when uncertain.
