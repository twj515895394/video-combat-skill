# Routing Contract — Governance / Audit Specification

This is the full reference-loading governance document.

**Normal generation does not need to read this file.**
The compact runtime rules are already embedded in `reference-router.md`.
Use this document for:
- project/routing review,
- maintenance,
- debugging route leakage,
- extending the routing architecture.

## 1. Router-authority rule

Only these files may authorize loading another content reference:
- `reference-router.md`
- `archetypes/archetype-router.md`
- `actions/action-router.md`
- `combinations/combination-router.md`
- `directing/directing-router.md`
- `directing/style-profiles/style-profile-index.md`
- `multi-opponent/multi-opponent-router.md`
- `style-index.md` only when style identity is genuinely ambiguous
- `reference-ingestion-pipeline.md` only in maintenance / learning mode

Validation authority:
- `qc-gates.md` may conditionally load only `qc/multi-opponent-qc.md` and `qc/directing-qc.md`.

All other content references are **leaf files**.
A leaf may mention another file for explanation, but that mention MUST NOT trigger another read.

## 2. No transitive loading

Never follow references recursively.

Bad:
`wuxia-courtyard -> wuxia-spatial-chains -> qinggong -> directing -> profile`

Correct:
1. classify request,
2. build explicit Load Manifest,
3. enforce budget / exclusions,
4. read exact selected leaves,
5. choreograph,
6. run compact QC and only its applicable specialized QC.

If a leaf reveals a genuine missing need, return to the root router, revise the manifest and deliberately add/swap one file.

## 3. Plan-before-load

Internal manifest:

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

Every non-null leaf needs a one-line reason tied to the user request.
If it cannot be justified, do not load it.

## 4. Non-runtime files

Do not read in ordinary generation:
- `README.md`
- `routing-contract.md`
- `reference-schema.md`
- `sources.md`
- `reference-ingestion-pipeline.md` unless maintenance mode
- `tests/`
- `style-index.md` unless style is unresolved/delegated

## 5. Hard content-leaf budgets

Router/index/QC routing files are control-plane files and are not counted as content leaves.

### SIMPLE_1V1 <=15s
Max **4** content leaves.

### CINEMATIC_1V1 <=15s
Max **6** content leaves.

### ONE_VS_MANY <=15s
Max **6** content leaves.
Typical:
- `archetypes/outnumbered.md`,
- 1 base style,
- 1-2 multi-opponent leaves,
- optional 1 directing OR cinematic,
- optional 1 action/combination if specifically needed.

### REPAIR / FAILURE ANALYSIS
Max **3** content leaves.

### REFERENCE INGESTION
Normally **1-3 target-local** leaves for dedupe/merge.

Prefer replacing a less-specific leaf over adding another.

## 6. Supersession / mutual exclusion

- named action-cinema profile supersedes generic `cinematic/hong-kong-action-language.md` by default,
- `multi-opponent/protagonist-centric-directing.md` supersedes generic framing unless a special framing issue is requested,
- `qinggong.md` requires actual elevated movement; wuxia genre alone is insufficient,
- Combination is not baseline continuity; Zero Idle already covers baseline,
- Atomic Action only fills missing mechanics,
- Core is diagnostic/edge-case context, not default generation context,
- generic `core/action-camera.md` should not be stacked with several detailed Directing leaves by default.

## 7. Stop-loading rule

Stop as soon as the manifest sufficiently answers:
- fight engine,
- fighter movement language,
- causal action continuity,
- spatial continuity,
- required camera information.

More potentially relevant files are not automatically better.

## 8. Directory-scan prohibition

During ordinary generation, repair or prompt creation:
- do not list the full `references/` tree,
- do not search all styles,
- do not wildcard-read directories,
- do not scan siblings for inspiration.

Broad scanning is allowed only for explicit project review, routing audit or library-maintenance work.
