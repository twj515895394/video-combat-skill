# Runtime Reference Router

This is the only root router required for ordinary generation.
Full governance details live in `routing-contract.md`, but that file is not a normal runtime dependency.

## 0. Runtime authority

Before leaf reads, build one internal Load Manifest:

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

Rules:
- leaf references cannot authorize another read,
- never follow cross-references transitively,
- every loaded leaf needs one concrete reason tied to the brief,
- never scan directories/sibling files for inspiration,
- if a new need appears, return here and deliberately revise the manifest.

Do not read during normal generation:
`README.md`, `sources.md`, `reference-schema.md`, `reference-ingestion-pipeline.md`, `routing-contract.md`, `tests/`.

## 1. Hard leaf budgets

Routers/indexes are not counted as leaves.

- SIMPLE 1v1 <=15s: **max 4 leaves**
- CINEMATIC 1v1 <=15s: **max 6 leaves**
- ONE-VS-MANY <=15s: **max 6 leaves**
- REPAIR / FAILURE ANALYSIS: **max 3 leaves**
- REFERENCE INGESTION: normally **1-3 target-local leaves**

Prefer replacing a less-specific leaf over adding another.
Stop loading as soon as fight engine, movement language, causality, space and required camera information are sufficient.

## 2. Brief confidence

If a missing fact would materially change combat identity, realism/wuxia level, weapons, participant count, initiator/dominance, environment, outcome or target format, read `brief-confirmation.md` and ask only the minimum unresolved points.

Do not re-ask known information.

## 3. Archetype — optional

Load an Archetype only when it adds useful macro structure beyond the brief.

Direct routes:
- continuous pressure -> `archetypes/pressure-duel.md`
- defense/counter -> `archetypes/counter-duel.md`
- chase while fighting -> `archetypes/pursuit-fight.md`
- narrow corridor/room -> `archetypes/confined-space.md`
- stairs/height -> `archetypes/vertical-terrain.md`
- environment drives routes -> `archetypes/environment-driven.md`
- one-vs-many -> `archetypes/outnumbered.md`
- boss escalation -> `archetypes/boss-escalation.md`
- evenly matched masters -> `archetypes/peer-duel-escalation.md`
- architecture-driven courtyard wuxia -> `archetypes/wuxia-courtyard.md`

Read `archetypes/archetype-router.md` only if the archetype itself is ambiguous.
Use at most one primary archetype for a short fight.

### One-vs-many specialization
If `outnumbered.md` is selected, read `multi-opponent/multi-opponent-router.md` and normally choose only **1-2** specialized leaves:
- threat handoff / anti-turn-taking -> `active-attacker-scheduling.md`
- lanes / funnel / encirclement -> `spatial-funneling.md`
- protagonist-centered group camera -> `protagonist-centric-directing.md`
- recovery / reentry / off-screen sound -> `recovery-reentry-and-sound.md`

## 4. Base style

If exact style is named, load its exact leaf directly.

### Modern / combat sports
- Boxing -> `styles/boxing.md`
- Kickboxing -> `styles/kickboxing.md`
- Muay Thai / 泰拳 -> `styles/muay-thai.md`
- Sanda / 散打 / 散手 -> `styles/sanda.md`
- MMA -> `styles/mma.md`
- Wrestling / Grappling -> `styles/wrestling-grappling.md`
- Karate / 空手道 -> `styles/karate.md`
- Taekwondo / 跆拳道 -> `styles/taekwondo.md`
- Judo / 柔道 -> `styles/judo.md`
- BJJ / 巴西柔术 -> `styles/brazilian-jiu-jitsu.md`
- Sambo -> `styles/sambo.md`
- Savate -> `styles/savate.md`
- Lethwei -> `styles/lethwei.md`
- Capoeira -> `styles/capoeira.md`

### Chinese martial arts
- 南拳 / Nanquan -> `styles/chinese/southern-nanquan.md`
- 北拳 / 长拳 / Changquan -> `styles/chinese/northern-longfist.md`
- 少林 -> `styles/chinese/shaolin-general.md`
- 咏春 -> `styles/chinese/wing-chun.md`
- 洪拳 -> `styles/chinese/hung-gar.md`
- 蔡李佛 -> `styles/chinese/choy-li-fut.md`
- 八极拳 -> `styles/chinese/bajiquan.md`
- 形意拳 -> `styles/chinese/xingyiquan.md`
- 八卦掌 -> `styles/chinese/baguazhang.md`
- 太极技击 -> `styles/chinese/taijiquan-combat.md`
- 通背 -> `styles/chinese/tongbei.md`
- 劈挂 -> `styles/chinese/pigua.md`
- 翻子 -> `styles/chinese/fanzi.md`
- 中国跤 / Shuai Jiao -> `styles/chinese/shuai-jiao.md`

