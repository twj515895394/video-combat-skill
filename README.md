# video-combat-skill

AI 视频打斗导演 Skill：把“怎么打”“为什么这样打”“整场怎么发展”“摄影机怎么看”分层处理，生成具有可读身体力学、连续动量、明确空间关系和影视级镜头语言的动作视频 Prompt。

## 七层知识架构

1. **Core Rules**：身体力学、朝向、脚步、动量、AI 生成硬约束。
2. **Fight Scene Archetypes**：压迫战、反击战、追击战、狭窄空间、楼梯高低战、一打多、Boss 战、庭院武侠等整场 Fight Engine。
3. **Combat Styles**：不同格斗/武术体系的距离、站姿、工具和战术 DNA。
4. **Atomic Actions**：拳、掌、肘、腿、格挡、接腿、步法、摔投等身体动作卡。
5. **Combination Patterns**：上一动作如何因果地变成下一动作。
6. **Cinematic Layers**：武侠、轻功、港式动作、现代写实等影视转换。
7. **Directing Library**：景别、主体选择、POV、撞击特写、运镜、遮挡切镜、环境破坏、剪辑节奏和动作电影风格档案。

另有 **Brief Confirmation** 层负责在需求真正模糊时先确认核心创作条件。

## 需求确认

如果用户已经明确时长、人数、徒手/兵器、场景、谁先攻、武术体系、写实/武侠程度，就直接创作，不重复提问。

如果缺失的信息会导致完全不同的打斗设计，则读取 `references/brief-confirmation.md`，一次性只确认最关键的 1-3 个点。

## Fight Scene Archetypes

当前覆盖：
- Pressure Duel
- Counter Duel
- Pursuit Fight
- Confined-Space Fight
- Vertical Terrain Fight
- Environment-Driven Fight
- Outnumbered Fight
- Boss Escalation
- Peer Duel Escalation
- Wuxia Courtyard Fight

## Directing Library

当前覆盖：
- 景别与镜头主体选择
- 单人镜头 / 局部身体镜头
- 拳脚向镜头逼近 / POV threat
- impact inserts
- 横移、后退、甩镜、落点截击
- 遮挡切镜
- 环境破坏
- 长镜头 vs 快切
- screen direction / continuity
- 20 个可复用动作镜头卡

## Action Cinema Style Profiles

- New-Wave Hong Kong Wuxia / Tsui Hark reference
- King Hu rhythmic widescreen wuxia
- Yuen Woo-ping tempo / prop / attack-defense design
- Lau Kar-leung grounded martial-arts display
- Sammo Hung practical weighted action

Named profiles are analytical references. Final generation prompts translate them into abstract shot grammar rather than merely writing a filmmaker name.

## 目录

- `SKILL.md`
- `agents/openai.yaml`
- `references/brief-confirmation.md`
- `references/reference-router.md`
- `references/reference-schema.md`
- `references/reference-ingestion-pipeline.md`
- `references/archetypes/`
- `references/styles/`
- `references/actions/`
- `references/combinations/`
- `references/cinematic/`
- `references/directing/`
- `references/directing/style-profiles/`
- `references/pairings/`
- `references/core/`
- `references/sources.md`
- `tests/`

## Reference budget

Agent 正常执行时禁止递归扫描整个 `references/`。

必须先经过 `reference-router.md`，只加载当前任务真正需要的少量 Archetype / Style / Action / Combination / Directing / Cinematic references。
