# Reference Router

Selective loading is mandatory. This repository is designed to grow large; broad scanning is a failure mode.

`routing-contract.md` must be loaded **once per task before leaf references**. If `SKILL.md` already loaded it, do not load it again.

## R0 — resolve brief confidence

If a missing detail would materially change combat identity, realism/wuxia level, weapons, participant count, initiator/dominance, core environment, outcome or target AI-video format, read `brief-confirmation.md` and ask only the minimum unresolved core questions.

Do not ask again for information already supplied.
Do not ask for minor details that can be inferred safely.

## R1 — classify, then build the Load Manifest

Classify:
- task mode: generation / repair / analysis / reference-ingest
- duration
- participant structure: 1v1 / one-vs-many
- armed / unarmed
- realism level
- base style(s)
- whether a macro archetype is actually needed
- whether a specific transition problem needs Combination
- whether elevated wuxia movement needs Qinggong
- whether explicit cinematography needs Directing
- whether a named action-cinema profile is requested

Build the complete internal Load Manifest **before reading leaf references**.
Do not incrementally follow links from leaf files.

## R2 — fight-scene archetype

Archetype is optional. Load one only when a macro fight engine adds information beyond the user's brief.

Direct map when obvious:
- continuous pressure -> `archetypes/pressure-duel.md`
- defense/counter -> `archetypes/counter-duel.md`
- chase while fighting -> `archetypes/pursuit-fight.md`
- narrow corridor/room -> `archetypes/confined-space.md`
- stairs/height -> `archetypes/vertical-terrain.md`
- props/architecture drive the fight -> `archetypes/environment-driven.md`
- one-vs-many -> `archetypes/outnumbered.md`
- boss escalation -> `archetypes/boss-escalation.md`
- evenly matched masters -> `archetypes/peer-duel-escalation.md`
- courtyard/long-corridor wuxia driven by architecture -> `archetypes/wuxia-courtyard.md`

Read `archetypes/archetype-router.md` only when the archetype itself is ambiguous.
Never load multiple archetypes merely for inspiration.

### R2A — one-vs-many specialization

When `archetypes/outnumbered.md` is selected, also read:
`multi-opponent/multi-opponent-router.md`

Default short-scene specialization:
- load `active-attacker-scheduling.md` when threat handoff / anti-turn-taking is the main risk,
- load `spatial-funneling.md` when environment / lanes / encirclement are the main risk,
- load `protagonist-centric-directing.md` only when group cinematography is explicitly important,
- load `recovery-reentry-and-sound.md` only when persistence/reentry/off-screen threat sound matters.

Normally select **1-2** multi-opponent leaf files, not all four.

## R3 — base style

Load the exact style file when explicitly named.

| User language | Route |
|---|---|
| 拳击 / boxing | `styles/boxing.md` |
| 踢拳 / kickboxing / low kick | `styles/kickboxing.md` |
| 泰拳 / Muay Thai | `styles/muay-thai.md` |
| 散打 / 散手 / Sanda | `styles/sanda.md` |
| MMA / 综合格斗 | `styles/mma.md` |
| 摔跤 / wrestling / grappling | `styles/wrestling-grappling.md` |
| 空手道 / Karate | `styles/karate.md` |
| 跆拳道 / Taekwondo / TKD | `styles/taekwondo.md` |
| 柔道 / Judo | `styles/judo.md` |
| 巴西柔术 / BJJ | `styles/brazilian-jiu-jitsu.md` |
| Sambo / 桑搏 | `styles/sambo.md` |
| Savate / 法式踢拳 | `styles/savate.md` |
| Lethwei / 缅甸拳 | `styles/lethwei.md` |
| Capoeira / 卡波耶拉 | `styles/capoeira.md` |
| 中国跤 / Shuai Jiao | `styles/chinese/shuai-jiao.md` |
| 南拳 / southern fist | `styles/chinese/southern-nanquan.md` |
| 北拳 / 长拳 / northern long fist | `styles/chinese/northern-longfist.md` |
| 少林 / Shaolin | `styles/chinese/shaolin-general.md` |
| 咏春 / Wing Chun | `styles/chinese/wing-chun.md` |
| 洪拳 / Hung Gar | `styles/chinese/hung-gar.md` |
| 蔡李佛 / Choy Li Fut | `styles/chinese/choy-li-fut.md` |
| 八极拳 / Baji | `styles/chinese/bajiquan.md` |
| 形意拳 / Xingyi | `styles/chinese/xingyiquan.md` |
| 八卦掌 / Bagua | `styles/chinese/baguazhang.md` |
| 太极技击 | `styles/chinese/taijiquan-combat.md` |
| 通背 / Tongbei | `styles/chinese/tongbei.md` |
| 劈挂 / Pigua | `styles/chinese/pigua.md` |
| 翻子 / Fanzi | `styles/chinese/fanzi.md` |