Read `style-index.md` only when exact style cannot be resolved or the user delegates a broad family choice. It is style-only and must not open other domains.

## 5. Cinematic layer — optional

- 写实武侠 / grounded wuxia -> `cinematic/grounded-wuxia.md`
- explicit 轻功 / 踩墙 / 借柱 / 踩栏 / airborne wuxia -> `cinematic/qinggong.md`
- generic 港式动作 with no named profile -> `cinematic/hong-kong-action-language.md`
- modern grounded close action -> `cinematic/grounded-modern-action.md`

Important:
- wuxia never replaces base martial-art mechanics,
- wuxia does **not** automatically imply qinggong,
- a named Style Profile normally supersedes generic Hong Kong action language.

## 6. Pairing — optional

Load `pairings/style-vs-style.md` only when two systems create a tactical conflict the scene needs to express: preferred range, entry, range restoration, throw-vs-strike, etc.

Different style names alone do not require Pairing.

## 7. Combination — optional, not baseline

Zero Idle already handles normal continuity.
Read `combinations/combination-router.md` only for a central transition problem:
- continued pressure after hit/miss/block,
- defense -> counter,
- strike -> clinch/throw,
- repeated range conversion,
- miss/landing/stumble -> next beat,
- architecture-driven wuxia chain.

Default: at most one Combination leaf for a short scene.

## 8. Directing / Style Profile — optional

Ordinary video prompts do not automatically require the Directing library.
Read `directing/directing-router.md` only for explicit/critical cinematography needs: partial-body framing, POV, attack-to-camera, impact insert, camera movement, occlusion cut, damage photography, editing rhythm or screen-direction design.

Named profile direct map:
- 徐克 / Tsui Hark / 新派港式武侠 -> `directing/style-profiles/tsui-hark-new-wave-wuxia.md`
- 胡金铨 / King Hu -> `directing/style-profiles/king-hu-rhythmic-wuxia.md`
- 袁和平 / Yuen Woo-ping -> `directing/style-profiles/yuen-woo-ping-action-design.md`
- 刘家良 / Lau Kar-leung -> `directing/style-profiles/lau-kar-leung-grounded-martial-arts.md`
- 洪金宝 / Sammo Hung -> `directing/style-profiles/sammo-hung-practical-action.md`

Read `style-profile-index.md` only when the requested tradition/profile is ambiguous or unmapped.
Use at most one profile unless the user explicitly asks for comparison/hybridization.

## 9. Atomic Action — optional

Read `actions/action-router.md` only when a specific move needs more biomechanical detail than its Style leaf already provides.

Do not load Atomic Action just because a move name appears in the Style reference.

## 10. Core repair — conditional

Core files are diagnostic/edge-case references, not default context.

- back-facing / orientation -> `core/combat-facing.md`
- feet / teleport / landing -> `core/biomechanics.md`
- synchronized hopping / aerial error -> `core/aerial-motion.md`
- turn-taking / reset -> `core/momentum-continuity.md`
- generic camera readability -> `core/action-camera.md`

For a specific cinematography failure, prefer the exact `directing/` leaf instead of loading generic camera core plus several directing files.
For a one-vs-many failure, prefer the exact `multi-opponent/` leaf.

## 11. Maintenance mode

Read `reference-ingestion-pipeline.md` only when the user explicitly asks to learn from a source, expand the library or maintain references.
Deduplication should be target-local, normally against only 1-3 nearby leaves.

## 12. Mutual-exclusion reminders

- named Style Profile -> normally no generic Hong Kong fallback,
- `multi-opponent/protagonist-centric-directing.md` -> normally no generic framing leaf,
- qinggong only for actual elevated movement,
- Combination only for a specific transition problem,
- Atomic only for missing mechanic detail,
- Core only for identified failure/edge case,
- avoid `core/action-camera.md` + multiple detailed Directing leaves by default.

## Precedence

User explicit choreography
> physical continuity
> base-style mechanics
> optional archetype / multi-opponent spatial logic
> specific combination causality
> shot readability
> cinematic / Style Profile transformation
> flourish.
