# Routing Contract

This file defines runtime reference-loading policy. It has higher priority than cross-references written inside leaf files.

## 1. Router-authority rule

Only these files may authorize loading another reference:
- `reference-router.md`
- `archetypes/archetype-router.md`
- `actions/action-router.md`
- `combinations/combination-router.md`
- `directing/directing-router.md`
- `directing/style-profiles/style-profile-index.md`
- `multi-opponent/multi-opponent-router.md`
- `style-index.md` only when style identity is genuinely ambiguous
- `reference-ingestion-pipeline.md` only in maintenance / learning mode

All other references are **leaf files**.

A leaf file may mention another style, action, combination, cinematic layer, directing file or profile for explanation, but that mention MUST NOT trigger another read.

## 2. No transitive loading

Never follow references recursively.

Bad:
`wuxia-courtyard.md -> useful combination -> wuxia-spatial-chains.md -> qinggong.md -> directing file -> style profile`

Correct:
1. classify the request,
2. build one explicit Load Manifest,
3. enforce the budget,
4. read only those exact files,
5. choreograph.

If a loaded leaf reveals a genuine missing requirement, return to the router, revise the Load Manifest, and add or swap one file deliberately. Do not follow the leaf automatically.

## 3. Plan-before-load

Before reading specialized leaf references, construct an internal Load Manifest:

```yaml
mode:
primary_archetype:
base_styles: []
pairing:
combination:
cinematic:
multi_opponent: []
directing: []
style_profile:
atomic_actions: []
core_repairs: []
```

Every non-null entry must have a one-line reason tied to the user's request.

If a file cannot be justified in one line, do not load it.

## 4. Runtime files that are NOT default references

Do not read these during normal generation unless their special condition applies:
- `README.md` — documentation only.
- `reference-schema.md` — library-authoring only.
- `sources.md` — verification / maintenance only.
- `reference-ingestion-pipeline.md` — only when user asks to learn, expand or maintain references.
- `style-index.md` — only when exact style cannot be resolved from the user request / root router.
- `tests/` — never runtime generation references.

## 5. Hard load budgets

Routers/indexes are lightweight routing files; leaf references are the main budget.

### SIMPLE_1V1, <=15s
Max leaf refs: **4**.
Typical:
- 1 base style,
- optional 1 archetype OR pairing,
- optional 1 cinematic/directing/combination,
- optional 1 atomic/core detail.

### CINEMATIC_1V1, <=15s
Max leaf refs: **6**.
Typical:
- 1-2 base styles,
- 0-1 archetype,
- 0-1 pairing/combination,
- 0-1 cinematic,
- 0-1 directing/profile.

### ONE_VS_MANY, <=15s
Max leaf refs: **6**.
Typical:
- `archetypes/outnumbered.md`,
- 1 base style,
- 1-2 multi-opponent leaves,
- 0-1 directing OR cinematic,
- 0-1 action/combination only if specifically needed.

### REPAIR / FAILURE ANALYSIS
Max leaf refs: **3**.
Load only the failed domain:
- style if identity is relevant,
- one core repair file,
- one directing/action file if needed.

### REFERENCE INGESTION
Default target-local leaf refs: **1-3**.
Never scan the whole library to deduplicate one candidate.

If a task truly needs more than the budget, prefer replacing a less-specific file rather than simply adding another.

## 6. Supersession / mutual-exclusion rules

### Named action-cinema profile vs generic Hong Kong camera language
If a specific profile such as Tsui Hark / King Hu / Yuen Woo-ping / Lau Kar-leung / Sammo Hung is selected, do **not** also load `cinematic/hong-kong-action-language.md` by default.
The specific profile supersedes generic Hong Kong camera grammar.

### Multi-opponent directing vs generic framing
If `multi-opponent/protagonist-centric-directing.md` is loaded, do not also load generic `directing/framing-and-subject-selection.md` unless the user explicitly requests a special framing problem.

### Qinggong vs Grounded Wuxia
Do not load `qinggong.md` merely because the genre is wuxia.
Load qinggong only when the requested choreography actually contains elevated push-off, wall/rail/pillar movement, gliding or airborne exchange.

### Combination layer
Do not load a combination file merely because all fights need continuity.
The universal Zero Idle rule already covers baseline continuity.
Load a combination file only when a specific transition problem is central: pressure chaining, counter conversion, range conversion, strike-to-throw, failure recovery, or wuxia spatial chaining.

### Atomic actions
Do not load atomic libraries to explain moves already sufficiently described by the selected style reference.
Load only when one specific body mechanic needs extra precision.

### Core repair files
Core files are not default generation context.
Load them for an identified failure mode or when the current brief specifically depends on that edge case.

### Camera core vs directing library
Do not load both `core/action-camera.md` and multiple directing files by default.
Use `core/action-camera.md` for generic camera-readability repair; use `directing/` for explicit cinematography design.

## 7. Stop-loading rule

Stop reading references as soon as the Load Manifest contains enough information to answer:
- what is the fight engine,
- how each fighter moves,
- how actions causally connect,
- how space is preserved,
- what the camera must show.

More potentially relevant references are not automatically better.

## 8. Directory-scan prohibition

During normal generation, repair or prompt creation:
- do not list the entire `references/` tree,
- do not search all style files,
- do not wildcard-read directories,
- do not scan sibling files “for inspiration”.

Broad repository scanning is allowed only for explicit project review, routing audit, or reference-maintenance tasks.