Read `style-index.md` only when exact style identity cannot be resolved from the user request or this table.

## R4 — cinematic transformation

| Intent | Route |
|---|---|
| 写实武侠 / grounded wuxia | `cinematic/grounded-wuxia.md` |
| explicit 轻功 / wall-step / pillar-step / railing leap / airborne wuxia | `cinematic/qinggong.md` |
| generic 港式动作 without a named profile | `cinematic/hong-kong-action-language.md` |
| 现代写实近身动作 | `cinematic/grounded-modern-action.md` |

Rules:
- Wuxia never replaces base martial-art mechanics.
- `qinggong.md` is **not** loaded merely because the genre is wuxia.
- If a specific action-cinema Style Profile is selected, normally skip generic `hong-kong-action-language.md`.

## R5 — mixed-style pairing

Load `pairings/style-vs-style.md` only when two different systems create a meaningful tactical conflict that the choreography must express.

Two different style labels alone are not enough reason.

## R6 — combination grammar

Baseline continuity is already enforced by Zero Idle. Do **not** load Combination by default.

Read `combinations/combination-router.md` only when one specific transition problem is central:
- pressure must chain through hit/miss/block,
- defense must convert to counter,
- striking must collapse into clinch/throw,
- preferred range repeatedly changes,
- miss/landing/stumble must drive the next beat,
- grounded wuxia architecture must create a causal spatial chain.

Default: at most one combination leaf for a short fight.

## R7 — directing

Do not load Directing merely because the output is a video prompt. The universal shot-function rules in `SKILL.md` are enough for ordinary coverage.

Read `directing/directing-router.md` only when the user explicitly requests or the scene critically depends on:
- special framing / partial-body shots,
- POV / attack-to-camera,
- impact inserts,
- camera movement,
- motivated occlusion cuts,
- environment-damage photography,
- editing rhythm,
- complex screen-direction design.

If a named filmmaker/choreographer/action-cinema tradition is requested, load the exact Style Profile directly when mapped below. Use `style-profile-index.md` only when the requested tradition/profile is ambiguous or not directly mapped.

Direct profile map:
- 徐克 / Tsui Hark / 新派港式武侠 -> `directing/style-profiles/tsui-hark-new-wave-wuxia.md`
- 胡金铨 / King Hu -> `directing/style-profiles/king-hu-rhythmic-wuxia.md`
- 袁和平 / Yuen Woo-ping -> `directing/style-profiles/yuen-woo-ping-action-design.md`
- 刘家良 / Lau Kar-leung -> `directing/style-profiles/lau-kar-leung-grounded-martial-arts.md`
- 洪金宝 / Sammo Hung -> `directing/style-profiles/sammo-hung-practical-action.md`

## R8 — atomic mechanics

Read `actions/action-router.md` only when a specific move's biomechanics need more detail than the chosen style already supplies.

Do not load atomic files just because the style file contains a similar action name.

## R9 — repair / troubleshooting

Core repair files are conditional, not default generation context.

| Failure | Reference |
|---|---|
| 背对对手 / 朝向错 | `core/combat-facing.md` |
| 脚步漂移 / 瞬移 / 落脚错 | `core/biomechanics.md` |
| 两人一起乱跳 | `core/aerial-motion.md` |
| 动作停顿 / 回合制 | `core/momentum-continuity.md` |
| generic camera readability failure | `core/action-camera.md` |
| specific cinematography failure | exact relevant `directing/` file |
| 多人一起扑 / 敌人排队 / 敌人消失重生 | exact relevant `multi-opponent/` file |

Do not load `core/action-camera.md` together with several directing files unless the repair explicitly spans both domains.

## R10 — maintenance mode

Read `reference-ingestion-pipeline.md` only when the user explicitly asks to learn from a source, expand the library, or maintain references.

Do not read `sources.md`, `reference-schema.md`, `README.md` or `tests/` during normal prompt generation.

## Runtime budget

Obey `routing-contract.md` hard budgets.

Typical short generation should use fewer references than the maximum.
More relevant-looking files are not automatically better.

## Precedence

User explicit choreography
> physical continuity
> selected base-style mechanics
> archetype macro-structure
> multi-opponent scheduling / spatial plausibility
> combination causality when specifically needed
> shot readability / screen continuity
> cinematic / style-profile transformation
> optional flourish.
