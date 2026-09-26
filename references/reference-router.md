# Reference Router

Selective loading is mandatory. This repository is designed to grow large; broad scanning is a failure mode.

## R0 — resolve brief confidence

Before specialized routing, determine whether the request is sufficiently defined.

If a missing detail would materially change:
- combat identity,
- realism / wuxia level,
- weapons,
- participant count,
- initiator / dominance,
- core environment,
- outcome,
- target AI-video format,

read `brief-confirmation.md` and ask only the minimum unresolved core questions.

Do not ask again for information already supplied.
Do not ask for minor details that can be inferred safely.

## R1 — classify the task

Determine:
- task: design / prompt / repair / analyze / reference-ingest
- duration
- armed or unarmed
- realism level
- base combat style(s)
- fight-scene archetype need
- multi-opponent need
- combination need
- cinematic layer
- directing need
- style-profile need
- whether fighters use different styles
- whether aerial / grappling / environment interaction is required

## R2 — choose fight-scene archetype

If the macro fight structure is not already obvious, read:
`archetypes/archetype-router.md`

Choose one primary archetype for a short sequence.

Examples:
- continuous pressure -> `archetypes/pressure-duel.md`
- defense/counter -> `archetypes/counter-duel.md`
- chase while fighting -> `archetypes/pursuit-fight.md`
- narrow corridor -> `archetypes/confined-space.md`
- stairs / height -> `archetypes/vertical-terrain.md`
- props / architecture -> `archetypes/environment-driven.md`
- one-vs-many -> `archetypes/outnumbered.md`
- boss escalation -> `archetypes/boss-escalation.md`
- evenly matched masters -> `archetypes/peer-duel-escalation.md`
- courtyard wuxia -> `archetypes/wuxia-courtyard.md`

Do not load multiple archetypes merely for inspiration.

### R2A — one-vs-many specialization

Whenever `archetypes/outnumbered.md` is selected, also read:
`multi-opponent/multi-opponent-router.md`

Then selectively load only the needed files:
- `multi-opponent/active-attacker-scheduling.md`
- `multi-opponent/spatial-funneling.md`
- `multi-opponent/protagonist-centric-directing.md`
- `multi-opponent/recovery-reentry-and-sound.md`

Do not treat one-vs-many as several independent 1v1 rounds.

## R3 — choose base style

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

If the user only says "中国武术", read `style-index.md` first, then select one family based on requested range and movement character.

## R4 — choose cinematic layer

| Intent | Route |
|---|---|
| 写实武侠 / grounded wuxia | `cinematic/grounded-wuxia.md` |
| 轻功 / 借物腾挪 | `cinematic/qinggong.md` |
| 港式动作摄影 | `cinematic/hong-kong-action-language.md` |
| 现代写实近身动作 | `cinematic/grounded-modern-action.md` |

Cinematic files never replace the base style.

## R5 — mixed-style fight

If two fighters use different systems and the tactical mismatch matters, load:
`pairings/style-vs-style.md`

## R6 — combination grammar

If the problem is “how should one move causally become the next,” read:
`combinations/combination-router.md`

Default to at most one combination file for a short fight.

## R7 — directing language

If the request concerns cinematic framing, POV, impact inserts, camera movement, occlusion cuts, destruction, long-take vs fast-cut rhythm, read:
`directing/directing-router.md`

Then load only the 1-2 directing files that solve the current visual problem.

If the user asks for a named filmmaker/choreographer/action-cinema tradition reference, use:
`directing/style-profiles/style-profile-index.md`
and then the exact selected profile.

Named profiles are analytical mechanisms only. Final prompt should translate them into abstract camera/staging/rhythm language rather than outputting only “in the style of X”.

## R8 — atomic mechanics only when needed

If exact body mechanics need expansion, read:
`actions/action-router.md`

Do not load all atomic files automatically.

## R9 — troubleshooting

| Failure | Reference |
|---|---|
| 背对对手 / 朝向错 | `core/combat-facing.md` |
| 脚步漂移 / 瞬移 / 落脚错 | `core/biomechanics.md` |
| 两人一起乱跳 | `core/aerial-motion.md` |
| 动作停顿 / 回合制 | `core/momentum-continuity.md` |
| 镜头遮住动作 | `core/action-camera.md` + relevant `directing/` file |
| 多人一起扑 / 敌人排队等 / 敌人消失重生 | relevant `multi-opponent/` file |

## R10 — knowledge maintenance

If the user asks to learn from a reference, expand the library, or extract reusable combat/directing assets, read:
`reference-ingestion-pipeline.md`

Route every candidate to exactly one primary target:
STYLE / ATOMIC ACTION / COMBINATION / ARCHETYPE / MULTI-OPPONENT / DIRECTING / STYLE PROFILE / CINEMATIC / PAIRING / CORE.

Never mutate the library merely because a reference was analyzed; maintenance intent must be explicit.

## Maximum normal load budget

For one short fight-generation task, default maximum:
- 1 router
- 0-1 archetype
- 0-2 multi-opponent files only for one-vs-many
- 1-2 base style references
- 0-1 pairing reference
- 0-1 combination pattern
- 0-1 cinematic layer
- 0-2 directing files
- 0-1 directing style profile
- 0-2 atomic action files only when mechanics need expansion
- 0-1 core repair file

Target: usually 3-8 specialized files, not the whole library.

## Precedence

User explicit choreography
> physical continuity
> selected base-style mechanics
> archetype macro-structure
> multi-opponent scheduling / spatial plausibility
> combination causality
> shot readability / screen continuity
> cinematic/style-profile transformation
> optional flourish.

Never force an archetype or visual style choice that contradicts the user's stated fight logic.
