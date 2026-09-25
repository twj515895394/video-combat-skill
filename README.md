# video-combat-skill

AI 视频打斗导演 Skill：将用户的打斗需求转换为具有可读身体力学、连续动量、明确空间关系和电影镜头语言的结构化视频 Prompt。

## 核心设计

本仓库把知识拆成四层：

1. **Core Rules**：所有打斗都必须遵守的身体力学、朝向、脚步、动量、镜头与 AI 生成约束。
2. **Combat Styles**：拳击、踢拳、泰拳、散打、MMA、摔跤、中国武术等“怎么打、偏好什么距离”的流派知识。
3. **Atomic Actions**：直拳、摆拳、掌、肘、侧踹、扫腿、架挡、接腿、抱摔、步法等可跨流派复用的身体动作卡。
4. **Cinematic Layers**：武侠、轻功、港式动作、现代写实动作等影视化表达层。

> 武侠不是一种基础格斗流派。它应作为 cinematic layer 叠加在具体的 base combat style 之上，例如：
> `southern-nanquan + grounded-wuxia`、`northern-longfist + qinggong`。

## 为什么要拆 Style 和 Atomic Action

如果每个流派文件都重复写“直拳怎么打、侧踹怎么落脚、扫腿怎么转髋”，reference 会迅速膨胀并互相矛盾。

因此：

- **Style** 决定战术 DNA：距离、站姿、偏好、进出方式、组合语法。
- **Atomic Action** 决定身体执行：支撑脚、发力链、运动路径、接触、受力结果、末态。
- **Cinematic Layer** 只负责影视放大：空间、轻功、镜头、衣摆、环境互动。

## 目录

- `SKILL.md`：主 Skill 规则与执行流程
- `agents/openai.yaml`：Skill UI 元数据
- `references/reference-router.md`：强制选择性路由
- `references/reference-schema.md`：所有武术 reference 的统一数据规范
- `references/reference-ingestion-pipeline.md`：新增资料/视频的入库协议
- `references/style-index.md`：流派注册表
- `references/core/`：跨流派硬规则
- `references/styles/`：真实格斗 / 武术流派
- `references/actions/`：原子动作卡
- `references/cinematic/`：影视动作层
- `references/pairings/`：不同流派对打时的战术关系
- `references/sources.md`：权威领域来源锚点
- `tests/`：路由、入库与 Prompt QC 测试

## Reference 原则

Reference 不是“招式名词百科”。

每个流派文件必须回答：

- 有效距离是什么？
- 基础站姿和重心是什么？
- 典型步法是什么？
- 主要攻击工具是什么？
- 防守和反击如何发生？
- 动作完成后的身体末态是什么？
- 怎样组成连续动作链？
- AI 视频最容易生成错什么？
- 哪些镜头最适合证明该动作？
- 与其他流派对打时，战术冲突是什么？

每个原子动作必须回答：

- 起始身体状态是什么？
- 哪只脚支撑？
- 哪条肢体启动？
- 运动路径是什么？
- 接触或落空后发生什么？
- 对手身体如何响应？
- 动作末态是什么？
- 下一动作如何从当前末态继续？

Agent 正常执行时禁止递归扫描整个 `references/`。必须先经过 `reference-router.md`，只读取当前任务必要的最小 reference 集。

## 当前第一版已覆盖

Combat sports:
- Boxing
- Kickboxing
- Muay Thai
- Sanda
- MMA
- Wrestling / Grappling

Chinese martial arts:
- Southern Nanquan
- Northern Long Fist
- Wing Chun
- Bajiquan
- Xingyiquan
- Baguazhang
- Taijiquan combat model
- Shuai Jiao

Cinematic:
- Grounded Wuxia
- Qinggong
- Hong Kong action language
- Grounded modern action

Atomic actions:
- footwork
- hand / upper-limb strikes
- kicks / knees
- defense / counters
- clinch / control
- throws / takedowns
