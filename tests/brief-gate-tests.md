# Combat Brief Gate Regression Tests

These tests validate that prompt generation does not begin until material combat-brief ambiguity is resolved or explicitly delegated.

## Case 1 — Yuen Woo-ping profile is not martial-art style
Input:
“生成一段10秒明代庭院打斗，红衣男子和蓝衣男子，徒手，袁和平武侠电影风格。”

Resolved:
- duration,
- participants,
- unarmed,
- environment,
- named action-cinema profile.

Still UNKNOWN unless prior context resolves/delegates them:
- base combat identity,
- reality level if “武侠” is not specific enough to distinguish grounded vs qinggong,
- fight relationship / ending intent.

Expected:
- ask one compact clarification containing only unresolved blocking points,
- do not generate choreography yet,
- do not build/load Style leaves yet,
- do not infer Northern Long Fist from “袁和平”.

## Case 2 — Explicit delegation passes gate
Input:
“10秒，明代庭院，红蓝两名男子徒手，袁和平动作设计。武术流派、谁先攻和结局你自己定，偏写实武侠，不要明显轻功。”

Expected:
- duration RESOLVED,
- participants RESOLVED,
- weapons RESOLVED,
- environment RESOLVED,
- base combat identity DELEGATED,
- reality level RESOLVED,
- relationship/ending DELEGATED,
- gate passes,
- proceed to router and choose smallest coherent assumptions.

## Case 3 — Do not re-ask known facts
Input:
“15秒，一对一，仓库，双方徒手，散打对泰拳，写实，蓝方先攻，最后红方险胜。”

Expected:
- all blocking fields resolved,
- no clarification,
- do not ask costume color, lens, exact cut count or exact number of strikes.

## Case 4 — Weapon ambiguity blocks
Input:
“10秒古代客栈，两人打斗，咏春风格，写实武侠，最后平手。”

If weapon state is not otherwise known:
Expected:
- ask whether this is unarmed or armed,
- do not draft fight prompt before answer/delegation.

## Case 5 — Generic combat identity blocks
Input:
“10秒街头，两名男子徒手格斗，写实，一方最后获胜。”

Expected:
- “格斗” is too broad if style materially matters,
- ask which system/style or whether the director should choose,
- also ask which side wins/initiates only if not already resolvable/delegated.

## Case 6 — Generic model name is not mandatory
Input:
“10秒，1v1，现代停车场，拳击，徒手写实，红方先攻最后蓝方反杀，给我视频提示词。”

Expected:
- gate passes without asking which video model,
- generic natural-language prompt is acceptable,
- ask target model only if user requests model-specific formatting or the model materially changes syntax/structure.

## Case 7 — Minor cinematography detail must not block
Input:
“10秒，明代庭院，红蓝男子徒手，八极对长拳，写实武侠，红先攻，不分胜负。”

Expected:
- gate passes,
- do not ask focal length, cut count, courtyard dimensions, robe fabric or exact camera height,
- director chooses those later through cinematic composition.

## Case 8 — User says ‘直接做’ after clarification
Context:
Assistant asks unresolved combat-style/outcome questions.
User replies:
“这些你自己定，直接做。”

Expected:
- unresolved fields become DELEGATED,
- do not ask again,
- choose smallest coherent assumptions and proceed.

## Case 9 — No provisional prompt while gate fails
Input has at least one UNKNOWN Blocking Core field.

Expected:
- response contains clarification only,
- no “先给你一版临时提示词”,
- no detailed choreography,
- no Style/Profile leaf scan beyond what is required to understand the brief gate.
