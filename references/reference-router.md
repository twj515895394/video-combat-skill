# Reference Router

Selective loading is mandatory. This repository is designed to grow large; broad scanning is a failure mode.

## Routing sequence

### R0 — classify the request

Determine:
- task: design / prompt / repair / analyze / reference-ingest
- duration
- armed or unarmed
- realism level
- base combat style(s)
- cinematic layer
- whether fighters use different styles
- whether aerial / grappling / environment interaction is required

### R1 — choose base style

Load the exact style file when explicitly named.

Direct map:

| User language | Route |
|---|---|
| 拳击 / boxing | `styles/boxing.md` |
| 踢拳 / kickboxing / low kick | `styles/kickboxing.md` |
| 泰拳 / Muay Thai | `styles/muay-thai.md` |
| 散打 / 散手 / Sanda | `styles/sanda.md` |
| MMA / 综合格斗 | `styles/mma.md` |
| 摔跤 / wrestling / grappling | `styles/wrestling-grappling.md` |
| 摔跤式中国跤 / 摔跤 / Shuai Jiao | `styles/chinese/shuai-jiao.md` |
| 南拳 / southern fist | `styles/chinese/southern-nanquan.md` |
| 北拳 / 长拳 / northern long fist | `styles/chinese/northern-longfist.md` |
| 咏春 / Wing Chun | `styles/chinese/wing-chun.md` |
| 八极拳 / Baji | `styles/chinese/bajiquan.md` |
| 形意拳 / Xingyi | `styles/chinese/xingyiquan.md` |
| 八卦掌 / Bagua | `styles/chinese/baguazhang.md` |
| 太极技击 | `styles/chinese/taijiquan-combat.md` |

If the user only says "中国武术", read `style-index.md` first, then select one family based on requested range and movement character.

### R2 — choose cinematic layer

| Intent | Route |
|---|---|
| 写实武侠 / grounded wuxia | `cinematic/grounded-wuxia.md` |
| 轻功 / 借物腾挪 | `cinematic/qinggong.md` |
| 港式动作摄影 | `cinematic/hong-kong-action-language.md` |
| 现代写实近身动作 | `cinematic/grounded-modern-action.md` |

Cinematic files never replace the base style.

### R3 — mixed-style fight

If two fighters use different systems and the tactical mismatch matters, load:
`pairings/style-vs-style.md`

Do not load it when both fighters share the same style and the user only needs a simple exchange.

### R4 — atomic mechanics only when needed

If the selected style tells the director **what tactical action to use** but the exact body mechanics need expansion, read `actions/action-router.md` and load only the exact atomic category needed.

Examples:
- boxing pivot detail -> `actions/footwork.md`
- Sanda kick catch -> `actions/defense-counter.md`
- Sanda sweep -> `actions/throws-takedowns.md`
- Baji shoulder/forearm impact -> `actions/hand-strikes.md`

Do not load all atomic files automatically.

### R5 — troubleshooting

Load core files only for the problem being repaired:

| Failure | Reference |
|---|---|
| 背对对手 / 朝向错 | `core/combat-facing.md` |
| 脚步漂移 / 瞬移 / 落脚错 | `core/biomechanics.md` |
| 两人一起乱跳 | `core/aerial-motion.md` |
| 动作停顿 / 回合制 | `core/momentum-continuity.md` |
| 镜头遮住动作 | `core/action-camera.md` |

### R6 — knowledge maintenance

If the user asks to:
- 学习这个参考视频,
- 看看有没有值得沉淀进 Skill,
- 补充 reference,
- 扩充某个流派招式库,
- 从资料中提取可复用动作,

read `reference-ingestion-pipeline.md`.

Route every candidate to exactly one primary target: STYLE / ATOMIC ACTION / CINEMATIC / PAIRING / CORE.

Never mutate the library merely because a reference was analyzed; maintenance intent must be explicit.

## Maximum normal load budget

For one short fight-generation task, default maximum:
- 1 router
- 1-2 base style references
- 0-1 cinematic layer
- 0-1 pairing reference
- 0-2 atomic action files only when mechanics need expansion
- 0-1 core repair file

Target: 2-5 specialized files, not the whole library.

## Precedence

User explicit choreography > physical continuity > selected base-style mechanics > cinematic layer > optional flourish.

Never force a reference move into a sequence if it breaks the user's action, duration, body state or spatial continuity.

## Unknown or hybrid style

If a named style is missing:
1. map it to a movement family by range, stance, tools and tactical goal,
2. use the closest registered mechanics only as a provisional base,
3. do not invent historical lineage or claim exact authenticity,
4. mark it as a library gap for later reference maintenance.
