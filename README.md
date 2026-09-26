# video-combat-skill

AI 视频打斗导演 Skill：把“怎么打”“为什么这样打”“整场怎么发展”“摄影机怎么看”分层处理，生成具有可读身体力学、连续动量、明确空间关系和影视级镜头语言的动作视频 Prompt。

## 知识层

1. **Core Rules**：身体力学、朝向、脚步、动量、AI 生成硬约束。
2. **Fight Scene Archetypes**：压迫、反击、追击、狭窄空间、高低地形、一打多、Boss、庭院武侠等宏观 Fight Engine。
3. **Combat Styles**：不同格斗/武术体系的距离、站姿、工具和战术 DNA。
4. **Atomic Actions**：拳、掌、肘、腿、格挡、接腿、步法、摔投等动作卡。
5. **Combination Patterns**：局部动作状态如何因果衔接。
6. **Cinematic Layers**：武侠、轻功、现代写实等运动/世界转换。
7. **Directing Library**：景别、局部主体、POV、撞击、运镜、遮挡切镜、环境破坏、剪辑节奏和动作电影 Style Profiles。

额外条件层：
- **Brief Confirmation**：只有需求真正模糊时才确认核心点。
- **Multi-Opponent**：一打多攻击权调度、空间漏斗、主角中心摄影、恢复重入。
- **QC**：核心 QC 常规执行，多人/导演 QC 条件加载。

## Runtime 主链

普通生成只需要遵循：

```text
SKILL.md
  ↓
Resolve Brief
  ↓
reference-router.md
  ↓
Build Load Manifest FIRST
  ↓
Read Exact Authorized Leaves Only
  ↓
Choreograph / Direct
  ↓
qc-gates.md
  ↓
conditional QC only if module is active
```

`routing-contract.md` 是完整治理/审计规范，**不是普通生成的固定必读文件**。

## 防止 Reference 过度扫描

### 1. No Transitive Loading
叶子 reference 里即使提到其它 reference，也不能自动继续读取。

### 2. Plan Before Load
必须先完成完整 Load Manifest，再读取叶子文件，不能边读边扩散。

### 3. Router Authority Only
只有明确的 Router / Index 可以授权读取新 reference。

### 4. Hard Leaf Budget
短视频默认：
- SIMPLE 1v1：最多 4 个 content leaves
- CINEMATIC 1v1：最多 6 个
- ONE-VS-MANY：最多 6 个
- REPAIR：最多 3 个
- REFERENCE INGESTION：默认只比对目标附近 1–3 个

通常应明显低于最大值。

### 5. Stop Loading Early
已有信息足够回答“怎么打、为什么接得上、空间在哪、镜头要看什么”时立即停止加载。

### 6. No Directory Scan
普通生成、修复、Prompt 创作禁止：
- 扫完整 `references/` 树，
- 遍历所有 style，
- wildcard 读取目录，
- 为了 inspiration 扫 sibling references。

只有明确的项目 Review / Routing Audit / Library Maintenance 才允许广泛扫描。

## 关键互斥规则

- 已选徐克 / 胡金铨 / 袁和平 / 刘家良 / 洪金宝等具体 Style Profile -> 默认不再读 generic `hong-kong-action-language.md`。
- 武侠 ≠ 自动轻功；只有真正出现踩墙、借柱、踩栏、腾跃等高低位移动才读 `qinggong.md`。
- Combination 不是默认层；Zero Idle 已负责基础连续性。
- Atomic Action 只补 Style 文件描述不足的具体身体机制。
- Core 主要用于明确故障/边界，不是默认上下文。
- 一打多默认只选 1–2 个 Multi-Opponent 专用 leaves，不全读四个。
- 多人专用 `protagonist-centric-directing` 已加载时，默认不再叠 generic framing。

## Runtime 不默认读取

- `README.md`
- `references/routing-contract.md`
- `references/reference-schema.md`
- `references/sources.md`
- `references/reference-ingestion-pipeline.md`
- `tests/`

`style-index.md` 只在具体流派无法由用户需求 / root router 直接确定时读取。

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
- 单人 / 局部身体镜头
- attack-to-camera / POV threat
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

Style Profiles 是分析参考，最终 Prompt 转译成抽象镜头、调度和节奏机制，而不是只写导演名字。

## 目录

- `SKILL.md`
- `agents/openai.yaml`
- `references/reference-router.md`
- `references/routing-contract.md` — governance/audit only
- `references/brief-confirmation.md`
- `references/qc-gates.md`
- `references/qc/`
- `references/archetypes/`
- `references/styles/`
- `references/actions/`
- `references/combinations/`
- `references/cinematic/`
- `references/directing/`
- `references/multi-opponent/`
- `references/pairings/`
- `references/core/`
- `tests/`
