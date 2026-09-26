# video-combat-skill

AI 视频打斗导演 Skill：把“怎么打”“为什么这样打”“整场怎么发展”“摄影机怎么看”分层处理，生成具有可读身体力学、连续动量、明确空间关系和影视级镜头语言的动作视频 Prompt。

## 七层知识架构

1. **Core Rules**：身体力学、朝向、脚步、动量、AI 生成硬约束。
2. **Fight Scene Archetypes**：压迫战、反击战、追击战、狭窄空间、楼梯高低战、一打多、Boss 战、庭院武侠等宏观 Fight Engine。
3. **Combat Styles**：不同格斗/武术体系的距离、站姿、工具和战术 DNA。
4. **Atomic Actions**：拳、掌、肘、腿、格挡、接腿、步法、摔投等身体动作卡。
5. **Combination Patterns**：上一动作如何因果地变成下一动作。
6. **Cinematic Layers**：武侠、轻功、现代写实等影视/运动空间转换。
7. **Directing Library**：景别、主体选择、POV、撞击特写、运镜、遮挡切镜、环境破坏、剪辑节奏和动作电影风格档案。

另有：
- **Brief Confirmation**：需求真正模糊时只确认核心点。
- **Multi-Opponent**：一打多专用攻击权调度、空间漏斗、主角中心摄影、恢复重入。
- **Routing Contract**：控制运行时只读取最小必要 reference。

## Runtime Routing Contract

正常生成时必须：

```text
Resolve Brief
   ↓
routing-contract.md
   ↓
reference-router.md
   ↓
Build Load Manifest FIRST
   ↓
Enforce Budget / Mutual Exclusions
   ↓
Read Exact Leaf Files Only
   ↓
Choreograph / Direct
   ↓
QC Routing Audit
```

核心规则：

- **No Transitive Loading**：叶子 reference 里提到另一个文件，不代表允许继续读取。
- **Router Authority Only**：只有指定 Router / Index 能授权新 reference。
- **Plan Before Load**：先生成完整 Load Manifest，再读叶子文件。
- **Stop Loading Early**：已经足够创作就停止加载。
- **No Directory Scan**：正常生成、修复、Prompt 创作禁止扫描整个 `references/`。

详见：
`references/routing-contract.md`

## Runtime 不默认读取

以下文件不是普通生成上下文：

- `README.md`
- `references/reference-schema.md`
- `references/sources.md`
- `references/reference-ingestion-pipeline.md`
- `tests/`

`style-index.md` 也只在无法确定具体武术流派时读取。

## Reference Budget

短视频默认硬上限：

- SIMPLE 1v1：最多 4 个 leaf references
- CINEMATIC 1v1：最多 6 个 leaf references
- ONE-VS-MANY：最多 6 个 leaf references
- REPAIR：最多 3 个 leaf references
- REFERENCE INGESTION：默认只检查目标附近 1–3 个 leaf references

通常应该明显低于最大值。

## 重要互斥规则

- 已选徐克 / 胡金铨 / 袁和平 / 刘家良 / 洪金宝等具体 Style Profile 时，默认不再读 generic `hong-kong-action-language.md`。
- “武侠”不自动等于“轻功”；只有真正需要踩墙、借柱、踩栏、腾跃等动作时才加载 `qinggong.md`。
- Combination 不是默认层；Zero Idle 已负责基础连续性，只有明确的转换问题才加载。
- Atomic Action 只有在 Style 文件对某个具体动作描述不够时才加载。
- Core 文件主要用于故障修复，不是默认上下文。
- 一打多默认只选 1–2 个 Multi-Opponent 专用 leaf，不全读四个。

## 需求确认

如果用户已经明确时长、人数、徒手/兵器、场景、谁先攻、武术体系、写实/武侠程度，就直接创作，不重复提问。

如果缺失的信息会导致完全不同的打斗设计，则读取 `references/brief-confirmation.md`，一次性只确认最关键的 1–3 个点。

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
- 可复用动作镜头卡

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
- `references/routing-contract.md`
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
- `references/multi-opponent/`
- `references/pairings/`
- `references/core/`
- `references/sources.md`
- `tests/`
