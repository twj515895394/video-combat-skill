# Combat Brief Gate

Use **before any routing, reference loading, choreography, shot design or prompt writing**.

This is a generation gate, not a production questionnaire.
The goal is to resolve the few facts that can materially change the fight. If a blocking field is unknown, **stop and ask the user before continuing**.

## 1. Blocking Core — must be resolved

For a normal fight-video prompt, resolve these fields first:

1. **Duration**
   - e.g. 5s / 10s / 15s.

2. **Participants / combat relationship**
   - count,
   - who is fighting whom,
   - any identity/color labels needed to track them.

3. **Weapon state**
   - unarmed,
   - armed and exact weapon class,
   - mixed if intentionally specified.

4. **Environment / fight space**
   - enough to establish usable spatial logic,
   - e.g. Ming courtyard, alley, staircase, warehouse, forest platform.
   - Exact dimensions are not required unless important.

5. **Base combat identity**
   - exact martial art / combat system when the user cares about it,
   - or an explicit user delegation such as “你自己定 / 按场景选 / 自由发挥”.

6. **Physical / cinematic reality level**
   - grounded realistic combat,
   - grounded wuxia,
   - heightened wuxia / qinggong,
   - fantasy / supernatural if explicitly wanted.

7. **Fight relationship / ending intent**
   Resolve enough to know the dramatic direction:
   - who initiates or whether either may initiate,
   - evenly matched vs one side pressuring,
   - ending: unresolved / one side gains advantage / decisive win / escape / interruption,
   - or explicit delegation to the director.

If any of these seven fields is genuinely unknown and not delegated, **do not generate the final fight prompt yet**.

## 2. Conditional fields — ask only when relevant

These are not universal blockers.

### A. Target generation model / prompt format
Ask only when model-specific formatting materially changes the prompt.
Examples:
- MiniMax H3,
- Seedance,
- Veo,
- Kling,
- generic natural-language video prompt.

If the user only asks for a generic prompt, do not block on model name.

### B. Named action-cinema / filmmaker profile
Examples:
- Yuen Woo-ping / 袁和平,
- Tsui Hark / 徐克,
- Sammo Hung / 洪金宝.

A named profile changes choreography/directing treatment, but it is **not a substitute for Base Combat Identity**.

**Hard rule:**
`Named Action Style Profile ≠ Base Combat Style`

Examples:
- “袁和平风格” does **not** mean Northern Long Fist.
- “徐克武侠” does **not** determine Nanquan / Baji / Wing Chun.
- “洪金宝式动作” does **not** determine boxing / kickboxing / Southern fist.

If the user names only a filmmaker/action profile but gives no martial-art identity and has not delegated that choice, ask.

### C. Special must-have / must-avoid constraints
Ask only when ambiguity materially changes composition.
Examples:
- must contain qinggong,
- no aerial movement,
- must use environment,
- no face close-ups,
- protagonist cannot be hit,
- must end on a throw.

## 3. Delegation counts as resolved

The user may explicitly hand a field to the director.
Examples:
- “武术流派你自己定”
- “谁先攻你安排”
- “结局你设计”
- “写实程度按袁和平电影感处理”

Treat explicit delegation as a resolved field.
Choose the smallest coherent assumption and do not ask again.

Do **not** silently treat missing information as delegated.

## 4. Broad but sufficient answers are valid

Do not over-question once the blocking intent is clear.

Examples:

“10秒，明代庭院，红蓝两名男子，徒手，南拳对北腿，写实武侠，红衣先攻，最后不分胜负。”

This is enough.
Do not ask:
- courtyard dimensions,
- exact robe fabric,
- lens focal length,
- exact cut count,
- exact strike count.

Another valid brief:

“10秒，明代庭院，两名男子徒手，袁和平动作设计，武术流派和谁占上风你自己定，写实武侠。”

This is also enough because the uncertain combat fields were explicitly delegated.

## 5. Compact confirmation format

Ask all unresolved blocking points in **one compact message**.
Do not drip-feed one question per turn unless the user's answer creates a new material ambiguity.

Preferred format:

“生成前还差3个核心点：
1）两人的武术流派是什么，还是由我来定？
2）偏写实武打、写实武侠，还是带明显轻功？
3）谁先攻、最后谁占上风，还是不分胜负？”

Keep the wording natural to the user's language.

## 6. Do not ask for already-known facts

Never re-ask a field already supplied in the current request or conversation.

Example:
If the user already said “10秒、明代庭院、红衣蓝衣、徒手、袁和平风格”, do **not** ask duration/environment/weapon state again.
Only ask the unresolved material fields such as Base Combat Identity, reality level or outcome if they were not delegated.

## 7. Pre-generation status

Internally classify each blocking field as:

```yaml
brief_gate:
  duration: RESOLVED | DELEGATED | UNKNOWN
  participants: RESOLVED | DELEGATED | UNKNOWN
  weapons: RESOLVED | DELEGATED | UNKNOWN
  environment: RESOLVED | DELEGATED | UNKNOWN
  base_combat_identity: RESOLVED | DELEGATED | UNKNOWN
  reality_level: RESOLVED | DELEGATED | UNKNOWN
  fight_relationship_ending: RESOLVED | DELEGATED | UNKNOWN
```

Proceed only when no blocking field remains `UNKNOWN`.

## 8. Gate behavior

If `UNKNOWN` exists:
- ask only for the unknown blocking fields,
- do not build the Load Manifest yet,
- do not load Style / Cinematic / Directing / Composer leaves,
- do not draft choreography,
- do not output a provisional fight prompt.

If all blocking fields are `RESOLVED` or `DELEGATED`:
- continue to `reference-router.md`,
- build the Load Manifest,
- compose the fight.
