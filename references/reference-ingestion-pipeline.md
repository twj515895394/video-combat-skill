# Reference Ingestion Pipeline

Use only when the user asks to learn from a source, expand the library, or determine whether a new reference contains reusable combat knowledge.

## Goal

Convert raw martial-arts material into reusable choreography knowledge without turning the repository into an unstructured archive.

## Source classes

### Tier A — Official rule / federation material
Use for:
- discipline boundaries,
- legal/illegal technique categories,
- competition terminology,
- event definitions.

Examples: IWUF, World Boxing, WAKO, IMMAF, UWW.

Do not infer one universal technical execution from rules alone.

### Tier B — Coaching / technical instruction
Use for:
- stance,
- footwork,
- limb path,
- common defense,
- combination mechanics.

Prefer reputable coaching or federation instructional material when available.

### Tier C — Fight / sparring / demonstration footage
Use for:
- observed movement patterns,
- transition logic,
- realistic timing,
- range changes,
- failure/recovery states.

Mark as observed choreography evidence, not official doctrine.

### Tier D — Film / stunt / wuxia references
Use for:
- camera grammar,
- action rhythm,
- environment interaction,
- cinematic exaggeration,
- qinggong/wire-like spatial design.

Never silently merge Tier D into real martial-art technique files.

## Classification before writing

Every candidate must be classified into exactly one primary target:

1. **STYLE** — changes a style's tactical identity or combination grammar.
2. **ATOMIC ACTION** — reusable biomechanical primitive across styles.
3. **CINEMATIC** — camera/stunt/film transformation.
4. **PAIRING** — style-vs-style interaction pattern.
5. **CORE** — universal physical or AI-generation constraint.

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

Deduplicate by **mechanics and exit state**, not by technique name.

Two names that share the same:
- support,
- limb path,
- contact logic,
- physical result,
- exit state

may belong to one atomic card with style-specific aliases.

Conversely, two techniques with similar names but different support/trajectory/result should remain separate.

## Extraction template

For a reusable action:

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
5. identify camera-specific effects separately,
6. route each candidate,
7. dedupe only against the exact target file,
8. write approved ADD/MERGE items.

Never scan the entire reference tree for every candidate.

## Quality gate

Before writing:
- mechanic is physically describable,
- target category is correct,
- base style and cinematic layer are not conflated,
- action has an exit state,
- wording is AI-video usable,
- duplicate check is target-local,
- source confidence is recorded when uncertain.
