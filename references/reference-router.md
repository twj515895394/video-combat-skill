# Reference Router

Selective loading is mandatory. This repository is designed to grow large; broad scanning is a failure mode.

## R0 — classify the request

Determine:
- task: design / prompt / repair / analyze / reference-ingest
- duration
- armed or unarmed
- realism level
- base combat style(s)
- combination need
- cinematic layer
- directing need
- style-profile need
- whether fighters use different styles
- whether aerial / grappling / environment interaction is required

## R1 — choose base style

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

## R2 — choose cinematic layer

| Intent | Route |
|---|---|
| 写实武侠 / grounded wuxia | `cinematic/grounded-wuxia.md` |
| 轻功 / 借物腾挪 | `cinematic/qinggong.md` |
| 港式动作摄影 | `cinematic/hong-kong-action-language.md` |
| 现代写实近身动作 | `cinematic/grounded-modern-action.md` |

Cinematic files never replace the base style.

## R3 — mixed-style fight

If two fighters use different systems and the tactical mismatch matters, load:
`pairings/style-vs-style.md`

## R4 — combination grammar

If the problem is “how should one move causally become the next,” read:
`combinations/combination-router.md`

Default to at most one combination file for a short fight.

Typical triggers:
- continuous offensive pressure,
- defense-to-counter,
- strike-to-clinch/throw,
- repeated long/close range changes,
- missed move / stumble / landing continuation,
- wuxia environmental movement.

## R5 — directing language

If the request explicitly concerns:
- 镜头设计,
- 景别,
- POV / 拳脚冲镜头,
- 撞击特写,
- 只拍局部身体,
- 运镜,
- 遮挡切镜,
- 环境破坏,
- 影视级动作拍摄,
- 长镜头 vs 快切,

read:
`directing/directing-router.md`

Then load only the 1-2 directing files that solve the current visual problem.

If the user asks for a named filmmaker/choreographer/action-cinema tradition reference, use:
`directing/style-profiles/style-profile-index.md`
and then the exact selected profile.

Named profiles are analytical mechanisms only. Final prompt should translate them into abstract camera/staging/rhythm language rather than outputting only “in the style of X”.

## R6 — atomic mechanics only when needed

If the selected style tells the director what tactical action to use but the exact body mechanics need expansion, read:
`actions/action-router.md`

Examples:
- boxing pivot detail -> `actions/footwork.md`
- Sanda kick catch -> `actions/defense-counter.md`
- Sanda sweep -> `actions/throws-takedowns.md`
- Baji shoulder/forearm impact -> `actions/hand-strikes.md`

Do not load all atomic files automatically.

## R7 — troubleshooting

| Failure | Reference |
|---|---|
| 背对对手 / 朝向错 | `core/combat-facing.md` |
| 脚步漂移 / 瞬移 / 落脚错 | `core/biomechanics.md` |
| 两人一起乱跳 | `core/aerial-motion.md` |
| 动作停顿 / 回合制 | `core/momentum-continuity.md` |
| 镜头遮住动作 | `core/action-camera.md` + relevant `directing/` file |

## R8 — knowledge maintenance

If the user asks to learn from a reference, expand the library, or extract reusable combat/directing assets, read:
`reference-ingestion-pipeline.md`

Route every candidate to exactly one primary target:
STYLE / ATOMIC ACTION / COMBINATION / DIRECTING / STYLE PROFILE / CINEMATIC / PAIRING / CORE.

Never mutate the library merely because a reference was analyzed; maintenance intent must be explicit.

## Maximum normal load budget

For one short fight-generation task, default maximum:
- 1 router
- 1-2 base style references
- 0-1 pairing reference
- 0-1 combination pattern
- 0-1 cinematic layer
- 0-2 directing files
- 0-1 directing style profile
- 0-2 atomic action files only when mechanics need expansion
- 0-1 core repair file

Target: usually 3-7 specialized files, not the whole library.

## Precedence

User explicit choreography
> physical continuity
> selected base-style mechanics
> combination causality
> shot readability / screen continuity
> cinematic/style-profile transformation
> optional flourish.

Never force a visual style choice that hides the movement information needed to understand the fight.

## Unknown or hybrid style

If a named style/profile is missing:
1. map it to movement or directing characteristics,
2. use the closest registered mechanics only as a provisional base,
3. do not invent historical lineage or claim exact authenticity,
4. mark it as a library gap for later reference maintenance.
