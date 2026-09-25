# video-combat-skill

AI 视频打斗导演 Skill：将用户的打斗需求转换为具有可读身体力学、连续动量、明确空间关系和电影镜头语言的结构化视频 Prompt。

## 核心设计

本仓库把知识拆成五层：

1. **Core Rules**：身体力学、朝向、脚步、动量、镜头与 AI 生成硬约束。
2. **Combat Styles**：拳击、踢拳、泰拳、散打、MMA、中国武术等“偏好什么距离、怎么打”的流派 DNA。
3. **Atomic Actions**：直拳、掌、肘、侧踹、扫腿、架挡、接腿、抱摔、步法等跨流派身体动作卡。
4. **Combination Patterns**：上一动作造成什么状态、下一动作为什么自然出现的因果语法。
5. **Cinematic Layers**：武侠、轻功、港式动作、现代写实动作等影视转换层。

> 武侠不是一种基础格斗流派。它应叠加在具体的 base combat style 之上，例如：
> `southern-nanquan + range-conversion + grounded-wuxia`
> `northern-longfist + recovery-chain + qinggong`

## 为什么要拆 Style / Action / Combination

- **Style** 决定战术：距离、站姿、偏好、进出方式。
- **Atomic Action** 决定身体执行：支撑脚、发力链、运动路径、接触、末态。
- **Combination** 决定因果连续：miss / block / impact / landing 之后为什么出现下一动作。
- **Cinematic Layer** 决定影视放大：空间、轻功、环境、镜头、衣摆。

这样可以避免每个流派重复写相同动作，也避免 Agent 把招式随机串成“动作拼盘”。

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
- `references/pairings/`
- `references/sources.md`
- `tests/`

## Reference 原则

Reference 不是“招式名词百科”。

流派文件回答“为什么这么打”；原子动作回答“身体怎么完成”；组合库回答“为什么下一招能接上”；影视层回答“怎么把有效动作拍得更像电影”。

Agent 正常执行时禁止递归扫描整个 `references/`。必须先经过 `reference-router.md`，只读取当前任务必要的最小 reference 集。

## 当前已覆盖

### Combat sports / modern
Boxing, Kickboxing, Muay Thai, Sanda, MMA, Wrestling/Grappling, Karate, Taekwondo, Judo, Brazilian Jiu-Jitsu, Sambo, Savate, Lethwei, Capoeira.

### Chinese martial arts
Southern Nanquan, Northern Long Fist, Wing Chun, Bajiquan, Xingyiquan, Baguazhang, Taijiquan combat, Shuai Jiao, Hung Gar, Choy Li Fut, Tongbei, Pigua, Fanzi, broad Shaolin fallback.

### Cinematic
Grounded Wuxia, Qinggong, Hong Kong action language, Grounded modern action.

### Atomic actions
Footwork, hand/upper-limb strikes, kicks/knees, defense/counter, clinch/control, throws/takedowns.

### Combination grammar
Pressure chains, counter conversions, clinch/throw transitions, range conversions, recovery/failure chains, grounded wuxia spatial chains.
