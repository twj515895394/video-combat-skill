# Brief & Archetype Tests

## Case 1 — clear brief, no questions
Input:
"10秒，古代庭院，蓝衣南拳、红衣北腿，纯徒手，红衣先攻，写实武侠。"

Expected:
- do not ask clarification,
- route to wuxia-courtyard or another clearly appropriate archetype,
- proceed.

## Case 2 — ambiguous martial art
Input:
"做10秒中国武术打斗。"

Expected:
Ask only a compact clarification because “中国武术” can materially change choreography:
- preferred style/family or movement character,
- realism vs wuxia if unclear,
- optionally initiator if story depends on it.

Do not ask costume/lens questions.

## Case 3 — ambiguous weapons
Input:
"两个古代高手打10秒。"

Expected:
Clarify whether:
- unarmed or armed,
- grounded martial arts / wuxia / fantasy,
if not inferable.

## Case 4 — pressure fight
Input:
"红衣一路压着蓝衣打，蓝衣不断后退但中间找机会反击。"

Expected:
- archetypes/pressure-duel.md
- appropriate style(s)
- pressure-chains or recovery-failure-chains as needed.

## Case 5 — chase combat
Input:
"两个人沿长廊边跑边打，红衣一直追。"

Expected:
- pursuit-fight.md
- directing lateral/depth movement references as needed.

## Case 6 — equal masters
Input:
"两个高手势均力敌，不要站桩试探，10秒里要逐渐升级。"

Expected:
- peer-duel-escalation.md.

## Case 7 — one-vs-many
Input:
"一个人被三个人围攻，要边打边突围。"

Expected:
- outnumbered.md,
- track each attacker's spatial state,
- do not let all three attack simultaneously without spatial reason.

## Case 8 — environment fight
Input:
"在酒楼里利用桌椅柱子打，撞击有破坏。"

Expected:
- environment-driven.md,
- environment-impact directing reference.

## Case 9 — user says proceed despite ambiguity
Input:
"你自己定，直接做。"

Expected:
- choose minimal reasonable assumptions,
- do not keep questioning,
- proceed and state key assumption briefly if useful.
