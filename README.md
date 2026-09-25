# video-combat-skill

AI 视频打斗导演 Skill：把“怎么打”与“怎么拍”分层处理，生成具有可读身体力学、连续动量、明确空间关系和影视级镜头语言的动作视频 Prompt。

## 六层知识架构

1. **Core Rules**：身体力学、朝向、脚步、动量、AI 生成硬约束。
2. **Combat Styles**：不同格斗/武术体系的距离、站姿、工具和战术 DNA。
3. **Atomic Actions**：拳、掌、肘、腿、格挡、接腿、步法、摔投等身体动作卡。
4. **Combination Patterns**：上一动作如何因果地变成下一动作。
5. **Cinematic Layers**：武侠、轻功、港式动作、现代写实等影视转换。
6. **Directing Library**：景别、主体选择、POV、撞击特写、运镜、遮挡切镜、环境破坏、剪辑节奏和动作电影风格档案。

## 核心原则

**Style 解决为什么这么打；Action 解决身体怎么完成；Combination 解决为什么能接下一招；Directing 解决观众怎么看见；Style Profile 解决整场动作采用什么影视语言。**

## 目录

- `SKILL.md`
- `agents/openai.yaml`
- `references/reference-router.md`
- `references/reference-schema.md`
- `references/reference-ingestion-pipeline.md`
- `references/style-index.md`
- `references/core/`
- `references/styles/`
- `references/actions/`
- `references/combinations/`
- `references/cinematic/`
- `references/directing/`
- `references/directing/style-profiles/`
- `references/pairings/`
- `references/sources.md`
- `tests/`

## Directing Library 当前覆盖

- 景别与镜头主体选择
- 单人镜头 / 局部身体镜头
- 拳脚向镜头逼近 / POV threat
- 拳掌打胸、格挡、肘肩撞击等 impact inserts
- 横移、后退、甩镜、落点截击等运镜
- 衣袖、身体、柱子、腿部等遮挡切镜
- 撞墙、木屑、石粉、栏杆、桌椅破坏
- 长镜头 vs 快切
- screen direction / action continuity

## Action Cinema Style Profiles

- New-Wave Hong Kong Wuxia / Tsui Hark reference
- King Hu rhythmic widescreen wuxia
- Yuen Woo-ping tempo / prop / attack-defense design
- Lau Kar-leung grounded martial-arts display
- Sammo Hung practical weighted action

Named profiles are analytical references. Final generation prompts translate them into abstract shot grammar rather than merely writing a filmmaker name.

## Reference budget

Agent 正常执行时禁止递归扫描整个 `references/`。

必须先经过 `reference-router.md`，只加载当前任务真正需要的少量 Style / Action / Combination / Directing / Cinematic references。
