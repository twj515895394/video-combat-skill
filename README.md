# video-combat-skill

AI 视频打斗导演 Skill：将用户的打斗需求转换为具有可读身体力学、连续动量、明确空间关系和电影镜头语言的结构化视频 Prompt。

## 核心设计

本仓库把知识拆成三层：

1. **Core Rules**：所有打斗都必须遵守的身体力学、朝向、脚步、动量、镜头与 AI 生成约束。
2. **Combat References**：拳击、踢拳、泰拳、散打、MMA、摔跤、中国武术等真实动作语言。
3. **Cinematic Layers**：武侠、港式动作、写实近身、夸张轻功等影视化表达层。

> 武侠不是一种基础格斗流派。它应作为 cinematic layer 叠加在具体的 base combat style 之上，例如：
> `southern_nanquan + grounded_wuxia`、`northern_longfist + qinggong`。

## 目录

- `SKILL.md`：主 Skill 规则与执行流程
- `references/reference-router.md`：强制选择性路由
- `references/reference-schema.md`：所有武术 reference 的统一数据规范
- `references/style-index.md`：流派注册表
- `references/core/`：跨流派硬规则
- `references/styles/`：真实格斗 / 武术流派
- `references/cinematic/`：影视动作层
- `references/pairings/`：不同流派对打时的战术关系
- `tests/`：路由与 Prompt QC 测试

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

Agent 正常执行时禁止递归扫描整个 `references/`。必须先经过 `reference-router.md`，只读取当前任务必要的最小 reference 集。
