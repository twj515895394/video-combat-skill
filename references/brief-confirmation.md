# Combat Brief Confirmation

Use before choreography when missing information would materially change the fight.

The goal is **not** to interrogate the user. Confirm only high-impact unknowns.

## Core fields

Try to resolve:

- duration
- participant count
- armed / unarmed
- environment / usable architecture
- initiator
- combat style(s)
- realism level
- cinematic tone
- outcome / ending state
- generation model or output format when relevant

## Ask only when material

Ask a concise clarification when one of these is genuinely ambiguous and would produce a different choreography:

### A. Combat identity
Examples:
- “中国武术” but the intended movement could be Nanquan, Long Fist, Wing Chun, Baji, etc.
- “格斗” but user may mean boxing, Sanda, Muay Thai, MMA.

### B. Realism level
Examples:
- grounded fight vs heightened wuxia vs fantasy qinggong.

### C. Weapons
If the request could plausibly be armed or unarmed and that changes the entire action design.

### D. Core relationship
Examples:
- who attacks first,
- who is dominant,
- evenly matched vs one-sided,
- 1v1 vs multiple attackers.

### E. Space
If environment interaction is important but location is unknown.

### F. Output target
If the user asks for “prompt” but platform/model format materially changes structure.

## Do not ask when easy to infer

Do not block the workflow for:
- exact costume color unless identity depends on it,
- small prop choices,
- minor camera lens choice,
- exact number of cuts,
- micro-details that can be designed safely.

Infer and proceed.

## Confirmation style

Prefer one compact message containing only the unresolved core points.

Good:
“先确认3个核心点：1）纯徒手还是允许兵器；2）偏写实武打、写实武侠还是高幻想轻功；3）红衣是否必须先攻且最终谁占上风？”

Bad:
20-question production questionnaire.

## If user already supplied the answer

Never ask again.

## If user gives a broad but workable brief

Example:
“10秒，古代武侠，红衣先攻，南拳对北腿，徒手。”

This is enough to proceed.
Do not ask:
- exact courtyard dimensions,
- exact lens,
- exact robe fabric,
unless user requests production-level specificity.

## If ambiguity remains but user asks to proceed

Make the smallest reasonable assumption and state it briefly in the response or internal brief.
